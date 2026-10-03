# Memo Teardown — Notion AI

**Họ tên:** Vũ Quang Tiến  
**MSV:** 2A202602872  
**Sản phẩm:** Notion AI

**Vì sao chọn sản phẩm này:** Notion AI đủ lịch sử công khai để đọc thành chuỗi quyết định: từ AI writer, sang khai thác tri thức nội bộ, kết nối các work tool rồi thành Agent. Use case rõ: giảm thời gian viết, tìm thông tin và điều phối công việc tri thức.

## §1. Timeline các cập nhật lớn

| Thời điểm | Cập nhật | Context lúc đó | Nguyên lý |
|---|---|---|---|
| 16/11/2022 | [Private alpha](https://www.notion.com/blog/introducing-notion-ai): AI writer để viết nháp, brainstorm, edit, tóm tắt trong Notion. | Notion đã là nơi user lưu docs, notes, project; founder cho biết đội nhận early access GPT-4 vào mùa thu 2022. [Nguồn](https://www.notion.com/blog/behind-the-scenes-notion-ai) | **Wrapper/moat:** AI writer dễ thành commodity; lợi thế ban đầu là phân phối trong workflow/data user đã có. |
| 22/02/2023 | [GA cho mọi user](https://www.notion.com/blog/notion-ai-is-here-for-everyone), đổi pricing credits/query sang phí cố định và thiết kế lại UX cho hành vi “Improve writing”. | Alpha 10 tuần cho feedback nhanh; waitlist tăng từ kỳ vọng 200 nghìn lên 1 triệu trong 5 tuần. Giá theo lượt làm user ngại thử. [Nguồn](https://www.notion.com/blog/lessons-we-learned-from-launching-notion-ai) | **Vòng lặp học + định nghĩa “tốt”:** đổi UX, thông điệp và giá theo hành vi thực tế, không giữ giả định “viết từ trang trắng”. |
| 31/05/2023 | [AI Autofill](https://www.notion.com/releases/2023-05-31) cho database/project management: summary, action items, project update. | Notion bổ sung templates, project workflow, GitHub integration, import Asana; database cung cấp context có cấu trúc. | **Moat từ workflow/data có cấu trúc:** AI vận hành trong schema và hệ thống công việc của team. |
| 14/11/2023 | [Q&A](https://www.notion.com/blog/introducing-q-and-a): hỏi đáp trên knowledge, docs, projects, meeting notes của workspace. | Phỏng vấn khách hàng cho thấy pain lớn là tìm thông tin khi cần; hướng sản phẩm chuyển từ editorial AI sang team knowledge. [Nguồn](https://www.notion.com/blog/lessons-we-learned-from-launching-notion-ai) | **Định nghĩa “tốt” theo JTBD:** user thuê công cụ để lấy câu trả lời đáng tin từ tri thức công ty, không phải “chat”. |
| 18/06/2024 | [AI search qua Slack, Drive, Salesforce, Jira](https://www.notion.com/releases/2024-06-18), có GPT-4, citation và phạm vi tìm kiếm. | Tri thức doanh nghiệp bị phân mảnh trong nhiều SaaS; trả lời không có nguồn khó được tin. | **Moat từ context/integration:** model phổ cập, nhưng kết nối nguồn, permission và citation trong workflow khó sao chép hơn. |
| 25/09/2024 | [“New Notion AI”](https://www.notion.com/releases/2024-09-25): connectors Google, chat GPT-4/Claude, style guide, đọc PDF/ảnh. | Chat AI độc lập ngày càng commodity; user cần AI có bối cảnh, đa model và nằm trong luồng cộng tác. | **Wrapper mỏng vs moat:** dùng model như commodity; giá trị nằm ở context, style, permission và collaboration layer. |
| 13/05/2025 | [AI Meeting Notes, Enterprise Search, Research Mode](https://www.notion.com/releases/2025-05-13); gộp AI vào Business/Enterprise. | Nhu cầu dịch từ năng suất cá nhân sang tri thức tổ chức; buyer cần bảo mật và pricing phù hợp. | **AI Expert + Domain Expert:** AI trong workflow knowledge work có permission/connectors là năng lực tổ chức, không chỉ add-on cá nhân. |
| 18/09/2025 | [Notion 3.0: Agents](https://www.notion.com/releases/2025-09-18): Agent làm chuỗi tác vụ nhiều bước trên pages/databases, có memory, instructions, connectors. | Sau database, search và connector, Notion đã có context lẫn bề mặt để hành động; thị trường chuyển từ AI trả lời sang agent hoàn thành việc. | **Moat workflow + vòng lặp hành động:** Agent đọc context và ghi ngược vào hệ thống; instruction, memory, lịch sử vận hành tăng switching cost. |

**Vì sao chọn những mốc này:** Tám mốc thể hiện bốn lần đổi lớp giá trị: AI writer → AI theo feedback → AI trên structured workflow/knowledge → AI liên thông và hành động. Tôi loại [AI dịch database property](https://www.notion.com/releases/2023-09-22), [one-click skills/global shortcut](https://www.notion.com/releases/2024-07-29), [Build with AI](https://www.notion.com/releases/2025-02-18) và [database research/Gmail/Linear search](https://www.notion.com/releases/2025-07-10), vì chúng là mở rộng/UX của các quyết định platform đã chọn, không đổi rõ JTBD, context hoặc buyer.

## §2. Tệp user & JTBD

| | Early adopters | Tệp hiện tại |
|---|---|---|
| **Đặc điểm** | *Linh* — PM/product marketer ở startup SaaS 10–50 người; dùng Notion hằng ngày cho brief/meeting notes, theo Product Hunt/AI Twitter, sẵn sàng thử alpha chưa hoàn thiện. | *Minh* — Head of Ops/Knowledge ở công ty công nghệ 100–500 người; giúp Sales, Product, Engineering tìm thông tin rải ở Notion, Slack, Drive, Jira mà không muốn ép team đổi tool. |
| **JTBD chính** | “Khi biến ý thô hoặc notes thành brief/email/proposal, hãy tạo bản nháp và chỉnh câu ngay trong trang tôi đang làm, để tôi gửi bản tốt nhanh hơn mà không mất context.” | “Khi có câu hỏi về dự án/chính sách/khách hàng, hãy tìm và tổng hợp câu trả lời có nguồn từ các hệ thống tôi được phép xem, để tôi trả lời hoặc quyết định trong vài phút.” |
| **Trước đó họ làm bằng cách nào** | Tự viết/sửa; copy–paste giữa Notion, Google/Grammarly/ChatGPT; đọc lại notes dài để rút action items. | Search keyword từng app, lục folder/page, nhắn người biết việc, dự họp lấy context rồi ghép câu trả lời thủ công. |

**Dịch chuyển tệp:** Q&A (14/11/2023) đổi job từ tạo artifact sang retrieval; connectors/citation (18/06/2024) và Enterprise Search/Research Mode (13/05/2025) mở Notion sang người sở hữu vấn đề tri thức cấp team/doanh nghiệp. Tệp mới cần câu trả lời có nguồn, permission và kết nối nhiều hệ thống.

**Switching cost (map 4 forces):**

| Force | Điều đang diễn ra với Notion AI |
|---|---|
| **Push** | Tool stack phân mảnh làm tốn thời gian tìm page, Slack thread, Drive file và hỏi đồng nghiệp; G2 cũng ghi nhận pain về navigation/tìm page trong workspace lớn. [G2](https://ai.g2.com/product/notion) |
| **Pull** | Citation, connected search, research, meeting notes và Agent hứa hẹn giảm context-switch, trả câu trả lời dùng được ngay trong workflow. |
| **Anxiety** | AI có thể sai/thiếu nếu knowledge base lộn xộn; có lo ngại privacy, permission, chi phí và agent sửa dữ liệu. Một review Q&A sớm phản ánh kết quả không đầy đủ. [Nguồn](https://www.reddit.com/r/Notion/comments/18wz58z) |
| **Habit & inertia** | Pages, databases, templates, taxonomy, history, quyền và automation của cả team đã nằm trong Notion; rời đi là phải tái tạo cấu trúc và dạy lại cách làm. Đây là lực giữ user mạnh nhất. |

Nếu dữ liệu, permission và automation có chuẩn mở để đối thủ thay thế không cần đổi thói quen, Notion AI dễ bị multi-home với ChatGPT/Slack AI/công cụ search khác; Notion có nguy cơ chỉ còn là nơi lưu tài liệu.

## §3. Ba dự đoán hướng đi (6–12 tháng tới)

> Mốc quan sát: **18/09/2025**; các dự đoán không dùng release sau ngày này.

**Dự đoán 1** *(loại: mở rộng tính năng)*  
- **Dự đoán:** Notion sẽ chuyển Agent thành custom agent theo phòng ban, có workflow template và trigger/schedule cho tác vụ lặp lại.
- **Lập luận:** Notion 3.0 đã có Agent, instructions, memory và hướng Custom Agents theo trigger/schedule; connectors + permissions từ §1 là nền để agent làm việc cho RevOps, HR, CS hay Engineering, không chỉ trả lời một lần.

**Dự đoán 2** *(loại: mở rộng segment)*  
- **Dự đoán:** Notion sẽ nhắm mạnh hơn tới RevOps, CS và People Ops — các team vận hành tri thức liên phòng ban.
- **Lập luận:** Tệp hiện tại ở §2 cần truy xuất câu trả lời giữa Notion, Slack, Drive, CRM và ticketing; các mốc 2024–2025 đã thêm Salesforce, Zendesk, Microsoft, Gmail, Linear, meeting notes và Research Mode. Đây là pain lớn, buyer rõ và phù hợp Enterprise Search/Agent hơn AI writer phổ thông.

**Dự đoán 3** *(loại: mô hình kiếm tiền)*  
- **Dự đoán:** Notion sẽ tách Agent/model cao cấp khỏi AI cơ bản bằng usage allowance hoặc add-on theo cấp doanh nghiệp.
- **Lập luận:** Họ từng đổi credits/query sang flat fee để khuyến khích khám phá AI writer, rồi gộp AI vào Business/Enterprise; nhưng Agent nhiều bước, Research Mode và model frontier có cost biến đổi cao. Pricing đồng hạng cho mọi mức dùng khó bền, nên tier/allowance là bước hợp logic.

**Dự đoán tự tin nhất:** Dự đoán 1, vì Notion 3.0 đã công bố rõ primitives và hướng Custom Agents. Nó sẽ gãy nếu doanh nghiệp không tin agent có quyền ghi/sửa dữ liệu, hoặc agent không đủ chính xác để vượt rủi ro governance; khi đó Notion sẽ dừng ở assistant/search “read-only”.

## §4. AI Log

| Việc | AI làm hay bạn làm? | Bạn kiểm chứng/phán đoán lại thế nào? |
|---|---|---|
| Tìm và tổng hợp changelog, launch post, Product Hunt/Hacker News/review | **AI (ChatGPT)** | AI đã mở nguồn chính thức và chèn link gốc. **Chưa có ghi nhận trong phiên này rằng học viên đã tự mở lại từng link**; cần làm việc đó trước khi nộp. |
| Chọn 8 milestone và loại mốc nhỏ | **AI (ChatGPT), theo tiêu chí đề bài** | AI dùng tiêu chí đổi JTBD/context/buyer để lọc và nêu mốc loại. Học viên cần rà lại xem có đồng ý với ranh giới “mốc lớn” không. |
| Viết context và map “revert nguyên lý” | **AI (ChatGPT)** | AI suy luận từ release/founder posts. Cần kiểm tra mỗi context có nguồn hỗ trợ và nguyên lý có khớp Day 16 không. |
| Lập archetype user, JTBD và 4 forces | **AI (ChatGPT)** | Archetype là suy luận, không phải phát ngôn của một user cụ thể; học viên cần đối chiếu với trải nghiệm free tier của mình. |
| Đưa ra 3 dự đoán | **AI (ChatGPT)** | Dự đoán được neo vào timeline/tệp user đến 18/09/2025. Học viên cần chọn điều mình thật sự tin và bảo vệ được khi bị hỏi. |

**Tự phản biện AI Log:** AI làm nhiều nhất ở research, tổng hợp và diễn đạt. Không nên coi đây là bài đã được học viên kiểm chứng hoàn toàn: trước khi nộp, học viên cần tự mở link nguồn, giải thích chuỗi “mốc → user/JTBD → dự đoán” và sửa mọi nhận định mình không đồng ý.
