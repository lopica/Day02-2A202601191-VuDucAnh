# 03 — Individual Reflection

## Đóng góp của Đức Anh trong nhóm

| Hoạt động | Đức Anh đã làm gì? | Kết quả / ảnh hưởng |
| --- | --- | --- |
| Scan cá nhân | Scan 10 problems; top 3 gồm Daily Report, Search material, Meeting management | Nhóm có candidate thuộc cluster **Học tập và tài nguyên giáo dục** (search/ôn tập) và góc nhìn về workflow lặp lại |
| Pitch Problem Card | Pitch **Daily Report** (#1) và **Search material** (#2) | Search material vào shortlist *Phân loại tài nguyên học tập* (score 29); Daily Report giúp nhóm thấy pattern "đọc → phân loại → chuyển tiếp" |
| Challenge | Hỏi các bài search/triển khai AI có **data access**, dữ liệu nhạy cảm và scope pilot trong lab không | Nhóm thống nhất thu hẹp scope, dùng dữ liệu ẩn danh/giả lập — áp dụng cả cho bài ngân hàng |
| Gom trùng / cluster | Góp ý Search material thuộc cluster tìm kiếm tài liệu; Daily Report thuộc pattern gom thông tin rời rạc | Khớp với 4 cluster nhóm gom: ngân hàng, số hóa, tìm kiếm tài liệu, học tập |
| Chọn candidate problem | Ban đầu ủng hộ bài gần gũi (Daily Report / tài nguyên học tập); sau thảo luận chấp nhận **Hỗ trợ ngân hàng** (score 32) | Nhóm chọn triage yêu cầu khách hàng tuyến đầu thay vì bài học tập |
| Validation / research | Tham gia soạn câu hỏi validation; đối chiếu pain "tìm từ ý tưởng mơ hồ" với pain "đọc yêu cầu tự do rồi phân loại queue" | Insight chung: bottleneck ở bước **đọc hiểu nội dung không chuẩn hóa**, không phải bước tiếp nhận |
| Workflow nhóm | Chia sẻ logic human review từ Daily Report (AI map → học viên kiểm tra trước commit) | Nhóm map sang future workflow: AI đề xuất intent/queue → **nhân viên review** trước khi route |
| Problem Statement | Góp ý boundary và metric — nhấn mạnh AI không tự gửi/nộp thay người, cần đo tỷ lệ chấp nhận output | PS v1 có human boundary rõ; metric gồm route đúng queue và 0 case AI tự xử lý nghiệp vụ nhạy cảm |
| Rule / Workflow / Agent | Ủng hộ **Workflow + Rule**, không Agent: workflow tuyến tính, Rule cho case chắc chắn, AI chỉ đề xuất | Khớp quyết định nhóm: Rule fallback + AI phân loại + nhân viên quyết định cuối |
| Decision | Thống nhất **Not Yet cho production; Go cho pilot offline** — chưa có baseline/dữ liệu thật nên không tuyên bố đã chứng minh hiệu quả | Decision trung thực với các ô `[CẦN ĐIỀN]` trong validation |

## Bảng dùng AI trong reflection

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai/hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
| --- | --- | --- | --- | --- |
| Scan | Gợi ý thêm lăng kính và problem theo vai trò học viên | Nhắc thêm search tài liệu, ôn tập, spec mập mờ | Gợi ý vài ý quá rộng (ví dụ "AI tutor toàn khóa học") | Chỉ giữ problem có workflow và dấu hiệu thật tôi đã gặp |
| Problem Card | Nhờ AI phản biện metric và scope Search material / Daily Report | Gợi ý tỷ lệ khớp nội dung, thời gian tìm đúng nguồn | Metric chất lượng vẫn mơ hồ; Search dễ bị phóng thành "semantic search toàn LMS" | Thu scope; ghi rõ data access khó và cần human confirm |
| Workflow | Nhờ AI chuyển mô tả thành flow có thời gian từng bước | Nhanh khi liệt kê bước triage và đánh dấu bottleneck 2–4 | AI gộp bước "đọc" và "phân loại" thành một bước | Tách lại vì pain tách thành đọc hiểu vs chọn queue |
| Research | Tìm pattern routing/phân loại (Dynamics 365, AI Builder, Textract) | Gợi ý nhanh mô hình Rule + AI + human review trong CS ngân hàng | Đề xuất tích hợp enterprise stack như thể nhóm đã có license và data | Chỉ giữ link chính thức; pilot offline trên case giả lập |
| Problem Statement | Nhờ AI phản biện PS v0 — field nào còn mơ hồ | Chỉ ra baseline chưa đo, intent chưa liệt kê | AI đề xuất Agent tự xử lý case hoặc tự trả lời khách | Nhóm thu về triage không giao dịch + nhân viên xác nhận |
| Rule / Workflow / Agent | Hỏi phản biện: Rule có đủ cho intent cố định không? | Giúp so sánh 4 mức (No AI / Rule / Workflow / Agent) | Thiên về Agent vì domain "ngân hàng = AI mạnh" | Giữ Workflow; Rule cho keyword/form; Agent chưa chọn |
| Decision | Gợi ý tiêu chí Go / Not Yet / No-Go | Liệt kê câu hỏi kiểm tra baseline, data, owner | Gợi ý Go production sớm dù chưa phỏng vấn nhân viên CSKH | Chốt Not Yet production + Go pilot có kiểm soát |

## Reflection câu hỏi mở

- **Tôi học được gì khi nghe top 3 problems của các bạn khác?**  
  Nhóm có 12 candidates rải across 4 cluster: ngân hàng, số hóa báo cáo, tìm kiếm tài liệu, học tập. Nhiều bài có pain thật nhưng khác nhau ở **baseline, data access và rủi ro**. Bài ngân hàng thắng shortlist vì actor/workflow rõ và metric triage đo được — dù validation thật vẫn còn `[CẦN ĐIỀN]`.

- **Nhóm có lúc nào bị solution-first không?**  
  Có — lúc đầu có xu hướng nói "làm chatbot/agent hỗ trợ ngân hàng" trước khi thu hẹp vào **triage intent + queue**. Sau research (Dynamics 365, AI Builder), nhóm quay lại: pain là bước đọc/phân loại, không phải tự động hóa toàn bộ CSKH.

- **Tôi có thay đổi ý kiến sau khi bị challenge không?**  
  Có. Ban đầu muốn nhóm chọn bài gần gũi (Daily Report hoặc Phân loại tài nguyên học tập). Sau khi nhóm hỏi "impact đo thế nào, pilot với data gì, rủi ro nếu AI sai", tôi đồng ý **Hỗ trợ ngân hàng (triage)** phù hợp hơn cho bài nộp nhóm — insight từ Search material (đọc nội dung mơ hồ, tìm đúng "nguồn"/queue) vẫn áp dụng được.

- **Tôi đóng góp gì thật sự vào artifact cuối?**  
  Scan rộng, pitch 2 Problem Cards, challenge scope/data access, và logic **human boundary** (AI đề xuất → người xác nhận). Phần này được nhóm dùng trong future workflow và boundary PS v1.

- **Điều khó nhất khi viết Problem Statement là gì?**  
  Chuyển "mất thời gian triage, dễ chuyển sai queue" thành metric có baseline thật (6 phút → ≤4,2 phút, ≥90% route đúng) trong khi nhóm **chưa phỏng vấn** nhân viên CSKH — phải ghi rõ giả định và `[CẦN ĐIỀN]`, không bịa số.

## Bài học của Đức Anh

- Problem tốt không phải problem nghe "AI" nhất, mà là problem có **actor, workflow, bottleneck, metric và boundary** rõ — kể cả domain nhạy cảm như ngân hàng.
- **Thu hẹp candidate** quan trọng hơn chọn tên bài hay: "hỗ trợ ngân hàng" → triage intent/queue không giao dịch.
- Vẽ workflow giúp thấy **Rule đủ ở đâu** (keyword, form), **AI hỗ trợ ở đâu** (câu tự do, file đính kèm), và **bắt buộc có người review** trước route/phản hồi.
- **Agent không phải đích đến mặc định.** Workflow + Rule hợp lý hơn khi cần audit, giới hạn permission và pilot offline.
- Pain Search material (ý tưởng mơ hồ → tìm đúng nguồn) và pain triage ngân hàng (yêu cầu tự do → chọn đúng queue) **cùng pattern**: đọc hiểu nội dung không chuẩn hóa là bottleneck.
- **Not Yet + Go pilot** là kết luận tốt khi chưa có baseline/dữ liệu — trung thực hơn Go sớm chỉ vì bài nghe "AI Product".

Nếu làm lại:

```text
Tôi sẽ chuẩn bị sẵn baseline cho bài mình pitch (log thời gian daily report hoặc search tài liệu) trước phase hội tụ, để tranh luận với bài ngân hàng dựa trên bằng chứng chứ không chỉ "gần gũi".

Tôi cũng sẽ chủ động hơn ở validation: hỏi sớm 2–3 người có kinh nghiệm CSKH/vận hành ngân hàng để thay [CẦN ĐIỀN] bằng số liệu thật trước khi nộp.
```

## Tự kiểm cuối bài

- [x] [12đ cá nhân] Cá nhân có 5+ problems và top 3 Problem Cards.
- [x] [12đ cá nhân] Tôi đã pitch rõ và challenge nhóm đúng trọng tâm.
- [x] Nhóm có nhật ký hội tụ từ 12 candidates về 1 bài (hỗ trợ ngân hàng — triage).
- [x] [15đ nhóm] Nhóm có workflow trước/sau (current 6 phút triage → future 2–3 phút xác định queue).
- [x] [20đ nhóm] Nhóm có Problem Statement v0/v1 với metric và boundary rõ.
- [x] [15đ nhóm] Nhóm có so sánh No AI / Rule / Workflow / Agent.
- [x] [10đ nhóm] Nhóm có Not Yet (production) + Go (pilot offline) và lý do rõ.
- [x] [10đ cá nhân] Reflection cá nhân có nói rõ vai trò trong nhóm, cách dùng AI, điều học được và nếu làm lại sẽ đổi gì.
- [x] [6đ cá nhân] Tôi tự giải thích được mạch problem → workflow → metric → boundary → độ phù hợp với AI.

---

*Day 02 Lab v2 — Individual Reflection — Vũ Đức Anh (2A202601191)*
