# 🌾 Nông Trại Xanh (Green Farm) - 2D Healing Game

![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)
![Firebase](https://img.shields.io/badge/firebase-ffca28?style=for-the-badge&logo=firebase&logoColor=black)
![Netlify](https://img.shields.io/badge/netlify-%23000000.svg?style=for-the-badge&logo=netlify&logoColor=#00C7B7)

**Nông Trại Xanh** là game nông trại 2D viết bằng Flutter, lấy cảm hứng từ phong cách *Stardew Valley*. Người chơi tiếp nhận mảnh đất từ bà ngoại, dần dần xây dựng nông trại, chăm sóc vật nuôi, câu cá, hoàn thành nhiệm vụ hằng ngày và leo cấp để mở khóa cây trồng & vật nuôi mới.

---

> **"Chữa lành tâm hồn - Thử thách công nghệ."** 🌿
>
> Không chỉ dừng lại ở một tựa game mang nhịp độ chậm rãi giúp gác lại âu lo, Nông Trại Xanh còn là một bài toán công nghệ đầy thách thức. Bằng việc tối ưu triệt để **Flutter thuần**, nhóm đã "hô biến" một nền tảng thiết kế giao diện thành một cỗ máy vận hành Game 2D mượt mà ở mức 60FPS. Một hệ sinh thái hoàn chỉnh được dựng lên từ những dòng code nguyên bản nhất, hoàn toàn không phụ thuộc vào bất kỳ Game Engine đồ sộ nào.

---

## 🎮 Trải nghiệm ngay (Live Demo)
👉 **Chơi trực tiếp trên Web (PC hoặc điện thoại):** [https://gamenongtraixanh.netlify.app/](https://gamenongtraixanh.netlify.app/)

---

## 🔥 NHỮNG ĐIỂM SÁNG KỸ THUẬT (Technical Highlights)
Đây là những kỹ thuật cốt lõi giúp game vận hành mượt mà trên trình duyệt web dù chứa hàng trăm luồng dữ liệu phức tạp:

* 🎨 **Engine-less Rendering (Không dùng Game Engine):** 100% bản đồ (Grid), nhân vật, và vòng đời sinh trưởng của thực vật được tự vẽ bằng thư viện `CustomPainter` kết hợp Canvas của Flutter.
* ⚡ **State Management Đỉnh cao:** Ứng dụng kiến trúc `ChangeNotifierProvider` để quản lý hàng trăm trạng thái đồng thời (tọa độ nhân vật, vòng đời ô đất, túi đồ, trạng thái vật nuôi...) mà UI không hề bị giật lag (rebuild cục bộ).
* ☁️ **Thuật toán Debounce Save (Tối ưu API):** Thay vì lưu liên tục lên đám mây gây nghẽn mạng và tốn phí Firebase, game lưu tạm vào Local và chỉ "đẩy" đồng bộ lên Firestore mỗi **3 giây/lần** sau thao tác cuối cùng.
* 🤖 **AI Chăn Nuôi (Roaming Logic):** Đàn vật nuôi (Gà, Bò, Cừu, Ngựa...) được lập trình AI di chuyển ngẫu nhiên ngộ nghĩnh, biết "đói" và tự động kích hoạt cơ chế sinh sản nông sản khi được người chơi cho ăn.

---

## 🌻 HỆ THỐNG GAMEPLAY CHI TIẾT

### 1. Trồng trọt & Chu kỳ Ngày Đêm 🌞🌛
Hệ thống logic nông nghiệp chặt chẽ với 4 giai đoạn sinh trưởng.
- **Tương tác Đất:** Cuốc đất tơi xốp ➡️ Gieo hạt (Hơn 10 loại hạt giống cấp độ từ Dâu tây đến Oải Hương, Việt Quất) ➡️ Tưới nước ➡️ Thu hoạch.
- **Phép màu thời gian:** Chu kỳ Ngày/Đêm tự động chuyển đổi. Giao diện (UI) và Âm thanh (Audio Service) tự động thay đổi từ nhạc nền vui nhộn (Ban ngày) sang tĩnh lặng, êm dịu (Ban đêm). Cây cối và vật nuôi chỉ phát triển khi có sự chuyển giao thời gian.

### 2. Ngôi nhà Đa nhiệm (Interactive House) 🏠
Không chỉ để trang trí, Ngôi nhà là một "cỗ máy" tăng cường sức mạnh:
- **Hệ thống Nấu Ăn (Cooking Buffs):** Tự do chế biến nông sản thành các món ăn mang lại hiệu ứng đặc biệt:
  - *Salad Tươi* (+10% Tốc độ thu hoạch) | *Bí Ngô Nướng* (+100 Vàng) | *Sữa Mật Ong* (+30% Năng suất thú).
- **Tương tác Môi trường:** Xem tin tức trên Tivi, đọc mẹo ở Kệ sách, bật/tắt BGM, hoặc vuốt ve Mèo Kitty để nhận lời chúc dễ thương.

### 3. Cửa hàng, Túi đồ & Kinh tế 🏪
- **Hệ thống Level:** Các loại Hạt giống và Thú cưng giá trị cao (Ngựa, Công) bị khóa, chỉ mở khi người chơi cày đủ Điểm Kinh Nghiệm (EXP).
- **Túi đồ thông minh:** Inventory dạng Chips, tự động phân loại, chỉ hiển thị những vật phẩm bạn đang sở hữu.

### 4. Nhiệm vụ & Xếp hạng Toàn cầu 🏆
- **Nhiệm vụ ngẫu nhiên (Daily Quests):** Mỗi ngày hệ thống sẽ Random các nhiệm vụ (Câu cá, Thu hoạch) để người chơi cày Vàng và EXP.
- **Bảng vàng (Leaderboard Real-time):** Dữ liệu được kéo trực tiếp từ Firebase liên tục, tôn vinh Top 20 tỷ phú nông dân chăm chỉ nhất server!

---

## 🎨 GIAO DIỆN (UI/UX)
Giao diện được trau chuốt tỉ mỉ theo phong cách **Cute Pastel - Glassmorphism**:
- Nút bấm Gradient đa sắc phát sáng (Glow).
- Màn hình NPC và đăng nhập có hiệu ứng mây trôi, sao lấp lánh và animation nổi bồng bềnh (Bounce effect).
- Hiệu ứng Toast Notification và Badge cấp độ cực kỳ nịnh mắt.

---

## 🚀 HƯỚNG DẪN CÀI ĐẶT (Installation)

```bash
# 1. Clone Source Code
git clone [https://github.com/ca-xao-xa-ot/NongTraiXanh.git](https://github.com/ca-xao-xa-ot/NongTraiXanh.git)

# 2. Cài đặt các gói thư viện Flutter
flutter pub get

# 3. Chạy game (Khuyên dùng trình duyệt Chrome)
flutter run -d chrome
```

## 📸 Hình ảnh Game (Screenshots)
<div align="center">
<img width="45%" alt="Screenshot 1" src="https://github.com/user-attachments/assets/cb4caea3-9fa2-4d7e-9ae4-2a55ef712047" />
<img width="45%" alt="Screenshot 2" src="https://github.com/user-attachments/assets/2e299412-ea32-4491-a113-d8de6127c933" />
<img width="45%" alt="Screenshot 3" src="https://github.com/user-attachments/assets/e436c4c1-a3d3-4f77-9222-ca582ebc93f8" />
<img width="45%" alt="Screenshot 4" src="https://github.com/user-attachments/assets/9421cdbf-e2a2-4d63-90ec-b37d63d99a6e" />
<img width="45%" alt="Screenshot 5" src="https://github.com/user-attachments/assets/4f195968-6299-4c50-8f89-87b3d2508596" />
<img width="45%" alt="Screenshot 6" src="https://github.com/user-attachments/assets/f8eba376-6a23-4785-830e-4030f9d7d98e" />
</div>




## 👨‍💻 Thông tin sinh viên
**Sản phẩm là Đồ án cơ sở, được thực hiện bằng cả tâm huyết bởi:**

**Nguyễn Thị Thu Giang** (MSSV: 23010871)

**Ngô Thị Minh Phương** (MSSV: 23012156)

Giảng viên hướng dẫn: **TS. Trịnh Thanh Bình**

💖 Cảm ơn thầy và các bạn đã dành thời gian khám phá Nông Trại Xanh. Chúc mọi người có những phút giây thư giãn thật tuyệt vời!
