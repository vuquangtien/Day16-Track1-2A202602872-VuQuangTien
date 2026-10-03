# AI Product Teardown — Notion AI

**Học viên:** Vũ Quang Tiến  
**MSV:** 2A202602872  
**Sản phẩm:** Notion AI  
**Phạm vi nghiên cứu ban đầu:** 11/2022–09/2025

## Step 0 — Chọn sản phẩm & khai phá nguồn

### Sản phẩm đã chốt: Notion AI

Notion AI đạt cả ba tiêu chí của lab:

1. **AI là phần trọng yếu của trải nghiệm:** Notion đưa AI vào trực tiếp nơi người dùng viết, quản lý dự án và lưu tri thức; sau đó mở rộng thành hỏi-đáp theo workspace, tìm kiếm qua các công cụ kết nối và Agent.
2. **Đủ dữ liệu công khai:** Có release archive chính thức theo ngày, bài launch/retrospective của CEO, và trang Product Hunt cho alpha.
3. **Use case/JTBD rõ:** Cá nhân và đội ngũ tri thức dùng Notion để viết, quản lý dự án và truy xuất tri thức nội bộ. AI giảm “work about work” như soạn thảo, tóm tắt, tìm thông tin và cập nhật dữ liệu.

### Ba nguồn checkpoint đã mở và kiểm chứng

| Loại nguồn | Link | Giá trị cho bài |
|---|---|---|
| Changelog/release archive chính thức | [Notion — What’s New](https://www.notion.com/releases) | Có danh sách release theo thời gian; là nguồn gốc cho các mốc tính năng và pricing/segment ở bước timeline. |
| Product Hunt archive | [Notion AI is in Alpha — Product Hunt](https://www.producthunt.com/stories/notion-ai-is-in-alpha) | Xác nhận alpha ngày 16/11/2022, đồng thời lưu cách sản phẩm được giới thiệu ra thị trường. |
| Bài founder | [Behind the scenes of Notion AI — Ivan Zhao](https://www.notion.com/blog/behind-the-scenes-notion-ai) | CEO mô tả lý do chọn GPT-4, quyết định UX, alpha, waitlist và vòng lặp lấy phản hồi. |

Nguồn bổ sung quan trọng: [launch GA do Ivan Zhao viết](https://www.notion.com/blog/notion-ai-is-here-for-everyone) và [bài học GTM của Notion](https://www.notion.com/blog/lessons-we-learned-from-launching-notion-ai).

### Kho mốc ứng viên thô

> Đây là backlog để sàng lọc ở Step 1, **chưa phải** 6–8 cột mốc cuối cùng. Các mục đánh dấu ★ có khả năng cao trở thành milestone vì thể hiện đổi trải nghiệm, đối tượng phục vụ hoặc mô hình giá trị.

| Thời điểm | Mốc ứng viên / tín hiệu cần đào sâu | Nguồn gốc ban đầu |
|---|---|---|
| 11/2022 | ★ Notion AI private alpha; AI writer, brainstorming, edit, summary; mở waitlist | [Founder launch](https://www.notion.com/blog/introducing-notion-ai) |
| 11/2022–02/2023 | 10 tuần thử nghiệm alpha; waitlist tăng mạnh; thu thập feedback | [Founder retrospective](https://www.notion.com/blog/behind-the-scenes-notion-ai) |
| 02/2023 | ★ General availability cho mọi người; AI nằm trong workspace thay vì một tab/chat riêng | [GA launch](https://www.notion.com/blog/notion-ai-is-here-for-everyone) |
| 02/2023 | Đổi pricing từ credits/query sang phí cố định theo tháng trước GA | [GTM lessons](https://www.notion.com/blog/lessons-we-learned-from-launching-notion-ai) |
| 02/2023 | Phát hiện hành vi chủ đạo: chỉnh đoạn văn có sẵn; “Improve writing” là tính năng quay lại nhiều nhất | [GA launch](https://www.notion.com/blog/notion-ai-is-here-for-everyone) |
| 04/2023 | Nghiên cứu cách hàng triệu người sử dụng Notion AI sau launch | [User-research post](https://www.notion.com/blog/millions-have-used-notion-ai-heres-what-weve-learned) |
| 05/2023 | ★ AI Autofill trong database: summary, action items, project update | [Release 2.30](https://www.notion.com/releases/2023-05-31) |
| 09/2023 | AI dịch database properties; nằm trong workflow automation | [Release 2.33](https://www.notion.com/releases/2023-09-22) |
| 11/2023 | ★ Q&A: hỏi đáp trên thông tin toàn workspace | [Q&A launch](https://www.notion.com/blog/introducing-q-and-a) |
| 04/2024 | Q&A beta đã có tín hiệu được người dùng yêu thích; cần đối chiếu cách định vị | [Release 2.39](https://www.notion.com/releases/2024-04-30) |
| 06/2024 | ★ AI tìm kiếm Slack, Google Drive, Salesforce, Jira; có GPT-4 và citation | [Release 2.41](https://www.notion.com/releases/2024-06-18) |
| 07/2024 | One-click AI skills, AI chat/search, global shortcut ngoài Notion | [Release 2.43](https://www.notion.com/releases/2024-07-29) |
| 09/2024 | ★ “New Notion AI”: connectors Google, hỏi đáp đa nguồn, phân tích PDF/ảnh, GPT-4 & Claude | [Release 2.45](https://www.notion.com/releases/2024-09-25) |
| 12/2024 | Mở rộng automation và câu trả lời từ GitHub | [Release archive](https://www.notion.com/releases) |
| 02/2025 | AI xây database/setup từ mô tả tự nhiên | [Release 2.48](https://www.notion.com/releases/2025-02-18) |
| 03/2025 | Page verification và forms có conditional logic — ứng viên context về enterprise workflow | [Release archive](https://www.notion.com/releases) |
| 05/2025 | ★ AI Meeting Notes, Enterprise Search, Research Mode và pricing AI gộp trong Business/Enterprise | [Release 2.51](https://www.notion.com/releases/2025-05-13) |
| 07/2025 | Research Mode hỏi đáp database phức tạp; tìm kiếm Gmail và Linear | [Release 2.52](https://www.notion.com/releases/2025-07-10) |
| 09/2025 | ★ Notion 3.0: Agent thực hiện chuỗi tác vụ nhiều bước trên pages/databases; memory và connectors | [Notion 3.0](https://www.notion.com/releases/2025-09-18) |

### Giả thuyết tuyến phát triển để kiểm tra ở Step 1

Notion AI có vẻ chuyển dần theo chuỗi **AI viết/chỉnh sửa trong tài liệu → AI khai thác tri thức nội bộ → AI có context liên công cụ → Agent hành động trên hệ thống công việc**. Đây mới là giả thuyết đọc từ nguồn thô, không phải kết luận; Step 1 cần chọn 6–8 mốc có tính quyết định nhất để kiểm chứng nó.

