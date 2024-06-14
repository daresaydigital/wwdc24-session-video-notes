# WWDC 24 - Session videos

This document will list some of the [Session videos from WWDC 24](https://developer.apple.com/videos/wwdc2024) ([youtube alternative to videos](https://www.youtube.com/@AppleDeveloper/videos)) and our own summary and comment if it is a good watch, or what ever note we'd like to add.

## Catch up on accessibility in SwiftUI
[Catch up on accessibility in SwiftUI](https://developer.apple.com/videos/play/wwdc2024/10073/) where they go through the accessibility elements provided by SwiftUI, and how they can be customized!

### Teddy's comments
SwiftUI creates accessibility elements per VIEW, which is awesome but it can also be too much. An Accessibility Element has three things: Label, Traits and Actions. If we have our own customized View (which is very normal, e.g. a VStack or HStack) then we can add an Accessibility modifier, e.g. `.accessibilityElement(children: .combine)` (this specific one will add all underlying accessibility elements to ONE. AWESOME). An update to the `.accessibilityLabel()` is the argument `isEnabled:` - here it applies the accessibility label only when it is enabled (a boolean variable is true). This keeps the original accessibility label (if it is good enough) and add a new one only when we need it. On macOS, the `.accesibilityLabel()` now handles View too! It can extract the text from the view (don't know how it will handle different type of views!). This gives additional info to the VoiceOver feature - at least for hover! New accessibility modifier: `.accessibilityDropPoint()` - helps the user drag and drop.
Good note: Always try how the views are working with accessibility tools available in the OS, such as VoiceOver.

This video is a must watch if you're interested in making an app accessible.


## Meet Swift Testing
['Meet Swift Testing' session](https://developer.apple.com/videos/play/wwdc2024/10179/) where they talk about the new testing for Swift! 

### Teddy's comments
It can now be used in Xcode too and exist together with XCTest. If we are using UIKit we should still use XCTest. As said, it's new so maybe not all the functions are there as XCTest and other frameworks from Apple has but I think it's an easy and good start for people like me who feels a bit unsecure and new when it comes to testing. Cool extra thing is it can be used where ever Swift can be used. 
Check it out! :) 

## What's new in SwiftUI
['What's new in SwiftUI'](https://developer.apple.com/videos/play/wwdc2024/10144/) where they talk about the new stuff for SwiftUI!

### Teddy's comments
In the first half they show loads of new stuff from SwiftUI but mainly focusing on iPadOS, macOS, visionOS, and watchOS. There are some cool stuff and I would guess these can be used for iOS too. There are some new animations (wiggle wiggle), new stuff for SF Symbols and color mesh! That one I thought was cool.
In the second half they talk and show the improvements that is done to the SwiftUI Foundation. New custom containers! There's a separate video of this. Sounded cool! #Previews gets an update! @FocusState gets an update! Now we can mix  colors too! New scrolling experience! It is easier to control it now! With Swift6, we do not need to use @MainActor anymore for Views, it's default.

Short and sweet: Check it out. It gives a great overview of what's new in SwiftUI, and there are many deep-dive videos for most of the things here.
