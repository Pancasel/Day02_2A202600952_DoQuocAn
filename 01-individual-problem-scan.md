# 01 - PROBLEM SCANNING REPORT
## CASE: TỰ ĐỘNG NHẬN DIỆN VÀ CHE LOGO KHÔNG PHÙ HỢP TRONG VIDEO



## 1. TỔNG QUAN BỐI CẢNH (CONTEXT OVERVIEW)
Trong các dự án triển khai giải pháp AI vào thực tế, việc xử lý và làm sạch dữ liệu hình ảnh/video đóng vai trò quyết định đến tính an toàn và uy tín của hệ thống. Bài báo cáo này tập trung phân tích quy trình vận hành, phát hiện các "nút thắt cổ chai" (bottlenecks) và xây dựng phương án tối ưu cho bài toán **"Tự động che logo không phù hợp"** trên các luồng dữ liệu video thực tế. 

Thông qua lăng kính kỹ thuật và quản lý vận hành, đội ngũ kỹ sư AI đối mặt với nhiều thách thức từ khâu chuẩn bị dữ liệu, tối ưu hóa kiến trúc mô hình cho đến đảm bảo hiệu năng thời gian thực (real-time prediction) trên hạ tầng phần cứng cố định.

---

## 2. BẢNG QUAN SÁT VÀ PHÂN TÍCH VẤN ĐỀ (PROBLEM SCAN MATRIX)

Dưới đây là danh sách 8 vấn đề cốt lõi được ghi nhận trong quá trình triển khai thực tế dự án, phân loại theo các lăng kính tối ưu hóa:

| STT | Lăng kính phân tích | Vấn đề quan sát được (Observed Problem) | Đối tượng chịu ảnh hưởng (Actor) | Dấu hiệu thực tế & Hệ quả (Symptoms/Consequences) |
| :--- | :--- | :--- | :--- | :--- |
| **1** | Quy trình lặp lại | Gắn nhãn dữ liệu lớn thủ công cho hàng nghìn hình ảnh chứa logo cần che mỗi khi cập nhật dữ liệu. | AI Engineer | Tiêu tốn từ **2 - 3 ngày** cho mỗi lần cập nhật và làm sạch tập dữ liệu (Data Update Lifecycle). |
| **2** | Quy trình lặp lại | Sinh thêm ảnh giả lập (Data Augmentation) để tăng độ đa dạng cho tập Dataset, giúp mô hình nhận diện tốt hơn. | AI Engineer | Tốn **30 - 40 phút/logo** do phải chỉnh sửa bằng tay để đảm bảo ảnh sinh ra phù hợp với ngữ cảnh thực tế. |
| **3** | Quy trình lặp lại | Chạy các script EDA (Exploratory Data Analysis) thủ công để kiểm tra hiện tượng lệch vế dữ liệu (Class Imbalance) khi nhận batch dữ liệu mới. | AI Engineer | Lãng phí **20 - 30 phút** cho mỗi batch dữ liệu đầu vào mà không có luồng tự động hóa. |
| **4** | AI làm tốt hơn | Các logo nhạy cảm bị lóa sáng, mờ nhòe do chuyển động (motion blur) hoặc bị che khuất một phần thường bị bỏ sót. | AI Engineer / Khách hàng | Gây lọt lưới logo nhạy cảm trên môi trường Production hoặc khi chạy Demo. (Có thể chấp nhận sai số nhỏ nhưng cần hạn chế tối đa). |
| **5** | AI có thể tốt hơn | Cấu hình cứng (Hard-coded configuration) khiến độ nhạy (Threshold) của mô hình bị sai lệch giữa các video có điều kiện ánh sáng khác nhau. | Cả Team (Dev & QA) | Kỹ sư phải liên tục tinh chỉnh threshold thủ công, thay đổi cấu trúc model và tối ưu lại (Optimize) để tương thích với hạ tầng. |
| **6** | AI làm tốt hơn | Khách hàng liên tục yêu cầu mở rộng danh sách đen (Blacklist), đưa thêm một loạt logo mới vào hệ thống cần che phủ. | Cả Team | Bắt buộc phải tiến hành Finetune lại toàn bộ mô hình, lặp lại các bước gán nhãn, sinh dữ liệu, hoặc phải thử nghiệm các hướng tiếp cận mới (Few-shot/One-shot). |
| **7** | Tối ưu thời gian | Đảm bảo tốc độ xử lý khung hình (FPS) và khả năng che phủ chính xác của mô hình khi chạy Live Demo trên một cấu hình phần cứng cố định. | Cả Team | Cần tối ưu hóa sâu luồng dữ liệu (Data Pipeline) và triển khai xử lý đa luồng (Multi-threading) để đáp ứng điều kiện thời gian thực. |
| **8** | Quy trình lặp lại | Tổ chức các buổi họp hằng ngày (Daily Standup), hằng tuần (Weekly) và chia nhỏ công việc (Break-task) dựa trên yêu cầu biến động của khách hàng. | Cả Team | Tiêu tốn khoảng **3 tiếng/tuần** cho các công việc quản lý hành chính và điều phối nội bộ. |

