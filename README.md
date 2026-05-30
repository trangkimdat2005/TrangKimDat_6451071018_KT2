# TrangKimDat_6451071018_KT2

## Tên đề tài

**Hệ thống Đăng nhập Facebook (Facebook OAuth Login)**

## Mô tả chức năng hệ thống

Đây là ứng dụng web cho phép người dùng đăng nhập thông qua tài khoản Facebook sử dụng Facebook OAuth 2.0 API.

### Các chức năng chính:

- **Đăng nhập bằng Facebook**: Người dùng click nút "Login with Facebook" để xác thực qua Facebook
- **Hiển thị thông tin profile**: Sau khi đăng nhập thành công, hiển thị:
  - Avatar (hình đại diện)
  - Tên người dùng
  - Email
- **Hiển thị JSON response**: Hiển thị toàn bộ dữ liệu API trả về dưới dạng JSON
- **Đăng xuất**: Người dùng có thể đăng xuất khỏi hệ thống

### Luồng hoạt động:

1. Người dùng mở trang web
2. Hệ thống tự động kiểm tra trạng thái đăng nhập Facebook
3. Nếu chưa đăng nhập -> Hiện nút "Login with Facebook"
4. Nếu đã đăng nhập -> Hiện thông tin profile và JSON response
5. Người dùng có thể click "Đăng xuất" để quay lại trạng thái chưa đăng nhập

## Hướng dẫn chạy project

### Yêu cầu:

- Trình duyệt web hiện đại (Chrome, Firefox, Edge, Safari)
- Tài khoản Facebook (để test đăng nhập)
- Web server để chạy (do Facebook SDK yêu cầu)

### Cách 1: Dùng Live Server (VS Code)

1. Mở project trong VS Code
2. Cài extension "Live Server"
3. Click chuột phải vào file `BT2/index.html`
4. Chọn "Open with Live Server"

### Cách 2: Dùng Python (Terminal)

```bash
cd BT2
python -m http.server 8080
```

Sau đó mở trình duyệt truy cập: `http://localhost:8080`

### Cách 3: Dùng Node.js

```bash
cd BT2
npx serve
```

### Lưu ý:

- Facebook App ID trong code: `2028420931352860` (đã được cấu hình sẵn)
- Nếu muốn sử dụng App ID riêng, thay đổi giá trị `appId` trong file `index.html`

## Cấu trúc project

```
TrangKimDat_6451071018_KT2/
├── BT2/
│   └── index.html          # File HTML chính (đã chứa CSS + JS)
├── README.md
└── .vscode/
    └── settings.json
```

## Công nghệ sử dụng

- **HTML5/CSS3**: Giao diện người dùng
- **Bootstrap 5.3**: CSS framework
- **Font Awesome 6.4**: Icons
- **Facebook JavaScript SDK**: Xác thực OAuth
- **JavaScript (ES6)**: Logic xử lý
