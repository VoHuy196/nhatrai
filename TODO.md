# TODO.md - QUẢN LÝ NHIỆM VỤ DỰ ÁN THƯ MỜI CƯỚI

## Nhiệm vụ hiện tại: Sửa lỗi form RSVP không lưu "Tham dự" vào Google Sheet

**Thông tin đã thu thập:**
- Form RSVP trong section #w-d688ytkq có các trường: Tên (#w-yj3hxu4w), SĐT (#w-qycil5et), Email/Lời chúc (#w-81v32j1d), Tham dự (#w-gkkgczp7 select), nút gửi #w-jsy0cioh.
- JS handler lấy attendance từ textContent option vì value có thể là "untitled".
- Lỗi: ID sai ('wi-81v32j1d' thay vì 'w-81v32j1d'), thiếu fullName/phone grab đúng, validation fail.

**Kế hoạch sửa lỗi:**
- Sửa ID trong JS: 'wi-81v32j1d' → 'w-81v32j1d'
- Thêm fullName = document.querySelector('#w-yj3hxu4w input').value.trim()
- phone = document.querySelector('#w-qycil5et input').value.trim()
- Cải thiện validation attendance và alert tiếng Việt.

## Các bước thực hiện:
- [x] Bước 0: Tạo TODO.md với kế hoạch chi tiết
- [ ] Bước 1: Đọc đầy đủ JS code trong index.html để xác định vị trí edit chính xác
- [ ] Bước 2: Edit index.html - sửa JS form submit handler
- [ ] Bước 3: Test form bằng http-server và submit thử
- [ ] Bước 4: Kiểm tra Google Sheet nhận đầy đủ data "Tham dự"
- [ ] Bước 5: Update TODO.md đánh dấu hoàn thành và attempt_completion

**Ghi chú:** Giữ nguyên cấu trúc code, chỉ sửa minimum để fix bug.