---

## 3. ĐÁNH GIÁ VÀ XẾP HẠNG ƯU TIÊN (TOP 3 PROBLEMS PRIORITIZATION)

Để tối ưu hóa tài nguyên và mang lại giá trị thực tế cao nhất cho dự án, 3 vấn đề trọng điểm sau đây đã được lựa chọn để tập trung giải quyết trước:

```
┌────────────────────────────────────────────────────────────────────────┐
│                          TOP 3 CORE PROBLEMS                           │
├───────────────┬────────────────────────────────────────────────────────┤
│    RANK 1     │  Quy trình Gắn nhãn & Sinh dữ liệu thủ công (Data)     │
├───────────────┼────────────────────────────────────────────────────────┤
│    RANK 2     │  Quy trình cập nhật cấu hình Logo mới (Architecture)   │
├───────────────┼────────────────────────────────────────────────────────┤
│    RANK 3     │  Tối ưu hóa chỉ số FPS cho Live Demo (Infrastructure)  │
└───────────────┴────────────────────────────────────────────────────────┘
```

### Bảng biện giải chi tiết lựa chọn:

| Hạng (Rank) | Vấn đề trọng tâm (Problem) | Vì sao lựa chọn (Rationale) | Yếu tố chưa chắc chắn (Uncertainties / Hypotheses) |
| :---: | :--- | :--- | :--- |
| **1** | **Gắn nhãn & Sinh dữ liệu thủ công** | Quy trình thao tác rất rõ ràng, là nút thắt cổ chai ngốn nhiều thời gian nhất của đội ngũ (2-3 ngày/đợt). Việc giải quyết bài toán này giúp đo lường thành công trực quan qua số giờ công tiết kiệm được. | Chất lượng dữ liệu khi áp dụng các giải pháp Tự động gán nhãn (Auto-labeling) liệu có đủ sạch để huấn luyện mô hình tiếp theo, hoặc đội ngũ kiểm duyệt (QA/Test) có chấp thuận hay không. |
| **2** | **Quy trình cập nhật logo mới** | Việc chuyển đổi kiến trúc từ Finetune truyền thống (YOLO) sang các mô hình Few-shot / One-shot Learning có thể mang lại bước đột phá lớn về mặt vận hành. | Sự đánh đổi (Trade-off) giữa tốc độ cập nhật danh mục logo mới nhanh chóng và độ chính xác của mô hình có nằm trong ngưỡng cho phép của khách hàng hay không. |
| **3** | **Tối ưu FPS cho Live Demo** | Tác động trực tiếp và rõ rệt nhất đến trải nghiệm thực tế của khách hàng, quyết định khả năng nghiệm thu dự án khi chạy trên môi trường thực tế. | Giới hạn cứng từ phần cứng cố định của hệ thống rất khó thay đổi; chưa xác định rõ việc tối ưu hóa mã nguồn và luồng dữ liệu ở tầng phần mềm có thể cải thiện thêm bao nhiêu % hiệu năng. |

---

## 4. THẺ CHI TIẾT VẤN ĐỀ (DETAILED PROBLEM CARDS)

