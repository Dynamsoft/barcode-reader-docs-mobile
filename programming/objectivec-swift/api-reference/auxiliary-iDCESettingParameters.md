---
layout: default-layout
title: Dynamsoft Barcode Reader Objective-C & Swift API Reference - iDCESettingParameters Class
description: This page shows the iDCESettingParameters Class of Dynamsoft Barcode Reader for iOS SDK.
keywords: iDCESettingParameters, class, api reference, iOS
needAutoGenerateSidebar: true
noTitleIndex: true
pageStartVer: 8.2.1
permalink: /programming/objectivec-swift/api-reference/auxiliary-iDCESettingParameters.html
---

# Class iDCESettingParameters

> Note:  
>  
> - This class is removed in 9.0 version. Please use the [video methods](primary-video.md) for video barcode scanning if you are using the latest version.

Stores the iDCESettingParameters information.

```objc
@interface iDCESettingParameters
```

| Attribute | type | Descriptions |
|-----------|------| ------------ |
| [`cameraInstance`](#camerainstance) | *DynamsoftCameraEnhancer* | The Camera Enhancer instance |
| [`textResultDelegate`](#textresultdelegate) | *DBRTextResultDelegate* | Set text result callback. |
| [`textResultData`](#textresultdata) | *NSObject* | Transfer user data. |
| [`intermediateResultDelegate`](#intermediateresultdelegate) | *DBRIntermediateResultDelegate* | Set intermediate result callback. |
| [`intermediateResultData`](#intermediateresultdata) | *NSObject* | Transfer user data. |

## cameraInstance

The instance of Camera Enhancer. This instance will enable DBR to fetch frames from the Camera Enhancer frame queue and also take control of the status of the camera.

```objc
DynamsoftCameraEnhancer* cameraInstance
```

## textResultDelegate

Set text result delegate.

```objc
DBRTextResultDelegate* textResultDelegate
```

The `textResultDelegate` includes the following Parameters:

`frame`: The frame data.  
`frameID`: The ID of frame.  
`results`: The recognized barcode result of the frame.  
`userData`: Arguments passed to your function.

## textResultData

Set the `UserData` of the `textResultDelegate`.

```objc
NSObject* textResultData
```

## intermediateResultDelegate

Set intermediate result delegate.

```objc
DBRIntermediateResultDelegate* intermediateResultDelegate
```

The `intermediateResultDelegate` includes the following Parameters:

`frameID`: The ID of frame.  
`results`: The intermediate result of the frame.  
`userData`: Arguments passed to your function.

## intermediateResultData

Set the `UserData` of the `intermediateResultDelegate`.

```objc
NSObject* intermediateResultData
```
