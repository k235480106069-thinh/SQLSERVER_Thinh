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
# PHẦN 1: DATABASE + TABLE
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/32fae88e-2cdb-4a5f-9c83-9e17bcb4f1fd" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/eca51c0c-729f-479f-bb1c-fcb647fb5440" />
Ảnh này cho thấy tôi đã tạo thành công database QuanLyBanHang_K23548010069 và chuyển sang sử dụng database này để thực hiện các bước tiếp theo.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/45d20676-5dc3-46ed-a74c-67216ed06377" />
Ảnh này cho thấy tôi đã tạo thành công 3 bảng KhachHang, SanPham, HoaDon với các kiểu dữ liệu phù hợp.
- Các khóa chính (PK): maKhachHang, maSanPham, maHoaDon
- Các khóa ngoại (FK): maKhachHang và maSanPham trong bảng HoaDon
- Sử dụng NVARCHAR để hỗ trợ Unicode (tiếng Việt)
- Sử dụng CHECK để đảm bảo dữ liệu hợp lệ (giá > 0, số lượng >= 0)

# PHẦN 2: INSERT DATA
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/976f003c-652a-44c5-bf3d-656b4f066c04" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/882aa4d0-783a-4835-a460-cc817f5ebbff" />
Ảnh trên cho thấy tôi đã thêm dữ liệu mẫu vào các bảng KhachHang, SanPham, HoaDon. 
Kết quả SELECT cho thấy dữ liệu đã được lưu thành công và các bảng liên kết đúng với nhau thông qua khóa ngoại.
Dữ liệu này sẽ được sử dụng để kiểm tra các Function, Store Procedure và Trigger ở các phần tiếp theo.

# PHẦN 3: FUNCTION
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/07b4d7ea-9af1-4161-a88a-227097653e4a" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/14a9eb4f-6fc6-49e7-983d-da99cd566381" />
Hàm fn_TinhTongTienHoaDon được xây dựng để tính tổng tiền của một hóa đơn dựa trên giá sản phẩm và số lượng mua.
Hàm sử dụng phép JOIN giữa bảng HoaDon và SanPham để lấy giá sản phẩm, sau đó nhân với số lượng để tính tổng tiền.
Kết quả trả về là một giá trị kiểu MONEY.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/80da3870-2553-4729-8635-1181a20e4469" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/dcfacc10-b387-49df-9562-38a9993537e1" />
Hàm fn_DanhSachHoaDonTheoKhach là Inline Table-Valued Function dùng để trả về danh sách các hóa đơn của một khách hàng cụ thể.
Hàm sử dụng phép JOIN giữa bảng HoaDon và SanPham để hiển thị đầy đủ thông tin hóa đơn cùng với tên sản phẩm và giá.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/764ba675-a73c-4abf-afc9-e35a3d8eea74" />
<img width="1920" height="1079" alt="image" src="https://github.com/user-attachments/assets/c5acbb3a-30cb-4e3a-837f-ff222ad626a4" />
Hàm fn_TongTienTheoKhach là Multi-statement Table-Valued Function dùng để tính tổng tiền của tất cả hóa đơn theo từng khách hàng.
Hàm sử dụng biến bảng @ketQua để lưu kết quả, có khai báo biến @tong để tính tổng tiền thông qua phép SUM giữa giá sản phẩm và số lượng.
Khác với Inline Function, hàm này có nhiều bước xử lý logic trong khối BEGIN...END.

# PHẦN 4: STORED PROCEDURE
<img width="1917" height="1077" alt="image" src="https://github.com/user-attachments/assets/f54a2b3b-aa8f-4479-8445-b2e861fa1b13" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/1ee15a92-6666-44e1-acf1-ef1554f5f052" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/1dd27daa-82eb-4c0b-a6b4-f3aa51ae6b05" />
Store Procedure sp_ThemSanPham được xây dựng để thêm sản phẩm mới vào bảng SanPham.
Procedure có kiểm tra điều kiện logic: nếu giá sản phẩm nhỏ hơn hoặc bằng 0 thì không cho phép thêm và hiển thị thông báo lỗi.
Khi giá hợp lệ, dữ liệu sẽ được thêm vào bảng SanPham.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/cb5a18e4-6eed-4d29-8bd0-8027cfcf5aae" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f32225ae-f000-4e7b-95ab-26bd45bbcaa1" />
Store Procedure sp_TongTienKhachHang được sử dụng để tính tổng tiền của một khách hàng.
Procedure sử dụng tham số OUTPUT để trả về giá trị tổng tiền sau khi tính toán từ bảng HoaDon và SanPham.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c7c5d327-e902-45fc-ab12-d8bfda3da8fc" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/ef007f50-0329-47a5-969a-d60945f89116" />
Store Procedure sp_DanhSachHoaDon được xây dựng để trả về danh sách hóa đơn.
Procedure sử dụng JOIN giữa các bảng HoaDon, KhachHang và SanPham để hiển thị đầy đủ thông tin gồm tên khách hàng, tên sản phẩm và giá.

# PHẦN 5: TRIGGER
<img width="1914" height="1076" alt="image" src="https://github.com/user-attachments/assets/d7392126-6821-467f-8c26-8a72f2113709" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/188c03b3-04d3-43b8-adad-8744bcc720bb" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/0ad2fce5-1bcd-48ba-9a84-09929815a276" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/343196f0-d4ef-4516-93f2-62b16ca8a29c" />
Trigger trg_GiamSoLuongTon được tạo để tự động giảm số lượng tồn của sản phẩm khi có hóa đơn mới được thêm vào.
Khi thực hiện INSERT vào bảng HoaDon, trigger sẽ kích hoạt và cập nhật lại số lượng tồn trong bảng SanPham tương ứng.



