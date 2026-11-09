# Báo cáo nhóm — Day 02 Discovery & Problem Framing

> Bản chung của nhóm, viết trên repo do nhóm trưởng fork. Không copy file này sang repo cá nhân.
> Template chi tiết và prompt mẫu: [docs/01-worksheet.md](../../docs/01-worksheet.md). Bài mẫu: [docs/02-deliverable-example.md](../../docs/02-deliverable-example.md).

## 1. Thông tin nhóm

- Tên nhóm: NhanToBiAn
- Thành viên: xem `TEAM.md`
- Candidate problem được chọn (1 câu): Học viên bỏ sót quy định nộp bài (tên repo, tên file, tiêu đề, mục bắt buộc) nằm rải rác ở nhiều file và chỉ phát hiện khi đã sát deadline
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
| 1 | Học viên khác cũng nộp sát deadline vì phát hiện thiếu sót muộn, không chỉ riêng một người | Value | 5 | 2 | ✅ |
| 2 | Lỗi bị trừ điểm chủ yếu là lỗi định dạng (tên file, tên repo, tiêu đề) do bỏ sót quy định, không phải do thiếu nội dung | Value | 5 | 2 | ✅ |
| 3 | Nộp muộn là do không biết bài còn thiếu gì, không phải do bắt đầu làm muộn | Value | 4 | 1 | ✅ |
| 4 | Quy định nộp bài giữa các lab đủ giống nhau để dùng chung một checklist hoặc một bộ kiểm tra | Feasibility | 4 | 3 | — |
| 5 | Ban tổ chức sẵn sàng thêm checklist hoặc bước kiểm tra tự động vào repo đề | Viability | 3 | 1 | Hỏi coach sau lab |

Giả định nhóm kiểm chứng trong buổi này: #1, #2, #3 (quan trọng cao, bằng chứng thấp).

### 3.2. Kiểm chứng

Cách đã dùng:

1. **Log** (git log của các repo lab và artefact trong repo nhóm): hành vi đã xảy ra, ghi theo vai trò, không ghi tên.
2. **Phỏng vấn nhanh 2–3 học viên nhóm khác** theo The Mom Test, mỗi buổi ~5'. Không phỏng vấn thành viên nhóm mình.

**Bộ câu hỏi phỏng vấn** (chỉ hỏi về hành vi đã xảy ra, không có câu "Bạn có muốn…" / "Bạn có dùng… không nếu…"):

| # | Câu hỏi | Kiểm giả định |
|---:|---|---|
| 1 | Lab gần nhất bạn nộp là lab nào? Bạn commit bản cuối lúc mấy giờ? (mở git log cùng xem nếu được) | #1 |
| 2 | Kể lại từ lúc mở đề tới lúc nộp: bạn làm những bước nào? | #3 |
| 3 | Lần gần nhất bạn phát hiện bài còn thiếu hoặc sai một quy định nộp bài là khi nào? Thiếu cái gì? Phát hiện lúc mấy giờ, bằng cách nào? | #1, #2 |
| 4 | Bạn đã từng bị trừ điểm hoặc phải sửa gấp vì tên repo, tên file, tiêu đề hay thiếu mục chưa? Chuyện gì đã xảy ra? | #2 |
| 5 | Trước khi nộp, bạn tự kiểm tra bài bằng cách nào? Mất khoảng bao lâu? | Workaround hiện tại |
| 6 | Lần đó bạn bắt đầu làm lúc mấy giờ? | #3 (phân biệt "bắt đầu muộn" với "phát hiện thiếu muộn") |

**Interview snapshot:** *Chờ nhóm điền sau khi phỏng vấn thật. Mỗi buổi ghi một bảng ngay sau khi xong; nếu chưa phỏng vấn kịp, để trống và ghi rõ là chưa thực hiện, không được điền số liệu giả định.*

**Snapshot 1**

| Trường | Nội dung |
|---|---|
| Người được hỏi (vai trò, không ghi tên thật) | |
| Câu nói đáng nhớ nhất (nguyên văn) | |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? | |
| Hiện đang xử lý bằng cách nào (workaround)? | |
| Mất bao lâu, bao lần? | |
| Insight / opportunity rút ra | |

