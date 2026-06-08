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
- Ưu điểm:
  + Miễn phí.
  + Dễ học.
  + Không cần cài đặt môi trường phức tạp.
  + Phù hợp cho người mới học lập trình.
  + Tạo ứng dụng nhanh chóng.
- Nhược điểm:
  + Khó phát triển hệ thống lớn.
  + Khả năng tùy biến hạn chế.
  + Hiệu năng không cao bằng Android Studio.

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
  Screen1 đóng vai trò là màn hình chính của ứng dụng. Màn hình này hiển thị thông tin cá nhân của sinh viên và cung cấp các nút điều hướng đến các chức năng khác.
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
  + Text: GIỚI THIỆU BẢN THÂN
  + FontSize: 22
  + FontBold: True
  + Width: Fill Parent
  + TextAlignment: Center
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/01afb828-26f8-4ec2-990e-f1e6e3c591f7" />

- Label này dùng để hiển thị tiêu đề của màn hình.

## Bước 3: Thêm ảnh đại diện
- Chuẩn bị một ảnh cá nhân có định dạng JPG hoặc PNG.
- Chọn Media bên phải màn hình -> Upload File để tải ảnh lên dự án.
- Tiếp theo từ Palette chọn: User Interface -> Image -> Kéo vào dưới tiêu đề.
- Thiết lập thuộc tính:
  + Picture = avatar.jpg
  + Width = 200 Pixels
  + Height = 180 Pixels
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/1db3427f-e56c-40ac-a17a-f62f5d553b61" />
- Thành phần Image được sử dụng để hiển thị ảnh đại diện của sinh viên.

## Bước 4: Thêm thông tin cá nhân
- Kéo thêm 4 Label gồm: Họ tên, MSSV, Ngành học, Trường.
- Thuộc tính:
  + FontSize = 15
  + Width = Fill Parent
  + TextAlignment = Center
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/392a4c90-e1d7-4d59-bf80-6098502dacf9" />

- 4 Label này có nhiệm vụ hiển thị thông tin giới thiệu của sinh viên.

## Bước 5: Tạo nút chuyển sang màn hình giải toán và website
- Từ Palette chọn: User Interface -> Button -> Kéo vào giao diện.
- Thiết lập:
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/0deb1d67-0e4d-46c9-aed9-da1e8fc58616" />

# 4. Thiết kế màn hình Screen 2 (Giải bài toán)
- Mục đích của màn hình này là thực hiện phép cộng hai số do người dùng nhập vào.
## Bước 1: Thiết lập màn hình
- Tạo màn hình mới bằng cách chọn: Add Screen
<img width="1920" height="1200" alt="12" src="https://github.com/user-attachments/assets/16301348-8184-4393-acd3-1884de86e609" />

- Đặt tên: ScreenMath -> nhấn OK
<img width="538" height="272" alt="image" src="https://github.com/user-attachments/assets/026afd7b-bcb2-4c92-b8b5-5d6da1adb9f0" />

## Bước 2: Tạo tiêu đề
- Kéo Label.
- Text: TÍNH TỔNG HAI SỐ
- Thiết lập:
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/93ad2134-52aa-446c-97a6-ecef22150592" />

## Bước 3: Tạo ô nhập số thứ nhất
- Kéo TextBox.
- Thiết lập:
  + Hint: Nhập số thứ nhất
  + NumbersOnly: True
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/ca6043ab-2797-4c47-ae33-93f54785d635" />

## Bước 4: Tạo ô nhập số thứ hai
- Kéo TextBox.
- Thiết lập:
  + Hint: Nhập số thứ hai
  + NumbersOnly: True
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/37d8256f-14a0-493b-bb25-6bc96c394cdd" />

## Bước 5: Tạo nút tính
- Kéo Button -> Nhập Text: Tính
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/58370799-0442-46af-81db-1ba20537aaf0" />

## Bước 6: Tạo vùng hiển thị kết quả và thêm nút quay lại screen 1
- Kéo Label -> Nhập Text: Kết quả
<img width="882" height="978" alt="image" src="https://github.com/user-attachments/assets/ce048434-d013-4aab-aab2-3e92b68bdd9b" />

<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/e045bdba-ddd5-418e-ae77-3884611edea2" />

# 5. Thiết kế Screen3 - WebView
- Tạo Screen mới: Add Screen -> ScreenWeb
<img width="621" height="838" alt="image" src="https://github.com/user-attachments/assets/86248502-46b3-49d0-b76c-a08bcca73cae" />

- Thêm WebViewer: Trong Palette -> User Interface -> WebViewer
- Thiết lập thuộc tính:
  + Width: Fill Parent
  + Height: Fill Parent
- HomeUrl: https://www.tnut.edu.vn
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/cf58f252-d329-4695-a1bd-42f9eb829261" />

- Khi mở màn hình, website sẽ được tải tự động.

