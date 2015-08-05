[![Carthage compatible](https://img.shields.io/badge/Carthage-compatible-4BC51D.svg?style=flat)](https://github.com/Carthage/Carthage)

![Sample](http://imgur.com/KDRw1LH)

# Localize-Swift
Localize-Swift is a Swift framework that improves i18n and localization with cleaner syntax and in-app language switching.

## Features

- Keep the localized .strings file your app already uses.
- Allow your users to change their current language (example coming soon).
- Use a more Swift-like syntax instead of NSLocalizedString.
- A simpler genstrings replacement.

## Usage

Import at the top of each Swift file that sets text:
```
import Localize
```

Wrap every string in Localized():
```
textLabel.text = Localized("Hello World")
```

To get an array of available localizations:
```
Localize.availableLanguages()
```

To change the current language:
```
Localize.setCurrentLanaguage("fr")
```

To reset back to the default translation:
```
Localize.resetCurrentLanaguageToDefault()
```

## genstrings

To support this new Localized("string") syntax, Localize-Swift includes a custom genstrings script.

To grab all strings from your app (including Localized and NSLocalizedString), copy the genstrings.py file into your project's root folder and run with

```
python genstrings.py
```

This will print the collected strings in the terminal. Select and copy to your base Localizable.strings.


### Setting up with Carthage

[Carthage](https://github.com/Carthage/Carthage) is a decentralized dependency manager that automates the process of adding frameworks to your Cocoa application.

You can install Carthage with [Homebrew](http://brew.sh/) using the following command:

```bash
$ brew update
$ brew install carthage
```

To integrate Localize-Swift into your Xcode project using Carthage, specify it in your `Cartfile`:

```ogdl
github "marmelroy/Localize-Swift"
```

### Setting up with [CocoaPods](http://cocoapods.org/?q=libPhoneNumber-iOS)
```
source 'https://github.com/CocoaPods/Specs.git'
pod 'Localize-Swift', '~> 0.0.1'
```
