# Flutter Firebase Storage Upload App
Welcome to the Flutter Firebase Storage Upload App! The objective of this Flutter web application is to provide a user-friendly interface for uploading files to Firebase Storage. Firebase Storage is a cloud-based storage service that allows developers to store and serve user-generated content, such as images, videos, and other files.
This Flutter web application aims to simplify the process of uploading files for users, making it seamless and efficient. The application utilizes the Flutter framework for building user interfaces and Firebase Storage for secure and scalable file storage.


### Features
* **User-Friendly Interface:** The app provides an intuitive user interface for a seamless experience.
* **File Upload:** Easily upload images or files from the device to Firebase Storage.
* **Firebase Storage Integration:** The app seamlessly integrates with Firebase Storage to store user-uploaded data.

## Getting Started
To get started with the app, follow these steps:

1. Clone the repository:<br>
git clone https://github.com/umer-saleem/flutter-upload-firebase.git

2. Navigate to the project directory:
cd flutter-firebase-storage-upload-app

3. Install dependencies:
flutter pub get

### 1. Installing Dependencies
Using
### 2. Firebase Storage Configuration
Ensure that you have set up Firebase Storage rules to allow user uploads. Update the rules in the Firebase Console or firebase.json file accordingly:
```
service firebase.storage {
  match /b/{bucket}/o {
    match /{allPaths=**} {
      allow read, write: if request.auth != null;}
  }
}
```

### 3. Firebase Initialization
```
void main() async{
  
  WidgetsFlutterBinding.ensureInitialized();
  if (kIsWeb) {
    await Firebase.initializeApp(
      options: const FirebaseOptions(
        apiKey: "AIzaSyAZF2w1o8KUvaZihjthZc5BW0uWYvvYlZw",
        authDomain: "flutterstorage1-46e3f.firebaseapp.com",
        projectId: "flutterstorage1-46e3f",
        storageBucket: "flutterstorage1-46e3f.appspot.com",
        messagingSenderId: "710281281",
        appId: "1:710281281:web:93a26ab125284ae8749ec0",
        ),);
  }
  else{
    WidgetsFlutterBinding.ensureInitialized();
  }
  
  runApp(const MyApp());
}
```
## Screenshots
![alt text](https://github.com/umer-saleem/flutter-upload-firebase/blob/main/ss1.PNG?raw=true)

## Contributions
Contributions are welcome! If you'd like to contribute to the project, please follow the standard GitHub fork and pull request workflow.

