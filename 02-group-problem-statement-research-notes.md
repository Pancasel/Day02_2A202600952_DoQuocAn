# Day 02 Lab — Worksheet nộp bài

# 1 — Nhóm trao đổi vấn đề
# BÁO CÁO TỔNG HỢP: PHÂN TÍCH VÀ ĐÁNH GIÁ VẤN ĐỀ (PROBLEM SCANNING)

Dưới đây là bảng tổng hợp đánh giá ưu tiên giải quyết vấn đề (Top 3 Problems) từ các thành viên trong nhóm, kèm theo lý do lựa chọn và những yếu tố rủi ro/chưa chắc chắn cần lưu ý.

---

## 1. Thành viên: Đỗ Quốc An
**Case Study:** Đi làm trong dự án thực tế che logo không phù hợp

| Rank | Problem | Vì sao chọn | Điều chưa chắc |
| :---: | :--- | :--- | :--- |
| **1** | **Gắn nhãn & Sinh dữ liệu thủ công** | Workflow rất rõ ràng, là nút thắt ngốn nhiều thời gian nhất (2-3 ngày/đợt). Dễ dàng đo lường thành công bằng số giờ tiết kiệm được. | Chất lượng của dữ liệu nếu dùng Auto-labeling có đủ sạch và chuẩn để train tiếp không hoặc team test chưa chấp thuận với data được xử lí. |
| **2** | **Quy trình update logo mới** | Giải pháp chuyển đổi sang One-shot/Few-shot có thể mang lại đột phá thay vì finetune truyền thống các model yolo. | Trade-off giữa tốc độ update và độ chính xác có đáp ứng được yêu cầu khách hàng không. |
| **3** | **Tối ưu FPS cho Live Demo** | Tác động trực tiếp đến trải nghiệm thực tế và khả năng đáp ứng của hệ thống. | Rào cản phần cứng cố định có thể là giới hạn cứng, khó biết phần mềm có thể tối ưu luồng data thêm bao nhiêu % nữa. |

---

## 2. Thành viên: Nguyễn Khánh Linh
**Case Study:** Tối ưu hóa quy trình giao tiếp và cập nhật kỹ thuật nội bộ

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc chắn |
| :---: | :--- | :--- | :--- |
| **1** | **Viết update kỹ thuật cho stakeholder non-tech** | Workflow rõ, mất nhiều thời gian (45 phút/lần), có metric tốt. | Update "đủ rõ cho stakeholder" đo thế nào. |
| **2** | **Tóm tắt research paper cho weekly** | Có pain thật, lặp hằng tuần, AI có thể giúp đọc/kết nối với product context. | Quality "tóm tắt không lạc hướng" khó đo định lượng. |
| **3** | **Viết ticket bug AI cho BE/FE** | Nhiều người đau (AI Engineer + BE/FE), impact 2 chiều, lặp hằng ngày. | Mỗi bug context khác nhau, khó chuẩn hóa template. |

---

## 3. Thành viên: Trần Diệu Linh
**Case Study:** Tối ưu hóa định hướng và phương pháp học tập cho học sinh

| Rank | Problem | Vì sao chọn | Điều chưa chắc |
| :---: | :--- | :--- | :--- |
| **1** | **Học sinh học quá nhiều môn nhưng thiếu định hướng dài hạn và thực hành** | Đây là vấn đề ảnh hưởng đến số lượng lớn học sinh trong thời gian dài. Quy trình học hiện tại quá thiên về học thuộc lòng và thiếu cá nhân hóa nên tạo cơ hội rõ ràng cho AI hỗ trợ học tập thích ứng và định hướng nghề nghiệp cá nhân hóa. Thành công cũng dễ đo lường thông qua khả năng ghi nhớ, động lực học tập và mức độ áp dụng kiến thức thực tế. | AI có thực sự đưa ra định hướng phù hợp cho từng học sinh hay không. Ngoài ra việc cá nhân hóa học tập có thể khó triển khai nếu chương trình giáo dục vẫn quá tiêu chuẩn hóa và phụ thuộc nhiều vào thi cử truyền thống. |
| **2** | **Học sinh nhanh quên kiến thức sau khi thi** | Đây là vấn đề phổ biến và dễ nhìn thấy trong thực tế. AI có thể hỗ trợ nhắc lại ngắt quãng, bài tập thực tế và phương pháp gợi nhớ chủ động để tăng khả năng ghi nhớ dài hạn thay vì học ngắn hạn chỉ để thi. | Chưa chắc học sinh có duy trì thói quen học cùng AI lâu dài hay không. Ngoài ra cũng khó đo chính xác mức độ ghi nhớ nếu không theo dõi trong thời gian dài. |
| **3** | **Thiếu kết nối giữa môn học và nghề nghiệp tương lai** | Nhiều học sinh mất động lực vì không hiểu học để làm gì. AI có thể giúp liên kết kiến thức với nghề nghiệp thực tế và tạo lộ trình phát triển cá nhân rõ ràng hơn. | Chưa chắc AI hiểu đầy đủ thị trường lao động và mục tiêu thay đổi liên tục của học sinh. Gợi ý không phù hợp có thể khiến học sinh định hướng sai. |

---

## 4. Thành viên: Thân Minh Hiếu
**Case Study:** Các vấn đề trong quy trình phân tích yêu cầu và phối hợp phát triển (BA & Development)

