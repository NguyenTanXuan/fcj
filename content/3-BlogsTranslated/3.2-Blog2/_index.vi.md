---
title: "Blog 2"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: " <b> 3.2. </b> "
---
# AWS CHO SAP

## Giới thiệu

Việc dịch chuyển hệ thống SAP lên AWS mang lại cho doanh nghiệp cơ hội hiện đại hóa hạ tầng và tận dụng khả năng co giãn linh hoạt của điện toán đám mây. Doanh nghiệp có thể mở rộng tài nguyên (compute, memory, storage) chỉ trong vài phút và tự động hóa quy trình cấp phát để giảm lỗi vận hành.

Tuy nhiên, việc áp dụng auto scaling cho SAP Application Servers lại phức tạp hơn. Truyền thống, các tổ chức phải cấp phát dư tài nguyên để tránh chậm hệ thống trong giờ cao điểm — dẫn đến trả chi phí cho mức tải tối đa ngay cả khi không cần thiết.

Các dịch vụ AWS như Auto Scaling groups, Target Groups và Launch Templates không hoàn toàn phù hợp với kiến trúc SAP. Để giải quyết vấn đề này, AWS Professional Services phát triển **SAP Auto Scaling solution**, hỗ trợ mở rộng ngang SAP Application Servers và giảm chi phí hạ tầng tới **50%**.

---

## Bài toán kinh doanh cho Auto Scaling

Giải pháp SAP Auto Scaling được xây dựng nhằm giải quyết các thách thức vận hành thực tế, bao gồm:

- Đảm bảo môi trường SAP tự động điều chỉnh theo tải — mở rộng khi tải cao, thu hẹp khi tải giảm.
- Cho phép quản trị viên chủ động bật/tắt máy chủ trong quá trình bảo trì hoặc nâng cấp.
- Giảm chi phí vận hành bằng việc tự động hóa các tác vụ hạ tầng định kỳ.

Giải pháp đặc biệt phù hợp cho doanh nghiệp:

- Có chu kỳ hoạt động không đồng đều (giảm tải vào buổi tối hoặc cuối tuần).
- Muốn tối ưu chi phí EC2 vào giờ thấp điểm.
- Vận hành môi trường Production với **từ 3 SAP Application Servers trở lên**.
- Ưu tiên mô hình chi phí linh hoạt, không cam kết dài hạn.

### Lợi ích chính

- Hiện đại hóa môi trường SAP bằng khả năng co giãn gốc của đám mây.
- Tiết kiệm tới **50%** chi phí EC2 so với chạy On-Demand liên tục.
- Mở rộng hiệu quả theo quy luật tải thực tế của doanh nghiệp.

---

## Cách giải pháp hoạt động

SAP Auto Scaling tự động quản lý trạng thái bật/tắt của SAP Application Servers. Hệ thống liên tục theo dõi mức sử dụng **Dialog Work Processes** trên máy chủ ASCS (ABAP SAP Central Services) để quyết định thời điểm scale up/down.

### Chức năng cốt lõi

- Khi tải tăng, hệ thống kích hoạt một EC2 instance đã cấu hình sẵn và tự động khởi chạy dịch vụ SAP.
- Các quyết định scale chỉ dựa trên mức tiêu thụ Dialog Work Processes của ASCS.
- Trước khi scale down, người dùng SAP GUI nhận được thông báo pop-up để lưu công việc và đăng nhập lại.
- SAP Soft Shutdown đảm bảo batch jobs hoàn tất trước khi tắt máy chủ.
- Có thể thiết lập lịch bật của Application Servers.
- Cho phép định nghĩa “khung giờ không scale” trong giờ vận hành quan trọng.
- Máy chủ quan trọng có thể được đánh dấu “luôn bật”.
- Gửi email thông báo mỗi khi có sự kiện scaling.

---

## Cây quyết định Scale-Up

Hệ thống tuân theo một luồng logic có cấu trúc để quyết định có thực hiện scale up hay không. Một luồng tương tự cũng được dùng cho scale down.
