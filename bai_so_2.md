# BÀI KIỂM TRA SỐ 2

## Thông tin sinh viên
- Họ tên: Nguyễn Đăng Thịnh
- MSSV: K235480106069
- Lớp: K59KMT.K01

## Yêu cầu bài toán
# Phần 1: Thiết kế và Khởi tạo Cấu trúc Dữ liệu (Kiến thức 6, 7)

Sinh viên tự chọn một chủ đề quản lý (Ví dụ: Quản lý thư viện, Quản lý khách sạn, hoặc Quản lý dự án, HOẶC BẤT KỲ BÀI TOÁN QUẢN LÝ NÀO KHÁC).

Tạo một Database mới với tên [Tên dự án]_[MaSV]. //LƯU Ý PHẢI CÓ MÃ SV CÁ NHÂN Ở TÊN CỦA DB ĐÚNG NHƯ YÊU CẦU, vd: QuanLyKhachSan_K123456789

Tạo ít nhất 3 bảng có quan hệ với nhau. Yêu cầu:

Sử dụng đa dạng các kiểu dữ liệu (Số nguyên, số thực, chuỗi ký tự Unicode, ngày tháng, tiền tệ, ...).

Áp dụng đúng quy tắc đặt tên (BướuLạcĐà).

Sử dụng cặp ngoặc [ ] để bọc tên bảng và tên trường trong script khởi tạo.

Có giải thích chỗ nào là PK, chỗ nào là FK, trường nào có ràng buộc cứng CK (ví dụ điểm từ 0..10),...

# Phần 2: Xây dựng Function (Kiến thức 8, 9)

Hãy cho biết trong SQL Server có những loại function build_in (hàm có sẵn) nào, nêu 1 vài system function build_in mà em tìm hiểu được (ko cần nhiều, cần đặc sắc theo góc nhìn của em), cho SQL khai thác các hàm đó.

Hàm do người dùng tự viết trong SQL thường mang mục đích gì? Nó có những loại nào? Mỗi loại thường được dùng khi nào? Tại sao có nhiều system function rồi mà vẫn cần tự viết fn riêng?

Viết 01 Scalar Function (Hàm trả về một giá trị): Đưa ra 1 logic cho cơ sở dữ liệu của em, mà cần dùng đến function này. (SV TỰ NGHĨ RA YÊU CẦU CỦA HÀM VÀ VIẾT HÀM GIẢI QUYẾT NÓ)

Sau khi đã có hàm, viết câu lệnh sql khai thác hàm đó.

Viết 01 Inline Table-Valued Function: Trả về danh sách các bản ghi theo một điều kiện lọc cụ thể (SV TỰ NGHĨ RA YÊU CẦU CỦA HÀM VÀ VIẾT HÀM GIẢI QUYẾT NÓ)

Sau khi đã có hàm, viết câu lệnh sql khai thác hàm đó.

Viết 01 Multi-statement Table-Valued Function: Thực hiện xử lý logic phức tạp bên trong (có sử dụng biến bảng) trước khi trả về kết quả. (SV TỰ NGHĨ RA YÊU CẦU CỦA HÀM VÀ VIẾT HÀM GIẢI QUYẾT NÓ)

Sau khi đã có hàm, viết câu lệnh sql khai thác hàm đó.

# Phần 3: Xây dựng Store Procedure (Kiến thức 10)

Trong SQL Server có những SP có sẵn nào? nêu 1 vài system sp mà em tìm hiểu được, giải thích cách dùng chúng.

Viết 01 Store Procedure đơn giản để thực hiện lệnh INSERT hoặc UPDATE dữ liệu, có kiểm tra điều kiện logic (SV TỰ NGHĨ RA YÊU CẦU CỦA SP VÀ VIẾT SP GIẢI QUYẾT NÓ)

Viết 01 Store Procedure có sử dụng tham số OUTPUT để trả về một giá trị tính toán (SV TỰ NGHĨ RA YÊU CẦU CỦA SP VÀ VIẾT SP GIẢI QUYẾT NÓ, SP NÀY CÓ DÙNG THAM SỐ LOẠI OUTPUT)

