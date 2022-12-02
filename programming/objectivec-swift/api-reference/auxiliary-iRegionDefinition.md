---
layout: default-layout
title: Dynamsoft Barcode Reader Objective-C & Swift API Reference - iRegionDefinition Class
description: This page shows the iRegionDefinition Class of Dynamsoft Barcode Reader for iOS SDK.
keywords: iRegionDefinition, class, api reference, objective-c, oc, swift
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /programming/objectivec-swift/api-reference/auxiliary-iRegionDefinition.html
---

# Class iRegionDefinition

Stores the region information.  

```objc
@interface iRegionDefinition
```  

| Attribute | Type | Descriptions |
|---------- | ---- | ------------ |
| [`regionTop`](#regiontop) | *NSInteger* | The top-most coordinate or percentage of the region. |
| [`regionLeft`](#regionleft) | *NSInteger* | The Left-most coordinate or percentage of the region. |
| [`regionRight`](#regionright) | *NSInteger* | The Right-most coordinate or percentage of the region. |
| [`regionBottom`](#regionbottom) | *NSInteger* | The Bottom-most coordinate or percentage of the region. |
| [`regionMeasuredByPercentage`](#regionmeasuredbypercentage) | *NSInteger* | Sets whether or not to use percentage to measure the region size. |

## regionTop

The top-most coordinate or percentage of the region.

```objc
@property (nonatomic, assign) NSInteger regionTop;
```

**Value Range**

regionMeasuredByPercentage = 0: [0, 0x7fffffff]  
regionMeasuredByPercentage = 1: [0, 100]  

**Default Value**

0

## regionLeft

The left-most coordinate or percentage of the region.

```objc
@property (nonatomic, assign) NSInteger regionLeft;
```

**Value Range**

regionMeasuredByPercentage = 0: [0, 0x7fffffff]  
regionMeasuredByPercentage = 1: [0, 100]  

**Default Value**

0

## regionRight

The right-most coordinate or percentage of the region.

```objc
@property (nonatomic, assign) NSInteger regionRight;
```

**Value Range**

regionMeasuredByPercentage = 0: [0, 0x7fffffff]
regionMeasuredByPercentage = 1: [0, 100]

**Default Value**

0

## regionBottom

The bottom-most coordinate or percentage of the region.

```objc
@property (nonatomic, assign) NSInteger regionBottom;
```

**Value Range**

regionMeasuredByPercentage = 0: [0, 0x7fffffff]  
regionMeasuredByPercentage = 1: [0, 100]  

**Default Value**

0

## regionMeasuredByPercentage

Sets whether or not to use percentage to measure the region size.

```objc
@property (nonatomic, assign) NSInteger regionMeasuredByPercentage;
```

**Value Range**

[0, 1]

**Default Value**

0

**Remarks**

When it's set to 1, the values of Top, Left, Right, Bottom indicate percentage (from 0 to 100); Otherwise, they indicate coordinates. 0: not by percentage 1: by percentage.