| Rank | Problem | Vì sao chọn | Điều chưa chắc |
| :---: | :--- | :--- | :--- |
| **1** | **Chất lượng tài liệu yêu cầu kém (Thiếu tiêu chí nghiệm thu, yêu cầu mơ hồ, phải họp làm rõ kéo dài)** | Nhân viên phân tích viết yêu cầu không đủ chuẩn cho nhóm phát triển làm việc, gây ảnh hưởng trực tiếp đến chất lượng và tiến độ dự án. | Việc áp dụng template hay công cụ AI hỗ trợ viết tài liệu có giải quyết triệt để vấn đề không, hay nguyên nhân chính là do năng lực và thời gian của từng BA. |
| **2** | **Giao tiếp & phối hợp kém (Lập trình viên liên tục hỏi lại BA, quản lý giục tiến độ, họp hành nhiều)** | Luồng thông tin không rõ ràng, đứt gãy, dẫn đến việc phải hỏi đi hỏi lại nhiều lần làm lãng phí nguồn lực và thời gian của cả team. | Giải pháp cải thiện giao tiếp có thực sự tối ưu được quy trình không hay lại sinh ra thêm các bước quản lý cồng kềnh khác. |
| **3** | **Thiếu quy trình và tài liệu hướng dẫn ban đầu cho nhân viên mới (Onboarding)** | Nhân viên mới không có mẫu tài liệu chuẩn, thiếu người kèm cặp dẫn đến việc mất rất nhiều thời gian để đạt được mức hiệu suất (chuẩn) yêu cầu. | Bộ tài liệu và quy trình tạo ra có được team cập nhật thường xuyên để bám sát thực tế không, người mới có chủ động theo dõi hay vẫn phụ thuộc vào người kèm. |

# 2 — Nhóm thống nhất vấn đề

## Nhóm hội tụ

| Nhóm | Ví dụ ứng viên | Mẫu hình chung |
|---|---|---|
| Chất lượng yêu cầu | Tài liệu thiếu tiêu chí nghiệm thu, yêu cầu mơ hồ, họp làm rõ kéo dài | Nhân viên phân tích viết yêu cầu không đủ chuẩn cho nhóm phát triển làm việc |
| Giao tiếp / phối hợp | Lập trình viên hỏi lại nhân viên phân tích, người quản lý hỏi tiến độ, họp nhiều | Thông tin không rõ, phải hỏi lại nhiều lần |
| Hướng dẫn ban đầu | Nhân viên mới không có mẫu tài liệu, thiếu người kèm | Người mới mất lâu để đạt chuẩn |

## Danh sách rút gọn và chấm điểm

| Ứng viên | Người rõ | Luồng rõ | Đau có bằng chứng | Tác động đo được | Làm trong buổi | So sánh 3 mức được | Nhóm hiểu lĩnh vực | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Tài liệu chất lượng thấp | 5 | 5 | 5 | 5 | 5 | 5 | 5 | 35 |
| Họp làm rõ kéo dài | 4 | 4 | 4 | 4 | 4 | 3 | 4 | 27 |
| Hướng dẫn ban đầu thiếu chuẩn | 4 | 3 | 3 | 4 | 4 | 3 | 4 | 25 |

**Nhóm chọn: Tài liệu yêu cầu chất lượng thấp từ nhân viên phân tích non.**

**Vì sao chọn:**
- Có người gặp cụ thể (nhân viên phân tích non) và người chịu ảnh hưởng rõ (nhóm phát triển).
- Có luồng công việc rõ ràng với nhiều điểm nghẽn đo được.
- Tác động trực tiếp đến năng suất chu kỳ và tỉ lệ làm lại.
- Có thể so sánh 3 mức giải pháp: Quy tắc / Luồng công việc / Trợ lý tự động.

**Vì sao không chọn:**
- Họp làm rõ kéo dài: là hệ quả của tài liệu chất lượng thấp, giải quyết gốc tốt hơn.
- Hướng dẫn ban đầu: là giải pháp dài hạn, không phải phát biểu vấn đề cho buổi thực hành.

---

## Kiểm chứng nhanh

| Nguồn | Số người | Tín hiệu xác nhận | Tín hiệu phản bác | Nhóm sửa vấn đề thế nào |
|---|---:|---|---|---|
| Kinh nghiệm bản thân (lập trình viên) | 1 | Mỗi chu kỳ 3-5 lần hỏi đáp, 30% làm lại | Có thể do lập trình viên không hỏi đủ lúc họp | Thêm chất lượng họp làm rõ vào chỉ số |
| Hỏi lập trình viên khác | 2 | Cả 2 đều xác nhận làm lại do yêu cầu thiếu | 1 người nói do quản lý sản phẩm không phải nhân viên phân tích | Thu hẹp: cả nhân viên phân tích và quản lý sản phẩm đều có thể gặp |
| Nghiên cứu ngành | Nhiều bài báo | "Yêu cầu kém gây 30-40% làm lại" (IREB) | Số liệu khác nhau theo ngành | Dùng khoảng 20-40% thay vì con số cố định |

**Nhận insight sau kiểm chứng:**

```
Đau thật không nằm ở nhân viên phân tích "non kinh nghiệm"
mà nằm ở việc không có cửa kiểm chất lượng — tài liệu yêu cầu
được gửi cho lập trình viên mà không qua bước kiểm tra tự động
nào. Trí tuệ nhân tạo có thể đóng vai trò cửa kiểm chất lượng
trước khi tài liệu đến tay Trưởng nhóm kỹ thuật và nhóm phát triển.
```

## Nghiên cứu giải pháp đã có

