# Học tiếng Nhật N5 – đưa lên Vercel

Thư mục này là một trang web tĩnh: không cần cài đặt, không cần server.

| File | Vai trò |
|---|---|
| `index.html` | Toàn bộ trang học (giao diện + dữ liệu + code) |
| `favicon.svg` | Biểu tượng trên tab trình duyệt |
| `og-image.png` | Ảnh xem trước khi gửi link qua Zalo / Facebook / Messenger |
| `vercel.json` | Cấu hình Vercel (luôn lấy bản mới nhất khi bạn cập nhật) |

---

## Cách 1 — Qua GitHub (dễ nhất, chỉ cần trình duyệt)

**Bước 1. Đưa file lên GitHub**
1. Vào https://github.com → đăng nhập → bấm **New** (tạo repository mới).
2. Đặt tên, ví dụ `tieng-nhat-n5` → chọn Public hoặc Private → **Create repository**.
3. Bấm dòng **uploading an existing file** → kéo thả 4 file trên vào → **Commit changes**.

**Bước 2. Kết nối Vercel**
1. Vào https://vercel.com → **Sign Up / Log in** bằng tài khoản GitHub.
2. Bấm **Add New… → Project** → chọn repo `tieng-nhat-n5` → **Import**.
3. Ở **Framework Preset** chọn **Other**, các ô khác để nguyên → **Deploy**.
4. Khoảng 30 giây sau bạn có link dạng `https://tieng-nhat-n5.vercel.app` để chia sẻ.

**Đổi tên link cho đẹp:** Project → **Settings → Domains** → sửa phần trước `.vercel.app`
(ví dụ `n5-minna.vercel.app`), hoặc gắn tên miền riêng nếu có.

**Cập nhật về sau:** vào repo trên GitHub → bấm vào `index.html` → biểu tượng 🗑 xoá hoặc
**Add file → Upload files** để thay bằng file mới → Commit. Vercel tự triển khai lại sau ~30 giây,
link giữ nguyên.

---

## Cách 2 — Dùng Vercel CLI (nếu máy đã có Node.js)

```bash
cd thu-muc-chua-4-file
npx vercel          # lần đầu: đăng nhập, trả lời các câu hỏi (cứ Enter)
npx vercel --prod   # đưa lên bản chính thức
```

---

## Sau khi có link: bật ảnh xem trước khi chia sẻ

Facebook và Zalo cần đường dẫn ảnh đầy đủ. Mở `index.html`, tìm dòng:

```html
<meta property="og:image" content="/og-image.png">
```

và sửa thành link thật của bạn, ví dụ:

```html
<meta property="og:image" content="https://n5-minna.vercel.app/og-image.png">
```

rồi cập nhật lại file như hướng dẫn ở trên.

---

## Lưu ý

- Link Vercel là **công khai**: ai có link đều mở được (không cần tài khoản).
- Tiến độ học, từ đã thuộc, lộ trình… lưu trên trình duyệt của từng người, không gửi đi đâu.
- Nét chữ kanji dùng dữ liệu KanjiVG (CC BY-SA 3.0) — giữ nguyên dòng ghi nguồn ở cuối trang.
