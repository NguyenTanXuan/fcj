---
title: "Worklog Tuần 6"
date: "`r Sys.Date()`"
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu Tuần 6:

* Triển khai và kiểm thử các API backend cho website thương mại điện tử bán quần áo.  
* Tích hợp AWS S3 để lưu trữ file và quản lý hình ảnh sản phẩm.  
* Thiết lập pipeline CI/CD cho quy trình triển khai tự động.

### Các nhiệm vụ cần thực hiện trong tuần:

| Ngày | Nhiệm vụ                                                                                                                                                                                        | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo                      |
| ---- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ---------------- | ---------------------------------------- |
| 1    | - Triển khai API CRUD cho sản phẩm <br> - Kiểm thử API bằng Postman hoặc Insomnia <br> - Validate dữ liệu request/response                                                                     | 13/10/2025   | 13/10/2025       | Tài liệu Spring Boot                     |
| 2    | - Tạo AWS S3 bucket cho hình ảnh sản phẩm <br> - Cấu hình bucket policies và CORS <br> - Triển khai chức năng upload/download hình ảnh                                                         | 14/10/2025   | 14/10/2025       | Tài liệu AWS S3                          |
| 3    | - Tích hợp upload file trong chức năng tạo sản phẩm <br> - Xử lý resize và tối ưu hình ảnh <br> - Kiểm thử toàn bộ quy trình upload hình                                                       | 15/10/2025   | 15/10/2025       | ImageIO, AWS SDK Documentation           |
| 4    | - Thiết lập GitHub Actions cho CI/CD <br> - Cấu hình automated testing <br> - Tạo workflow triển khai tự động                                                                                 | 16/10/2025   | 16/10/2025       | Tài liệu GitHub Actions                  |
| 5    | - Triển khai ứng dụng lên AWS EC2 <br> - Cấu hình load balancer và auto-scaling <br> - Thiết lập giám sát bằng CloudWatch                                                                      | 17/10/2025   | 17/10/2025       | Tài liệu AWS EC2, CloudWatch             |

### Kết quả đạt được trong Tuần 6:

* Hoàn thành triển khai đầy đủ các chức năng CRUD cho quản lý sản phẩm.  
* Tích hợp AWS S3 để lưu trữ hình ảnh an toàn và mở rộng.  
* Cấu hình chính sách bucket để đảm bảo truy cập bảo mật.  
* Xây dựng pipeline CI/CD tự động bằng GitHub Actions.  
* Triển khai ứng dụng lên AWS EC2 với giám sát đầy đủ.  
* Thực hiện tối ưu hóa hình ảnh giúp cải thiện hiệu năng hệ thống.  
* Thiết lập automated testing để đảm bảo chất lượng mã nguồn.  
* Cấu hình CloudWatch để giám sát và cảnh báo hoạt động của ứng dụng.
