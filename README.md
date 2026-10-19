# CNTT1-nh-p-m-n-c-ng-ngh-th-ng-tin-Session11_Ex02
### 1. Phân tích lỗi (Vi phạm 3 Quy tắc Vàng)

1. **Gộp ô (Merge Cells) ở tiêu đề/dữ liệu:** Làm đứt gãy cấu trúc bảng, khiến Excel không nhận diện đúng cột và gây lỗi khi lọc, sắp xếp hoặc dùng công thức.
2. **Tồn tại hàng/cột trống hoàn toàn (Blank Rows/Columns):** Khi nhấn `Ctrl + Shift + L`, Excel chỉ tự động nhận diện vùng dữ liệu liên tục đến trước hàng trống. Hàng trống làm ngắt vùng (Data Region), khiến Filter bị mất hiệu lực ở phần dưới.
3. **Dữ liệu không chuẩn hóa (Khoảng trắng thừa/Inconsistent Data):** Nhập thừa dấu cách đầu/cuối chuỗi làm Excel hiểu "Hỏng " và "Hỏng" là hai giá trị khác nhau, dẫn đến thống kê và lọc sai lệch.

---

### 2. Các bước hoàn thiện & Xử lý

1. **Gỡ bỏ Merge Cells & Sửa tiêu đề:**
* Chọn toàn bộ bảng $\rightarrow$ Bấm nút **Merge & Center** trên thanh công cụ để gỡ gộp ô.
* Điền lại tiêu đề cho rõ ràng trên từng cột duy nhất.


2. **Xóa hàng trống ngắt đoạn:**
* Bôi đen vùng dữ liệu $\rightarrow$ Bấm `F5` (hoặc `Ctrl + G`) $\rightarrow$ Chọn **Special...** $\rightarrow$ Tích chọn **Blanks** $\rightarrow$ **OK**.
* Nhấp chuột phải vào dòng trống đang chọn $\rightarrow$ **Delete** $\rightarrow$ **Table Rows** (hoặc **Shift cells up**).


3. **Làm sạch dữ liệu bằng hàm TRIM:**
* Tạo một cột phụ bên cạnh cột "Trạng thái".
* Gõ công thức: `=TRIM(C2)` *(với C2 là ô chứa trạng thái ban đầu)* rồi kéo xuống hết bảng.
* Copy cột mới $\rightarrow$ Paste Values đè lại vào cột "Trạng thái" cũ $\rightarrow$ Xóa cột phụ.


4. **Kích hoạt lại AutoFilter:**
* Chọn một ô bất kỳ trong bảng dữ liệu sạch.
* Bấm `Ctrl + Shift + L` để bật lại Filter. Lúc này menu lọc chỉ còn 1 nhóm "Hỏng" chuẩn và hoạt động xuyên suốt toàn bộ bảng.
