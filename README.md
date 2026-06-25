# Biểu Đồ Vàng - Giá vàng Ngọc Thẩm (GitHub Pages)

Bộ source HTML tĩnh đã được làm sạch để chạy trên GitHub Pages.

## Cấu trúc

```text
.
├── index.html
├── 404.html
├── .nojekyll
├── assets/
│   ├── css/github-fixes.css
│   └── js/github-fixes.js
└── gia-vang/
    └── ngoctham/
        └── index.html
```

## Đã fix

- Sửa `type="...-text/javascript"` do Cloudflare Rocket Loader làm JavaScript không chạy.
- Xóa Rocket Loader, Cloudflare Email Decode và Cloudflare Insights để tránh lỗi `/cdn-cgi/...` trên GitHub Pages.
- Giải mã email `contact@bieudovang.com`.
- Xóa `csrf_token` vì đây là web tĩnh.
- Thêm Tailwind CDN fallback và CSS fix riêng để giữ giao diện.
- Thêm JavaScript fix cho tìm kiếm và menu mobile.
- Tạo route `/gia-vang/ngoctham/` để mở đúng slug khi deploy GitHub Pages.
- Thêm `.nojekyll` để GitHub Pages phục vụ file tĩnh đúng hơn.

## Cách deploy GitHub Pages

1. Tạo repository mới trên GitHub.
2. Upload toàn bộ file trong thư mục này lên repository.
3. Vào **Settings → Pages**.
4. Chọn **Deploy from a branch**.
5. Chọn branch `main`, folder `/root`.
6. Truy cập URL GitHub Pages sau khi deploy xong.

> Lưu ý: các dữ liệu live/chart vẫn dùng asset và endpoint từ `https://bieudovang.com/`, vì đây là bản HTML tĩnh.
