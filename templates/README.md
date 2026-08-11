# Khung các trang — dùng thế nào

> Đây là **khuôn**, không phải nội dung. AI sẽ dùng chúng khi dựng `SecondBrain/wiki/`.
> Giữ nguyên cấu trúc heading, chỉ thay `[...]` bằng nội dung thật. **Thiếu thì để nguyên placeholder — không bịa.**

---

## Hai file gốc — dựng trước tiên

`index.md` và `log.md` nằm ở gốc `SecondBrain/`, không nằm trong `wiki/`. Dựng từ `index.md` và `log.md` trong thư mục này — **đừng tạo rỗng**: mỗi người một định dạng thì skill `nap-kho` về sau ghi thêm vào một cấu trúc không tồn tại.

---

## Vòng 1 — 11 trang neo *(luôn tạo, dựng từ phỏng vấn)*

Trang ngắn nhưng mọi trang khác quy chiếu về. Chúng quyết định bộ não chạy được hay không.

`about-me` · `goals` · `offer-ladder` · `target-customer` · `values-and-principles` · `contrarian-beliefs` · `ai-operating-preferences` · `systems-and-stack` · `decision-style` · `network` · `customers`

⚡ Hai trang dễ bị coi nhẹ nhất, và cũng là hai trang không có nguồn nào ngoài đầu bạn:

- **`ai-operating-preferences`** — không có nó thì mỗi phiên bạn lại phải dặn lại AI từ đầu, và nó sẽ tự ý làm những việc lẽ ra phải hỏi.
- **`contrarian-beliefs`** — nền của mọi định vị. Không có nó thì mọi thứ AI viết ra sẽ đúng nhưng ai cũng nói được.

---

## Vòng 2 — chỉ dựng khi CÓ tài liệu

| Trang | Điều kiện |
|---|---|
| `voice-profile` | **≥10 bài đã đăng thật.** Chưa đủ → để trống, ghi rõ *"chưa đủ bài"* |
| `experiences-library` | có ghi chép/bản ghi buổi chia sẻ, coaching |
| `customer-wins` | có feedback/testimonial thật, kèm số liệu |
| `expertise` | dựng được từ phỏng vấn, nhưng dày hơn nhiều nếu có tài liệu |

⚠️ **Đừng dựng `voice-profile` bằng cách hỏi suông.** Cái người ta *nghĩ* mình viết thường khác hẳn cái họ *thật sự* viết — và không ai tự phát hiện ra sự lệch đó. Chưa đủ 10 bài thì để trống còn hơn dựng sai, vì trang này chi phối mọi thứ AI viết ra sau đó.

---

## Vòng 3 — tạo file rỗng có khung, KHÔNG điền *(thư mục `vong3/`)*

`audience-insights` · `business-metrics` · `content-library` · `hook-library` · `competitors`

Các trang này **sinh ra từ vận hành**, không nạp được bằng trí nhớ. Nhưng vẫn tạo sẵn — không có chỗ đúng thì nội dung sẽ bị nhét bừa vào trang khác, và bộ não loạn từ tuần thứ ba.

Mỗi file đã có sẵn dòng đầu ghi rõ nó sinh ra từ đâu. **Giữ nguyên dòng đó** cho tới khi có dữ liệu thật.

⚠️ Nhưng vẫn **thay `[Tên bạn]` ở tiêu đề** bằng tên thật. "Không điền" nói về phần nội dung, không nói về tên.

---

## Khung lặp lại *(thư mục `khung-lap-lai/`)*

Mỗi lần thêm một hình mẫu / một người / một dự án / một nguồn học — nhân bản khung tương ứng thành một file mới:

| Khung | Nhân thành | Đặt ở |
|---|---|---|
| `models.md` | mỗi hình mẫu một file | `wiki/models/` |
| `people.md` | mỗi người quan trọng một file | `wiki/people/` |
| `projects.md` | mỗi dự án một file | `wiki/projects/` |
| `learnings.md` | mỗi chủ đề học được một file | `wiki/learnings/` |

---

## Ba luật khi điền bất kỳ trang nào

1. **Giữ nguyên chữ của người dùng** ở phần trích dẫn. Chỉ dọn câu chữ ở phần đúc kết. Câu cửa miệng và ẩn dụ của họ là thứ không tái tạo được — viết lại cho "hay hơn" là làm hỏng.
2. **Mọi trang phải nối `[[liên kết]]`** tới ít nhất 2 trang khác. Trang mồ côi là trang sẽ không bao giờ được tìm thấy lại.
3. **Thiếu thì để `[ngoặc vuông]`.** Một bộ não có chỗ trống thì sửa được. Một bộ não có chỗ bịa thì hỏng mà không ai biết — và AI sẽ dùng chỗ bịa đó y như dùng sự thật.
