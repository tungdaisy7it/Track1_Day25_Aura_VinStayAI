# QUÁ TRÌNH LÀM VIỆC CÁ NHÂN & TỔNG HỢP NHÓM (INDIVIDUAL TO TEAM WORKFLOW)
**Track 1 - Day 25: AI Team Lab**  
**Team: Aura** • **Dự án: VinStay AI**

---

Tài liệu này ghi lại chi tiết các bước làm việc độc lập của từng cá nhân (**Cá nhân → Team** và **Team → Cá nhân → Team**) trước khi thống nhất vào sản phẩm đầu ra chính thức (**Day25_AI-Team-Lab_TeamAura.pdf**) theo đúng yêu cầu phương pháp luận của bài học.

---

## 1. PHASE 1: LIỆT KÊ STAKEHOLDER ĐỘC LẬP (CÁ NHÂN → TEAM)
*Mỗi thành viên tự liệt kê độc lập ít nhất 6 stakeholder cụ thể trước khi nhóm họp để loại trùng và xếp lên ma trận Influence × Interest.*

### 👤 Thành viên 1: Nguyễn Khánh Duy (Lead / AI Product)
1. **Ban Quản lý Vinhomes Ocean Park (BQL):** Kiểm soát an ninh thang máy, quy chế sử dụng sảnh và phòng cháy chữa cháy.
2. **Hội đồng Thẩm định & Giảng viên AI20K (VinUni):** Chấm điểm Demo Day, tài trợ GPU compute và định hướng kiến trúc Agent.
3. **Chủ nhà nhóm Tiên phong (20 căn hộ Sapphire 1 & 2):** Cung cấp giỏ hàng thực tế để chạy thử nghiệm matching agent.
4. **Đội ngũ Field Host nội khu:** Sinh viên VinUni nhận ca dẫn khách qua sảnh an ninh bằng thẻ cư dân hợp chuẩn.
5. **Đơn vị cung cấp giải pháp Smart Lock / Cổng thanh toán VietQR:** Đối tác tích hợp API khóa và thanh toán cọc.
6. **Môi giới truyền thống tại Ocean Park:** Bên có thể phản đối do bị cạnh tranh nguồn phí hoa hồng cho thuê.

### 👤 Thành viên 2: Lê Thanh Tùng (Fullstack / Field Operations)
1. **Khách thuê trẻ (Sinh viên VinUni & Chuyên gia TechnoPark):** Người trực tiếp trải nghiệm duyệt phòng và đặt cọc qua Web App.
2. **Bảo vệ sảnh & Lễ tân các tòa Sapphire (S1.02, S1.08, S2.05):** Người giám sát trực tiếp khách ra vào sảnh và thang máy.
3. **Đội thợ kỹ thuật & sửa chữa điện nước Ocean Park:** Nhận xử lý sự cố thiết bị căn hộ theo mô hình biến phí Asset-Light.
4. **Chủ nhà ở xa (Hà Nội / Ngoại tỉnh):** Cần hệ thống theo dõi lịch mở cửa và báo cáo tài chính căn hộ từ xa 100%.
5. **Cửa hàng tiện lợi / Quán cafe nội khu (Highlands sảnh S2):** Điểm hỗ trợ khách chờ trong tình huống Field Host gặp sự cố trễ.
6. **Cư dân lân cận tại tầng căn hộ:** Bên có thể phản ánh nếu khách thuê gây ồn ào hoặc mất trật tự an ninh.

### 👤 Thành viên 3: Cao Đức Hiệp (Backend & Data / AI Engineer)
1. **Công an khu vực / Cảnh sát khu vực Gia Lâm:** Đơn vị tiếp nhận thủ tục khai báo tạm trú cho khách thuê căn hộ.
2. **Khách thuê lo ngại rủi ro bảo mật dữ liệu CCCD:** Cần giải pháp Zero-Storage OCR tiêu hủy ảnh ngay sau bóc tách.
3. **Đơn vị cung cấp dịch vụ hạ tầng Cloud & LLM API (OpenAI/Anthropic):** Đảm bảo SLA uptime và độ trễ phản hồi < 2s.
4. **20 Chủ nhà gửi độc quyền căn hộ:** Cung cấp thông tin chi tiết về giá trần, nội thất và quy chế căn hộ để nạp vào DB.
5. **Mentor công nghệ AI20K:** Đánh giá độ tin cậy của Matching Agent và bộ kiểm thử Eval 50 golden cases.
6. **Mạng lưới Field Host dự phòng:** Đảm bảo tỷ lệ sẵn sàng nhận ca trong vòng 3 phút khi có phát sinh đột xuất.

👉 **Kết quả gộp nhóm:** Nhóm Aura đã thảo luận, loại bỏ các đối tượng trùng lặp và chốt **6 stakeholder đại diện cốt lõi** cùng **4 stakeholder ưu tiên** đưa vào **Trang 1 của PDF**.

---

## 2. PHASE 2: VIẾT LẠI PITCH THEO CÁCH CỦA TỪNG CÁ NHÂN (TEAM → CÁ NHÂN → TEAM)
*Sau khi nhóm có bản nháp chung, mỗi cá nhân tự viết lại Pitch theo góc nhìn chuyên môn của mình để kiểm tra mức độ thấu hiểu thông điệp cốt lõi trước khi chốt bản cuối cùng.*

