# Lịch sử phiên bản

Bộ khung này còn tiến hoá. Trang này ghi cái gì đổi và **vì sao** — để bạn biết bản mới có đáng `git pull` không.

---

## v2 — 2026-08-11

Bản gộp hai bộ kit cũ (24/06 và 16/07) + bổ sung toàn bộ lộ trình 8 việc.

### Thêm mới

| Thứ | Vì sao |
|---|---|
| **Việc 0 — skill `banh-xe-cuoc-doi`** | Phần còn lại nạp *dữ liệu việc*. Việc 0 nạp *con người*. Thiếu nó thì bộ não nạp rất nhanh một mục tiêu mà chính chủ chưa tự kiểm lại |
| **Việc 6 — skill `kiem-chung`** | Bắt cái bẫy phổ biến nhất: *tưởng đã lưu vào bộ não, thật ra chỉ nằm trong trí nhớ của đoạn chat*. Hai trường hợp đó trông giống hệt nhau — chỉ bài test này phân biệt được |
| **Skill `nap-kho`** | Đường ghi **duy nhất** vào `wiki/`. Sửa tay file `.md` thì nhanh hơn — và sau vài tuần bộ não sẽ có cùng một chuyện ở ba trang, hai trang nói ngược nhau, `log.md` không phản ánh gì |
| **`BAT-DAU-TU-DAY.md`** | Checklist 8 việc, kiêm bằng chứng cho cam kết hoàn tiền |
| **`reference/huong-dan-cai-dat.md`** | Việc 1 + Việc 5 + bảng tra lỗi. Trước đây nằm ngoài bộ kit |
| **`reference/luat-du-lieu-nhay-cam.md`** | Bộ não sắp chứa tên khách thật. Hai bản cũ không nói một chữ nào |
| **`templates/vong3/`** | Trang sinh ra từ vận hành — tạo rỗng có khung, không bắt điền. Không có chỗ đúng thì nội dung bị nhét bừa vào trang khác |
| **`templates/khung-lap-lai/`** | Khung cho `models` · `people` · `projects` · `learnings` |
| **`templates/customers.md`** | Mục "dữ liệu khách hàng" trong 7 mục tối thiểu trước đây không có trang nào để đặt vào |
| **`.gitignore` chặn `SecondBrain/`** | Để một lần `git push` không đưa dữ liệu khách hàng lên mạng |

### Sửa

- **Bốn trang neo bị bỏ sót** nay vào danh sách bắt buộc: `target-customer` · `values-and-principles` · `contrarian-beliefs` · `ai-operating-preferences`. Đo trên một bộ não đã chạy 6 tuần, bốn trang này nằm trong nhóm được trỏ vào nhiều nhất — nhưng bộ 7 mục tối thiểu cũ không có cái nào. Hệ quả: bộ não trả lời đúng về dự án nhưng viết hộ một bài thì ra giọng máy, và tự ý làm việc lẽ ra phải hỏi.
- **Giai đoạn 0 — hỏi tài liệu có sẵn TRƯỚC khi phỏng vấn.** Lấy từ bộ 16/07. Phần lớn giá trị thật nằm trong bài viết cũ và ghi chép cũ; phỏng vấn chỉ để lấp phần không lấy được từ tài liệu.
- **`voice-profile` có luật chặn:** chưa đủ 10 bài đã đăng thật thì **không được dựng bằng phỏng vấn**, phải để trống kèm lý do. Cái người ta *nghĩ* mình viết thường khác hẳn cái họ *thật sự* viết, và không ai tự phát hiện ra sự lệch đó.
- **Dựng wiki chia 3 vòng** thay vì tạo một lượt: trang neo → trang cần tài liệu → trang rỗng có khung.
- Phỏng vấn thêm 2 nhóm câu: **nguồn lực đang có** và **danh sách khách hàng thật** — hai mục trong 7 mục tối thiểu mà bộ câu hỏi cũ không hỏi.
- Luật sắt từ 6 lên 7 điều: thêm **"không bịa"** và **"chỉ một đường ghi"**.

---

## v1 — 2026-06-24 · `second-brain-kit.zip`

Bản đầu. `CLAUDE.md` + `START-HERE.txt` + `reference/` + 2 skill (`brain`, `onboard`).

**Có:** cơ chế tự chạy — ném vào workspace là AI tự đọc luật mỗi phiên.
**Thiếu:** không có khung trang nào, nên mỗi người ra một bộ não cấu trúc khác nhau; không hỏi tài liệu có sẵn; không có bước kiểm chứng.

---

## Bản song song — 2026-07-16 · `second-brain-onboarding-kit.zip`

Không phải phiên bản kế tiếp của v1 mà là **một cách làm khác**: 14 template + `AGENT_INSTRUCTIONS.md` dán tay vào bất kỳ chatbot nào.

**Có:** Giai đoạn 0 và bộ template — hai thứ tốt nhất, đã được đưa vào v2.
**Thiếu:** không có `CLAUDE.md` nên không có gì thường trực — đóng đoạn chat là AI thành người lạ. Thiết kế cho chatbot thường nên bộ não sinh ra sống trong đoạn chat, đúng cái bẫy mà Việc 6 sinh ra để bắt.
