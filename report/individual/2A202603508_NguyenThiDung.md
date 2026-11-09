# Báo cáo cá nhân — MSSV_HoTen

## 1. Thông tin học viên

- Họ tên: Nguyễn Thị Dung 
- MSSV: 2A202603508
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: NhanToBiAn
- Link repo nhóm: https://github.com/b-baocode/K5-L3A-Day02-NhanToBiAn-DiscoveryProblemFraming

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Lặp lại | Khi tiếp nhận một tập dữ liệu ảnh y khoa phục vụ nghiên cứu hoặc phát triển mô hình, tôi muốn kiểm tra được ảnh, metadata và kết luận chuyên môn tương ứng (label) có đầy đủ và khớp nhau, để dữ liệu đầu vào đủ tin cậy cho các bước phân tích tiếp theo. | AI Engineer, nhóm dữ liệu hoặc chuyên gia gán nhãn | Chưa có số liệu để xác định số lượng bộ dữ liệu hoặc lỗi mỗi tuần và thời gian xử lý; cần thống kê trên thực tế. |
| 2 | Tốn thời gian | Khi cần tìm hiểu một chủ đề nghiên cứu mới về phân tích ảnh y khoa hoặc phương pháp AI, tôi muốn nhanh chóng xác định các bài báo, phương pháp, dữ liệu và kết quả có liên quan, để có cơ sở lựa chọn hướng thử nghiệm mà không phải đọc tràn lan nhiều tài liệu. | AI Engineer, researcher, nhóm VRIC | Chưa có nhật ký thời gian đọc tìm kiếm; cần ghi thời gian cho 3–5 lần tìm literature review để có baseline. Với tần suất là mỗi lần có đề tài mới hay rà soát lại đề tài của mình đều phải tìm kiếm và đọc bài báo khoa học liên quan.|
| 3 | Cần đọc, tổng hợp nhiều thông tin | Khi phải so sánh nhiều bài báo hoặc phương pháp trên cùng một bài toán, tôi muốn đối chiếu được mục tiêu, dữ liệu, cách đánh giá, giới hạn và kết quả của từng nghiên cứu, để tránh kết luận dựa trên abstract hoặc một vài chỉ số riêng lẻ. | AI Engineer, researcher | Chưa đo số paper/lần và số giờ/tổng hợp; cần ghi lại ở lần review kế tiếp. |
| 4 | Lặp lại | Khi phát triển hoặc chạy lại một pipeline phân tích dữ liệu, tôi muốn biết chính xác đầu vào, tham số, phiên bản công cụ và trạng thái từng bước, để có thể tái lập kết quả và khoanh vùng lỗi khi pipeline thất bại. | AI Engineer, researcher, người duy trì pipeline | Trước đây tôi có công việc với workflow phân tích như BinDel/WISECONDORX và xử lý code có nhu cầu ghi lại các tham số trong mỗi lần chạy . Dấu hiệu cần ghi nhận là số lần chạy lại, lỗi phát sinh và thời gian tìm nguyên nhân.|
| 5 | Pain từ người khác | Khi bác sĩ cần xem xét một lượng lớn ảnh X-quang/MRI, tôi muốn hiển thị các gợi ý, hỗ trợ quy trình đọc ảnh mà không thay thế quyết định chuyên môn của bác sĩ. | Bác sĩ chẩn đoán hình ảnh, kỹ thuật viên, bệnh nhân | Các chỉ số cần lấy từ đơn vị vận hành: số ca/bác sĩ/ca, thời gian trả kết quả (TAT), tỷ lệ ca tồn đọng và thời gian đọc mỗi ca.|
| 6 | Cần đọc, tổng hợp nhiều thông tin | Khi cần hiểu một yêu cầu kỹ thuật được mô tả qua tài liệu, issue, code, github và trao đổi rời rạc, tôi muốn gom được bối cảnh, mục tiêu, ràng buộc và tiêu chí hoàn thành, để triển khai đúng yêu cầu và hạn chế phải hỏi lại nhiều lần. | AI Engineer, người giao việc, reviewer | Đây là tình huống khi tôi đọc nhiều file trong github trong 30 phút mà chưa có cái nhìn tổng quát về vấn đề. |
| 7 | Tốn thời gian | Khi cần chuẩn bị báo cáo kỹ thuật hoặc cập nhật tiến độ, tôi muốn tập hợp được các kết quả thử nghiệm, các thay đổi code và các vấn đề còn tồn tại theo một cấu trúc thống nhất, để người đọc nắm được tiến độ và quyết định bước tiếp theo. | AI Engineer, tech lead, nhóm dự án | Công việc báo cáo kỹ thuật gắn với các deliverable và workflow đã thực hiện, thời gian tổng hợp thường 1 giờ. |
| 8 | Pain từ người khác | Khi một thành viên khác cần chạy lại hoặc review kết quả phân tích, tôi muốn hướng dẫn chạy, cấu hình và kết quả trung gian được ghi rõ, để họ không phụ thuộc vào việc hỏi trực tiếp người viết pipeline. | Thành viên nhóm, reviewer, người tiếp nhận bàn giao | Có thể kiểm tra bằng số câu hỏi hỗ trợ sau bàn giao, số lỗi do thiếu hướng dẫn và thời gian người mới chạy thành công.|

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