### 👤 Phiên bản của Nguyễn Khánh Duy (Góc nhìn Product & Kiến trúc)
> *"Kính gửi BQL và Hội đồng: VinStay AI đề xuất hợp tác triển khai giải pháp 'Cho thuê căn hộ số hóa an toàn' tại 75 căn Sapphire. Bằng việc số hóa quy trình và dùng Field Host nội khu đón khách tận sảnh, chúng tôi cam kết loại bỏ 100% Lockbox vi phạm và giảm người lạ tự do trong thang máy. Dữ liệu thử nghiệm tòa S2.05 cho thấy thời gian khớp căn chỉ mất 28s và 100% khách được đón đúng hẹn. Kính đề nghị BQL dành 30 phút thứ Sáu này để xem demo trực tiếp luồng đón khách qua sảnh an ninh."*

### 👤 Phiên bản của Lê Thanh Tùng (Góc nhìn Vận hành thực địa & Người dùng)
> *"Chào BQL Vinhomes: Thay vì để chủ nhà tự treo hộp khóa Lockbox gây mất mỹ quan và mất an toàn hành lang, VinStay AI cung cấp giải pháp Field Host là cư dân/sinh viên VinUni đón khách trực tiếp từ sảnh bằng thẻ cư dân hợp lệ. Toàn bộ lịch xem phòng được điều phối qua OTP chính xác đến từng phút, có cơ chế nhắc hẹn kép T-10m. Chúng tôi đã thực hiện 15 lượt đón khách thử nghiệm an toàn tuyệt đối. Kính mời BQL thí điểm 10 căn đầu tiên tại S1.02 từ tuần tới."*

### 👤 Phiên bản của Cao Đức Hiệp (Góc nhìn Dữ liệu & An ninh thông tin)
> *"Kính gửi BQL Ocean Park: VinStay AI giải quyết bài toán an ninh cư trú bằng công nghệ AI khớp căn chuẩn xác và Zero-Storage OCR CCCD. Chúng tôi tự động hóa trích xuất thông tin khách thuê hợp pháp trong 15 giây mà không lưu trữ ảnh CCCD, sẵn sàng chuyển thông tin khai báo tạm trú tức thì. Khách không thể tự ý vào tòa nhà nếu không có mã đặt chỗ và Field Host bảo lãnh đón sảnh. Đề xuất buổi làm việc 30 phút để kiểm tra hệ thống bảo mật và cơ chế cấp quyền."*

👉 **Kết quả gộp nhóm:** Nhóm đã chọn lọc các luận điểm sắc bén nhất từ 3 bản nháp: **Cam kết 0% Lockbox (Tùng), Tốc độ khớp căn 28s & Small Ask 30 phút (Duy), Dữ liệu tạm trú minh bạch (Hiệp)** để tạo thành bản Pitch hoàn chỉnh ở **Trang 2 của PDF**.

---

## 3. PHASE 4: TỰ CHẤM ĐIỂM TEAM HEALTH ĐỘC LẬP (CÁ NHÂN → TEAM)
*Mỗi người tự chấm điểm 1–5 cho 4 khía cạnh sức khỏe nhóm và ghi chú lý do độc lập trước khi đối chiếu.*

| Khía cạnh | Duy | Tùng | Hiệp | Lý do & Phân tích chênh lệch |
|:---|:---:|:---:|:---:|:---|
| **Chất lượng AI** | 3.5 | 3.5 | 4.0 | Hiệp chấm 4.0 vì backend pipeline chạy ổn định; Duy và Tùng chấm 3.5 vì nhận thấy khi khách nhập yêu cầu quá dài thì matching agent đôi khi bỏ sót tiêu chí tầng/hướng. |
| **Tiến độ** | 4.0 | 4.5 | 4.5 | Tùng và Hiệp hài lòng với tiến độ hoàn thành các task kỹ thuật; Duy chấm 4.0 vì cần đẩy nhanh hơn việc kết nối thực địa với chủ nhà. |
| **Tinh thần team** | 5.0 | 4.5 | 4.5 | Cả 3 đều cho điểm rất cao (4.5 - 5.0). Nhóm giao tiếp minh bạch, phản hồi ngay lập tức trên nhóm chat và không có xung đột cá nhân. |
| **Tốc độ ra sản phẩm** | 3.5 | 3.5 | 3.0 | Điểm thấp nhất nhóm. Hiệp chấm 3.0 vì mỗi lần sửa code lại phải test thủ công từng endpoint mất nhiều thời gian; cả nhóm đồng thuận đây là điểm nghẽn lớn nhất. |

👉 **Kết quả gộp nhóm:** Nhóm xác định **Tốc độ ra sản phẩm (3.3)** và **Chất lượng AI (3.7)** là vấn đề ưu tiên hàng đầu, từ đó thống nhất chọn **Evals & Quality Benchmarking** làm năng lực cần nâng cấp và xây dựng **3 hành động Growth Plan 30 ngày** ở **Trang 4 của PDF**.