| Nguồn / công cụ / trường hợp | Đường dẫn | Họ giải quyết phần nào? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| Hướng dẫn chất lượng yêu cầu IREB | https://www.ireb.org | Tiêu chuẩn cho tiêu chí chất lượng | Khung đã được chứng minh | Không có công cụ tự động kiểm tra | Dùng làm danh mục kiểm tra cho trí tuệ nhân tạo |
| Mẫu tài liệu Jira + Confluence | https://www.atlassian.com | Mẫu phiếu yêu cầu, tiêu chí nghiệm thu | Dễ dùng, phổ biến | Không tự động kiểm tra chất lượng | Mẫu là nền tảng, trí tuệ nhân tạo là cửa kiểm |
| ChatGPT/Gemini kiểm tra tài liệu | Công cụ chat trí tuệ nhân tạo | Có thể kiểm tra chữ, gợi ý cải thiện | Linh hoạt, rẻ | Không tích hợp luồng công việc, dễ quên dùng | Cần nhúng trí tuệ nhân tạo vào luồng, không dùng riêng lẻ |

**Nhận rút từ nghiên cứu:**

```
Không cần công cụ chuyên biệt. Mẫu hình hợp lý: dùng trí tuệ
nhân tạo như cửa kiểm chất lượng trong luồng công việc — nhân
viên phân tích viết tài liệu → trí tuệ nhân tạo tự động kiểm tra
theo danh mục (tiêu chí nghiệm thu, trường hợp phát sinh, từ ngữ
mơ hồ) → nhân viên sửa → trưởng nhóm xem lại → nhóm phát triển
nhận. Trí tuệ nhân tạo không thay nhân viên phân tích, trí tuệ
nhân tạo giúp nhân viên non viết tốt hơn nhanh hơn.
```

---

## Luồng công việc trước/sau

### Luồng hiện tại — Tài liệu yêu cầu chất lượng thấp

```
═══════════════════════════════════════════════════════════
 LUỒNG HIỆN TẠI — Vấn đề chất lượng tài liệu yêu cầu
═══════════════════════════════════════════════════════════

 ┌─────────────────┐
 │ 1. Quản lý giao │  5 phút
 │    tính năng    │
 └────────┬────────┘
          ▼
 ┌─────────────────────────┐
 │ 2. Nhân viên phân tích  │  60 phút
 │    tự nghiên cứu        │
 │    (không có hướng dẫn) │
 └────────┬────────────────┘
          ▼
 ┌──────────────────────────┐
 │ 3. Viết tài liệu yêu cầu │  120 phút
 └────────┬─────────────────┘
          ▼
 ┌──────────────────────────────┐      ╔══════════════════════╗
 │ 4. Trưởng nhóm kỹ thuật      │ 30'  ║  ĐIỂM NGHẼN SỐ 1     ║
 │    xem lại → TỪ CHỐI         │      ║  2-3 vòng xem lại    ║
 └──────────────┬───────────────┘      ╚══════════════════════╝
          KHÔNG ▼
     ┌───────────────────┐
     │ 5. Nhân viên phân │  90 phút (2-3 vòng)
     │    tích sửa lại   │
     └────────┬───────────┘
              ▼
 ┌──────────────────────────────┐
 │ 6. Họp làm rõ yêu cầu        │  120 phút
 │    (cả nhóm, yêu cầu mờ)     │
 └──────────────┬───────────────┘
                ▼
 ┌──────────────────────────────┐      ╔══════════════════════╗
 │ 7. Lập trình viên hỏi làm rõ │ 180' ║  ĐIỂM NGHẼN SỐ 2     ║
 │    trong chu kỳ              │      ║  3-5 lần/chu kỳ     ║
 └──────────────┬───────────────┘      ╚══════════════════════╝
                ▼
 ┌──────────────────────────┐
 │ 8. Lập trình viên code   │  30 phút
 │    → nhân viên xác nhận  │
 └──────────────┬───────────┘
        KHÔNG ỔN ▼
 ┌──────────────────────────────┐      ╔══════════════════════╗
 │ 9. LẬP TRÌNH VIÊN LÀM LẠI    │ 120' ║  ĐIỂM NGHẼN SỐ 3     ║
 │    (hiểu sai yêu cầu)        │      ║  khoảng 30% đầu việc ║
 └──────────────────────────────┘      ╚══════════════════════╝

 TỔNG: khoảng 10 giờ hỏi đáp + làm lại/chu kỳ
 3-5 lần hỏi đáp, 30% tỉ lệ làm lại
```

### Luồng tương lai — Cửa kiểm chất lượng bằng trí tuệ nhân tạo

