# 03 — Individual Reflection

> Viết bằng lời của bạn (Phase 7 trong `01-worksheet.md`). Có thể dùng AI gợi ý câu hỏi tự soi, không dùng AI viết thay. 8-12 câu, có chuyện cụ thể.

## Thông tin cá nhân

- Họ và tên: Vũ Huy Độ
- Mã học viên: 2A202602555
- Nhóm: Nhóm A2-05
- Candidate problem nhóm chọn: Tự động trích xuất và tạo Bug Report / GitHub Issue có cấu trúc từ Error Log và Traceback trong terminal.

---

## 1. Tôi đã tham gia vào phần nào?

Ghi việc cụ thể + kết quả cụ thể. Không ghi chung chung kiểu "tham gia thảo luận".

| Hoạt động | Tôi đã làm gì? (việc cụ thể) | Kết quả / ảnh hưởng tới nhóm |
|---|---|---|
| Scan cá nhân | Tự quét 10 problems từ trải nghiệm thực tế khi làm lab AI và thực tập phần mềm, phủ trọn 4 lăng kính và bấm giờ thực tế | Nhóm có nguồn đầu vào phong phú, chất lượng cao; đóng góp 3 bài vào danh sách 12 candidates chung của nhóm |
| Pitch Problem Card | Trình bày trực tiếp Card #1 về tạo issue từ traceback log trong 2 phút, nhấn mạnh số đo 18 phút → 4 phút | Thuyết phục cả nhóm đồng thuận chọn bài toán làm candidate duy nhất để đào sâu |
| Challenge bài của bạn khác | Đặt câu hỏi phản biện bài Discord FAQ của Trang về rủi ro phân quyền API và bài sinh Unit Test của Đức về rủi ro sinh test sai | Giúp nhóm tránh chọn những đề tài quá rộng hoặc khó kiểm soát chất lượng trong thời gian lab |
| Gom trùng / cluster | Đề xuất gom 12 bài toán thành 4 cụm theo vòng đời phát triển phần mềm (Debug/Issue, Code review, Tri thức/Q&A, Quản lý task) | Giúp nhóm có cái nhìn tổng quan, gom cụm logic và loại bỏ các ý tưởng trùng lặp nhanh chóng |
| Chọn candidate problem | Trực tiếp bảo vệ bài toán trước bảng chấm điểm 7 tiêu chí và giải trình các thắc mắc về tính khả thi | Nhóm đạt điểm đồng thuận cao nhất (34/35) cho bài Bug Report mà không cần biểu quyết cảm tính |
| Validation / research | Hỗ trợ Trang thiết kế câu hỏi mini poll trên Discord lớp và trích xuất dữ liệu từ 15 issue trên repo đồ án cũ của nhóm | Thu thập được dữ liệu định lượng và quote thực tế chứng minh pain point là có thật |
| Workflow nhóm | Trực tiếp phác thảo sơ đồ ASCII workflow trước/sau, tính toán thời gian từng bước và chỉ rõ Human Boundary | Giúp nhóm nhìn ra điểm nghẽn 8 phút ở khâu viết narrative và vị trí chính xác AI cần can thiệp |
| Problem Statement | Cùng Đức hoàn thiện PS v0 và v1, trực tiếp viết phần Boundary phân định rõ phạm vi làm và không làm | Ngăn chặn nguy cơ trượt scope sang việc tự sửa code (auto-fix) nguy hiểm |
| Rule / Workflow / Agent | Phân tích 5 câu hỏi chốt, chứng minh vì sao không cần Agent tự hành mà chỉ cần Workflow kết hợp Rule | Giúp nhóm tiết kiệm tài nguyên, tránh bẫy solution-first và kiểm soát được rủi ro |
| Decision | Thiết kế kế hoạch pilot nhỏ trên 10 file log runtime thực tế và đặt ra 3 chỉ số đo lường cụ thể | Cung cấp bằng chứng thực nghiệm vững chắc để nhóm tự tin đưa ra quyết định GO |

**Dấu tay rõ nhất của tôi trong artifact cuối (1-2 câu):**

```text
Dấu tay rõ nhất của tôi là việc đề xuất bài toán gốc, trực tiếp thiết kế toàn bộ sơ đồ Workflow trước/sau (xác lập Human Boundary tại khâu review issue) và đưa ra giải pháp Rule Regex Sanitization để loại bỏ rủi ro rò rỉ dữ liệu nhạy cảm.
```

---