-AI được dùng sau khi hỗ trợ tổng hợp các bối cảnh công việc đã xuất hiện trong trao đổi trước đây để sắp xếp thành các nhóm problem và viết Job Story. 


---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Hỗ trợ bác sĩ ưu tiên xem xét ảnh y khoa có dấu hiệu bất thường tại Vinmec | Actor rõ; workflow từ tiếp nhận ảnh đến đọc và trả kết quả có thể vẽ; bottleneck giả thuyết nằm ở khâu bác sĩ xem xét từng ca; có thể đo thời gian đọc/TAT và tỷ lệ ca cần ưu tiên. Phù hợp định hướng AI hỗ trợ phát hiện dấu hiệu bất thường, không tự chẩn đoán. | Chưa có baseline số ca/bác sĩ/ca, thời gian đọc, TAT, tỷ lệ cảnh báo sai/bỏ sót; cần phỏng vấn bác sĩ và xác minh quyền truy cập dữ liệu. |
| 2 | Tìm kiếm, đọc và tổng hợp tài liệu nghiên cứu cho nhóm VRIC | Actor là researcher/AI Engineer; quy trình literature review có đầu vào và đầu ra rõ; pain nằm ở việc tìm đúng paper rồi đối chiếu phương pháp, dữ liệu và giới hạn; có thể đo thời gian tìm và tổng hợp một chủ đề. | Chưa biết tần suất review, số paper mỗi chủ đề, nguồn tài liệu được phép truy cập và tiêu chí đánh giá một bản tổng hợp đủ tin cậy. |
| 3 | Kiểm tra tính đầy đủ và nhất quán của bộ dữ liệu ảnh y khoa ghép với kết luận chuyên môn | Liên quan trực tiếp đến chất lượng dữ liệu trước huấn luyện/đánh giá; quy trình có các bước kiểm tra được; lỗi thiếu cặp ảnh–kết luận hoặc sai metadata có thể làm giảm độ tin cậy của dữ liệu. | Chưa có thống kê tỷ lệ lỗi, quy mô batch, thời gian kiểm tra thủ công và quy trình xử lý bất đồng giữa người gán nhãn/chuyên gia. |

### Problem Card #1 — Hỗ trợ bác sĩ ưu tiên xem xét ảnh y khoa