```
═══════════════════════════════════════════════════════════
 LUỒNG TƯƠNG LAI — Cửa kiểm chất lượng bằng trí tuệ nhân tạo
═══════════════════════════════════════════════════════════

 ┌─────────────────┐
 │ 1. Quản lý giao │  5 phút
 │    tính năng    │
 └────────┬────────┘
          ▼
 ┌─────────────────────────────┐
 │ 2. Nhân viên nghiên cứu     │  45 phút
 │    (+ trí tuệ nhân tạo gợi  │  ← Trí tuệ nhân tạo hỗ trợ
 │     ý cấu trúc)             │
 └──────────────┬───────────────┘
                ▼
 ┌──────────────────────────────┐
 │ 3. Viết tài liệu yêu cầu     │  90 phút
 └──────────────┬───────────────┘
                ▼
 ┌──────────────────────────────┐      ╔══════════════════════╗
 │ 4. TRÍ TUỆ NHÂN TỰ ĐỘNG      │  2'  ║  BƯỚC TRÍ TUỆ NHÂN  ║
 │    KIỂM TRA TÀI LIỆU         │      ║  Cửa kiểm chất lượng │
 │  - Kiểm tra thiếu tiêu chí   │      ║  tự động             ║
 │    nghiệm thu                │      ║  Theo danh mục IREB  ║
 │  - Kiểm tra trường hợp phát  │      ╚══════════════════════╝
 │    sinh                      │
 │  - Kiểm tra từ ngữ mơ hồ     │
 │  - Gợi ý cải thiện           │
 └──────────────┬───────────────┘
                ▼
 ┌──────────────────────────────┐
 │ 5. Nhân viên sửa theo gợi ý  │  30 phút
 └──────────────┬───────────────┘
                ▼
 ┌──────────────────────────────┐      ╔══════════════════════╗
 │ 6. Trưởng nhóm xem lại       │ 15'  ║  NGƯỜI VẪN QUYẾT     ║
 │    → PHÊ DUYỆT               │      ║  Trưởng nhóm vẫn là  ║
 └──────────────┬───────────────┘      ║  người chốt cuối     ║
         CÓ     ▼                      ╚══════════════════════╝
 ┌──────────────────────────────┐
 │ 7. Họp làm rõ yêu cầu        │  60 phút (ngắn hơn)
 │    (tài liệu đã rõ, ít câu   │
 │     hỏi)                     │
 └──────────────┬───────────────┘
                ▼
 ┌──────────────────────────────┐
 │ 8. Lập trình viên code       │  30 phút
 │    → nhân viên xác nhận      │
 └──────────────┬───────────────┘
                ▼
         ÍT LÀM LẠI HƠN
 ┌──────────────────────────────┐      ╔══════════════════════╗
 │ 9. Làm lại (nếu có)          │  30' ║  tối đa 10% làm lại  ║
 │    + cập nhật danh mục kiểm  │      ║  Vòng phản hồi       ║
 └──────────────────────────────┘      ╚══════════════════════╝

 TỔNG: khoảng 2-3 giờ hỏi đáp + làm lại/chu kỳ
 tối đa 1 lần hỏi đáp, tối đa 10% làm lại

 PHƯƠNG ÁN DỰ PHÒNG:
 - Nếu trí tuệ nhân tạo bỏ sót lỗi → trưởng nhóm phát hiện → cập nhật danh mục
 - Nếu trí tuệ nhân tạo gợi ý sai → nhân viên từ chối → không bắt buộc làm theo
 - Nếu tài liệu vẫn tệ sau kiểm tra → trưởng nhóm báo cáo cho quản lý
```

### So sánh trước/sau

| Chỉ số | Trước | Sau kỳ vọng | Ghi chú |
|---|---:|---:|---|
| Tổng thời gian hỏi đáp + làm lại | khoảng 10 giờ/chu kỳ | khoảng 2-3 giờ/chu kỳ | Mục tiêu chính |
| Số lần hỏi đáp | 3-5 lần/chu kỳ | tối đa 1 lần/chu kỳ | Đo qua bình luận trong hệ thống |
| Vòng xem lại | 2-3 vòng | tối đa 1 vòng | Đo qua nhật ký xem lại tài liệu |
| Tỉ lệ làm lại | khoảng 30% | tối đa 10% | Đo qua phiếu mở lại |
| Họp làm rõ | 120 phút | 60 phút | Cả nhóm được lợi |
| Điểm nghẽn chính | Xem lại bị từ chối + hỏi đáp | Trưởng nhóm xem lại (chấp nhận được) | Người vẫn quyết định |
| Rủi ro mới | Không có | Trí tuệ nhân tạo bỏ sót, nhân viên quá phụ thuộc | Cần danh mục + trưởng nhóm xem lại |

---

## Phát biểu vấn đề bản đầu tiên

| Trường | Nội dung |
|---|---|
| **Người gặp** | Nhân viên phân tích nghiệp vụ non (dưới 1 năm kinh nghiệm) viết yêu cầu cho nhóm Phát triển. |
| **Luồng công việc** | Quản lý giao → nhân viên nghiên cứu → nhân viên viết tài liệu → trưởng nhóm xem lại → họp làm rõ → lập trình viên code → nhân viên xác nhận. |
| **Điểm nghẽn** | Tài liệu thiếu tiêu chí nghiệm thu, trường hợp phát sinh, luồng rõ → trưởng nhóm từ chối 2-3 vòng + lập trình viên hỏi làm rõ 3-5 lần/chu kỳ + 30% làm lại. |
| **Tác động** | Khoảng 10 giờ hỏi đáp + làm lại/chu kỳ. Năng suất chu kỳ giảm khoảng 20%. Nhân viên non căng thẳng, mất 4-6 tuần để đạt chuẩn. |
| **Chỉ số thành công** | Hỏi đáp tối đa 1 lần/chu kỳ, làm lại tối đa 10%, vòng xem lại tối đa 1 vòng, họp làm rõ tối đa 60 phút. |
| **Giới hạn** | Trí tuệ nhân tạo không viết tài liệu thay nhân viên. Trí tuệ nhân tạo chỉ kiểm tra và gợi ý. Trưởng nhóm vẫn là người phê duyệt cuối. Lập trình viên không nhận tài liệu chưa qua trí tuệ nhân tạo kiểm tra + trưởng nhóm phê duyệt. |

---

