<p align="center">
    <a href="http://www.bagisto.com"><img src="https://bagisto.com/wp-content/themes/bagisto/images/logo.png" alt="Total Downloads"></a>
</p>

<p align="center">
    <a href="https://twitter.com/intent/follow?screen_name=bagistoshop"><img src="https://img.shields.io/twitter/follow/bagistoshop?style=social"></a>
    <a href="https://www.youtube.com/channel/UCbrfqnhyiDv-bb9QuZtonYQ"><img src="https://img.shields.io/youtube/channel/subscribers/UCbrfqnhyiDv-bb9QuZtonYQ?style=social"></a>
    <a href="https://deepwiki.com/bagisto/opensource-ecommerce-mobile-app"><img src="https://deepwiki.com/badge.svg" alt="Ask DeepWiki"></a>
</p>


# Open Source eCommerce Mobile App

[Bagisto](https://bagisto.com/en/) revolutionizes the world of mobile commerce with its open-source eCommerce mobile app solution. This open-source mobile ecommerce app seamlessly transforms your Bagisto store into a powerful mobile platform, providing real-time synchronization of products and categories. With a user-friendly interface, managing orders becomes a breeze, making it an essential tool for tech-savvy individuals and those new to eCommerce.

This mobile app, built on the foundation of the Bagisto eCommerce framework and leveraging the robust Laravel stack, offers many features for a comprehensive and efficient mobile shopping experience. The app ensures easy product information management and accelerates time-to-market for your products, all while giving you complete control over your store.

# Live Demo

Android: <https://play.google.com/store/apps/details?id=com.webkul.bagisto.mobikul>

iOS: <https://apps.apple.com/us/app/mobikul-bagisto-laravel-app/id6447519140>

# Features

The open-source ecommerce mobile app comes with an array of features to improve your customers' shopping experience.

## Interactive Home Page and Search

![enter image description here](https://raw.githubusercontent.com/bagisto/temp-media/master/interactive-homepage-and-search.png)

## All Type Product Supported

![enter image description here](https://raw.githubusercontent.com/bagisto/temp-media/master/product-details.png)

## Dark Mode and Push Notification

![enter image description here](https://raw.githubusercontent.com/bagisto/temp-media/master/dark-theme-and-push-notifications.png)

## Discount Coupons and Guest Checkout

![enter image description here](https://raw.githubusercontent.com/bagisto/temp-media/master/coupon-and-guest-checkout.png)

## Wishlist and Product Category

![enter image description here](https://raw.githubusercontent.com/bagisto/temp-media/master/category%3Dpage-and-wishlist.png)

## Order Details and Product Reviews

![enter image description here](https://raw.githubusercontent.com/bagisto/temp-media/master/order-details-and-product-reviews.png)

## Installation Guide

Before beginning with the installation, you will need the following with the mentioned versions

- Bagisto Version - v2.3.6
- Android Studio Meerkat | 2024.3.1 Patch 2
- Flutter Version - 3.32.5
- Dart - 3.8.1
- Xcode - 16.3
- Swift - 6.1

Make sure you have installed the [API module](https://github.com/bagisto/headless-ecommerce/) and set this up properly on your bagisto.

> NOTE: It is recommended that you run a simple Hello World program in Flutter first before proceeding further so that you are sure that the environment is properly set up.

## Installation Steps

### Clone the repository

- Open your terminal or command prompt
- Navigate to the directory where you want to save the project
- Use the git clone command followed by the repository URL

```sh
git clone https://github.com/bagisto/opensource-ecommerce-mobile-app.git
```

### Install dependencies

- Navigate to the project's directory

```sh
cd <repository-name>
```

- Run the following command to install the required packages

```sh
flutter pub get
```

### Generate Required files

- Navigate to the project's directory

```sh
cd <repository-name>
```

- Run the following command to generate the required files

```sh
flutter pub run build_runner build --delete-conflicting-outputs 
```

### Connect a device or emulator

- Physical Device

  1. Enable USB debugging on your device
  2. Connect it to your computer using a USB cable.

- Emulator

  1. Start an Android or iOS emulator using your preferred IDE or tools.

### Run the Project

- Use the following command to build and run the project

```sh
flutter run
```

## Minimum Versions

- Android: 22
- iOS: 16

## Configurations Steps

### For Setup

Change the baseDomain  as per your store

**Path:** lib/utils/server_configuration.dart

```sh
static const String baseDomain = ‘....’;
```

> Note: Add the value of the complete URL ending with the GraphQL API endpoint. E.g - <https://example.com/graphql>

### For Theme

Change the Theme for your app

**Path:** lib/utils/mobikul_theme.dart

```sh
static const Color primaryColor = Color(***********);  
static const Color accentColor = Color(***********); 
```

### For Push Notification Service

- Android

Replace "google-services.json".

- iOS

Replace "GoogleService-Info.plist".

> Helpful Articles

> Android  → <https://mobikul.com/knowledgebase/generating-google-service-file-enable-fcm-firebase-cloud-messaging-android-application/>

> iOS → <https://mobikul.com/knowledgebase/generating-new-googleservice-info-plist-file-fcm-based-project-ios-app/>

### For Application Title

- Android

  1. **Path:** android/app/src/main/AndroidManifest.xml
  2. **Change app name:** android:label="***********"

- iOS

  1. Go to the general tab and identity change the display name to your app name

> For Homepage Header Title - Go to ‘assets/language/en.json’
> (Note: Here, “en” in en.json refers to the languages that would be supported within the application)

### For Splash Screen

- For adding Lottie as Splash Screen

  1. **Path:** assets/lottie/splash_screen.json
  2. After updating the Lottie file, update the ‘splashLottie’ in lib/utils/assets_constants.

```sh
 static const String splashLottie = "assets/lottie/splash_screen.json";
```

- For adding an Image as a Splash Screen

  1. **Path:** assets/images/splash.png
  2. After updating the Image file, update the ‘splashImage’ in lib/utils/assets_constants.

```sh
  static const String splashImage = "assets/images/splash.png";
```

### For App Icon

- **Android:** Open the android folder in Android Studio and then right click app > new > Image Asset set Image.
- **iOS:** Replace the icons over the path > ios/Runner/Assets.xcassets/AppIcon.appiconset

## Installation Video

[![Watch the video](https://i.ibb.co/c6qd31t/thumbnail-1.jpg)](https://www.youtube.com/watch?v=tvm2NUZP9ks)

## API Documentation

For the API Documentation, please go through - <https://github.com/bagisto/headless-ecommerce/>

## Usage

For detailed usage instructions, refer to the official documentation

## Contributing

Contributions are welcome! Follow the contribution guidelines to get started.

## License

Bagisto is open-sourced software licensed under the MIT license.
---

## 🤝 Contributing

Contributions are welcome! We encourage the community to help improve this project.

1. **Fork** the repository
2. Create a **feature branch** (`git checkout -b feature/amazing-feature`)
3. **Commit** your changes (`git commit -m 'Add amazing feature'`)
4. **Push** to the branch (`git push origin feature/amazing-feature`)
5. Open a **Pull Request**

Please make sure to update tests as appropriate and follow the existing code style.

---

## 📬 Contact

**Mulky Malikul Dhaher** — [mulkymalikuldhaher@email.com](mailto:mulkymalikuldhaher@email.com)

GitHub: [https://github.com/mulkymalikuldhrs](https://github.com/mulkymalikuldhrs)

---

## ⚠️ Disclaimer

**This project is for Education Purpose only.**

All content, code, and documentation provided in this repository are intended solely for educational and research purposes. Nothing in this repository constitutes financial, investment, legal, or professional advice.

**Risiko apapun tidak kita tanggung.** (We are not responsible for any risks or damages.)

Use at your own risk. The authors and contributors assume no liability for any losses, damages, or consequences arising from the use of this software or information provided herein.

---

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

Copyright © Mulky Malikul Dhaher. All rights reserved.


---

## Disclaimer

**For Education Purpose Only.** This project is for educational and research purposes only. The author assumes no responsibility for any losses, damages, or consequences arising from the use of this software.

**Hanya untuk Tujuan Pendidikan.** Proyek ini hanya untuk tujuan pendidikan dan penelitian. Risiko apapun tidak kita tanggung.

**仅用于教育目的。** 本项目仅供教育和研究目的。作者对因使用本软件而造成的任何损失不承担责任。

---

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.

## Contact

**Mulky Malikul Dhaher** — [mulkymalikuldhaher@email.com](mailto:mulkymalikuldhaher@email.com)
