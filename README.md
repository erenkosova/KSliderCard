# KSliderCard

<p align="center">
<img src="https://user-images.githubusercontent.com/16580898/64905379-25667200-d6e0-11e9-9c3d-84cc4aed8b32.png" width="100%">
</p>

<br><p align="center">
<img src="https://user-images.githubusercontent.com/16580898/64905440-28ae2d80-d6e1-11e9-9456-eab7dd59832a.gif" width="35%"/>
<img src="https://user-images.githubusercontent.com/16580898/64905425-e258ce80-d6e0-11e9-9f0a-361179edf5e2.gif" width="35%"/>
</p>

<p align="center">
  <img alt="MIT Licance" src="https://img.shields.io/github/license/KenanAtmaca/KSliderCard"/>
  <img alt="Release" src="https://img.shields.io/github/v/tag/KenanAtmaca/KSliderCard"/>
  <img alt="Swift" src="https://img.shields.io/badge/Swift-5.0%2B-orange"/>
  <img alt="Twitter" src="https://img.shields.io/twitter/url/https/github.com/KenanAtmaca/KSliderCard?style=social"/>
</p>

## Requirements

- Xcode 9.0 +
- iOS 11.0 or greater

## Installation

### CocoaPods

1. Install [CocoaPods](http://cocoapods.org)
2. Add this repo to your `Podfile`

```ruby
platform :ios, '11.0'

target 'ProjectName' do
  use_frameworks!
  pod 'KSliderCard', :git => 'https://github.com/KenanAtmaca/KSliderCard'
end
```

3. Run `pod install`
4. Open up the new `.xcworkspace` that CocoaPods generated
5. Whenever you want to use the library: `import KSliderCard`

### Manually

1. Simply download the `KSliderCard` source files and import them into your project.

## Usage

```Swift
import UIKit
import KSliderCard

class ViewController: UIViewController {
    
    var sliderCard:KSliderCard!

    override func viewDidLoad() {
        super.viewDidLoad()
        showSliderCard()
    }
    
    func showSliderCard() {
        sliderCard = KSliderCard(items: [KSliderCardItem(image: UIImage(named: "img1"), title: "Hello 🎉", text: "..."),
                                         KSliderCardItem(image: UIImage(named: "img2"), title: "Hii", text: "..."),
                                         KSliderCardItem(image: UIImage(named: "img3"), title: "Heey", text: "...")])
        sliderCard.options.isBlurImage = false
        sliderCard.options.backgroundStyle = .dark
        sliderCard.options.backAction = true
        sliderCard.options.backButtonImage = UIImage(named: "back")
        sliderCard.options.backButtonSize = CGSize(width: 64, height: 64)
        sliderCard.options.backButtonBackgroundColor = .clear
        sliderCard.options.backButtonColor = .white
        sliderCard.show(to: self.view)
    }
}

```

## Options

```Swift
titleColor:UIColor?
titleFont:UIFont?
textColor:UIColor?
textFont:UIFont?
isBlurImage:Bool = true
isAnimation:Bool = true
backgroundStyle:KSliderBackgroundStyle? // .dark, .light
blurStyle:KSliderBackgroundStyle? // .dark, .light
backAction:Bool = false
backButtonTitle:String?
backButtonImage:UIImage?
backButtonBackgroundColor:UIColor?
backButtonColor:UIColor?
backButtonTextColor:UIColor?
backButtonFont:UIFont?
backButtonSize:CGSize?
```

## License
Usage is provided under the [MIT License](http://http//opensource.org/licenses/mit-license.php). See LICENSE for the full details.
