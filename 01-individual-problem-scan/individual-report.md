# 01 — Individual Problem Scan

## Scan rộng

Đức Anh scan 10 problems, vượt mức tối thiểu 5.

| #   | Lăng kính          | Problem quan sát được                                                                              | Ai chịu ảnh hưởng?  | Dấu hiệu thật                |
| --- | ------------------ | -------------------------------------------------------------------------------------------------- | ------------------- | ---------------------------- |
| 1   | Lặp lại            | Mỗi khi có lịch họp thì mình lại phải dừng công việc lại để ghi chú lịch hẹn                       | người làm văn phòng | Mất khoảng 90 phút/tuần      |
| 2   | Tốn thời gian      | Mỗi khi có nhu cầu tìm việc, tôi lại cần chỉnh cv và đi tìm thông tin các cty hiện tại đang mở đơn | người tìm việc      | Lặp lại mỗi lần tìm việc mới |
| 3   | Tốn thời gian      | tôi cần đọc file readme, codelab để có thể hình dung quy trình làm bài lab                         | học viên            | 45 phút/bản                  |
| 4   | Lặp lại            | Viết daily và weekly trên discord, rồi viết lại trên repo                                          | học viên            | 30 phút/buổi                 |
| 5   | AI có thể tốt hơn  | Tìm kiếm lại nội dung bài học nhưng không nhớ slide nào bài nào mà chỉ ý tưởng                     | học viên member     | Có ý tưởng nhưng mơ hồ       |
| 6   | AI có thể tốt hơn  | Muốn tự ôn luyện phải tự tìm bài tập, hoặc thậm chí tự làm câu hỏi                                 | học viên            | 1 tiếng/lần tìm              |
| 7   | Pain từ người khác | Developer phải hỏi lại vì spec từ Brse mập mờ                                                      | Developer           | Hỏi lại 2-3 lần/spec         |
| 8   | Pain từ người khác | PM hỏi update nhưng report chưa sẵn                                                                | PM                  | Hay bị trễ deadline thứ Hai  |
| 9   | Tốn thời gian      | Game có meta mới lại phải học lại trang bị, ngọc, skill mới                                        | gamer               | Lặp lại mỗi lần meta đổi     |
| 10  | Lặp lại            | Uống cafe mỗi sáng cần tự pha                                                                      | người uống cafe     | 5-10 phút/ngày               |

## Top 3

| Rank | Problem            | Vì sao chọn                                     | Điều còn chưa chắc                    |
| ---- | ------------------ | ----------------------------------------------- | ------------------------------------- |
| 1    | Daily Report       | Workflow rõ, mất nhiều thời gian, có metric tốt | Narrative "đủ tốt" đo thế nào         |
| 2    | Search material    | Có pain thật, AI có thể giúp đọc/tóm tắt        | Data access khó, scope có thể quá lớn |
| 3    | Meeting management | Nhiều người đau, impact rộng                    | Action có thể làm bị hạn chế          |

## Problem Card #1 — Daily Report

Problem 1 câu:
Học viên AI thực chiến mỗi ngày phải viết daily trên Discord rồi viết lại trên repo cho mentor và Gate 2, tốn ~30 phút/buổi và dễ lệch nội dung giữa hai nơi.

Actor:
Học viên khóa AI Product Labs (mentor và reviewer Gate 2 là stakeholder nhận report).

Thời điểm / bối cảnh:
Cuối ngày học hoặc sáng hôm sau, trước deadline nộp daily/weekly và trước các mốc Gate 2 giữa khóa.

Current workflow 3-7 bước:

1. Làm lab / học trong ngày, ghi chú rời hoặc nhớ trong đầu
2. Viết daily trên Discord theo format mentor (việc làm, blocker, plan ngày mai)
3. Scroll lại Discord hoặc cố nhớ nội dung đã post
4. Mở repo, tìm đúng file và cấu trúc markdown daily report
5. Viết lại nội dung cho repo — chỉnh format, bổ sung field Gate 2 yêu cầu
6. Self-check: Discord và repo đã khớp chưa, đủ field chưa
7. Commit và push (hoặc nộp theo quy trình khóa)

Bottleneck:
Bước 3–5 — phải nhớ/tra lại Discord rồi viết lại lần hai; buổi sáng đang học nên hay trì hoãn, dẫn đến report repo bị trễ hoặc thiếu field.

Impact:
~30 phút/buổi × hầu hết ngày học trong tuần. Nội dung Discord và repo không thống nhất → mentor hỏi lại hoặc Gate 2 thiếu bằng chứng tiến độ. Trì hoãn buổi sáng làm report repo hay bị dồn cuối ngày.

