# Tutoring Platform

Nền tảng quản lý gia sư và khóa học trực tuyến toàn diện, kết nối giáo viên và học sinh một cách hiệu quả.

## Mục đích

CNPM Tutoring Platform là một ứng dụng web tiên tiến giúp:

- **Học sinh**: Tìm kiếm gia sư, đăng ký khóa học, xem tài liệu và quản lý lịch học
- **Gia sư**: Quản lý học sinh, lập lịch dạy học, đăng ký khóa tư vấn
- **Quản trị viên**: Quản lý người dùng, khóa học, phiên hội thoại và tài liệu

## Tính năng chính

### Cho Học sinh

- Xem danh sách gia sư có sẵn
- Xem và quản lý các phiên học
- Tải về và xem tài liệu học
- Cập nhật hồ sơ cá nhân
- Đăng ký khóa học mới

### Cho Gia sư

- Quản lý danh sách học sinh
- Lập lịch dạy học
- Đăng ký khóa tư vấn
- Xem nội dung phiên học
- Tải lên tài liệu giảng dạy

### Cho Quản trị viên

- Quản lý người dùng (Gia sư, Học sinh)
- Quản lý phiên hội thoại
- Phê duyệt gia sư mới
- Quản lý tài liệu
- Thống kê và báo cáo

## Công nghệ sử dụng

### Frontend

- **React 19** - Thư viện UI
- **Vite 7** - Build tool & Dev server
- **React Router 7** - Định tuyến
- **Material-UI (MUI 7)** - Component library
- **Framer Motion** - Animation
- **Dayjs** - Xử lý ngày tháng
- **Lucide React** - Icon library

### Build & Development

- **ESLint** - Linting
- **Babel/SWC** - Transpiling

## Cấu trúc dự án

```
src/
├── components/          # Các component tái sử dụng
│   ├── Buttons/        # Component nút bấm
│   ├── Tables/         # Component bảng
│   ├── dashboard/      # Dashboard components
│   └── ...
├── pages/              # Các trang chính
│   ├── Admin/          # Trang quản trị
│   ├── Student/        # Trang học sinh
│   ├── Tutor/          # Trang gia sư
│   ├── AccountSetting/ # Cài đặt tài khoản
│   └── ...
├── context/            # React Context (Auth, Session, Toast)
├── hooks/              # Custom React hooks
├── layouts/            # Layout templates
├── routes/             # Router configuration
├── data/               # Mock data
├── utils/              # Utility functions
└── styles/             # CSS files
```

## Hướng dẫn cài đặt

### Yêu cầu

- Node.js 16+
- npm hoặc yarn

### Cài đặt

1. **Clone repository**

   ```bash
   git clone https://github.com/lonangyyn/tutor-student-web
   cd CNPM
   ```

2. **Cài đặt dependencies**

   ```bash
   npm install
   ```

3. **Chạy development server**

   ```bash
   npm run dev
   ```

   Ứng dụng sẽ mở tại `http://localhost:5173`

4. **Build cho production**

   ```bash
   npm run build
   ```

5. **Preview build**
   ```bash
   npm run preview
   ```

## 👥 Tài khoản test

Sử dụng các tài khoản sau để test:

| Email              | Mật khẩu | Vai trò       |
| ------------------ | -------- | ------------- |
| admin@example.com  | 123      | Quản trị viên |
| tutor@gmail.com    | 123      | Gia sư        |
| student@gmail.com  | 123      | Học sinh      |
| kieuminh@gmail.com | 123      | Admin         |

## Routing

### Public Routes

- `/` - Trang chủ
- `/login` - Đăng nhập

### Protected Routes (Cần đăng nhập)

- `/home` - Dashboard
- `/studentList` - Danh sách học sinh
- `/management` - Quản lý chung
- `/studentManagement` - Quản lý học sinh
- `/sessionManagement` - Quản lý phiên
- `/tutorManagement` - Quản lý gia sư
- `/tutorPendingList` - Danh sách gia sư chờ duyệt
- `/registerTutor` - Đăng ký gia sư
- `/sessions` - Xem phiên học
- `/documents` - Xem tài liệu
- `/tutorSchedule` - Lịch gia sư
- `/dashboard` - Bảng điều khiển
- `/settings` - Cài đặt tài khoản
- Và nhiều route khác...

## Linting

Kiểm tra code quality:

```bash
npm run lint
```

## Ghi chú phát triển

- Ứng dụng sử dụng **React Context** để quản lý state toàn cục (Auth, Session, Toast)
- Hiện tại sử dụng **mock data** - cần kết nối với backend API
- Hỗ trợ **Responsive Design** cho tất cả thiết bị
- Sử dụng Material-UI theme cho giao diện nhất quán

## Authentication

Hệ thống sử dụng:

- **AuthContext** để quản lý trạng thái đăng nhập
- **ProtectedRoute** để bảo vệ các trang riêng tư
- Mock login API hiện tại - cần thay thế bằng backend thực

## Styling

- CSS modules cho các component cụ thể
- Material-UI `sx` prop cho styling inline
- Tailored theme tùy chỉnh

## Responsive Design

Giao diện tự động thích ứng với:

- Desktop
- Tablet
- Mobile

## Đóng góp

1. Tạo branch mới cho feature: `git checkout -b feature/TenFeature`
2. Commit thay đổi: `git commit -m 'Thêm feature mới'`
3. Push lên branch: `git push origin feature/TenFeature`
4. Tạo Pull Request

## License

Dự án này được tạo cho mục đích học tập và phát triển.

## Liên hệ & Hỗ trợ

Để báo cáo lỗi hoặc đề xuất tính năng, vui lòng tạo issue trên repository.

---

**Last Updated:** 2026-04-27
