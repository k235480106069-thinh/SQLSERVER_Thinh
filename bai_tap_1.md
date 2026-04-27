# SQL SERVER

## Họ & tên: Nguyễn Đăng Thịnh
## Lớp: K59KMT.K01  
## MSSV: K235480106069
1.Download và cài đặt SQL Server 2025, phiên bản Developer
(Do em cài quên chụp lên em mở lại demo để chụp ạ)
<img width="1920" height="1080" alt="tải sql" src="https://github.com/user-attachments/assets/f4bf348e-9b32-4911-aec4-f42f547369ba" />

2.Cấu hình cho SQL Server làm việc ở cổng động (Dynamic Port), TCP: enable+active yes cho 127.0.0.1, chọn cổng động là 3xxxx với xxxx là 4 số cuối của mã số sv, (nếu cổng này đã mở sẵn trước đó bởi 1 ứng dụng khác thì chọn cổng là 4xxxx hoặc 5xxxx)
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/21cc2932-fb25-4723-80c8-343e95a421b0" />
enable+active yes cho 127.0.0.1 ,  cổng động là 46069

Kiểm tra xem service SQL Server có đang running và mở đúng cổng đã chọn hay không?
<img width="1920" height="1078" alt="ảnh 5" src="https://github.com/user-attachments/assets/bed43cc5-b53b-45ab-980a-e70cf675e610" />
SQL Server có đang running 
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/dc5044a5-5716-4b6e-84a4-bbc1cefdd078" />
Sử dụng lệnh trên cmd: netstat -ano | findstr LISTENING 

4.Cài Đặt SQL Server Management Studio
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/5ace46fb-62e5-4088-8b95-606febf95d3c" />

5.Chạy phần mềm ssms để Đăng nhập vào SQL Server bằng 2 cách: Windows Authentication và SQL Server Authentication.
Cài đặt với 2 kiểu login (Mixed Mode): Windows Authentication (nhớ Add Current User) và SQL Server Authentication (username mặc định là sa, chỉ cần nhập mật khẩu 123 , nhớ nhập 2 chỗ: Enter password và Confirm password)
<img width="1920" height="1080" alt="ảnh 7" src="https://github.com/user-attachments/assets/33032d4b-2789-4ba6-9127-bfd9b3bfc040" />
Kiểu Windows Authentication
<img width="1920" height="1080" alt="sa" src="https://github.com/user-attachments/assets/6c72c6a2-a6b3-43a9-ab2a-ef6938547b53" />
Kiểu SQL Server Authentication

6.Sử dụng giao diện đồ hoạ của ssms: Tạo cơ sở dữ liệu mới (create database) với tên tuỳ ý, chọn Path (nơi lưu trữ db) cho file lưu dữ liệu và file lưu log ở ổ đĩa khác với ổ C. mở path đã chọn xem 2 file đã tạo ra.
(do máy em đầy dung lượng lên không thể tạo thêm ổ D lên em lưu file vào ổ C)
<img width="1920" height="1080" alt="ảnh 10" src="https://github.com/user-attachments/assets/c60289fb-e932-49e9-a8f8-80f00ae2ea6c" />
 Tạo cơ sở dữ liệu mới (create database) với tên tuỳ ý, chọn Path (nơi lưu trữ db) 
<img width="1917" height="1075" alt="file " src="https://github.com/user-attachments/assets/5b6be627-9cf0-4886-b438-b9c3234d898a" />
 mở path đã chọn xem 2 file đã tạo ra.

 7.Sử dụng giao diện đồ hoạ của ssms: Tạo bảng dữ liệu (create and design table) với tên bảng tuỳ ý, có các trường dữ liệu phù hợp với dữ liệu của file data mẫu (CSV), với Khoá chính (Primary Key) là trường masv
<img width="1920" height="1080" alt="taoj bangr" src="https://github.com/user-attachments/assets/110e7985-a5b5-4a23-8303-f36e9a59f016" />
Tạo bảng dữ liệu (create and design table) Khoá chính (Primary Key) là trường masv

8.Sử dụng giao diện đồ hoạ của ssms: Tìm cách import dữ liệu từ file mẫu vào trong bảng vừa tạo.
<img width="1918" height="1076" alt="BULK INSERT" src="https://github.com/user-attachments/assets/14c662da-a984-4fc7-a831-8b09f572cd61" />
import dữ liệu file từ ổ C

9.Mở cửa sổ mới để gõ lệnh trong ssms: GÕ lệnh để kiểm tra xem số dòng của bảng dữ liệu sau khi import, kết quả ok sẽ khoảng 12020 dòng.
<img width="1920" height="1078" alt="SELECT COUNT" src="https://github.com/user-attachments/assets/4aac1b48-f782-4cba-bbd2-c8f69eff3d83" />
Kết quả ra 12020 dòng

10.Trong cửa sổ mới để gõ lệnh: Gõ lệnh để thêm (insert) 1 row vào bảng, với dữ liệu là thông tin cá nhân của sv đang làm bài (mỗi sv sẽ luôn khác nhau ở bước này).
<img width="1920" height="1080" alt="chèn tên mình" src="https://github.com/user-attachments/assets/c14f3a42-fa70-45f4-8e57-30cee7e17f43" />
Đã thêm lệnh insert
<img width="1919" height="1078" alt="in thành công" src="https://github.com/user-attachments/assets/33b73c5d-f09d-4d64-9aaa-258546b7c55b" />
Đã thêm dữ liệu vào bảng
<img width="1920" height="1080" alt="update lại vì sai ngày sinh" src="https://github.com/user-attachments/assets/53bb28ff-f54b-4d9a-bd3f-cebc9c4fc714" />
Update lại vì để sai thứ tự ngày tháng năm sinh
<img width="1920" height="1080" alt="sửa thành công" src="https://github.com/user-attachments/assets/85c1e389-0e5e-423e-a5e9-4a5dc1342c83" />