# 03 — So sánh 3 mức giải pháp + Quyết định

## Ma trận độ phù hợp với trí tuệ nhân tạo

| | Độ mơ hồ thấp | Độ mơ hồ cao |
|---|---|---|
| **Độ phức tạp thấp** | Quy tắc hoặc luồng đơn giản thường đủ | Luồng có trí tuệ nhân tạo hỗ trợ một bước có thể đủ |
| **Độ phức tạp cao** | Luồng điều phối nhiều bước rõ ràng, chưa chắc cần trợ lý tự động | Trợ lý tự động có thể phù hợp, nhưng cần giới hạn, người thật kiểm tra và phương án quay về rất rõ |

**Bài toán này nằm ở ô:** Độ mơ hồ **cao** (chất lượng tài liệu khó định lượng tuyệt đối) nhân Độ phức tạp **cao** (nhiều bước: nghiên cứu → viết → xem lại → làm rõ → code → xác nhận).

**Vì sao:** Tài liệu yêu cầu có nhiều yếu tố khó đo (tiêu chí đủ chưa? trường hợp nào quan trọng? mô tả có rõ không?), nhưng luồng công việc có đường đi cố định và có trưởng nhóm xem lại làm cửa kiểm chất lượng cuối.

## So sánh 3 giải pháp

### Giải pháp 1: Quy tắc — Mẫu tài liệu + Danh mục kiểm tra + Định nghĩa sẵn sàng

```
┌─────────────────────────────────────────────────────────────┐
│ GIẢI PHÁP QUY TẮC: Mẫu tài liệu + Danh mục kiểm tra         │
│ (Không dùng trí tuệ nhân tạo)                               │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  ┌──────────┐   ┌──────────┐   ┌──────────────────────┐     │
│  │ Nhân viên│──▶│ Mở tài   │──▶│ Điền theo mẫu       │     │
│  │ phân tích│   │ liệu theo│   │ tài liệu có sẵn     │     │
│  │ non      │   │ mẫu      │   └──────────┬───────────┘     │
│  └──────────┘   └──────────┘              │                  │
│                                           ▼                  │
│                          ┌──────────────────────────────┐    │
│                          │ Tự kiểm theo danh mục trên   │    │
│                          │ giấy:                        │    │
│                          │ □ Có tiêu chí nghiệm thu chưa?│    │
│                          │ □ Có trường hợp phát sinh     │    │
│                          │   chưa?                      │    │
│                          │ □ Có sơ đồ luồng chưa?       │    │
│                          │ □ Có từ ngữ mơ hồ không?     │    │
│                          └─────────┬────────────────────┘    │
│                                    │                         │
│                          Có thể bỏ ▼ sót                     │
│                           ┌──────────────┐                   │
│                           │ Gửi cho      │                   │
│                           │ trưởng nhóm  │                   │
│                           │ xem lại      │                   │
│                           └──────┬───────┘                   │
│                                  │ Trưởng nhóm vẫn từ chối   │
│                                  │ nếu danh mục không được   │
│                                  │ làm đúng                  │
│                                  ▼                           │
│                           ┌──────────────┐                   │
│                           │ Trưởng nhóm  │                   │
│                           │ xem lại      │                   │
│                           │ → phê duyệt/ │                   │
│                           │   từ chối    │                   │
│                           └──────────────┘                   │
│                                                             │
│  ƯU ĐIỂM:                                                   │
│  - Đơn giản, không cần công nghệ                            │
│  - Dễ triển khai ngay                                       │
│                                                             │
│  NHƯỢC ĐIỂM:                                                │
│  - Nhân viên non VẪN có thể bỏ sót danh mục kiểm tra        │
│  - Không bắt buộc làm theo — không ai nhắc nhân viên kiểm   │
│  - Danh mục kiểm tra trên giấy không thông minh, không gợi ý│
│  - Vẫn phụ thuộc 100% vào kinh nghiệm nhân viên             │
└─────────────────────────────────────────────────────────────┘
```

### Giải pháp 2: Luồng công việc — Trí tuệ nhân tạo tự động kiểm tra chất lượng tài liệu (ĐƯỢC CHỌN)