| Trường | Nội dung |
|---|---|
| Job Story | Khi phải đọc một lượng lớn ảnh X-quang/MRI trong ca làm việc, bác sĩ chẩn đoán hình ảnh muốn nhận biết những ca hoặc vùng ảnh có dấu hiệu bất thường cần chú ý, để ưu tiên xem xét và đưa ra kết luận chuyên môn kịp thời. |
| Actor | Bác sĩ chẩn đoán hình ảnh là người sử dụng và ra quyết định cuối cùng; kỹ thuật viên thực hiện chụp và chuyển ảnh; AI Engineer/nhóm kỹ thuật hỗ trợ xây dựng, kiểm thử công cụ. |
| Thời điểm / bối cảnh | Sau khi bệnh nhân được chỉ định chụp và ảnh được lưu vào hệ thống PACS, trong giai đoạn bác sĩ tiếp nhận và đọc ảnh. Cần xác minh cụ thể theo modality (X-quang hay MRI) và quy trình tại cơ sở. |
| Quy trình hiện tại (3–7 bước) | 1. Bác sĩ tiếp nhận danh sách ca và chỉ định (ước lượng 2–5 phút/ca). 2. Mở ảnh trên PACS và kiểm tra thông tin ca (ước lượng 1–3 phút). 3. Quan sát các ảnh/series và đối chiếu vùng giải phẫu (ước lượng 5–15 phút, tùy modality và độ phức tạp). 4. Đối chiếu tiền sử/thông tin lâm sàng nếu có (ước lượng 1–3 phút). 5. Ghi nhận phát hiện và soạn kết quả (ước lượng 2–5 phút). 6. Hoàn tất, ký và trả kết quả (ước lượng 1–2 phút). **Toàn bộ thời gian là giả thuyết ban đầu, không phải số đo tại Vinmec.** |
| Bottleneck (bước nào, mất bao nhiêu phút) | Giả thuyết bottleneck: bước 3 — bác sĩ quan sát và rà soát ảnh/series để tìm dấu hiệu cần chú ý. Thời gian giả định 5–15 phút/ca; cần đo theo modality, độ khó ca và kinh nghiệm bác sĩ. Không mặc định mọi ca đều bị nghẽn ở bước này. |
| Impact (nếu không giải thì sao) | Ca có dấu hiệu bất thường có thể không được ưu tiên xem xét sớm trong bối cảnh khối lượng ảnh lớn; thời gian trả kết quả có thể kéo dài. Đây là rủi ro cần kiểm chứng, không khẳng định đã xảy ra tại Vinmec. |
| Success metric (baseline → target) | **Metric đề xuất:** thời gian từ lúc ảnh sẵn sàng trên PACS đến lúc bác sĩ mở/đọc ca; tỷ lệ ca ưu tiên được bác sĩ xác nhận; độ nhạy và tỷ lệ cảnh báo giả của hệ thống trên tập kiểm thử có nhãn chuyên gia. **Baseline:** chưa có, cần trích log PACS/worklist và đo theo modality. **Target pilot đề xuất:** giảm 10–20% thời gian xác định ca cần ưu tiên mà không làm tăng tỷ lệ bỏ sót tổn thương quan trọng; phải được bác sĩ và đơn vị chuyên môn duyệt trước khi đặt làm KPI chính thức. |
| Phương án không dùng AI | Tối ưu worklist theo quy tắc nghiệp vụ đã được bệnh viện phê duyệt (mức độ khẩn, loại chỉ định, thời điểm tiếp nhận); chuẩn hóa protocol đọc ảnh và checklist; phân luồng ca theo quy trình hiện có. |
| Giả thuyết về AI (nếu có) | Mô hình computer vision có thể đánh dấu vùng/ca nghi ngờ để bác sĩ xem xét trước. Đầu ra chỉ là tín hiệu hỗ trợ, cần được đánh giá theo từng loại ảnh và từng dấu hiệu cụ thể; không đưa ra chẩn đoán độc lập. |
| Cảm nhận nhanh | Workflow có bước AI hỗ trợ phân tích ảnh + bác sĩ kiểm tra (HITL). Chưa đủ bằng chứng để kết luận cần Agent; ưu tiên đánh giá No AI/Rule trước. |

Quy trình nháp hiện tại:

```text
BÁC SĨ ĐỌC ẢNH — QUY TRÌNH GIẢ THUYẾT, CẦN ĐO THỰC TẾ

[1. Tiếp nhận worklist / chỉ định: 2–5']
        |
[2. Mở ảnh trên PACS, kiểm tra thông tin ca: 1–3']
        |
[3. Quan sát ảnh/series, tìm dấu hiệu bất thường: 5–15']
        |  <-- BOTTLENECK GIẢ THUYẾT
[4. Đối chiếu thông tin lâm sàng: 1–3']
        |
[5. Ghi nhận phát hiện, soạn kết quả: 2–5']
        |
[6. Kiểm tra, ký và trả kết quả: 1–2']

Boundary: bác sĩ đọc ảnh, xác nhận phát hiện và chịu trách nhiệm kết luận.
AI (nếu thử nghiệm) chỉ đánh dấu vùng/ca nghi ngờ; không tự kết luận,
không tự ký và không tự trả kết quả.
```

