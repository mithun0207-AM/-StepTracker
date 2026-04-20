<div align="center">

<img src="art/banner.png" alt="StepTracker Banner" width="100%"/>

# 👣 StepTracker

### Production-Grade Android Fitness App

[![Android](https://img.shields.io/badge/Platform-Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)](https://android.com)
[![Kotlin](https://img.shields.io/badge/Kotlin-2.0.21-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white)](https://kotlinlang.org)
[![Jetpack Compose](https://img.shields.io/badge/Jetpack_Compose-Latest-4285F4?style=for-the-badge&logo=jetpackcompose&logoColor=white)](https://developer.android.com/jetpack/compose)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)
[![API](https://img.shields.io/badge/Min_API-26-orange?style=for-the-badge)](https://android-arsenal.com/api?level=26)

**A clean, modern step tracking app built with the latest Android tech stack.**  
*Real-world architecture • Offline-first • Beautiful UI*

[📱 Download APK](#-download) • [🏗️ Architecture](#-architecture) • [✨ Features](#-features) • [🚀 Getting Started](#-getting-started)

</div>

---

## 📸 Screenshots

<div align="center">
<table>
  <tr>
    <td align="center"><b>🏠 Home</b></td>
    <td align="center"><b>📊 Weekly Stats</b></td>
    <td align="center"><b>📅 History</b></td>
    <td align="center"><b>⚙️ Settings</b></td>
  </tr>
  <tr>
    <td><img src="screenshots/home.png" width="200"/></td>
    <td><img src="screenshots/stats.png" width="200"/></td>
    <td><img src="screenshots/history.png" width="200"/></td>
    <td><img src="screenshots/settings.png" width="200"/></td>
  </tr>
</table>
</div>

> 📷 *Add your own screenshots by taking them on your device and placing them in the `screenshots/` folder*

---

## ✨ Features

- 🦶 **Real-time Step Tracking** — Uses Android's built-in step counter sensor for accurate, battery-efficient tracking
- 📊 **Beautiful Analytics** — Weekly & monthly charts powered by Vico, visualizing your fitness journey
- 💾 **Offline-First** — All data stored locally with Room database. Works without internet
- 🎨 **Material You Design** — Fully supports dynamic theming and Dark/Light mode
- ⚡ **Optimized Performance** — Kotlin Coroutines + Flow for smooth, reactive UI
- 🔔 **Daily Goals** — Set personal step goals and track your progress
- 📅 **History View** — Browse all your past activity with detailed breakdowns

---

## 🏗️ Architecture

This project follows **Clean Architecture** with **MVVM** pattern — the same architecture used in production apps at top tech companies.

```
📦 StepTrackerApp
 ┣ 📂 data
 ┃ ┣ 📂 local          → Room Database, DAOs, Entities
 ┃ ┣ 📂 repository     → Repository implementations
 ┃ ┗ 📂 datastore      → User preferences (DataStore)
 ┣ 📂 domain
 ┃ ┣ 📂 model          → Business models
 ┃ ┣ 📂 repository     → Repository interfaces
 ┃ ┗ 📂 usecase        → Business logic use cases
 ┗ 📂 presentation
   ┣ 📂 home           → Home screen UI + ViewModel
   ┣ 📂 history        → History screen UI + ViewModel
   ┣ 📂 stats          → Stats screen UI + ViewModel
   ┗ 📂 settings       → Settings screen UI + ViewModel
```

### Why Clean Architecture?
- ✅ **Testable** — Each layer can be tested independently
- ✅ **Scalable** — Easy to add new features without breaking existing ones
- ✅ **Maintainable** — Clear separation of concerns
- ✅ **Industry Standard** — Used by Flipkart, PhonePe, CRED & more

---

## 🛠️ Tech Stack

| Category | Technology | Purpose |
|---|---|---|
| 🎨 **UI** | Jetpack Compose + Material 3 | Modern declarative UI |
| 🏛️ **Architecture** | MVVM + Clean Architecture | Scalable code structure |
| 💉 **DI** | Hilt | Dependency injection |
| 🗄️ **Database** | Room | Local data persistence |
| 🔄 **Async** | Kotlin Coroutines + Flow | Reactive data streams |
| 📊 **Charts** | Vico | Beautiful data visualization |
| 💾 **Preferences** | DataStore | User settings storage |
| 🧭 **Navigation** | Navigation Compose | Screen routing |
| 🔧 **Build** | KSP | Fast annotation processing |
| 🧪 **Testing** | JUnit + MockK + Turbine | Unit & integration tests |

---

## 🚀 Getting Started

### Prerequisites
- Android Studio Hedgehog or newer
- JDK 17+
- Android device or emulator (API 26+)

### Clone & Run

```bash
# 1. Clone the repository
git clone https://github.com/YOUR_USERNAME/StepTrackerApp.git

# 2. Open in Android Studio
# File → Open → Select the cloned folder

# 3. Sync Gradle
# File → Sync Project with Gradle Files

# 4. Run the app
# Press the green Play ▶ button
```

### Build Requirements

```toml
# libs.versions.toml
kotlin = "2.0.21"
ksp    = "2.0.21-1.0.28"
agp    = "8.5.2"
```

---

## 📁 Project Structure

```
StepTrackerApp/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/steptracker/app/
│   │   │   │   ├── data/
│   │   │   │   ├── domain/
│   │   │   │   ├── presentation/
│   │   │   │   └── di/
│   │   │   └── res/
│   │   └── test/
│   └── build.gradle.kts
├── gradle/
│   └── libs.versions.toml
├── screenshots/
├── .github/
└── README.md
```

---

## 🧪 Testing

```bash
# Run unit tests
./gradlew test

# Run instrumented tests
./gradlew connectedAndroidTest

# Generate test coverage report
./gradlew jacocoTestReport
```

Test coverage includes:
- ✅ ViewModel logic
- ✅ Repository layer
- ✅ Use cases
- ✅ Room database operations

---

## 📈 What I Learned Building This

1. **Clean Architecture in practice** — How to properly separate data, domain and presentation layers in a real app
2. **Hilt DI** — Managing dependencies across Android components without memory leaks
3. **Room + Flow** — Building a reactive, offline-first database layer
4. **Jetpack Compose** — Building complex, animated UIs declaratively
5. **Sensor integration** — Working with Android's hardware step counter sensor
6. **KSP vs KAPT** — Why KSP is 2x faster and how to migrate

---

## 🤝 Contributing

Contributions are welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) before submitting a PR.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

```
MIT License

Copyright (c) 2026 Mithun

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software.
```

---

## 👨‍💻 Author

<div align="center">

**Mithun**


[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=for-the-badge&logo=github)](https://github.com/mithun0207-AM)
[![Email](https://img.shields.io/badge/Email-Contact-EA4335?style=for-the-badge&logo=gmail)](mailto:mbm33353@gmail.com)

*Android Developer | Kotlin Enthusiast | Clean Code Advocate*

⭐ **If this project helped you, please give it a star!** ⭐

</div>

---

<div align="center">
<sub>Built with ❤️ in Bengaluru, India 🇮🇳</sub>
</div>

