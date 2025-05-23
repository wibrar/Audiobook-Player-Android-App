# Audiobook Player App (Android Studio)

This project is a simple Audiobook Player Android application developed using **Java** in **Android Studio** as part of a university coursework. The app is designed to play `.mp3` audiobooks stored on the device's SD card and continue playback in the background while allowing full user control via multiple activities.

> This project is individual coursework and contributes 25% to the final module mark.

---

## Features

### Core Functionality

- **Audiobook List Activity**
  - Displays available audiobooks and user-created bookmarks from `/sdcard/Music/`
  - Allows playback to start from the beginning or a specific timestamp via bookmarks

- **Player Activity**
  - Standard playback controls: Play, Pause, Stop, Next, Previous
  - Displays current playback progress and selected playback speed
  - Allows users to add bookmarks at the current timestamp

- **Settings Activity**
  - Lets users customize playback speed
  - Provides background color selection for personalization

### System Features

- **Persistent Background Playback**
  - Audio continues playing even when the app is not in the foreground
  - Implemented using a bound `Service`

- **User Notification**
  - Persistent notification shown when an audiobook is playing

- **Bookmark Support**
  - Resumes playback from saved timestamps with one tap

- **Lifecycle and State Management**
  - Playback state and settings persist across activity changes (e.g., orientation changes)

---

## 🧱 Architecture

- 3 Main Activities:
  - `AudiobookListActivity` — shows all audiobooks and bookmarks
  - `PlayerActivity` — controls playback and progress
  - `SettingsActivity` — modifies speed and UI preferences

- 1 Bound Service:
  - `AudiobookService` — handles long-running playback in the background

- Media playback handled via a provided `Audiobook` wrapper class (encapsulates `MediaPlayer`)

---

## How to Build and Run

### Prerequisites

- Android Studio Electric Eel or newer
- Android Emulator (e.g., Pixel 5, API 34 - Android 14 "Upside Down Cake")

### Running the App

1. Clone or download the project
2. Open the project in Android Studio
3. Place sample `.mp3` files in the emulator at `/sdcard/Music/` using the **Device Explorer**
4. Build and run the project on an emulator
5. Use the main screen to browse and play audiobooks

---

## 📁 File Structure

```
├── app
│   ├── java/com/example/audiobookplayer
│   │   ├── AudiobookListActivity.java
│   │   ├── PlayerActivity.java
│   │   ├── SettingsActivity.java
│   │   ├── AudiobookService.java
│   │   ├── Audiobook.java (provided class, unmodified)
│   └── res/
│       └── layout/   # XML UI files for each activity
│       └── values/   # Strings and themes
```

---


## 📌 Notes

- This project adheres to the Android Activity and Service lifecycle best practices.
- No third-party libraries were used unless explicitly referenced and licensed.
- The app was tested on an Android 14 emulator (Pixel 5, API 34, 1080x1920, 420dpi).

---

## 📜 License

This project is submitted for academic purposes and is not licensed for commercial use.

---

## ✍️ Author

- Student Name: *Wasif Ibrar*
- University Module: Mobile Application Development
