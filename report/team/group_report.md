# Báo cáo nhóm — Day 02 Discovery & Problem Framing

> Bản chung của nhóm, viết trên repo do nhóm trưởng fork. Không copy file này sang repo cá nhân.
> Template chi tiết và prompt mẫu: [docs/01-worksheet.md](../../docs/01-worksheet.md). Bài mẫu: [docs/02-deliverable-example.md](../../docs/02-deliverable-example.md).

## 1. Thông tin nhóm

- Tên nhóm:
- Thành viên: xem `TEAM.md`
- Candidate problem được chọn (1 câu):
- Quyết định cuối: Go / Not Yet / No-Go

---

## 2. Hội tụ nhóm (CP3)

### 2.1. Pitch

| # | Người đưa ra | Candidate (Job Story ngắn) | Actor | Bottleneck | Câu hỏi phản biện nhận được (ai hỏi) |
|---:|---|---|---|---|---|
| 1 | Ngô Gia Bảo | Khi tới tối ngày lab mà bài chưa xong, muốn biết còn thiếu phần nào so với yêu cầu, để nộp đủ trước 23h59 | Học viên AI20K | Tự đối chiếu bài với rubric rồi quay lại sửa (~60', lặp 12 lần lưu, commit nộp 00:19) | |
| 2 | Ngô Gia Bảo | Khi chạy prototype gọi API bị lỗi, muốn biết lỗi do code mình hay do nhà cung cấp, để không sửa nhầm chỗ | Học viên làm lab có gọi API | Đoán nguyên nhân lỗi 404/503/504/ReadTimeout (~16' trên tổng ~30') | |
| 3 | Ngô Gia Bảo | Khi nhận đề lab nhiều file, muốn nắm nhanh phải nộp gì, đặt tên thế nào, lỗi nào bị trừ nặng, để không mất điểm oan | Học viên AI20K | Rút các quy định bị trừ điểm nằm rải rác ở 11 file/1.325 dòng (dễ bỏ sót, ví dụ tên repo `DAY02`) | |
| 4 | Nguyễn Văn Ba | Khi mở đề lab mới, cần biết ngay phải nộp file nào, điền mục nào, đặt tên ra sao, để bắt tay làm sau ~10' | Học viên K5 | Đối chiếu qua lại 6–7 file để biết phải nộp gì (~10' trên tổng ~35') | |
| 5 | Nguyễn Văn Ba | Khi đầu giờ quên mật khẩu/bị khóa tài khoản mạng nội bộ, cần lấy lại quyền truy cập mà không phải chờ IT | Nhân viên văn phòng; IT helpdesk | Chờ IT phản hồi và xác minh (~40' trên tổng ~60') | |
| 6 | Nguyễn Văn Ba | Khi đặt hàng về quê và app báo "đang giao" từ sáng, cần biết khoảng giờ hàng tới để không phải chờ cả ngày | Khách ở tỉnh lẻ; shipper | Shipper giao theo thứ tự nhận đơn, chạy lặp giữa các xã (~8 giờ, có khi sang hôm sau) | |
| 7 | Nguyễn Quang Duy | Khi làm thủ tục hành chính lần đầu, muốn biết chính xác giấy tờ và thứ tự các bước cho trường hợp của mình, để không đi lại nhiều lần | Người làm thủ tục; người thân đi cùng | Đối chiếu nhiều nguồn (30–60') và bổ sung hồ sơ khi bị yêu cầu (60–180'/lần) | |
| 8 | Nguyễn Quang Duy | Khi người lớn tuổi nhận tin nhắn/cuộc gọi đòi chuyển tiền hay bấm link, muốn biết mức độ đáng ngờ trước khi làm theo | Người lớn tuổi; con cháu | Chờ con cháu kiểm tra (5–60'); tự đánh giá theo cảm nhận là bước rủi ro nhất | |
| 9 | Nguyễn Quang Duy | Khi lên bữa ăn cho cả tuần, muốn chốt thực đơn hợp ngân sách, khẩu vị và đồ còn trong tủ, để bớt nghĩ lại mỗi ngày và bớt lãng phí | Người nội trợ; gia đình | Nhớ khẩu vị và chọn món theo ngân sách (15–30'/tuần) | |
| 10 | Nguyễn Thị Dung | Khi bác sĩ đọc lượng lớn ảnh X-quang/MRI, muốn nhận biết ca hoặc vùng ảnh có dấu hiệu bất thường để ưu tiên xem xét | Bác sĩ chẩn đoán hình ảnh | Quan sát, rà soát ảnh/series (giả thuyết 5–15'/ca, chưa đo) | |
| 11 | Nguyễn Thị Dung | Khi bắt đầu chủ đề nghiên cứu mới, muốn tìm và đối chiếu các nghiên cứu liên quan, để chọn hướng tiếp cận dựa trên bằng chứng | Researcher / AI Engineer VRIC | Đọc sâu và đối chiếu methodology, dataset, evaluation (giả thuyết 30–60'/paper) | |
| 12 | Nguyễn Thị Dung | Khi chuẩn bị dữ liệu ảnh y khoa cho mô hình, muốn phát hiện bản ghi thiếu ảnh, thiếu kết luận hoặc sai liên kết | AI Engineer / data engineer | Ghép ID ảnh với kết luận chuyên môn (giả thuyết 30–60'/batch) | |

### 2.2. Cluster

| Cluster | Các candidate | Pattern chung |
|---|---|---|
| A — Hiểu yêu cầu và nộp lab đúng chuẩn | #1 Nộp sát deadline (Bảo), #3 Đọc đề nhiều file (Bảo), #4 Đọc đề lab mất thời gian (Ba) | Yêu cầu nộp bài nằm rải rác ở nhiều file, thiếu sót chỉ phát hiện khi đã sát hoặc quá deadline |
| B — Tìm và đối chiếu thông tin từ nhiều nguồn | #7 Thủ tục hành chính lần đầu (Duy), #11 Literature review (Dung) | Phải đọc và đối chiếu nhiều nguồn rời rạc mới biết chính xác cần làm gì |
| C — Lỗi lặp lại có cách xử lý cố định | #2 Lỗi API khi chạy prototype (Bảo), #5 Quên mật khẩu mạng nội bộ (Ba), #12 Kiểm tra dữ liệu ảnh ghép nhãn (Dung) | Lỗi có mã hoặc quy tắc rõ ràng nhưng người dùng vẫn phải tự đoán hoặc chờ người khác xử lý |
| D — Phát hiện rủi ro cao, con người quyết định cuối | #8 Tin nhắn lừa đảo người lớn tuổi (Duy), #10 Ưu tiên đọc ảnh y khoa (Dung) | Sai hoặc bỏ sót một lần là hậu quả lớn; cần người có thẩm quyền kết luận |
| E — Việc vặt đời sống | #6 Shipper giao chậm ở tỉnh (Ba), #9 Lên thực đơn tuần (Duy) | Pain có thật nhưng nhẹ, đã có cách làm đơn giản khá hiệu quả |

### 2.3. Opportunity Solution Tree rút gọn

Gốc là **1 outcome**. Nhánh là **opportunity** (nhu cầu, pain), không phải tính năng hay công cụ.

```text
OUTCOME: Học viên nộp lab đủ mục, đúng tên, trước deadline, với ít thời gian dò đề hơn
         (đo bằng: giờ commit cuối so với deadline, số lỗi định dạng bị trừ điểm, số phút từ lúc mở đề đến lúc biết rõ phải nộp gì)
├── Opportunity A: Quy định nộp bài nằm rải rác ở 6–11 file, phải đối chiếu qua lại mới biết phải nộp gì   (#3 Bảo, #4 Ba)
├── Opportunity B: Không biết bài còn thiếu mục nào cho tới khi đã sát hoặc quá deadline                  (#1 Bảo)
└── Opportunity C: Quy định nộp bài thay đổi sát giờ và khác nhau giữa các lab, dễ nộp sai cách          (#3 Bảo: đề sửa 12 commit trong ~14 giờ trước lab)
```

Outcome lấy từ cluster A (bảng 2.2), cluster có nhiều candidate nhất và có 2 thành viên tự tìm ra cùng một pain.

Những ý đã gạch bỏ vì là solution đội lốt opportunity:

- ✗ "Chatbot hỏi đáp đề lab": tên một công cụ, không phải pain.
- ✗ "Script tự kiểm tên file và cấu trúc thư mục": là cách giải cho Opportunity A/C.
- ✗ "Checklist nộp bài đặt đầu README": là cách giải, không phải nhu cầu.
- ✗ "Autograder đối chiếu bài với rubric": là cách giải cho Opportunity B.

### 2.4. Chấm điểm shortlist (1–5)

| Candidate | Actor rõ | Quy trình rõ | Pain có bằng chứng | Impact đo được | Vừa sức lab | So sánh được No AI/Rule/Workflow/Agent | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| A. Hiểu yêu cầu và nộp lab đúng chuẩn (#1, #3, #4) | 5 | 5 | 4 | 4 | 5 | 5 | 5 | **33** |
| #7 Thủ tục hành chính lần đầu | 4 | 4 | 2 | 4 | 4 | 5 | 3 | 26 |
| #5 Quên mật khẩu mạng nội bộ | 4 | 5 | 2 | 4 | 4 | 4 | 3 | 26 |

Lý do chấm:

- **A:** actor là chính học viên trong lớp; quy trình đọc đề → làm → tự kiểm → nộp vẽ được ngay; có bằng chứng từ log (commit nộp lúc 00:19 ngày 07/11, 12 lần lưu notebook từ 20:46; đề Day 02 có 11 file/1.325 dòng; repo nhóm ban đầu đặt sai tên `Day02`), 2 thành viên tự tìm ra cùng một pain. Pain có bằng chứng = 4 vì thời gian đọc đề vẫn là ước tính (15' và 35' khác nhau giữa 2 người).
- **#7:** quy trình rõ và so sánh đủ 4 mức rất tốt, nhưng chưa có số liệu thật (chỉ có cách đo); quy định khác nhau theo địa phương nên dễ quá rộng.
- **#5:** quy trình rõ, nhưng số 25 yêu cầu/tuần và 60% cùng 3 lỗi là ước lượng từ công việc cũ, chưa kiểm chứng; nhóm hiện không ở môi trường đó.

**Candidate được chọn:** A — Hiểu yêu cầu và nộp lab đúng chuẩn (gộp #1, #3 của Bảo và #4 của Ba).

**Vì sao chọn:** điểm cao nhất; có bằng chứng hành vi thật từ git log; actor là học viên nên kiểm chứng được ngay trong buổi bằng cách hỏi bạn ở nhóm khác; so sánh rõ được No AI (checklist) / Rule (script kiểm tên file) / Workflow (đối chiếu bài với rubric) / Agent.

**Vì sao loại các candidate còn lại:**

- **#7 Thủ tục hành chính:** chưa có số liệu thật nào; mỗi thủ tục và mỗi địa phương có yêu cầu khác nhau nên khó thu hẹp trong một buổi lab. Ghi vào hướng tiếp theo.
- **#5 Quên mật khẩu:** đã có giải pháp chuẩn (trang tự đặt lại mật khẩu), kết luận gần như chắc chắn là No AI; nhóm không kiểm chứng được vì không còn làm ở môi trường đó.
- **#10 Ảnh y khoa:** không tiếp cận được bác sĩ, PACS hay dữ liệu trong buổi lab; mọi số liệu là giả thuyết; rủi ro y tế cao.
- **#11 Literature review, #12 Kiểm tra dữ liệu ảnh:** chỉ một thành viên gặp, baseline chưa đo.
- **#8 Tin nhắn lừa đảo:** thiệt hại lớn nhưng khó đo tần suất, không kiểm chứng được với người lớn tuổi trong buổi lab.
- **#2 Lỗi API, #6 Shipper, #9 Thực đơn:** phạm vi hẹp hoặc pain nhẹ; #2 nhiều khả năng chỉ cần Rule (retry, fallback).

**Xử lý bất đồng (nếu có):** [Nhóm điền sau khi thảo luận: ai muốn chọn candidate khác, vì sao, nhóm chốt thế nào]

---

## 3. Kiểm chứng + research giải pháp đã có (CP4)

### 3.1. Assumption Map

| # | Giả định | Loại (Value / Usability / Feasibility / Viability) | Quan trọng (1–5) | Đã có bằng chứng (1–5) | Kiểm chứng trước? |
|---:|---|---|---:|---:|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |
| 6 | | | | | |

*Điền 4–6 giả định; xóa dòng thừa.*

Giả định nhóm kiểm chứng trong buổi này:

### 3.2. Kiểm chứng

Cách đã dùng: Phỏng vấn / Survey / Log, ticket, review

Interview snapshot (mỗi buổi phỏng vấn một bảng, hoặc đặt file trong `report/assets/cp4-interview-snapshot-N.md`):

| Trường | Nội dung |
|---|---|
| Người được hỏi (vai trò, không ghi tên thật) | |
| Câu nói đáng nhớ nhất (nguyên văn) | |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? | |
| Hiện đang xử lý bằng cách nào (workaround)? | |
| Mất bao lâu, bao lần? | |
| Insight / opportunity rút ra | |

Tổng hợp:

| Nguồn | Số người / số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác |
|---|---:|---|---|
| | | | |

**Nhóm đã sửa problem thế nào sau kiểm chứng:**

### 3.3. Research giải pháp đã có

| Công cụ / case / pattern | Link | Giải bước nào trong quy trình? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| | | | | | |
| | | | | | |
| | | | | | |

---

## 4. Quy trình trước/sau (CP5)

### 4.1. Quy trình hiện tại

Sơ đồ (ASCII, Mermaid hoặc link ảnh trong `report/assets/`):

```text

```

| Bước | Actor | Input | Output | Thời gian / tần suất | Ghi chú |
|---:|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |

**Bottleneck chính:**

### 4.2. Quy trình tương lai

Ghi rõ bước nào **Rule**, bước nào **AI**, bước nào **con người**, **boundary** ở đâu, **phương án quay về** khi AI sai.

```text

```

### 4.3. Before / after

| Chỉ số | Trước | Sau (kỳ vọng) | Ghi chú |
|---|---:|---:|---|
| Số bước | | | |
| Tổng thời gian | | | |
| Số bước thủ công | | | |
| Bottleneck chính | | | |
| Rủi ro mới phát sinh | | | |

---

## 5. Problem Statement v0 (CP5)

| Trường | Nội dung |
|---|---|
| **Actor** | |
| **Quy trình** | |
| **Bottleneck** | |
| **Impact** | |
| **Success Metric** (baseline → target, cách đo) | |
| **Boundary** (AI không được làm gì; khi nào cần con người kiểm tra — HITL) | |

Phản biện nhận được (từ AI hoặc nhóm khác) và nhóm có đồng ý không:

-

---

## 6. Mức can thiệp AI (CP6)

### 6.1. Ma trận độ mơ hồ × độ phức tạp

Bài của nhóm nằm ở ô:

Vì sao:

### 6.2. So sánh 4 mức

| Mức | Phương án cho bài của nhóm | Đủ khi nào | Rủi ro | Chọn? |
|---|---|---|---|---|
| **No AI** (sửa quy trình) | | | | |
| **Rule** | | | | |
| **Workflow** | | | | |
| **Agent** | | | | |

**Mức chọn:**

**Vì sao không chọn mức đơn giản hơn:**

### 6.3. AI Canvas rút gọn

| Thành phần | Nội dung |
|---|---|
| **Prediction** — AI dự đoán / tạo ra gì? | |
| **Judgment** — con người cân nhắc, quyết định gì? | |
| **Action** — hành động cuối cùng là gì, ai làm? | |
| **Outcome** — đo kết quả bằng gì? | |
| **Input** — AI cần dữ liệu đầu vào gì mỗi lần chạy? Có sẵn không? | |
| **Feedback** — lấy phản hồi ở đâu để cải thiện? | |

### 6.4. Hai câu hỏi của Google PAIR

- Người dùng muốn **được hỗ trợ (augment)** hay **giao hẳn việc (automate)**? Bằng chứng:
- AI sai kiểu nào tệ hơn, **báo nhầm** hay **bỏ sót**? Vì sao, và thiết kế đã xử lý thế nào:

---

## 7. Problem Statement v1 + tiêu chí đánh giá (CP6)

| Trường | Nội dung |
|---|---|
| **Actor** | |
| **Quy trình** | |
| **Bottleneck** | |
| **Impact** | |
| **Success Metric** (baseline → target, cách đo) | |
| **Boundary** | |
| **AI intervention point** | |
| **Mức chọn** | No AI / Rule / Workflow / Agent |
| **Rủi ro & người kiểm tra** | |

**Thay đổi so với v0 và lý do:**

| Trường | v0 | v1 | Vì sao đổi |
|---|---|---|---|
| | | | |

**Tiêu chí đánh giá đầu ra của AI (3–5 tiêu chí):**

| # | Tiêu chí | Đạt khi | Không đạt khi |
|---:|---|---|---|
| 1 | | | |
| 2 | | | |
| 3 | | | |

---

## 8. Quyết định (CP6)

### 8.1. Bốn rủi ro

| Rủi ro | Câu hỏi | Mức độ rủi ro (Thấp = an toàn / TB / Cao = nguy hiểm) | Lý do / bằng chứng |
|---|---|---|---|
| **Value** | Người dùng có thật sự cần và sẽ dùng không? | | |
| **Usability** | Người dùng có dùng được, có hiểu và sửa được đầu ra của AI không? | | |
| **Feasibility** | Có đủ dữ liệu, công cụ, kỹ năng để làm không? | | |
| **Viability** | Có hợp chi phí, pháp lý, quy định tổ chức không? Ai vận hành? | | |

### 8.2. Kết luận

**Quyết định:** Go / Not Yet / No-Go

**Lý do:**

**Nếu Go — pilot nhỏ nhất:**

**Nếu Not Yet — cần kiểm chứng gì trước:**

**Nếu No-Go — nên làm gì thay AI:**

**Ngưỡng dừng** (nếu sau … mà … thì quay về …):

---

## 9. Hạn chế và hướng tiếp theo

-

## 10. Tài liệu tham khảo

-
