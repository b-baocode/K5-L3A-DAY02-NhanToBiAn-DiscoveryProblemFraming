# Team

> Điền file này trên repo chung do nhóm trưởng fork. Nhóm điền phần **Thông tin nhóm** và **Thành viên**. Mỗi người tự điền phần của mình trong **Cá nhân**. Không copy file này sang repo khác.

## Thông tin nhóm

- Tên nhóm: NhanToBiAn
- Candidate problem nhóm chọn (1 câu): Học viên bỏ sót quy định nộp bài (tên repo, tên file, tiêu đề, mục bắt buộc) nằm rải rác ở nhiều file và chỉ phát hiện khi đã sát deadline
- Quyết định cuối (Go / Not Yet / No-Go): Go, phạm vi nhỏ — Rule (rào cản pre-push + Actions kiểm lại + checklist), không dùng AI

## Thành viên

| STT | Họ và tên        | MSSV        | Vai trò trong nhóm | Tài khoản GitHub |
| --: | ---------------- | ----------- | ------------------ | ---------------- |
|   1 | Ngô Gia Bảo      | 2A202603482 | Nhóm trưởng, điều phối, phụ trách kiểm chứng và research | b-baocode        |
|   2 | Nguyễn Văn Ba    | 2A202603489 | Vẽ quy trình, viết Problem Statement | xtraiter         |
|   3 | Nguyễn Quang Duy | 2A202603462 |                    | nduy120505       |
|   4 | Nguyễn Thị Dung  | 2A202603508 |                    | zoesayhii        |

Không ghi email hay số điện thoại vào bảng này, vì repo có thể để public.

Gợi ý vai trò (một người có thể giữ nhiều vai): điều phối thời gian, ghi chép, người phản biện chính, phụ trách kiểm chứng (phỏng vấn/survey), phụ trách research, vẽ quy trình, viết Problem Statement.

## Phân công theo checkpoint

| Checkpoint                                 | Người chính | Người hỗ trợ | Sản phẩm                                       |
| ------------------------------------------ | ----------- | ------------ | ---------------------------------------------- |
| CP3 — Hội tụ nhóm                          | Ngô Gia Bảo |              | Cluster, cây OST, bảng chấm điểm               |
| CP4 — Kiểm chứng                           | Ngô Gia Bảo |              | Assumption map, snapshot hoặc survey           |
| CP4 — Research                             | Ngô Gia Bảo |              | Bảng research có link                          |
| CP5 — Quy trình trước/sau                  | Nguyễn Văn Ba |              | Quy trình + bảng before/after                  |
| CP5 — Problem Statement v0                 | Nguyễn Văn Ba |              | Problem Statement v0                           |
| CP6 — Mức can thiệp + Problem Statement v1 | Nguyễn Văn Ba |              | Ma trận, AI Canvas, eval, Problem Statement v1 |
| CP6 — Quyết định                           | Nguyễn Văn Ba |              | 4 rủi ro + Go/Not Yet/No-Go                    |

## Cá nhân

Mỗi thành viên thêm một mục theo mẫu dưới đây, tiêu đề là `HoVaTen-MSSV`.

### NgoGiaBao-2A202603482

**Phần việc phụ trách:**

- Nhóm trưởng: tạo repo chung, điều phối nhóm
- CP1–CP2 cá nhân: scan problem, viết Problem Card kèm quy trình nháp
- CP3: dẫn buổi hội tụ nhóm
- CP4: kiểm chứng và research

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- CP3: tổng hợp pitch, gom cluster, dựng cây OST và bảng chấm điểm shortlist trong `group_report.md`
- CP4: soạn bộ câu hỏi phỏng vấn, mẫu snapshot và bổ sung nguồn research cho `group_report.md`
- Viết ghi chú research CP4 riêng: `report/assets/cp4-research-ho-tro-su-co-tu-doi-pin.md`
- Phát hiện repo nhóm đặt tên `Day02` sai mẫu `DAY02` và đổi tên trong buổi lab

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- `report/individual/2A202603482_NgoGiaBao.md`
- `report/assets/cp4-research-ho-tro-su-co-tu-doi-pin.md`
- Commit "CP3: pitch, cluster, OST va cham diem shortlist"
- Commit "CP4: bo cau hoi phong van, mau snapshot, bo sung nguon research"
- Commit "Add CP1-CP2 individual report and CP4 research notes (NgoGiaBao)"

**Điều mình học được từ phần nhóm:**

- Cách làm việc nhóm: phân công theo checkpoint, mỗi người làm phần của mình rồi gộp vào báo cáo chung
- Cách research thông tin: tìm nguồn có link và ngày đăng, tự mở lại từng nguồn để kiểm trước khi đưa vào báo cáo

### NguyenVanBa-2A202603489

**Phần việc phụ trách:**

- CP1–CP2 cá nhân: scan 5 problem, viết 3 Problem Card kèm quy trình nháp
- Pitch 3 card trong buổi hội tụ nhóm (CP3)

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Đưa ra 3 candidate: đọc đề lab mất thời gian, quên mật khẩu mạng nội bộ, shipper giao chậm ở tỉnh
- Candidate "Đọc đề lab mất thời gian" được gộp vào cluster A và trở thành một phần của candidate nhóm chọn; quy trình 5 bước, bottleneck ở bước đối chiếu qua lại 6–7 file và baseline 35 phút được dùng làm bằng chứng cho Opportunity A trong cây OST
- Candidate "Quên mật khẩu" lọt vào shortlist 3 candidate ở bảng chấm điểm

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- `report/individual/2A202603489_NguyenVanBa.md` mục 2 và 3
- `group_report.md` mục 2.1 (dòng #4, #5, #6), mục 2.2 (cluster A, C, E), mục 2.3 (Opportunity A), mục 2.4 (shortlist #5)
- Commit "Them bao cao ca nhan CP1-CP2 - Nguyen Van Ba"

**Điều mình học được từ phần nhóm:**

-

### NguyenQuangDuy-2A202603462

**Phần việc phụ trách:**

- CP1–CP2 cá nhân: scan 5 problem, viết 3 Problem Card kèm quy trình nháp
- Pitch 3 card trong buổi hội tụ nhóm (CP3)

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Đưa ra 3 candidate: xử lí thủ tục hành chính, lọc cuộc gọi lừa đảo, tư vấn món ăn
- Candidate "Xử lí thủ tục hành chính lần đầu" lọt vào shortlist 3 candidate ở bảng chấm điểm

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- `report/individual/2A202603462_NguyenQuangDuy.md` mục 2 và 3
- `group_report.md` mục 2.1 (dòng #7, #8, #9), mục 2.2 (cluster B, D, E), mục 2.4 (shortlist #7)
- Commit "idea"

**Điều mình học được từ phần nhóm:**

-
