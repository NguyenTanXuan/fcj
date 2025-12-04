---
title: "Worklog Tuần 4"
date: "`r Sys.Date()`"
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---


### Mục tiêu tuần 4:

* Làm quen với các thành viên trong nhóm và thảo luận hướng phát triển tổng thể của dự án **web bán quần áo**.  
* Tìm hiểu cấu trúc backend, công nghệ sử dụng và phân chia vai trò trong nhóm.  
* Bắt đầu tìm hiểu cách **tích hợp các dịch vụ AWS** (như S3, EC2, RDS) vào hệ thống backend.

---

### Nhiệm vụ thực hiện trong tuần:
| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | -------- | ------------- | ---------------- | ------------------ |
| 2 | - Gặp gỡ các thành viên trong nhóm và trao đổi về tổng quan dự án <br> - Xác định vai trò chính của từng người (Backend, Frontend, UI/UX, v.v.) | 29/09/2025 | 29/09/2025 | Ghi chú cuộc họp nhóm |
| 3 | - Khám phá cấu trúc backend của dự án (Spring Boot) <br> - Thiết lập môi trường phát triển cục bộ <br> - Tìm hiểu cấu trúc API và cơ sở dữ liệu hiện tại | 30/09/2025 | 30/09/2025 | Kho lưu trữ GitHub nội bộ |
| 4 | - Nghiên cứu các dịch vụ AWS có thể tích hợp vào hệ thống <br>&emsp; + AWS S3 để lưu trữ hình ảnh sản phẩm <br>&emsp; + AWS RDS để lưu trữ cơ sở dữ liệu <br>&emsp; + AWS EC2 để triển khai backend | 01/10/2025 | 01/10/2025 | [Tài liệu AWS](https://aws.amazon.com/documentation/) |
| 5 | - Thảo luận chiến lược triển khai với nhóm <br> - Lên kế hoạch các API liên quan đến quản lý sản phẩm (CRUD cho quần áo) | 02/10/2025 | 02/10/2025 | Tài liệu nội bộ |
| 6 | - Bắt đầu thiết kế và lập trình các API <br>&emsp; + Danh sách sản phẩm <br>&emsp; + Quản lý danh mục <br>&emsp; + Thử nghiệm upload ảnh với AWS S3 | 03/10/2025 | 03/10/2025 | Tài liệu Spring Boot |

---

### Kết quả đạt được trong tuần:

* Đã kết nối và trao đổi hiệu quả với các thành viên trong nhóm, hiểu rõ mục tiêu và quy trình làm việc của dự án.  
* Xác định rõ **vai trò backend** và thiết lập thành công môi trường làm việc cục bộ.  
* Nắm được cấu trúc tổng thể của **website bán quần áo**, bao gồm cơ sở dữ liệu, tầng dịch vụ và luồng API.  
* Tìm hiểu và đánh giá khả năng tích hợp các dịch vụ AWS:  
  * **AWS S3** — dùng để lưu trữ hình ảnh sản phẩm.  
  * **AWS RDS** — dùng để lưu trữ cơ sở dữ liệu MySQL.  
  * **AWS EC2** — dùng cho triển khai backend sau này.  
* Đóng góp vào việc thiết kế các API liên quan đến sản phẩm (CRUD).  
* Đã thực hiện thử nghiệm thành công việc upload và truy xuất ảnh bằng **AWS S3**.  
* Củng cố thêm kiến thức về quy trình phát triển backend và tích hợp AWS trong ứng dụng web thực tế.

---
