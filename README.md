# WeRunNY Android App

WeRunNY is an Android application for running enthusiasts in New York.

## Prerequisites

Before building the project, make sure you have the following installed:

- **Android Studio** (latest version recommended)
- **Android SDK** with API level 34 or higher
- **Java Development Kit (JDK)** 8 or 11
- **Git** for version control

## Setup Instructions

1. **Clone the repository:**
   ```bash
   git clone https://github.com/lulloa37/WeRunNY.git
   cd WeRunNY
   ```

2. **Navigate to the Android project:**
   ```bash
   cd WeRunNY_Android_Project_Fixed_Updated_Gradle
   ```

3. **Create local.properties file:**
   Create a `local.properties` file in the project root with your Android SDK path:
   ```
   sdk.dir=/path/to/your/android/sdk
   ```
   
   **Note:** This file is ignored by Git and should not be committed to version control.

## Building the Project

### Using Android Studio

1. Open Android Studio
2. Select "Open an existing Android Studio project"
3. Navigate to the `WeRunNY_Android_Project_Fixed_Updated_Gradle` folder and select it
4. Wait for Gradle sync to complete
5. Build the project using **Build > Make Project** or **Ctrl+F9**

### Using Command Line

1. Navigate to the project directory:
   ```bash
   cd WeRunNY_Android_Project_Fixed_Updated_Gradle
   ```

2. Make the Gradle wrapper executable (if needed):
   ```bash
   chmod +x gradlew
   ```

3. Build the project:
   ```bash
   ./gradlew build
   ```

4. To build a debug APK:
   ```bash
   ./gradlew assembleDebug
   ```

5. To build a release APK:
   ```bash
   ./gradlew assembleRelease
   ```

## Running the App

### Using Android Studio

1. Connect an Android device or start an emulator
2. Click the "Run" button or press **Shift+F10**

### Using Command Line

1. Ensure a device is connected or an emulator is running:
   ```bash
   adb devices
   ```

2. Install and run the debug APK:
   ```bash
   ./gradlew installDebug
   ```

## Project Structure

```
WeRunNY_Android_Project_Fixed_Updated_Gradle/
├── app/                    # Main application module
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/       # Java/Kotlin source files
│   │   │   ├── res/        # Resources (layouts, strings, etc.)
│   │   │   └── AndroidManifest.xml
│   └── build.gradle        # App-level build configuration
├── gradle/                 # Gradle wrapper files
├── build.gradle           # Project-level build configuration
├── settings.gradle        # Project settings
├── gradle.properties      # Gradle properties
└── local.properties       # Local configuration (not in version control)
```

## Development Guidelines

- **Minimum SDK:** API 21 (Android 5.0)
- **Target SDK:** API 34 (Android 14)
- **Language:** Kotlin
- **Build System:** Gradle

## Troubleshooting

### Common Issues

1. **"SDK location not found" error:**
   - Ensure the `local.properties` file exists with the correct SDK path
   - Check that the Android SDK is properly installed

2. **Build fails with dependency errors:**
   - Run `./gradlew clean` and then `./gradlew build`
   - Check your internet connection for dependency downloads

3. **Gradle sync issues:**
   - Try **File > Invalidate Caches and Restart** in Android Studio
   - Delete the `.gradle` folder and re-sync

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is licensed under the MIT License - see the [LICENSE](../LICENSE) file for details.