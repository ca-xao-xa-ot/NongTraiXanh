# 🌾 Nông Trại Xanh (Green Farm) - Healing 2D Game

![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)
![Firebase](https://img.shields.io/badge/firebase-ffca28?style=for-the-badge&logo=firebase&logoColor=black)
![Netlify](https://img.shields.io/badge/netlify-%23000000.svg?style=for-the-badge&logo=netlify&logoColor=#00C7B7)

> **"Chữa lành tâm hồn sau những giờ học tập và làm việc căng thẳng."** 🌿
> 
> Đồ án Game mô phỏng Nông trại 2D được xây dựng bằng **Flutter thuần** (sử dụng `CustomPainter`), không dùng Game Engine. Game có đồ họa Cute Pastel, hiệu ứng mượt mà và tính năng lưu trữ đám mây Real-time.

---

## 🎮 Trải nghiệm ngay (Live Demo)
👉 **Chơi trực tiếp trên Web (PC/Mobile):** [https://gamenongtraixanh.netlify.app/](https://gamenongtraixanh.netlify.app/)

---

## ✨ Điểm nhấn Giao diện (UI/UX Cải tiến)
Giao diện được thiết kế theo phong cách **Cute Pastel** cực kỳ đáng yêu:
* 🎨 **Hiệu ứng Glass-morphism:** Các bảng HUD, Thanh EXP và thanh công cụ (Toolbar) có hiệu ứng kính mờ, đổ bóng (shadow glow) đa sắc.
* 🌟 **Background động:** Màn hình đăng nhập và NPC giới thiệu có mây bay, sao lấp lánh và hiệu ứng nảy (bounce animation) sống động.
* 🔔 **Tương tác mượt mà:** Nút bấm Gradient, Toast notification xanh mát, và Inventory Chips thông minh chỉ hiện khi có vật phẩm.

---

## 🌻 Hệ thống Nông trại & Chăn nuôi Đa dạng
Người chơi có thể tương tác (Cuốc, Gieo, Tưới, Thu hoạch) với hệ thống cây trồng và vật nuôi phong phú, mở khóa theo Cấp độ (Level):

### 🌱 Cây Trồng
Ngoài các cây cơ bản, cập nhật bổ sung 5 loại cây trồng giá trị cao:
- 🥬 **Bắp Cải:** (Lv 3) - Thu hoạch: 70🪙
- 🌶️ **Ớt:** (Lv 11) - Thu hoạch: 115🪙
- 💜 **Oải Hương:** (Lv 14) - Thu hoạch: 130🪙
- 🍑 **Đào:** (Lv 20) - Thu hoạch: 160🪙
- 🫐 **Việt Quất:** (Lv 16) - Thu hoạch: 180🪙

### 🐾 Vật Nuôi (Tích hợp AI Roaming)
Vật nuôi di chuyển tự do, biết đói và đẻ ra nông sản. Cập nhật 3 loài mới:
- 🦃 **Gà Tây:** (Lv 12) - Cho Trứng lớn 🥚 (55🪙/lần)
- 🦚 **Công:** (Lv 22) - Cho Lông đuôi 🪶 (130🪙/lần)
- 🐴 **Ngựa:** (Lv 25) - Cho Sữa ngựa 🥛 (150🪙/lần)

---

## 🏠 Ngôi Nhà Nâng Cấp (House System)
Khu vực Nhà ở với hàng loạt tương tác thú vị giúp gia tăng trải nghiệm:
- 🍳 **Bếp Nấu Ăn (Cooking System):** Nấu ăn để nhận các Buff lợi ích:
  - 🥗 *Salad Tươi* → +10% Tốc độ thu hoạch
  - 🍲 *Canh Rau* → +20 Năng lượng
  - 🍰 *Bánh Dâu* → +50 EXP thưởng
  - 🎃 *Bí Ngô Nướng* → +100 Vàng
  - 🍯 *Sữa Mật Ong* → +30% Năng suất vật nuôi
- 🐱 **Pet Mèo Kitty:** Vuốt ve để nhận những thông điệp dễ thương.
- 📺 **Tương tác khác:** Bật/Tắt nhạc nền 🎵, Xem Bản tin nông trại trên Tivi, Đọc mẹo chơi ở Kệ sách 📚, Xem Thống kê 📊.

---

## 🛠️ Công nghệ sử dụng (Tech Stack)
* **Frontend:** Flutter & Dart.
* **Đồ họa Render:** Thư viện `CustomPainter` vẽ vòng đời cây trồng đạt 60 FPS.
* **Quản lý Trạng thái:** Kiến trúc `Provider`.
* **Backend & Lưu trữ:** Firebase Firestore (Cloud Save Real-time) & Firebase Authentication.

---

## 🚀 Hướng dẫn cài đặt (Installation)
Clone dự án về máy và chạy thông qua Terminal:

```bash
# 1. Clone code
git clone [https://github.com/ca-xao-xa-ot/NongTraiXanh.git](https://github.com/ca-xao-xa-ot/NongTraiXanh.git)

# 2. Cài đặt thư viện
flutter pub get

# 3. Chạy game (Khuyên dùng trên Chrome)
flutter run -d chrome
```
---

## 📸 Hình ảnh Game (Screenshots)
<img width="454" height="321" alt="Picture1 2" src="https://github.com/user-attachments/assets/cb4caea3-9fa2-4d7e-9ae4-2a55ef712047" />

<img width="454" height="314" alt="Picture3" src="https://github.com/user-attachments/assets/2e299412-ea32-4491-a113-d8de6127c933" />
<img width="454" height="313" alt="Picture5" src="https://github.com/user-attachments/assets/e436c4c1-a3d3-4f77-9222-ca582ebc93f8" />
<img width="454" height="313" alt="Picture4" src="https://github.com/user-attachments/assets/9421cdbf-e2a2-4d63-90ec-b37d63d99a6e" />
<img width="454" height="316" alt="Picture7" src="https://github.com/user-attachments/assets/4f195968-6299-4c50-8f89-87b3d2508596" />

<img width="454" height="313" alt="Picture8" src="https://github.com/user-attachments/assets/f8eba376-6a23-4785-830e-4030f9d7d98e" />

👥 ĐỘI NGŨ PHÁT TRIỂN (Team 6)
Sản phẩm là Đồ án Học phần Lập trình di động, được thực hiện bằng cả tâm huyết bởi:

Ngô Thị Minh Phương (MSSV: 23012156)

Nguyễn Thị Thu (MSSV: 23010871)

Giảng viên hướng dẫn: TS. Trịnh Thanh Bình

💖 Cảm ơn thầy và các bạn đã dành thời gian khám phá Nông Trại Xanh. Chúc mọi người có những phút giây thư giãn thật tuyệt vời!