## 2. Bảng dùng AI (mỗi dòng 1 phase có dùng AI — 2 cột cuối bắt buộc)

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai / hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| Scan | Mở rộng góc nhìn tìm thêm pain points từ các lăng kính khác nhau | Gợi ý góc nhìn phân tách giữa người tạo lỗi (tester) và người tiếp nhận fix lỗi | Đưa ra các ý tưởng giải pháp viển vông (AI tự viết toàn bộ đồ án, AI họp thay người) | Loại bỏ hoàn toàn các ý tưởng solution-first, chỉ giữ lại các điểm nghẽn quy trình thật có thể đo lường |
| Problem Card | Đóng vai skeptical PM phản biện điểm yếu của Card #1 | Cảnh báo log terminal chứa nhiều warning rác và nguy cơ hallucination ở bước reproduce steps | Nhận xét chung chung, không đưa ra được giải pháp kỹ thuật cụ thể | Tự bổ sung bước Rule Regex Sanitization ở đầu và thiết lập Human Boundary bắt buộc trước khi post issue |
| Workflow | Gợi ý cấu trúc phân rã thời gian cho từng bước trong flow | Cung cấp khung sơ đồ trước/sau mạch lạc, dễ hình dung | Đoán thời gian AI xử lý quá lạc quan (0.1s) và bỏ quên thời gian con người đọc review | Tự đo thời gian thực tế, nâng thời gian review của dev lên 2 phút để đảm bảo tính khả thi |
| Research | Tìm kiếm 2-3 giải pháp hoặc pattern tương tự trên thị trường | Gợi ý đúng các công cụ liên quan như Sentry, Copilot for Issues và Raygun | Đưa ra các con số thống kê thị phần mà không có nguồn hoặc link kiểm chứng | Tự tìm kiếm tài liệu chính thức từ trang chủ của từng công cụ, kiểm tra link và viết lại phần bài học cho nhóm |
| Problem Statement | Rà soát độ chặt chẽ của các trường trong bản v0 | Chỉ ra phần Boundary ban đầu còn mơ hồ về xử lý dữ liệu nhạy cảm | Viết lại câu chữ theo phong cách marketing hoa mỹ, dài dòng | Giữ nguyên ngôn ngữ kỹ thuật cô đọng, bổ sung chi tiết ranh giới 'Làm gì' và 'Không làm gì' |
| Rule / Workflow / Agent | Phản biện lựa chọn giữa Workflow và Agent | Cung cấp các câu hỏi kiểm tra tính cần thiết của việc gọi tool động | Ban đầu gợi ý làm Agent cho 'thông minh và tự động hóa toàn diện' | Kiên quyết giữ lựa chọn Workflow vì các bước đi theo đường thẳng và cần con người kiểm duyệt |
| Decision | Gợi ý tiêu chí cho vòng chạy thử nghiệm (pilot) | Gợi ý 3 chỉ số đo lường: thời gian, độ chính xác và độ an toàn lọc token | Đề xuất tập dữ liệu pilot quá lớn (hàng nghìn log) không phù hợp thời gian lab | Thu hẹp phạm vi pilot xuống 10 file log lỗi runtime thực tế từ bài lab Day 1 của chính nhóm |

> Nếu phase nào không dùng AI, ghi `Không dùng` và vì sao tự làm.

---

## 3. Reflection câu hỏi mở

Chọn 3-4 câu trong 6 câu dưới để viết thành đoạn 8-12 câu (không trả lời bullet 1 dòng):
- Tôi học được gì khi nghe top 3 problems của các bạn khác?
- Nhóm có lúc nào bị solution-first, đòi làm Agent cho ngầu không?
- Tôi có thay đổi ý kiến sau khi bị challenge không, vì sao đổi?
- Tôi đóng góp gì thật sự vào artifact cuối, phần nào có dấu tay của tôi?
- Điều khó nhất khi viết Problem Statement là gì, metric hay boundary?
- Nếu làm lại, tôi sẽ challenge nhóm mạnh hơn ở điểm nào?

**Reflection:**

```text
Trong quá trình thảo luận nhóm ở Phase 3, tôi nhận ra bài học lớn nhất là ranh giới mong manh giữa một "vấn đề thật" và một "ý tưởng nghe có vẻ ngầu". Ban đầu, thành viên Đức rất hào hứng muốn xây dựng một Autonomous Agent tự động đọc lỗi trong terminal, tự mở code ra debug và tự commit bản vá sửa lỗi. Tôi và Nam đã phải thẳng thắn kéo cả nhóm trở lại thực tế bằng câu hỏi: "Nếu AI sửa sai làm hỏng cả nhánh main trước giờ demo thì ai sẽ chịu trách nhiệm?". Chính cuộc tranh luận đó giúp nhóm nhận ra điểm nghẽn thực sự của chúng tôi không phải là việc sửa code, mà là sự lười biếng và tốn thời gian khi phải đọc cả trăm dòng traceback để viết lại thành reproduce steps có nghĩa. Tôi cũng thay đổi suy nghĩ của mình sau khi bị Đức challenge về rủi ro lộ API keys trong file log; thay vì chủ quan cho rằng dev sẽ tự xóa, tôi đã bổ sung ngay bước Rule Regex Sanitization vào quy trình. Điều khó nhất với tôi khi hoàn thiện Problem Statement không phải là metric thời gian mà chính là xác lập Boundary: kiên quyết giới hạn giải pháp ở khâu hỗ trợ tạo bản nháp issue trên máy local chứ không can thiệp sâu vào source code. Dấu tay rõ nhất của tôi trong sản phẩm cuối chính là việc định hình workflow bán tự động với một Human Boundary vững chắc, giúp bài toán vừa giải quyết triệt để nỗi đau hằng tuần vừa an toàn tuyệt đối. Nếu được làm lại từ đầu, tôi sẽ challenge nhóm sớm hơn ở khâu gom cụm để không mất thời gian tranh luận về những bài toán thuần Rule như format linter hay auto-commit.
```

---

## 4. Tự kiểm cuối bài (check trước khi nộp repo)

- [x] [12đ] Cá nhân có 5+ problems + top 3 Problem Cards
- [x] [12đ] Tôi đã pitch rõ + challenge nhóm đúng trọng tâm (ghi ở bảng mục 1)
- [x] Nhóm có nhật ký hội tụ từ candidates về 1 bài
- [x] [15đ] Nhóm có workflow trước/sau
- [x] [20đ] Nhóm có PS v0/v1 với metric + boundary rõ
- [x] [15đ] Nhóm có so sánh No AI / Rule / Workflow / Agent
- [x] [10đ] Nhóm có Go / Not Yet / No-Go + lý do rõ
- [x] [10đ] Reflection này có vai trò thật + AI giúp/sai ở đâu + điều học được + nếu làm lại đổi gì
- [x] [6đ] Tôi tự giải thích được mạch problem → workflow → metric → boundary → độ phù hợp AI