Success metric:
Giảm tổng thời gian từ ~30 phút xuống dưới 10 phút/buổi; tỷ lệ nội dung khớp Discord ↔ repo ≥ 95%; tỷ lệ nộp daily repo đúng hạn ≥ 90%/tuần.

Non-AI alternative:
Copy nội dung Discord sang Notepad rồi paste vào repo — giảm phần "nhớ lại" nhưng vẫn phải format thủ công và dễ sót field Gate 2.

AI hypothesis:
Học viên viết daily trên Discord (hoặc dictation ngắn) → AI map sang code local markdown + checklist field Gate 2 → học viên review/edit rồi commit. AI không tự push thay học viên.

Quick gut:
[ ] No AI / process fix
[ ] Rule
[x] Workflow
[] Agent
[ ] Chưa biết

### Draft current workflow

```text
CURRENT STATE — ~30 phút/buổi

[1 Làm lab / học trong ngày: —]
→ [2 Viết daily Discord: 8']
→ [3 Nhớ / scroll lại Discord: 5']  <-- bottleneck
→ [4 Mở repo + tìm file: 3']
→ [5 Viết lại + format repo: 12']  <-- bottleneck
→ [6 Self-check + commit: 2']
```

### Draft future workflow

```text
FUTURE STATE — ~8 phút/buổi

[1 Viết daily trên Discord (nguồn chính): 8']
→ [2 AI chuyển sang code trên máy local: 1']
→ [3 Học viên review + sửa: 2']  <-- human boundary
→ [4 tự commit + push: 1']

Fallback: AI map sai field hoặc note chưa cụ thể → học viên sửa thủ công hoặc copy từ Discord như hiện tại.
```

## Problem Card #2 — Search material

Problem 1 câu:
Khi ôn tập hoặc làm lab, học viên nhớ ý tưởng/khái niệm nhưng không nhớ nằm ở đâu, nên mất nhiều thời gian tìm lại trong Vlearn, Codelab và tài liệu rời rạc trong discord.

Actor:
Học viên khóa AI thực chiến (và mentor khi cần trả lời câu hỏi lặp lại).

Thời điểm / bối cảnh:
Trước deadline lab, khi ôn lại bài cũ, hoặc khi có ý tưởng mơ hồ và cần tra cứu nguồn gốc trong slide/repo.

Current workflow 3-7 bước:

1. Nhớ một ý tưởng hoặc keyword mơ hồ (ví dụ: "workflow trước/sau", "Problem Card")
2. Mở lần lượt slide trong vlearn, codelab, Discord hỏi đáp
3. Ctrl+F hoặc scroll từng file vì không biết chính xác nằm ở đâu
4. Đọc qua nhiều đoạn không liên quan để xác nhận đúng/sai ngữ cảnh
5. (Nếu ôn tập) Tự tìm thêm bài tập hoặc tự nghĩ câu hỏi luyện tập
6. Ghi chú lại nguồn nếu tìm được — hoặc bỏ cuộc nếu quá lâu

Bottleneck:
Bước 3–4 — search theo keyword trong nhiều nguồn rời rạc; ý tưởng mơ hồ nên keyword search hay trượt hoặc trả về quá nhiều kết quả nhiễu.