```
┌─────────────────────────────────────────────────────────────┐
│ GIẢI PHÁP LUỒNG CÔNG VIỆC: Cửa kiểm chất lượng bằng trí tuệ │
│ nhân tạo (ĐƯỢC CHỌN)                                        │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  ┌──────────────────────────────────────────────────────┐  │
│  │  GIAI ĐOẠN 1: NHÂN VIÊN VIẾT TÀI LIỆU               │  │
│  │  (có trí tuệ nhân tạo hỗ trợ)                        │  │
│  │                                                      │  │
│  │  ┌──────┐   ┌────────────┐   ┌──────────────────┐   │  │
│  │  │Quản lý│──▶│Nhân viên   │──▶│Nhân viên viết    │   │  │
│  │  │giao   │   │nghiên cứu  │   │tài liệu yêu cầu  │   │  │
│  │  │tính   │   │+ trí tuệ   │   │trong Docs        │   │  │
│  │  │năng   │   │nhân tạo    │   └────────┬─────────┘   │  │
│  │  └──────┘   │gợi ý cấu  │            │             │  │
│  │             │trúc        │            │             │  │
│  │             └────────────┘            │             │  │
│  └───────────────────────────────────────┼─────────────┘  │
│                                          │                │
│                                          ▼                │
│  ┌──────────────────────────────────────────────────────┐  │
│  │  GIAI ĐOẠN 2: TRÍ TUỆ NHÂN TẠO TỰ ĐỘNG KIỂM TRA     │  │
│  │  (cửa kiểm chất lượng tự động)                       │  │
│  │                                                      │  │
│  │  ┌─────────────────────────────────────────────┐     │  │
│  │  │              BỘ MÁY KIỂM TRA                │     │  │
│  │  │  Đầu vào: Tài liệu + danh mục IREB          │     │  │
│  │  │                                              │     │  │
│  │  │  ┌─────────────────────────────────────┐    │     │  │
│  │  │  │ 1. Kiểm tra tiêu chí nghiệm thu     │    │     │  │
│  │  │  │    → Thiếu? → Đánh dấu + gợi ý      │    │     │  │
│  │  │  │ 2. Kiểm tra trường hợp phát sinh    │    │     │  │
│  │  │  │    → Thiếu? → Đánh dấu + gợi ý      │    │     │  │
│  │  │  │ 3. Kiểm tra từ ngữ mơ hồ            │    │     │  │
│  │  │  │    → Từ không rõ? → Đánh dấu + gợi ý│    │     │  │
│  │  │  │ 4. Kiểm tra đầy đủ trường thông tin │    │     │  │
│  │  │  │    → Thiếu? → Đánh dấu              │    │     │  │
│  │  │  │ 5. Chấm điểm chất lượng (1-10)      │    │     │  │
│  │  │  └─────────────────────────────┬───────┘    │     │  │
│  │  └────────────────────────────────┼────────────┘     │  │
│  │                                   ▼                  │  │
│  │                    ┌──────────────────────┐          │  │
│  │                    │ BÁO CÁO cho nhân viên│          │  │
│  │                    │ - Thiếu 3 tiêu chí   │          │  │
│  │                    │   nghiệm thu         │          │  │
│  │                    │ - Thiếu 2 trường hợp │          │  │
│  │                    │   phát sinh          │          │  │
│  │                    │ - 5 từ ngữ mơ hồ     │          │  │
│  │                    │ - Điểm chất lượng    │          │  │
│  │                    │   6 trên 10          │          │  │
│  │                    └──────────────────────┘          │  │
│  └──────────────────────────────────┬──────────────────┘  │
│                                     │                      │
│                                     ▼                      │
│  ┌──────────────────────────────────────────────────────┐  │
│  │  GIAI ĐOẠN 3: NHÂN VIÊN SỬA + TRƯỞNG NHÓM XEM LẠI   │  │
│  │  (người vẫn quyết định)                              │  │
│  │                                                      │  │
│  │  ┌──────────┐ ┌────────────┐ ┌──────────────────┐   │  │
│  │  │Nhân viên │─▶│Sửa tài    │─▶│Trưởng nhóm kỹ    │   │  │
│  │  │sửa theo  │ │liệu theo   │ │thuật xem lại     │   │  │
│  │  │gợi ý của │ │gợi ý       │ │→ thường PHÊ DUYỆT│   │  │
│  │  │trí tuệ   │ │(30 phút)   │ │vì đã qua cửa kiểm│   │  │
│  │  │nhân tạo  │ └────────────┘ │chất lượng        │   │  │
│  │  └──────────┘               └────────┬─────────┘   │  │
│  │                                      │             │  │
│  │                                      ▼             │  │
│  │                             ┌──────────────────┐   │  │
│  │                             │ Nhóm phát triển  │   │  │
│  │                             │ nhận tài liệu    │   │  │
│  │                             │ chất lượng cao   │   │  │
│  │                             │ → code ngay      │   │  │
│  │                             └──────────────────┘   │  │
│  └──────────────────────────────────────────────────────┘  │
│                                                             │
│  PHƯƠNG ÁN DỰ PHÒNG:                                        │
│  - Trí tuệ nhân tạo bỏ sót → trưởng nhóm phát hiện          │
│    → cập nhật danh mục kiểm tra                             │
│  - Trí tuệ nhân tạo gợi ý sai → nhân viên từ chối           │
│    → không bắt buộc làm theo                                │
│  - Tài liệu vẫn tệ sau kiểm tra → trưởng nhóm báo cáo       │
│    cho quản lý                                              │
│                                                             │
│  ƯU ĐIỂM:                                                   │
│  - Mọi tài liệu đều qua cửa kiểm chất lượng trước khi       │
│    đến trưởng nhóm                                          │
│  - Trí tuệ nhân tạo kiểm tra đều đặn, không bỏ sót          │
│    như người                                                │
│  - Nhân viên non học được từ gợi ý của trí tuệ nhân tạo     │
│  - Trưởng nhóm ít từ chối hơn → tiết kiệm thời gian cả 2   │
│    bên                                                      │
│  - Danh mục kiểm tra tự cải thiện qua thời gian             │
│                                                             │
│  RỦI RO:                                                    │
│  - Nhân viên quá phụ thuộc trí tuệ nhân tạo                 │
│    → không tự tư duy                                        │
│  - Danh mục kiểm tra không cập nhật                         │
│    → bỏ sót mẫu hình mới                                    │
│  → Giảm rủi ro: Trưởng nhóm vẫn xem lại,                    │
│    buổi tổng kết chu kỳ cập nhật danh mục                   │
└─────────────────────────────────────────────────────────────┘
```

### Giải pháp 3: Trợ lý tự động — Trí tuệ nhân tạo tự nghiên cứu, tự viết tài liệu, tự gửi