### PROBLEM CARD 1: Gắn nhãn & Sinh dữ liệu thủ công
* **Actor (Đối tượng thực hiện):** AI Engineer.
* **Workflow (Luồng công việc hiện tại):** Nhận danh sách các logo mới từ khách hàng $
ightarrow$ Thu thập dữ liệu thô và sinh thêm ảnh mô phỏng (Data Augmentation) $
ightarrow$ Gắn nhãn thủ công từng khung hình $
ightarrow$ Chạy script EDA kiểm tra phân phối $
ightarrow$ Tiến hành huấn luyện (Train) lại mô hình.
* **Bottleneck (Nút thắt):** Việc căn chỉnh ngữ cảnh, ánh sáng khi sinh ảnh giả lập tiêu tốn từ 30 - 40 phút cho mỗi logo; hoạt động gắn nhãn thủ công hàng nghìn ảnh chiếm dụng từ 2 - 3 ngày làm việc của kỹ sư cho mỗi đợt phát hành batch dữ liệu mới.
* **Impact (Hệ quả):** Vòng lặp cập nhật và tối ưu mô hình bị kéo dài, làm chậm tiến độ dự án; các kỹ sư AI bị lãng phí phần lớn thời gian vào các công việc thủ công (tay chân) thay vì tập trung cải tiến thuật toán.
* **Success Metric (Tiêu chí thành công):** * Giảm tổng thời gian chuẩn bị và xử lý dữ liệu xuống **dưới 1 ngày/đợt** cập nhật.
  * Đội ngũ QA/Test nghiệm thu thành công và chấp thuận chất lượng của tập dữ liệu sinh ra tự động.
* **Boundary (Phạm vi giải pháp):** Cơ chế tự động chỉ đóng vai trò hỗ trợ tiền gán nhãn (Pre-labeling) và sinh dữ liệu thô; tuyệt đối không tự ý đẩy thẳng dữ liệu vào tập huấn luyện chính thức khi chưa có sự kiểm soát của con người.
* **Điểm AI can thiệp:** Tích hợp trực tiếp vào bước sinh dữ liệu giả lập tự động theo ngữ cảnh và khoanh vùng đối tượng (Bounding Box) tự động trước khi chuyển cho kỹ sư kiểm duyệt.
* **Mức chọn hợp tác (Workflow Level):** Hệ thống AI tự động sinh dữ liệu giả lập và pre-label; Kỹ sư AI đóng vai trò kiểm duyệt (Reviewer), chỉ tập trung chỉnh sửa và tinh chỉnh các nhãn khó hoặc nhãn bị lệch biên.
* **Rủi ro & Cơ chế kiểm soát (HITL):** Mô hình Auto-label có thể nhận diện sai hoặc ảnh sinh ra không sát với phân phối thực tế. *Giải pháp:* Thiết lập quy trình lấy mẫu ngẫu nhiên (Random Sampling) với tỷ lệ nhất định để kỹ sư AI/QA đánh giá định lượng chất lượng nhãn trước khi chốt tập dữ liệu train.

---

### PROBLEM CARD 2: Quy trình cập nhật cấu hình logo mới
* **Actor (Đối tượng thực hiện):** AI Engineer, Khách hàng, Đội ngũ kiểm duyệt (Moderator).
* **Workflow (Luồng công việc hiện tại):** Tiếp nhận yêu cầu thêm logo từ phía đối tác. Đội ngũ tiến hành thu thập, gán nhãn dữ liệu bổ sung. Tiến hành Finetune lại mô hình YOLO hiện tại. Đánh giá độ chính xác (Evaluation). Triển khai lên hệ thống (Deployment).
* **Bottleneck (Nút thắt):** Kiến trúc hệ thống hiện tại bị phụ thuộc hoàn toàn vào phương pháp Finetune truyền thống, đòi hỏi phải lặp lại toàn bộ pipeline chuẩn bị dữ liệu phức tạp từ đầu mỗi khi có một class mới xuất hiện.
* **Impact (Hệ quả):** Hệ thống thiếu tính linh hoạt (scalability), phản hồi rất chậm trước các yêu cầu bổ sung khẩn cấp của khách hàng; chi phí tài nguyên tính toán (GPU/CPU) cho việc tái huấn luyện (Retrain) mô hình định kỳ rất lớn.
* **Success Metric (Tiêu chí thành công):**
  * Giảm thiểu tối đa hoặc loại bỏ hoàn toàn thời gian phải thu thập dữ liệu diện rộng và Finetune lại từ đầu khi thêm logo mới.
  * Đảm bảo sự đánh đổi về mặt độ chính xác (Đặc biệt là các chỉ số Precision/Recall) nằm trong ngưỡng sai số mà khách hàng đã ký kết chấp thuận.