### Problem Card #2 — Tìm kiếm và tổng hợp tài liệu nghiên cứu cho VRIC

| Trường | Nội dung |
|---|---|
| Job Story | Khi bắt đầu nghiên cứu một chủ đề hoặc cần lựa chọn phương pháp cho một thử nghiệm, tôi muốn tìm và đối chiếu được các nghiên cứu liên quan, để lựa chọn hướng tiếp cận dựa trên bằng chứng thay vì đọc rời rạc từng tài liệu. |
| Actor | AI Engineer/researcher tại VRIC; người hướng dẫn hoặc technical lead là người sử dụng kết quả tổng hợp để thảo luận hướng nghiên cứu. |
| Thời điểm / bối cảnh | Khi bắt đầu một research question, chuẩn bị đề xuất phương pháp, hoặc cần cập nhật related work trước thử nghiệm. |
| Quy trình hiện tại (3–7 bước) | 1. Xác định từ khóa và câu hỏi nghiên cứu (ước lượng 10–20 phút). 2. Tìm paper trên các nguồn học thuật (ước lượng 20–40 phút). 3. Lọc tiêu đề/abstract để chọn tài liệu liên quan (ước lượng 20–30 phút). 4. Đọc methodology, dataset và evaluation của các paper đã chọn (ước lượng 30–60 phút/paper). 5. Ghi chú và đối chiếu ưu/nhược điểm (ước lượng 30–60 phút). 6. Tổng hợp thành nhận định và danh sách tài liệu tham khảo (ước lượng 30–60 phút). **Thời gian phụ thuộc số paper; cần log một phiên review thực tế để xác lập baseline.** |
| Bottleneck (bước nào, mất bao nhiêu phút) | Giả thuyết bottleneck: bước 4–5 — đọc sâu và đối chiếu thông tin nằm ở nhiều phần của nhiều paper. Ước lượng ban đầu 30–60 phút/paper cho đọc sâu, chưa được đo. |
| Impact (nếu không giải thì sao) | Mất thời gian để tìm lại thông tin; có nguy cơ bỏ sót nghiên cứu liên quan hoặc so sánh sai do chỉ dựa trên abstract/metric không cùng điều kiện. |
| Success metric (baseline → target) | **Metric đề xuất:** thời gian để tạo bảng tổng hợp cho một research question; tỷ lệ claim trong bảng có trích dẫn đúng đến paper/section; số lỗi trích dẫn hoặc thông tin không được nguồn hỗ trợ. **Baseline:** cần ghi thời gian cho 3 chủ đề gần nhất. **Target pilot đề xuất:** giảm 30% thời gian tạo bảng tổng hợp, đồng thời 100% claim quan trọng có nguồn đối chiếu được và không tăng lỗi factual. |
| Phương án không dùng AI | Dùng protocol literature review, bộ từ khóa chuẩn, citation manager, spreadsheet extraction template và checklist đánh giá chất lượng paper. |
| Giả thuyết về AI (nếu có) | Công cụ tìm kiếm ngữ nghĩa/RAG có thể hỗ trợ truy xuất đoạn liên quan, trích xuất trường thông tin và tạo bản nháp so sánh. Người nghiên cứu phải mở paper gốc để xác minh claim, số liệu và citation. |
| Cảm nhận nhanh | Workflow có retrieval và hỗ trợ tổng hợp; không cần Agent tự quyết định kết luận nghiên cứu. |

Quy trình nháp hiện tại:

```text
LITERATURE REVIEW — QUY TRÌNH GIẢ THUYẾT

[1. Xác định research question / keywords: 10–20']
        |
[2. Tìm paper từ nguồn học thuật: 20–40']
        |
[3. Lọc title / abstract: 20–30']
        |
[4. Đọc sâu methodology, dataset, evaluation: 30–60'/paper]
        |  <-- BOTTLENECK GIẢ THUYẾT
[5. Đối chiếu các paper, ghi chú: 30–60']
        |
[6. Tổng hợp nhận định và references: 30–60']

Boundary: researcher xác minh paper gốc, số liệu, phương pháp và kết luận.
Không dùng nội dung không có citation kiểm tra được.
```

