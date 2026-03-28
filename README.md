# Lapakly
Platform pencarian & pemesanan UMKM terdekat berbasis lokasi. Dibangun dengan React + Vite, terhubung ke backend Laravel yang sudah live.

# Fitur utama
👤 Auth & User
Login & Register
Logout
Edit Profile (nama, email, no hp, password)
Forgot Password & Reset Password

🛍️ Buyer
Lihat daftar toko
Detail toko + daftar produk
Search produk di dalam toko 🔍
Tambah ke keranjang
Checkout & lihat pesanan
Chat dengan penjual 💬

🏪 Seller
Dashboard penjual
Kelola produk
Kelola toko
Update status pesanan:
accepted → preparing → completed

💬 Chat
Chat antara pembeli & penjual per toko
Auto refresh (realtime sederhana)
Notifikasi pesan masuk

🎨 UI/UX
Design modern & clean
Konsisten dengan branding:
Primary: #006633
Secondary: #339933
Font:
Heading: Retrograde Regular
Body: Work Sans
Responsive (mobile & desktop)

🛠️ Tech Stack
React (Vite)
React Router
Context API
CSS Module
React Hot Toast

# Struktur Project
umkm-frontend/
├── public/
│   └── favicon.svg
├── src/
│   ├── components/
│   │   ├── common/       # Button, Input, Loading, Badge, BottomNav, SideNav, ThemeToggle
│   │   ├── cart/         # CartItem
│   │   ├── order/        # OrderCard
│   │   ├── product/      # ProductCard
│   │   └── store/        # StoreCard
│   │   └── chat/        # ChatBubble, ChatInput
│   ├── context/          # AuthContext, CartContext, ThemeContext
│   ├── hooks/            # useLocation
│   ├── mocks/            # Data dummy untuk testing tanpa backend
│   ├── pages/
│   │   ├── auth/         # Login, Register, ResetPassword, ForgotPassword
│   │   ├── buyer/        # Home, Explore, StoreDetail, Cart, Checkout, Order Detail, Profile, Chat, Order List, Store Detail
│   │   └── seller/       # Dashboard, Products, Store, Finance, Chat
│   ├── routes/           # PrivateRoute, SellerRoute
│   ├── services/         # api, auth, store, product, cart, order, chat
│   └── utils/            # constants, formatCurrency, calculateDistance, excelexcelExport
│   └── App.jsx
│   └── Index
│   └── main.jsx
├── .env.example
├── .gitignore
├── index.html
├── package.json
├── package-lock.json
├── README.md
├── replaceColors.js
└── vite.config.js

# Instalasi & Menjalankan project
1. Install dependencies
   npm install

2. Buat file .env
    cp .env.example .env
   
4. Sesuaikan isi .env
    VITE_MOCK_MODE=false (Kalau pakai backend) /   VITE_MOCK_MODE=true (tanpa         backend)
    VITE_API_BASE_URL=http://umkm-platform.my.id/api
    VITE_APP_NAME=Lapakly

5. Jalankan
    npm run dev

5. Buka browser
   http://localhost:5173

6. login harus daftar akun dulu baru bisa masuk

# Catatan
 - Backend perlu support fitur preparing status
 - Chat masih menggunakan polling (bukan websocket)
 - Notifikasi pesan berbasis frontend

    
