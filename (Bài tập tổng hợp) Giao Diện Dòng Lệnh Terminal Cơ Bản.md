## Phần 1 — CLI vs GUI và cấu trúc câu lệnh

1 Phân tích lệnh ls -Force C:\\Windows\\Logs:



Command: ls (hoặc Get-ChildItem)



Options/Flags: -Force



Argument: C:\\Windows\\Logs

2 Lý do dùng Terminal (PowerShell/SSH) cho máy chủ Cloud:



Tối ưu tài nguyên phần cứng: Máy chủ Cloud (headless server) không cài giao diện đồ họa GUI để dành 100% RAM, CPU và băng thông phục vụ trực tiếp cho các dịch vụ/ứng dụng chạy ngầm backend.

## Phần 2 — Điều hướng hệ thống file

Relative Path di chuyển vào quan-ly-sinh-vien từ Desktop:

Plaintext

cd .\\quan-ly-sinh-vien\\

Absolute Path chuẩn Windows tới file main.py:

Plaintext

D:\\02\_Projects\\quan-ly-sinh-vien\\src\\main.py

Lệnh PowerShell xem nội dung (kể cả file ẩn) của thư mục data\\ đứng từ src\\:

Plaintext

ls -Force ..\\data\\

## Phần 3 — Thao tác file và thư mục

Tạo đồng thời 2 thư mục con src và data (tự tạo thư mục cha):

mkdir quan-ly-sinh-vien\\src, quan-ly-sinh-vien\\data

Tạo 3 file rỗng trong một dòng lệnh:

ni main.py, utils.py, README.md

Đổi tên và sao lưu thư mục dự án:

Rename-Item quan-ly-sv quan-ly-sinh-vien

Sao lưu đệ quy (-Recurse):

Copy-Item -Recurse quan-ly-sinh-vien backup-quan-ly-sinh-vien

## Phần 4 — Xử lý lỗi Terminal

Log lỗi số 2 (Path Not Found):

Chẩn đoán: Sai chính tả hoặc đường dẫn không tồn tại.

Kiểm tra: Nhấn phím Tab để autocomplete; nếu không nhảy tên file/thư mục nghĩa là đường dẫn bị sai.

Log lỗi số 3 (Execution Policy):

Chẩn đoán: Windows chặn thực thi script cục bộ do chính sách bảo mật.

Khắc phục: Chạy lệnh Set-ExecutionPolicy RemoteSigned -Scope Process.Log lỗi số 1 (Cảnh báo xóa thư mục):Chẩn đoán: PowerShell yêu cầu xác nhận trước khi xóa thư mục chứa dữ liệu để tránh xóa nhầm.Đơn thuốc (xóa sạch không hỏi):PlaintextRemove-Item -Recurse -Force old-version

Log lỗi số 4 (Quy trình 3 bước):

Chính xác tuyệt đối! Các bước phân tích log lỗi của bạn hoàn toàn chuẩn xác theo tư duy debugging chuyên nghiệp của lập trình viên:



Bước (a): Luôn tập trung ngay vào \*\*dòng cuối cùng\*\* của traceback (nơi Python/Terminal bắn ra ngoại lệ cốt lõi) thay vì đọc từ trên xuống.

Bước (b): Nhận diện nhanh \*\*Error Keyword\*\* (như `FileNotFoundError`, `ModuleNotFoundError`, v.v.) để phân loại ngay loại sự cố phần cứng/phần mềm.

Bước (c): Kiểm tra \*\*ngữ cảnh hiện tại\*\* (`pwd`) đối chiếu với đường dẫn (đặc biệt là Relative Path) để tìm điểm gãy kết nối.





