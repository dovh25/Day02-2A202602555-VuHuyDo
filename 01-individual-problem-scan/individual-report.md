# 01 — Individual Problem Scan

> Điền theo Phase 1 + Phase 2 trong `01-worksheet.md`. Tự scan trước, dùng AI sau để phản biện. Không copy ví dụ Weekly Report.

## Thông tin cá nhân

- Họ và tên: Vũ Huy Độ
- Mã học viên: 2A202602555
- Vai trò / bối cảnh (VD: sinh viên năm X, intern PM, ...): Sinh viên năm 4 ngành Công nghệ Thông tin, Học viên chương trình AI Engineer (VinUni AI20k), kiêm Thực tập sinh Kỹ thuật phần mềm (Software Engineer Intern).
- Công việc hằng tuần (3-5 gạch đầu dòng để soi problem):
  - Tham gia các buổi lab thực hành AI/LLM, giải quyết bài tập lập trình và nộp báo cáo qua repository GitHub hằng tuần.
  - Nghiên cứu tài liệu kỹ thuật, API docs, papers và tài liệu hướng dẫn để cấu hình môi trường và tích hợp thư viện/framework AI.
  - Phối hợp làm việc nhóm: họp sync kiến trúc, phân chia task sprint, trao đổi kỹ thuật trên Discord và quản lý issue/PR trên GitHub.
  - Chạy thử nghiệm, kiểm thử code, debug lỗi hệ thống/môi trường và tham gia review Pull Request của bạn cùng nhóm.
  - Viết tài liệu kỹ thuật, tổng hợp tiến độ sprint và chuẩn bị slide demo sản phẩm đồ án.

---

## Phase 1 — Scan 5+ problems (tối thiểu 5, khuyến khích 8-10)

**Cách điền:** mỗi dòng = việc gì + ai chịu + đo bằng gì. Cột `Dấu hiệu thật` bắt buộc có số: mất bao lâu (bấm giờ mấy lần), mấy lần/tuần, bao nhiêu người gặp, log/ticket/quote nào.

