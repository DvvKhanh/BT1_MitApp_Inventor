# BÀI TẬP LỚN PHÁT TRIỂN ỨNG DỤNG TRÊN THIẾT BỊ DI ĐỘNG
# Sinh viên: Đậu Văn Khánh
# MSSV: K225480106099
# Lớp: K58KTP
# Mô tả đề bài:
## Viết phần mềm trên công cụ Mit App inventor
- App có 3 screen:
   + Màn hình giới thiệu (About): Hiển thị thông tin cá nhân của sinh viên và cung cấp các nút điều hướng để chuyển đến các màn hình chức năng khác.
   + Màn hình giải bài toán đơn giản: Cho phép người dùng nhập dữ liệu, thực hiện tính toán và hiển thị kết quả của một bài toán cơ bản.
   + Màn hình WebView: Sử dụng thành phần WebViewer để hiển thị một trang web có sẵn, bảo đảm khả năng hiển thị phù hợp trên thiết bị di động.

# 1. Giới thiệu
- MIT App Inventor là nền tảng phát triển ứng dụng Android trực tuyến do Viện Công nghệ Massachusetts (MIT) phát triển. Công cụ này cho phép người dùng tạo ứng dụng bằng phương pháp kéo thả các thành phần giao diện và lập trình trực quan bằng các khối lệnh (Blocks) mà không cần viết nhiều mã nguồn như các ngôn ngữ lập trình truyền thống.
- Mục tiêu của đề tài là xây dựng một ứng dụng Android đơn giản gồm ba màn hình nhằm tìm hiểu quy trình thiết kế giao diện, xử lý sự kiện và phát triển ứng dụng trên nền tảng MIT App Inventor.

# 2. Tạo dự án mới
- Truy cập MIT App Inventor, mở trình duyệt: https://appinventor.mit.edu
- Chọn: Create Apps!
<img width="1920" height="1200" alt="11" src="https://github.com/user-attachments/assets/7bd957fe-9d51-4fd0-826e-9b3c26cec7cb" />

- Đăng nhập bằng Gmail.
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/af6920cf-d8fd-4173-a05a-3ab50ee6b945" />

- Tạo project:
  + Chọn: Projects -> New Project
  + Đặt tên project: BTL_MOBILE -> Nhấn OK
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/9d9a8965-2749-4cc6-8404-4fa6fd3e1d16" />
- Lúc này sẽ xuất hiện màn hình Screen1 -> đây là màn hình đầu tiên của ứng dụng.
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/2295691c-76a7-45cb-aeb6-084d69a1c280" />

# 3. Thiết kế màn hình Screen 1 (About)
## Bước 1: Tạo bố cục giao diện
- Từ Palette chọn: Layout -> Vertical Arrangement
- Kéo thả vào Viewer.
- Sau đó thiết lập:
  + Width = Fill Parent
  + Height = Fill Parent
  + AlignHorizontal = Center
- Việc sử dụng Vertical Arrangement giúp các thành phần được sắp xếp theo chiều dọc, giao diện gọn gàng và dễ quản lý hơn.
<img width="355" height="731" alt="image" src="https://github.com/user-attachments/assets/e129dd8f-43b7-48d3-93cc-028505117fee" />

## Bước 2: Thêm tiêu đề
- Từ Palette chọn: User Interface -> Label
- Kéo Label vào Vertical Arrangement.
- Thiết lập thuộc tính:
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/01afb828-26f8-4ec2-990e-f1e6e3c591f7" />
- Label này dùng để hiển thị tiêu đề của màn hình.

## Bước 3: Thêm ảnh đại diện
- Chuẩn bị một ảnh cá nhân có định dạng JPG hoặc PNG.
- Chọn Media bên phải màn hình -> Upload File để tải ảnh lên dự án.
- Tiếp theo từ Palette chọn: User Interface -> Image -> Kéo vào dưới tiêu đề.
- Thiết lập thuộc tính:
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/1db3427f-e56c-40ac-a17a-f62f5d553b61" />
- Thành phần Image được sử dụng để hiển thị ảnh đại diện của sinh viên.

## Bước 4: Thêm thông tin cá nhân
- Kéo thêm 4 Label gồm: Họ tên, MSSV, Ngành học, trường.
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/c081b0c3-8533-439f-a592-e1ec2adbb33a" />
- 4 Label này có nhiệm vụ hiển thị thông tin giới thiệu của sinh viên.

## Bước 5: Tạo nút chuyển sang màn hình giải toán và website
- Từ Palette chọn: User Interface -> Button -> Kéo vào giao diện.
- Thiết lập:
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/5fa73d71-42a8-47f9-8573-7f31e2bf4f92" />

# 4. Thiết kế màn hình Screen 2 (Giải bài toán)
