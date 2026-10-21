---


---

<h2 id="phần-1-–-cli-vs-gui-và-cấu-trúc-câu-lệnh">Phần 1 – CLI vs GUI và Cấu trúc Câu lệnh</h2>
<h3 id="phân-tích-câu-lệnh-ls--force-cwindowslogs">1. Phân tích câu lệnh: <code>ls -Force C:\Windows\Logs</code></h3>
<ul>
<li>
<p><strong>Command:</strong>  <code>ls</code> (Alias của <code>Get-ChildItem</code> – lệnh xem danh sách file/thư mục).</p>
</li>
<li>
<p><strong>Options/Flags:</strong>  <code>-Force</code> (Cờ tùy chọn để hiện cả file/thư mục bị ẩn).</p>
</li>
<li>
<p><strong>Argument:</strong>  <code>C:\Windows\Logs</code> (Đường dẫn mục tiêu cần thao tác).</p>
</li>
</ul>
<h3 id="lý-do-bắt-buộc-dùng-terminal-với-máy-chủ-cloud">2. Lý do bắt buộc dùng Terminal với máy chủ Cloud</h3>
<ul>
<li><strong>Tối ưu tài nguyên &amp; Không có GUI (Headless):</strong> Máy chủ Cloud thường loại bỏ giao diện đồ họa (GUI) để tiết kiệm tối đa CPU/RAM và tăng tính bảo mật. Do đó, Terminal (PowerShell/SSH) là cách <strong>duy nhất</strong> để truy cập, quản trị và deploy project.</li>
</ul>

