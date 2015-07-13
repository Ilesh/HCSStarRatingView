# HCSStarRatingView

`HCSStarRatingView` is a `UIControl` subclass to easily provide users with a basic star rating interface.

It supports all device resolutions and requires no images do render the stars, thanks to <a href="http://www.paintcodeapp.com" target=_blank>PaintCode</a>.

<img src="https://raw.github.com/hugocampossousa/HCSStarRatingView/master/Assets/ios.gif" width="288" height="86	" />

## Installation

### Carthage

```
github "hugocampossousa/HCSStarRatingView"
```

### CocoaPods

```
pod 'HCSStarRatingView', :git => 'https://github.com/hugocampossousa/HCSStarRatingView.git'
```

and run `pod install`

### Manually

You can also install it manually by copying `HCSStarRatingView.{h|m}` into your project or including the project in your own project/workspace, similar to what's being done in `Sample`.

## Usage

### Programatically

You can create a new rating view programatically by importing HCSStarRatingView.h and HCSStarRatingView.m into your project and:

```objective-c
#import "HCSStarRatingView.h"
```

```objective-c
HCSStarRatingView *starRatingView = [[HCSStarRatingView alloc] initWithFrame:CGRectMake(50, 200, 200, 50)];
starRatingView.maximumValue = 10;
starRatingView.minimumValue = 0;
starRatingView.value = 0;
starRatingView.tintColor = [UIColor redColor];
[starRatingView addTarget:self action:@selector(didChangeValue:) forControlEvents:UIControlEventValueChanged];
[self.view addSubview:starRatingView];
```

It also supports half-star ratings:

```objective-c
starRatingView.allowsHalfStars = YES;
starRatingView.value = 2.5f;
```

### Interface Builder

`HCSStarRatingView` also implements IB_DESIGNABLE and IBInspectable so you can fully customize it in Interface Builder.

<a href="https://raw.github.com/hugocampossousa/HCSStarRatingView/master/Assets/ib.png"><img src="https://raw.github.com/hugocampossousa/HCSStarRatingView/master/Assets/ib.png"/></a>

## Accessibility

Users with specific needs should be able to fully read and interact with `HCSStarRatingView`, since it fully supports VoiceOver.

If you or your users have other specific needs and you're having issues with this control, please contact me so we can figure it out! :-)

## Contact
Hugo Sousa
* [github.com/hugocampossousa](http://github.com/hugocampossousa)
* [twitter/hsousa](http://twitter.com/hsousa)
* [hsousa@me.com](hsousa@me.com)

## License
HCSStarRatingView is available under the MIT license. See the LICENSE file for more info.
