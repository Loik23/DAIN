# Contributing to EchoCall

Thank you for your interest in contributing to EchoCall! This document provides guidelines and information for contributors.

## 🚀 Getting Started

### Prerequisites
- Flutter 3.13.0 or higher
- Dart 3.1.0 or higher
- Git
- IDE (VS Code, Android Studio, or IntelliJ)

### Setup
1. Fork the repository
2. Clone your fork: `git clone https://github.com/YOUR_USERNAME/echocall.git`
3. Run the setup script: `./scripts/setup.sh`
4. Create a new branch: `git checkout -b feature/your-feature-name`

## 📋 Development Guidelines

### Code Style
- Follow [Dart style guide](https://dart.dev/guides/language/effective-dart/style)
- Use `flutter format .` before committing
- Run `flutter analyze` to check for issues
- Maintain 80-character line limit where possible

### Architecture
- Follow Clean Architecture principles
- Use feature-based folder structure
- Implement proper separation of concerns
- Use Riverpod for state management

### Git Workflow
1. Create feature branches from `main`
2. Use descriptive commit messages
3. Squash commits before merging
4. Update documentation as needed

### Testing
- Write unit tests for business logic
- Add widget tests for UI components
- Ensure integration tests pass
- Maintain 80%+ code coverage

## 🐛 Bug Reports

When reporting bugs, please include:
- Flutter version (`flutter --version`)
- Platform (iOS/Android version)
- Steps to reproduce
- Expected vs actual behavior
- Screenshots/recordings if applicable

## ✨ Feature Requests

For new features:
- Check existing issues first
- Provide detailed use case
- Consider implementation complexity
- Discuss with maintainers before starting

## 📝 Pull Request Process

1. **Before submitting:**
   - Ensure tests pass: `flutter test`
   - Run code analysis: `flutter analyze`
   - Format code: `flutter format .`
   - Update documentation if needed

2. **PR Requirements:**
   - Clear description of changes
   - Link to related issues
   - Screenshots for UI changes
   - Update CHANGELOG.md

3. **Review Process:**
   - At least one approval required
   - All CI checks must pass
   - Address review feedback
   - Squash and merge when approved

## 🏗️ Project Structure

```
lib/
├── core/                   # Core functionality
│   ├── config/            # App configuration
│   ├── models/            # Data models
│   ├── services/          # Core services
│   ├── theme/             # UI theme
│   └── router/            # Navigation
├── features/              # Feature modules
│   ├── call/              # Call simulation
│   ├── home/              # Home dashboard
│   ├── auth/              # Authentication
│   └── social/            # Social features
└── main.dart              # App entry point
```

## 🎨 UI/UX Guidelines

### Design System
- Follow iOS Human Interface Guidelines
- Use consistent spacing (8px grid)
- Implement dark/light mode support
- Ensure accessibility compliance

### Animations
- Use Flutter Animate for complex animations
- Follow iOS timing curves
- Maintain 60fps performance
- Add haptic feedback for interactions

## 🔧 API Integration

### Voice AI Services
- ElevenLabs for voice generation
- OpenAI for conversation creation
- Implement proper error handling
- Cache responses when appropriate

### Firebase Setup
- Authentication: Firebase Auth
- Database: Cloud Firestore
- Storage: Firebase Storage
- Analytics: Firebase Analytics

## 🧪 Testing Strategy

### Unit Tests
```dart
// Example test structure
group('CallData', () {
  test('should create call with correct properties', () {
    final call = CallData(
      callerName: 'Test User',
      callerNumber: '+1234567890',
    );
    
    expect(call.callerName, 'Test User');
    expect(call.status, CallStatus.pending);
  });
});
```

### Widget Tests
```dart
// Example widget test
testWidgets('CallScreen displays caller name', (tester) async {
  await tester.pumpWidget(
    MaterialApp(
      home: CallScreen(callData: mockCallData),
    ),
  );
  
  expect(find.text('Test User'), findsOneWidget);
});
```

## 📱 Platform-Specific Guidelines

### iOS Development
- Test on multiple iOS versions (15+)
- Verify App Store guidelines compliance
- Implement proper background audio handling
- Use iOS-native UI patterns

### Android Development
- Support Android 14+ (API level 34+)
- Test on different screen sizes
- Implement proper audio focus handling
- Follow Material Design guidelines

## 🔒 Security & Privacy

### Data Protection
- Encrypt sensitive user data
- Implement proper authentication
- Follow GDPR/CCPA compliance
- No data collection without consent

### API Security
- Use environment variables for keys
- Implement proper error handling
- Add rate limiting where needed
- Validate all user inputs

## 📚 Documentation

### Code Documentation
- Document public APIs with dartdoc
- Add inline comments for complex logic
- Update README for significant changes
- Maintain architecture documentation

### User Documentation
- Update help screens
- Create tutorial content
- Maintain FAQ section
- Document known issues

## 🚀 Release Process

### Version Management
- Use semantic versioning (x.y.z)
- Update version in pubspec.yaml
- Tag releases in Git
- Maintain CHANGELOG.md

### App Store Preparation
1. Update app metadata
2. Generate release builds
3. Test on physical devices
4. Submit for review
5. Monitor crash reports

## 💬 Communication

### Discord Server
Join our Discord for real-time discussion:
- General discussion
- Development help
- Feature planning
- Bug reports

### GitHub Discussions
Use GitHub Discussions for:
- Feature proposals
- Architecture decisions
- Community Q&A
- Release planning

## 🏆 Recognition

Contributors will be recognized in:
- CONTRIBUTORS.md file
- App credits screen
- Release notes
- Social media shoutouts

## 📄 License

By contributing to EchoCall, you agree that your contributions will be licensed under the MIT License.

---

Thank you for contributing to EchoCall! Together, we're building the future of AI-powered call simulation. 🚀