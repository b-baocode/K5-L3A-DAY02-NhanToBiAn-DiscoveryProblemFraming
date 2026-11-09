# Báo cáo nhóm — Day 02 Discovery & Problem Framing

> Bản chung của nhóm, viết trên repo do nhóm trưởng fork. Không copy file này sang repo cá nhân.
> Template chi tiết và prompt mẫu: [docs/01-worksheet.md](../../docs/01-worksheet.md). Bài mẫu: [docs/02-deliverable-example.md](../../docs/02-deliverable-example.md).

## 1. Thông tin nhóm

- Tên nhóm: NhanToBiAn
- Thành viên: xem `TEAM.md`
- Candidate problem được chọn (1 câu): Học viên bỏ sót quy định nộp bài (tên repo, tên file, tiêu đề, mục bắt buộc) nằm rải rác ở nhiều file và chỉ phát hiện khi đã sát deadline
- Quyết định cuối: Go, phạm vi nhỏ — Rule (rào cản pre-push + Actions kiểm lại + checklist), không dùng AI

---

## 2. Hội tụ nhóm (CP3)

### 2.1. Pitch

|   # | Người đưa ra     | Candidate (Job Story ngắn)                                                                                                            | Actor                                 | Bottleneck                                                                                        | Câu hỏi phản biện nhận được (ai hỏi) |
| --: | ---------------- | ------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------ |
|   1 | Ngô Gia Bảo      | Khi tới tối ngày lab mà bài chưa xong, muốn biết còn thiếu phần nào so với yêu cầu, để nộp đủ trước 23h59                             | Học viên AI20K                        | Tự đối chiếu bài với rubric rồi quay lại sửa (~60', lặp 12 lần lưu, commit nộp 00:19)             |                                      |
|   2 | Ngô Gia Bảo      | Khi chạy prototype gọi API bị lỗi, muốn biết lỗi do code mình hay do nhà cung cấp, để không sửa nhầm chỗ                              | Học viên làm lab có gọi API           | Đoán nguyên nhân lỗi 404/503/504/ReadTimeout (~16' trên tổng ~30')                                |                                      |
|   3 | Ngô Gia Bảo      | Khi nhận đề lab nhiều file, muốn nắm nhanh phải nộp gì, đặt tên thế nào, lỗi nào bị trừ nặng, để không mất điểm oan                   | Học viên AI20K                        | Rút các quy định bị trừ điểm nằm rải rác ở 11 file/1.325 dòng (dễ bỏ sót, ví dụ tên repo `DAY02`) |                                      |
|   4 | Nguyễn Văn Ba    | Khi mở đề lab mới, cần biết ngay phải nộp file nào, điền mục nào, đặt tên ra sao, để bắt tay làm sau ~10'                             | Học viên K5                           | Đối chiếu qua lại 6–7 file để biết phải nộp gì (~10' trên tổng ~35')                              |                                      |
|   5 | Nguyễn Văn Ba    | Khi đầu giờ quên mật khẩu/bị khóa tài khoản mạng nội bộ, cần lấy lại quyền truy cập mà không phải chờ IT                              | Nhân viên văn phòng; IT helpdesk      | Chờ IT phản hồi và xác minh (~40' trên tổng ~60')                                                 |                                      |
|   6 | Nguyễn Văn Ba    | Khi đặt hàng về quê và app báo "đang giao" từ sáng, cần biết khoảng giờ hàng tới để không phải chờ cả ngày                            | Khách ở tỉnh lẻ; shipper              | Shipper giao theo thứ tự nhận đơn, chạy lặp giữa các xã (~8 giờ, có khi sang hôm sau)             |                                      |
|   7 | Nguyễn Quang Duy | Khi làm thủ tục hành chính lần đầu, muốn biết chính xác giấy tờ và thứ tự các bước cho trường hợp của mình, để không đi lại nhiều lần | Người làm thủ tục; người thân đi cùng | Đối chiếu nhiều nguồn (30–60') và bổ sung hồ sơ khi bị yêu cầu (60–180'/lần)                      |                                      |
|   8 | Nguyễn Quang Duy | Khi người lớn tuổi nhận tin nhắn/cuộc gọi đòi chuyển tiền hay bấm link, muốn biết mức độ đáng ngờ trước khi làm theo                  | Người lớn tuổi; con cháu              | Chờ con cháu kiểm tra (5–60'); tự đánh giá theo cảm nhận là bước rủi ro nhất                      |                                      |
|   9 | Nguyễn Quang Duy | Khi lên bữa ăn cho cả tuần, muốn chốt thực đơn hợp ngân sách, khẩu vị và đồ còn trong tủ, để bớt nghĩ lại mỗi ngày và bớt lãng phí    | Người nội trợ; gia đình               | Nhớ khẩu vị và chọn món theo ngân sách (15–30'/tuần)                                              |                                      |
|  10 | Nguyễn Thị Dung  | Khi bác sĩ đọc lượng lớn ảnh X-quang/MRI, muốn nhận biết ca hoặc vùng ảnh có dấu hiệu bất thường để ưu tiên xem xét                   | Bác sĩ chẩn đoán hình ảnh             | Quan sát, rà soát ảnh/series (giả thuyết 5–15'/ca, chưa đo)                                       |                                      |
|  11 | Nguyễn Thị Dung  | Khi bắt đầu chủ đề nghiên cứu mới, muốn tìm và đối chiếu các nghiên cứu liên quan, để chọn hướng tiếp cận dựa trên bằng chứng         | Researcher / AI Engineer VRIC         | Đọc sâu và đối chiếu methodology, dataset, evaluation (giả thuyết 30–60'/paper)                   |                                      |
|  12 | Nguyễn Thị Dung  | Khi chuẩn bị dữ liệu ảnh y khoa cho mô hình, muốn phát hiện bản ghi thiếu ảnh, thiếu kết luận hoặc sai liên kết                       | AI Engineer / data engineer           | Ghép ID ảnh với kết luận chuyên môn (giả thuyết 30–60'/batch)                                     |                                      |

### 2.2. Cluster

| Cluster                                             | Các candidate                                                                                                     | Pattern chung                                                                                  |
| --------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| A — Hiểu yêu cầu và nộp lab đúng chuẩn              | #1 Nộp sát deadline (Bảo), #3 Đọc đề nhiều file (Bảo), #4 Đọc đề lab mất thời gian (Ba)                           | Yêu cầu nộp bài nằm rải rác ở nhiều file, thiếu sót chỉ phát hiện khi đã sát hoặc quá deadline |
| B — Tìm và đối chiếu thông tin từ nhiều nguồn       | #7 Thủ tục hành chính lần đầu (Duy), #11 Literature review (Dung)                                                 | Phải đọc và đối chiếu nhiều nguồn rời rạc mới biết chính xác cần làm gì                        |
| C — Lỗi lặp lại có cách xử lý cố định               | #2 Lỗi API khi chạy prototype (Bảo), #5 Quên mật khẩu mạng nội bộ (Ba), #12 Kiểm tra dữ liệu ảnh ghép nhãn (Dung) | Lỗi có mã hoặc quy tắc rõ ràng nhưng người dùng vẫn phải tự đoán hoặc chờ người khác xử lý     |
| D — Phát hiện rủi ro cao, con người quyết định cuối | #8 Tin nhắn lừa đảo người lớn tuổi (Duy), #10 Ưu tiên đọc ảnh y khoa (Dung)                                       | Sai hoặc bỏ sót một lần là hậu quả lớn; cần người có thẩm quyền kết luận                       |
| E — Việc vặt đời sống                               | #6 Shipper giao chậm ở tỉnh (Ba), #9 Lên thực đơn tuần (Duy)                                                      | Pain có thật nhưng nhẹ, đã có cách làm đơn giản khá hiệu quả                                   |

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

| Candidate                                          | Actor rõ | Quy trình rõ | Pain có bằng chứng | Impact đo được | Vừa sức lab | So sánh được No AI/Rule/Workflow/Agent | Nhóm hiểu domain |   Tổng |
| -------------------------------------------------- | -------: | -----------: | -----------------: | -------------: | ----------: | -------------------------------------: | ---------------: | -----: |
| A. Hiểu yêu cầu và nộp lab đúng chuẩn (#1, #3, #4) |        5 |            5 |                  4 |              4 |           5 |                                      5 |                5 | **33** |
| #7 Thủ tục hành chính lần đầu                      |        4 |            4 |                  2 |              4 |           4 |                                      5 |                3 |     26 |
| #5 Quên mật khẩu mạng nội bộ                       |        4 |            5 |                  2 |              4 |           4 |                                      4 |                3 |     26 |

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

**Xử lý bất đồng (nếu có):** Không có bất đồng khi chọn candidate. A hơn hai candidate xếp sau 7 điểm (33 so với 26), và 2 thành viên (Bảo, Ba) tự tìm ra cùng một pain, nên nhóm chốt A. Điểm còn bàn là thời gian đọc đề có phải pain thật không (ước tính 15' và 35' lệch nhau). Nhóm xử lý bằng cách không dùng thời gian đọc đề làm metric chính, chuyển sang đếm lỗi định dạng (mục 3.2).

---

## 3. Kiểm chứng + research giải pháp đã có (CP4)

### 3.1. Assumption Map

|   # | Giả định                                                                                                                | Loại (Value / Usability / Feasibility / Viability) | Quan trọng (1–5) | Đã có bằng chứng (1–5) | Kiểm chứng trước? |
| --: | ----------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------- | ---------------: | ---------------------: | ----------------- |
|   1 | Học viên khác cũng nộp sát deadline vì phát hiện thiếu sót muộn, không chỉ riêng một người                              | Value                                              |                5 |                      2 | ✅                |
|   2 | Lỗi bị trừ điểm chủ yếu là lỗi định dạng (tên file, tên repo, tiêu đề) do bỏ sót quy định, không phải do thiếu nội dung | Value                                              |                5 |                      2 | ✅                |
|   3 | Nộp muộn là do không biết bài còn thiếu gì, không phải do bắt đầu làm muộn                                              | Value                                              |                4 |                      1 | ✅                |
|   4 | Quy định nộp bài giữa các lab đủ giống nhau để dùng chung một checklist hoặc một bộ kiểm tra                            | Feasibility                                        |                4 |                      3 | —                 |
|   5 | Ban tổ chức sẵn sàng thêm checklist hoặc bước kiểm tra tự động vào repo đề                                              | Viability                                          |                3 |                      1 | Hỏi coach sau lab |

Giả định nhóm kiểm chứng trong buổi này: #1, #2, #3 (quan trọng cao, bằng chứng thấp).

### 3.2. Kiểm chứng

Cách đã dùng:

1. **Log** (git log của các repo lab và artefact trong repo nhóm): hành vi đã xảy ra, ghi theo vai trò, không ghi tên.
2. **Phỏng vấn nhanh 2–3 học viên nhóm khác** theo The Mom Test, mỗi buổi ~5'. Không phỏng vấn thành viên nhóm mình.

**Bộ câu hỏi phỏng vấn** (chỉ hỏi về hành vi đã xảy ra, không có câu "Bạn có muốn…" / "Bạn có dùng… không nếu…"):

|   # | Câu hỏi                                                                                                                                | Kiểm giả định                                            |
| --: | -------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------- |
|   1 | Lab gần nhất bạn nộp là lab nào? Bạn commit bản cuối lúc mấy giờ? (mở git log cùng xem nếu được)                                       | #1                                                       |
|   2 | Kể lại từ lúc mở đề tới lúc nộp: bạn làm những bước nào?                                                                               | #3                                                       |
|   3 | Lần gần nhất bạn phát hiện bài còn thiếu hoặc sai một quy định nộp bài là khi nào? Thiếu cái gì? Phát hiện lúc mấy giờ, bằng cách nào? | #1, #2                                                   |
|   4 | Bạn đã từng bị trừ điểm hoặc phải sửa gấp vì tên repo, tên file, tiêu đề hay thiếu mục chưa? Chuyện gì đã xảy ra?                      | #2                                                       |
|   5 | Trước khi nộp, bạn tự kiểm tra bài bằng cách nào? Mất khoảng bao lâu?                                                                  | Workaround hiện tại                                      |
|   6 | Lần đó bạn bắt đầu làm lúc mấy giờ?                                                                                                    | #3 (phân biệt "bắt đầu muộn" với "phát hiện thiếu muộn") |

**Interview snapshot:** _Chờ nhóm điền sau khi phỏng vấn thật. Mỗi buổi ghi một bảng ngay sau khi xong; nếu chưa phỏng vấn kịp, để trống và ghi rõ là chưa thực hiện, không được điền số liệu giả định._

**Snapshot 1**

| Trường                                            | Nội dung |
| ------------------------------------------------- | -------- |
| Người được hỏi (vai trò, không ghi tên thật)      |          |
| Câu nói đáng nhớ nhất (nguyên văn)                |          |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? |          |
| Hiện đang xử lý bằng cách nào (workaround)?       |          |
| Mất bao lâu, bao lần?                             |          |
| Insight / opportunity rút ra                      |          |

**Snapshot 2**

| Trường                                            | Nội dung |
| ------------------------------------------------- | -------- |
| Người được hỏi (vai trò, không ghi tên thật)      |          |
| Câu nói đáng nhớ nhất (nguyên văn)                |          |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? |          |
| Hiện đang xử lý bằng cách nào (workaround)?       |          |
| Mất bao lâu, bao lần?                             |          |
| Insight / opportunity rút ra                      |          |

**Snapshot 3** (tùy chọn)

| Trường                                            | Nội dung |
| ------------------------------------------------- | -------- |
| Người được hỏi (vai trò, không ghi tên thật)      |          |
| Câu nói đáng nhớ nhất (nguyên văn)                |          |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? |          |
| Hiện đang xử lý bằng cách nào (workaround)?       |          |
| Mất bao lâu, bao lần?                             |          |
| Insight / opportunity rút ra                      |          |

Tổng hợp:

| Nguồn | Số người / số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác |
|---|---:|---|---|
| Git log repo nhóm lab Day 02 codelab (07/11/2026) — commit nội dung cuối của từng thành viên | 5 học viên | 3/5 thành viên commit nội dung cuối sau 21h (21:05, 21:28, 22:22); 1 thành viên commit "fix" lúc 22:22, merge bản cuối lúc 22:28 | 2/5 thành viên xong trước 15h30 (13:07, 15:20) → nộp sát giờ không xảy ra với mọi người; có thể phụ thuộc thời điểm bắt đầu (giả định #3) |
| Git log lab Day 01 AI Foundation, cá nhân (06–07/11/2026) | 1 học viên | Lưu notebook 12 lần từ 20:46 tới 00:22; commit "submit day 1 lab" lúc 00:19 ngày 07/11, sau mốc 23h59 | Mới có 1 người, chưa đủ kết luận cho cả lớp |
| Lịch sử commit repo đề Day 02 (08–09/11/2026) | 12 commit | Đề được sửa 12 commit trong ~14 giờ trước lab, có commit "Fix grading-rule conflicts", "Sua cac cho chua nhat quan trong de bai" → quy định thay đổi sát giờ (Opportunity C) | Các sửa đổi nhằm làm đề nhất quán hơn, không phải đổi yêu cầu nộp bài |
| Artefact trong repo nhóm hôm nay (09/11/2026) | 1 repo, 4 file báo cáo cá nhân | Repo nhóm ban đầu đặt tên `Day02` thay vì `DAY02` (sai mẫu, −5 điểm), phải đổi trong buổi; 2/4 file báo cáo cá nhân có dòng tiêu đề chưa khớp tên file dù template yêu cầu "Sửa cả dòng tiêu đề phía trên cho khớp" → lỗi định dạng xảy ra ngay cả khi đã đọc đề (giả định #2) | Lỗi tên repo được phát hiện và sửa trong buổi; 2 lỗi tiêu đề vẫn còn tại thời điểm viết báo cáo, chỉ được phát hiện khi rà lại cả repo. Đây là 3 lỗi dùng làm baseline ở mục 5 |
| Phỏng vấn học viên nhóm khác (snapshot 1–3)                                                  |           3 bạn cùng phòng lab | Cả 3 đều cảm thấy không quá hứng thú với chức năng này                                                                                                                                                                                                                         | Đây là vấn đề mà có 3 thành viên trong nhóm gặp phải                                                                                      |
| Ước tính thời gian đọc đề trong báo cáo CP1 | 2 thành viên | Cả 2 đều coi việc tìm quy định nộp bài trong nhiều file là bước khó nhất | Ước tính lệch nhau nhiều (15' và 35'/lab) → thời gian đọc đề không phải pain chắc chắn |

**Nhóm đã sửa problem thế nào sau kiểm chứng:**

- **Trước kiểm chứng:** "Đọc đề lab nhiều file mất thời gian" (nhấn vào thời gian đọc).
- **Sau kiểm chứng:** thu hẹp thành **"bỏ sót quy định nộp bài (tên repo, tên file, tiêu đề, mục bắt buộc) và chỉ phát hiện khi đã sát deadline"**. Lý do: log cho thấy lỗi định dạng xảy ra thật ngay trong nhóm (tên repo, tiêu đề file), trong khi thời gian đọc đề giữa các thành viên lệch nhau nhiều và chưa chắc là pain.
- **Giả định #3 chưa được xác nhận:** 2/5 học viên ở lab Day 02 codelab xong sớm, nên nộp muộn có thể do bắt đầu muộn. Nhóm không dùng "nộp muộn" làm metric chính; metric chính chuyển sang **số lỗi định dạng phát hiện trước khi nộp**.

### 3.3. Research giải pháp đã có

| Công cụ / case / pattern                | Link                                                                                                                                                                                                         | Giải bước nào trong quy trình?                                                                                                                        | Điểm mạnh                                                                                                     | Khoảng trống / rủi ro                                                                                                                            | Bài học cho nhóm                                                                                      |
| --------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------- |
| GitHub Classroom autograding            | https://docs.github.com/en/education/manage-coursework-with-github-classroom/teach-with-github-classroom/use-autograding                                                                                     | Bước tự kiểm trước khi nộp: chạy test mỗi lần học viên push, học viên xem kết quả và sửa                                                              | Đúng pattern "kiểm tự động ngay khi push", học viên thấy lỗi trước deadline                                   | Trang tài liệu ghi GitHub Classroom **ngừng hoạt động từ 28/08/2026**; lab này không dùng Classroom mà dùng repo fork                            | Ý tưởng đúng nhưng công cụ đã ngừng → phải dùng thứ còn hoạt động (GitHub Actions)                    |
| GitHub Actions (workflow chạy khi push) | https://docs.github.com/en/actions/writing-workflows/quickstart · https://docs.github.com/en/billing/managing-billing-for-your-products/managing-billing-for-github-actions/about-billing-for-github-actions | Bước kiểm tên file, cấu trúc thư mục, mục bắt buộc: workflow trong `.github/workflows` tự chạy khi push (`on: [push]`), chạy được lệnh shell (`run:`) | Runner chuẩn của GitHub miễn phí cho repo public (theo trang billing); chạy ngay trên repo fork; không cần AI | Phải có người viết và bảo trì script; chỉ kiểm được thứ có quy tắc rõ (tên, cấu trúc, mục có hay không), không đánh giá được chất lượng nội dung | Phần lớn lỗi bị trừ điểm (tên repo, tên file, tiêu đề, thiếu file) là **Rule**, kiểm được bằng script |
| ls-lint (+ GitHub Action chính thức)    | https://ls-lint.org/ · https://github.com/ls-lint/action                                                                                                                                                     | Bước kiểm tên file và thư mục theo quy ước khai báo trong `.ls-lint.yml`                                                                              | Công cụ có sẵn, cấu hình một file, có GitHub Action chính thức                                                | Chỉ kiểm tên file/thư mục, không kiểm tên repo hay nội dung trong file                                                                           | Không cần tự viết từ đầu phần kiểm tên file; kết hợp với checklist cho phần nội dung                  |

**Kết luận research:** các bước kiểm định dạng (tên repo, tên file, cấu trúc, mục bắt buộc) đã có công cụ Rule làm được và không cần AI. Phần chưa có công cụ là **đối chiếu nội dung bài với rubric** (mục có đủ ý chưa, có số liệu chưa) — đây là chỗ duy nhất có thể cân nhắc AI ở CP6.

---

## 4. Quy trình trước/sau (CP5)

### 4.1. Quy trình hiện tại

Sơ đồ (ASCII, Mermaid hoặc link ảnh trong `report/assets/`):

```text
HIỆN TẠI — mỗi lab, ghép từ card #1, #3 (Bảo) và #4 (Ba)

[1 Mở README: 2–5'] → [2 Đọc RULES/CHECKPOINTS/RUBRIC/SUBMISSION + worksheet: 11–18']
→ [3 Tự rút quy định nộp bài từ nhiều file: 2–10'] ← BOTTLENECK (bỏ sót tên repo, tên file, tiêu đề, mục bắt buộc)
→ [4 Làm bài: phần lớn buổi lab]
→ [5 Tự đối chiếu bài với rubric, sửa mục thiếu: ~60', lặp nhiều vòng]
→ [6 Kiểm tên file, cấu trúc bằng mắt, commit + nộp: 5–10']   ← lỗi bỏ sót ở bước 3 chỉ lộ ra ở đây, sát deadline
```

| Bước | Actor           | Input                                             | Output                                                                 | Thời gian / tần suất            | Ghi chú                                                                      |
| ---: | --------------- | ------------------------------------------------- | ---------------------------------------------------------------------- | ------------------------------- | ---------------------------------------------------------------------------- |
|    1 | Học viên        | README của đề                                     | Nắm mục tiêu lab                                                       | 2–5' / mỗi lab                  |                                                                              |
|    2 | Học viên        | RULES, CHECKPOINTS, RUBRIC, SUBMISSION, worksheet | Biết các bước và tiêu chí chấm                                         | 11–18' / mỗi lab                | Đề Day 02: 11 file, 1.325 dòng                                               |
|    3 | Học viên        | Các file ở bước 2 + template báo cáo              | Danh sách tự ghi "phải nộp gì, đặt tên thế nào" (thường chỉ trong đầu) | 2–10' / mỗi lab                 | Ước tính lệch nhau giữa Bảo (~15' cả bước 1–3) và Ba (~35')                  |
|    4 | Học viên / nhóm | Đề + danh sách ở bước 3                           | Bài làm                                                                | Phần lớn buổi lab               |                                                                              |
|    5 | Học viên        | Bài làm + RUBRIC                                  | Danh sách mục còn thiếu, bài đã sửa                                    | ~60' (ước tính), lặp nhiều vòng | Day 01: 12 lần lưu từ 20:46 tới 00:22                                        |
|    6 | Học viên        | Bài đã sửa                                        | Commit + link nộp LMS                                                  | 5–10' / mỗi lab                 | Day 01: commit nộp 00:19; Day 02 codelab: 3/5 thành viên commit cuối sau 21h |

**Bottleneck chính:** Bước 3, tự rút quy định nộp bài từ 11 file. Bước này không lâu (2–10') nhưng là chỗ sinh ra lỗi: quy định nào bị bỏ sót ở đây thì không có bước nào kiểm lại một cách có hệ thống, chỉ lộ ra khi tự soát bằng mắt ở bước 5–6, sát deadline. Bằng chứng: repo nhóm đặt sai `Day02`, 2/4 file báo cáo cá nhân có tiêu đề chưa khớp tên file (mục 3.2).

### 4.2. Quy trình tương lai

Ghi rõ bước nào **Rule**, bước nào **AI**, bước nào **con người**, **boundary** ở đâu, **phương án quay về** khi AI sai.

```text
TƯƠNG LAI — mỗi lab, không có bước AI

[1 Đọc checklist "Phải nộp gì" ở đầu README: 2–5']        ← NO AI (checklist viết 1 lần/lab, trích dẫn file gốc)
→ [2 Bật rào cản, 1 lần/repo: 1']                          ← CON NGƯỜI (git config core.hooksPath .githooks)
→ [3 Đọc file chi tiết khi cần: 10–15']                    ← CON NGƯỜI
→ [4 Làm bài, commit]                                      ← CON NGƯỜI
→ [5 git push → hook pre-push tự kiểm trên máy: < 10 giây] ← RULE (RÀO CẢN)
      kiểm: tên repo đúng mẫu DAY02 · tên file MSSV_HoTen.md · tiêu đề khớp tên file · đủ các mục bắt buộc, mục không trống
      sai quy cách → CHẶN push, in lỗi kèm trích dẫn file đề
      đúng quy cách → cho push, in NHẮC NHỞ các mục nội dung bộ kiểm không kiểm được (đối chiếu rubric, reflection tự viết…)
→ [6 Sửa theo báo lỗi, push lại: 2–5']                     ← CON NGƯỜI
→ [7 GitHub Actions kiểm lại trên repo: < 2']             ← RULE (LƯỚI AN TOÀN: bắt lỗi khi push từ máy chưa bật hook, hoặc sửa file trên web)
→ [8 Tự đối chiếu nội dung với rubric: ~60']             ← CON NGƯỜI (ngoài phạm vi bộ kiểm)
→ [9 Nộp link LMS: 2']                                     ← CON NGƯỜI

Boundary: bộ kiểm chặn push nhưng không đổi tên, không sửa file, không tự commit, không chấm nội dung;
khi kết quả bộ kiểm khác với file đề, file đề là quy định chính thức.
Học viên luôn được vượt rào bằng `git push --no-verify` khi chắc chắn bộ kiểm sai hoặc sát deadline:
nộp được bài quan trọng hơn đúng quy cách; mỗi lần vượt rào báo nhóm trưởng để sửa rule.
Phương án quay về: hook chặn nhầm → vượt rào bằng --no-verify, chuyển hook sang chế độ chỉ nhắc (cảnh báo nhưng vẫn cho push);
hook và Actions đều không chạy → tick tay checklist ở bước 1, 1 thành viên soát chéo trước deadline 1 giờ.
```

### 4.3. Before / after

| Chỉ số | Trước | Sau (kỳ vọng) | Ghi chú |
|---|---:|---:|---|
| Số bước | 6 | 9 | Thêm bật rào cản (1 lần/repo), kiểm trên máy khi push, sửa theo báo lỗi, kiểm lại trên repo |
| Tổng thời gian | ~80–100' ngoài thời gian làm bài | ~75–95' | Thời gian gần như không đổi; cái đổi là **thời điểm phát hiện lỗi**: từ sát deadline sang **trước khi bài lên repo** |
| Số bước thủ công | 6 | 7 | Thêm 1 bước bật rào cản (chỉ 1 lần); bước tự rút quy định (bước 3 cũ) được thay bằng checklist có sẵn + kiểm tự động |
| Lỗi sai quy cách lên được repo | Có, không ai chặn | Chỉ khi vượt rào bằng `--no-verify` hoặc chưa bật hook; Actions vẫn bắt lại | Rào cản chuyển từ "báo sau" sang "chặn trước" |
| Bottleneck chính | Bước 3: tự rút quy định từ 11 file, dễ bỏ sót | Bước 8: đối chiếu nội dung với rubric | Phần định dạng được Rule xử lý; phần nội dung chưa giải, ghi vào hướng tiếp theo |
| Rủi ro mới phát sinh | — | **Chặn nhầm sát deadline** làm không push được bài (rủi ro lớn nhất, xử lý bằng quyền vượt rào); hook chỉ chạy khi mỗi người tự bật trên máy mình; bộ kiểm lỗi thời khi đề sửa sát giờ (đề Day 02 có 12 commit sửa trong ~14 giờ trước lab); học viên coi "qua được rào" là đủ và bỏ qua kiểm nội dung | Xử lý ở boundary (mục 4.2), tiêu chí đánh giá (mục 7) và ngưỡng dừng (mục 8) |

---

## 5. Problem Statement v0 (CP5)

| Trường                                                                     | Nội dung                                                                                                                                                                                                                                                                                                                                                 |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Actor**                                                                  | Học viên AI20K làm lab cá nhân và nhóm trên repo GitHub, nộp link repo qua LMS                                                                                                                                                                                                                                                                           |
| **Quy trình**                                                              | Mở README → đọc RULES, CHECKPOINTS, RUBRIC, SUBMISSION, worksheet → tự rút quy định nộp bài → làm bài → tự đối chiếu bài với rubric → kiểm tên file, commit, nộp (mục 4.1)                                                                                                                                                                               |
| **Bottleneck**                                                             | Bước tự rút quy định nộp bài từ 11 file/1.325 dòng: quy định bị bỏ sót ở đây không có bước nào kiểm lại có hệ thống, chỉ lộ ra khi tự soát bằng mắt sát deadline                                                                                                                                                                                         |
| **Impact**                                                                 | Mỗi lỗi tên repo/file có nguy cơ bị trừ 5 điểm. Day 02: 3 lỗi định dạng trong 1 repo nhóm 4 người (tên repo `Day02`, 2 file báo cáo có tiêu đề chưa khớp tên file). Lỗi phát hiện muộn kéo theo sửa gấp sát giờ (Day 01: commit nộp lúc 00:19, sau 23h59)                                                                                                |
| **Success Metric** (baseline → target, cách đo)                            | (1) Số lỗi định dạng còn trong repo tại commit cuối trước deadline: 3/repo (Day 02, đếm tay ngày 09/11) → 0. (2) Thời điểm phát hiện lỗi: khi có người tình cờ thấy, có khi sát deadline → trong buổi lab, ngay lần push đầu tiên sau khi lỗi phát sinh. Cách đo: đếm lỗi theo danh sách quy định tại commit cuối của 3 lab tiếp theo, đối chiếu git log |
| **Boundary** (AI không được làm gì; khi nào cần con người kiểm tra — HITL) | Không công cụ nào được tự đổi tên repo/file, tự sửa nội dung, tự commit hay tự nộp bài; không chấm nội dung thay người chấm. File đề là quy định chính thức. HITL: học viên tự đọc kết quả kiểm và quyết định sửa; mỗi khi đề sửa quy định nộp bài, người phụ trách cập nhật lại danh sách quy định trước khi dùng                                       |

Phản biện nhận được (từ AI hoặc nhóm khác) và nhóm có đồng ý không:

- **AI (vai PM hoài nghi): baseline 3 lỗi chỉ đếm trên 1 repo nhóm, mẫu quá nhỏ.** Đồng ý một phần: đây là lỗi thật, đếm được, nhưng chưa đại diện cho cả lớp. Giữ làm baseline, ghi rõ cần phỏng vấn nhóm khác (mục 3.2) để mở rộng.
- **AI: metric chỉ đếm lỗi định dạng, bỏ qua lỗi thiếu nội dung.** Đồng ý: thu hẹp phạm vi có chủ đích vì lỗi định dạng có đúng/sai rõ và đã có bằng chứng; lỗi nội dung ghi vào hạn chế (mục 9).
- **AI: Boundary nói "không công cụ nào được…" có phải đang ngầm chứa giải pháp không?** Không đồng ý: boundary chỉ giới hạn phạm vi can thiệp, chưa chọn công cụ cụ thể; giải pháp chỉ chốt ở mục 6.

---

## 6. Mức can thiệp AI (CP6)

### 6.1. Ma trận độ mơ hồ × độ phức tạp

Bài của nhóm nằm ở ô: **Độ mơ hồ thấp × Độ phức tạp thấp** → Rule hoặc Workflow đơn giản thường đủ.

Vì sao:

- **Mơ hồ thấp:** mỗi quy định có đúng/sai rõ ràng: repo có tên `DAY02` hay không, file có đúng mẫu `MSSV_HoTen.md` hay không, tiêu đề có khớp tên file hay không, mục bắt buộc có hay không.
- **Phức tạp thấp:** 1 nguồn dữ liệu (chính repo của học viên), các phép kiểm độc lập nhau, bước sau không phụ thuộc kết quả bước trước.

### 6.2. So sánh 4 mức

| Mức | Phương án cho bài của nhóm | Đủ khi nào | Rủi ro | Chọn? |
|---|---|---|---|---|
| **No AI** (sửa quy trình) | Checklist "Phải nộp gì" ở đầu README, mỗi dòng trích dẫn file gốc; 1 thành viên soát chéo trước deadline 1 giờ | Học viên đọc và tick đủ checklist | Chỉ nhắc, không kiểm: template Day 02 đã ghi rõ "Sửa cả dòng tiêu đề phía trên cho khớp" mà 2/4 file vẫn sai | Có, làm nền |
| **Rule** | Hook `pre-push` trên máy học viên: chặn push khi sai quy cách, nhắc các mục nội dung khi đúng quy cách; GitHub Actions + ls-lint kiểm lại trên repo làm lưới an toàn | Quy định có đúng/sai rõ: đủ cho cả 3 lỗi đã xảy ra ở Day 02 | Chặn nhầm sát deadline; mỗi người phải tự bật hook; lỗi thời khi đề sửa sát giờ; repo fork phải bật Actions | **Có** |
| **Workflow** | Script lấy bài + rubric, AI đánh giá mục nào còn thiếu ý | Khi cần kiểm **nội dung** (đủ ý, có số liệu) | Mơ hồ cao, chưa có tiêu chí "đủ ý" rõ; AI báo "đủ" khi chưa đủ làm học viên chủ quan | Không, để sau |
| **Agent** | AI tự đọc đề, tự sửa tên, tự sửa bài, tự commit | Không có trường hợp nào trong bài này cần AI tự quyết bước tiếp theo | Tự sửa bài và tự commit vi phạm quy định "không viết hộ"; sai thì mất điểm thật | Không |

**Mức chọn:** Rule, kèm checklist (No AI) làm nền.

**Vì sao không chọn mức đơn giản hơn:** No AI (checklist) đã có sẵn dạng ghi chú trong template nhưng vẫn bị bỏ sót: 2/4 file báo cáo cá nhân Day 02 có tiêu đề chưa khớp tên file dù template ghi rõ yêu cầu. Checklist chỉ nhắc, còn lỗi chỉ hết khi có bước **kiểm** tự động chạy mỗi lần push. Nhóm chọn **chặn trước khi push** thay vì chỉ báo sau khi push: báo sau (Actions) hiện dấu ✗ trên repo nhưng bài sai đã lên rồi và học viên dễ không để ý; chặn ở pre-push đưa lỗi ra đúng lúc học viên đang chủ động nộp. Đây là giả định, sẽ kiểm trong pilot bằng số lỗi lọt lên repo.

**Vì sao không lên Workflow:** sau kiểm chứng, problem đã thu hẹp về lỗi định dạng, vốn có đúng/sai rõ. Phần kiểm nội dung theo rubric chưa có tiêu chí đạt/không đạt đủ rõ để đánh giá AI (dấu hiệu nên chọn Not Yet cho phần đó).

### 6.3. AI Canvas rút gọn

Không điền vì nhóm chọn Rule. Bài toán không cần AI dự đoán hay tạo nội dung: mọi quy định cần kiểm đều có đúng/sai rõ, Rule xử lý được cả 3 lỗi đã ghi nhận ở Day 02, và đầu ra mong muốn là một danh sách lỗi cố định chứ không phải nội dung mới. Thêm AI chỉ thêm chi phí và kiểu sai mới (báo "đúng" khi sai).

### 6.4. Hai câu hỏi của Google PAIR

Không áp dụng vì không có bước AI. Với giải pháp Rule, nhóm vẫn xét kiểu sai:

- **Augment hay automate:** học viên vẫn tự sửa và tự nộp; bộ kiểm chặn và báo lỗi nhưng không sửa hộ (augment). Lý do: quy định "không viết hộ" và mỗi người phải commit bằng tài khoản của mình.
- **Báo nhầm hay bỏ sót tệ hơn:** **bỏ sót** tệ hơn trong điều kiện bình thường, vì lỗi lọt qua là bị trừ điểm thật. Nhưng khi đã có rào cản thì **chặn nhầm sát deadline** còn tệ hơn cả bỏ sót, vì không push được thì bài không được chấm. Thiết kế: rule viết theo hướng chặt để không bỏ sót, mỗi lỗi kèm trích dẫn file đề gốc; đồng thời học viên luôn vượt rào được bằng `git push --no-verify`.

---

## 7. Problem Statement v1 + tiêu chí đánh giá (CP6)

| Trường | Nội dung |
|---|---|
| **Actor** | Học viên AI20K làm lab cá nhân và nhóm trên repo GitHub, nộp link repo qua LMS |
| **Quy trình** | Đọc checklist "Phải nộp gì" → bật rào cản (1 lần/repo) → đọc file chi tiết khi cần → làm bài, commit → push, hook kiểm trên máy (sai thì chặn, đúng thì nhắc) → sửa, push lại → Actions kiểm lại trên repo → tự đối chiếu nội dung với rubric → nộp (mục 4.2) |
| **Bottleneck** | Bước tự rút quy định nộp bài từ 11 file/1.325 dòng (không đổi so với v0) |
| **Impact** | Mỗi lỗi tên repo/file có nguy cơ bị trừ 5 điểm; Day 02: 3 lỗi định dạng trong 1 repo nhóm 4 người; lỗi phát hiện muộn kéo theo sửa gấp sát giờ |
| **Success Metric** (baseline → target, cách đo) | (1) Số lỗi định dạng còn trong repo tại commit cuối trước deadline: 3/repo → 0. (2) Thời điểm phát hiện lỗi: sát deadline → ngay lần push đầu sau khi lỗi phát sinh. (3) Số lần bộ kiểm chặn nhầm: chưa có → tối đa 1 lần/lab, 0 lần trong 1 giờ trước deadline. (4) Số lần push lên repo bị Actions báo lỗi (tức là đã vượt rào hoặc chưa bật hook): chưa có → 0. Cách đo: log GitHub Actions + thành viên báo lại mỗi lần bị chặn nhầm + đếm tay theo checklist tại commit cuối, 3 lab tiếp theo |
| **Boundary** | Bộ kiểm được chặn push khi sai quy cách nhưng không đổi tên, không sửa file, không tự commit, không chấm nội dung. File đề là quy định chính thức khi có khác biệt. Học viên tự quyết định sửa gì và luôn được vượt rào bằng `git push --no-verify`; nộp được bài trước deadline được ưu tiên hơn đúng quy cách |
| **AI intervention point** | Không có. Lý do: mọi quy định cần kiểm có đúng/sai rõ, Rule xử lý được cả 3 lỗi đã ghi nhận |
| **Mức chọn** | Rule: rào cản pre-push + Actions kiểm lại (kèm checklist No AI làm nền) |
| **Rủi ro & người kiểm tra** | Chặn nhầm sát deadline → học viên vượt rào bằng `--no-verify`, báo nhóm trưởng sửa rule; rule lỗi thời khi đề sửa sát giờ → nhóm trưởng đối chiếu lại rule với file đề mỗi khi đề có commit mới; thành viên quên bật hook → Actions bắt lại trên repo, nhóm trưởng nhắc trong chat nhóm; học viên coi "qua được rào" là đủ → lời nhắc khi push ghi rõ bộ kiểm không kiểm nội dung, bước đối chiếu rubric vẫn do học viên làm |

**Thay đổi so với v0 và lý do:**

| Trường | v0 | v1 | Vì sao đổi |
|---|---|---|---|
| Success Metric | 2 chỉ số, đếm tay tại commit cuối | Thêm (3) số lần chặn nhầm và (4) số push sai quy cách lọt lên repo; cách đo thêm log GitHub Actions | Khi đã chọn Rule có rào cản thì phải đo cả kiểu sai mới của giải pháp (chặn nhầm) và chỗ rào cản bị bỏ qua, không chỉ đo lỗi của học viên |
| Boundary | Giới hạn chung cho mọi công cụ | Bộ kiểm được chặn push nhưng không sửa gì; học viên luôn được vượt rào; nộp được bài ưu tiên hơn đúng quy cách | Rào cản có thể cản học viên nộp bài, nên phải ghi rõ ai có quyền vượt rào và khi nào |
| Quy trình | 6 bước hiện tại | 9 bước tương lai: rào cản trên máy + kiểm lại trên repo | Chỉ báo sau khi push thì bài sai đã lên repo; chặn trước khi push đưa lỗi ra đúng lúc học viên đang nộp |

**Tiêu chí đánh giá đầu ra của giải pháp Rule (3–5 tiêu chí):**

| # | Tiêu chí | Đạt khi | Không đạt khi |
|---:|---|---|---|
| 1 | Không bỏ sót | Bắt được 100% lỗi trong bộ test dựng từ lỗi thật: repo tên `Day02`, tiêu đề còn `MSSV_HoTen`, MSSV thiếu tiền tố `2A`, file báo cáo thiếu mục bắt buộc | Lọt bất kỳ lỗi nào trong bộ test |
| 2 | Không chặn nhầm | Repo và file đúng chuẩn thì luôn push được; tối đa 1 lần chặn nhầm/lab trong pilot, 0 lần trong 1 giờ trước deadline | Chặn push trên file đúng chuẩn từ 2 lần/lab trở lên, hoặc chặn nhầm sát deadline |
| 3 | Báo lỗi và nhắc nhở dễ hiểu | Mỗi lỗi ghi rõ file nào, vi phạm quy định nào, trích dẫn dòng trong file đề gốc; khi đúng quy cách vẫn in lời nhắc các mục nội dung chưa được kiểm | Chỉ báo "failed" mà không nói sai ở đâu; hoặc qua rào mà không có lời nhắc nội dung |
| 4 | Chặn kịp thời, không cản nộp bài | Hook chạy xong trong < 10 giây khi push; `git push --no-verify` luôn vượt được rào; Actions có kết quả trong < 2 phút | Hook chạy lâu làm học viên tắt hẳn; không có cách vượt rào khi bộ kiểm sai |
| 5 | Theo kịp đề | Khi đề có commit sửa quy định nộp bài, rule được cập nhật trước khi lab bắt đầu | Rule kiểm theo quy định cũ đã bị sửa |

---

## 8. Quyết định (CP6)

### 8.1. Bốn rủi ro

| Rủi ro | Câu hỏi | Mức độ rủi ro (Thấp = an toàn / TB / Cao = nguy hiểm) | Lý do / bằng chứng |
|---|---|---|---|
| **Value** | Người dùng có thật sự cần và sẽ dùng không? | TB | Lỗi định dạng xảy ra thật ngay trong nhóm (3 lỗi ở Day 02, 2 lỗi xảy ra dù template đã ghi rõ yêu cầu). Chưa có phỏng vấn nhóm khác nên chưa biết pain có phổ biến cả lớp không |
| **Usability** | Người dùng có dùng được, có hiểu và sửa được đầu ra của AI không? | TB | Lỗi hiện ngay lúc push, chỉ rõ file và quy định nên tự sửa được. Nhưng hook không tự đi theo repo: mỗi người phải tự chạy 1 lệnh bật trên máy mình, quên bật thì rào cản không có tác dụng; người mới bị chặn push lần đầu dễ bối rối |
| **Feasibility** | Có đủ dữ liệu, công cụ, kỹ năng để làm không? | Thấp | Git hỗ trợ sẵn hook pre-push (exit khác 0 là hủy push) và `core.hooksPath` để dùng chung thư mục hook trong repo; GitHub Actions, ls-lint có Action chính thức (mục 3.3); runner chuẩn miễn phí cho repo public. Cần thêm thời gian viết script, ước tính vài giờ, chưa làm thử |
| **Viability** | Có hợp chi phí, pháp lý, quy định tổ chức không? Ai vận hành? | TB | Trong repo nhóm: nhóm trưởng vận hành, không tốn phí. Muốn đưa vào repo đề cho cả lớp thì cần ban tổ chức đồng ý (giả định #5, chưa hỏi); đề sửa sát giờ nên phải có người cập nhật rule mỗi lab |

### 8.2. Kết luận

**Quyết định:** **Go, phạm vi nhỏ** — dùng Rule (rào cản pre-push + Actions kiểm lại + checklist), **không dùng AI**.

**Lý do:** không rủi ro nào ở mức Cao; problem đã thu hẹp về lỗi định dạng có đúng/sai rõ; công cụ Rule có sẵn và miễn phí; bằng chứng cho thấy checklist đơn thuần (No AI) đã không đủ. Value và Usability còn ở mức TB (chưa phỏng vấn nhóm khác; mỗi người phải tự bật hook), nên pilot giới hạn trong repo nhóm trước khi đề xuất cho cả lớp.

**Nếu Go — pilot nhỏ nhất:** trong repo nhóm NhanToBiAn, 3 lab tiếp theo: (1) checklist "Phải nộp gì" ở đầu README nhóm, mỗi dòng trích dẫn file đề; (2) thư mục `.githooks/` chứa hook `pre-push` kiểm 4 quy định (tên repo, tên file `MSSV_HoTen.md`, tiêu đề khớp tên file, đủ các mục bắt buộc và không trống): sai thì chặn, đúng thì in lời nhắc phần nội dung; mỗi thành viên chạy `git config core.hooksPath .githooks` một lần; (3) 1 workflow GitHub Actions chạy lại cùng 4 phép kiểm trên repo làm lưới an toàn. Nhóm trưởng phụ trách cập nhật rule khi đề sửa.

**Nếu Not Yet — cần kiểm chứng gì trước:** áp dụng cho phần **kiểm nội dung theo rubric** (Workflow có AI): cần phỏng vấn 2–3 học viên nhóm khác (mục 3.2) và viết được tiêu chí "mục đủ ý" trước khi cân nhắc.

**Nếu No-Go — nên làm gì thay AI:** áp dụng cho việc dùng AI ở phần định dạng: không cần, Rule đã đủ.

**Ngưỡng dừng:** nếu có lần nào hook chặn nhầm khiến thành viên không push được trong 1 giờ trước deadline, hoặc chặn nhầm từ 2 lần/lab trở lên, thì **bỏ chặn**, chuyển hook về chế độ chỉ nhắc (cảnh báo nhưng vẫn cho push). Nếu sau 3 lab mà vẫn còn lỗi định dạng lọt tới commit cuối, thì quay về checklist tick tay + 1 thành viên soát chéo trước deadline 1 giờ. Nếu phỏng vấn cho thấy nhóm khác không gặp lỗi định dạng, giữ pilot trong nhóm, không đề xuất cho cả lớp.

---

## 9. Hạn chế và hướng tiếp theo

- Chưa phỏng vấn học viên nhóm khác; Value đang dựa trên bằng chứng trong nhóm (1 repo, 4 file báo cáo, git log của thành viên).
- Baseline 3 lỗi/repo đếm trên 1 repo của 1 lab, mẫu nhỏ.
- Thời gian đọc đề chưa bấm giờ thật; ước tính lệch nhau giữa 2 thành viên (15 và 35 phút/lab).
- Phần đối chiếu nội dung bài với rubric chưa giải, vẫn là bottleneck sau khi có bộ kiểm; hướng tiếp theo là viết tiêu chí "mục đủ ý" rồi cân nhắc Workflow có AI.
- Hướng khác đáng làm tiếp: #7 Thủ tục hành chính lần đầu (Duy), sau khi có số liệu thật.

## 10. Tài liệu tham khảo

- [GitHub Docs — Use autograding (GitHub Classroom)](https://docs.github.com/en/education/manage-coursework-with-github-classroom/teach-with-github-classroom/use-autograding)
- [GitHub Docs — Actions quickstart](https://docs.github.com/en/actions/writing-workflows/quickstart)
- [GitHub Docs — About billing for GitHub Actions](https://docs.github.com/en/billing/managing-billing-for-your-products/managing-billing-for-github-actions/about-billing-for-github-actions)
- [ls-lint](https://ls-lint.org/) · [ls-lint GitHub Action](https://github.com/ls-lint/action)
- [Git — githooks (pre-push, core.hooksPath)](https://git-scm.com/docs/githooks) · [Git — git-push (--no-verify)](https://git-scm.com/docs/git-push)
- Rob Fitzpatrick — *The Mom Test*; David Bland — *Testing Business Ideas* (Assumption Map); Teresa Torres — Opportunity Solution Tree; Jeff Gothelf — *Lean UX*; Google PAIR Guidebook; Anthropic — *Building Effective Agents*; Marty Cagan (SVPG) — 4 rủi ro (theo [docs/01-worksheet.md](../../docs/01-worksheet.md))
- Git log các repo lab Day 01, Day 02 của thành viên nhóm; lịch sử commit repo đề Day 02