### Problem Card #3 — Kiểm tra dữ liệu ảnh y khoa ghép với kết luận chuyên môn

| Trường | Nội dung |
|---|---|
| Job Story | Khi chuẩn bị dữ liệu ảnh y khoa cho nghiên cứu hoặc huấn luyện/đánh giá mô hình, tôi muốn xác định các bản ghi thiếu ảnh, thiếu kết luận, sai liên kết hoặc metadata không nhất quán, để chỉ đưa dữ liệu đã được kiểm tra vào pipeline. |
| Actor | AI Engineer/data engineer phụ trách chuẩn bị dữ liệu; bác sĩ/chuyên gia gán nhãn xác nhận nội dung chuyên môn; data manager quản lý quyền truy cập và nguồn dữ liệu. |
| Thời điểm / bối cảnh | Sau khi nhận batch ảnh và báo cáo/kết luận từ nguồn được cấp quyền, trước bước annotation, chia tập dữ liệu và huấn luyện/đánh giá mô hình. |
| Quy trình hiện tại (3–7 bước) | 1. Nhận batch ảnh và file metadata (ước lượng 10–20 phút/batch). 2. Kiểm tra cấu trúc thư mục, định dạng và khả năng đọc ảnh (ước lượng 15–30 phút). 3. Đối chiếu mã ca/ID ảnh với kết luận chuyên môn (ước lượng 30–60 phút). 4. Kiểm tra trường metadata bắt buộc và giá trị bất thường (ước lượng 15–30 phút). 5. Đưa bản ghi lỗi vào danh sách cần làm rõ (ước lượng 10–20 phút). 6. Nhờ người có chuyên môn xác nhận các trường hợp không rõ ràng và cập nhật trạng thái (thời gian chờ chưa xác định). **Các con số chỉ là ước lượng khởi tạo; cần đo theo kích thước batch và cấu trúc dữ liệu thực tế.** |
| Bottleneck (bước nào, mất bao nhiêu phút) | Giả thuyết bottleneck: bước 3 — ghép đúng ảnh với kết luận chuyên môn và xử lý trường hợp không khớp. Ước lượng 30–60 phút/batch; cần đo trên batch thực tế. |
| Impact (nếu không giải thì sao) | Dữ liệu sai cặp hoặc thiếu nhãn có thể làm nhiễu quá trình huấn luyện/đánh giá, gây sai lệch kết quả và tốn công rà soát lại. |
| Success metric (baseline → target) | **Metric đề xuất:** tỷ lệ bản ghi hợp lệ sau kiểm tra; tỷ lệ lỗi liên kết được phát hiện trước khi vào pipeline; thời gian kiểm tra mỗi 100 bản ghi; tỷ lệ trường hợp bị đánh dấu nhầm. **Baseline:** chưa có, cần audit một batch đại diện và ghi số bản ghi/lỗi/thời gian. **Target pilot đề xuất:** phát hiện 100% lỗi cấu trúc và lỗi thiếu trường bắt buộc trong bộ test đã gán lỗi; giảm 30% thời gian kiểm tra thủ công mà không tự động chấp nhận các cặp ảnh–kết luận còn mơ hồ. |
| Phương án không dùng AI | Schema validation, checksum/file integrity, quy tắc kiểm tra metadata, đối chiếu ID bằng script và hàng đợi review thủ công cho bản ghi không khớp. |
| Giả thuyết về AI (nếu có) | AI có thể hỗ trợ phát hiện bất thường trong metadata hoặc gợi ý nhóm bản ghi cần rà soát; việc ghép cặp ảnh–kết luận và xác nhận nhãn chuyên môn phải dựa trên ID/nguồn có kiểm soát và người có thẩm quyền. Không dùng LLM để tự suy diễn chẩn đoán thay bác sĩ. |
| Cảm nhận nhanh | Rule trước, Workflow nếu cần điều phối review; chưa có lý do chọn Agent. |

Quy trình nháp hiện tại:

