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
Before getting started, ensure that you have a Flutter development environment set up and Firebase project created with Firebase Storage enabled. Update the necessary dependencies inside your 
“pubspec.yaml” file of the flutter project.
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
  await Firebase.initializeApp();
  runApp(const MyApp());
}
```
### 4. Running the Project
To run the flutter application, within the main project folder, navigate to the “lib” subfolder and then open the “main.dart” file before running it to initialize the application. 

## 5. Screenshots
![alt text](https://github.com/umer-saleem/flutter-upload-firebase/blob/main/ss1.PNG?raw=true)

## 6. Contributions
Contributions are welcome! If you'd like to contribute to the project, please follow the standard GitHub fork and pull request workflow.

