# KTT STORE - Ứng dụng Bán Quần áo thời trang

## 📝 Mô tả
KTT Store là dự án gồm ứng dụng bán quần áo thời trang trực tuyến được xây dựng bằng android studio và website cho admin quản lý với giao diện thân thiện và trải nghiệm mua sắm mượt mà.

## 🛠️ Công nghệ sử dụng
- Frontend: 
  - Android studio
  
- Backend:
  - Node.js
  - Express
  - MongoDB
  - Mongoose
  - JWT
  - Nodemailer
  - Cloudinary
  - PayOS
  - Socket.io

## ✨ Tính năng chính

### 👤 Người dùng
- Đăng ký, đăng nhập, quên mật khẩu
- Xem và tìm kiếm sản phẩm theo danh mục, giới tính
- Quản lý giỏ hàng và thanh toán
- Theo dõi đơn hàng và lịch sử mua hàng
- Đánh giá sản phẩm
- Quản lý thông tin cá nhân và địa chỉ
- Sử dụng mã giảm giá
- Theo dõi sản phẩm yêu thích
- Nhận thông báo về khuyến mãi và đơn hàng

### 👨‍💼 Quản trị viên
- Quản lý sản phẩm (thêm, sửa, xóa, cập nhật tồn kho)
- Quản lý đơn hàng
- Quản lý khuyến mãi và mã giảm giá
- Quản lý người dùng
- Quản lý thông báo
- Xem thống kê và báo cáo

## 🚀 Hướng dẫn cài đặt

### Yêu cầu hệ thống
- Node.js phiên bản 18.x trở lên
- MongoDB phiên bản 6.x trở lên
- Git

### Các bước cài đặt

1. Clone repository
```bash
git clone https://github.com/WiniFyCode/KTTStore-React.git
cd KTTStore-React
```

2. Mở Terminal 1 và chạy lệnh để cài đặt dependencies cho client ( ctrl + shift + `)
```bash
cd client
npm install
```
3. Mở Terminal 2 và chạy lệnh để cài đặt dependencies cho server ( ctrl + shift + `)
```bash
cd server
npm install
```

4. Cấu hình database
- Tạo database MongoDB mới
- Copy file `.env.example` thành `.env` trong thư mục server
- Cập nhật thông tin kết nối MongoDB trong file `.env`:
  ```
  MONGODB_URI=mongodb+srv://<username>:<password>@<cluster>.mongodb.net/<database>?retryWrites=true&w=majority&appName=<appName> 
  ```

5. Khởi chạy ứng dụng

Chạy server:
```bash
cd server
npm run dev
```

Chạy client:
```bash
cd client
npm run dev
```

Ứng dụng sẽ chạy tại:
- Frontend: http://localhost:5037
- Backend: http://localhost:5000

## 📁 Cấu trúc thư mục

### 🖥️ Frontend (client)
```
kttstore-android/
├── app/
│   ├── build/
│   │   └── ... (build artifacts)
│   ├── libs/
│   │   └── ... (external libraries)
│   ├── src/
│   │   ├── androidTest/
│   │   │   └── ... (instrumentation tests)
│   │   ├── main/
│   │   │   ├── java/
│   │   │   │   └── com/
│   │   │   │       └── example/
│   │   │   │           └── kttstore/
│   │   │   │               ├── activity/      <-- Your focus area
│   │   │   │               │   ├── AddressEditActivity.java
│   │   │   │               │   ├── ... (Other Activities)
│   │   │   │               │   └── AddressEditActivity.class (compiled)
│   │   │   │               ├── adapter/       
│   │   │   │               │   ├── ... (RecyclerView Adapters)
│   │   │   │               ├── Authentication/     
│   │   │   │               │   ├── ... (forgotPassword, login, register)
│   │   │   │               ├── MenuFragment/     
│   │   │   │               │   ├── ... (Fragments)
│   │   │   │               ├── model/         
│   │   │   │               │   ├── Product.java
│   │   │   │               │   ├── User.java
│   │   │   │               │   └── ... (Data Models)
│   │   │   │               ├── Layout/    
│   │   │   │               │   ├── ... (Bottom Navigation Activity)
│   │   │   │               ├── Utils/      
│   │   │   │               │    └── ... (utility classes)
│   │   │   │               ├── SERVER.java
│   │   │   │               └── SplashActivity.java
│   │   │   ├── res/
│   │   │   │   ├── layout/
│   │   │   │   │   ├── activity_address_edit.xml
│   │   │   │   │   └── ... (Layout files)
│   │   │   │   ├── values/
│   │   │   │   │   ├── colors.xml
│   │   │   │   │   ├── strings.xml
│   │   │   │   │   └── ... (Other value resources)
│   │   │   │   ├── drawable/
│   │   │   │   │   └── ... (Image assets)
│   │   │   │   ├── mipmap/
│   │   │   │   │   └── ... (Launcher icons)
│   │   │   │   └── ... (Other resource types)
│   │   │   └── AndroidManifest.xml
│   │   └── test/
│   │       └── ... (unit tests)
│   └── ...
├── gradle/
│   └── ... (gradle wrapper)
├── build.gradle
├── gradle.properties
├── settings.gradle
└── ... (other project files)
```

### ⚙️ Backend (server)
```
server/
├── controllers/                # Route controllers
│   ├── AuthController.js
│   ├── ProductController.js
│   └── ...
│
├── data/                       # Static data/seeds
│   └── trainingData.js
│
├── mail/                       # Email templates & handlers
│   ├── EmailController.js
│   └── templates/
│
├── middlewares/                # Custom middlewares
│   ├── auth.js
│   └── ...
│
├── models/                     # Database models
│   ├── User.js
│   ├── Product.js
│   └── ...
│
├── routes/                     # API routes
│   ├── auth.js
│   ├── products.js
│   └── ...
│
├── uploads/                    # Uploaded files
│
├── utils/                      # Utility functions
│
├── .env                        # Environment variables
├── .gitignore                  # Git ignore file
├── package.json                # Dependencies
└── server.js                   # Entry point
```

## 🤝 Đóng góp
Mọi đóng góp đều được chào đón! Vui lòng:
1. Fork repository
2. Tạo branch mới 
3. Commit changes
4. Push to branch 
5. Tạo Pull Request

## 📝 License
Dự án được phân phối dưới giấy phép MIT. Xem `LICENSE` để biết thêm thông tin.

## 📧 Liên hệ
- Email: nguyenduykhoi45@gmail.com
- GitHub: [@NguyenDuyKhoi98](https://github.com/NguyenDuyKhoi98)
- Link báo cáo Word, Powerpoint: https://drive.google.com/drive/folders/1GtXYQeIi-e0vXXUtFSE8ShCbm4vwfV8h?usp=drive_link