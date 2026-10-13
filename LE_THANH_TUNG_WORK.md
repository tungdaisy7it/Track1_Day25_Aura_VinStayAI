# NHẬT KÝ CÔNG VIỆC & ĐÓNG GÓP DỰ ÁN VINSTAY AI
**Thành viên:** Lê Thanh Tùng  
**MSSV:** 2A202602499  
**Team:** Aura  
**Vai trò cốt lõi (Core Role):** Fullstack Engineer & Field Operations Lead  
**Dự án:** VinStay AI — Hệ điều hành Cho thuê & Vận hành Căn hộ Tinh gọn (Asset-Light) tại Vinhomes Ocean Park

---

## 1. PHẠM VI TRÁCH NHIỆM TRONG DỰ ÁN VINSTAY AI (TECHNICAL SCOPE)

### A. Tầng Giao diện & Trải nghiệm Người dùng (Frontend & Client Layer - Next.js 15)
- **Tenant Portal (Web App Khách thuê):** Xây dựng Catalog căn hộ Sapphire 1 & 2, bộ lọc ngân sách trần và công cụ tính toán chi phí trọn gói thời gian thực (**All-in Cost Calculator** bao gồm: tiền thuê + phí dịch vụ BQL + điện nước ước tính).
- **Host Mobile Dashboard (Web App dành cho Field Host):** Thiết kế giao diện mobile cho Field Host nội khu nhận ca trong vòng 3 phút, kiểm tra mã đặt chỗ OTP và dẫn khách qua sảnh an ninh.
- **Tích hợp Thanh toán VietQR & Khóa căn:** Xây dựng luồng tạo mã QR thanh toán cọc bảo đảm, tự động kích hoạt trạng thái giữ phòng trong 24 giờ để khách an tâm chuẩn bị dọn vào.

### B. Vận hành Thực địa Tinh gọn (Asset-Light Field Operations)
- **Mô hình Field Host thay thế Lockbox:** Đề xuất và đặc tả quy trình vận hành hợp chuẩn 100% quy chế BQL Vinhomes (thay vì dùng hộp khóa cơ vi phạm quy chế); tuyển dụng và phân bổ mạng lưới sinh viên VinUni/cư dân làm theo ca biến phí.
- **Cơ chế nhắc hẹn kép (T-10m Alert):** Cài đặt luồng nhắc hẹn tự động push notification cho Field Host trước 10 phút giờ hẹn; nếu không xác nhận trong 3 phút, hệ thống tự động gán cho Host dự phòng cùng tòa.
- **Biên bản bàn giao số (Digital Handover Passport):** Thiết lập checklist kiểm tra hiện trạng nội thất có chụp ảnh đối chứng ngay trên điện thoại khi đón khách và khi khách trả phòng.

---

## 2. ĐÓNG GÓP CHI TIẾT TRONG BÀI LAB DAY 25 (AI TEAM LAB)

### 📌 Phase 1: Danh sách Stakeholder độc lập (Góc nhìn Vận hành & Trải nghiệm)
Trong bước làm việc cá nhân, tôi đã tự liệt kê 6 stakeholder cụ thể gắn liền với thực tế vận hành:
1. **Khách thuê trẻ (Sinh viên VinUni & Chuyên gia TechnoPark):** Người trực tiếp duyệt phòng, cần giá All-in trọn gói và xem listing thật 100%.
2. **Bảo vệ sảnh & Lễ tân các tòa Sapphire (S1.02, S1.08, S2.05):** Đội ngũ kiểm soát thẻ cư dân thang máy, cần phối hợp nhịp nhàng để không gây ùn tắc sảnh.
3. **Đội thợ kỹ thuật & sửa chữa nội khu:** Đối tác nhận việc theo mô hình biến phí, hỗ trợ bảo trì điện nước nhanh chóng khi căn hộ có sự cố.
4. **Chủ nhà ở xa (Hà Nội / Ngoại tỉnh):** Cần hệ thống thông báo mở cửa tức thì và báo cáo doanh thu minh bạch để yên tâm ủy quyền.
5. **Cửa hàng tiện lợi / Quán cafe nội khu (Highlands sảnh S2):** Điểm hỗ trợ khách ngồi chờ kèm voucher nếu phát sinh tình huống Field Host trễ hẹn.
6. **Cư dân lân cận cùng tầng căn hộ:** Bên có thể phản ánh nếu khách thuê gây ồn ào; cần quy chế ứng xử rõ ràng.