11.Trong cửa sổ mới để gõ lệnh: Gõ lệnh để cập nhật(update) trường noisinh thành 'Sao Hoả' cho những dòng có noisinh và diachi đều là NULL.
<img width="1919" height="1080" alt="tạo dòng null" src="https://github.com/user-attachments/assets/eaa48ff9-53ef-4088-8f2b-a20ed928f23f" />
Update NULL
<img width="1920" height="1080" alt="up sao hỏa" src="https://github.com/user-attachments/assets/6b704f52-6621-4acd-94f3-ebad47542e76" />
Update Sao Hỏa
<img width="1915" height="1080" alt="kiểm tra" src="https://github.com/user-attachments/assets/cbd552e1-6576-455c-853b-9e305e01b087" />
Kiểm Tra

12.Sử dụng giao diện đồ hoạ của ssms: Tạo bảng SaoHoa gồm những sinh viên có nơi sinh ở 'Sao Hoả', keyword gợi ý: sử dụng 1 câu lệnh: SELECT + INTO
<img width="1919" height="1080" alt="tạo bảng sao hỏa" src="https://github.com/user-attachments/assets/82a7691c-b3dc-467a-8425-33aa9dff07d8" />
Tạo bảng SaoHoa
<img width="1920" height="1080" alt="ktra bảng sao hỏa" src="https://github.com/user-attachments/assets/8bbf0446-8149-4a9a-8835-026818a8b0e5" />
COUNT bảng SaoHoa
<img width="1920" height="1080" alt="table sao hỏa" src="https://github.com/user-attachments/assets/8bdaffd6-c5d8-4228-9def-a301d85477ab" />
Table SaoHoa xuất hiện trong SSMS

13.Trong cửa sổ mới để gõ lệnh: Gõ lệnh xoá (delete) trong bảng SaoHoa những sinh viên cùng họ với em, vd em họ nguyễn thì xoá những sv họ nguyễn.
<img width="1920" height="1080" alt="DELETE THEO HỌ" src="https://github.com/user-attachments/assets/b96abaed-cae8-4db4-8fca-182e3bb2e03f" />
Gõ lệnh xóa 
<img width="1920" height="1080" alt="ktra họ nguyễn" src="https://github.com/user-attachments/assets/e7e6999e-bf51-406e-b190-0276834b4cc2" />
Kiểm tra họ nguyễn

14.Sử dụng giao diện đồ hoạ của ssms: Xuất toàn bộ kết quả của các bước 6,7,8,9,10,11,12,13 ra file dulieu.sql , keyword gợi ý: sử dụng tính năng GEN SCRIPT struct+data cho database
<img width="1920" height="1080" alt="Generate Scripts" src="https://github.com/user-attachments/assets/cde7b04e-98fe-4b49-a269-bd30e81c276e" />

<img width="1917" height="1080" alt="tiếp của Generate Scripts" src="https://github.com/user-attachments/assets/9ebf19d7-e218-43f7-81f5-3474b2084b35" />

<img width="1919" height="1077" alt="save file" src="https://github.com/user-attachments/assets/7e08b174-c38f-4385-8d83-fb2cdaa01fe4" />

<img width="1920" height="1080" alt="lưu thành công" src="https://github.com/user-attachments/assets/ec3ea0ca-4549-4624-bbc3-54a108d6eed4" />

15.Sử dụng giao diện đồ hoạ của ssms: Xoá csdl đã tạo, sau khi xoá thành công, kiểm tra tại path (path chọn ở bước 6) xem còn tồn tại 2 file của bước 6 không?
<img width="1919" height="1080" alt="Chuyển sang database khác" src="https://github.com/user-attachments/assets/beda7289-93b2-458d-bcda-26b1063ac728" />
Chuyển sang databases mới
<img width="1920" height="1080" alt="xóa databases" src="https://github.com/user-attachments/assets/1cd389d2-6149-400a-823b-a752a04e474f" />
Xóa CSDL 
<img width="1920" height="1080" alt="qlsv biến mất" src="https://github.com/user-attachments/assets/2e5439dc-44c8-45a5-9444-5a30e688cae6" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/9efa5f7a-8ae3-4b38-95fc-85feeffdb867" />
kiểm tra tại path 

16.Tạo cửa sổ mới để gõ lệnh: mở file dulieu.sql của bước 14, chạy toàn bộ các lệnh này. REFRESH lại cây liệt kê các database => kiểm chứng kết quả được tạo ra tương đương với các bước 6,7,8,9,10,11,12,13.
<img width="1920" height="1080" alt="CHẠY LẠI FILE" src="https://github.com/user-attachments/assets/18aaefa4-cffb-4f52-86a1-53429c6beb4a" />
mở file dulieu.sql của bước 14, chạy toàn bộ các lệnh này
<img width="1920" height="1080" alt="ktra dữ liệu bài" src="https://github.com/user-attachments/assets/26b99ab2-46dc-49d5-952b-f2b9f55523f4" />
<img width="1920" height="1080" alt="ktra" src="https://github.com/user-attachments/assets/12f58ff3-b74c-4c04-8156-443b9278106c" />
<img width="1920" height="1080" alt="ktra 2" src="https://github.com/user-attachments/assets/a3bb59e3-9be8-460e-b26f-aaa2f0346fa7" />
Kiểm Tra 

17.Upload file dulieu.sql lên github repository của em (repository mà em đang edit file README.md)
<img width="1920" height="1076" alt="image" src="https://github.com/user-attachments/assets/594f27e5-d701-4be8-8b6d-6317055217bc" />































