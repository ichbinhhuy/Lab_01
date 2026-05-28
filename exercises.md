# Ngày 1 — Bài Tập & Phản Ánh

## Nền Tảng LLM API | Phiếu Thực Hành

**Thời lượng:** 1:30 giờ
**Cấu trúc:** Lập trình cốt lõi (60 phút) → Bài tập mở rộng (30 phút)

---

## Phần 1 — Lập Trình Cốt Lõi (0:00–1:00)

Chạy các ví dụ trong Google Colab tại: https://colab.research.google.com/drive/172zCiXpLr1FEXMRCAbmZoqTrKiSkUERm?usp=sharing

Triển khai tất cả TODO trong `template.py`. Chạy `pytest tests/` để kiểm tra tiến độ.

**Điểm kiểm tra:** Sau khi hoàn thành 4 nhiệm vụ, chạy:

```bash
python template.py
```

Bạn sẽ thấy output so sánh phản hồi của GPT-4o và GPT-4o-mini.

---

## Phần 2 — Bài Tập Mở Rộng (1:00–1:30)

### Bài tập 2.1 — Độ Nhạy Của Temperature

Gọi `call_openai` với các giá trị temperature 0.0, 0.5, 1.0 và 1.5 sử dụng prompt **"Hãy kể cho tôi một sự thật thú vị về Việt Nam."**

**Bạn nhận thấy quy luật gì qua bốn phản hồi?** (2–3 câu)

> Temperature càng thấp thì câu trả lời càng ổn định và ít sáng tạo. Temperature cao hơn làm phản hồi đa dạng, sáng tạo và có khả năng làm câu trả lời lan man hoặc ngẫu nhiên hơn.

**Bạn sẽ đặt temperature bao nhiêu cho chatbot hỗ trợ khách hàng, và tại sao?**

> Khoảng 0.2–0.5 để chatbot trả lời ổn định, chính xác và ít có khả năng bị hallucination.

---

### Bài tập 2.2 — Đánh Đổi Chi Phí

Xem xét kịch bản: 10.000 người dùng hoạt động mỗi ngày, mỗi người thực hiện 3 lần gọi API, mỗi lần trung bình ~350 token.

**Ước tính xem GPT-4o đắt hơn GPT-4o-mini bao nhiêu lần cho workload này:**

> GPT-4o có giá khoảng 0.010 USD / 1K token, còn GPT-4o-mini là 0.0006 USD / 1K token. Như vậy GPT-4o đắt hơn khoảng 16–17 lần.

**Mô tả một trường hợp mà chi phí cao hơn của GPT-4o là xứng đáng, và một trường hợp GPT-4o-mini là lựa chọn tốt hơn:**

> GPT-4o phù hợp cho các tác vụ cần suy luận mạnh hoặc chất lượng cao như trợ lý AI chuyên nghiệp. GPT-4o-mini phù hợp cho chatbot đơn giản hoặc ứng dụng cần phục vụ nhiều người dùng với chi phí thấp.

---

### Bài tập 2.3 — Trải Nghiệm Người Dùng với Streaming

**Streaming quan trọng nhất trong trường hợp nào, và khi nào thì non-streaming lại phù hợp hơn?** (1 đoạn văn)

> Streaming quan trọng khi phản hồi dài hoặc người dùng cần cảm giác phản hồi ngay lập tức, ví dụ chatbot AI hoặc trợ lý lập trình. Non-streaming phù hợp khi câu trả lời ngắn, cần xử lý hoàn chỉnh trước khi hiển thị hoặc khi hệ thống cần đơn giản hơn.

## Danh Sách Kiểm Tra Nộp Bài

* [ ] Tất cả tests pass: `pytest tests/ -v`
* [ ] `call_openai` đã triển khai và kiểm thử
* [ ] `call_openai_mini` đã triển khai và kiểm thử
* [ ] `compare_models` đã triển khai và kiểm thử
* [ ] `streaming_chatbot` đã triển khai và kiểm thử
* [ ] `retry_with_backoff` đã triển khai và kiểm thử
* [ ] `batch_compare` đã triển khai và kiểm thử
* [ ] `format_comparison_table` đã triển khai và kiểm thử
* [ ] `exercises.md` đã điền đầy đủ
* [ ] Sao chép bài làm vào folder `solution` và đặt tên theo quy định
