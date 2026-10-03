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

## Step 1 — Timeline & revert nguyên lý

### Tiêu chuẩn lọc

Tôi chỉ giữ một mốc nếu nó thay đổi ít nhất một trong ba thứ: **(1)** loại công việc AI làm cho user, **(2)** context/data AI có thể dùng, hoặc **(3)** đối tượng trả tiền và mô hình giá trị. Vì vậy bảng dưới là chuỗi quyết định, không phải danh sách release.

| Thời điểm | Cập nhật | Context lúc đó | Revert nguyên lý |
|---|---|---|---|
| 16/11/2022 | **Notion AI private alpha**: đưa AI writer (viết nháp, brainstorm, edit, tóm tắt) vào ngay trong Notion và mở waitlist. [Nguồn gốc](https://www.notion.com/blog/introducing-notion-ai) | Notion đã là nơi người dùng lưu docs, notes và project. Theo CEO Ivan Zhao, đội ngũ vừa có early access GPT-4 vào mùa thu 2022 và nhận ra năng lực model đã vượt mức “autocomplete”; vài ngày sau alpha, ChatGPT làm kỳ vọng của thị trường bùng nổ. [Retrospective founder](https://www.notion.com/blog/behind-the-scenes-notion-ai) | **Wrapper/moat — phân phối và workflow trước model.** Bản thân AI writer dễ bị model/chatbot hấp thụ, nên giá trị ban đầu là đặt nó ngay trong nơi công việc đang diễn ra, giảm copy–paste và switching cost. |
| 22/02/2023 | **General availability + đổi cách định vị/giá.** Sau 10 tuần alpha, Notion mở AI cho toàn bộ user; đồng thời từ pricing credits/query chuyển sang phí cố định theo tháng. Họ cũng thiết kế lại UI sau khi thấy user chủ yếu highlight văn bản có sẵn để “Improve writing”, thay vì tạo trang trắng để viết. [GA launch](https://www.notion.com/blog/notion-ai-is-here-for-everyone) · [Bài học launch](https://www.notion.com/blog/lessons-we-learned-from-launching-notion-ai) | Waitlist tăng từ kỳ vọng 200 nghìn lên 1 triệu trong 5 tuần; pricing theo lượt khiến người mới ngại thử. Dữ liệu alpha cho thấy giả định “AI viết bài mới” không phải hành vi lặp lại mạnh nhất. | **Vòng lặp học + định nghĩa “tốt” bằng hành vi thực.** Không bảo vệ giả định feature ban đầu; dùng feedback để đổi UX, thông điệp và pricing sao cho user dám khám phá, rồi quay lại dùng tính năng hữu ích. |
| 31/05/2023 | **AI Autofill cho database/project management**: tự sinh summary, action items, project updates trong thuộc tính database. [Release 2.30](https://www.notion.com/releases/2023-05-31) | Sau GA, Notion không chỉ cạnh tranh ở trang tài liệu: họ bổ sung template, GitHub integration, import từ Asana và workflow cho đội dự án. Structured data trong database cho AI context rõ hơn văn bản tự do. | **Moat từ workflow và dữ liệu có cấu trúc.** AI chuyển từ trợ lý viết cho một block thành thành phần của hệ thống vận hành công việc; database schema và thói quen cập nhật workflow khó thay thế hơn một prompt. |
| 14/11/2023 | **Notion AI Q&A**: hỏi đáp trên tri thức nằm trong toàn workspace, không chỉ tạo/chỉnh nội dung tại trang đang mở. [Q&A launch](https://www.notion.com/blog/introducing-q-and-a) | Notion ghi nhận pain point lớn nhất trong SaaS là tìm đúng thông tin khi cần; đây là kết luận sau các cuộc phỏng vấn khách hàng AI, khiến họ chuyển trọng tâm từ editorial AI sang “team-based database knowledge”. [Bài học launch](https://www.notion.com/blog/lessons-we-learned-from-launching-notion-ai) | **Định nghĩa “tốt” theo JTBD, không theo capability.** User không thuê AI để “chat”; họ thuê nó để lấy được câu trả lời đáng tin trong kho tri thức của công ty. Q&A chuyển sản phẩm từ content generation sang knowledge retrieval. |
| 18/06/2024 | **AI search mở ra ngoài Notion**: truy xuất Slack, Google Drive, Salesforce, Jira; bổ sung GPT-4, citation và phạm vi tìm kiếm có thể chỉ định. [Release 2.41](https://www.notion.com/releases/2024-06-18) | Tri thức công ty bị phân mảnh trong nhiều SaaS; Notion phải thắng không chỉ bằng page/database của mình mà bằng khả năng trả lời nơi data thực sự nằm. Citation là điều kiện để user tin kết quả trong ngữ cảnh công việc. | **Moat từ context và integration, không phải model.** Frontier model có thể phổ cập, nhưng lớp quyền truy cập, kết nối nguồn và câu trả lời có thể kiểm chứng trong workflow doanh nghiệp tạo lợi thế khó sao chép hơn. |
| 25/09/2024 | **Tái định vị “New Notion AI”**: connectors Google Docs/Sheets/Slides, chat với GPT-4/Claude, tạo/chỉnh theo style guide trong workspace và phân tích PDF/ảnh. [Release 2.45](https://www.notion.com/releases/2024-09-25) | LLM đa phương thức và nhiều model frontier đã phổ biến; chat độc lập trở thành commodity. Notion gom search, generate, analyze và chat vào chính workspace, thay vì cạnh tranh bằng một model riêng. | **Wrapper mỏng vs moat.** Notion không cố xây “model tốt nhất”; họ dùng nhiều model như commodity và tăng giá trị bằng context riêng, style guide, permission và luồng cộng tác đã tồn tại. |
| 13/05/2025 | **AI Meeting Notes + Enterprise Search + Research Mode; đưa AI vào Business/Enterprise plan.** AI ghi/tóm tắt họp, search thêm nguồn, research từ workspace + connected tools + web, và pricing chuyển sang AI bao gồm trong plan doanh nghiệp. [Release 2.51](https://www.notion.com/releases/2025-05-13) | Use case dịch từ năng suất cá nhân sang nhu cầu tổ chức: ghi nhận tri thức họp, tìm xuyên hệ thống, tạo báo cáo. Đây là lúc việc mua AI cần đi kèm quyền, bảo mật, connector và mô hình giá phù hợp buyer doanh nghiệp. | **Segment/premium moat: AI Expert + Domain Expert.** Giá trị không còn là “một prompt hay”; nó là workflow knowledge work có bối cảnh doanh nghiệp, phân quyền và nguồn dữ liệu. Gói AI vào Business/Enterprise biến AI thành năng lực của tổ chức thay vì add-on cá nhân. |
| 18/09/2025 | **Notion 3.0: Agents**: Agent làm được chuỗi tác vụ nhiều bước trên pages/databases, có memory, instructions, connectors và khả năng tạo/cập nhật hàng loạt. [Notion 3.0 release](https://www.notion.com/releases/2025-09-18) | Sau khi đã có database, integrations và enterprise search, Notion có đủ context lẫn bề mặt hành động. Thị trường chuyển từ AI trả lời sang agent có thể hoàn thành công việc; Notion giới hạn mốc này cho Business/Enterprise. | **Vòng lặp học có action + moat workflow.** Agent vừa đọc context vừa ghi ngược vào nơi công việc được vận hành; mỗi workflow, instruction, memory và lịch sử sử dụng làm chi phí chuyển đổi tăng lên. Đây là bước từ “trợ lý trả lời” sang “đồng đội thực hiện”. |

### Vì sao chọn 8 mốc này

Tám mốc tạo thành bốn lần chuyển lớp rõ ràng: **AI writer → AI chỉnh sửa theo feedback → AI trên structured workflow → AI truy xuất tri thức → AI liên thông nhiều hệ thống → AI đa model/multimodal → AI enterprise workflow → AI agent có hành động.** Mỗi mốc đều đổi JTBD, context/data, hoặc buyer/pricing; các mốc có link nguồn gốc chính thức.

### Mốc đã cân nhắc nhưng loại

| Mốc loại | Lý do không đủ tư cách là quyết định lớn |
|---|---|
| 22/09/2023 — AI dịch database property | Là mở rộng use case hẹp của AI Autofill/database, không thay đổi lớp context hay đối tượng phục vụ. [Release 2.33](https://www.notion.com/releases/2023-09-22) |
| 29/07/2024 — one-click skills, global shortcut, UI chat | Cải thiện adoption/khả năng truy cập; quyết định chiến lược search + đa nguồn đã được phản ánh tốt hơn ở mốc 18/06 và 25/09. [Release 2.43](https://www.notion.com/releases/2024-07-29) |
| 18/02/2025 — “Build with AI” tạo database từ mô tả | Hữu ích nhưng chủ yếu là interface mới cho thế mạnh database; không đổi thesis như Meeting Notes/Enterprise Search/Research Mode. [Release 2.48](https://www.notion.com/releases/2025-02-18) |
| 10/07/2025 — Research Mode hỏi đáp database, Gmail/Linear search | Là mở rộng connector và dữ liệu của mốc 13/05; giữ nó sẽ khiến timeline tách một quyết định platform thành nhiều bản vá release. [Release 2.52](https://www.notion.com/releases/2025-07-10) |
