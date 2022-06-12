#  Onboarding Info Screen

An introduction/onboarding screen for Flutter apps.
This is a fork of fancy_on_boarding.
* Checkout the [original project](https://github.com/xsahil03x/fancy_on_boarding).


<img src="https://user-images.githubusercontent.com/107174897/173245602-cec1ce12-d88e-4f70-9787-6929d3635551.gif" height="400" alt="GIF"/>

<!---
## 💻 Installation
In the `dependencies:` section of your `pubspec.yaml`, add the following line:

[![Version](https://img.shields.io/pub/v/fancy_on_boarding.svg)](https://pub.dartlang.org/packages/fancy_on_boarding)

```
fancy_on_boarding: <latest_version>
```

## ❔ Usage

### Import this class
```dart
import 'package:fancy_on_boarding/fancy_on_boarding.dart';
```

### Create a List of PageModel

```dart
  final pageList = [
    PageModel(
        color: const Color(0xFF678FB4),
        heroImagePath: 'assets/png/hotels.png',
        title: Text('Hotels',
            style: TextStyle(
              fontWeight: FontWeight.w800,
              color: Colors.white,
              fontSize: 34.0,
            )),
        body: Text('All hotels and hostels are sorted by hospitality rating',
            textAlign: TextAlign.center,
            style: TextStyle(
              color: Colors.white,
              fontSize: 18.0,
            )),
        iconImagePath: 'assets/png/key.png'),
    PageModel(
        color: const Color(0xFF65B0B4),
        heroImagePath: 'assets/png/banks.png',
        title: Text('Banks',
            style: TextStyle(
              fontWeight: FontWeight.w800,
              color: Colors.white,
              fontSize: 34.0,
            )),
        body: Text(
            'We carefully verify all banks before adding them into the app',
            textAlign: TextAlign.center,
            style: TextStyle(
              color: Colors.white,
              fontSize: 18.0,
            )),
        iconImagePath: 'assets/png/wallet.png'),
    PageModel(
      color: const Color(0xFF9B90BC),
      heroImagePath: 'assets/png/stores.png',
      title: Text('Store',
          style: TextStyle(
            fontWeight: FontWeight.w800,
            color: Colors.white,
            fontSize: 34.0,
          )),
      body: Text('All local stores are categorized for your convenience',
          textAlign: TextAlign.center,
          style: TextStyle(
            color: Colors.white,
            fontSize: 18.0,
          )),
      icon: Icon(
        Icons.shopping_cart,
        color: const Color(0xFF9B90BC),
      ),
    ),
    // SVG Pages Example
    PageModel(
        color: const Color(0xFF678FB4),
        heroImagePath: 'assets/svg/hotel.svg',
        title: Text('Hotels SVG',
            style: TextStyle(
              fontWeight: FontWeight.w800,
              color: Colors.white,
              fontSize: 34.0,
            )),
        body: Text('All hotels and hostels are sorted by hospitality rating',
            textAlign: TextAlign.center,
            style: TextStyle(
              color: Colors.white,
              fontSize: 18.0,
            )),
        iconImagePath: 'assets/svg/key.svg',
        heroImageColor: Colors.white),
    PageModel(
        color: const Color(0xFF65B0B4),
        heroImagePath: 'assets/svg/bank.svg',
        title: Text('Banks SVG',
            style: TextStyle(
              fontWeight: FontWeight.w800,
              color: Colors.white,
              fontSize: 34.0,
            )),
        body: Text(
            'We carefully verify all banks before adding them into the app',
            textAlign: TextAlign.center,
            style: TextStyle(
              color: Colors.white,
              fontSize: 18.0,
            )),
        iconImagePath: 'assets/svg/cards.svg',
        heroImageColor: Colors.white),
    PageModel(
      color: const Color(0xFF9B90BC),
      heroImagePath: 'assets/svg/store.svg',
      title: Text('Store SVG',
          style: TextStyle(
            fontWeight: FontWeight.w800,
            color: Colors.white,
            fontSize: 34.0,
          )),
      body: Text('All local stores are categorized for your convenience',
          textAlign: TextAlign.center,
          style: TextStyle(
            color: Colors.white,
            fontSize: 18.0,
          )),
      iconImagePath: 'assets/svg/cart.svg',
    ),
  ];
```

### Pass it into the FancyOnBoarding widget
```dart
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: FancyOnBoarding(
        doneButtonText: "Done",
        skipButtonText: "Skip",
        pageList: pageList,
        onDoneButtonPressed: () =>
            Navigator.of(context).pushReplacementNamed('/mainPage'),
        onSkipButtonPressed: () =>
            Navigator.of(context).pushReplacementNamed('/mainPage'),
      ),
    );
  }
```

## 🎨 Customization and Attributes

#### FancyOnBoarding attributes
<table>
    <th>Attribute Name</th>
    <th>Example Value</th>
    <th>Description</th>
    <tr>
        <td>pageList</td>
        <td>List&lt;PageModel&gt;</td>
        <td>The list of pages to be displayed</td>
    </tr>
    <tr>
        <td>onDoneButtonPressed</td>
        <td>(){}</td>
        <td>Function to be called on pressing done button</td>
    </tr>
    <tr>
        <td>onSkipButtonPressed</td>
        <td>(){}</td>
        <td>Function to be called on pressing skip button</td>
    </tr>
    <tr>
        <td>doneButtonText</td>
        <td>"Let's Go"</td>
        <td>Done button text content defaults to "Done"</td>
    </tr>
    <tr>
        <td>skipButtonText</td>
        <td>"Skip"</td>
        <td>Skip button text content defaults to "Skip"</td>
    </tr>
    <tr>
        <td>showSkipButton</td>
        <td>true</td>
        <td>Skip button should be visible or not. Defaults to true</td>
    </tr>
    <tr>
        <td>bottomMargin</td>
        <td>8.0</td>
        <td>Indicator bottom margin. Defaults to 8.0</td>
    </tr>
    <tr>
        <td>doneButton</td>
        <td>Button(onPressed:(){},child:Text('Done'))</td>
        <td>Custom DoneButton. Will replace default doneButton if provided</td>
    </tr>
    <tr>
        <td>skipButton</td>
        <td>Button(onPressed:(){},child:Text('Skip'))</td>
        <td>Custom SkipButton. Will replace default doneButton if provided</td>
    </tr>
</table>

#### PageModel attributes 
<table>
    <th>Attribute Name</th>
    <th>Example Value</th>
    <th>Description</th>
    <tr>
        <td>color</td>
        <td>Color(0xFF65B0B4)</td>
        <td>The background color of the page</td>
    </tr>
    <tr>
        <td>heroAssetPath</td>
        <td>'assets/banks.png'</td>
        <td>The main onboarding image</td>
    </tr>
    <tr>
        <td>heroAssetColor</td>
        <td>Color(0xFF65B0B4)</td>
        <td>Main onboarding image color</td>
    </tr>
    <tr>
        <td>title</td>
        <td>Text('Banks')</td>
        <td>Title of the page</td>
    </tr>
    <tr>
        <td>body</td>
        <td>Text('We carefully verify all banks before adding them into the app')</td>
        <td>Body of the page</td>
    </tr>
    <tr>
        <td>iconAssetPath</td>
        <td>'assets/wallet.png'</td>
        <td>Icon for the floating bubble</td>
    </tr>
    <tr>
        <td>icon</td>
        <td>Icon(Icons.shopping_cart)</td>
        <td>Icon for the floating bubble, Will replace 'iconAssetPath' if provided</td>
    </tr>
    
</table>
--->


# 📃 License [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

  ### MIT license<br>
  Copyright (c) 2018 Sahil Kumar<br>
  Copyright (c) 2022 FurryProtogen
    
    Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
    
    The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.
    
    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
<!---
## Getting Started

For help getting started with Flutter, view our online [documentation](https://flutter.io/).

For help on editing package code, view the [documentation](https://flutter.io/developing-packages/).
--->