Viết 01 Store Procedure trả về một tập kết quả (Result set) từ lệnh SELECT sau khi đã join nhiều bảng. (SV TỰ NGHĨ RA YÊU CẦU CỦA SP VÀ VIẾT SP GIẢI QUYẾT NÓ)

# Phần 4: Trigger và Xử lý logic nghiệp vụ (Kiến thức 11)

Viết 01 Trigger để tự động làm gì đó tại 1 bảng B khi mà dữ liệu thay đổi dữ liệu ở bảng A. Logic giải quyết do sv tự nghĩ ra, sao cho thực tế và thuyết phục.

Thử viết Trigger cho Bảng A : Khi insert thì cập nhật dữ liệu vào bảng B; sau đó viết trigger cho bảng B để khi B được cập nhật thì cập nhật sang bảng A : Quan sát các thông báo (nếu có) của hệ thống, giải thích các thông báo đó (nếu có). Đưa ra nhật xét cuối cùng về tình trạng này.

# Phần 5: Cursor và Duyệt dữ liệu (Kiến thức 11)

Viết một đoạn script sử dụng CURSOR để duyệt qua danh sách của 1 câu lệnh SQL dạng SELECT, duyệt qua từng bản ghi, xử lý riêng từng bản ghi (THEO LOGIC SV TỰ ĐẶT RA: SAO CHO HỢP LÝ VÀ THUYẾT PHỤC)

Tìm cách không sử dụng CURSOR để giải quyết bài toán mà em đã dùng CURSOR mới giải quyết được ở trên. thử so sánh tốc độ giữa có dùng cursor và không dùng cursor (nếu cùng kết quả) thì thời gian xử lý cái nào nhanh hơn, cần ảnh chụp màn hình minh chứng.

Nếu vẫn tìm được cách dùng SQL để giải quyết vấn đề mà ko cần CURSOR: thử nghĩ bài toán khác, mà chỉ CURSOR mới giải quyết được, còn SQL rất khó giải quyết đc (theo logic suy nghĩ của em)
## Cách thực hiện
- Sử dụng SQL Server để tạo database và các bảng
- Áp dụng các ràng buộc khóa chính, khóa ngoại
- Sử dụng JOIN để xử lý dữ liệu giữa các bảng
- Kiểm tra kết quả bằng SELECT và EXEC
- 
# PHẦN 1: DATABASE + TABLE
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/32fae88e-2cdb-4a5f-9c83-9e17bcb4f1fd" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/eca51c0c-729f-479f-bb1c-fcb647fb5440" />
Trong 2 ảnh này, em đã thực hiện tạo database mới với tên là QuanLyBanHang_K23548010069 theo đúng yêu cầu đề bài (có kèm mã sinh viên).
Sau khi tạo xong, em sử dụng lệnh USE để chuyển sang database này nhằm thực hiện các bước tiếp theo.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/45d20676-5dc3-46ed-a74c-67216ed06377" />
Ảnh này thể hiện việc em đã tạo thành công 3 bảng gồm: KhachHang, SanPham, HoaDon.

Các bảng có liên kết với nhau thông qua khóa:
Khóa chính (PK): maKhachHang, maSanPham, maHoaDon
Khóa ngoại (FK): maKhachHang, maSanPham trong bảng HoaDon
Ngoài ra:
Sử dụng kiểu dữ liệu NVARCHAR để hỗ trợ tiếng Việt
Có dùng ràng buộc CHECK để đảm bảo dữ liệu hợp lệ (giá > 0, số lượng >= 0)

# PHẦN 2: INSERT DATA
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/976f003c-652a-44c5-bf3d-656b4f066c04" />
Ở phần này, em đã sử dụng lệnh INSERT INTO để thêm dữ liệu mẫu vào các bảng:

KhachHang
SanPham
HoaDon
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/882aa4d0-783a-4835-a460-cc817f5ebbff" />
Sau khi thêm dữ liệu, em dùng lệnh SELECT để kiểm tra.

Kết quả cho thấy:

Dữ liệu đã được thêm thành công
Các bảng liên kết đúng với nhau thông qua khóa ngoại