* **Boundary (Phạm vi giải pháp):** Các mô hình tiếp cận theo hướng Few-shot / One-shot Learning không thay thế hoàn toàn lõi mô hình YOLO hiện tại ngay lập tức, mà chỉ áp dụng thử nghiệm độc lập cho các nhóm logo cần cập nhật khẩn cấp hoặc các lớp dữ liệu hiếm (Rare Classes).
* **Điểm AI can thiệp:** Áp dụng tại Module phát hiện đối tượng (Object Detection Pipeline) khi hệ thống nhận diện tín hiệu từ một danh sách đen (Blacklist) động do khách hàng cấu hình.
* **Mức chọn hợp tác (Architecture Level):** Chuyển dịch một phần luồng xử lý sang các mô hình Zero-shot/Few-shot để nhận diện nhanh các đối tượng mới dựa trên ảnh mẫu, bypass hoàn toàn bước huấn luyện lại mô hình cốt lõi.
* **Rủi ro & Cơ chế kiểm soát (HITL):** Mô hình Few-shot thường có tỷ lệ bỏ sót đối tượng (False Negative) cao hơn so với mô hình YOLO được tối ưu hóa sâu. *Giải pháp:* Thiết lập bộ lọc kiểm tra ngưỡng tin cậy (Confidence Score Filter). Các khung hình có độ tự tin thấp sẽ tự động được gửi về phân hệ kiểm duyệt thủ công (Human Moderator) để xử lý hậu kỳ.

---

### PROBLEM CARD 3: Tối ưu hóa FPS cho Live Demo
* **Actor (Đối tượng thực hiện):** AI Engineer, Khách hàng (Người xem trực tiếp buổi demo).
* **Workflow (Luồng công việc hiện tại):** Luồng dữ liệu video đi vào hệ thống $
ightarrow$ Giải mã video (Decode) $
ightarrow$ Mô hình AI thực hiện dự đoán vị trí logo (Inference) $
ightarrow$ Tiến hành che/gột bỏ logo (Censorship/Blurring) $
ightarrow$ Xuất bản và hiển thị video kết quả đầu ra (Live Demo UI).
* **Bottleneck (Nút thắt):** Cấu hình phần cứng bị giới hạn cố định từ trước, trong khi pipeline xử lý tuần tự hiện tại chưa được tối ưu, dẫn đến hiện tượng nghẽn cổ chai (bottleneck) nghiêm trọng tại khâu xử lý inference của mô hình, làm giảm đáng kể chỉ số FPS.
* **Impact (Hệ quả):** Trải nghiệm xem Live Demo của khách hàng bị giật lag, trễ hình (latency cao); đối tác đánh giá thấp năng lực triển khai thời gian thực và tính khả thi của giải pháp phần mềm.
* **Success Metric (Tiêu chí thành công):**
  * Đẩy chỉ số FPS lên mức mượt mà chuẩn thời gian thực (đáp ứng từ **25 - 30 FPS trở lên**) trên cấu hình phần cứng cố định.
  * Duy trì tỷ lệ che phủ chính xác, không làm giảm độ ổn định của việc nhận diện logo.
* **Boundary (Phạm vi giải pháp):** Tập trung tối ưu hóa hoàn toàn ở tầng phần mềm (Software-level optimization) bao gồm: cấu trúc lại luồng I/O, xử lý đa luồng, tối ưu framework. Tuyệt đối không giải quyết bài toán bằng cách yêu cầu nâng cấp hoặc mua sắm thêm thiết bị phần cứng mới.
* **Điểm AI can thiệp:** Tối ưu hóa tại bước tăng tốc Inference (ví dụ: chuyển đổi định dạng và lượng hóa trọng số mô hình sang TensorRT hoặc ONNX Runtime) và tối ưu hóa kiến trúc hàng đợi dữ liệu (Queue Management).
* **Mức chọn hợp tác (System Level):** Áp dụng kiến trúc đa luồng (Multi-threading / Multi-processing) tách biệt luồng Đọc/Ghi khung hình với luồng xử lý của mô hình AI; thiết lập cơ chế gom cụm dữ liệu (Batching Size) tối ưu nhất cho phần cứng hiện tại.
* **Rủi ro & Cơ chế kiểm soát (HITL):** Việc ép hiệu năng hoặc áp dụng các kỹ thuật skip-frame (bỏ qua khung hình) quá mức để đạt FPS cao có thể dẫn đến việc logo bị lọt lưới trong vài mili-giây. *Giải pháp:* Xây dựng một kịch bản kiểm thử tự động (Automation Test Suite) chạy song song nhằm đo lường chính xác tỷ lệ lọt logo ứng với từng mức tinh chỉnh FPS, giúp kỹ sư tìm ra điểm cân bằng (Sweet Spot) tối ưu nhất.