# Weather Dashboard - Android Auto

Ứng dụng hiển thị thông tin thời tiết trên Android Auto dashboard.

## Tính năng

- 📍 Hiển thị thời tiết theo vị trí hiện tại
- 🌡️ Nhiệt độ, độ ẩm, tốc độ gió
- 🌤️ Dự báo thời tiết 5 ngày
- 🗺️ Hỗ trợ nhiều địa điểm
- 🔄 Cập nhật dữ liệu tự động

## Yêu cầu

- Android Studio 2022.1+
- Android SDK 31+
- API Key từ OpenWeatherMap (miễn phí)

## Cài đặt

### 1. Clone repository
```bash
git clone https://github.com/soin29106-ui/Android-auto.git
cd Android-auto
```

### 2. Lấy API Key
- Truy cập: https://openweathermap.org/api
- Đăng ký tài khoản miễn phí
- Copy API Key

### 3. Cấu hình API Key
Mở file `app/src/main/res/values/strings.xml` và thêm:
```xml
<string name="weather_api_key">YOUR_API_KEY_HERE</string>
```

### 4. Mở trong Android Studio
- File → Open → Chọn folder Android-auto
- Chờ Gradle sync hoàn tất
- Chạy trên emulator hoặc thiết bị

### 5. Chạy ứng dụng
```bash
./gradlew assembleDebug
./gradlew installDebug
```

## Cấu trúc dự án

```
app/
├── src/
│   ├── main/
│   │   ├── AndroidManifest.xml
│   │   ├── java/com/weather/
│   │   │   ├── MainActivity.kt
│   │   │   ├── api/WeatherService.kt
│   │   │   ├── model/Weather.kt
│   │   │   ├── ui/WeatherFragment.kt
│   │   │   └── util/LocationManager.kt
│   │   └── res/
│   │       ├── layout/
│   │       ├── values/
│   │       └── drawable/
│   └── test/
├── build.gradle
└── settings.gradle
```

## Sử dụng

1. **Khởi động ứng dụng** trên Android Auto
2. **Cho phép quyền truy cập vị trí**
3. **Xem thông tin thời tiết** hiện tại
4. **Vuốt sang** để xem dự báo

## API được sử dụng

- **OpenWeatherMap Current Weather API**
- **OpenWeatherMap Forecast API**

Endpoint: `https://api.openweathermap.org/data/2.5/`

## Dependencies

- Retrofit 2.9+
- Coroutines
- Android Car Library
- Jetpack Compose (UI)

## Troubleshooting

### Lỗi: "Permission denied"
→ Vào Settings → Cho phép quyền vị trí

### Lỗi: "Invalid API Key"
→ Kiểm tra lại API Key trong strings.xml

### Không hiển thị dữ liệu
→ Kiểm tra kết nối Internet
→ Xem logcat: `adb logcat | grep Weather`

## Liên hệ

Tác giả: soin29106-ui
License: MIT