```
┌─────────────────────────────────────────────────────────────┐
│ GIẢI PHÁP TRỢ LÝ TỰ ĐỘNG: Trí tuệ nhân tạo tự động toàn bộ  │
│ (KHÔNG CHỌN)                                                │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  ┌──────┐   ┌──────────────────────────────────────────┐    │
│  │Quản lý│──▶│          TRỢ LÝ TRÍ TUỆ NHÂN TẠO        │    │
│  │giao   │   │  ┌────────────────────────────────────┐  │    │
│  │tính   │   │  │ 1. Tự nghiên cứu (tìm tài liệu,    │  │    │
│  │năng   │   │  │    tìm trên mạng)                  │  │    │
│  │       │   │  │ 2. Tự hỏi quản lý làm rõ           │  │    │
│  │       │   │  │ 3. Tự viết bản nháp tài liệu       │  │    │
│  │       │   │  │ 4. Tự kiểm tra lại                 │  │    │
│  │       │   │  │ 5. Tự gửi cho trưởng nhóm xem lại  │  │    │
│  │       │   │  │ 6. Tự trả lời câu hỏi lập trình viên│ │    │
│  │       │   │  └────────────────────────────────────┘  │    │
│  └──────┘   └──────────────────┬───────────────────────┘    │
│                                │                            │
│                                ▼                            │
│                   ┌─────────────────────────┐               │
│                   │ RỦI RO:                 │               │
│                   │ - Trợ lý nghiên cứu SAI │               │
│                   │   → Tài liệu SAI từ gốc │               │
│                   │ - Trợ lý hỏi quản lý    │               │
│                   │   không đúng ngữ cảnh   │               │
│                   │ - Nhiều rủi ro bảo mật  │               │
│                   │   và quyền truy cập     │               │
│                   │   (vào tài liệu, email) │               │
│                   │ - Không ai kiểm soát    │               │
│                   │   được quyết định của   │               │
│                   │   trợ lý                │               │
│                   └─────────────────────────┘               │
│                                                             │
│  TẠI SAO KHÔNG CHỌN:                                        │
│  - Quá mức cho vấn đề hiện tại                              │
│  - Tài liệu yêu cầu cần ngữ cảnh sâu mà trợ lý khó nắm      │
│  - Nhiều rủi ro bảo mật và quyền truy cập                   │
│  - Nhân viên phân tích non không học được gì                │
│    nếu trí tuệ nhân tạo làm hết                             │
│  - Luồng công việc (giải pháp 2) đã giải quyết đủ           │
│    điểm nghẽn                                               │
└─────────────────────────────────────────────────────────────┘
```

### Bảng so sánh tóm tắt

| Mức | Phương án | Khi nào đủ | Rủi ro | Chọn? |
|---|---|---|---|---|
| **Quy tắc** | Mẫu tài liệu yêu cầu + danh mục kiểm tra IREB + định nghĩa sẵn sàng. Nhân viên tự kiểm trước khi gửi. | Đủ nếu nhân viên có kỷ luật tự kiểm. | Nhân viên non vẫn bỏ sót, không có cơ chế bắt buộc. | Không chọn làm chính — dùng làm nền tảng danh mục cho trí tuệ nhân tạo. |
| **Luồng công việc** | Nhân viên viết tài liệu → trí tuệ nhân tạo tự động kiểm tra theo danh mục → nhân viên sửa → trưởng nhóm xem lại → nhóm phát triển nhận. | Hợp lý vì: luồng thẳng, trí tuệ nhân tạo làm cửa kiểm, trưởng nhóm vẫn phê duyệt. | Trí tuệ nhân tạo bỏ sót lỗi, nhân viên quá phụ thuộc. Cần cập nhật danh mục liên tục. | **Chọn** |
| **Trợ lý tự động** | Trợ lý tự nghiên cứu, tự viết bản nháp tài liệu, tự hỏi quản lý làm rõ, tự gửi cho trưởng nhóm. | Chỉ cần nếu số lượng tài liệu quá lớn, nhân viên không viết kịp. | Quá rộng, nhiều rủi ro bảo mật, tài liệu sai ngữ cảnh. | Chưa chọn — quá mức cho vấn đề hiện tại. |

**Mức chọn:**

```text
Luồng công việc.
```

**Vì sao chọn:**
- Chất lượng tài liệu cần danh mục kiểm tra có cấu trúc → trí tuệ nhân tạo kiểm nhanh và đều hơn người.
- Luồng công việc thẳng, không cần trợ lý tự quyết định bước tiếp theo.
- Trưởng nhóm vẫn là người chốt cuối — trí tuệ nhân tạo chỉ là cửa kiểm chất lượng phụ trợ.
- Mẫu hình "trí tuệ nhân tạo kiểm tra/gợi ý → người thật phê duyệt" đã được chứng minh.

**Vì sao không chọn mức đơn giản hơn:**
- Quy tắc (mẫu + danh mục kiểm tra) không bắt buộc được — nhân viên non vẫn quên kiểm tra.
- Trí tuệ nhân tạo tự động kiểm tra đảm bảo mọi tài liệu đều qua cửa kiểm trước khi đến trưởng nhóm.

## Phát biểu vấn đề bản thứ nhất

