---


---

<h1 id="bài-làm-bài-tập-tổng-hợp-tech-lead-cyber-arena">BÀI LÀM: BÀI TẬP TỔNG HỢP TECH LEAD CYBER ARENA</h1>
<h2 id="phần-1-–-lĩnh-vực-cntt-và-đơn-vị-lưu-trữ">PHẦN 1 – LĨNH VỰC CNTT VÀ ĐƠN VỊ LƯU TRỮ</h2>
<h3 id="lựa-chọn-ứng-viên-kỹ-thuật">1. Lựa chọn ứng viên kỹ thuật</h3>
<p>Lựa chọn: Chọn Ứng viên B (Mạng máy tính / Quản trị hệ thống).</p>
<p>Giải thích: Nhu cầu cấp thiết nhất của Cyber Arena lúc này là duy trì hệ thống phòng máy vận hành ổn định, xử lý sự cố phần cứng, lắp ráp cấu hình và tối ưu đường truyền mạng để phục vụ cả khách chơi game lẫn livestream/thi đấu. Việc viết ứng dụng đặt lịch (của ứng viên A) chưa phải là ưu tiên sinh tử và có thể tạm thời sử dụng các phần mềm quản lý phòng máy có sẵn trên thị trường.</p>
<h3 id="sắp-xếp-các-đơn-vị-lưu-trữ-theo-thứ-tự-tăng-dần">2. Sắp xếp các đơn vị lưu trữ theo thứ tự tăng dần</h3>
<p>Byte &lt; KB &lt; MB &lt; GB &lt; TB</p>
<h2 id="phần-2-–-mô-hình-ipo-và-lĩnh-vực-cntt">PHẦN 2 – MÔ HÌNH IPO VÀ LĨNH VỰC CNTT</h2>
<h3 id="bảng-mô-hình-ipo-hệ-thống-quay--xem-lại-trận-đấu">1. Bảng mô hình IPO hệ thống quay / xem lại trận đấu</h3>
<p>Thành phần</p>
<p>Trong hệ thống quay/xem lại trận đấu</p>
<p>Input</p>
<p>Tín hiệu hình ảnh/âm thanh từ màn hình chơi game và camera/micro của tuyển thủ.</p>
<p>Process</p>
<p>Phần mềm mã hóa (encode) tín hiệu video/audio và nén thành file định dạng MP4.</p>
<p>Output</p>
<p>Video trận đấu hiển thị trên màn hình xem lại hoặc luồng phát trực tiếp (livestream) lên YouTube.</p>
<p>Storage</p>
<p>Ổ cứng SSD (hoặc thiết bị lưu trữ) dùng để lưu trữ lại các file video trận đấu (.mp4).</p>
<h3 id="lĩnh-vực-cntt-gắn-với-hoạt-động-của-cyber-arena">2. Lĩnh vực CNTT gắn với hoạt động của Cyber Arena</h3>
<p>Mạng máy tính &amp; Truyền thông: Phụ trách đảm bảo đường truyền internet cáp quang băng thông rộng, độ trễ thấp để truyền tải dữ liệu livestream ổn định lên YouTube và kết nối game mượt mà.</p>
<p>Quản trị hệ thống &amp; Phần cứng (Computer Hardware &amp; System Administration): Phụ trách quản lý, bảo trì cấu hình phòng máy, tối ưu hóa khả năng xử lý phần cứng và lưu trữ video trận đấu.</p>
<h2 id="phần-3-–-tính-toán-dung-lượng-và-tốc-độ-mạng">PHẦN 3 – TÍNH TOÁN DUNG LƯỢNG VÀ TỐC ĐỘ MẠNG</h2>
<h3 id="tính-dung-lượng-lưu-trữ">1. Tính dung lượng lưu trữ</h3>
<p>Tổng dung lượng 20 trận (MB):</p>
<p>20trận500MB/trận=10.000MB</p>
<p>Đổi sang GB (dùng chuẩn 1GB=1.024MB theo ràng buộc):</p>
<p>10.000MB1.0249,77GB</p>
<p>Đánh giá khả năng lưu trữ của SSD 512 GB:</p>
<p>SSD 512 GB chứa thừa đủ video của 1 tháng (9,77GB&lt;512GB).</p>
<p>Dung lượng còn trống sau 1 tháng vận hành đầu tiên:</p>
<p>512GB-9,77GB=502,23GB</p>
<h3 id="tính-tốc-độ-mạng-và-thời-gian-upload">2. Tính tốc độ mạng và thời gian Upload</h3>
<p>Tốc độ mạng tối đa ra MB/s (dùng công thức MB/s=Mbps8):</p>
<p>100Mbps8=12,5MB/s</p>
<p>Thời gian tối thiểu tải lên (Upload) video 200 MB:</p>
<p>Thờigian=200MB12,5MB/s=16giây</p>
<p>1 Lý do thực tế thời gian tải lên thường lâu hơn tính toán:</p>
<p>Do sự hao hụt băng thông/suy hao tín hiệu đường truyền (ngẽn mạng cục bộ, sự cố hạ tầng ISP) hoặc do giới hạn tốc độ ghi/xử lý nhận dữ liệu từ phía máy chủ YouTube.</p>
<h2 id="phần-4-–-phần-cứng-và-mô-hình-dikw">PHẦN 4 – PHẦN CỨNG VÀ MÔ HÌNH DIKW</h2>
<h3 id="nâng-cấp-linh-kiện-giải-quyết-vấn-đề-giật-lag">1. Nâng cấp linh kiện giải quyết vấn đề giật lag</h3>
<p>Lựa chọn: Nâng cấp CPU (Chip xử lý).</p>
<p>Giải thích: Việc vừa chơi game eSports vừa quay/encode video livestream đòi hỏi năng lực tính toán cực kỳ lớn cùng lúc từ các nhân/luồng của CPU. RAM 16 GB hiện tại đã đủ dung lượng cho tác vụ này, nhưng nếu CPU bị quá tải (100% CPU utilization) thì hệ thống sẽ xuất hiện hiện tượng giật/khung hình bị khựng (drop frame) ngay lập tức.</p>
<h3 id="bảng-áp-dụng-mô-hình-dikw">2. Bảng áp dụng mô hình DIKW</h3>
<p>Tầng</p>
<p>Nội dung trong tình huống</p>
<p>Vì sao thuộc tầng này?</p>
<p>Data</p>
<p>Video ghi lại toàn bộ diễn biến trận đấu (hoặc các mốc thời gian/chỉ số trong video).</p>
<p>Là dữ liệu thô dạng hình ảnh/âm thanh chưa qua phân tích hay rút ra ý nghĩa.</p>
<p>Information</p>
<p>Tuyển thủ hay chết ở phút 15 – 20.</p>
<p>Dữ liệu thô đã được theo dõi và xử lý thành thông tin có ngữ cảnh thời gian và sự kiện cụ thể.</p>
<p>Knowledge</p>
<p>Phát hiện nguyên nhân chết do thiếu tầm nhìn bản đồ.</p>
<p>Đã kết nối thông tin (thời điểm chết) với hiểu biết chuyên môn eSports để giải thích được bản chất nguyên nhân.</p>
<p>Wisdom</p>
<p>Huấn luyện viên yêu cầu mua thêm mắt (Ward) cho trận sau.</p>
<p>Đưa ra quyết định/hành động chiến thuật đúng đắn từ tri thức đã đúc kết nhằm cải thiện kết quả.</p>

