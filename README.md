# Voice control cho camera điện thoại

## 1. Giới thiệu đề tài
* **Đề tài:** Voice control cho camera điện thoại.
* **Môn học:** Mạng cảm biến.
* **Mục tiêu:** Xây dựng hệ thống điều khiển camera bằng giọng nói dựa trên mô hình **Audio-KWS (Keyword Spotting)**.
* **Hỗ trợ các lệnh:** "mở camera", "chụp ảnh", "dừng", "noise" và từ khóa kích hoạt "trung lĩnh".

## 2. Thành viên thực hiện
* **Họ và tên:** Nguyễn Trần Trung Lĩnh
* **MSSV:** N23DCCI040
* **Lớp:** D23CQCI01-N

## 3. Cấu trúc thư mục
```text
├── edge-impulse-standalone.js    # Thư viện hỗ trợ suy luận
├── edge-impulse-standalone.wasm  # Lõi mô hình đã nén
├── index.html                    # Giao diện kiểm thử (UI)
├── run-impulse.js                # Logic xử lý và kết nối Microphone
├── server.py                     # Script hỗ trợ chạy local server
└── README.md                     # Tài liệu hướng dẫn
```
## 4. Phụ thuộc (Dependencies)
Để đảm bảo hệ thống vận hành đúng, môi trường chạy cần đáp ứng các yêu cầu sau:
- Phần cứng: * Thiết bị có tích hợp Microphone (Laptop, PC, hoặc Smartphone).
- Phần mềm & Môi trường:
  - Trình duyệt: Khuyến khích sử dụng Google Chrome, Microsoft Edge hoặc Brave (phiên bản mới nhất) để hỗ trợ tốt nhất cho WebAssembly (WASM) và Web Audio API.
  - Môi trường Local Server: Cần cài đặt Python 3.x để thực hiện lệnh chạy server cục bộ.
  - Mạng: Kết nối Internet ổn định (chỉ cần lúc tải lần đầu, sau đó mô hình chạy hoàn toàn Offline trên trình duyệt).
## 5. Hướng dẫn cài đặt và chạy
Dự án hỗ trợ hai phương thức kiểm thử:

- **Phương thức 1:** Trải nghiệm qua Web-based Deployment
  - Truy cập vào liên kết triển khai từ Edge Impulse: [Nhấn vào đây để mở Camera Voice Control]
  - Cấp quyền truy cập Microphone và bắt đầu trải nghiệm.

- **Phương thức 2:** Chạy Local
  - Clone repository:
    ``git clone https://github.com/raumaniac/mangcambien-cuoiky-nguyentrantrunglinh``
  - Chạy server (cần Python):
    ``cd browser
    python -m http.server 8000``
  - Mở trình duyệt tại: http://localhost:8000