### 📌 Phase 2: Bản nháp Pitch & Trách nhiệm RACI
- **Bản nháp Pitch cá nhân (Góc nhìn Vận hành thực địa):**
  > *"Chào BQL Vinhomes: Thay vì để chủ nhà tự ý treo hộp khóa Lockbox gây mất mỹ quan và mất an toàn hành lang, VinStay AI cung cấp giải pháp Field Host là cư dân/sinh viên VinUni đón khách trực tiếp từ sảnh bằng thẻ cư dân hợp lệ. Toàn bộ lịch xem phòng được điều phối qua OTP chính xác đến từng phút, có cơ chế nhắc hẹn kép T-10m. Chúng tôi đã thực hiện 15 lượt đón khách thử nghiệm an toàn tuyệt đối. Kính mời BQL thí điểm 10 căn đầu tiên tại S1.02 từ tuần tới."*
- **Trách nhiệm trong ma trận RACI:**
  - **Accountable (A) - Chịu trách nhiệm chính:** 
    * *Đầu việc 4:* Phát triển Giao diện All-in Cost & Host Mobile Dashboard.
    * *Đầu việc 6:* Vận hành thử nghiệm Pilot 30 căn hộ thực tế tại phân khu Sapphire.
  - **Responsible (R) - Thực hiện trực tiếp:**
    * *Đầu việc 1:* Phối hợp cùng Lead xây dựng quy chế Field Host.
    * *Đầu việc 5:* Tham gia chạy thử nghiệm 50 cases kiểm thử.

### 📌 Phase 4: Đánh giá Team Health & Cam kết Growth Plan 30 ngày
- **Điểm tự chấm sức khỏe nhóm (Team Health):**
  * *Chất lượng AI:* **3.5/5** (Cần cải thiện việc nhận diện yêu cầu ngữ cảnh sâu).
  * *Tiến độ:* **4.5/5** (Rất hài lòng với tốc độ hoàn thành các Sprint của nhóm).
  * *Tinh thần team:* **4.5/5** (Giao tiếp thẳng thắn, phối hợp mượt mà).
  * *Tốc độ ra sản phẩm:* **3.5/5** (Cần giảm bớt thời gian kiểm thử thủ công).
- **Cam kết hành động trong Growth Plan 30 ngày:**
  * **Hành động phụ trách (Owner):** Tối ưu hóa Host Mobile Web App với chế độ 1 chạm nhận ca và checklist kiểm tra bàn giao căn hộ điện tử (Digital Handover Passport).
  * **Deadline:** 03/11/2026.
  * **Kết quả đo lường (Dấu hiệu hoàn thành):** Thời gian Field Host xác nhận tiếp nhận ca giảm xuống **< 60 giây**; 100% biên bản bàn giao có ảnh chụp upload ngay lên hệ thống.

---

## 3. HƯỚNG DẪN TỰ PUSH COMMIT ĐÓNG GÓP LÊN GITHUB (DÀNH CHO TÙNG)
Nếu muốn ghi nhận commit cá nhân từ tài khoản của bạn lên repo `Track1_Day25_Aura_VinStayAI`, bạn có thể thực hiện trên máy của mình:

```bash
# 1. Clone repo về máy (nếu chưa clone)
git clone https://github.com/tungdaisy7it/Track1_Day25_Aura_VinStayAI.git
cd Track1_Day25_Aura_VinStayAI

# 2. Tạo branch cá nhân
git checkout -b feature/tung-field-ops

# 3. Thêm file LE_THANH_TUNG_WORK.md vào thư mục và commit
git add LE_THANH_TUNG_WORK.md
git commit -m "docs(tung): add personal task log and field operations deliverables"

# 4. Push lên GitHub
git push -u origin feature/tung-field-ops
```
*Sau đó tạo Pull Request trên giao diện web GitHub và merge vào `main` để lịch sử đóng góp hiển thị trọn vẹn!*
