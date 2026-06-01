# ShopApp — Mobile E-Commerce Application
### MAD Semester Project | 6th Semester | Section AI

**Students:**
- Muhammad Murtaza — 23MDBCS443
- Izaz Akbar — 23MDBCS436

---

## 🚀 How to Run

### Prerequisites
- Flutter SDK (3.0+)
- Android Studio with Flutter & Dart plugins
- Android Emulator or physical device

### Steps
```bash
# 1. Open project in Android Studio
# 2. Run pub get
flutter pub get

# 3. Run on emulator
flutter run
```

### Demo Login
- **Email:** demo@example.com
- **Password:** demo123

---

## 📱 App Screens

| Screen | Description |
|--------|-------------|
| Login | Email/password authentication |
| Register | New user sign-up |
| Home | Featured products, categories, banner |
| Products | Search, filter by category, grid view |
| Product Detail | Full details, rating, add to cart |
| Cart | Items, quantity control, total |
| Checkout | Shipping address + payment method |
| Order Success | Confirmation screen |
| Orders | Order history with status |
| Profile | User info, stats, settings |

---

## 🏗️ Architecture

```
Flutter App (Client)
    ↓
Provider (State Management)
    ↓
Models (User, Product, Cart, Order, Payment)
    ↓
Mock Data (Local — no backend connected)
```

### Design Patterns Used
- **Provider Pattern** — State management
- **Repository Pattern** — Data access through providers
- **MVC** — Model-View separation via screens/providers/models

---

## 📦 Dependencies

| Package | Use |
|---------|-----|
| provider | State management |
| shared_preferences | Local storage |
| http | HTTP requests (ready for backend) |
| cached_network_image | Image caching |
| flutter_rating_bar | Star ratings |
| badges | Cart count badge |

---

## 📊 Class Diagram

```
User ──────────────────── Cart
(userID, name,           (cartID, userID,
 email, password)         productList[])
      │                        │
      │ 1:many                 │ 1:many
      ▼                        ▼
    Order ──────────── Product
(orderID, totalAmount,  (productID, name,
 status, items[])        price, description)
      │
      │ 1:1
      ▼
   Payment
(paymentID, method,
 status, amount)
```

---

## 🔮 Future Enhancements
- [ ] Real backend (Node.js + MongoDB)
- [ ] Firebase authentication
- [ ] Push notifications
- [ ] Payment gateway integration (Stripe)
- [ ] Product reviews & ratings
- [ ] Wishlist / favorites
- [ ] Dark mode

---

*Project for Mobile Application Development (MAD) course*
