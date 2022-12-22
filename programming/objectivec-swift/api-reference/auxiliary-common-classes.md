---
layout: default-layout
title: Common Classes - Dynamsoft Barcode Reader iOS API Reference
description: The common classes of Dynamsoft Barcode Reader SDK iOS edition such as point, quadrilateral, & region definition.
keywords: Common Classes, API reference, iOS
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
permalink: /programming/objectivec-swift/api-reference/auxiliary-common-classes.html
---

# Common Classes

## [iDBRPoint](auxiliary-iDBRPoint.md)

The point class Stores the x and y coordinate of the points.

```objc
@interface iDBRPoint
```

| Attribute | Type | Descriptions |
|---------- | ---- | ------------ |
| [`x`](auxiliary-iDBRPoint.md#x) | *NSInteger* | The X coordinate of the point. |
| [`y`](auxiliary-iDBRPoint.md#y) | *NSInteger* | The y coordinate of the point. |

## [iQuadrilateral](auxiliary-iQuadrilateral.md)

This class stores the quadrilateral points data.

```objc
@interface iQuadrilateral 
```  

| Attribute | Type | Descriptions |
|---------- | ---- | ------------ |
| [`points`](auxiliary-iQuadrilateral.md#points) | *NSArray\** | Four vertexes in a clockwise direction of a quadrilateral. Index 0 represents the left-most vertex. |

## [iRegionDefinition](auxiliary-iRegionDefinition.md)

This class stores the region data. You can make settings on the scan region through this class.

```objc
@interface iRegionDefinition
```  

| Attribute | Type | Descriptions |
|---------- | ---- | ------------ |
| [`regionTop`](auxiliary-iRegionDefinition.md#regiontop) | *NSInteger* | The top-most coordinate or percentage of the region. |
| [`regionLeft`](auxiliary-iRegionDefinition.md#regionleft) | *NSInteger* | The left-most coordinate or percentage of the region. |
| [`regionRight`](auxiliary-iRegionDefinition.md#regionright) | *NSInteger* | The right-most coordinate or percentage of the region. |
| [`regionBottom`](auxiliary-iRegionDefinition.md#regionbottom) | *NSInteger* | The bottom-most coordinate or percentage of the region. |
| [`regionMeasuredByPercentage`](auxiliary-iRegionDefinition.md#regionmeasuredbypercentage) | *NSInteger* | Sets whether or not to use percentage to measure the region size. |