```text
DATA PREPARATION — QUY TRÌNH GIẢ THUYẾT

[1. Nhận batch ảnh + metadata: 10–20']
        |
[2. Kiểm tra file, định dạng, cấu trúc: 15–30']
        |
[3. Ghép ID ảnh với kết luận chuyên môn: 30–60']
        |  <-- BOTTLENECK GIẢ THUYẾT
[4. Kiểm tra metadata bắt buộc / bất thường: 15–30']
        |
[5. Tạo danh sách bản ghi lỗi, cần xác minh: 10–20']
        |
[6. Chuyên gia xác nhận trường hợp mơ hồ: chưa xác định]

Boundary: không tự suy diễn kết luận y khoa; không tự ghép các bản ghi
mơ hồ; mọi trường hợp không chắc chắn phải chuyển người có thẩm quyền.
```

### Card muốn pitch nhất

- **Card số:** 1 — Hỗ trợ bác sĩ ưu tiên xem xét ảnh y khoa.
- **Vì sao:** Bài toán có actor và workflow lâm sàng cụ thể; đầu ra có thể giới hạn ở việc đánh dấu vùng/ca nghi ngờ để bác sĩ kiểm tra, phù hợp nguyên tắc human-in-the-loop. Bài toán cũng có các metric vận hành và chất lượng chuyên môn có thể xác định sau khi tiếp cận đúng stakeholder và dữ liệu.
- **Câu hỏi muốn nhóm phản biện:** Bottleneck thực sự nằm ở khâu bác sĩ quan sát ảnh, ở việc ưu tiên worklist, hay ở bước trước đó như chất lượng ảnh và thông tin lâm sàng chưa đầy đủ? Nhóm cần loại bằng chứng nào từ bác sĩ/PACS để xác định đúng bottleneck trước khi đề xuất AI?

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Chưa có số liệu thực tế chứng minh bác sĩ đang quá tải hoặc thời gian đọc ảnh là bottleneck. | Đồng ý. | Không ghi “bác sĩ quá tải” như một sự thật. Chuyển thành giả thuyết cần xác minh bằng số ca/bác sĩ/ca, thời gian đọc và TAT. |
| “Phát hiện bất thường” còn quá rộng; mỗi modality và loại dấu hiệu có yêu cầu dữ liệu/đánh giá khác nhau. | Đồng ý. | Giới hạn card ở hỗ trợ ưu tiên xem xét; yêu cầu xác định modality và dấu hiệu cụ thể trước khi thử nghiệm. |
| Chỉ đo thời gian có thể khiến hệ thống nhanh hơn nhưng cảnh báo sai hoặc bỏ sót dấu hiệu quan trọng. | Đồng ý. | Bổ sung metric chất lượng như độ nhạy, tỷ lệ cảnh báo giả và yêu cầu đánh giá trên tập dữ liệu có nhãn chuyên gia; không để AI tự ra kết luận. |
| Có thể dùng Rule/worklist optimization thay vì AI cho một phần bài toán. | Đồng ý. | Bổ sung phương án không dùng AI và yêu cầu so sánh No AI/Rule trước khi quyết định Workflow. |
| Card #3 có thể là bottleneck nền tảng của Card #1: dữ liệu ảnh và kết luận không được ghép cặp/kiểm tra tốt thì mô hình không đáng tin. | Đồng ý. | Giữ Card #3 trong top 3 như một problem độc lập, đồng thời xem đây là dependency cần kiểm tra nếu nhóm chọn Card #1. |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | | |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: | |
| Nhận phản biện | Câu hỏi tôi nhận được: | Tôi đã sửa gì: |
| Gom cluster / cây OST | | |
| Chọn candidate problem | | |
| Kiểm chứng / research | | |
| Quy trình nhóm | | |
| Problem Statement | | |
| Mức can thiệp AI | | |
| Quyết định | | |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | | | | |
| CP2 Problem Card | | | | |
| CP4 Research | | | | |
| CP5 Quy trình | | | | |
| CP5–6 Problem Statement | | | | |
| CP6 Mức can thiệp / quyết định | | | | |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

**6.5. Điều khó nhất khi viết Problem Statement là gì?**

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.

---

## 7. Tài liệu tham khảo

-
