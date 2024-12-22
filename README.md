# Jim Carrier Flutter

This project is initially a part of Capstone Design Course in Sungkyunkwan University.

## Related Repository

[API Server](https://github.com/nicolaics/jim-carrier-server)
- This is the repository used for the server, written in Golang.


## Motivation

Living in a foreign country as international students or immigrant workers could be difficult. We are not accustomed with foods, cultures, and things that we usually get in our home countries. Hence, at times we miss those kinds of things that existed back home. Also, there are high chances that we left some important documents we left at our home countries that we suddenly need it.

There are some services exist, such as post offices, however, these services are quite expensive and take some time. Hence, as students who have limited amount of money or immigrant workers who want to save money as much as they can, these services are not a suitable option.

The solution to this is that some people who are going back to their home country and/or vice-versa and still have some weight left in the baggage can sold it in a considerably cheaper price to those who need it. With this solution, people can get their stuffs faster with a considerably cheaper price.

## Goals

We want to improve the efficiency and effectiveness on how the users can find each other, the so-called carriers and givers.

Hence, we would like to create a platform in which we combine all available carriers and givers that wanted to use the carriers’ services.

## Main Features

### User Features:

- Create, modify, and delete accounts.
- Verification of Account via Emai.
- Reset Password.
- Add and modify Bank Details.
- Communicate via Email.

### Core Features:

- Create, modify, and delete listing.
- Create, modify, and delete order.
- Confirm Orders by Carrier.
- Leave Reviews.
- Browse Listings.

### Additional Features:

- Uploading Profile Pictures.
- Upload Payment Proof.
- Upload Package Image.
- Email Notifications for Images:
    - Payment proof images are sent to the corresponding user via email.
    - Package images are shared with the relevant user through email.


## How to Run
1. Have the recent version of Android Studio and Flutter.
2. Go to the jim-carrier-flutter directory.
3. Run the command flutter run.

## Tech-Stacks

- **Frontend**
    - Dart with Flutter Framework
    - Figma for Initial Designs
- **Backend**
    - Golang
    - MySQL for Database
- **Deployment**
    - AWS EC2 Instance
    - AWS RDS
    - AWS S3 Buckets
    - Tailscale for Testing and Debugging
- **Project Management Software Tools**
    - Jira by Atlassian

## Frontend Flowchart

Below is the visual representation of interaction among different interfaces in our application.

![Flowchart](https://github.com/user-attachments/assets/ea401fcc-8446-45fa-915a-6a383aa20932)

## Environment Variables Example

```
ENCRYPTION_NUMBER_KEY=some_key
ENCRYPTION_NUMBER_IV=some_iv
ENCRYPTION_HOLDER_KEY=some_key
ENCRYPTION_HOLDER_IV=some_iv

BASE_URL=api_url

#FIREBASE
FIREBASE_PROJECT_ID=some_id
FIREBASE_AUTH_DOMAIN=some_domain
FIREBASE_STORAGE_BUCKET=some_bucket
FIREBASE_IOS_BUNDLE_ID=some_id

# FIREBASE WEB
FIREBASE_WEB_API_KEY=api_key
FIREBASE_WEB_APP_ID=app_id
FIREBASE_MESSAGING_SENDER_ID=sender_id

# FIREBASE ANDROID
FIREBASE_ANDROID_API_KEY=api_key
FIREBASE_ANDROID_APP_ID=app_id
FIREBASE_ANDROID_MESSAGING_SENDER_ID=sender_id

# FIREBASE IOS
FIREBASE_IOS_API_KEY=api_key
FIREBASE_IOS_APP_ID=app_id
FIREBASE_IOS_MESSAGING_SENDER_ID=sender_id
FIREBASE_IOS_CLIENT_ID=client_id

# FIREBASE MAC OS
FIREBASE_MAC_OS_API_KEY=api_key
FIREBASE_MAC_OS_APP_ID=app_id
FIREBASE_MAC_OS_MESSAGING_SENDER_ID=sender_id
FIREBASE_MAC_OS_IOS_CLIENT_ID=client_id

# FIREBASE WINDOWS
FIREBASE_WINDOWS_API_KEY=api_key
FIREBASE_WINDOWS_APP_ID=app_id
FIREBASE_WINDOWS_MESSAGING_SENDER_ID=sender_id

```

## Further Development

There are still some limitations that can be solved in further developments, such as:
1. Change encryption into RSA-256 instead of AES-256.
2. 

## Contributors

- **Pravas Giri**
    - [GitHub](https://github.com/PravasGiri7)

- **Nicolai Christian Suhalim**
    - [LinkedIn](https://www.linkedin.com/in/nicolaics/)
    - [GitHub](https://github.com/nicolaics/)

## Directory Structure
```
.
├── android
|   ├── app
|   |   ├── src
|   |   |   ├── debug
|   |   |   ├── main
|   |   |   |   ├── java
|   |   |   |   ├── kotlin
|   |   |   |   ├── res
|   |   |   |   └── AndroidManifest.xml
|   |   |   └── profile
|   |   └── build.gradle
|   ├── gradle
|   ├── .gitignore
|   ├── buid.gradle
|   ├── gradle.properties
|   └── settings.gradle
├── assets
|   └── images
|       ├── loginpage
|       |   └── google_icon.png
|       └── welcomePage
|           └── welcome_screen.png
├── ios
|   ├── Flutter
|   ├── Runner
|   ├── Runner.xcodeproj
|   ├── Runner.xcworkspace
|   ├── RunnerTests
|   ├── .gitignore
|   └── Podfile
├── lib
|   ├── src
|   |   ├── api
|   |   |   ├── api_service.dart
|   |   |   ├── auth.dart
|   |   |   ├── listing.dart
|   |   |   ├── order.dart
|   |   |   └── review.dart
|   |   ├── auth
|   |   |   ├── encryption.dart
|   |   |   └── secure_storage.dart
|   |   ├── base_class
|   |   |   ├── firebase_notif.dart
|   |   |   └── login_google.dart
|   |   ├── constants
|   |   |   ├── colors.dart
|   |   |   ├── currency.dart
|   |   |   ├── image_strings.dart
|   |   |   ├── sizes.dart
|   |   |   └── text_strings.dart
|   |   ├── screens
|   |   |   ├── auth
|   |   |   |   ├── email_verification.dart
|   |   |   |   ├── forgot_pw.dart
|   |   |   |   ├── login_screen.dart
|   |   |   |   ├── otp_screen_fp.dart
|   |   |   |   ├── otp_screen.dart
|   |   |   |   ├── register_screen.dart
|   |   |   |   └── reset_password.dart
|   |   |   ├── home
|   |   |   |   ├── bottom_bar.dart
|   |   |   |   └── home_page.dart
|   |   |   ├── listing
|   |   |   |   ├── add_listing.dart
|   |   |   |   └── edit_listing.dart
|   |   |   ├── order
|   |   |   |   ├── confirm_order.dart
|   |   |   |   ├── new_order.dart
|   |   |   |   └── previous_order.dart
|   |   |   ├── profile
|   |   |   |   ├── profile_menu.dart
|   |   |   |   ├── profile_screen.dart
|   |   |   |   ├── update_password.dart
|   |   |   |   └── update_profile.dart
|   |   |   ├── received_order
|   |   |   |   └── received_order.dart
|   |   |   ├── review
|   |   |   |   └── review_page.dart
|   |   |   ├── try.dart
|   |   |   └── welcome.dart
|   |   └── utils
|   |       └── formatter.dart
|   ├── firebase_options.dart
|   └── main.dart
├── linux
|   ├── flutter
|   ├── .gitignore
|   ├── main.cc
|   ├── my_application.cc
|   └── my_application.h
├── macos
|   ├── Flutter
|   ├── Runner
|   ├── Runner.xcodeproj
|   ├── Runner.xcworkspace
|   ├── RunnerTests
|   ├── .gitignore
|   └── Podfile
├── test
|   └── widget_test.dart
├── web
|   ├── icons
|   ├── favicon.png
|   ├── index.html
|   └── manifest.json
├── windows
|   ├── runner
|   └── .gitignore
├── .gitignore
├── .metadata
├── analysis_options.yaml
├── LICENSE
├── pubspec.yaml
└── README.md
```
