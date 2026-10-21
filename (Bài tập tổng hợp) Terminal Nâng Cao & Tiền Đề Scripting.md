Dưới đây là đáp án ngắn gọn và chuẩn xác theo yêu cầu:

---

### Phần 1 – Đọc và định vị tệp tin

1. `Get-Content logs\server.log`
2. **Notepad** tải toàn bộ file 500 MB vào RAM cùng lúc gây tràn bộ nhớ; **PowerShell** đọc và xử lý theo từng dòng (streaming) nên tiết kiệm RAM.
3. `Get-ChildItem -Path . -Filter *.log -Recurse`

---

### Phần 2 – Lọc dữ liệu và Pipe

1. `Get-Content logs\server.log | Select-String "ERROR"`
2. Câu hỏi: "File server.log đang nằm ở thư mục nào?"

Lệnh: Get-ChildItem -Recurse -Filter server.log

Câu hỏi: "Bên trong file này có dòng nào chứa lỗi 404 không?"

Lệnh: Get-Content logs\server.log | Select-String "404"
lệnh pipe : `Get-Content logs\server.log | Select-String "404"`
3. `Get-ChildItem -Path . -Filter *.log -Recurse | Get-Content | Select-String "INFO" -NotMatch`

---

### Phần 3 – Toán tử chuyển hướng > và >>

1. `Get-Content logs\server.log | Select-String "404" > reports\daily_report.txt`
2.  Thêm dòng mới: `Get-Content logs\server.log | Select-String "404" >> reports\daily_report.txt`
* Giải thích: Nếu dùng nhầm `>`, toàn bộ báo cáo cũ sẽ bị ghi đè (xóa sạch).



---

### Phần 4 – Shell Script và lệnh echo

1.  `Write-Output "Dang loc log..."`
    `Write-Output "=== LOG REPORT ===" > reports\daily_report.txt`


2. Nội dung `scripts\auto_report.ps1`:
```powershell
# Tu dong trich xuat log 404
Write-Output "Bat dau chay..."
Get-Content logs\server.log | Select-String "404" > reports\daily_report.txt

```



---

### Phần 5 – Viết, chạy và thẩm định Script AI

1.  (a) `.\scripts\auto_report.ps1`
    (b) `Get-Content reports\daily_report.txt`


2. * (a) Dòng nguy hiểm: `Remove-Item -Recurse -Force C:\*` -> Xóa sạch ổ C:\ và làm sập hệ thống.
* (b) Sửa lại: `Remove-Item -Recurse -Force devops-lab\temp\*`
