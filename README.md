# 🚀 EchoCall - Hyper-Realistic AI Fake Phone Call Simulator

<div align="center">
  <img src="assets/images/app_icon.png" alt="EchoCall Logo" width="120" height="120">
  
  [![Flutter](https://img.shields.io/badge/Flutter-3.13.0-blue.svg)](https://flutter.dev/)
  [![Dart](https://img.shields.io/badge/Dart-3.1.0-blue.svg)](https://dart.dev/)
  [![Platform](https://img.shields.io/badge/Platform-iOS%20%7C%20Android-lightgrey.svg)](https://flutter.dev/)
  [![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
</div>

## 📱 About EchoCall

EchoCall is a cutting-edge mobile application that creates hyper-realistic fake phone call simulations using advanced AI voice technology. Built with Flutter, it offers pixel-perfect iOS call screen replication, multi-language AI voices, and viral social sharing features.

### ✨ Key Features

- **🎭 Ultra-Realistic Call Simulation**: Pixel-perfect iOS/Android call UI replication
- **🤖 AI-Powered Conversations**: GPT-generated natural dialogue with emotional context
- **🗣️ Multilingual Voices**: 30+ languages with ElevenLabs integration
- **📱 Native Mobile Experience**: Optimized for iOS 17+ and Android 14+
- **🎥 Social Content Creation**: Record and share calls for TikTok, Instagram, YouTube
- **🎮 Gamified Experience**: Trending templates, challenges, and viral leaderboards
- **🔒 Privacy-First Design**: End-to-end encryption and auto-delete features

## 🏗️ Architecture

The app follows Clean Architecture principles with a feature-based structure:

```
lib/
├── core/                   # Core functionality
│   ├── config/            # App configuration
│   ├── models/            # Data models
│   ├── services/          # Core services
│   ├── theme/             # UI theme system
│   └── router/            # Navigation routing
├── features/              # Feature modules
│   ├── call/              # Call simulation
│   ├── home/              # Home dashboard
│   ├── auth/              # Authentication
│   ├── social/            # Social features
│   └── settings/          # App settings
└── main.dart              # App entry point
```

## 🛠️ Tech Stack

### Frontend
- **Flutter 3.13+**: Cross-platform framework
- **Riverpod**: State management
- **Flutter Animate**: Advanced animations
- **Glassmorphism UI**: Modern design effects

### Backend & Services
- **Firebase**: Authentication, Firestore, Storage
- **ElevenLabs API**: AI voice generation
- **OpenAI GPT**: Conversation generation
- **Just Audio**: Audio playback system

### Development Tools
- **Build Runner**: Code generation
- **Hive**: Local data storage
- **Cached Network Image**: Image caching

## 🚀 Getting Started

### Prerequisites

- Flutter 3.13.0 or higher
- Dart 3.1.0 or higher
- iOS 17+ / Android 14+ (for testing)
- Xcode 15+ (for iOS development)
- Android Studio (for Android development)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/echocall.git
   cd echocall
   ```

2. **Install dependencies**
   ```bash
   flutter pub get
   ```

3. **Generate code**
   ```bash
   flutter packages pub run build_runner build
   ```

4. **Set up Firebase**
   - Create a Firebase project
   - Add iOS and Android apps
   - Download and place configuration files:
     - `ios/Runner/GoogleService-Info.plist`
     - `android/app/google-services.json`

5. **Configure API Keys**
   Create a `.env` file in the root directory:
   ```env
   ELEVENLABS_API_KEY=your_elevenlabs_key
   OPENAI_API_KEY=your_openai_key
   ```

6. **Run the app**
   ```bash
   flutter run
   ```

## 📂 Project Structure

### Core Components

#### `CallData` Model
```dart
class CallData {
  final String callerName;
  final String callerNumber;
  final CallType callType;
  final List<ConversationPart> conversation;
  final CallSettings settings;
  // ... other properties
}
```

#### `AudioService`
Handles all audio operations:
- Voice playback with call-quality effects
- Recording with high-fidelity audio
- Ringtone and vibration patterns
- Speaker and mute controls

#### `CallScreen` Widget
Pixel-perfect iOS call interface:
- Blurred background with contact photo
- Animated pulse effects during ringing
- Authentic call controls layout
- Haptic feedback for all interactions

## 🎨 Design System

### iOS-Style Theme
- **Colors**: iOS system colors and gradients
- **Typography**: SF Pro font family
- **Animations**: Native iOS timing curves
- **Components**: Cupertino-style widgets

### Call Screen Features
- **Incoming Calls**: Lock screen overlay with slide-to-answer
- **Active Calls**: Full control panel with mute, speaker, keypad
- **Audio Waveform**: Real-time voice visualization
- **Call Timer**: Accurate duration tracking

## 🔧 Configuration

### Audio Configuration
```dart
// Audio settings in app_config.dart
static const int audioSampleRate = 44100;
static const int audioBitRate = 128000;
static const String audioFormat = 'aac';
```

### Voice Settings
```dart
class VoiceSettings {
  final String voiceId;
  final String language;
  final VoiceGender gender;
  final double speed;
  final double pitch;
}
```

## 🚀 Deployment

### iOS Deployment
1. **Configure signing**
   - Set up provisioning profiles
   - Configure app identifier
   - Enable required capabilities

2. **Build for release**
   ```bash
   flutter build ios --release
   ```

3. **Submit to App Store**
   - Upload to App Store Connect
   - Complete app metadata
   - Submit for review

### Android Deployment
1. **Generate signing key**
   ```bash
   keytool -genkey -v -keystore release-key.keystore -alias release -keyalg RSA -keysize 2048 -validity 10000
   ```

2. **Build signed APK**
   ```bash
   flutter build apk --release
   ```

3. **Upload to Play Store**
   - Create Play Console listing
   - Upload APK/AAB
   - Submit for review

## 🎯 Features Roadmap

### Phase 1: Core Features ✅
- [x] Basic call simulation
- [x] iOS-style UI
- [x] Audio playback system
- [x] Home dashboard

### Phase 2: AI Integration 🔄
- [ ] ElevenLabs voice generation
- [ ] GPT conversation creation
- [ ] Multi-language support
- [ ] Emotion detection

### Phase 3: Social Features 📋
- [ ] Video recording
- [ ] Social sharing
- [ ] Viral templates
- [ ] User challenges

### Phase 4: Monetization 📋
- [ ] Freemium model
- [ ] In-app purchases
- [ ] Premium voice packs
- [ ] Subscription tiers

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines
- Follow Flutter/Dart style guidelines
- Write comprehensive tests
- Update documentation
- Ensure iOS/Android compatibility

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🔗 Links

- **App Store**: Coming Soon
- **Google Play**: Coming Soon
- **Website**: [echocall.app](https://echocall.app)
- **Support**: [support@echocall.app](mailto:support@echocall.app)

## 📊 Analytics & Privacy

EchoCall respects user privacy:
- End-to-end encryption for user data
- Optional analytics with user consent
- GDPR and CCPA compliant
- No personal data collection without permission

---

<div align="center">
  Made with ❤️ by the EchoCall Team
  
  <a href="https://flutter.dev">
    <img src="https://img.shields.io/badge/Made%20with-Flutter-blue.svg" alt="Made with Flutter">
  </a>
</div>
