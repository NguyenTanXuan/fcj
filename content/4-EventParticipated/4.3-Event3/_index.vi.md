---
title: "Event 2"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: " <b> 4.3 </b> "
---

# Bài thu hoạch: Chuỗi AWS Cloud Mastery #3 — Trụ cột Bảo mật AWS Well-Architected

## 1. Mục đích sự kiện
- Giới thiệu vai trò của Trụ cột Bảo mật (Security Pillar) trong Khung kiến trúc AWS Well-Architected.
- Trình bày 5 lĩnh vực của bảo mật: IAM, Phát hiện, Bảo vệ cơ sở hạ tầng, Bảo vệ dữ liệu, Ứng phó sự cố.
- Cung cấp các phương pháp hay nhất (best practices) và kịch bản thực tế để bảo vệ ứng dụng trong môi trường Đám mây.

## 2. Nội dung chính

### Trụ cột 1 — Quản lý Danh tính & Truy cập (IAM)
- Nguyên tắc: Đặc quyền tối thiểu (Least Privilege), Zero Trust, Phòng thủ chiều sâu (Defense in Depth).
- IAM hiện đại: Tránh thông tin xác thực dài hạn, ưu tiên IAM Roles và các chính sách được quản lý (managed policies).
- IAM Identity Center: SSO, Bộ quyền (Permission Sets), quản lý truy cập tập trung.
- Bảo mật đa tài khoản: Service Control Policies (SCP) và Ranh giới quyền (Permission Boundaries).
- Demo nhỏ: Kiểm tra chính sách IAM và mô phỏng hành vi truy cập.

### Trụ cột 2 — Phát hiện (Detection)
- Giám sát liên tục với CloudTrail (cấp tổ chức), GuardDuty, Security Hub.
- Ghi nhật ký đa tầng: VPC Flow Logs, nhật ký ALB, nhật ký truy cập S3.
- Cảnh báo tự động qua Amazon EventBridge.

### Trụ cột 3 — Bảo vệ cơ sở hạ tầng
- Bảo mật mạng: phân tách mạng (VPC public/private).
- Cơ chế phòng thủ: Security Groups so với NACLs, AWS WAF, Shield, Network Firewall.
- Bảo mật khối lượng công việc (Workload): EC2, ECS/EKS ở mức cơ bản.

### Trụ cột 4 — Bảo vệ dữ liệu
- Mã hóa dữ liệu khi lưu trữ (at-rest) và khi truyền tải (in-transit) (S3, EBS, RDS, DynamoDB).
- KMS để quản lý khóa; Secrets Manager và Parameter Store để quản lý bí mật (secrets).
- Phân loại dữ liệu và thiết lập các rào chắn (guardrails) truy cập.

### Trụ cột 5 — Ứng phó sự cố (Incident Response)
- Vòng đời Ứng phó sự cố theo AWS.
- Xây dựng kịch bản ứng phó (IR playbook) và tự động hóa với Lambda/Step Functions.
- Kịch bản mẫu: lộ khóa IAM, lộ S3 ra công cộng, phát hiện phần mềm độc hại trên EC2.

## 3. Bài học rút ra
- Hiểu về 5 lĩnh vực của Trụ cột Bảo mật và Mô hình Trách nhiệm Chia sẻ.
- Áp dụng IAM nâng cao: Identity Center, SCPs, tránh sử dụng thông tin xác thực dài hạn.
- Hiểu tầm quan trọng của Bảo mật Dữ liệu: KMS, quản lý bí mật.
- Biết cách xây dựng và tự động hóa Quy trình Ứng phó sự cố thông qua các quy trình serverless.

## 4. Trải nghiệm sự kiện
- Workshop tổng hợp chuỗi kiến thức, củng cố nền tảng bảo mật trước khi hoàn thiện dự án.
- Phần IAM Identity Center và Secrets Manager giải quyết trực tiếp vấn đề xác thực và quản lý khóa API của nhóm.
- Các kịch bản IR (như lộ S3) giúp củng cố chính sách bảo mật cho dự án.
- Phiên hỏi đáp hướng dẫn thêm về lộ trình chứng chỉ AWS Security Specialty.