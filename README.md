# Focus Games - Game rèn luyện tập trung

Web app gồm 2 game: Stroop Test (60 giây) và Anti-arrow (60 giây).

#

## Thành viên
| Người | Tên | Phụ trách |
|---|---|---|
| A | ... | Khung web, giao diện, deploy, README |
| B | ... | Module dùng chung, thống kê, biểu đồ |
| C | ... | Game Stroop |
| D | ... | Game Anti-arrow |

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

**Xong khi:** mở trang chủ thấy menu, bấm vào game thấy khung trống, gọi thử `updateScore(10)` thì

