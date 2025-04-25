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
# chạy và đợi hki hoàn thành và ta đã có data base 
![image](https://github.com/user-attachments/assets/c086a20b-c0eb-447a-a9d5-df419e585a6f)
# với dữ liệu họ tên và nagỳ sinh 27-09-2004 Std: 0395345078 - tiến hành các ý 3-10
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




