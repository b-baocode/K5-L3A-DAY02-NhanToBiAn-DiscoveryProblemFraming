# CP4 — Research: Hỗ trợ sự cố tại tủ đổi pin xe máy điện (V-Green / VinFast)

> Người thực hiện: Ngô Gia Bảo (2A202603482). Ngày kiểm link: 09/11/2026.
> Candidate lấy từ bài Day 01 của tôi (Quick Card #2). Research có dùng AI hỗ trợ tìm kiếm; **mọi link dưới đây đã được mở lại để kiểm nội dung**. Thông tin không mở được hoặc không kiểm được đã bị loại.
>
> ⚠️ Các con số trong bài Day 01 (20 phút/cuộc gọi, 300 cuộc gọi/ngày, 45% xử lý xong ngay lần đầu, ~40% hướng dẫn lần đầu không hiệu quả) là **ước tính do AI đưa ra, không có nguồn**. File này **không dùng** các con số đó làm bằng chứng. Baseline thật phải lấy từ kiểm chứng ở CP4.

---

## 1. Bài toán (Job Story, chưa có giải pháp)

**Bản Day 01 (actor = tổng đài viên):**
Khi khách gọi báo tủ đổi pin gặp lỗi, tổng đài viên muốn hiểu nhanh tủ đang bị gì và hướng dẫn đúng ngay lần đầu, để khách không phải đứng chờ lâu với xe sắp hết pin.

**Bản đề xuất cho Day 02 (actor = người đi đổi pin, dễ kiểm chứng hơn):**
Khi đến tủ đổi pin mà tủ báo lỗi, không nhả pin, hoặc không còn pin đầy, tôi muốn biết ngay phải làm gì tiếp (thử lại, sang tủ nào, gọi ai), để không bị kẹt giữa đường với xe sắp hết pin.

> Lý do đề xuất đổi actor: lab yêu cầu phỏng vấn **người thật đã gặp vấn đề**. Tổng đài viên V-Green rất khó tiếp cận trong 1 buổi; còn người dùng xe đổi pin (kể cả tài xế xe ôm điện) có thể hỏi được ngay. Nhóm tự quyết.

---

## 2. Bằng chứng công khai về pain (tín hiệu xác nhận và phản bác)

| # | Nguồn | Nội dung đã kiểm | Loại tín hiệu |
|---:|---|---|---|
| 1 | [Threads — bài đăng người dùng, 27/05/2026](https://www.threads.com/@adn.anh.duc.nguyen/post/DY2ZbnLganV/) | Lần đổi pin thứ 5, tại tủ ở Điện Máy Xanh 146 Kim Mã: tủ yêu cầu cắm lại nhưng không đẩy pin ra, khoảng 1 phút sau báo đèn đỏ và "nuốt" pin. Bài không nói đã xử lý thế nào | ✅ Xác nhận: sự cố tại tủ có thật, người dùng không biết bước tiếp theo |
| 2 | [Voz — "Bất cập hiện tại của xe đổi pin Vinfast", 03/04/2026](https://voz.vn/t/bat-cap-hien-tai-cua-xe-doi-pin-vinfast.1224732/) | Tủ báo "chưa sẵn sàng, vui lòng quét tủ khác"; trạm ở Cầu Giấy không còn pin đầy; phải **gọi tổng đài hỏi trạm gần nhất** và được chỉ tới trạm cũng hết pin; pin tụt từ 15% xuống 8% khi đi tìm tủ | ✅ Xác nhận: pain nằm ở **hết pin đầy + thông tin tủ thay thế sai**, không chỉ lỗi kỹ thuật |
| 3 | [Green SM — Hướng dẫn đổi pin trên tủ V-Green, 02/06/2026](https://www.greensm.com/vn-vi/news/green-sm-cung-v-green-huong-dan-doi-pin-xe-may-dien-tren-tu-doi-pin) | Khi thao tác đổi pin không thành công: liên hệ tổng đài **1900 232 389, nhấn phím 5** | ✅ Xác nhận: kênh xử lý sự cố hiện tại là **gọi tổng đài** |
| 4 | [Báo Đầu tư — Bắt đối tượng đập phá tủ đổi pin, 02/06/2026](https://baodautu.vn/tphcm-bat-doi-tuong-dap-pha-hang-loat-tu-doi-pin-xe-dien-vinfast-d610500.html) | Hơn 10 tủ ở TP.HCM bị đập màn hình và thiết bị từ cuối 4/2026; mỗi tủ sửa khoảng 14 triệu đồng | ⚠️ Gián tiếp: có những lỗi **không xử lý được từ xa**, bắt buộc phải cử kỹ thuật |
| 5 | [Mekong ASEAN — V-Green triển khai hơn 3.000 tủ tại PVOIL, 08/05/2026](https://mekongasean.vn/v-green-trien-khai-hon-3000-tu-doi-pin-xe-may-dien-tai-cay-xang-pvoil-54965.html) | Hơn 3.000 tủ tại gần 1.000 cây xăng PVOIL; mục tiêu 60.000 tủ trong Q2/2026. **Bài không nói tủ có nhân viên trực hay không** | ⚠️ Bối cảnh: quy mô lớn và tăng nhanh. Giả định "không người trực" **chưa có nguồn xác nhận trực tiếp** |
| 6 | [Tiền Phong — Người dùng đi xa nhờ tủ đổi pin, 02/07/2026](https://tienphong.vn/nguoi-dung-xe-may-dien-vinfast-di-xa-khong-phai-nghi-nho-he-thong-tu-doi-pin-phu-kin-post1856201.tpo) | Reviewer: đổi pin "chưa đầy 1 phút"; một người đi 116 km đổi 3 lần, không nhắc sự cố | ❌ **Phản bác:** với nhiều người, đổi pin trơn tru. Cần đo **tỷ lệ lượt đổi gặp sự cố** chứ không giả định là nhiều. (Lưu ý: bài mang tính quảng bá) |

**Kết luận từ bằng chứng công khai:**
- Có sự cố thật, nhưng **chỉ có giai thoại (2 bài người dùng)**, không có số liệu tần suất.
- Pain hay gặp nhất trong nguồn đã kiểm là **"tủ hết pin đầy / tủ chưa sẵn sàng → phải đi tìm tủ khác"**. Loại này nghiêng về **thông tin trạng thái tủ**, không phải "hiểu mô tả mơ hồ của khách". Điều này có thể làm đổi bottleneck so với bài Day 01.

---

## 3. Research giải pháp đã có (dùng cho mục 3.3 báo cáo nhóm)

| Công cụ / case / pattern | Link | Giải bước nào trong quy trình? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| **Gogoro Network app** (Đài Loan, mạng đổi pin lớn nhất thế giới cùng loại) | [App Store — Gogoro Network](https://apps.apple.com/app/id1463351156) | Bước khách gặp lỗi → báo sự cố: app có tra cứu xử lý sự cố, **chụp ảnh + ghi chú gửi hỗ trợ**, bản đồ GoStation, xem xu hướng sạc pin để chọn giờ đổi | Khách tự báo sự cố kèm ảnh, **không phải mô tả qua điện thoại**; hỗ trợ 24/7 | Mô tả trên App Store không nói rõ có hiện **số pin đầy theo thời gian thực** hay không | Nhiều phần pain giải được bằng **app + form báo lỗi có ảnh + trạng thái tủ (Rule/No AI)**, chưa cần AI |
| **Google Cloud Agent Assist** (knowledge assist, generative knowledge assist, tóm tắt cuộc gọi) | [Google Cloud docs — Agent Assist](https://docs.cloud.google.com/contact-center/ccai-platform/docs/agent-assist) | Bước tổng đài viên nghe mô tả → tra tài liệu → hướng dẫn: gợi ý bài hướng dẫn theo nội dung hội thoại theo thời gian thực, tóm tắt cuộc gọi khi kết thúc | Đúng pattern "AI gợi ý, **người quyết định chia sẻ gì**" ("An agent can examine the suggestions and decide which to share"); có sẵn, không phải tự xây | **Bắt buộc có knowledge base** ("You must create a knowledge base to use knowledge assist"); cấu hình IAM phức tạp; chưa kiểm hỗ trợ tiếng Việt | Không nên tự xây. Việc phải làm trước là **chuẩn hóa tài liệu mã lỗi + danh mục thao tác**. Đây là việc No AI, có giá trị ngay |
| **Zendesk Copilot — Suggested first replies** | [Zendesk — Turning on suggested first replies](https://support.zendesk.com/hc/en-us/articles/8037936748570-Turning-on-suggested-first-replies) | Bước soạn hướng dẫn cho khách qua chat/email: ưu tiên **macro có sẵn**, rồi bài help center; kênh messaging có thể rơi về nội dung LLM tự sinh | Thứ tự **macro (Rule) → help center → LLM** là kiến trúc hay để học; agent được sửa hoặc từ chối | Kênh messaging có thể dùng nội dung LLM **không dựa trên help center** (rủi ro bịa); Zendesk thông báo **ngừng tính năng này từ 19/01/2027** | Mượn kiến trúc "Rule trước, AI sau, người duyệt". Phụ thuộc vào một tính năng sắp ngừng là rủi ro Viability |

**Kết luận research:**

```text
Phần lớn quy trình đã có pattern/công cụ giải được. Không có lý do tự xây agent.
1. Pain "hết pin đầy / tủ chưa sẵn sàng" → Rule/No AI: app hiển thị trạng thái tủ và tủ thay thế từ dữ liệu IoT (Gogoro làm theo hướng app).
2. Pain "báo lỗi qua điện thoại khó mô tả" → No AI: form báo lỗi trong app có mã tủ + ảnh.
3. Pain "tổng đài viên tra tài liệu lâu" → trước hết chuẩn hóa knowledge base mã lỗi (No AI);
   chỉ khi khối lượng cuộc gọi đủ lớn mới cân nhắc Workflow có AI gợi ý (kiểu Agent Assist), người duyệt.
```

Khác biệt so với bài Day 01: Day 01 chọn ngay "Rule + LLM" cho tổng đài viên. Research cho thấy **phần lớn pain có thể là Rule/No AI**, còn bước AI chỉ đáng làm khi có số liệu khối lượng cuộc gọi. Điều này khớp với quyết định NOT YET của Day 01.

---

## 4. Giả định cần kiểm chứng (gợi ý cho Assumption Map, mục 3.1)

| # | Giả định | Loại | Quan trọng | Đã có bằng chứng | Ghi chú |
|---:|---|---|---:|---:|---|
| 1 | Người đổi pin gặp sự cố tại tủ đủ thường xuyên (ví dụ ≥1 lần/tháng) | Value | 5 | 2 | 2 giai thoại online; 1 bài phản bác |
| 2 | Loại sự cố phổ biến nhất là hết pin đầy / tủ chưa sẵn sàng, không phải lỗi kỹ thuật phức tạp | Value | 5 | 2 | Nếu đúng → bài toán nghiêng về Rule |
| 3 | Khi gặp sự cố, người dùng không biết làm gì tiếp và phải gọi tổng đài | Value | 4 | 3 | Green SM ghi hotline; Voz có người gọi tổng đài |
| 4 | Tủ không có nhân viên trực để hỗ trợ tại chỗ | Feasibility / bối cảnh | 4 | 1 | **Chưa có nguồn chính thức**, phải hỏi người dùng thật |
| 5 | Dữ liệu trạng thái tủ (pin đầy, lỗi) có sẵn và cập nhật thời gian thực | Feasibility | 4 | 1 | Voz: tổng đài chỉ tới tủ cũng hết pin → có thể dữ liệu chưa tốt |

---

## 5. Gợi ý kiểm chứng (The Mom Test, không dùng AI để trả lời)

**Hỏi ai:** người đang đi xe máy điện đổi pin VinFast (bạn học, người quen); **tài xế xe ôm điện** (đặt một chuyến và hỏi trong lúc đi); không phỏng vấn thành viên nhóm.

**Câu hỏi (hỏi hành vi đã xảy ra):**
1. Lần gần nhất anh/chị đi đổi pin là khi nào? Kể lại từ lúc đến tủ.
2. Lần gần nhất đổi pin **không thành công** là khi nào? Chuyện gì đã xảy ra?
3. Lúc đó anh/chị đã làm gì? Thử lại, sang tủ khác, gọi tổng đài hay làm gì khác?
4. Mất bao lâu từ lúc gặp sự cố tới lúc đổi được pin? Pin còn bao nhiêu %?
5. Nếu đã gọi tổng đài: chờ bao lâu, được hướng dẫn gì, có xử lý được không?
6. Trong tháng vừa rồi, khoảng bao nhiêu lần đổi pin, bao nhiêu lần gặp trục trặc?
7. Hiện anh/chị làm gì để tránh chuyện đó (ví dụ: kiểm tra app trước, chỉ đổi ở tủ quen)?

**Tránh hỏi:** "Anh/chị có muốn app AI hướng dẫn xử lý lỗi không?", "Nếu có trợ lý ảo thì có dùng không?"

**Ghi cả tín hiệu phản bác:** nếu đa số nói "chưa bao giờ bị lỗi" hoặc "chỉ cần biết tủ nào còn pin", phải thu hẹp problem hoặc chọn No AI/Rule.

---

## 6. Hạn chế của research

- Không tìm được số liệu chính thức về tỷ lệ lỗi tủ, số cuộc gọi sự cố hay thời gian xử lý của V-Green.
- Bằng chứng người dùng chỉ có 2 bài đăng online, chưa đại diện.
- Chưa kiểm được Agent Assist có hỗ trợ tiếng Việt cho từng tính năng hay không.
- Chưa có nguồn chính thức xác nhận tủ "không người trực". Một số trang đại lý vẫn khuyên "liên hệ bộ phận hỗ trợ tại trạm".
