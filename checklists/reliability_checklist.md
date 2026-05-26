# Reliability Checklist - Analytics Service

| Tiêu chí | Đạt? | Chú thích |
|---|---|---|
| **1. Trạng thái HTTP chuẩn xác** | [x] | Các test case assert rõ ràng status code (200, 201, 400, 401, v.v.). |
| **2. Auth Validation** | [x] | Client sẽ nhận 401 nếu gọi thiếu token (có test case đi kèm). |
| **3. Negative Payload Handling** | [x] | POST request thiếu field bắt buộc sẽ nhận lỗi client (400/422 + ProblemDetails format). |
| **4. Rate Limiting** | [x] | Boundary test chấp nhận 429 nếu gọi dồn dập (Mock/Local). |
| **5. Phụ thuộc (Consumer-side Test)**| [x] | Core Business service mock call được verify ở collection. |
| **6. Non-Functional Latency** | [x] | Kiểm tra dưới 1s cho endpoint /health trên môi trường Local. |
