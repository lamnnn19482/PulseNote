# PulseNote ✦ AI Summary – Privacy Policy

_Last updated: 13 November 2025_

PulseNote là tiện ích Chrome giúp bạn lấy phụ đề chính thức từ YouTube và gửi chúng đến dịch vụ tóm tắt AI mà bạn tự cấu hình. Chính sách này giải thích loại dữ liệu nào được xử lý và cách chúng tôi sử dụng dữ liệu đó.

## 1. Dữ liệu chúng tôi xử lý

| Loại dữ liệu | Nguồn | Mục đích | Lưu trữ |
| ------------ | ----- | -------- | ------- |
| **Website content** – văn bản phụ đề do YouTube cung cấp | Trình duyệt của bạn khi mở video có phụ đề | Hiển thị transcript, cho phép tải `.txt`, và (khi bạn yêu cầu) gửi tới API tóm tắt | Chỉ tồn tại trong bộ nhớ tạm của tiện ích; không gửi đi nếu bạn không bấm **Start Summary** |
| **Tùy chỉnh người dùng** – ngôn ngữ đầu ra, trạng thái còn lượt miễn phí, license Gumroad | Do bạn nhập trong popup | Nhớ cấu hình giữa các phiên và xác thực giới hạn sử dụng | Lưu trong `chrome.storage.sync/local` trên thiết bị của bạn |
| **Yêu cầu tóm tắt** – transcript, ngôn ngữ, token license | Gửi tới endpoint mà bạn cấu hình (`SUMMARY_API_BASE_URL`) | Nhận bản tóm tắt AI | Truyền qua HTTPS trực tiếp đến máy chủ của bạn; PulseNote không giữ bản sao |

PulseNote **không** thu thập hoặc gửi thông tin nhận dạng cá nhân (PII), thông tin tài chính, thông tin sức khỏe, hay lịch sử duyệt web ngoài trang YouTube hiện tại.

## 2. Bên xử lý dữ liệu

- **YouTube (Google LLC)** – cung cấp phụ đề thông qua API chính thức.
- **Máy chủ tóm tắt của bạn** – bạn chịu trách nhiệm về hạ tầng backend, bao gồm các dịch vụ như Gumroad nếu sử dụng để kích hoạt license.

Chúng tôi không bán, cho thuê, hoặc chia sẻ dữ liệu người dùng cho bên thứ ba ngoài các dịch vụ cần thiết nói ở trên.

## 3. Quyền và kiểm soát của bạn

- Bạn có thể xóa mọi dữ liệu cục bộ bằng cách gỡ PulseNote hoặc xóa dữ liệu extension trong `chrome://settings/siteData`.
- Không bấm **Start Summary** nếu bạn không muốn transcript được gửi tới máy chủ tóm tắt.
- Thay đổi `SUMMARY_API_BASE_URL` để trỏ tới máy chủ mà bạn tin tưởng.

## 4. Liên hệ

Câu hỏi về quyền riêng tư xin gửi tới `privacy@pulsenote.ai` hoặc mở issue tại [GitHub PulseNote](https://github.com/lamnnn19482/PulseNote/issues).
