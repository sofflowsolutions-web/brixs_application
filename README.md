# BRIXS WebView App

A Flutter application that provides a native mobile wrapper for the BRIXS purchase website, offering a seamless mobile experience with enhanced features like offline detection, error handling, and Google Sign-In integration.

## Features

- **WebView Integration**: Native wrapper for the BRIXS purchase website (https://purchase.brixs.live/)
- **Loading Screens**: Animated loading screens with Lottie animations for better user experience
- **Offline Detection**: Automatic detection of network connectivity with retry functionality
- **Error Handling**: Comprehensive error handling for web resource failures
- **Google Sign-In**: Integrated Google authentication with native account picker
- **Accessibility Support**: Full accessibility features with semantic labels and hints
- **Internationalization**: Support for multiple languages using Flutter's localization
- **Dark Theme**: Modern dark theme optimized for mobile devices
- **Exit Confirmation**: User-friendly exit confirmation dialog
- **Cross-Platform**: Supports Android and iOS platforms

## Screenshots

*(Add screenshots here when available)*

## Installation

### Prerequisites

- Flutter SDK (^3.9.0)
- Dart SDK
- Android Studio (for Android development)
- Xcode (for iOS development, macOS only)

### Setup

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd brixs_webview_app
   ```

2. Install dependencies:
   ```bash
   flutter pub get
   ```

3. Generate app icons (optional):
   ```bash
   flutter pub run flutter_launcher_icons
   ```

4. Run the app:
   ```bash
   flutter run
   ```

### Building for Production

#### Android APK
```bash
flutter build apk --release
```

#### iOS (macOS only)
```bash
flutter build ios --release
```

## Dependencies

### Core Dependencies
- `webview_flutter: ^4.8.0` - WebView integration
- `connectivity_plus: ^6.0.3` - Network connectivity detection
- `google_sign_in: ^6.2.1` - Google authentication
- `lottie: ^3.1.0` - Loading animations

### Development Dependencies
- `flutter_lints: ^5.0.0` - Code linting
- `flutter_launcher_icons: ^0.13.1` - App icon generation

## Project Structure

```
lib/
├── main.dart              # Main application entry point
├── constants.dart         # App constants and configuration
├── widgets/
│   ├── splash_screen.dart # Splash screen widget
│   ├── loading_screen.dart # Loading screen with animation
│   └── ...
├── l10n/                  # Localization files
└── ...
```

## Configuration

The app can be configured through the `lib/constants.dart` file:

- **Colors**: Primary, background, and accent colors
- **URLs**: Website URL and other endpoints
- **User Agent**: Custom user agent string for web requests
- **Animations**: Loading animation durations and parameters

## Testing

Run the test suite:
```bash
flutter test
```

### Test Features

The app includes floating action buttons for testing various features:
- **Google Sign-In Test**: Test Google account authentication
- **Back Navigation Test**: Test exit confirmation dialog
- **Loading Screen Test**: Test loading animations
- **Exit Dialog Test**: Test exit confirmation

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Localization

The app supports internationalization. To add a new language:

1. Add a new ARB file in `lib/l10n/` (e.g., `app_fr.arb`)
2. Update the localization delegates in `main.dart`
3. Run `flutter gen-l10n` to generate the localization files

## Troubleshooting

### Common Issues

1. **WebView loading**: Check internet connectivity and ensure the website URL is accessible
2. **Google Sign-In  working**: Verify Google Sign-In configuration and ensure proper OAuth setup
3. **Build failures**: Ensure all dependencies are installed with `flutter pub get`

### Debug Mode

Enable debug mode in Android by setting:
```kotlin
AndroidWebViewController.enableDebugging(true)
```

## License

This project is private and not intended for public distribution.

## Author

**SFS**

## Version

Current version: 1.0.0+1

---

