# CarStore - Website Bán Xe Demo

Một ứng dụng demo website bán xe được xây dựng với Next.js và Tailwind CSS, dễ dàng deploy lên Vercel.

## 🚀 Tính năng

- **Trang chủ**: Hero section và danh sách xe nổi bật
- **Danh sách xe**: Hiển thị tất cả xe với thông tin chi tiết
- **Chi tiết xe**: Thông tin đầy đủ về từng xe
- **Wishlist**: Lưu trữ danh sách xe yêu thích
- **Đặt lịch lái xe thử**: Form đặt lịch lái xe thử
- **Admin Panel**: Quản lý users và lịch lái xe thử
- **Responsive Design**: Tương thích với mọi thiết bị

## 🛠️ Công nghệ sử dụng

- **Frontend**: Next.js 15, React 19, Tailwind CSS
- **Backend**: Next.js API Routes
- **Database**: JSON file (dễ deploy)
- **Deployment**: Vercel

## 📁 Cấu trúc dự án

```
car-selling/
├── src/
│   ├── app/
│   │   ├── api/
│   │   │   ├── cars/
│   │   │   │   ├── route.js          # API danh sách xe
│   │   │   │   └── [id]/route.js     # API chi tiết xe
│   │   │   └── wishlist/
│   │   │       ├── route.js          # API wishlist
│   │   │       └── [id]/route.js     # API xóa wishlist
│   │   ├── cars/
│   │   │   ├── page.js               # Trang danh sách xe
│   │   │   └── [id]/page.js          # Trang chi tiết xe
│   │   ├── wishlist/
│   │   │   └── page.js               # Trang wishlist
│   │   ├── layout.js
│   │   └── page.js                   # Trang chủ
│   └── components/
│       ├── CarCard.js                # Component hiển thị xe
│       ├── CarList.js                # Component danh sách xe
│       └── Hero.js                   # Component hero section
├── data/
│   └── wishlist.json                 # File lưu wishlist
└── public/
    └── car-placeholder.jpg           # Ảnh placeholder
```

## 🚀 Cách chạy locally

1. **Clone repository**:

   ```bash
   git clone <repository-url>
   cd car-selling
   ```

2. **Cài đặt dependencies**:

   ```bash
   npm install
   ```

3. **Chạy development server**:

```bash
npm run dev
```

4. **Mở trình duyệt**: http://localhost:3000

## 🚀 Deploy lên Vercel

### Cách 1: Deploy trực tiếp từ GitHub

1. **Push code lên GitHub**
2. **Truy cập [Vercel](https://vercel.com)**
3. **Import project từ GitHub**
4. **Vercel sẽ tự động detect Next.js và deploy**

### Cách 2: Deploy bằng Vercel CLI

1. **Cài đặt Vercel CLI**:

   ```bash
   npm i -g vercel
   ```

2. **Login và deploy**:
   ```bash
   vercel login
   vercel
   ```

## 📱 Các trang chính

### 1. Trang chủ (`/`)

- Hero section với call-to-action
- Danh sách 6 xe nổi bật
- Navigation menu

### 2. Danh sách xe (`/cars`)

- Hiển thị tất cả xe
- Grid layout responsive
- Thông tin cơ bản: tên, giá, thương hiệu

### 3. Chi tiết xe (`/cars/[id]`)

- Thông tin đầy đủ về xe
- Ảnh lớn
- Nút "Thêm vào Wishlist"

### 4. Wishlist (`/wishlist`)

- Danh sách xe yêu thích
- Chức năng xóa xe khỏi wishlist
- Link đến trang chi tiết xe

### 5. Admin Dashboard (`/admin`)

- **Authentication**: Đăng nhập bảo mật với email/password
- **Protected Routes**: Tất cả trang admin được bảo vệ
- Tổng quan hệ thống với thống kê
- Quản lý users (CRUD operations) với password
- Quản lý lịch lái xe thử với các trạng thái
- Xác nhận/từ chối/hoàn thành lịch lái xe thử
- **Demo Account**: admin@carstore.com / admin123

## 🔧 API Endpoints

### Cars API

- `GET /api/cars` - Lấy danh sách tất cả xe
- `GET /api/cars/[id]` - Lấy thông tin chi tiết xe

### Wishlist API

- `GET /api/wishlist` - Lấy danh sách wishlist
- `POST /api/wishlist` - Thêm xe vào wishlist
- `DELETE /api/wishlist/[id]` - Xóa xe khỏi wishlist

### Test Drives API

- `POST /api/test-drives` - Đặt lịch lái xe thử

### Admin API

- `POST /api/admin/auth/login` - Đăng nhập admin
- `GET /api/admin/users` - Lấy danh sách users
- `POST /api/admin/users` - Thêm user mới
- `PUT /api/admin/users/[id]` - Cập nhật user
- `DELETE /api/admin/users/[id]` - Xóa user
- `GET /api/admin/test-drives` - Lấy danh sách lịch lái xe thử
- `PUT /api/admin/test-drives/[id]` - Cập nhật trạng thái lịch
- `DELETE /api/admin/test-drives/[id]` - Xóa lịch lái xe thử

## 🎨 UI/UX Features

- **Modern Design**: Sử dụng Tailwind CSS với thiết kế hiện đại
- **Responsive**: Tương thích mobile, tablet, desktop
- **Loading States**: Skeleton loading cho trải nghiệm tốt hơn
- **Error Handling**: Xử lý lỗi gracefully
- **Smooth Transitions**: Hiệu ứng hover và transition mượt mà

## 📊 Dữ liệu mẫu

Ứng dụng có sẵn 8 xe mẫu với thông tin đầy đủ:

- Toyota Camry 2.5G
- Honda Civic RS
- Mazda CX-5 2.0G
- Ford Ranger Wildtrak
- Hyundai Tucson G
- BMW X3 xDrive30e
- Mercedes-Benz C-Class
- Audi A4 2.0 TFSI

## 🔮 Tính năng có thể mở rộng

- **Authentication**: Đăng nhập/đăng ký
- **Search & Filter**: Tìm kiếm và lọc xe
- **Pagination**: Phân trang cho danh sách xe
- **Real Database**: Chuyển từ JSON sang database thực
- **Payment Integration**: Tích hợp thanh toán
- **Admin Panel**: Quản lý xe cho admin

## 📝 Lưu ý

- Đây là ứng dụng demo, dữ liệu được lưu trong JSON file
- Ảnh xe sử dụng Unsplash URLs
- Dễ dàng customize và mở rộng theo nhu cầu

## 🤝 Đóng góp

Mọi đóng góp đều được chào đón! Hãy tạo issue hoặc pull request.

## 📄 License

MIT License
