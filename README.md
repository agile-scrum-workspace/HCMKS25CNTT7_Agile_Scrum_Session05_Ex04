# PHÂN TÍCH ƯU TIÊN HÓA PRODUCT BACKLOG BẰNG MoSCoW CHO SPRINT TIẾP THEO (RIKKEIGO)

**Bối cảnh:** Phát hành bản mới cho chương trình "Tháng khuyến mãi" | **Năng lực Sprint (Velocity):** 10 Story Points (SP).

---

## Phần 1: Đề xuất 2 cách tiếp cận gán nhãn MoSCoW

* **Cách 1: Gán nhãn theo Nguyện vọng các bên liên quan (Stakeholder-Driven Prioritization):**  
  Xếp hạng mục dựa trên mức độ yêu cầu cấp thiết từ các phòng ban chức năng (Marketing, CSKH, Vận hành), coi trọng cam kết hình ảnh và trải nghiệm tương tác trực tiếp của từng bộ phận.
* **Cách 2: Gán nhãn theo Phép thử Nghiệp vụ tối thiểu & Giải pháp thay thế (Workaround & Viability Test):**  
  Dựa trên bản chất kỹ thuật và giá trị cốt lõi của bản phát hành: Một hạng mục chỉ là **Must** nếu thiếu nó hệ thống bị lỗi nghiêm trọng hoặc chiến dịch không thể hoạt động được; nếu đã có cách xử lý tạm thời (workaround) hoặc thiếu vẫn chạy được thì tối đa chỉ là **Should** hoặc **Could**.

---

## Phần 2: So sánh 2 cách gán nhãn

| Tiêu chí so sánh | Cách 1: Theo nguyện vọng bên liên quan | Cách 2: Theo phép thử nghiệp vụ & giải pháp thay thế |
| :--- | :--- | :--- |
| **1. Tính khách quan khi nhiều bên cùng đề xuất** | **(–)** Dễ dẫn đến tranh chấp quyền lực và cảm tính; ai có tiếng nói lớn hơn sẽ giành ưu tiên, gây lạm phát nhãn "Must". | **(+)** Minh bạch, có căn cứ rõ ràng bằng tiêu chí logic: kiểm tra xem có giải pháp thay thế tạm thời không để hạ nhãn thuyết phục. |
| **2. Khả năng bảo vệ hạng mục bắt buộc (#1 - Sửa lỗi tính tiền)** | **(–)** Rủi ro cao bị đẩy xuống do các bên thường mải mê tính năng mới/trang trí bề nổi mà xem nhẹ lỗi kỹ thuật nền tảng. | **(+)** Bảo vệ tuyệt đối; lỗi sai tiền là rủi ro pháp lý/tài chính cốt lõi, không có giải pháp thay thế nên bắt buộc phải đứng đầu. |

---

## Phần 3: Áp dụng lựa chọn và Chốt danh sách Sprint

**Lựa chọn:** Áp dụng **Cách 2 (Phép thử nghiệp vụ & giải pháp thay thế)** để đảm bảo tính khách quan và an toàn hệ thống.

### 1. Phân loại MoSCoW cho 6 hạng mục

1. **#1 - Sửa lỗi hiển thị sai cước sau khuyến mãi (2 SP) – [MUST]:** Thu sai tiền gây mất uy tín và rủi ro pháp lý, hoàn toàn không có cách xử lý tạm thời thay thế.
2. **#2 - Áp mã khuyến mãi khi đặt xe (2 SP) – [MUST]:** Là tính năng cốt lõi bắt buộc phải có để khởi chạy chiến dịch "Tháng khuyến mãi" cho khách.
3. **#3 - Thanh toán bằng ví RikkeiPay (3 SP) – [SHOULD]:** Quan trọng để thúc đẩy thanh toán không tiền mặt, nhưng khách vẫn có thể trả bằng tiền mặt nếu hoãn sang Sprint sau.
4. **#4 - Hẹn giờ đặt xe trước (3 SP) – [WON'T]:** Tính năng tiện ích riêng lẻ, chưa cấp thiết cho mục tiêu chạy chiến dịch khuyến mãi của Sprint này (chuyển sang Backlog sau).
5. **#5 - Chat với tài xế (3 SP) – [COULD]:** Tiện ích phụ, khách và tài xế vẫn có thể liên lạc trực tiếp qua cuộc gọi thông thường (đã có Workaround).
6. **#6 - Giao diện trang trí cho chương trình (2 SP) – [COULD]:** Thiếu banner trang trí thì hệ thống và khuyến mãi vẫn hoạt động trơn tru bình thường; có thể bổ sung nếu dư năng lực.

---

### 2. Chốt phạm vi đưa vào Sprint (Capacity: 10 SP)

| Thứ tự | Hạng mục | Nhãn MoSCoW | Điểm (SP) | Trạng thái đưa vào Sprint |
| :---: | :--- | :---: | :---: | :---: |
| 1 | #1. Sửa lỗi hiển thị sai cước sau khuyến mãi | **Must** | 2 | **Đưa vào Sprint** |
| 2 | #2. Áp mã khuyến mãi khi đặt xe | **Must** | 2 | **Đưa vào Sprint** |
| 3 | #3. Thanh toán bằng ví RikkeiPay | **Should** | 3 | **Đưa vào Sprint** |
| 4 | #6. Giao diện trang trí cho chương trình | **Could** | 2 | **Đưa vào Sprint** |
| 5 | #5. Chat với tài xế | **Could** | 3 | *Dự phòng ngoài Sprint (Cắt giảm)* |
| 6 | #4. Hẹn giờ đặt xe trước | **Won't** | 3 | *Không đưa vào Sprint này (Báo PO/Stakeholders)* |

* **Tổng điểm cam kết trong Sprint:** $2 + 2 + 3 + 2 = \mathbf{9\text{ SP}}$ (nằm an toàn trong trần năng lực 10 SP, chừa 1 SP đệm rủi ro phát sinh).
* **Tỷ lệ hạng mục Must:**  
  $$\text{Tỷ lệ Must} = \frac{2 + 2}{9} \approx 44.4\% \quad (\text{hoặc } \frac{4}{10} = 40\% \text{ tổng năng lực})$$
* **Đánh giá tỷ lệ:** Đảm bảo dưới ngưỡng an toàn 60%, giúp đội phát triển có độ co giãn linh hoạt (khoảng 55% còn lại dành cho Should/Could) để sẵn sàng cắt tỉa nếu Sprint gặp trở ngại kỹ thuật.