---
title: "Worklog Tuần 7"
date: "`r Sys.Date()`"
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu Tuần 7:

* Nâng cấp hệ thống thương mại điện tử với chức năng xác thực và phân quyền người dùng.  
* Triển khai chức năng giỏ hàng và quản lý đơn hàng.  
* Thiết lập tối ưu hóa và bảo mật cơ sở dữ liệu.

### Các nhiệm vụ cần thực hiện trong tuần:

| Ngày | Nhiệm vụ                                                                                                                                                                                        | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo                        |
| ---- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ---------------- | ------------------------------------------ |
| 1    | - Triển khai hệ thống xác thực dựa trên JWT <br> - Tạo API đăng ký và đăng nhập người dùng <br> - Thiết lập mã hóa và kiểm tra mật khẩu                                                        | 20/10/2025   | 20/10/2025       | Tài liệu Spring Security                   |
| 2    | - Thiết kế và triển khai phân quyền theo vai trò <br> - Tạo role admin và khách hàng <br> - Bảo mật các API bằng cơ chế authorization phù hợp                                                   | 21/10/2025   | 21/10/2025       | Spring Security, JWT Documentation         |
| 3    | - Triển khai chức năng giỏ hàng <br> - Tạo session quản lý giỏ hàng <br> - Xử lý thêm / xóa / cập nhật sản phẩm trong giỏ                                                                          | 22/10/2025   | 22/10/2025       | Redis, Spring Session Documentation        |
| 4    | - Xây dựng hệ thống quản lý đơn hàng <br> - Tạo chức năng đặt hàng và theo dõi đơn hàng <br> - Triển khai quy trình xử lý trạng thái đơn hàng                                                    | 23/10/2025   | 23/10/2025       | Spring Boot, JPA Documentation             |
| 5    | - Thiết lập AWS RDS cho môi trường production <br> - Cấu hình security groups cho cơ sở dữ liệu <br> - Triển khai backup và giám sát cơ sở dữ liệu                                              | 24/10/2025   | 24/10/2025       | AWS RDS, CloudWatch Documentation          |

### Kết quả đạt được trong Tuần 7:

* Triển khai thành công hệ thống xác thực dựa trên JWT với cơ chế quản lý token an toàn.  
* Xây dựng hệ thống phân quyền theo vai trò đầy đủ cho từng loại người dùng.  
* Tạo hệ thống giỏ hàng hiệu quả với session management.  
* Phát triển hoàn chỉnh quy trình quản lý đơn hàng từ đặt hàng đến xử lý.  
* Di chuyển cơ sở dữ liệu sang AWS RDS với cấu hình bảo mật phù hợp.  
* Triển khai chiến lược backup tự động để bảo vệ dữ liệu.  
* Thiết lập giám sát và cảnh báo cơ sở dữ liệu qua CloudWatch.  
* Tăng cường bảo mật API thông qua các lớp xác thực và phân quyền chặt chẽ.