| Trường | Nội dung |
|---|---|
| **Người gặp** | Nhân viên phân tích nghiệp vụ non (dưới 1 năm kinh nghiệm) viết yêu cầu cho nhóm Phát triển. |
| **Luồng công việc** | Quản lý giao → nhân viên nghiên cứu → nhân viên viết tài liệu → trí tuệ nhân tạo tự động kiểm tra → nhân viên sửa → trưởng nhóm xem lại → họp làm rõ → nhóm phát triển code. |
| **Điểm nghẽn** | Tài liệu thiếu cửa kiểm chất lượng tự động → trưởng nhóm từ chối 2-3 vòng + lập trình viên hỏi làm rõ 3-5 lần/chu kỳ + 30% làm lại. |
| **Tác động** | Khoảng 10 giờ hỏi đáp + làm lại/chu kỳ. Năng suất chu kỳ giảm khoảng 20%. |
| **Chỉ số thành công** | Hỏi đáp tối đa 1 lần/chu kỳ, làm lại tối đa 10%, vòng xem lại tối đa 1 vòng, họp làm rõ tối đa 60 phút. |
| **Giới hạn** | Trí tuệ nhân tạo không viết tài liệu thay nhân viên. Trí tuệ nhân tạo chỉ kiểm tra + gợi ý. Trưởng nhóm vẫn phê duyệt. Nhóm phát triển không nhận tài liệu chưa qua trí tuệ nhân tạo kiểm tra + trưởng nhóm phê duyệt. |
| **Điểm trí tuệ nhân tạo can thiệp** | Sau khi nhân viên viết xong tài liệu, trước khi trưởng nhóm xem lại. Trí tuệ nhân tạo kiểm theo danh mục: tiêu chí nghiệm thu, trường hợp phát sinh, từ ngữ mơ hồ, đầy đủ thông tin. |
| **Mức chọn** | Luồng công việc: nhân viên viết → trí tuệ nhân tạo tự động kiểm tra → nhân viên sửa → trưởng nhóm phê duyệt. |
| **Rủi ro và người thật kiểm tra** | Rủi ro: trí tuệ nhân tạo bỏ sót lỗi, nhân viên quá phụ thuộc trí tuệ nhân tạo, danh mục không cập nhật. Giảm rủi ro: trưởng nhóm vẫn xem lại, nhân viên có quyền từ chối gợi ý của trí tuệ nhân tạo, danh mục cập nhật sau mỗi buổi tổng kết chu kỳ. |

## Quyết định cuối

| Câu hỏi | Có / Chưa / Không | Ghi chú |
|---|---|---|
| Người gặp và luồng công việc đã rõ chưa? | **Có** | Nhân viên phân tích non → nhóm phát triển, luồng chu kỳ rõ |
| Đường cơ sở và chỉ số thành công đã đo được chưa? | **Chưa** | Cần đo đường cơ sở thực tế từ hệ thống quản lý đầu việc |
| Có dữ liệu đầu vào đủ dùng không? | **Chưa** | Cần gom tài liệu mẫu tốt và kém để tinh chỉnh danh mục kiểm |
| Nếu trí tuệ nhân tạo sai, hậu quả có chấp nhận được không? | **Có** | Trưởng nhóm vẫn xem lại, sai chỉ là bỏ sót — không phải bịa số liệu |
| Có người xem lại/chủ trì vận hành không? | **Chưa** | Cần chỉ định chủ trì (Trưởng nhóm kỹ thuật hoặc Trưởng nhóm phân tích) duy trì danh mục |
| Có cách không dùng trí tuệ nhân tạo đơn giản hơn không? | **Chưa** | Mẫu + danh mục kiểm tra đủ nhưng không bắt buộc — cần trí tuệ nhân tạo để tự động bắt buộc |

**Quyết định:**

```text
Đi với phạm vi nhỏ (thử nghiệm).
```

**Thử nghiệm nhỏ nhất là:**
- Chọn 1 nhóm chu kỳ (3-5 lập trình viên + 1 nhân viên phân tích non + 1 trưởng nhóm kỹ thuật).
- Nhân viên viết tài liệu như bình thường.
- Trước khi gửi trưởng nhóm, nhân viên dán tài liệu vào câu hỏi chuẩn với danh mục kiểm tra (tiêu chí nghiệm thu, trường hợp phát sinh, từ ngữ mơ hồ, đầy đủ thông tin).
- Trí tuệ nhân tạo kiểm tra → nhân viên sửa → trưởng nhóm xem lại.
- Đo: số lần hỏi đáp, tỉ lệ làm lại, vòng xem lại, thời gian họp làm rõ trong 2 chu kỳ.
- So sánh với đường cơ sở 2 chu kỳ trước đó.

**Điều kiện dừng / quay lại:**
- Nếu số lần hỏi đáp không giảm sau 2 chu kỳ → quay về mẫu + danh mục kiểm tra thủ công.
- Nếu nhân viên quá phụ thuộc trí tuệ nhân tạo (không sửa gợi ý sai) → đào tạo lại nhân viên về cách dùng trí tuệ nhân tạo.
- Nếu trưởng nhóm vẫn từ chối 2 vòng trở lên → danh mục kiểm của trí tuệ nhân tạo chưa đủ → cập nhật danh mục.

**Lý do quyết định:**
- Vấn đề rõ, người gặp rõ, luồng công việc rõ.
- Trí tuệ nhân tạo nằm ở 1 bước cụ thể (cửa kiểm chất lượng), không ôm toàn bộ luồng.
- Người xem lại (trưởng nhóm) vẫn là người chốt cuối.
- Có thành phần không dùng trí tuệ nhân tạo (mẫu, danh mục kiểm tra, định nghĩa sẵn sàng).
- Thử nghiệm nhỏ, đo được, quay lại dễ.
