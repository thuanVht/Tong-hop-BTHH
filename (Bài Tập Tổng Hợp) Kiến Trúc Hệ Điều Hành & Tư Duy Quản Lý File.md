(Bài Tập Tổng Hợp) Kiến Trúc Hệ Điều Hành & Tư Duy Quản Lý File
Phần 1 Kiến trúc Hệ điều hành :
 1. Theo mục 3a, Máy của bạn đang cùng lúc chạy Word, Chrome, VS Code và phần mềm nộp bài. Hãy cho biết: đây là hoạt động của chức năng nào trong **4 chức năng cốt lõi** của HDH? Vì sao 4 phần mềm này chạy được cùng lúc mà không conflic nhau?
Chức năng: Quản lý tiến trình có công dụng điều phối CPU phân chia thời gian xử lý cho các phần mềm đang chạy, đảm bảo các ứng dụng hoạt động song song mượt mà và không bị xung đột tài nguyên nhờ vào đó  4 phần mềm này chạy được cùng lúc mà không conflic nhau
 2. Khi bạn double-click vào file báo cáo để mở, hành động đó thực chất được xử lý qua lớp nào trước — **Shell** hay **Kernel**? Nêu vai trò của lớp đó và vì sao người dùng thường không tương tác trực tiếp với lớp còn lại.
Khi bạn double-click vào file báo cáo để mở, hành động đó thực chất được xử lý qua lớp Shell trước, Shell nhận thao tác click chuột của người dùng, dịch thành lệnh rồi gửi xuống Kernel. Kernel tiếp nhận và trực tiếp điều khiển phần cứng (RAM, Disk).
Không tương tác trực tiếp Kernel: Vì Kernel là cốt lõi hệ thống; thao tác sai sót trực tiếp vào Kernel dễ dẫn đến sập toàn bộ hệ điều hành
Phần 2 Cây thư mục & Ổ đĩa :
1. Dựa vào cây thư mục ở mục 3b, hãy xác định:
 Đâu là **Root Directory**?
D:\
 Đâu là **Parent Directory** trực tiếp của file `anh 1.jpg`?
\Hinh anh\
 File `anh 1.jpg` đóng vai trò là "cành" hay "lá" trong mô hình cây thư mục?
đóng vai trò lá vì là thư mục cuối cùng
 2. Giả sử toàn bộ dự án đang nằm ở `Desktop` hoặc `Downloads` (thuộc User Profile trên ổ `C:\`). Nêu **2 lý do kỹ thuật** đây là lựa chọn nguy hiểm và đề xuất nơi lưu đúng.
Rất dễ bị mất file khi reset máy tính, và bị lỗi đường dẫn User trên máy khác
Phần 3 — Đường dẫn Path :

1. Viết **Absolute Path** đầy đủ, chính xác của file `anh 1.jpg` trong cây thư mục ở mục 3b.
D:\Nam1\HocKy1\MonHoc\CongNgheThongTin\BaiTapLon\Session02\BaoCaoCuoiKy\Chuong1\Hinh anh\anh 1.jpg
2. Dựa vào cấu trúc dự án ở mục 3e, hãy viết **Relative Path** để chèn file `logo.png` vào trong file `report.html` (sử dụng đúng ký hiệu `.` hoặc `..` nếu cần). Giải thích ngắn gọn vì sao dùng **Relative Path** ở đây sẽ giúp dự án không bị lỗi khi bạn nén thư mục `BaiTapLonIT101` gửi cho giảng viên qua máy khác.
<img src="assets/logo.png" alt="Logo">
Sử dụng Relative Path giúp đường dẫn mang tính linh hoạt cao. Khi bạn nén thư mục BaiTapLonIT101 gửi cho giảng viên chạy trên máy tính khác (có thể ổ đĩa không phải là D:\ mà là E:\ hoặc C:\), đường dẫn vẫn được giữ nguyên tính chính xác dựa trên cấu trúc thư mục nội bộ, tránh tuyệt đối lỗi File Not Found.
Phần 4 — Quy tắc Đặt tên chuẩn
1. Đổi tên file ở mục 3c — `Báo cáo bài tập lớn IT101 (bản cuối) v2.docx` — thành một tên file chuẩn theo `kebab-case`.
bao-cao-bai-tap-lon-it101-v2.docx
Phần 5 — Tổ chức & Dọn dẹp Ổ đĩa
1. Đường dẫn ở mục 3b đang lồng bao nhiêu cấp thư mục? Vi phạm quy tắc nào mà các bạn đã được học ? Hãy thiết kế lại đường dẫn thư mục chứa file `anh 1.jpg` sao cho tuân thủ **Quy tắc 3 Cấp Thư Mục** và mô hình **4 Trụ Cột** (`01_HocTap`, `02_Projects`, `03_Personal`, `04_Media`) trên ổ `D:\`.

Đánh giá: Đường dẫn cũ lồng 9 cấp (tính từ gốc ổ D:), vi phạm nghiêm trọng Quy tắc 3 Cấp Thư Mục (quá sâu, dễ quá giới hạn 260 ký tự path của Windows).
Cấu trúc mới chuẩn 3 cấp & 4 Trụ Cột (trên ổ D:):
Cấp 1 (Trụ cột): D:\01_HocTap\
Cấp 2 (Môn học): D:\01_HocTap\IT101\
Cấp 3 (Dự án/Bài tập): D:\01_HocTap\IT101\BaiTapLonSession02\
Đường dẫn tối ưu chứa file: D:\01_HocTap\IT101\BaiTapLonSession02\anh-1.jpg
Phần 6 — Đuôi file & File ẩn
1. File ở mục 3d hiển thị là `de-thi-dap-an.pdf` nhưng máy đang ẩn đuôi mở rộng. Hãy giải thích: đây có thể là cạm bẫy gì, tên file thật có khả năng là gì, và thao tác cụ thể nào trong Windows File Explorer giúp bạn phát hiện ra sự thật này **trước khi** nhấp đôi chuột mở file?
Cạm bẫy: Kẻ xấu lợi dụng tính năng ẩn đuôi file của Windows để phát tán mã độc.
Tên file thật có thể là: de-thi-dap-an.pdf.exe hoặc de-thi-dap-an.pdf.scr (file thực thi mã độc núp bóng file PDF).
Cách hiển thị lại đuôi file:
Mở File Explorer -> Chọn tab View -> Tích chọn File name extensions.
