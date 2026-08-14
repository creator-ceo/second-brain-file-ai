# Lịch sử phiên bản

Bộ khung này còn tiến hoá. Trang này ghi cái gì đổi và **vì sao** — để bạn biết bản mới có đáng `git pull` không.

---

## v2.5 — 2026-08-14

- **Thêm mục hướng dẫn cho máy Windows.** Toàn bộ tài liệu trước đó viết theo góc nhìn Mac (*"mở Terminal"*), trong khi phần lớn member nhiều khả năng dùng Windows. Bốn chỗ hay vấp nay có sẵn cách chữa: lệnh `claude` báo *not recognized* (phải mở lại PowerShell, không phải cài hỏng) · chưa có Git · đường dẫn có dấu cách cần nháy kép · thư mục ẩn `.claude` không thấy trong File Explorer.
- **Nói rõ dùng PowerShell chứ không dùng CMD**, kèm cách phân biệt (`PS C:\...` vs `C:\...`) và bảng ba khác biệt. Lệnh cài đặt không chạy được trong CMD; và ngay cả khi `claude` chạy được, Claude Code sẽ có lúc yêu cầu chuyển sang PowerShell giữa chừng.
- Ghi rõ Claude Code có bản chạy thẳng trên Windows, **không cần WSL và không cần Node.js** — hai thứ này là yêu cầu của cách cài cũ và vẫn còn trong nhiều hướng dẫn trên mạng, đủ để làm người mới bỏ cuộc ngay bước đầu.

---

## v2.4 — 2026-08-14

- **README: mục cập nhật viết lại cho cả người dùng zip.** Trước đó chỉ hướng dẫn `git pull`, bỏ quên nhóm cài bằng zip — vốn là nhóm đông hơn và ít rành kỹ thuật hơn. Nay có đủ hai đường, cộng phép kiểm 2 câu sau khi cập nhật.
- **⛔ Cảnh báo: đừng nhờ AI "tự đọc bản mới rồi bổ sung phần còn thiếu".** Câu đó mơ hồ giữa *thiếu file khung* và *thiếu nội dung trong bộ não* — AI dễ hiểu sang nghĩa thứ hai rồi tự tạo và tự điền trang trong `wiki/`, phá Luật sắt số 2, và bịa nội dung để lấp chỗ trống. Thay khung thủ công thì chắc chắn và kiểm được; AI chỉ nên dùng để xác nhận sau khi thay.

---

## v2.3 — 2026-08-11

- **Thêm `AGENTS.md`** — Codex CLI đọc `AGENTS.md`, không đọc `CLAUDE.md`. Trước bản này, member dùng Codex clone về sẽ không được nạp luật nào cả, và không có cách nào nhận ra ngoài việc thấy AI trả lời như bình thường. `AGENTS.md` **trỏ về `CLAUDE.md` chứ không chép lại** — hai bản luật song song sẽ lệch nhau sau vài lần cập nhật.
- **Bảng kích hoạt 4 skill bằng lời nói.** Codex tìm skill ở `.codex/skills/`, bộ này để ở `.claude/skills/`, nên Codex không có lệnh gạch chéo. `AGENTS.md` dặn AI mở đúng file khi nghe *"làm bánh xe cuộc đời"*, *"lưu vào não"*, *"kiểm chứng"*... Với người không quen gõ lệnh thì cách này còn dễ hơn.
- **README: cảnh báo chỗ hay sai nhất — mở công cụ đúng thư mục.** `CLAUDE.md` và 4 skill chỉ được nạp khi thư mục này là gốc của phiên. Clone về rồi vẫn ngồi ở thư mục cũ thì nhắn *"bắt đầu"* không có gì xảy ra, và trông y hệt như bộ khung hỏng. Thêm dấu hiệu nhận biết + phép kiểm nhanh.

---

## v2.2 — 2026-08-11

Sửa 5 lỗi tìm ra khi **chạy thử trọn lộ trình 8 việc trên một bản clone sạch** — đóng vai member từ đầu tới cuối.

- 🔴 **Việc 6 chẩn đoán sai.** Bảng chấm cũ kết luận điểm thấp = *"bộ não chưa lưu được"*, hướng người dùng đi sửa cài đặt. Nhưng bộ não lưu tốt mà mới điền được vài trang cũng ra điểm thấp y hệt — hai vấn đề ngược nhau, hai cách chữa ngược nhau. Thêm **Câu 0** hỏi trước (*"đọc file goals.md, cho tôi biết dòng đầu"*) để tách hẳn hai nhánh: đọc được = lỗi nội dung, đi điền tiếp; không đọc được = lỗi công cụ, dừng test. Lỗi này nhắm đúng vào người làm dở dang, tức người ít khả năng tự gỡ nhất.
- **Thêm khuôn `templates/index.md` và `templates/log.md`.** Hai file ở gốc bộ não, được Luật sắt nhắc tới nhưng không có khuôn nào — mỗi người ra một định dạng, và `nap-kho` về sau ghi thêm vào cấu trúc không tồn tại.
- **Vòng 3 vẫn phải thay `[Tên bạn]` ở tiêu đề.** Câu *"tạo file rỗng, KHÔNG bắt điền"* bị hiểu thành không đụng gì cả, nên 5 trang vào bộ não với placeholder ngay dòng đầu.
- Cây thư mục ghi rõ `raw/` còn rỗng lúc tạo, file onboarding lưu vào ở **cuối** buổi.
- Nói rõ `index.md` và `log.md` **không tạo rỗng**.

---

## v2.1 — 2026-08-11

- **Bổ sung mục "Kiến trúc — mẫu LLM Wiki của Karpathy"** vào `CLAUDE.md` và `README.md`. Trước đó chỉ có một dòng nhắc tên; phần giải thích thật nằm trong `reference/Notion-Build-Kit-advanced.md` — file tuỳ chọn về Notion mà người dùng file sẽ không bao giờ mở. Lý lẽ cốt lõi của cả kiến trúc đang nằm nhầm chỗ.
- **Khối tạo thư mục viết lại cho đủ:** thêm 4 thư mục con `wiki/models` `people` `projects` `learnings` (trước đó vòng 3 và khung lặp lại đều giả định chúng tồn tại, nhưng không chỗ nào bảo AI tạo), thêm bước **in ra đường dẫn tuyệt đối** của bộ não cho người dùng, thêm luật dùng `templates/` (là khuôn, không copy cả thư mục vào `wiki/`).
- Việc 2 trong checklist thêm ô chép đường dẫn — nối thẳng sang Việc 5 (mở Obsidian), chỗ tắc phổ biến nhất vì người dùng không biết trỏ vào đâu.

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
