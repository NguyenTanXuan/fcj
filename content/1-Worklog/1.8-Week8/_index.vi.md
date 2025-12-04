---
title: "Worklog tuần 8"
date: "`r Sys.Date()`"
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu Tuần 8:

* Tích hợp hệ thống thanh toán và xử lý đơn hàng.
* Thiết lập dịch vụ gửi email thông báo và các tính năng thời gian thực.
* Tối ưu hiệu năng ứng dụng và áp dụng chiến lược caching.

### Các công việc thực hiện trong tuần:
| Ngày | Công việc                                                                                                                                                                                               | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo                         |
| --- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ---------------- | ------------------------------------------- |
| 1   | - Tích hợp cổng thanh toán (Stripe/PayPal) <br> - Triển khai xử lý thanh toán an toàn <br> - Xử lý các trường hợp xác nhận và thất bại thanh toán                                                       | 27/10/2025   | 27/10/2025       | Stripe API, PayPal SDK Documentation       |
| 2   | - Thiết lập AWS SES cho email thông báo <br> - Tạo template email cho đơn hàng <br> - Gửi email xác nhận đơn hàng                                                 | 28/10/2025   | 28/10/2025       | AWS SES Documentation                      |
| 3   | - Triển khai thông báo thời gian thực bằng WebSocket <br> - Cập nhật trạng thái đơn hàng theo thời gian thực <br> - Xây dựng hệ thống thông báo cho admin                                               | 29/10/2025   | 29/10/2025       | WebSocket, Spring WebSocket Documentation  |
| 4   | - Thiết lập Redis để caching <br> - Triển khai caching cho danh mục sản phẩm <br> - Thêm caching cho session để tăng hiệu năng                                     | 30/10/2025   | 30/10/2025       | Redis, Spring Cache Documentation          |
| 5   | - Tối ưu các truy vấn database <br> - Triển khai phân trang và lọc dữ liệu <br> - Tạo chức năng tìm kiếm sử dụng Elasticsearch                                   | 31/10/2025   | 31/10/2025       | JPA, Elasticsearch Documentation           |

### Thành tựu Tuần 8:

* Tích hợp thành công hệ thống thanh toán an toàn với nhiều phương thức khác nhau.
* Xây dựng hệ thống gửi email thông báo hoàn chỉnh sử dụng AWS SES.
* Phát triển hệ thống thông báo thời gian thực giúp cải thiện trải nghiệm người dùng.
* Thiết lập Redis caching giúp hiệu năng ứng dụng cải thiện rõ rệt.
* Tối ưu hóa truy vấn cơ sở dữ liệu và triển khai chức năng tìm kiếm hiệu quả.
* Tạo cơ chế xử lý lỗi mạnh mẽ cho quá trình thanh toán và xử lý đơn hàng.
* Nâng cấp khả năng mở rộng hệ thống bằng chiến lược caching thích hợp.
* Triển khai hệ thống giám sát giao dịch thanh toán và hiệu năng hệ thống.
