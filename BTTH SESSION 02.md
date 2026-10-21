---


---

<h1 id="báo-cáo-bài-tập-lớn--session-02---tổng-hợp-kiến-thức-hệ-thống">BÁO CÁO BÀI TẬP LỚN / SESSION 02 - TỔNG HỢP KIẾN THỨC HỆ THỐNG</h1>
<h2 id="phần-1-kiến-trúc-hệ-điều-hành-"><strong>Phần 1 Kiến trúc Hệ điều hành :</strong></h2>
<h6 id="theo-mục-3a-máy-của-bạn-đang-cùng-lúc-chạy-word-chrome-vs-code-và-phần-mềm-nộp-bài.-hãy-cho-biết-đây-là-hoạt-động-của-chức-năng-nào-trong-4-chức-năng-cốt-lõi-của-hdh-vì-sao-4-phần-mềm-này-chạy-được-cùng-lúc-mà-không-conflic-nhau"> <strong>1. Theo mục 3a, Máy của bạn đang cùng lúc chạy Word, Chrome, VS Code và phần mềm nộp bài. Hãy cho biết: đây là hoạt động của chức năng nào trong **4 chức năng cốt lõi** của HDH? Vì sao 4 phần mềm này chạy được cùng lúc mà không conflic nhau?</strong></h6>
<ul>
<li><strong>Chức năng: Quản lý tiến trình có công dụng điều phối CPU phân chia thời gian xử lý cho các phần mềm đang chạy, đảm bảo các ứng dụng hoạt động song song mượt mà và không bị xung đột tài nguyên nhờ vào đó  4 phần mềm này chạy được cùng lúc mà không conflic nhau</strong></li>
</ul>
<h6 id="khi-bạn-double-click-vào-file-báo-cáo-để-mở-hành-động-đó-thực-chất-được-xử-lý-qua-lớp-nào-trước-—-shell-hay-kernel-nêu-vai-trò-của-lớp-đó-và-vì-sao-người-dùng-thường-không-tương-tác-trực-tiếp-với-lớp-còn-lại."> <strong>2. Khi bạn double-click vào file báo cáo để mở, hành động đó thực chất được xử lý qua lớp nào trước — **Shell** hay **Kernel**? Nêu vai trò của lớp đó và vì sao người dùng thường không tương tác trực tiếp với lớp còn lại.</strong></h6>
<ul>
<li><strong>Khi bạn double-click vào file báo cáo để mở, hành động đó thực chất được xử lý qua lớp Shell trước, Shell nhận thao tác click chuột của người dùng, dịch thành lệnh rồi gửi xuống Kernel. Kernel tiếp nhận và trực tiếp điều khiển phần cứng (RAM, Disk).</strong></li>
<li><strong>Không tương tác trực tiếp Kernel: Vì Kernel là cốt lõi hệ thống; thao tác sai sót trực tiếp vào Kernel dễ dẫn đến sập toàn bộ hệ điều hành</strong></li>
</ul>
<h2 id="phần-2-cây-thư-mục--ổ-đĩa-"><strong>Phần 2 Cây thư mục &amp; Ổ đĩa :</strong></h2>
<p><strong>1. Dựa vào cây thư mục ở mục 3b, hãy xác định:</strong></p>
<ul>
<li> <strong>Đâu là **Root Directory**?</strong></li>
</ul>
<p><strong>D:\</strong></p>
<ul>
<li> <strong>Đâu là **Parent Directory** trực tiếp của file <code>anh 1.jpg</code>?</strong></li>
</ul>
<p><strong>\Hinh anh\</strong></p>
<ul>
<li> <strong>File <code>anh 1.jpg</code> đóng vai trò là “cành” hay “lá” trong mô hình cây thư mục?</strong></li>
</ul>
<p><strong>đóng vai trò lá vì là thư mục cuối cùng</strong></p>
<p> <strong>2. Giả sử toàn bộ dự án đang nằm ở <code>Desktop</code> hoặc <code>Downloads</code> (thuộc User Profile trên ổ <code>C:\\</code>). Nêu **2 lý do kỹ thuật** đây là lựa chọn nguy hiểm và đề xuất nơi lưu đúng.</strong></p>
<ul>
<li><strong>Rất dễ bị mất file khi reset máy tính, và bị lỗi đường dẫn User trên máy khác</strong></li>
</ul>
<h3 id="phần-3-—-đường-dẫn-path-"><strong>Phần 3 — Đường dẫn Path :</strong></h3>
<p><strong>1. Viết **Absolute Path** đầy đủ, chính xác của file <code>anh 1.jpg</code> trong cây thư mục ở mục 3b.</strong></p>
<ul>
<li><strong>D:\Nam1\HocKy1\MonHoc\CongNgheThongTin\BaiTapLon\Session02\BaoCaoCuoiKy\Chuong1\Hinh anh\anh 1.jpg</strong></li>
</ul>
<p><strong>2. Dựa vào cấu trúc dự án ở mục 3e, hãy viết **Relative Path** để chèn file <code>logo.png</code> vào trong file <code>report.html</code> (sử dụng đúng ký hiệu <code>.</code> hoặc <code>..</code> nếu cần). Giải thích ngắn gọn vì sao dùng **Relative Path** ở đây sẽ giúp dự án không bị lỗi khi bạn nén thư mục <code>BaiTapLonIT101</code> gửi cho giảng viên qua máy khác.</strong></p>
<ul>
<li>img src=“assets/logo.png” alt=“Logo”</li>
<li><strong>Sử dụng Relative Path giúp đường dẫn mang tính linh hoạt cao. Khi bạn nén thư mục BaiTapLonIT101 gửi cho giảng viên chạy trên máy tính khác (có thể ổ đĩa không phải là D:\ mà là E:\ hoặc C:\), đường dẫn vẫn được giữ nguyên tính chính xác dựa trên cấu trúc thư mục nội bộ, tránh tuyệt đối lỗi File Not Found.</strong></li>
</ul>
<h2 id="phần-4-—-quy-tắc-đặt-tên-chuẩn"><strong>Phần 4 — Quy tắc Đặt tên chuẩn</strong></h2>
<p><strong>1. Đổi tên file ở mục 3c — <code>Báo cáo bài tập lớn IT101 (bản cuối) v2.docx</code> — thành một tên file chuẩn theo <code>kebab-case</code>.</strong></p>
<ul>
<li><strong>bao-cao-bai-tap-lon-it101-v2.docx</strong></li>
</ul>
<h2 id="phần-5-—-tổ-chức--dọn-dẹp-ổ-đĩa"><strong>Phần 5 — Tổ chức &amp; Dọn dẹp Ổ đĩa</strong></h2>
<p><strong>1. Đường dẫn ở mục 3b đang lồng bao nhiêu cấp thư mục? Vi phạm quy tắc nào mà các bạn đã được học ? Hãy thiết kế lại đường dẫn thư mục chứa file <code>anh 1.jpg</code> sao cho tuân thủ **Quy tắc 3 Cấp Thư Mục** và mô hình **4 Trụ Cột** (<code>01\_HocTap</code>, <code>02\_Projects</code>, <code>03\_Personal</code>, <code>04\_Media</code>) trên ổ <code>D:\\</code>.</strong></p>
<ul>
<li><strong>Đánh giá: Đường dẫn cũ lồng 9 cấp (tính từ gốc ổ D:), vi phạm nghiêm trọng Quy tắc 3 Cấp Thư Mục (quá sâu, dễ quá giới hạn 260 ký tự path của Windows).</strong></li>
</ul>
<p><strong>Cấu trúc mới chuẩn 3 cấp &amp; 4 Trụ Cột (trên ổ D:):</strong></p>
<p><strong>Cấp 1 (Trụ cột): D:\01_HocTap\</strong></p>
<p><strong>Cấp 2 (Môn học): D:\01_HocTap\IT101\</strong></p>
<p><strong>Cấp 3 (Dự án/Bài tập): D:\01_HocTap\IT101\BaiTapLonSession02\</strong></p>
<p><strong>Đường dẫn tối ưu chứa file: D:\01_HocTap\IT101\BaiTapLonSession02\anh-1.jpg</strong></p>
<h2 id="phần-6-—-đuôi-file--file-ẩn"><strong>Phần 6 — Đuôi file &amp; File ẩn</strong></h2>
<p><strong>1. File ở mục 3d hiển thị là <code>de-thi-dap-an.pdf</code> nhưng máy đang ẩn đuôi mở rộng. Hãy giải thích: đây có thể là cạm bẫy gì, tên file thật có khả năng là gì, và thao tác cụ thể nào trong Windows File Explorer giúp bạn phát hiện ra sự thật này **trước khi** nhấp đôi chuột mở file?</strong></p>
<ul>
<li><strong>Cạm bẫy: Kẻ xấu lợi dụng tính năng ẩn đuôi file của Windows để phát tán mã độc.</strong></li>
<li><strong>Tên file thật có thể là: de-thi-dap-an.pdf.exe hoặc de-thi-dap-an.pdf.scr (file thực thi mã độc núp bóng file PDF).</strong></li>
<li><strong>Cách hiển thị lại đuôi file:</strong></li>
</ul>
<p><strong>Mở File Explorer -&gt; Chọn tab View -&gt; Tích chọn File name extensions.</strong></p>

