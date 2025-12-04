---
title: "Blog 1"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

# Các mô hình Open-Weight của OpenAI hiện đã có trên AWS

Các mô hình **open-weight** của OpenAI hiện đã có mặt trên **AWS**, giúp các tổ chức và nhà phát triển có thể tích hợp AI tiên tiến với mức độ linh hoạt, khả năng mở rộng và khả năng kiểm soát cao hơn. Những mô hình này được thiết kế cho **tạo văn bản, lập luận, lập trình và khối lượng công việc khoa học**, hỗ trợ độ dài ngữ cảnh lên đến **128K tokens** và mức độ suy luận có thể điều chỉnh.

Bài viết này trình bày chi tiết về sự ra mắt của các mô hình mới của OpenAI, các quyết định kiến trúc đằng sau việc tích hợp với AWS, và cách để bắt đầu sử dụng thông qua **Amazon Bedrock** và **Amazon SageMaker JumpStart**.

---

## Hướng dẫn kiến trúc

Các mô hình mới — **gpt-oss-120b** và **gpt-oss-20b** — hiện có sẵn thông qua **Amazon Bedrock** và **Amazon SageMaker JumpStart**:  
- **Amazon Bedrock**: Cung cấp khả năng truy cập mô hình dạng serverless, thông qua API `InvokeModel` hoặc `Converse`.  
- **SageMaker JumpStart**: Cho phép tinh chỉnh, triển khai quy mô lớn và tích hợp vào môi trường sản xuất bằng **console** hoặc **Python SDK**.  

**Điểm nổi bật trong kiến trúc giải pháp:**  
- Truy cập mô hình trực tiếp qua endpoint của Bedrock  
- Tùy chọn triển khai quản lý qua SageMaker  
- Hỗ trợ quy trình đa dịch vụ và kiến trúc hướng sự kiện  

---

Mặc dù thuật ngữ *open-weight models* khá rộng, một số đặc điểm chính gồm:  
- Tính linh hoạt cao với các tùy chọn **triển khai tùy chỉnh**  
- **Minh bạch** nhờ dấu vết suy luận để dễ giải thích  
- Thiết kế để tích hợp vào **quy trình hướng sự kiện và agent**  
- Tương thích với **OpenAI SDKs** và các dịch vụ gốc AWS  

Khi lựa chọn phương án triển khai, cần xem xét:  
- **Yếu tố nội tại**: kích thước ngữ cảnh, hiệu năng, chất lượng suy luận  
- **Yếu tố bên ngoài**: khả năng mở rộng, nhu cầu tích hợp, khả năng tái sử dụng  
- **Yếu tố con người**: năng suất lập trình viên, trách nhiệm vận hành  

---

## Lựa chọn công nghệ và phạm vi tích hợp

| Phạm vi tích hợp               | Dịch vụ / Mẫu hình AWS đề xuất                               |
| ------------------------------ | ------------------------------------------------------------ |
| Truy cập & kiểm thử mô hình    | Amazon Bedrock (chat playground, APIs)                      |
| Tinh chỉnh & triển khai        | Amazon SageMaker JumpStart                                   |
| Quy trình hướng sự kiện        | Amazon EventBridge, AWS Lambda, Bedrock AgentCore            |
| AI agent tăng cường công cụ    | Strands Agents với các mô hình tích hợp qua Bedrock          |

---

## So sánh với mô hình Hub-and-Spoke

Tương tự như **pub/sub hub** trong microservices, AWS hỗ trợ mô hình hub-and-spoke cho AI:  
- Mô hình được truy cập qua **endpoint của Bedrock**  
- Tương tác tiêu chuẩn hóa thông qua **API tương thích OpenAI**  
- Lập trình viên có thể chuyển đổi giữa các mô hình nền tảng mà không cần viết lại logic ứng dụng  

**Điểm cần lưu ý:** cần có **phối hợp và giám sát cẩn thận** để quản lý nhiều mô hình và mức suy luận khác nhau.  

---

## Truy cập mô hình cốt lõi

Nền tảng để sử dụng mô hình OpenAI trên AWS bao gồm:  
- **Amazon Bedrock** cho suy luận dạng serverless  
- **Amazon SageMaker JumpStart** để triển khai quản lý và tinh chỉnh  
- **Tích hợp OpenAI SDK** để dễ dàng sử dụng  
- **Hỗ trợ dấu vết suy luận** nhằm tăng tính minh bạch  

> Các mô hình này đã sẵn sàng cho môi trường sản xuất và được tối ưu để tích hợp với các khối lượng công việc hiện có trên AWS.  

---

## Điểm truy cập cho nhà phát triển

- Truy cập mô hình qua **Bedrock console**: yêu cầu quyền truy cập mô hình và bắt đầu thử nghiệm trong playground  
- Xác thực thông qua **AWS IAM policies**  
- Sử dụng **OpenAI SDK** bằng cách trỏ `OPENAI_BASE_URL` đến endpoint runtime của Bedrock  

**Ví dụ Python:**

```python
from openai import OpenAI

client = OpenAI()

response = client.chat.completions.create(
  messages=[{"role": "user", "content": "Tính căn bậc hai của 42 ^ 3"}],
  model="openai.gpt-oss-120b-1:0",
  stream=True
)

for item in response:
    print(item)
