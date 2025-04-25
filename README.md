# Lương Quốc Đệ mssv K225480106004 
Bài tập 6: Hệ quản trị CSDL
Chủ đề: Câu lệnh Select
Yêu cầu bài tập: 
Cho file sv_tnut.sql (1.6MB)
1. Hãy nêu các bước để import được dữ liệu trong sv_tnut.sql vào sql server của em
2. dữ liệu đầu vào là tên của sv; sđt; ngày, tháng, năm sinh của sinh viên (của sv đang làm bài tập này)
3. nhập sql để tìm xem có những sv nào trùng hoàn toàn ngày/tháng/năm với em?
4. nhập sql để tìm xem có những sv nào trùng ngày và tháng sinh với em?
5. nhập sql để tìm xem có những sv nào trùng tháng và năm sinh với em?
6. nhập sql để tìm xem có những sv nào trùng tên với em?
7. nhập sql để tìm xem có những sv nào trùng họ và tên đệm với em.
8. nhập sql để tìm xem có những sv nào có sđt sai khác chỉ 1 số so với sđt của em.
9. BẢNG SV CÓ HƠN 9000 ROWS, HÃY LIỆT KÊ TẤT CẢ CÁC SV NGÀNH KMT, SẮP XẾP THEO TÊN VÀ HỌ ĐỆM, KIỂU TIẾNG  VIỆT, GIẢI THÍCH.
10. HÃY NHẬP SQL ĐỂ LIỆT KÊ CÁC SV NỮ NGÀNH KMT CÓ TRONG BẢNG SV (TRÌNH BÀY QUÁ TRÌNH SUY NGHĨ VÀ GIẢI NHỮNG VỨNG MẮC)

Ghi chú: Giải thích tại sao lại có SQL như vậy.


