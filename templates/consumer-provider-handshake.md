# Consumer - Provider Handshake Agreement

## 1. Thành phần tham gia
- **Provider:** Core Business (`team-core`)
- **Consumer:** Analytics Service (`team-analytics`)

## 2. API Contract Thỏa thuận
Analytics sử dụng API Alert creation hoặc kiểm tra Health từ Core Business. 
Để phục vụ Smoke Test, Analytics kỳ vọng:
- GET `/health` của Core Business mock luôn sinh ra status hợp lệ `02_Auth` / `05_Consumer_side_Smoke` test (collection).
- Trả về JSON bao gồm `status`.

## 3. SLA Đề xuất
- **Phản hồi:** < 1000ms.
- **Tính khả dụng:** 99.9%.

**Bên Analytics xác nhận (Consumer):** ✔ Đã implement mock request test.
**Bên Core Business xác nhận (Provider):** ✔ Đã có openapi hợp lệ.
