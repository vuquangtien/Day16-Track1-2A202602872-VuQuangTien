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

## Step 2 — Tệp user & JTBD

### Lưu ý về bằng chứng

Hai chân dung dưới đây là **archetype phân tích**, không phải khẳng định mọi user đều như vậy. Chúng được suy ra từ: (a) cách Notion tuyển early adopters qua alpha/waitlist và điều họ thực sự dùng ([bài học launch](https://www.notion.com/blog/lessons-we-learned-from-launching-notion-ai)); (b) phản hồi sớm trên [Hacker News](https://news.ycombinator.com/item?id=33623201), nơi người dùng vừa dùng Notion hằng ngày vừa đề xuất semantic search/Q&A; và (c) phản hồi quy mô lớn hiện nay trên [G2](https://ai.g2.com/product/notion), trong đó điểm mạnh là gom workstream/customization/AI, còn điểm yếu là navigation và độ phức tạp. Các chi tiết về hành vi là suy luận có đánh dấu, không phải lời trích dẫn của một cá nhân cụ thể.

### Early adopters và tệp hiện tại

| | Early adopters (11/2022–2023) | Tệp hiện tại (2024–2025) |
|---|---|---|
| **Gọi tên một người thật** | *Linh*, product marketer hoặc PM tại startup SaaS 10–50 người; đã dùng Notion hằng ngày để viết brief/meeting note, theo dõi Product Hunt/AI Twitter và đủ tò mò để vào waitlist thử alpha dù sản phẩm chưa hoàn thiện. | *Minh*, Head of Operations/Knowledge tại công ty công nghệ 100–500 người; phải giúp sales, product và engineering tìm đúng chính sách/trạng thái dự án đang nằm rải ở Notion, Slack, Google Drive và Jira. Có quyền đề xuất/cấu hình workspace, nhưng không muốn ép mọi người đổi công cụ. |
| **Dấu hiệu nhận diện** | Đã có dữ liệu/notes trong Notion, chấp nhận thử nghiệm, tự viết nhiều và cần sửa/tóm tắt nhanh. Đây khớp với alpha private/waitlist và phát hiện rằng lệnh được dùng nhiều nhất là chỉnh phần văn bản user đã viết. [GA launch](https://www.notion.com/blog/notion-ai-is-here-for-everyone) | Đang chịu chi phí “work about work”: tìm thông tin, hỏi đồng nghiệp, tổng hợp update và ghi họp. Họ cần sự tin cậy, permission và citation hơn một chatbot viết hay. Notion hiện định vị Enterprise Search là tìm câu trả lời có citation dựa trên các work tools và quyền truy cập. [Enterprise Search](https://www.notion.com/product/enterprise-search) |
| **JTBD chính** | “Khi tôi đang biến ý thô/ghi chú họp thành brief, email hoặc proposal, hãy giúp tôi có bản nháp và chỉnh câu ngay trong trang tôi đang làm, để tôi hoàn thành bản có thể gửi nhanh hơn mà không mất ngữ cảnh.” | “Khi một đồng nghiệp hỏi trạng thái dự án/chính sách/khách hàng, hãy tìm và tổng hợp câu trả lời có nguồn từ các hệ thống tôi được phép xem, để tôi ra quyết định hoặc trả lời trong vài phút thay vì lục app hay hỏi nhiều người.” |
| **Cách cũ** | Tự viết rồi sửa; copy–paste giữa Notion và Google/Grammarly/ChatGPT; đọc lại notes dài để rút action items. | Search keyword từng app, lục folder/page, nhắn người biết việc, dự họp để lấy context, rồi ghép câu trả lời thủ công. Một phản hồi HN sớm đã nêu nhu cầu semantic search/Q&A thay vì chỉ “predict next sentence”. [HN discussion](https://news.ycombinator.com/item?id=33623201) |
| **Giá trị quyết định mua/dùng** | Nhanh bắt đầu và ít friction: AI xuất hiện ngay nơi đang viết, không cần học công cụ/chat mới; pricing cố định làm việc thử ít áp lực hơn. | Giảm thời gian truy xuất tri thức và handoff giữa các team; kết quả phải biết nguồn, tôn trọng permission và chạy qua Slack/Drive/Jira chứ không chỉ dữ liệu đã nằm trong Notion. |
| **Mốc Step 1 gây/đẩy dịch chuyển** | 16/11/2022 alpha và 22/02/2023 GA/repricing: AI writer được nhúng vào workspace, sau đó tối ưu theo hành vi “Improve writing”. | 14/11/2023 Q&A mở rộng job sang knowledge retrieval; 18/06/2024 connectors/citations và 13/05/2025 Enterprise Search/Research Mode biến Notion từ editor thành lớp truy xuất tri thức liên công cụ. |

**Kết luận về segment-shift:** Notion không thay người dùng cũ bằng người dùng mới hoàn toàn. Họ mở rộng từ cá nhân/nhóm nhỏ đã có thói quen viết trong Notion sang người sở hữu vấn đề tri thức cấp team/doanh nghiệp. Khác biệt quyết định là JTBD: **tạo/chỉnh một artifact** chuyển thành **tìm và vận dụng tri thức đáng tin xuyên hệ thống**.

### Switching cost theo 4 forces

| Force | Biểu hiện với Notion AI | Hệ quả cho hành vi chuyển đổi |
|---|---|---|
| **Push — vấn đề của cách hiện tại** | Tool stack phân mảnh khiến người dùng mất thời gian tìm page, Slack thread, Drive file và hỏi đồng nghiệp; review G2 cũng nêu pain point navigation/tìm đúng page trong workspace lớn. [G2 review summary](https://ai.g2.com/product/notion) | Push tạo động lực thử Notion AI/Enterprise Search; nó mạnh hơn với tệp hiện tại có nhiều hệ thống và handoff. |
| **Pull — sức hút của lựa chọn mới** | Một bề mặt hỏi-đáp có citation, search connector, research, meeting notes và về sau Agent có thể hành động trên pages/databases. [Release 2.51](https://www.notion.com/releases/2025-05-13) · [Notion 3.0](https://www.notion.com/releases/2025-09-18) | User không chỉ mua “một model”; họ bị kéo bởi lời hứa giảm context-switch và có câu trả lời dùng được ngay trong workflow. |
| **Anxiety — nỗi lo khi chuyển/đổi cách làm** | AI có thể trả lời thiếu/sai nếu knowledge base lộn xộn; người dùng lo privacy, phân quyền, chi phí và việc AI làm sai dữ liệu. Phản hồi Q&A sớm đã nêu kết quả đếm page không đầy đủ. [Reddit review](https://www.reddit.com/r/Notion/comments/18wz58z) | Citation, permission-aware search và beta rollout giảm anxiety, nhưng adoption enterprise vẫn phụ thuộc chất lượng dữ liệu và governance, không tự xảy ra chỉ nhờ model tốt. |
| **Habit & inertia — thói quen/chi phí ở lại** | Pages, databases, template, taxonomy, history, permission, liên kết giữa task–doc và thói quen cộng tác của cả team đã nằm trong Notion. Khi connector và Agent dùng chính context đó, giá trị tăng theo lượng workflow đã tích lũy. | Đây là lực **giữ ở lại** mạnh nhất: rời Notion không chỉ là export file, mà là dạy lại team, tái tạo cấu trúc, quyền và automation ở nơi khác. |

### Trả lời phản biện CP2

**Lực giữ user mạnh nhất là Habit & inertia, cụ thể là dữ liệu + workflow cộng tác tích lũy trong workspace.** Model có thể bị thay thế và AI writer là wrapper tương đối mỏng; nhưng một workspace có pages, database, permissions, template, integrations và quy ước làm việc của cả team thì khó “mang đi” nguyên trạng. Nếu lực này biến mất — ví dụ dữ liệu/permission/automation có chuẩn mở và một đối thủ index được mọi nguồn với chất lượng tương đương, không cần team đổi thói quen — Notion AI dễ bị multi-home: user dùng ChatGPT, Slack AI hoặc công cụ search khác, và Notion bị kéo về vai trò nơi lưu tài liệu thay vì lớp AI chủ đạo.

## Step 3 — Ba dự đoán hướng đi

> **Mốc quan sát để dự đoán: 18/09/2025.** Các dự đoán dưới đây chỉ dùng những bằng chứng ở Step 1–2, không dùng release sau ngày này.

**Dự đoán 1 — Mở rộng tính năng: Agent chuyển từ “trợ lý cá nhân” sang custom agent theo phòng ban, có trigger/schedule và template workflow.**  
**Lập luận:** Notion 3.0 đã cho Agent đọc–ghi pages/databases, dùng instructions/memory và công bố Custom Agents chạy theo trigger hoặc lịch; nền connectors + permission đã được dựng từ Q&A/Enterprise Search. Đây là bước hợp logic để biến knowledge đã tích lũy thành hành động lặp lại cho RevOps, HR, CS hay Engineering, thay vì chỉ trả lời một lần. [Notion 3.0](https://www.notion.com/releases/2025-09-18)

**Dự đoán 2 — Mở rộng segment: Notion sẽ bán mạnh hơn cho team vận hành tri thức liên phòng ban (đặc biệt RevOps/CS/People Ops), không chỉ team vốn đã “sống trong Notion”.**  
**Lập luận:** Tệp hiện tại ở Step 2 cần trả lời nhanh câu hỏi phân tán giữa Notion, Slack, Drive, CRM và ticketing; mốc 2024–2025 đã thêm Salesforce, Zendesk, Microsoft, Gmail, Linear, meeting notes và Research Mode. Nhóm này có pain “work about work” rõ, nhiều người hỏi lặp lại và có buyer doanh nghiệp — phù hợp hơn với Enterprise Search/Agent so với một AI writer phổ thông. [Release 2.41](https://www.notion.com/releases/2024-06-18) · [Release 2.51](https://www.notion.com/releases/2025-05-13)

**Dự đoán 3 — Thay đổi mô hình kiếm tiền: Notion sẽ tách giá trị agent/high-cost model khỏi AI cơ bản bằng hạn mức usage hoặc add-on theo cấp doanh nghiệp.**  
**Lập luận:** Notion đã đi từ credits/query sang flat fee để khuyến khích khám phá AI writer, rồi gộp AI vào Business/Enterprise khi tính năng trở thành team workflow. Nhưng Agent chạy nhiều bước, Research Mode và model frontier có cost biến đổi cao; pricing đồng hạng cho mọi mức sử dụng sẽ không bền, nên tier/allowance theo tác vụ agent hoặc model cao cấp là bước tiếp theo hợp lý. [Bài học pricing](https://www.notion.com/blog/lessons-we-learned-from-launching-notion-ai) · [Release 2.51](https://www.notion.com/releases/2025-05-13)

### Trả lời phản biện CP3

**Tự tin nhất: Dự đoán 1.** Nó không chỉ là suy đoán từ xu hướng: Notion 3.0 đã có Agent, instructions, memory và nói rõ Custom Agents theo trigger/schedule là hướng đang tới. Giả định làm nó gãy là doanh nghiệp không tin agent có quyền ghi/sửa dữ liệu, hoặc kết quả không đủ chính xác để vượt qua rủi ro governance; khi đó Notion có thể dừng ở search/assistant “read-only” thay vì agent tự hành động.
