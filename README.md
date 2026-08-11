# second-brain-file-ai

**Bộ khung dựng Bộ Não Thứ 2** — dành cho thành viên Creator CEO / Creator Việt Nam.

Ném thư mục này vào một công cụ AI bậc 2, nhắn *"bắt đầu"*, trả lời phỏng vấn — bạn có một bộ não thứ 2 chạy được thật trong 5–10 tiếng.

> **Phiên bản:** `v2.1` · 2026-08-11 — xem [CHANGELOG.md](CHANGELOG.md)

---

## Cài đặt

### Cách 1 — `git clone` *(khuyên dùng)*

Bộ khung này còn tiến hoá. Clone thì sau này gõ một lệnh là có bản mới nhất.

```bash
git clone https://github.com/tohaidoanfake-afk/second-brain-file-ai.git
cd second-brain-file-ai
```

Cập nhật về sau:

```bash
git pull
```

### Cách 2 — tải file zip

Chưa quen `git` thì tải bản `.zip`, giải nén là dùng được ngay. Đổi lại: có bản mới thì phải tải lại thủ công, và bạn sẽ không biết lúc nào có bản mới.

---

## Bắt đầu

1. Mở công cụ AI **bậc 2** — Claude Cowork, Claude Code, hoặc AntiGravity.
   *(Chatbot thường như ChatGPT web không dùng được: nó không ghi file ra máy bạn, mà bộ não thứ 2 chính là các file trên máy bạn.)*
2. Đặt thư mục này làm workspace — hoặc kéo cả thư mục vào cửa sổ công cụ.
3. Nhắn: **`bắt đầu`**

AI tự tạo `SecondBrain/` rồi phỏng vấn bạn từng câu.

📍 **Toàn bộ lộ trình 8 việc:** [BAT-DAU-TU-DAY.md](BAT-DAU-TU-DAY.md) — tick từng ô, vừa là bản đồ vừa là bằng chứng.

---

## Bộ não của bạn trông như thế nào

AI sẽ tạo ra một thư mục `SecondBrain/` ngay cạnh các file này:

```
SecondBrain/
  raw/          nguồn gốc — bài viết cũ, transcript, ghi chép bạn thả vào
                ⛔ AI KHÔNG BAO GIỜ được sửa thư mục này
  wiki/         các trang AI viết ra, nối nhau bằng [[liên kết]]
    models/     hình mẫu bạn đang học
    people/     người quan trọng
    projects/   dự án
    learnings/  thứ học được từ sách/khoá/người khác
  index.md      mục lục
  log.md        nhật ký — mỗi lần nạp một dòng, chỉ thêm không xoá
```

Đây là mẫu **LLM Wiki** của Andrej Karpathy (thành viên sáng lập OpenAI). Khác biệt nằm ở một chỗ:

> Chatbot thông thường **suy luận lại từ đầu** mỗi lần bạn hỏi — dùng 100 lần vẫn y như lần đầu.
> Bộ não thứ 2 thì **biên tập** những gì bạn đưa vào thành các trang dày, liên kết chéo. Mỗi lần dùng là một lần nó dày thêm.
>
> **Ngừng suy luận lại từ đầu, bắt đầu tích luỹ.**

Khung này đã được thiết kế sẵn — bạn **không cần tự nghĩ ra cấu trúc**, chỉ cần trả lời câu hỏi. Và vì nó là file markdown thuần trên máy bạn, nó là **của bạn**: đổi công cụ AI, đổi máy, hay ngừng trả phí đều không mất.

---

## Trong này có gì

```
CLAUDE.md                    luật vận hành — AI tự đọc mỗi phiên
BAT-DAU-TU-DAY.md            checklist 8 việc
START-HERE.txt               hướng dẫn 1 phút

.claude/skills/
  banh-xe-cuoc-doi/          Việc 0 — nhìn lại 8 khía cạnh, ra kế hoạch dài/ngắn hạn
  onboard/                   dựng bộ não lần đầu
  nap-kho/                   đường ghi DUY NHẤT vào wiki
  kiem-chung/                Việc 6 — bài test bộ não đã lưu thật chưa

templates/                   khung 11 trang neo + vòng 2
  vong3/                     trang sinh ra từ vận hành (tạo rỗng, không điền)
  khung-lap-lai/             khung cho models · people · projects · learnings

reference/
  huong-dan-cai-dat.md       Việc 1 + Việc 5 + bảng tra lỗi
  luat-du-lieu-nhay-cam.md   ĐỌC TRƯỚC khi nạp dữ liệu khách hàng
  Persona-Extraction-Protocol.md   bộ 48 câu hỏi sâu
  Notion-Build-Kit-advanced.md     nếu bạn muốn dùng Notion thay vì file
```

---

## Bốn lệnh dùng hằng ngày

| Lệnh | Làm gì |
|---|---|
| `/banh-xe-cuoc-doi` | Việc 0 — làm **trước tiên**, trước cả khi dựng bộ não |
| `/nap-kho` | nạp chuyện mới, insight mới, tài liệu mới — **đường ghi duy nhất**, đừng sửa tay file `.md` |
| `/kiem-chung` | Việc 6 — chạy sau khi dựng xong, và sau mỗi lần nạp khối lớn |
| `/onboard` | dựng lại từ đầu nếu cần |

---

## ⚠️ Hai điều đọc trước khi bắt đầu

**1. Bộ não của bạn KHÔNG nằm trong repo này.**
AI sẽ tạo thư mục `SecondBrain/` — thư mục đó đã được `.gitignore` chặn sẵn. Nghĩa là dữ liệu khách hàng, doanh thu, chuyện riêng của bạn **không bao giờ bị đẩy lên** khi bạn `git push`.

Đừng gỡ dòng `SecondBrain/` khỏi `.gitignore`. Một lần push nhầm là đủ, và xoá file sau đó không cứu được — lịch sử git vẫn giữ.

**2. Đọc `reference/luat-du-lieu-nhay-cam.md` trước khi nạp khách hàng.**
Mất 3 phút. Bộ não này sắp chứa tên người thật và chuyện của người khác.

---

## Cập nhật bộ khung mà không mất bộ não

`git pull` chỉ động vào các file khung (`CLAUDE.md`, `templates/`, `.claude/skills/`). Thư mục `SecondBrain/` của bạn nằm ngoài git nên không bị đụng tới.

Nếu bạn có sửa file khung và `git pull` báo xung đột: giữ bản của bạn hoặc lấy bản mới đều được — **không có gì trong bộ não của bạn bị ảnh hưởng**.

---

## Đóng góp ngược

Dùng thấy chỗ nào tắc, câu hỏi nào thừa, khung trang nào thiếu — báo lại trong nhóm. Bộ khung này lớn lên bằng đúng cách đó: người dùng thật gặp chỗ vướng thật.
