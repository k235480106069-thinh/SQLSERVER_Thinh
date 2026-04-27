# BÀI KIỂM TRA SỐ 2

## Thông tin sinh viên
- Họ tên: Nguyễn Đăng Thịnh
- MSSV: K235480106069
- Lớp: K59KMT.K01

## Yêu cầu bài toán
Xây dựng hệ thống quản lý bán hàng gồm:
- Tạo database và các bảng (KhachHang, SanPham, HoaDon)
- Thêm dữ liệu mẫu
- Xây dựng các Function
- Xây dựng Stored Procedure
- Xây dựng Trigger

## Cách thực hiện
- Sử dụng SQL Server để tạo database và các bảng
- Áp dụng các ràng buộc khóa chính, khóa ngoại
- Sử dụng JOIN để xử lý dữ liệu giữa các bảng
- Kiểm tra kết quả bằng SELECT và EXEC
# PHẦN 1: DATABASE + TABLE
<img width="1910" height="1067" alt="image" src="https://github.com/user-attachments/assets/e37827c5-949e-4b12-ac27-e718900f5a9b" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/1c1faf91-2a30-4267-94ac-0613d2a0aaee" />
Ảnh này cho thấy tôi đã tạo thành công database QuanLyBanHang_K23548010069 và chuyển sang sử dụng database này để thực hiện các bước tiếp theo.
<img width="1917" height="1079" alt="image" src="https://github.com/user-attachments/assets/f45e519d-28de-413b-bfe5-a045b01b76b4" />
Ảnh này cho thấy tôi đã tạo thành công 3 bảng KhachHang, SanPham, HoaDon với các kiểu dữ liệu phù hợp. 
Trong đó:
- maKhachHang, maSanPham, maHoaDon là khóa chính (PK)
- maKhachHang và maSanPham trong bảng HoaDon là khóa ngoại (FK)
- Các ràng buộc CHECK đảm bảo dữ liệu hợp lệ (giá > 0, số lượng >= 0)

# PHẦN 2: INSERT DATA
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6df258b8-0253-4e2d-a9c3-3b5734f43d3c" />
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/d1fc1856-174c-4a4f-b0ac-50853f9beac8" />
Ảnh này cho thấy tôi đã thêm dữ liệu mẫu vào các bảng KhachHang, SanPham, HoaDon. 
Dữ liệu này sẽ được sử dụng để kiểm tra các Function, Store Procedure và Trigger ở các phần sau.

# PHẦN 3: FUNCTION
<img width="1920" height="1077" alt="image" src="https://github.com/user-attachments/assets/fe44aced-6003-4902-a0aa-b04a1fe86830" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/5e0934e6-9af6-402e-b261-cd737fcef59b" />
Hàm fn_TinhTongTienHoaDon được xây dựng để tính tổng tiền của một hóa đơn dựa trên giá sản phẩm và số lượng mua.
Hàm sử dụng phép JOIN giữa bảng HoaDon và SanPham để lấy giá sản phẩm, sau đó nhân với số lượng để tính tổng tiền.
Kết quả trả về là một giá trị kiểu MONEY.

<img width="1881" height="1053" alt="image" src="https://github.com/user-attachments/assets/4b5cf433-5193-4a4b-87a3-5dea3b0d9cd6" />
<img width="1892" height="1053" alt="image" src="https://github.com/user-attachments/assets/1c810a02-5868-4240-bac0-74f25be5b914" />
Hàm fn_DanhSachHoaDonTheoKhach là Inline Table-Valued Function dùng để trả về danh sách các hóa đơn của một khách hàng cụ thể.
Hàm sử dụng phép JOIN giữa bảng HoaDon và SanPham để hiển thị đầy đủ thông tin hóa đơn cùng với tên sản phẩm và giá.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c2813b48-00b4-491e-aa8f-fa57e26d7339" />
<img width="1883" height="1038" alt="image" src="https://github.com/user-attachments/assets/f7c12a3a-680d-4ecf-9f4e-1d959a322cff" />
Hàm fn_TongTienTheoKhach là Multi-statement Table-Valued Function dùng để tính tổng tiền của tất cả hóa đơn theo từng khách hàng.
Hàm sử dụng biến bảng @ketQua để lưu kết quả, có khai báo biến @tong để tính tổng tiền thông qua phép SUM giữa giá sản phẩm và số lượng.
Khác với Inline Function, hàm này có nhiều bước xử lý logic trong khối BEGIN...END.

# PHẦN 4: STORED PROCEDURE
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/503fc661-74ba-4275-8807-87a264bcea84" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6cd40d7e-3697-4b60-b1d9-1cfc0e2e4e62" />
<img width="1918" height="1079" alt="image" src="https://github.com/user-attachments/assets/32484718-0163-45a6-bd6b-5c2176b1fdcf" />
Store Procedure sp_ThemSanPham được xây dựng để thêm sản phẩm mới vào bảng SanPham.
Procedure có kiểm tra điều kiện logic: nếu giá sản phẩm nhỏ hơn hoặc bằng 0 thì không cho phép thêm và hiển thị thông báo lỗi.
Khi giá hợp lệ, dữ liệu sẽ được thêm vào bảng SanPham.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/8ffc4e36-ae86-49f9-abd6-a92e85e6953c" />
<img width="1920" height="1079" alt="image" src="https://github.com/user-attachments/assets/ec520bd1-a1ce-4ae0-b8b7-06afd3492bf2" />
Store Procedure sp_TongTienKhachHang được sử dụng để tính tổng tiền của một khách hàng.
Procedure sử dụng tham số OUTPUT để trả về giá trị tổng tiền sau khi tính toán từ bảng HoaDon và SanPham thông qua phép JOIN.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/db2f5277-edc1-473c-bbd1-adcd27d25b3b" />
<img width="1916" height="1080" alt="image" src="https://github.com/user-attachments/assets/355d541a-1247-4f02-bc90-067751a85820" />
Store Procedure sp_DanhSachHoaDon được xây dựng để trả về danh sách hóa đơn.
Procedure sử dụng JOIN giữa các bảng HoaDon, KhachHang và SanPham để hiển thị đầy đủ thông tin gồm tên khách hàng, tên sản phẩm và giá.

# PHẦN 5: TRIGGER
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/8d8e30eb-e5ce-4880-a864-3eb84d0b3378" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c0d4eba3-a72e-47b5-a4c0-27352c8ab80a" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6d8be090-a9d5-4513-9afb-85f8333e25b8" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/766e14a4-cb70-4578-9c2f-82e84d32265f" />
Trigger trg_GiamSoLuongTon được tạo để tự động giảm số lượng tồn của sản phẩm khi có hóa đơn mới được thêm vào.
Khi thực hiện INSERT vào bảng HoaDon, trigger sẽ kích hoạt và cập nhật lại số lượng tồn trong bảng SanPham tương ứng.