# tiến hành import với tài khoản SSMS của máy, với các bước cơ bảng là tạo Data base và Open file .Sql bằng SSMS 
![Screenshot 2025-04-25 182229](https://github.com/user-attachments/assets/7c54da10-28f5-4f65-9b55-a1da96bb3dde)
# *Lưu ý ki tiến hành chạy code file .sql hãy chú ý tới việc sử dụng data base chính xác
![Screenshot 2025-04-25 182659](https://github.com/user-attachments/assets/e1fc08a6-94e1-44ed-98e6-a8779ac599b0)
# chạy và đợi khi hoàn thành và ta đã có data base 
![image](https://github.com/user-attachments/assets/c086a20b-c0eb-447a-a9d5-df419e585a6f)
# với dữ liệu họ tên và ngày sinh 27-09-2004 Std: 0395345078 - tiến hành các ý 3-10
# sinh viên trùng ngày tháng năm sử dụng lệch select vào cột ns đưa ra 
![image](https://github.com/user-attachments/assets/f1f3f0f5-874f-4cfb-be51-52e53a2e3e55)
# tương tự với trùng ngày tháng sinh với nhưng ở đây ta chọn ngày và tháng với hỗ trợ lệnh của dạng Date
![image](https://github.com/user-attachments/assets/b0837e63-12a1-4469-91aa-af7cdcca08f1)
# và làm như v với  tháng và năm 
![image](https://github.com/user-attachments/assets/71f9ee12-4381-4f78-8d80-4ea20f5e7680)
# với tìm tên ta select cột tên với ... tên đệ thôi 
![image](https://github.com/user-attachments/assets/1eb94a82-6740-44cd-a7ac-f726480c844a)
dữ liệu của tất cả các trường chưa chắc có ai trùng tên :)
# với họ và đệm ta quét cột hodem 
![image](https://github.com/user-attachments/assets/cb3e617a-1d93-4e50-a2ad-d930d9387509)
# ta có thể thấy với cột Sdt dữ liệu đã bị khuyết mất số 0 vậy nên ta đi con đường ngắn là tìm kiếm với dữ liệu đầu vào khuyết số 0 
# là 395345078 để thực hiện yêu cầu trên ngoài việc chỉ quét cột sdt không ta còn cần quét từng số có 2 cách: 
# 1 là lặp để kiểm tra từng số 
![image](https://github.com/user-attachments/assets/d2d3efc3-3235-4886-a7db-e1de82408e02)
# chỉ việc lặp từng vị trí số để so sánh nhưng sẽ vừa lâu vừa mỏi nên ta có cách 2 là dùng hàm đếm
# với việc dùng hàm để đếm xem số khác biệt trong sdt là bao nhiêu nếu chỉ 1 ký tự số sai thôi thì tiến hành in còn không thì bỏ qua
![image](https://github.com/user-attachments/assets/8c2032db-0d28-4d96-9eea-9c6b470f802d)
# sau khi tạo hàm trên ta sẽ sử dụng hàm để so sánh với cách này về sau khi tiến hành tìm ta chỉ cần gọi hàm ra thôi không cần phải viết lại câu lặp nữa
![image](https://github.com/user-attachments/assets/5225cd53-362d-411a-951b-c78a4d920fc6)
# và nêu như ta không muốn tự cắt số 0 ví dụ như đưa cho người khác họ không biết thì sao 
# ta khi so sánh sẽ chuẩn hóa dữ liệu sdt tạm tời với số 0 ở đầu 
![image](https://github.com/user-attachments/assets/e190e875-0657-4fae-ab6e-545e1e9d15ec)
# với cách này sẽ giúp tốii ưu hết mức và cũng tránh thiếu sót nêu 1 vài dữ liệu có đủ sdt 

# với yêu cầu tìm mã lớp nhưng không có cột ngành dựa vào mã lớp do theo mã lớp chuỗi ký tự KMT  sẽ biểu thị cho học sinh lớp ngành KMT 
![image](https://github.com/user-attachments/assets/729b9163-0707-433b-82a2-ac3d4c63822c)
# để đữ sắp theo tên tiêng việt ta có thể thấy lệnh COLLATE Vietnamese_CI_AS tìm theo tiếng việt CI là khôn gphân biệt hoa thường và AS là xác định cả dấu
# với yêu cầu cuối là tìm thêm cả giới tính là nữ nhưng không có cột giới tính ta có cách tìm chính xác khoảng gần đúng hết 
# ta có thể thấy ở Việt Nam ta thấy rằng các lên của nữ thường sẽ là 
Lan, Hương, Mai, Ngọc, Yến, Thu,Hà,Phương, Anh, Hiền và tất cả các tên bạn có thể nghĩ ra ờm có thể tham khảo qua bách khoa
https://hoten.org/100-ten-nu-gioi-pho-bien/
![image](https://github.com/user-attachments/assets/0afd562d-aba5-4a71-b99a-21eac58d9583)
# ngoài ra còn có các loại tên đệp nữa Thị, Ngọc, Thu, Mai, Thanh, Diệu, Bích, Trà, Lan, Hồng ... với tất cả những gì mình biết
![image](https://github.com/user-attachments/assets/8ca5386a-0fb3-4ea6-a4a5-3965d3dcec6e)
# nhưng nếu tìm tên đệp sẽ bị lẫn cách bạn nam do tên có thể khác như Phương Nam chẳng hạn
# vậy sẽ ra sao nếu cả 2 phương thức lọc trên dùng 1 lúc ... nó sẽ quét Đệm trước để tìm các người có đệm mang tính nữ và sau đó quét tên để xác định tên nữ
![image](https://github.com/user-attachments/assets/01db33b5-90c2-4345-8711-cb30d71ca383)
# vậy cách trên sẽ tối ưu trong việc tìm kiếm tên của ai là nữ trong KMT nhưng sẽ không tôi ưu trong tìm hết tất cả các tên và sẽ bị sót vì tên mà có người có thể 
# tên có vẻ là nam nhưng lại là nữ ( như cô mình tên Quốc Việt nhưng lại là nữ vậy) nên để tối ưu nhất vẫn là nhập giới tính vào 1 bảng để phân biệt và lọc dẽ hơn.










