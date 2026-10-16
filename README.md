# Focus Games - Game rèn luyện tập trung

Web app gồm 2 game: Stroop Test (60 giây) và Anti-arrow (60 giây).

#

## Thành viên
1. Nguyễn Minh Tường      | (https://github.com/phatbangq)
2. Phạm Đình Hải Triều    | (https://github.com/HaiTrieu46)
3. Nguyễn Minh Niên       | (https://github.com/ngnien1336-cmyk)
4. Hồ Trương Thái Phương  | (https://github.com/Player102-ChapMotTay) 

## Cách chạy
git clone, rồi mở index.html bằng trình duyệt.

## Luật từng giai đoạn

> Mỗi thành viên đọc kỹ trước khi nhận thẻ. Chỉ làm thẻ của giai đoạn đang chạy.

---

### 🔵 GĐ1: Chuẩn bị và nền tảng

**Mục tiêu:** dựng bộ khung và các hàm dùng chung. Game chưa cần chơi được.

**Được làm:**

- Tạo repo, cấu trúc thư mục, trang chủ có menu chọn game
- Chốt màu, font, CSS variables (style cơ bản, đủ nhìn rõ)
- Khung màn chơi chung: điểm, đồng hồ, thanh tiến trình, vùng kích thích, dòng phím điều khiển
- Các module dùng chung: đo phản xạ, tính điểm, hẹn giờ, đếm ngược (chỉ là chức năng: số 3, 2, 1 đổi đúng), lưu localStorage
- README bản đầu, quy ước nhánh và commit

**Tuyệt đối không làm:**

- ❌ Mọi hiệu ứng: chớp màu, rung, phóng to, fade, chuyển cảnh, confetti
- ❌ Âm thanh
- ❌ Logic của game cụ thể (sinh đề Stroop, sinh mũi tên)
- ❌ Biểu đồ, trang thống kê

**Xong khi:** mở trang chủ thấy menu, bấm vào game thấy khung trống, gọi thử `updateScore(10)` thì đồng hồ chạy đúng. Mỗi module có chú thích cách dùng ở đầu file để C và D gọi được.
**Việc bắt buộc:** đặt tên `id`/`class` rõ ràng (`#score`, `#timer`, `#progress-fill`, `#stimulus`) để GĐ3 thêm hiệu ứng mà không phải sửa khung.

---

### 🟢 GĐ2: Làm hai game

**Mục tiêu:** hai game chơi được trọn vẹn từ đầu đến cuối, dù còn "trơ".

**Được làm:**

- Stroop: sinh đề, bắt phím/nút, kiểm tra đúng sai, chạy 60 giây, hết giờ thì kết thúc
- Anti-arrow: sinh mũi tên, bắt phím ngược hướng, kiểm tra đúng sai, tăng tốc dần
- Màn hướng dẫn và lượt luyện tập (chữ và nút đơn giản)
- Dùng các module của B (đo phản xạ, timer, điểm). Không tự viết lại.
- Ghi lại dữ liệu mỗi lượt (đúng/sai, thời gian phản xạ, loại lượt) để GĐ3 dùng

**Tuyệt đối không làm:**

- ❌ Hiệu ứng, âm thanh
- ❌ Công thức điểm tập trung, các chỉ số nâng cao (hiệu ứng nhiễu, độ ổn định, mệt mỏi)
- ❌ Màn hình kết quả đẹp, biểu đồ
- ❌ Sửa file module chung của B. Cần sửa thì báo B hoặc tạo thẻ.

**Xong khi:** chơi hết một ván mà không lỗi, đúng/sai tính chuẩn, hết giờ thì dừng, dữ liệu từng lượt được lưu đủ. Chỉ cần hiện điểm đơn giản, chưa cần đẹp.

---

### 🟠 GĐ3: Thống kê, điểm và hiệu ứng

**Mục tiêu:** biến game "trơ" thành game có chiều sâu và đẹp. Đây là giai đoạn duy nhất được thêm hiệu ứng.

**Được làm:**

- Tính chỉ số và điểm tập trung, xếp loại
- Màn hình kết quả, trang lịch sử, biểu đồ Chart.js, điểm cao nhất
- Hiệu ứng đúng/sai, combo, đếm ngược 3-2-1, chuyển màn hình
- Âm thanh và nút tắt tiếng
- Confetti, dòng "Kỷ lục mới"

**Tuyệt đối không làm:**

- ❌ Đổi luật chơi hay logic game đã xong ở GĐ2
- ❌ Hiệu ứng nặng trong lúc kích thích đang hiện (nền động, hạt bay, fade-in chữ). Nó làm sai thời gian phản xạ.
- ❌ Hiệu ứng phản hồi dài quá 300ms

**Xong khi:** chơi xong thấy kết quả, biểu đồ và lịch sử đúng với dữ liệu thật, hiệu ứng mượt mà không làm chậm game, tắt tiếng được.

---

### 🟣 GĐ4: Hoàn thiện

**Mục tiêu:** sửa lỗi, kiểm tra, đóng gói để nộp.

**Được làm:**

- Test chéo (C test game của D và ngược lại), ghi lỗi thành thẻ Bug
- Test điện thoại, trình duyệt khác, sửa giao diện
- Sửa lỗi dữ liệu và thống kê
- Chốt README, ảnh chụp, link demo, slide, ảnh chụp board Trello

**Tuyệt đối không làm:**

- ❌ Thêm tính năng mới. Có ý tưởng hay thì ghi vào mục "Hướng phát triển" trong README.
- ❌ Sửa lớn code đang chạy ổn mà không có thẻ Bug

