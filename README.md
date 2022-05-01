<!--
*** Thanks for checking out this README Template. If you have a suggestion that would
*** make this better, please fork the repo and create a pull request or simply open
*** an issue with the tag "enhancement".
*** Thanks again! Now go create something AMAZING! :D
-->





<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]



<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/oliverbytes/alchemy">
    <img src="https://github.com/oliverbytes/alchemy/raw/master/images/logo.png" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">Alchemy</h3>

  <p align="center">
    An Alchemy Platform client for Flutter & Dart
    <br />
    <br />
    <a href="https://github.com/oliverbytes/alchemy/issues">Report Bug</a>
    ·
    <a href="https://github.com/oliverbytes/alchemy/issues">Request Feature</a>
  </p>
</p>



<!-- TABLE OF CONTENTS -->
## Table of Contents

* [About the Project](#about-the-project)
  * [Built With](#built-with)
* [Getting Started](#getting-started)
  * [Prerequisites](#prerequisites)
  * [Installation](#installation)
* [Usage](#usage)
* [Roadmap](#roadmap)
* [Contributing](#contributing)
* [License](#license)
* [Contact](#contact)
* [Acknowledgements](#acknowledgements)


## About The Project

An Alchemy Platform client for Flutter & Dart

### EXAMPLE PROJECT SCREENSHOT

[![Playground Desktop App][screenshots-desktop]](https://github.com/oliverbytes/alchemy)

### Supported Platforms
- iOS
- Android
- Mac OS
- Windows
- Linux
- Web

### Built With
Google Flutter SDK
* [Flutter](https://flutter.dev)



<!-- GETTING STARTED -->
## Getting Started


### Prerequisites

* [Flutter SDK](https://flutter.dev)
* [Android SDK & Android Studio](https://developer.android.com/studio) for deployment to Android
* [XCode IDE](https://developer.apple.com/xcode/) for deployment to iOS/iPad/MacOS
* [VS Code IDE](https://code.visualstudio.com/) optional

### Installation

1. Clone the repo
```sh
git clone https://github.com/oliverbytes/alchemy.git
```
2. Install packages dependencies
```
flutter pub get
```
3. Run
```
flutter run
```



<!-- USAGE EXAMPLES -->
## Usage

```dart
// Import Package
import 'package:alchemy/alchemy.dart';

// Instantiate Object
final alchemy = Alchemy();

// Configuration
alchemy.client.init(
    subDomain: 'polygon-mumbai.g', // network
    apiKey: <Your-API-Key>,
    verbose: true,
);

debugPrint('requesting...');
final result = await alchemy.polygon.getBalance(
    address: '0x0ef2e86a73c7be7f767d7abe53b1d4cbfbccbf3a',
);

result.fold(
    (error) { // ERROR
        debugPrint(error.toJson().toString());
    },
    (response) { // SUCCESS
        debugPrint(response.toJson().toString());
    },
);

debugPrint('request done');
```

<!-- ROADMAP -->
## Roadmap

* Complete API
* Unit Testing

See the [open issues](https://github.com/oliverbytes/alchemy/issues) for a list of proposed features (and known issues).



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request



<!-- LICENSE -->
## License
 
Distributed under the MIT License. See `LICENSE` for more information.



<!-- CONTACT -->
## Contact

Oliver Martinez - [@oliverbytes](https://twitter.com/oliverbytes) - nemoryoliver@gmail.com

Project Link: [https://github.com/oliverbytes/alchemy](https://github.com/oliverbytes/alchemy)



<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements
* [Alchemy Platform](https://www.alchemy.com/)
* [Alchemy Docs](https://docs.alchemy.com/alchemy/)





<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/oliverbytes/alchemy.svg?style=flat-square
[contributors-url]: https://github.com/oliverbytes/alchemy/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/oliverbytes/alchemy.svg?style=flat-square
[forks-url]: https://github.com/oliverbytes/alchemy/network/members
[stars-shield]: https://img.shields.io/github/stars/oliverbytes/alchemy.svg?style=flat-square
[stars-url]: https://github.com/oliverbytes/alchemy/stargazers
[issues-shield]: https://img.shields.io/github/issues/oliverbytes/alchemy.svg?style=flat-square
[issues-url]: https://github.com/oliverbytes/alchemy/issues
[license-shield]: https://img.shields.io/github/license/oliverbytes/alchemy.svg?style=flat-square
[license-url]: https://github.com/oliverbytes/alchemy/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=flat-square&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/oliverbytes
[screenshots-desktop]: images/screenshots_desktop.png
