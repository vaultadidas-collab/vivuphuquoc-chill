# Kodeeboyzz — Tour Phú Quốc

Website bán tour & vé du lịch Phú Quốc: tour 4 đảo, cáp treo Hòn Thơm, VinWonders, Vinpearl Safari, lặn ngắm san hô, câu cá & hoàng hôn đảo ngọc.

🔗 **Live:** https://kodeeboyzz.com

---

## Là gì

Một file HTML tự chạy (self-contained) — không cần build, không cần server. Tất cả hình ảnh nhúng base64, QR Zalo nhúng sẵn, video YouTube embed. Mở là chạy, kể cả offline hoặc GitHub Pages.

## Tính năng

- Bảng giá tour & vé 2026 (cáp treo, VinWonders/Safari combo)
- Gallery video YouTube: Tour 4 đảo · Lặn ngắm san hô · Cáp treo & VinWonders
- Đặt tour qua form + chuyển khoản (MB Bank / MoMo / ZaloPay / USDT-TON)
- QR Zalo đặt tour nhanh
- Đa ngôn ngữ (data-i18n)
- Bản đồ Google Maps Phú Quốc
- SEO: schema JSON-LD cho video & tour

## Cấu trúc

```
.
├── index.html      # Trang chính (đổi tên từ vip.html — xem bên dưới)
├── CNAME           # Domain: kodeeboyzz.com
└── README.md
```

---

## Deploy lên GitHub Pages

1. Up `index.html`, `CNAME`, `README.md` lên repo.
2. Vào **Settings → Pages → Source** chọn branch `main`, folder `/ (root)`, bấm **Save**.
3. Đợi vài phút, site lên ở `https://<username>.github.io/<repo>` hoặc domain custom.

> ⚠️ **Quan trọng:** GitHub Pages chỉ tự mở file tên `index.html`. File hiện tại là `vip.html` → **đổi tên thành `index.html`** trước khi up. Nếu muốn giữ `vip.html` thì phải vào link `kodeeboyzz.com/vip.html` mới ra.

---

## Trỏ domain kodeeboyzz.com

### Bước 1 — Trong repo
File `CNAME` đã có sẵn nội dung `kodeeboyzz.com`. Giữ nguyên, đừng xoá.

### Bước 2 — Bên nhà cung cấp DNS (chỗ mua domain)
Thêm các bản ghi sau:

**Cho domain gốc (kodeeboyzz.com) — 4 bản ghi A:**

| Type | Name | Value           |
|------|------|-----------------|
| A    | @    | 185.199.108.153 |
| A    | @    | 185.199.109.153 |
| A    | @    | 185.199.110.153 |
| A    | @    | 185.199.111.153 |

**Cho www (www.kodeeboyzz.com) — 1 bản ghi CNAME:**

| Type  | Name | Value                    |
|-------|------|--------------------------|
| CNAME | www  | `<username>.github.io.`  |

> Thay `<username>` bằng tên GitHub của mày.

### Bước 3 — Trong GitHub
Vào **Settings → Pages → Custom domain**, nhập `kodeeboyzz.com`, Save. Tick **Enforce HTTPS** (đợi vài tiếng để cấp chứng chỉ SSL).

> DNS có thể mất từ vài phút đến 24–48 tiếng để cập nhật toàn cầu.

---

## Sửa nội dung

Mở `index.html` bằng editor bất kỳ:
- **Bảng giá / tour:** tìm theo tên tour trong HTML
- **Thông tin thanh toán:** tìm `pay: {` (sửa số tài khoản / MoMo / ZaloPay)
- **Video:** tìm `youtube-nocookie.com/embed/` rồi thay video ID
- **Liên hệ / QR Zalo:** tìm `Liên Hệ` trong footer

---

© 2026 Kodeeboyzz · Đặc khu Phú Quốc, Việt Nam