# 6. Lập trình bằng Blocks
## Điều hướng từ Screen1 sang ScreenMath
- Chọn tab Blocks:
<img width="1920" height="1200" alt="12" src="https://github.com/user-attachments/assets/6b546064-36ae-4a1c-976c-63af94ccb07c" />

- Giao diện tab blocks:
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/6ee2111c-ba73-4094-872c-b69e00b30bc8" />

- Chọn Button 1 (nút Giải Toán) -> Kéo block: when Button1.Click
<img width="1920" height="1200" alt="12" src="https://github.com/user-attachments/assets/b5ee0bec-6359-40c3-82b6-8e39dc0301b1" />

- Từ nhóm Control kéo: open another screen screenName
<img width="1920" height="1200" alt="12" src="https://github.com/user-attachments/assets/f6b7b9b8-a720-4c69-926c-b4978254bc43" />

- Chọn tên màn hình: ScreenMath
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/0fb87b87-b258-4b10-8054-020c8ad9536c" />

- Khi người dùng nhấn nút "Giải bài toán", ứng dụng sẽ chuyển sang màn hình ScreenMath.
## Điều hướng từ Screen1 sang ScreenWeb
- Kéo: when Button2.Click
<img width="1920" height="1200" alt="12" src="https://github.com/user-attachments/assets/b6c4bffe-9e74-49bb-b78e-d6d49b18e3e0" />

- Từ nhóm Control kéo: open another screen screenName
- Chọn tên màn hình: ScreenWeb
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/a41d55b6-101a-4486-8adf-d2aba79a3310" />

- Khi người dùng nhấn nút "Xem Website", ứng dụng sẽ chuyển sang màn hình ScreenWeb.
## Xử lý tính tổng
  Trong ScreenMath kéo:
- Chọn tab Blocks.
- Chọn Button1 (nút Tính).
- Kéo block: when Button1.Click
- Chọn Label2 và kéo: set Label2.Text to
- Từ nhóm Math, kéo block dấu cộng (+).
- Từ TextBox1 kéo: TextBox1.Text
- Từ TextBox2 kéo: TextBox2.Text
- Ghép các block lại để thực hiện phép cộng và hiển thị kết quả lên Label2.
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/472bbd4b-4862-472a-bacb-348b01a238a3" />

## Block nút quay lại screen 1 của screen 3
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/167c133c-8a9b-46a5-912c-5ac4e8495903" />

# 7. Bản chất của Blocks
- Blocks là hình thức lập trình trực quan.
- Thay vì viết mã nguồn bằng Java hoặc Kotlin, người dùng kéo thả các khối lệnh và ghép chúng với nhau.
- Mỗi khối lệnh đại diện cho một chức năng hoặc câu lệnh trong chương trình.
- Ví dụ:
  + Event Block: xử lý sự kiện.
  + Math Block: tính toán.
  + Logic Block: điều kiện.
  + Control Block: điều khiển chương trình.

# 8. Ưu điểm và nhược điểm của Blocks
- Ưu điểm:
  + Dễ học và dễ sử dụng.
  + Không cần ghi nhớ cú pháp.
  + Hạn chế lỗi cú pháp.
  + Tạo ứng dụng nhanh.
  + Phù hợp với người mới học lập trình.
- Nhược điểm:
  + Khó quản lý khi dự án lớn.
  + Số lượng Block nhiều dễ gây rối.
  + Khả năng mở rộng hạn chế.
  + Không mạnh bằng các công cụ lập trình chuyên nghiệp.

# 9. Chạy thử ứng dụng
- Chọn: Connect -> AI Companion
<img width="1920" height="1200" alt="12" src="https://github.com/user-attachments/assets/0bcbbfb0-5d9e-4f25-a9cf-dc745b0227af" />

- Xuất hiện QR sau khi chọn AI Companion:
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/2ea8a89b-a9eb-4079-b6b3-9141a4ccef45" />

- Sau đó: Mở ứng dụng MIT AI2 Companion trên điện thoại và quét mã QR.
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/2786f609-ed24-4fed-b9aa-890a5be9750f" />

- Lúc này ứng dụng sẽ chạy trên điện thoại.
9. Sử dụng Backpack

Backpack là công cụ hỗ trợ sao chép và tái sử dụng Block.

Cách thực hiện:

Bước 1: Chọn Block cần sao chép.

Bước 2: Kéo Block xuống biểu tượng Backpack.

Bước 3: Chuyển sang màn hình khác.

Bước 4: Mở Backpack.

Bước 5: Kéo Block từ Backpack ra vị trí mong muốn.

Backpack giúp tiết kiệm thời gian và tránh phải tạo lại các Block giống nhau.

10. Kết luận

Ứng dụng đã được xây dựng thành công với ba màn hình gồm màn hình giới thiệu, màn hình giải bài toán và màn hình hiển thị website. Thông qua quá trình thực hiện, người học hiểu được quy trình phát triển ứng dụng trên MIT App Inventor, cách thiết kế giao diện bằng kéo thả, lập trình bằng Blocks và tái sử dụng mã lệnh bằng Backpack.
