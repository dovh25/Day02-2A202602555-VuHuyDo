# 02 — Group Problem Statement (Bản nộp nhóm)

> Làm chung 1 bản, mỗi thành viên copy vào repo cá nhân. Đi theo Phase 3 → 6 trong `01-worksheet.md`. Nhóm chỉ chọn **candidate problem** ở Phase 3, viết Problem Statement sau khi validate + vẽ workflow.

## Thành viên nhóm

| STT | Họ và tên | Mã học viên | Vai trò trong nhóm (VD: facilitator, workflow, research, writer) |
|-----|-----------|-------------|---------------------------------------------------------------|
| 1   | Vũ Huy Độ | 2A202602555 | Workflow & Tech Lead (đề xuất candidate, dựng workflow trước/sau, thiết kế ranh giới AI & fallback) |
| 2   | Nguyễn Hoàng Nam | 2A202602114 | Facilitator & Synthesis (điều phối thảo luận, gom cluster và thư ký tổng hợp tài liệu) |
| 3   | Trần Thu Trang | 2A202602388 | Validation & Research (thực hiện mini survey 8 học viên, phỏng vấn nhanh 2 dev, tìm kiếm giải pháp có sẵn) |
| 4   | Lê Minh Đức | 2A202602052 | Critic & Problem Statement Writer (đóng vai skeptic phản biện, rà soát boundary, viết hoàn thiện PS v0/v1) |

**Candidate problem nhóm chọn (1 câu):**
Tự động trích xuất và tạo Bug Report / GitHub Issue có cấu trúc từ Error Log và Traceback trong terminal.

---

## Phase 3 — Group Convergence: từ 9-12 candidates về 1

### 3.1. Trình bày top 3 mỗi người (mỗi candidate 1-2 phút)

| # | Người đưa ra | Candidate problem | Người gặp vấn đề | Điểm nghẽn | Cảm nhận nhanh của nhóm |
|---|---|---|---|---|---|
| 1 | Vũ Huy Độ | Chuyển traceback log thô thành GitHub Issue có cấu trúc | Học viên, dev test/fix bug | Đọc hiểu stack trace và gõ tay các bước reproduce steps | Rất thiết thực, ai cũng gặp hàng tuần, workflow đo được bằng phút |
| 2 | Vũ Huy Độ | Phân tích diff code đề xuất edge case checklist khi review PR | Peer reviewer trong nhóm | Đọc diff và tự nhẩm tìm lỗ hổng/edge case logic | Đau thật nhưng chất lượng gợi ý phụ thuộc ngữ cảnh toàn dự án |
| 3 | Vũ Huy Độ | Rà soát tự động checklist format nộp bài lab theo rubric | Học viên nộp bài lab | Soát thủ công từng tiêu chí trong rubric và từng file .md | Bài toán hay nhưng phần lớn giải được bằng script Rule đơn giản |
| 4 | Nguyễn Hoàng Nam | Tổng hợp Action Items và phân công task sau buổi họp online | Nhóm trưởng, facilitator | Nghe lại audio/đọc chat rời rạc để bóc tách task và hạn chót | Hay nhưng nhiều app meeting notes (Otter, Fellow) đã có sẵn |
| 5 | Nguyễn Hoàng Nam | Tự động nhắc hạn chót và cảnh báo chậm tiến độ task sprint | Thành viên nhóm đồ án | Hay quên cập nhật trạng thái task trên Kanban/Trello | Rule-based hoặc webhook bot nhắc việc là đủ, chưa cần đến AI |
| 6 | Nguyễn Hoàng Nam | Tạo bản tin Standup Update mỗi sáng từ git commit hôm trước | Developer, Tech Lead | Nhớ lại hôm qua đã làm gì để gõ báo cáo standup | Tiết kiệm ít thời gian (5 phút), giá trị tác động chưa đủ lớn |
| 7 | Trần Thu Trang | Tìm kiếm quyết định kỹ thuật từ lịch sử thảo luận Discord | Thành viên nhóm học tập | Search từ khóa Discord ra tin nhắn rời rạc, mất kết luận | Rất đau nhưng quyền truy cập API Discord và phân mảnh kênh quá lớn |
| 8 | Trần Thu Trang | Tra cứu nhanh barem điểm và quy chế nộp bài từ syllabus môn học | Học viên, trợ giảng (TA) | Hỏi lặp lại các câu hỏi đã có trong file hướng dẫn | Phạm vi hẹp, có thể giải quyết bằng tài liệu FAQ ghim đầu kênh |
| 9 | Trần Thu Trang | Tóm tắt tài liệu kỹ thuật dài và slide bài giảng phục vụ ôn lab | Sinh viên trong lớp | Đọc tài liệu dài 30-50 trang trước buổi thực hành | Quá rộng, khó xác định tiêu chí thành công cụ thể |
| 10 | Lê Minh Đức | Tự động sinh dữ liệu Mock API JSON cho Frontend kiểm thử | Frontend/Backend dev | Viết schema JSON mock thủ công cho các endpoint | Kỹ thuật tốt nhưng chỉ gặp ở bài tập lớn, bài lab nhỏ ít dùng |
| 11 | Lê Minh Đức | Đề xuất Unit Test cases cho các hàm xử lý logic phức tạp | Developer viết code | Tự nghĩ các trường hợp test bao phủ nhánh rẽ code | Hữu ích nhưng rủi ro AI sinh unit test sai cao, dễ mất thời gian debug test |
| 12 | Lê Minh Đức | Tự động chuẩn hóa format code và sửa lỗi linter trước khi commit | Developer nộp bài | Chạy linter và sửa tay từng lỗi thụt lề/format | Rule (Prettier, Black, Flake8) giải quyết 100%, không cần dùng AI |

