+++
author = "author"
date = "2017-09-30T15:11:24Z"
description = "description"
draft = true
keywords = ["key","words"]
tags = ["one","two"]
title = "does the iphone support nfc"
topics = ["topic 1"]
type = "post"

+++
At GoWi.Fi we have been bravely waiting for Apple to join everyone else in supporting NFC tags since Google added NFC functionality to Android in late 2010. 

At WWDC 2017 in June Apple announced that iOS 11 would have support for reading NFC tags and NDEF messages. 

With Apple’s event on Sept. 12th, 2017 Apple has finally announced the new iPhone 8 and the iPhone X. Apple also released iOS 11 to the general public for download on Sept. 19th, 2017. 

iOS 11 includes an NFC SDK for iOS, Core NFC which allows for iPhone apps to read NDEF records from NFC tags. Before this, the NFC controller in the iPhone had only been used to support Apple Pay. This means that all iPhone 7 and newer iPhones will be able to read NFC tags just like Android has been able to do for years. 

Now that it’s possible to read NFC tags on an iPhone, we will investigate how NFC works on an iPhone, how NFC is different on iOS than on Android and what this means for you.

## How NFC Works on the iPhone
For those that are not familiar with NFC, here is a short NFC tutorial. All modern smartphones now have an NFC controller chip in them, similar to WiFi and GPS. NFC tags are inexpensive, passive RFID tags that are stuck on, or embedded into products, packaging, promotional items and many other things. NFC tags have a small amount of memory, which when written to (encoded) carry a bit of data which can be read by an NFC enabled devices, such as a phone or fixed NFC reader. When the phone comes in very close proximity to the NFC tag (25 mm), the phone detects the NFC tag and can interact with it. 

The phone reads the data that was previously encoded onto the NFC tag, but there are several other modes of operation possible. Based on the software running on the device (app), the device often performs an action based on the type of data encoded onto the NFC tag. For example, if the website https://3dquu.com is encoded onto an NFC tag, a common action that would be done on the phone would be to open that URL in a browser. Thus an NFC tag can be placed on a physical thing to provide a digital experience when the NFC tag is interacted with by a phone.

Apple’s implementation of NFC on iOS is different than Android, which is what most NFC users and developers are used to. Apple has taken a more conservative approach to NFC. 

Here are some important facts about NFC on the iPhone:

 - Only the iPhone 7, iPhone 8 and iPhone X supports reading NFC tags.

 - The iPhone 6 and earlier does not support reading NFC tags. 

 - While the iPhone 6 does have an NFC controller to support Apple Pay, Apple has decided not to allow the iPhone 6 to read NFC tags. 

 - Previous versions of the iPhone do not have any NFC hardware and cannot use NFC tags.

 - An app is required to use the NFC SDK on iOS. iOS does not have any native support for reading NFC labels and performing actions on the local device. 

 - A 3rd party app must be installed to implement these steps. Android has always handled basic NDEF record types natively, without an app installed. For example, if a NDEF website record is encoded onto an NFC tag, on Android it will automatically open the website in a browser when interacted with while on the home screen; in iOS, a 3rd party app must be installed and opened first before an NFC tag can be read. An iPhone NFC App, such as the  GoToTags iPhone App is required. 

 - Only tag reader mode is supported. NFC has several methods of operation; reader/writer, tag emulation and peer-to-peer. On iOS, only the reader/writer mode is supported, and even then only reading is supported. 

 - Only NDEF encoded NFC tags can be interpreted by the iPhone. Unencoded NFC tags are not able to be read. This has implications for developers and hobbyists, although it probably doesn’t matter much to consumers who usually just read NFC tags and don’t encode them. NFC tags purchased from Amazon are usually not encoded and will not work on the iPhone until encoded. 

 - An iPhone NFC app only has access to the NDEF records; apps do not have access to the NFC chip’s UID or other special features in the NFC chip. 

 - An app must explicitly trigger the process of reading NFC tags. In Android apps can poll for NFC tags in the background and listen to NDEF messages the app was specifically coded for. In iOS, reading NFC tags is an explicit, user-initiated action that must occur in the foreground.

 - iOS does not have the Android idea of a NDEF record type to trigger an app download (AAR record). When Apple does allow for more open reading of NFC tags, hopefully, we will see an equivalent to the AAR on iOS.