| # | Lăng kính (Lặp lại / Tốn thời gian / AI có thể tốt hơn / Pain từ người khác) | Problem quan sát được | Ai chịu ảnh hưởng? | Dấu hiệu thật (số + bằng chứng) |
|---|---|---|---|---|
| 1 | Lặp lại | Khi chạy test/code phát sinh lỗi, phải copy-paste và format lại log lỗi/traceback hàng trăm dòng thành bug issue ticket có cấu trúc trên GitHub | Dev phụ trách test/fix bug, người review | 4-5 lần/tuần; mất 15-20 phút/lần format; tuần trước có 8 issue thiếu context khiến đồng đội phải nhắn hỏi lại 3-4 lần/issue trên Discord |
| 2 | Lặp lại | Rà soát thủ công từng tiêu chí trong checklist/rubric trước khi nộp bài tập lab (tên file, format bảng, metadata, cấu trúc folder) | Học viên nộp bài (Vũ Huy Độ) | 2-3 lần/tuần; mất 25-30 phút/lần bấm giờ; tuần trước có 3 bạn trong nhóm bị trừ 10-15% điểm do nộp thiếu ảnh workflow hoặc sai tên file |
| 3 | Tốn thời gian | Đọc lướt và phân tích diff code 200-400 dòng trong Pull Request để phát hiện các edge cases tiềm ẩn và rủi ro logic | Peer reviewer trong nhóm đồ án | 3-4 PR/tuần; mất 40-50 phút/PR; từng để lọt 2 bug nghiêm trọng vào nhánh chính (main) làm crash chương trình demo tuần trước |
| 4 | Tốn thời gian | Đọc và chắt lọc tài liệu API/thư viện AI mới dài hàng chục trang để tìm đúng cấu hình tham số và cú pháp tương thích | Học viên làm lab, AI Intern | 2 lần/tuần; mất 60-90 phút/lần; trung bình mở 8-10 tab tài liệu và phải thử sai 3-4 lần mới cấu hình thành công |
| 5 | Tốn thời gian | Tổng hợp biên bản họp online (30-45') thành danh sách action items, deadline và người phụ trách lên bảng task nhóm | Nhóm trưởng / Facilitator nhóm | 2 lần/tuần; mất 35-40 phút/lần nghe lại/đọc chat ghi chú; tuần nào cũng có ít nhất 1 thành viên hỏi lại "task này hạn chót là khi nào" |
| 6 | AI có thể tốt hơn | Tìm kiếm và xâu chuỗi các quyết định kỹ thuật / câu trả lời giải đáp từ hàng trăm tin nhắn thảo luận trên Discord nhóm/lớp | Học viên, thành viên trong nhóm | 3-5 lần/tuần; mất 15-20 phút/lần scroll tìm kiếm; Discord search chỉ tìm từ khóa rời rạc không tổng hợp được kết luận cuối |
| 7 | AI có thể tốt hơn | Đối chiếu và lập bảng so sánh benchmark kỹ thuật (latency, throughput, VRAM, context window) của các mô hình LLM từ nhiều bài báo/blog | AI Engineer Intern, sinh viên làm đồ án | 1-2 lần/sprint; mất ~2 giờ đọc lướt 5-6 bài viết khác nhau để gom số liệu vào bảng tính |
| 8 | Pain từ người khác | Bạn cùng nhóm liên tục hỏi lại cách cấu hình môi trường chạy code (Python venv, CUDA driver, Docker) vì tài liệu setup thiếu context OS | Dev ít kinh nghiệm DevOps và người phải hỗ trợ (Độ) | 2-3 lần mỗi khi bắt đầu đồ án mới; mất 30-45 phút/lần hỗ trợ qua screen share Discord; tuần trước mất 2 tiếng fix lỗi pip dependency cho 2 bạn |
| 9 | Pain từ người khác | Giảng viên/Trợ giảng (TA) phải trả lời lặp đi lặp lại cùng một câu hỏi về quy định nộp bài muộn và barem điểm trên email/Discord | Trợ giảng (TA), giảng viên | TA nhận 15-20 câu hỏi trùng nội dung trong 48h trước deadline; mất 2-3 giờ/tuần chỉ để copy-paste câu trả lời từ syllabus |
| 10 | Pain từ người khác | Thành viên nhóm viết commit message và mô tả Pull Request quá sơ sài ("update code", "fix bug") khiến người merge không hiểu bối cảnh | Sub-lead kỹ thuật, người maintain repo | 5-7 PR/tuần có mô tả dưới 10 từ; mất 10-15 phút/PR trao đổi xác nhận trước khi dám merge; từng gây xung đột code mất 1 giờ rollback |

> Gợi ý tự soi: tuần trước mất nhiều thời gian nhất vào việc gì? Việc gì hay trì hoãn? Người khác hay hỏi lại câu gì? Workflow nào ai cũng biết là chậm?

**AI đã dùng ở Phase 1 (nếu có):**
- Prompt đã hỏi: "Tôi là sinh viên năm cuối CNTT kiêm Software Engineer Intern tại một nhóm dự án AI. Công việc hằng tuần gồm làm lab AI/LLM, review PR, debug lỗi runtime, setup môi trường và viết báo cáo tiến độ. Hãy gợi ý thêm các pain points thường gặp theo 4 lăng kính (Lặp lại, Tốn thời gian, AI có thể tốt hơn, Pain từ người khác) kèm actor cụ thể và số đo định lượng. Không đưa ý tưởng chung chung kiểu làm chatbot hay trợ lý toàn năng."
- Ý dùng được: Phân tách góc nhìn giữa người tạo lỗi (tester/developer) và người tiếp nhận xử lý (reviewer/assignee) ở khâu ghi nhận bug; gợi ý số đo cụ thể về số tin nhắn hỏi lại (back-and-forth messages) trên Discord khi bug report thiếu ngữ cảnh.
- Ý bỏ vì không phải pain thật: AI gợi ý "Tự động sinh toàn bộ code đồ án từ yêu cầu môn học" và "Agent tự động tham gia họp và nói thay sinh viên" — đây là những bài toán giải pháp viển vông (solution-first), thiếu tính khả thi và vi phạm tính trung thực học thuật, không phản ánh điểm nghẽn quy trình thực tế.

**Self-check Phase 1:**
- [x] Đủ 5+ dòng, mỗi dòng có actor + số đo cụ thể (đã scan đủ 10 dòng có số liệu thật)
- [x] Dùng ít nhất 3/4 lăng kính (đã dùng đủ cả 4 lăng kính)
- [x] Không có dòng chung chung kiểu "mất nhiều thời gian"

---

## Phase 2 — Top 3 Problem Cards

### 2.1. Chọn top 3

Giữ bài nào: actor cụ thể, workflow vẽ được 3-7 bước, bottleneck ở 1 bước, impact đo được. Loại bài quá rộng.

| Rank | Problem (copy từ bảng scan) | Vì sao chọn (2-3 ý) | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Khi chạy test/code phát sinh lỗi, phải copy-paste và format lại log lỗi/traceback hàng trăm dòng thành bug issue ticket có cấu trúc trên GitHub | 1. Workflow 5 bước cực kỳ rõ ràng, bottleneck tập trung ở bước trích xuất ngữ cảnh và viết reproduce steps.<br>2. Đo lường được chính xác bằng thời gian (18 phút -> 4 phút/issue).<br>3. Ranh giới giữa Rule (lọc log, che token), AI (tóm tắt, draft narrative) và Human (review, submit) rất tường minh. | Cần cơ chế regex hiệu quả để loại bỏ dữ liệu nhạy cảm (API key, token, user credentials) trước khi đẩy log vào LLM. |
| 2 | Đọc lướt và phân tích diff code 200-400 dòng trong Pull Request để phát hiện các edge cases tiềm ẩn và rủi ro logic | 1. Pain point lớn hàng tuần của nhóm, ảnh hưởng trực tiếp đến chất lượng code nhánh chính.<br>2. Giảm thiểu nguy cơ lọt bug vào production/demo.<br>3. AI hỗ trợ tốt việc đối chiếu diff code với các mẫu lỗi edge case thường gặp. | Chất lượng gợi ý edge case của AI có thể phụ thuộc nhiều vào ngữ cảnh toàn dự án mà diff code không thể hiện hết. |
| 3 | Rà soát thủ công từng tiêu chí trong checklist/rubric trước khi nộp bài tập lab (tên file, format bảng, metadata, cấu trúc folder) | 1. Tần suất lặp lại cố định 2 lần/tuần, sát sườn với quyền lợi điểm số của học viên.<br>2. Dễ dàng kết hợp Rule-based (kiểm tra cây thư mục, tên file) và AI (đánh giá độ đầy đủ nội dung text).<br>3. Giúp loại bỏ hoàn toàn lỗi bất cẩn trước hạn nộp. | Phải cập nhật rubric mẫu liên tục theo từng bài lab khác nhau để AI đối chiếu chuẩn xác. |

### 2.2. Problem Cards chi tiết (lặp lại cho cả 3 cards)

---

#### Problem Card #1 — Tự động trích xuất và tạo Bug Report / GitHub Issue có cấu trúc từ Error Log và Traceback

```text
Problem 1 câu:
Khi chạy kiểm thử hoặc chạy lab phát sinh lỗi, học viên/lập trình viên mất 15-20 phút mỗi lần để lọc qua hàng trăm dòng traceback thô trong terminal, đọc hiểu và viết lại thành bug report / GitHub issue có cấu trúc với các bước tái hiện (reproduce steps) rõ ràng.

Actor:
Học viên / Software Engineer Intern (người trực tiếp chạy code, thực hiện kiểm thử và ghi nhận lỗi để bàn giao cho đồng đội).

Thời điểm / bối cảnh:
Trong quá trình phát triển đồ án nhóm hoặc làm bài lab thực hành, khi gặp crash/exception trong terminal cần tạo issue trên GitHub để theo dõi và bàn giao cho người fix.

Current workflow 3-7 bước:
1. Chạy test/chương trình gặp lỗi crash, xuất hiện traceback 50-200 dòng trong terminal (2')
2. Đọc lướt log, lần theo stack trace để xác định file, hàm và thông báo lỗi gốc (5')
3. Mở GitHub Repository -> New Issue, chọn mẫu Bug Report template (1')
4. Tự viết diễn giải lỗi: tóm tắt ngữ cảnh, viết các bước tái hiện (reproduce steps) và kết quả mong muốn (8')
5. Copy đoạn log lỗi liên quan dán vào khối markdown, gán label/assignee và bấm submit (2')

Bottleneck:
Bước 4 — Đọc hiểu traceback và chuyển đổi thủ công các dòng mã lỗi kỹ thuật thành văn bản mô tả mạch lạc kèm reproduce steps chuẩn chỉnh (mất 8-10 phút, dễ nản nên hay viết sơ sài).

Impact:
4-5 lần/tuần, tốn 75-90 phút/tuần cho 1 cá nhân; cả nhóm 4 người tốn ~5-6 giờ/tuần. Nếu viết ẩu ("lỗi không chạy được"), đồng đội mất thêm 20-30 phút chat hỏi lại ngữ cảnh để tái hiện lỗi.

Success metric:
Giảm tổng thời gian tạo issue từ 18 phút xuống dưới 4 phút/issue; 100% issue tạo ra có đủ 4 phần (Tiêu đề chuẩn, Ngữ cảnh, Reproduce steps, Log trích đoạn); giảm 70% số tin nhắn hỏi lại thông tin trên Discord.

Non-AI alternative:
Sử dụng GitHub Issue Template tĩnh + Script regex lọc bỏ bớt dòng log thừa. Tuy nhiên regex không thể tự tóm tắt root cause logic và không suy luận được reproduce steps từ chuỗi gọi hàm.

AI hypothesis:
Script tự động thu thập log thô và che thông tin nhạy cảm (Rule) -> LLM phân tích stack trace, xác định nguyên nhân cốt lõi và draft sẵn tiêu đề, ngữ cảnh cùng reproduce steps (AI) -> Người dùng kiểm tra lại độ chính xác và bấm submit (Human boundary).

Quick gut:
[ ] No AI / process fix
[ ] Rule
[x] Workflow
[ ] Agent
[ ] Chưa biết
```

**Draft workflow Card #1** (ASCII / Mermaid / ảnh đính kèm):

```text
CURRENT STATE — 18 phút

[1 Run test fail: 2'] 
→ [2 Đọc traceback: 5'] 
→ [3 Mở GitHub issue: 1'] 
→ [4 Viết mô tả & reproduce steps: 8']  <-- bottleneck
→ [5 Copy log & submit: 2']

FUTURE STATE — 4 phút

[1 Script auto-capture log & regex sanitize: 0.5']  -- Rule
→ [2 AI parse stack trace & draft issue (context + steps): 1']  -- AI Workflow step
→ [3 Dev review, chỉnh sửa ngữ cảnh: 2']  <-- human boundary
→ [4 Auto-post GitHub issue: 0.5']

Fallback: nếu AI draft sai hoặc thiếu logic thì Dev nhấn "Reset to manual template" và tự điền như cũ (mất 15 phút, không làm tắc nghẽn quy trình).
```

File đính kèm (nếu vẽ riêng): `01-individual-problem-scan-workflow-card-1.png`

---

#### Problem Card #2 — Phân tích Git Diff và đề xuất Edge Case Checklist hỗ trợ Review Pull Request

```text
Problem 1 câu:
Reviewer mất 40-50 phút cho mỗi Pull Request 200-400 dòng diff code vì phải tự nhẩm đọc từng khối logic để tìm kiếm các trường hợp biên (edge cases) và rủi ro hồi quy (regression) chưa được xử lý.

Actor:
Peer reviewer trong nhóm đồ án môn học / Junior Developer.

Thời điểm / bối cảnh:
Mỗi khi thành viên trong nhóm tạo Pull Request yêu cầu merge code tính năng mới vào branch chính (develop/main).

Current workflow 3-7 bước:
1. Mở PR trên GitHub, đọc tiêu đề và mô tả task liên quan (3')
2. Mở tab Files Changed, đọc lướt cấu trúc thay đổi và danh sách file (7')
3. Đọc chi tiết từng dòng diff code, tự suy luận luồng dữ liệu và nhẩm tìm edge case (null check, type casting, exception, boundary value) (25')
4. Soạn thảo comment góp ý hoặc chỉ ra các trường hợp biên chưa được cover (10')
5. Đưa ra quyết định cuối: Approve, Request Changes hoặc Comment (2')

Bottleneck:
Bước 3 — Tự suy luận và lùng sục các edge case tiềm ẩn trong logic diff mà không có gợi ý hỗ trợ (mất 25 phút, gây mỏi mắt và rất dễ bỏ sót khi review lúc đêm muộn).

Impact:
3-4 PR/tuần, tốn ~150-180 phút/tuần; tuần trước có 2 lỗi crash lọt vào nhánh chính làm hỏng môi trường demo do reviewer bỏ sót trường hợp null input.

Success metric:
Giảm thời gian review từ 47 phút xuống dưới 20 phút/PR; tăng tỷ lệ phát hiện edge case trước khi merge từ 50% lên 85%; 0 lỗi crash nghiêm trọng lọt vào main branch.

Non-AI alternative:
Sử dụng Linter (Flake8, ESLint) và Báo cáo Coverage Unit Test. Linter chỉ bắt lỗi cú pháp/style; Unit test do dev tự viết nên thường chỉ bao quát happy path, không phát hiện được edge case bị bỏ sót.

AI hypothesis:
GitHub Action đọc git diff và commit message -> AI đối chiếu với mẫu lỗi phổ biến để sinh danh sách 3-5 câu hỏi kiểm tra edge case cụ thể dưới dạng draft comment -> Reviewer chỉ cần tích chọn kiểm tra và ra quyết định.

Quick gut:
[ ] No AI / process fix
[ ] Rule
[x] Workflow
[ ] Agent
[ ] Chưa biết
```

**Draft workflow Card #2:**

```text
CURRENT STATE — 47 phút

[1 Đọc PR summary: 3'] 
→ [2 Xem file diff: 7'] 
→ [3 Đọc code & tự nhẩm tìm edge cases: 25']  <-- bottleneck
→ [4 Viết comment góp ý: 10'] 
→ [5 Chốt Approve/Request change: 2']

FUTURE STATE — 18 phút

[1 GitHub Action trigger khi tạo PR: 1']  -- Rule
→ [2 AI phân tích diff & sinh checklist 3-5 edge cases: 2']  -- AI Workflow step
→ [3 Reviewer đọc code đối chiếu với checklist gợi ý: 12']  <-- human boundary
→ [4 Reviewer chọn/sửa comment và chốt Approve: 3']

Fallback: nếu checklist AI gợi ý chung chung hoặc sai lệch, reviewer bỏ qua checklist và tự review thủ công như quy trình truyền thống.
```

File đính kèm: `01-individual-problem-scan-workflow-card-2.png`

---

#### Problem Card #3 — Kiểm tra tự động checklist định dạng và tính đầy đủ của bài nộp lab/đồ án theo rubric

```text
Problem 1 câu:
Học viên mất 25-30 phút trước mỗi hạn nộp bài để dò soát thủ công từng tiêu chí trong file rubric môn học (đủ file, đúng tên, đúng cấu trúc repo, không bỏ sót placeholder trống trong markdown).

Actor:
Học viên khóa học AI/CNTT (Vũ Huy Độ) và các thành viên chịu trách nhiệm nộp bài trong nhóm.

Thời điểm / bối cảnh:
1-2 tiếng trước hạn chót (deadline) nộp bài tập lab hàng tuần hoặc đồ án môn học lên GitHub / LMS.

Current workflow 3-7 bước:
1. Mở file README / Worksheet chứa rubric và checklist chấm điểm môn học (3')
2. Mở cây thư mục bài làm trên VS Code, đối chiếu tên folder và tên file theo quy định (5')
3. Mở từng file report (.md) kiểm tra thủ công xem có sót ô trống, placeholder ("...", "___") hoặc thiếu bảng không (12')
4. Chạy script test / linter nếu có để kiểm tra lỗi cú pháp (3')
5. Soát lại lần cuối danh sách checklist tự kiểm (3')
6. Git add, commit, push và dán link repo vào hệ thống nộp bài (2')

Bottleneck:
Bước 3 — Mở từng file markdown đọc lướt dò thủ công từng phần để tìm xem có sót placeholder hoặc thiếu mục bắt buộc hay không (mất 12 phút, rất dễ hoa mắt sót lỗi khi sát giờ nộp).

Impact:
2 lần/tuần, mất gần 60 phút/tuần; tuần trước có 3 học viên trong lớp bị trừ 10-15% điểm vì nộp thiếu file ảnh workflow và để trống 1 bảng khảo sát.

Success metric:
Giảm thời gian kiểm tra từ 28 phút xuống dưới 5 phút/lần nộp; phát hiện 100% các lỗi thiếu trường bắt buộc hoặc tên file sai quy cách trước khi push git; 0% rủi ro bị trừ điểm format.

Non-AI alternative:
Viết script Python/Bash kiểm tra file tồn tại và dùng regex tìm chuỗi trống. Tuy nhiên regex khó đánh giá được chất lượng nội dung (ví dụ câu trả lời quá ngắn dưới 10 từ hoặc trả lời lệch câu hỏi).

AI hypothesis:
Script kiểm tra cây thư mục và tên file (Rule) + LLM đọc lướt nội dung các file .md đối chiếu với rubric để phát hiện các mục bị bỏ trống hoặc trả lời hời hợt -> Xuất báo cáo kiểm tra (Pre-flight checklist) trước khi nộp.

Quick gut:
[ ] No AI / process fix
[ ] Rule
[x] Workflow
[ ] Agent
[ ] Chưa biết
```

**Draft workflow Card #3:**

```text
CURRENT STATE — 28 phút

[1 Đọc rubric môn học: 3'] 
→ [2 Dò tên file & folder: 5'] 
→ [3 Dò soát nội dung từng file .md tìm mục sót: 12']  <-- bottleneck
→ [4 Chạy script test: 3'] 
→ [5 Soát checklist tổng thể: 3'] 
→ [6 Git commit & nộp: 2']

FUTURE STATE — 5 phút

[1 Chạy pre-submission verification script: 0.5']  -- Rule (check files/dirs)
→ [2 AI quét nội dung markdown & đối chiếu checklist rubric: 1']  -- AI Workflow step
→ [3 Học viên xem pre-flight report (các cảnh báo thiếu sót nếu có): 2']  <-- human boundary
→ [4 Bổ sung phần thiếu và bấm lệnh auto-commit/push: 1.5']

Fallback: nếu tool kiểm tra gặp lỗi runtime, học viên mở file checklist markdown tự rà soát thủ công như cũ.
```

File đính kèm: `01-individual-problem-scan-workflow-card-3.png`

---

### 2.3. Card muốn pitch nhất (chuẩn bị 2 phút)

**Card tôi muốn pitch nhất:**

```text
Card #1 — Tự động trích xuất và tạo Bug Report / GitHub Issue có cấu trúc từ Error Log và Traceback.
```

**Vì sao (2-3 câu: workflow gì, số đo gì, impact gì):**

```text
1. Workflow rõ ràng 5 bước: Đi từ raw terminal traceback → trích xuất root cause → draft reproduce steps → human review → GitHub Issue.
2. Số đo định lượng cụ thể: Giảm thời gian tạo bug issue từ 18 phút xuống dưới 4 phút/issue (tiết kiệm ~75% thời gian), 100% issue có đủ ngữ cảnh cần thiết.
3. Impact thiết thực: Giảm thiểu hơn 70% số tin nhắn trao đổi qua lại trên Discord giữa người phát hiện lỗi và người sửa lỗi, loại bỏ hoàn toàn các bug report vô nghĩa kiểu "code bị lỗi rồi".
```

**Câu hỏi tôi muốn nhóm challenge (1-2 câu hỏi đúng chỗ yếu):**

```text
1. Làm thế nào để đảm bảo an toàn dữ liệu, ngăn chặn việc vô tình gửi các thông tin nhạy cảm (API key, token xác thực, database credentials) từ log terminal sang LLM?
2. Trong trường hợp lỗi bắt nguồn từ logic nghiệp vụ phức tạp (chứ không chỉ là exception cú pháp), liệu bước suy luận reproduce steps của AI có nguy cơ bị ảo giác (hallucination) khiến dev sửa bug đi lạc hướng hay không?
```

**AI phản biện Card (nếu có):**
- Điểm yếu AI chỉ ra: AI cảnh báo rằng file log terminal thường chứa nhiều "rác" (warning không liên quan) hoặc token bảo mật, và nếu quá phụ thuộc vào AI để đoán reproduce steps thì có thể tạo ra các bước tái hiện không có thật trên thực tế.
- Tôi sửa gì: Thêm bước Rule Regex Sanitization ở đầu để lọc sạch credentials và warning thừa; đồng thời xác định rõ AI chỉ đóng vai trò "draft gợi ý bước tái hiện", người báo cáo lỗi (human reviewer) bắt buộc phải kiểm tra và xác nhận bước tái hiện trước khi issue được post lên GitHub.

### Self-check nộp phần 01
- [x] Có 5+ problems + top 3 Cards đủ field (đã hoàn thành 10 problems và 3 cards đầy đủ)
- [x] Mỗi Card có workflow trước/sau + bottleneck + metric + fallback
- [x] Đã chọn 1 card pitch + câu hỏi challenge