### 3.2. Gom trùng / cluster (gom 9-12 ý thành 3-4 cụm)

| Cluster | Candidates included | Pattern chung | Ghi chú |
|---|---|---|---|
| A (Debug, Logging & Issue Tracking) | #1 (Độ), #10 (Đức), #11 (Đức) | Chuyển đổi dữ liệu kỹ thuật runtime thô (log, exception, API schema) thành tài liệu có cấu trúc phục vụ kiểm thử và sửa lỗi | Dữ liệu đầu vào dồi dào, có cấu trúc kỹ thuật sẵn, điểm nghẽn nằm ở khâu đọc hiểu và diễn giải |
| B (Code Review & Đảm bảo chất lượng) | #2 (Độ), #12 (Đức) | Đánh giá và kiểm tra mã nguồn tĩnh trước khi tích hợp vào nhánh chính (code diff, convention, edge cases) | #12 hoàn toàn là Rule; #2 cần AI nhưng phụ thuộc nhiều vào toàn bộ codebase |
| C (Quản lý tri thức, Q&A & Tra cứu tài liệu) | #7 (Trang), #8 (Trang), #9 (Trang) | Gom nhặt thông tin phân tán từ nhiều nguồn (Discord, syllabus, slides) để trả lời thắc mắc | Rủi ro data access phức tạp, dễ bị trượt thành chatbot tổng quát khó kiểm soát |
| D (Báo cáo, Họp & Quản lý Task) | #3 (Độ), #4 (Nam), #5 (Nam), #6 (Nam) | Quy trình hành chính nhóm: họp hành, theo dõi tiến độ, kiểm tra định dạng nộp bài | Đa số các bước có thể dùng Rule, checklist hoặc công cụ chuyên dụng có sẵn |

### 3.3. Shortlist (giữ 2-3 bài trả lời được 7 câu hỏi worksheet)