👉 Dữ liệu này dùng để test cho các phần Function, Procedure và Trigger phía sau.

# PHẦN 3: FUNCTION
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/07b4d7ea-9af1-4161-a88a-227097653e4a" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/14a9eb4f-6fc6-49e7-983d-da99cd566381" />
Em xây dựng hàm fn_TinhTongTienHoaDon để tính tổng tiền của một hóa đơn.

Cách hoạt động:
Lấy giá sản phẩm từ bảng SanPham
Nhân với số lượng trong bảng HoaDon
Có sử dụng JOIN giữa 2 bảng
Hàm trả về một giá trị kiểu MONEY

👉 Giúp tính toán nhanh mà không cần viết lại nhiều lần.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/80da3870-2553-4729-8635-1181a20e4469" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/dcfacc10-b387-49df-9562-38a9993537e1" />
Hàm fn_DanhSachHoaDonTheoKhach dùng để lấy danh sách hóa đơn của một khách hàng.

Hàm trả về một bảng dữ liệu
Có JOIN giữa HoaDon và SanPham
Hiển thị được:
Tên sản phẩm
Giá
Số lượng

👉 Dùng khi cần truy vấn dữ liệu theo điều kiện.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/764ba675-a73c-4abf-afc9-e35a3d8eea74" />
<img width="1920" height="1079" alt="image" src="https://github.com/user-attachments/assets/c5acbb3a-30cb-4e3a-837f-ff222ad626a4" />
Hàm fn_TongTienTheoKhach dùng để tính tổng tiền theo từng khách hàng.

Có sử dụng:
Biến bảng @ketQua
Biến trung gian để tính toán
Xử lý nhiều bước trong BEGIN...END

👉 Phù hợp với các bài toán phức tạp hơn so với Inline Function.

# PHẦN 4: STORED PROCEDURE
<img width="1917" height="1077" alt="image" src="https://github.com/user-attachments/assets/f54a2b3b-aa8f-4479-8445-b2e861fa1b13" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/1ee15a92-6666-44e1-acf1-ef1554f5f052" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/1dd27daa-82eb-4c0b-a6b4-f3aa51ae6b05" />
Procedure sp_ThemSanPham dùng để thêm sản phẩm mới.

Có kiểm tra điều kiện:
Nếu giá ≤ 0 thì báo lỗi
Nếu hợp lệ thì mới thêm vào database

👉 Giúp tránh dữ liệu sai ngay từ đầu.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/cb5a18e4-6eed-4d29-8bd0-8027cfcf5aae" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f32225ae-f000-4e7b-95ab-26bd45bbcaa1" />
Procedure sp_TongTienKhachHang dùng để tính tổng tiền của một khách hàng.

Có sử dụng tham số OUTPUT
Trả về tổng tiền sau khi tính toán

👉 Giúp tái sử dụng logic dễ dàng.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c7c5d327-e902-45fc-ab12-d8bfda3da8fc" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/ef007f50-0329-47a5-969a-d60945f89116" />
Procedure sp_DanhSachHoaDon dùng để hiển thị danh sách hóa đơn.

Có JOIN 3 bảng:
HoaDon
KhachHang
SanPham
Hiển thị đầy đủ thông tin:
Tên khách hàng
Tên sản phẩm
Giá

# PHẦN 5: TRIGGER
<img width="1914" height="1076" alt="image" src="https://github.com/user-attachments/assets/d7392126-6821-467f-8c26-8a72f2113709" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/188c03b3-04d3-43b8-adad-8744bcc720bb" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/0ad2fce5-1bcd-48ba-9a84-09929815a276" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/343196f0-d4ef-4516-93f2-62b16ca8a29c" />
Trigger trg_GiamSoLuongTon được tạo để tự động cập nhật số lượng tồn kho.

Khi thêm hóa đơn (INSERT vào HoaDon):
→ Trigger sẽ chạy
→ Giảm số lượng trong bảng SanPham

Công thức:

số lượng tồn = số lượng tồn - số lượng mua

👉 Giúp hệ thống tự động cập nhật, không cần làm thủ công.


