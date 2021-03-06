<p align=center>
<a href="">
<img alt="Logo" src="logo.png">
</a>
</p>
<p align=center>
    <a href="https://www.codacy.com/app/witekbobrowski/EPUBKit?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=witekbobrowski/EPUBKit&amp;utm_campaign=Badge_Grade"><img alt="CodacyBadge" src="https://api.codacy.com/project/badge/Grade/35b59c32fd77448da5bab9041ebba524"</a>
    <a href="https://swift.org"><img alt="Swift" src="https://img.shields.io/badge/Swift-4.0-oragne.svg"></a>
    <a href="https://cocoapods.org/pods/EPUBKit"><img alt="CocoaPods" src="https://img.shields.io/badge/pod-0.2.1-blue.svg"></a>
    <a><img alt="Platforms" src="https://img.shields.io/badge/platform-iOS-oragne.svg"></a>
    <a href="https://twitter.com/witekbobrowski"><img alt="Contact" src="https://img.shields.io/badge/contact-@witekbobrowski-blue.svg"></a>
</p>
<p align=center>
📚 A simple swift library for parsing EPUB documents
</p>

__Note:__ This library is still in its early stages! I will experiment and change the API until I am satisfied with the result. I do not reccomend using this library in larger projects (who am I fooling, nobody will use it anyway), although feedback will be highly appreciated 🙇
 
## Installation

#### CocoaPods
Add the following to your `Podfile`:
```
pod 'EPUBKit'
```
__Note:__ Future versions will support [Carthage](https://github.com/Carthage/Carthage) and [Swift Package Manager](https://swift.org/package-manager/) 💃

## Usage
Just import EPUBKit in your swift file.
```
import EPUBKit
```

Initialize document instance with `URL` of your EPUB document. 
```
guard
    let path = Bundle.main.url(forResource: "steve_jobs", withExtension: "epub"),
    let document = EPUBDocument(url: path) 
    else { return }
```

If the document gets parsed correctly, you have access to full document metadata, contents, etc.
```
print(document.title) 
> Steve Jobs
print(document.author) 
> Walter Isaacson
```
__Note:__ Documentation is not yet ready, but you should find it easy to explore the api by yourself 🙃

## Contents

```
EPUBKit
├── EPUBKit.h
├── Info.plist
├── Model
│   ├── Creator.swift
│   ├── EPUBDocument.swift
│   ├── EPUBManifest.swift
│   ├── EPUBManifestItem.swift
│   ├── EPUBMediaType.swift
│   ├── EPUBMetadata.swift
│   ├── EPUBSpine.swift
│   ├── EPUBSpineItem.swift
│   └── EPUBTableOfContents.swift
└── Utils
    ├── EPUBParsable.swift
    ├── EPUBParser.swift
    └── EPUBParserError.swift
```
