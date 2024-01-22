# Flutter Firebase Storage Upload App
Welcome to the Flutter Firebase Storage Upload App! This Flutter application allows users to easily upload their data, such as images or files, to Firebase Storage. Firebase Storage provides a scalable and secure solution for storing and serving user-generated content, making it an excellent choice for your Flutter applications.

## Features
* **User-Friendly Interface:** The app provides an intuitive user interface for a seamless experience.
* **Firebase Authentication:** Users can sign in securely using Firebase Authentication to ensure data privacy.
* **File Upload:** Easily upload images or files from the device to Firebase Storage.
* **Real-time Progress:** Users can track the real-time progress of their file uploads.
* **Firebase Storage Integration:** The app seamlessly integrates with Firebase Storage to store user-uploaded data.

# Getting Started
To get started with the app, follow these steps:

1. Clone the repository:<br>
git clone https://github.com/your-username/flutter-firebase-storage-upload-app.git

2. Navigate to the project directory:
cd flutter-firebase-storage-upload-app

3. Install dependencies:
flutter pub get

# Firebase Storage Configuration
Ensure that you have set up Firebase Storage rules to allow user uploads. Update the rules in the Firebase Console or firebase.json file accordingly:
```
service firebase.storage {
  match /b/{bucket}/o {
    match /{allPaths=**} {
      allow read, write: if request.auth != null;}
  }
}
```
# Screenshots
![alt text](https://github.com/umer-saleem/flutter-upload-firebase/blob/main/ss1.PNG?raw=true)

# Contributions
Contributions are welcome! If you'd like to contribute to the project, please follow the standard GitHub fork and pull request workflow.

