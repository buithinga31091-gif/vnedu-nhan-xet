# EduRemark – Quản lý nhận xét đa môn và hỗ trợ VNEDU

## Dùng ngay
- Mở `index.html` bằng Chrome để thêm/sửa nhận xét theo môn, theo T/H/C. Dữ liệu lưu localStorage trên thiết bị.
- Chọn **Xuất kho nhận xét JSON** để sao lưu.
- Cài Tampermonkey, tạo tập lệnh mới, dán nội dung `vnedu-helper.user.js`, lưu và bật.
- Vào VNEDU ở **đúng tên miền được cấp phép**, chọn Sổ nhận xét, đúng môn và kỳ; mở công cụ nổi, nhập JSON kho, bấm kiểm tra / xem trước. Chỉ khi kiểm tra thành công mới bật được nút điền.

## Đăng GitHub Pages
1. Tạo repository `vnedu-nhan-xet` và upload `index.html` + `README.md` (không upload file JSON riêng có dữ liệu nhạy cảm).
2. Settings → Pages → Deploy from a branch → main → /(root) → Save.
3. Trang thường có URL dạng `https://TEN_TAI_KHOAN.github.io/vnedu-nhan-xet/` sau khi triển khai.

## Giới hạn & an toàn
- Trang GitHub Pages **không** được phép thay đổi trực tiếp tab VNEDU khác nguồn; dùng Tampermonkey mới có thể chèn công cụ vào VNEDU.
- Tập lệnh chỉ chạy trên *.vnedu.vn theo cấu hình mẫu. Nếu trường dùng tên miền khác, cần kiểm tra tên miền chính xác và sửa `@match` có chủ đích.
- Tập lệnh chỉ hỗ trợ giao diện bảng HTML với cột nhận xét/xếp loại được nhận diện. Nếu VNEDU dùng iframe, bảng tùy biến hoặc cơ chế thay đổi tự lưu, tính năng có thể không hoạt động. Cần kiểm thử trên tài khoản được phép và dữ liệu thử.
- Tập lệnh không vượt quyền, không tự đăng nhập, không bấm nút Lưu, không gửi dữ liệu đi mạng. Tuy nhiên thao tác ô có thể kích hoạt cơ chế tự lưu phía VNEDU; hãy kiểm tra trước khi sử dụng thực tế.
- Chỉ sử dụng trong phạm vi nhà trường cho phép. Không đưa dữ liệu học sinh vào kho mã nguồn công khai.