| Candidate | Vì sao vào shortlist (2-3 ý) | Rủi ro / điều chưa rõ |
|---|---|---|
| 1. Bug Report từ Error Traceback (Độ) | 1. Actor rõ ràng (học viên/dev chạy code bị lỗi), workflow 5 bước đo lường bằng phút cụ thể.<br>2. Bằng chứng pain point hàng tuần: 4-5 lần/tuần, đồng đội mất thời gian hỏi lại context.<br>3. Input (traceback log) có sẵn local, dễ chạy thử và kiểm chứng ngay trong lab. | Cần cơ chế lọc an toàn (Sanitization) để không đẩy API keys hay credentials trong log lên LLM. |
| 2. Edge Case Checklist cho PR Review (Độ & Đức) | 1. Ảnh hưởng trực tiếp đến chất lượng sản phẩm (tránh bug lọt vào main branch).<br>2. Đo lường được số bug phát hiện trước khi merge.<br>3. Workflow tích hợp tự nhiên vào GitHub Pull Request. | Khó khăn khi code diff ngắn nhưng logic liên quan đến nhiều file bên ngoài không có trong diff. |
| 3. Discord Chat FAQ Search (Trang) | 1. Nỗi đau chung của toàn bộ học viên trong lớp (ai cũng mất 15-20' tìm tin nhắn trôi).<br>2. Giá trị cộng đồng cao nếu giải quyết được. | Vấn đề phân quyền Discord API, dữ liệu chat phi cấu trúc, scope quá rộng cho lab 4 tiếng. |

### 3.4. Score để đồng thuận (chấm 1-5, ép nói rõ vì sao cho 5 / cho 3)

| Candidate | Actor rõ | Workflow rõ | Pain có evidence | Impact đo được | Làm trong lab | So sánh R/W/A được | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| **Bug Report từ Traceback Log** | 5 | 5 | 5 | 5 | 5 | 5 | 4 | **34** |
| **Edge Case Checklist cho PR** | 4 | 4 | 4 | 4 | 4 | 4 | 4 | **28** |
| **Discord Chat FAQ Search** | 4 | 3 | 5 | 4 | 3 | 4 | 4 | **27** |

**Candidate nhóm chọn (1 bài duy nhất):**

```text
Tự động trích xuất và tạo Bug Report / GitHub Issue có cấu trúc từ Error Log và Traceback trong terminal.
```

**Vì sao chọn (4-5 câu):**

```text
1. Bài toán xuất phát từ trải nghiệm thực tế hằng ngày của cả 4 thành viên khi chạy lab và code đồ án.
2. Quy trình hiện tại có điểm nghẽn rất rõ ràng ở bước diễn giải stack trace thành reproduce steps, mất trung bình 8-10 phút/lần.
3. Dữ liệu đầu vào (terminal log/traceback) hoàn toàn kiểm soát được ở máy cá nhân, không bị phụ thuộc vào phân quyền hệ thống bên ngoài.
4. Ranh giới giữa Rule (lọc sạch log, ẩn credentials), AI (phân tích lỗi, draft markdown issue) và Con người (kiểm tra ngữ cảnh, phê duyệt post) cực kỳ mạch lạc.
5. Chỉ số thành công đo lường được trực tiếp bằng thời gian (từ 18 phút xuống dưới 4 phút) và mức độ đầy đủ của issue.
```

**Vì sao KHÔNG chọn các candidate còn lại (mỗi bài 2-3 câu):**

```text
- Edge Case Checklist cho PR: Mặc dù có giá trị cao, nhưng việc phân tích edge case từ git diff đòi hỏi hiểu toàn bộ kiến trúc codebase; nếu chỉ đưa diff ngắn thì AI rất dễ sinh ra các gợi ý chung chung hoặc sai lệch, khó kiểm chứng chất lượng trong thời gian lab.
- Discord Chat FAQ Search: Vấn đề dữ liệu chat rất nhạy cảm về quyền riêng tư, cấu trúc kênh Discord phân tán và API rate limit phức tạp; nếu làm sẽ dễ trượt sang một dự án chatbot RAG cồng kềnh vượt quá khuôn khổ lab 4 tiếng.
```

**Disagreement (nếu có — ai lo gì, chốt ra sao):**

```text
Thành viên Đức lo ngại rằng file terminal log thường chứa các thông tin nhạy cảm như API key cá nhân, token kết nối database hoặc đường dẫn nhạy cảm của hệ điều hành, nếu đẩy thẳng lên cloud LLM sẽ vi phạm bảo mật.
Nhóm đã thống nhất giải quyết triệt để bằng cách: Đặt một bước bắt buộc dùng Rule Regex Sanitization chạy local trước khi dữ liệu được gửi đến LLM; đồng thời quy định LLM chỉ trả về bản nháp (draft) trên máy cá nhân để người dùng review trước khi bấm xác nhận tạo issue trên GitHub.
```

---

## Phase 4 — Quick Validation + Research

### 4.1. Quick validation (ít nhất 1 cách: interview 2-3 người hoặc survey 5-10 người)

| Nguồn | Số người / mẫu | Tín hiệu xác nhận (kèm quote nguyên văn) | Tín hiệu phản bác | Nhóm sửa problem thế nào |
|---|---:|---|---|---|
| Interview | 2 dev sinh viên lớp khác | "Mỗi lần test fail mà log dài cả trang là mình ngán nhất khoản copy rồi viết lại step tái hiện, nhiều lúc lười quá toàn ghi 'lỗi không chạy được' rồi bạn fix phải hỏi lại 4-5 tin nhắn." | "Nếu là lỗi cú pháp đơn giản thì nhìn 5 giây là sửa xong ngay, không cần mất công tạo issue làm gì." | Thu hẹp phạm vi: Chỉ áp dụng cho các lỗi runtime/exception phức tạp trong kiểm thử hoặc luồng phối hợp nhóm cần giao task fix bug. |
| Survey / poll | 8 học viên trong nhóm Discord | 7/8 bạn thừa nhận từng tạo issue thiếu thông tin ngữ cảnh hoặc bỏ qua bước reproduce steps vì tốn thời gian; 6/8 mong muốn có công cụ tự bóc tách dòng lỗi và file liên quan. | 2/8 bạn lo lắng công cụ tự động tạo rác (spam issue) nếu không được kiểm duyệt trước khi đăng. | Bổ sung Human Boundary bắt buộc: AI chỉ draft nội dung trên giao diện local, lập trình viên phải ấn nút 'Approve & Create Issue' mới gửi lên GitHub. |
| Log / ticket / review (nếu có) | 15 issues trên repo đồ án cũ | Rà soát 15 issue gần nhất: có 7 issue chỉ có tiêu đề cụ thể dưới 10 từ không có traceback; 5 issue khiến người fix phải comment hỏi lại môi trường và tham số đầu vào. | 3 issue có template đầy đủ nhưng người viết mất hơn 20 phút để soạn thảo. | Khẳng định tính cần thiết: Bài toán giải quyết cả hai mặt — vừa tiết kiệm thời gian cho người báo lỗi, vừa tăng chất lượng thông tin cho người sửa lỗi. |

**Insight sau validation (1-2 câu — pain thật nằm ở đâu):**

```text
Pain thật không nằm ở việc bấm nút tạo issue trên GitHub, mà nằm ở công đoạn đọc hiểu stack trace thô để viết thành reproduce steps và tóm tắt ngữ cảnh lỗi có nghĩa cho người khác đọc.
```

Bằng chứng đính kèm (nếu có): `02-group-problem-statement-survey.png`, `02-group-problem-statement-interview-notes.md`

### 4.2. Research giải pháp đã có (ít nhất 2-3 tools/patterns + 1-2 link kiểm được)

| Nguồn / tool / case | Link | Họ giải quyết bước nào? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| Sentry Error Tracking | https://sentry.io/welcome/ | Tự động bắt unhandled exceptions, gom nhóm lỗi (issue grouping) và trích xuất stack trace trên production | Rất mạnh về gom nhóm log lỗi, hiển thị breadcrumbs và metadata môi trường | Thiết kế cho hệ thống production lớn, quá cồng kềnh cho sinh viên chạy lab local; không tự viết narrative reproduce steps theo ngữ cảnh bài tập | Học tập cách bóc tách stack trace (file, line number, exception type) bằng Rule trước khi xử lý ngôn ngữ |
| GitHub Copilot for Issues | https://github.com/features/copilot | Hỗ trợ tóm tắt issue, gợi ý giải pháp sửa lỗi trực tiếp trong repository | Tích hợp sâu vào hệ sinh thái GitHub, hiểu bối cảnh mã nguồn repo | Bắt đầu từ khi issue đã tồn tại; chưa hỗ trợ khâu lấy log từ terminal máy cá nhân để khởi tạo issue ban đầu | Điểm can thiệp của nhóm là khâu 'Tiền Issue' (Terminal Log → Draft Issue) thay vì cạnh tranh ở khâu 'Hậu Issue' |
| Raygun Crash Reporting | https://raygun.com/platform/crash-reporting | Báo cáo crash tự động và phân loại mức độ nghiêm trọng của lỗi | Giao diện theo dõi lỗi trực quan, phân tích tần suất xuất hiện lỗi | Thiếu khả năng diễn giải ngôn ngữ tự nhiên thành các bước tái hiện thân thiện cho học viên | Cần kết hợp LLM để chuyển đổi dữ liệu kỹ thuật khô khan thành ngôn ngữ tự nhiên mạch lạc |

**Research takeaway (2-3 câu — nên build gì / không build gì):**

```text
Nhóm không nên cố gắng build một Agent tự động phân tích code hay tự sửa bug vì độ phức tạp quá cao và dễ ảo giác. Hướng đi đúng đắn nhất là xây dựng một Workflow bán tự động: dùng Rule để bắt log và lọc dữ liệu nhạy cảm, dùng LLM để phân tích stack trace và draft issue (tiêu đề, ngữ cảnh, reproduce steps), và giữ người lập trình làm chốt chặn kiểm duyệt cuối cùng trước khi tạo issue trên GitHub.
```

> Lưu ý: không dùng số liệu AI đưa nếu không verify được link chính thức. Ghi rõ giả định chưa chắc.

---

## Phase 5 — Workflow + Problem Statement

### 5.1. Current workflow bản nhóm

Dán workflow hoặc link file: `02-group-problem-statement-workflow.png/pdf/md`

```text
[1 Run test crash: 2' - Dev] → [2 Đọc traceback: 5' - Dev] → [3 Mở GitHub Issue: 1' - Dev] → [4 Viết mô tả & reproduce steps: 8' (bottleneck) - Dev] → [5 Copy log & Submit: 2' - Dev]
```

| Bước | Actor | Input | Output | Thời gian / tần suất | Ghi chú (handoff? bottleneck?) |
|---|---|---|---|---|---|
| 1 | Lập trình viên / Tester | Lệnh chạy test hoặc chạy script lab | Lỗi crash, xuất hiện traceback 50-200 dòng trong terminal | 2 phút / 4-5 lần/tuần | Người chạy test nhìn thấy màn hình báo lỗi đỏ |
| 2 | Lập trình viên | Traceback thô trên terminal | Xác định file bị lỗi, hàm gọi lỗi và loại exception | 5 phút | Phải scroll ngược terminal, dò từng frame gọi hàm |
| 3 | Lập trình viên | Trình duyệt web | Mẫu GitHub Bug Report mở sẵn | 1 phút | Chuyển ngữ cảnh từ Terminal sang Browser |
| 4 | Lập trình viên | Hiểu biết cá nhân về lỗi vừa xảy ra | Đoạn văn tóm tắt lỗi, ngữ cảnh xảy ra và các bước tái hiện (reproduce steps) | 8 phút | **Bottleneck chính**: Mất nhiều công sức chuyển đổi mã lỗi kỹ thuật thành văn bản mạch lạc, dễ nản và viết sơ sài |
| 5 | Lập trình viên | Đoạn log chọn lọc + nội dung đã viết | Issue chính thức được tạo trên GitHub với label/assignee | 2 phút | Handoff: Bàn giao task sửa bug cho đồng đội qua link issue |

**Bottleneck chính (2-3 câu):**

```text
Điểm nghẽn nằm ở Bước 4 (Viết mô tả ngữ cảnh và các bước tái hiện lỗi), chiếm gần 50% tổng thời gian quy trình (8/18 phút). Đây là công đoạn đòi hỏi nỗ lực tư duy diễn giải từ dữ liệu máy (traceback) sang ngôn ngữ người, dẫn đến tình trạng học viên hay bỏ qua hoặc viết sơ sài, gây hậu quả là đồng đội phải tốn thêm 20-30 phút hỏi lại ngữ cảnh để tái hiện bug.
```

### 5.2. Future workflow bản nhóm

Phải nhìn ra 5 thứ: bước nào máy (Rule), bước nào AI, bước nào người, boundary ở đâu, fallback khi AI sai.

```text
[1 Script auto-capture log & regex sanitize: 0.5' - Máy/Rule] 
→ [2 AI parse stack trace & draft issue (context + steps): 1' - AI Workflow] 
→ [3 Dev review, chỉnh sửa ngữ cảnh: 2' - Người (Human Boundary)] 
→ [4 Auto-post GitHub issue qua API: 0.5' - Máy/Rule]

Fallback: Nếu AI draft sai hoặc thiếu logic, Dev nhấn nút "Reset to manual template" và tự điền như quy trình cũ (mất 15 phút, không làm tắc nghẽn công việc).
```

**Before/after impact:**

| Metric | Trước | Sau kỳ vọng | Cách đo |
|---|---:|---:|---|
| Tổng thời gian | 18 phút | Dưới 4 phút | Bấm giờ thực tế từ khi crash terminal đến khi có issue trên GitHub |
| Số bước | 5 bước | 4 bước | Đếm số công đoạn trong sơ đồ quy trình |
| Số bước thủ công | 5 / 5 bước | 1 / 4 bước | Chỉ còn bước Dev review & approve là thủ công |
| Bottleneck chính | Viết diễn giải & reproduce steps (8') | Dev đọc lướt kiểm tra bản nháp (2') | Thời gian của bước chiếm tỷ trọng cao nhất trong flow |
| Risk mới | Không có AI hallucination | AI có thể suy đoán sai bước tái hiện hoặc lọt API key | Đo tỷ lệ issue phải sửa lại sau khi AI draft và kiểm tra regex log |

### 5.3. Problem Statement v0 (mỗi field 2-3 câu)

| Field | Nội dung |
|---|---|
| **Actor** | Học viên khóa kỹ sư AI và sinh viên kỹ thuật phần mềm đang làm việc nhóm trong các bài tập lab hoặc đồ án sprint. Họ là những người trực tiếp chạy code kiểm thử và phát hiện lỗi runtime cần bàn giao cho đồng đội sửa. |
| **Workflow** | Quy trình ghi nhận bug gồm: gặp lỗi crash trong terminal → đọc hiểu traceback → mở GitHub Issue → gõ tay mô tả và các bước tái hiện → copy log và submit issue. |
| **Bottleneck** | Khâu đọc hiểu stack trace thô và chuyển thể thành các bước tái hiện (reproduce steps) cùng ngữ cảnh lỗi bằng ngôn ngữ tự nhiên mất từ 8-10 phút mỗi lần và rất dễ gây nản. |
| **Impact** | Tốn khoảng 75-90 phút/tuần cho mỗi cá nhân (khoảng 5-6 giờ/tuần cho cả nhóm 4 người). Hậu quả phụ là các issue được tạo quá sơ sài ("lỗi không chạy được") làm người nhận fix bug mất thêm 20-30 phút trao đổi qua lại trên Discord. |
| **Success Metric** | Giảm tổng thời gian tạo một bug issue hoàn chỉnh từ 18 phút xuống dưới 4 phút. Đảm bảo 100% issue tạo ra có đầy đủ 4 trường chuẩn: Tiêu đề súc tích, Ngữ cảnh hệ thống, Các bước tái hiện chi tiết và Log trích đoạn sạch. |
| **Boundary** | Phạm vi làm: Hỗ trợ tự động trích xuất log lỗi runtime từ terminal cá nhân, làm sạch dữ liệu và sinh bản nháp issue trên máy local. Phạm vi không làm: Không can thiệp vào mã nguồn để tự sửa code (auto-fix) và không tự ý đăng issue lên GitHub mà chưa có sự phê duyệt của người dùng. |

**Câu hỏi AI phản biện v0 (nếu có):**
- Field nào mơ hồ: Boundary chưa nói rõ cách xử lý khi log lỗi quá dài vượt quá context window của model hoặc khi log chứa dữ liệu nhạy cảm.
- Tôi sửa gì: Bổ sung cơ chế Rule Regex Sanitization vào boundary để loại bỏ API keys/tokens trước khi gửi log, và quy định giới hạn độ dài log tối đa 200 dòng quan trọng nhất của stack trace.

---

## Phase 6 — Rule / Workflow / Agent + Decision

### 6.0. Ma trận độ phù hợp (suy nghĩ nhanh, không thay quyết định cuối)

- Độ mơ hồ: [x] Thấp (có đúng/sai rõ) / [ ] Cao (nhiều cách trả lời vẫn OK) — Vì sao: Lỗi crash có mã lỗi, tên file, dòng code và thông điệp ngoại lệ (exception message) hoàn toàn xác định; mục tiêu là trích xuất chính xác thông tin này vào mẫu issue chuẩn.
- Độ phức tạp: [ ] Thấp (1-2 bước) / [x] Cao (3+ bước/nguồn, phụ thuộc nhau) — Vì sao: Quy trình gồm nhiều bước nối tiếp: bắt log từ terminal → lọc sạch dữ liệu nhạy cảm bằng Regex → gọi LLM phân tích stack trace → hiển thị giao diện review local → gọi API GitHub tạo issue.

**Bài toán nhóm nằm ở ô nào:**

```text
Ô "Độ mơ hồ thấp — Độ phức tạp cao" (Workflow điều phối nhiều bước rõ ràng, chưa cần Agent).
```

**Vì sao (2-3 câu):**

```text
Bài toán đòi hỏi sự phối hợp chặt chẽ giữa các công cụ xác định (terminal capture, regex filter, GitHub API) và một bước xử lý ngôn ngữ tự nhiên (draft narrative). Các bước đi theo một đường thẳng cố định, không đòi hỏi hệ thống phải tự động lên kế hoạch động hay tự quyết định rẽ nhánh phức tạp.
```

### 6.1. So sánh Rule / Workflow / Agent (so trên cùng 1 bài)

| Mức | Phương án cho bài toán nhóm | Khi nào đủ | Rủi ro | Chọn? (Dùng cho bước nào?) |
|---|---|---|---|---|
| **Rule** | Viết script regex bắt log terminal, lọc file/dòng lỗi và dán thẳng nguyên văn vào GitHub Issue template | Đủ khi chỉ cần báo cáo lỗi đơn giản, người đọc tự đọc log thô để hiểu | Không viết được ngữ cảnh, không sinh được các bước tái hiện (reproduce steps); người fix vẫn phải tự đọc log | Dùng cho bước 1 (bắt log, lọc token/keys) và bước 4 (post API lên GitHub) |
| **Workflow** | Chuỗi kết hợp: Rule lọc log và ẩn credentials → LLM phân tích stack trace draft nội dung issue → Lập trình viên kiểm duyệt/sửa nhanh → Script đẩy lên GitHub | Đủ khi các bước xử lý đi theo luồng xác định, AI chỉ hỗ trợ khâu tóm tắt và draft narrative | Rủi ro AI có thể suy đoán sai bước reproduce nếu log thiếu tham số; cần người review duyệt trước khi post | **CHỌN TOÀN BỘ GIẢI PHÁP** (Phù hợp nhất với mục tiêu và năng lực nhóm) |
| **Agent** | Xây dựng Agent tự động đọc terminal, tự mở source code kiểm tra, tự động chạy lại các lệnh để tìm cách tái hiện rồi tự post issue | Đủ khi cần một hệ thống QA tự hành hoàn toàn không cần sự can thiệp của con người | Cực kỳ phức tạp, tốn token, độ trễ cao, rủi ro chạy lệnh ngoài ý muốn trên máy người dùng, dễ gây spam issue | **KHÔNG CHỌN** (Quá phức tạp, không cần thiết cho mục tiêu tiết kiệm thời gian) |

**5 câu hỏi chốt (trả lời câu đầy đủ):**
1. Rule có giải được 70-80% case không? -> Không, Rule chỉ lọc và format được văn bản tĩnh, không thể diễn giải stack trace thành các bước tái hiện (reproduce steps) bằng ngôn ngữ tự nhiên.
2. Các bước có đi thẳng một đường không hay phải rẽ nhánh? -> Quy trình đi thẳng một đường tuần tự: Bắt log → Làm sạch → AI draft → Người review → Đăng issue.
3. Có thật sự cần Agent tự lập kế hoạch + gọi tool không? -> Hoàn toàn không cần, vì thứ tự các bước đã cố định và không cần agent tự suy nghĩ bước tiếp theo.
4. Nếu AI sai, ai phát hiện đầu tiên và sửa trong bao lâu? -> Lập trình viên tại bước Human Boundary sẽ phát hiện ngay trên màn hình preview và sửa lại chỉ trong 30-60 giây hoặc bấm nút fallback.
5. Có hạ được từ Agent → Workflow → Rule không? -> Có thể hạ từ Agent xuống Workflow rất tự nhiên; và nếu AI gặp sự cố, hệ thống tự động fallback về Rule (mở template điền tay truyền thống).

**Mức chọn:**

```text
Workflow
```

**Vì sao chọn (3-4 câu):**

```text
Workflow là điểm cân bằng hoàn hảo giữa hiệu quả và độ tin cậy. Nó tận dụng tối đa sức mạnh của Rule ở những khâu đòi hỏi tính chính xác tuyệt đối (lọc dữ liệu nhạy cảm, gọi API) và tận dụng LLM ở đúng bước nghẽn nhất (đọc hiểu traceback và draft narrative). Mô hình này loại bỏ hoàn toàn sự cồng kềnh và rủi ro khó kiểm soát của Agent tự hành.
```

**Vì sao không chọn mức đơn giản hơn (2-3 câu):**

```text
Mức Rule đơn thuần đã tồn tại dưới dạng GitHub Issue Template tĩnh từ lâu nhưng không giải quyết được gốc rễ của điểm nghẽn: lập trình viên vẫn phải tự đọc hàng chục dòng log và tự gõ từng bước reproduce steps, dẫn đến việc họ tiếp tục viết sơ sài hoặc bỏ qua bước ghi nhận lỗi.
```

### 6.2. Problem Statement v1 (v0 sửa chặt hơn + 3 field cuối)

| Field | Nội dung |
|---|---|
| **Actor** | Học viên khóa kỹ sư AI và sinh viên kỹ thuật phần mềm đang làm việc nhóm trong các dự án lab/sprint, chịu trách nhiệm kiểm thử và bàn giao bug report cho đồng đội qua GitHub. |
| **Workflow** | Chạy code gặp lỗi runtime trong terminal → Script tự động bắt log và dùng Rule Regex lọc sạch credentials → AI phân tích stack trace và draft issue chuẩn → Người dùng kiểm duyệt/chỉnh sửa trên giao diện local → Tự động tạo GitHub Issue. |
| **Bottleneck** | Bước đọc hiểu stack trace thô và chuyển thể thành các bước tái hiện (reproduce steps) cùng ngữ cảnh lỗi bằng ngôn ngữ tự nhiên (hiện chiếm 8-10 phút/lần). |
| **Impact** | Tiết kiệm 75-90 phút/tuần cho mỗi lập trình viên; giảm hơn 70% số tin nhắn hỏi lại ngữ cảnh trên Discord; nâng cao chất lượng tài liệu hóa lỗi trong dự án. |
| **Success Metric** | Giảm tổng thời gian từ khi gặp crash đến khi issue được tạo từ 18 phút xuống dưới 4 phút; 100% issue có đủ 4 phần chuẩn; tỷ lệ issue phải sửa đổi sau khi tạo giảm xuống dưới 10%. |
| **Boundary** (làm / không làm) | **Làm**: Bắt log terminal local, lọc sạch API key/token, trích xuất mã lỗi, sinh bản nháp markdown issue, hỗ trợ xem trước và chỉnh sửa. **Không làm**: Không tự động sửa code trong repository, không tự ý chạy lại lệnh terminal nguy hiểm, không tự động đăng issue lên GitHub khi chưa có sự xác nhận của người dùng. |
| **AI intervention point** (can thiệp sau bước nào, trước bước nào) | Can thiệp sau bước 1 (sau khi log thô đã được Rule bắt và lọc sạch dữ liệu nhạy cảm) và trước bước 3 (trước khi bản nháp được hiển thị cho lập trình viên kiểm duyệt). |
| **Mức chọn** (Rule / Workflow / Agent + 1 câu vì sao) | **Workflow** — vì quy trình gồm các bước xác định nối tiếp nhau, AI chỉ đóng vai trò hỗ trợ phân tích và draft nội dung ở một công đoạn cụ thể có con người kiểm soát. |
| **Rủi ro & người thật kiểm tra** (rủi ro lớn nhất + ai kiểm tra bằng cách nào) | Rủi ro lớn nhất là AI suy đoán sai các bước tái hiện (hallucination) do log không đủ thông tin; người báo cáo lỗi (human reviewer) là chốt chặn kiểm tra trực tiếp trên giao diện preview trước khi bấm nút xác nhận tạo issue. |

### 6.3. Final decision

| Câu hỏi | Yes / Not Yet / No | Ghi chú (câu đầy đủ) |
|---|---|---|
| Actor + workflow rõ chưa? | Yes | Actor là sinh viên/dev chạy code kiểm thử; workflow gồm 4 bước tuần tự rõ ràng. |
| Baseline + metric đo được chưa? | Yes | Baseline 18 phút/issue; mục tiêu dưới 4 phút/issue đo bằng đồng hồ bấm giờ. |
| Data/input đủ dùng chưa? | Yes | Terminal log và traceback có sẵn ngay trên máy local mỗi khi chạy lệnh kiểm thử. |
| AI sai, hậu quả chấp nhận được không? | Yes | Nếu AI draft sai, người dùng chỉ mất 30 giây sửa lại trên giao diện preview hoặc bấm fallback điền tay. |
| Có người review/owner không? | Yes | Người chạy code kiểm thử đóng vai trò reviewer bắt buộc trước khi tạo issue trên GitHub. |
| Có cách non-AI đơn giản hơn không? | Yes | Đã so sánh với Rule-based template và khẳng định Rule không thể tự sinh reproduce steps bằng ngôn ngữ tự nhiên. |

**Decision:**

```text
Go
```

**Lý do (3-4 câu dựa trên bằng chứng):**

```text
1. Bài toán có giá trị thực tế cao, giải quyết trúng điểm nghẽn tốn thời gian hằng ngày của sinh viên và kỹ sư phần mềm.
2. Dữ liệu đầu vào (terminal log) hoàn toàn sẵn có, không phụ thuộc vào quyền truy cập hệ thống phức tạp bên ngoài.
3. Ranh giới giải pháp là Workflow bán tự động với Human in the loop, đảm bảo rủi ro bằng không đối với hệ thống mã nguồn.
4. Mức độ khả thi kỹ thuật cao, hoàn toàn có thể xây dựng bản mẫu (prototype) và kiểm chứng ngay trong một sprint ngắn.
```

**Nếu Go — pilot nhỏ nhất (data nào, chạy tay ra sao, đo 3 số nào):**

```text
- Data: Thu thập 10 file log lỗi runtime Python thực tế từ các bài thực hành Day 1 và Day 2 của nhóm.
- Chạy tay: Chạy script trích xuất log local, đưa qua prompt LLM chuẩn hóa để sinh bản nháp markdown, sau đó 2 thành viên trong nhóm thực hiện review và đăng thử nghiệm lên repo test GitHub.
- Đo 3 số:
  1. Thời gian trung bình từ lúc nạp log đến khi hoàn tất issue (mục tiêu: < 4 phút).
  2. Tỷ lệ bước tái hiện (reproduce steps) chính xác mà không cần sửa lại (mục tiêu: > 80%).
  3. Tỷ lệ lọc sạch 100% các chuỗi token/credentials mẫu giả lập trong log (mục tiêu: 100%).
```

**Nếu Not Yet — cần validate gì trước:**

```text
Không áp dụng vì nhóm đã quyết định GO.
```

**Nếu No-Go — làm gì thay AI:**

```text
Không áp dụng vì nhóm đã quyết định GO.
```

**Exit / rollback (khi nào dừng AI, quay về cách cũ):**

```text
Nếu trong quá trình pilot nhận thấy: (1) Tỷ lệ hallucination của AI ở bước reproduce steps vượt quá 30% khiến người dùng mất nhiều thời gian sửa lại hơn cả tự viết; hoặc (2) Phí token API quá cao so với giá trị thời gian tiết kiệm được; nhóm sẽ rollback về sử dụng script Rule thuần túy (chỉ format log và chèn vào issue template tĩnh của GitHub).
```

---

### Self-check nộp phần 02 (nhóm)
- [x] Có nhật ký hội tụ 9-12 → 1 (cluster + shortlist + score)
- [x] Có validation (quote thật) + research (link kiểm được)
- [x] Có workflow trước/sau đủ thời gian, handoff, bottleneck, boundary, fallback
- [x] Có PS v0 → v1, metric có trước/sau + cách đo, boundary có làm/không làm
- [x] Có so sánh Rule/Workflow/Agent + Decision Go/Not Yet/No-Go có lý do