**Snapshot 2**

| Trường | Nội dung |
|---|---|
| Người được hỏi (vai trò, không ghi tên thật) | |
| Câu nói đáng nhớ nhất (nguyên văn) | |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? | |
| Hiện đang xử lý bằng cách nào (workaround)? | |
| Mất bao lâu, bao lần? | |
| Insight / opportunity rút ra | |

**Snapshot 3** (tùy chọn)

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
| Git log repo nhóm lab Day 02 codelab (07/11/2026) — commit nội dung cuối của từng thành viên | 5 học viên | 3/5 thành viên commit nội dung cuối sau 21h (21:05, 21:28, 22:22); 1 thành viên commit "fix" lúc 22:22, merge bản cuối lúc 22:28 | 2/5 thành viên xong trước 15h30 (13:07, 15:20) → nộp sát giờ không xảy ra với mọi người; có thể phụ thuộc thời điểm bắt đầu (giả định #3) |
| Git log lab Day 01 AI Foundation, cá nhân (06–07/11/2026) | 1 học viên | Lưu notebook 12 lần từ 20:46 tới 00:22; commit "submit day 1 lab" lúc 00:19 ngày 07/11, sau mốc 23h59 | Mới có 1 người, chưa đủ kết luận cho cả lớp |
| Lịch sử commit repo đề Day 02 (08–09/11/2026) | 12 commit | Đề được sửa 12 commit trong ~14 giờ trước lab, có commit "Fix grading-rule conflicts", "Sua cac cho chua nhat quan trong de bai" → quy định thay đổi sát giờ (Opportunity C) | Các sửa đổi nhằm làm đề nhất quán hơn, không phải đổi yêu cầu nộp bài |
| Artefact trong repo nhóm hôm nay (09/11/2026) | 1 repo, 4 file báo cáo cá nhân | Repo nhóm ban đầu đặt tên `Day02` thay vì `DAY02` (sai mẫu, −5 điểm), phải đổi trong buổi; 2/4 file báo cáo cá nhân có dòng tiêu đề chưa khớp tên file dù template yêu cầu "Sửa cả dòng tiêu đề phía trên cho khớp" → lỗi định dạng xảy ra ngay cả khi đã đọc đề (giả định #2) | Lỗi được phát hiện và sửa trước deadline; chưa biết có lỗi nào lọt tới lúc chấm |
| Phỏng vấn học viên nhóm khác (snapshot 1–3) | *chờ điền* | *Điền sau khi phỏng vấn* | *Điền sau khi phỏng vấn* |
| Ước tính thời gian đọc đề trong báo cáo CP1 | 2 thành viên | Cả 2 đều coi việc tìm quy định nộp bài trong nhiều file là bước khó nhất | Ước tính lệch nhau nhiều (15' và 35'/lab) → thời gian đọc đề không phải pain chắc chắn |

**Nhóm đã sửa problem thế nào sau kiểm chứng:**

- **Trước kiểm chứng:** "Đọc đề lab nhiều file mất thời gian" (nhấn vào thời gian đọc).
- **Sau kiểm chứng:** thu hẹp thành **"bỏ sót quy định nộp bài (tên repo, tên file, tiêu đề, mục bắt buộc) và chỉ phát hiện khi đã sát deadline"**. Lý do: log cho thấy lỗi định dạng xảy ra thật ngay trong nhóm (tên repo, tiêu đề file), trong khi thời gian đọc đề giữa các thành viên lệch nhau nhiều và chưa chắc là pain.
- **Giả định #3 chưa được xác nhận:** 2/5 học viên ở lab Day 02 codelab xong sớm, nên nộp muộn có thể do bắt đầu muộn. Nhóm không dùng "nộp muộn" làm metric chính; metric chính chuyển sang **số lỗi định dạng phát hiện trước khi nộp**.

### 3.3. Research giải pháp đã có

| Công cụ / case / pattern | Link | Giải bước nào trong quy trình? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| GitHub Classroom autograding | https://docs.github.com/en/education/manage-coursework-with-github-classroom/teach-with-github-classroom/use-autograding | Bước tự kiểm trước khi nộp: chạy test mỗi lần học viên push, học viên xem kết quả và sửa | Đúng pattern "kiểm tự động ngay khi push", học viên thấy lỗi trước deadline | Trang tài liệu ghi GitHub Classroom **ngừng hoạt động từ 28/08/2026**; lab này không dùng Classroom mà dùng repo fork | Ý tưởng đúng nhưng công cụ đã ngừng → phải dùng thứ còn hoạt động (GitHub Actions) |
| GitHub Actions (workflow chạy khi push) | https://docs.github.com/en/actions/writing-workflows/quickstart · https://docs.github.com/en/billing/managing-billing-for-your-products/managing-billing-for-github-actions/about-billing-for-github-actions | Bước kiểm tên file, cấu trúc thư mục, mục bắt buộc: workflow trong `.github/workflows` tự chạy khi push (`on: [push]`), chạy được lệnh shell (`run:`) | Runner chuẩn của GitHub miễn phí cho repo public (theo trang billing); chạy ngay trên repo fork; không cần AI | Phải có người viết và bảo trì script; chỉ kiểm được thứ có quy tắc rõ (tên, cấu trúc, mục có hay không), không đánh giá được chất lượng nội dung | Phần lớn lỗi bị trừ điểm (tên repo, tên file, tiêu đề, thiếu file) là **Rule**, kiểm được bằng script |
| ls-lint (+ GitHub Action chính thức) | https://ls-lint.org/ · https://github.com/ls-lint/action | Bước kiểm tên file và thư mục theo quy ước khai báo trong `.ls-lint.yml` | Công cụ có sẵn, cấu hình một file, có GitHub Action chính thức | Chỉ kiểm tên file/thư mục, không kiểm tên repo hay nội dung trong file | Không cần tự viết từ đầu phần kiểm tên file; kết hợp với checklist cho phần nội dung |

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

| Bước | Actor | Input | Output | Thời gian / tần suất | Ghi chú |
|---:|---|---|---|---|---|
| 1 | Học viên | README của đề | Nắm mục tiêu lab | 2–5' / mỗi lab | |
| 2 | Học viên | RULES, CHECKPOINTS, RUBRIC, SUBMISSION, worksheet | Biết các bước và tiêu chí chấm | 11–18' / mỗi lab | Đề Day 02: 11 file, 1.325 dòng |
| 3 | Học viên | Các file ở bước 2 + template báo cáo | Danh sách tự ghi "phải nộp gì, đặt tên thế nào" (thường chỉ trong đầu) | 2–10' / mỗi lab | Ước tính lệch nhau giữa Bảo (~15' cả bước 1–3) và Ba (~35') |
| 4 | Học viên / nhóm | Đề + danh sách ở bước 3 | Bài làm | Phần lớn buổi lab | |
| 5 | Học viên | Bài làm + RUBRIC | Danh sách mục còn thiếu, bài đã sửa | ~60' (ước tính), lặp nhiều vòng | Day 01: 12 lần lưu từ 20:46 tới 00:22 |
| 6 | Học viên | Bài đã sửa | Commit + link nộp LMS | 5–10' / mỗi lab | Day 01: commit nộp 00:19; Day 02 codelab: 3/5 thành viên commit cuối sau 21h |

**Bottleneck chính:** Bước 3, tự rút quy định nộp bài từ 11 file. Bước này không lâu (2–10') nhưng là chỗ sinh ra lỗi: quy định nào bị bỏ sót ở đây thì không có bước nào kiểm lại một cách có hệ thống, chỉ lộ ra khi tự soát bằng mắt ở bước 5–6, sát deadline. Bằng chứng: repo nhóm đặt sai `Day02`, 2/4 file báo cáo cá nhân có tiêu đề chưa khớp tên file (mục 3.2).

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