Impact:
Mất khoảng 45–60 phút/lần khi cần ôn hoặc tra cứu sâu (#6 scan: ~1 tiếng/lần tìm bài tập). Học viên hay trì hoãn ôn tập vì "biết có nhưng không tìm ra". Mentor/Discord cũng bị hỏi lại cùng câu vì tài liệu khó tra.

Success metric:
Giảm thời gian tìm đúng nguồn từ ~45 phút xuống dưới 10 phút/lần; tỷ lệ tìm đúng slide/bài ngay lần đầu ≥ 80%.

Non-AI alternative:
Bookmark thủ công, index markdown trong repo, hoặc một Notion page tổng hợp link — giúp nếu ai đó duy trì thường xuyên, nhưng không giải quyết search theo ý tưởng mơ hồ.

AI hypothesis:
AI index semantic toàn bộ tài liệu khóa học; học viên hỏi bằng ngôn ngữ tự nhiên → AI trả về đoạn liên quan + link/slide cụ thể. Học viên vẫn đọc lại và xác nhận trước khi dùng.

Quick gut:
[ ] No AI / process fix
[ ] Rule
[x] Workflow
[ ] Agent
[ ] Chưa biết

### Draft current workflow

```text
CURRENT STATE — ~50 phút

[1 Nhớ ý tưởng mơ hồ: —]
→ [2 Mở README / worksheet / codelab: 5']
→ [3 Ctrl+F từng file: 15']  <-- bottleneck
→ [4 Đọc nhiều đoạn để lọc: 20']
→ [5 Tự tìm bài tập / câu hỏi: 10']
```

### Draft future workflow

```text
FUTURE STATE — ~12 phút

[1 Học viên mô tả ý tưởng bằng câu tự nhiên: 2']
→ [2 AI semantic search + trả snippet + nguồn: 1']
→ [3 Học viên đọc và xác nhận đúng ngữ cảnh: 7']  <-- human boundary
→ [4 (Tuỳ chọn) AI gợi ý 2-3 câu hỏi ôn tập: 2']

Fallback: AI trả sai nguồn → học viên search thủ công như hiện tại.
```

## Problem Card #3 — Meeting management

Problem 1 câu:
Mỗi khi có lịch họp mới, người làm văn phòng phải dừng việc đang làm để ghi chú lịch hẹn, đồng bộ thông tin và nhắc các bên liên quan — tốn khoảng 90 phút/tuần và hay gây gián đoạn công việc chính.

Actor:
Người làm văn phòng / admin phụ trách lịch họp và điều phối phòng họp.

Thời điểm / bối cảnh:
Khi email/chat thông báo lịch họp mới, đổi giờ, hoặc thêm người tham dự — thường xen giữa các task đang làm buổi sáng.

Current workflow 3-7 bước:

1. Nhận thông báo lịch họp qua email, Zalo hoặc chat nội bộ
2. Dừng công việc hiện tại để đọc và trích xuất: giờ, phòng, người tham dự, agenda
3. Mở Google Calendar / Outlook và tạo hoặc cập nhật event thủ công
4. Kiểm tra trùng lịch phòng hoặc trùng lịch key stakeholder
5. Ghi chú thêm context (ai book, cần chuẩn bị gì) vào mô tả event
6. Nhắn lại người liên quan xác nhận hoặc báo conflict
7. Quay lại công việc cũ — thường mất thêm vài phút để vào lại focus

Bottleneck:
Bước 2–3 — context switch + nhập liệu thủ công từ nguồn không chuẩn hóa (email/chat khác format nhau).

Impact:
~90 phút/tuần cho một người phụ trách; nhiều cuộc họp/ngày thì gián đoạn liên tục. Lịch cập nhật chậm → người tham dự miss meeting hoặc phòng bị double-book.

Success metric:
Giảm thời gian xử lý mỗi lịch họp từ ~15 phút xuống dưới 5 phút; giảm tổng thời gian/tuần từ 90 phút xuống dưới 30 phút; số lần conflict phòng/phải hỏi lại không tăng.

Non-AI alternative:
Form chuẩn đặt lịch (Google Form) + quy tắc "chỉ accept qua form" — giảm email rời, nhưng khó ép toàn bộ stakeholder và vẫn cần người review conflict.

AI hypothesis:
AI đọc email/chat invite → trích xuất structured fields → draft event trên calendar → người phụ trách review 1-click approve. Conflict check vẫn do rule/calendar, human confirm trước khi gửi invite.

Quick gut:
[ ] No AI / process fix
[ ] Rule
[x] Workflow
[ ] Agent
[ ] Chưa biết

### Draft current workflow

```text
CURRENT STATE — ~15 phút/lịch, ~90 phút/tuần

[1 Nhận thông báo lịch: 1']
→ [2 Dừng việc + đọc/trích info: 5']  <-- bottleneck (context switch)
→ [3 Nhập Calendar thủ công: 5']
→ [4 Check conflict + ghi chú: 3']
→ [5 Nhắn xác nhận: 1']
→ [6 Vào lại focus: 2–5' (ẩn)]
```

### Draft future workflow

```text
FUTURE STATE — ~5 phút/lịch

[1 Email/chat vào hàng đợi: auto]
→ [2 AI trích xuất giờ/phòng/người/agenda: 1']
→ [3 Rule check conflict phòng + lịch: 1']
→ [4 Admin review + approve 1-click: 2']  <-- human boundary
→ [5 Auto gửi invite + nhắc: 1']

Fallback: AI trích sai giờ/người → admin sửa thủ công trước khi gửi.
```

## Problem Cards #2 và #3 — tóm tắt

| Card               | Actor               | Bottleneck                          | Metric                      | Quick gut | Vì sao chưa chọn làm #1                |
| ------------------ | ------------------- | ----------------------------------- | --------------------------- | --------- | -------------------------------------- |
| Search material    | Học viên            | Tìm từ ý tưởng mơ hồ qua nhiều file | 45 phút → dưới 10 phút/lần  | Workflow  | Data access khó, scope có thể quá lớn  |
| Meeting management | Người làm văn phòng | Context switch + nhập lịch thủ công | 90 phút/tuần → dưới 30 phút | Workflow  | Phụ thuộc quy trình công ty, khó pilot |

---

Card tôi muốn pitch nhất:

```text
card 1
```

Vì sao:

```text
vấn đề gần gũi nhất, cụ thể, dễ đo lường
```
