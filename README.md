# ScreenType

![ScreenType](/ScreenType.gif "ScreenType")

[![Version](https://img.shields.io/cocoapods/v/ScreenType.svg?style=flat)](http://cocoapods.org/pods/ScreenType)
[![License](https://img.shields.io/cocoapods/l/ScreenType.svg?style=flat)](http://cocoapods.org/pods/ScreenType)
[![Platform](https://img.shields.io/cocoapods/p/ScreenType.svg?style=flat)](http://cocoapods.org/pods/ScreenType)

Easily distinguish between iPhone models in Objective-C and Swift.

## Example

To demo the example project, clone or download the repo, and open "*ScreenType.xcworkspace*" from the "*Example*" directory.

## Requirements

Swift 4.0+

Xcode 9.0+

iOS 9.0+

## Installation

ScreenType is available through [CocoaPods](https://cocoapods.org/pods/ScreenType). To install
it, simply add the following line to your Podfile:

```ruby
pod 'ScreenType'
```

### Manual Installation

Install ScreenType manually by importing [ScreenType.swift](https://github.com/allgamesallfree/ScreenType/blob/master/ScreenType/Classes/ScreenType.swift) into your project

## Usage

### Swift

If you're using Cocoapods add: `import ScreenType` prior to using ScreenType in your file.

```Swift
// Check for a specific model
if UIScreen.current == .iPhoneX {
    print("Screen type is iPhone X")
}

// Check for multiple models
if UIScreen.current == .iPhone6 || UIScreen.current == .iPhone6Plus {
    print("Screen type is either iPhone 6 or 6 Plus")
}

// Find all models smaller than a certain screen size
if UIScreen.current < .iPhone6 {
    print("Screen is smaller than an iPhone 6")
}

// Find all models larger than or equal to a certain screen size
if UIScreen.current >= .iPad10_5 {
    print("Screen type is either iPad 10.5 or iPad 12.9")
}

```

### Objective-C

You'll need a [bridging header](https://www.hackingwithswift.com/example-code/language/how-to-create-an-objective-c-bridging-header-to-use-code-in-swift) in order to use ScreenType in Objective-C. 

If you're using Cocoapods add `@import ScreenType;` to the top of your file as well.

```Objective-C
// Check for a specific model
if ([UIScreen current] == ScreenTypeIPhoneX) {
    NSLog(@"Screen Type is iPhone X");
}

// Find all models larger than a certain screen size
if ([UIScreen current] > ScreenTypeIPhone5) {
    NSLog(@"Screen is larger than an iPhone 5");
}
```

## Contributions

You are welcome to fork and submit pull requests

## License

ScreenType is available under the MIT license. See the LICENSE file for more info.
