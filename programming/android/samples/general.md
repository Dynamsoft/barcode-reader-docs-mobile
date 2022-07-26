---
layout: default-layout
title: Dynamsoft Barcode Reader for Android - General Settings Sample
description: This is the General Settings Sample page of Dynamsoft Barcode Reader for Android SDK.
keywords: android, samples, General
needAutoGenerateSidebar: true
breadcrumbText: GeneralSettings
permalink: /programming/android/samples/general.html
---

# GeneralSettings Sample

This sample shows the general barcode decoding settings and how to configure the settings via [`PublicRuntimeSettings`]({{ site.android_api }}auxiliary-PublicRuntimeSettings.html) struct or JSON when using Dynamsoft Barcode Reader Android SDK.

**View the Sample(s)**

- <a href="https://github.com/Dynamsoft/barcode-reader-mobile-samples/tree/main/android/GeneralSettings/" target="_blank">Java (Android) General Settings Sample</a>

## General Settings

**Barcode Formats & Expected Barcode Count**

The barcode formats settings and the barcode count settings are the most basic settings that determine the readability of your scan app. These parameters are all available for users to make changes through the class [`PublicRuntimeSettings`]({{ site.android_api }}auxiliary-PublicRuntimeSettings.html). To view all available barcode formats, please view the enumeration [`BarcodeFormat`]({{ site.mobile-enum }}barcode-format.html?lang=android) and [`BarcodeFormat_2`]({{ site.mobile-enum }}barcode-format2.html?lang=android).

**Scan Region**

For video barcode decoding scenarios, specifying a **scanRegion** can reduce the size of the processing area, which sharply increases the barcode decoding speed. To specify the scan region, you can use the **CameraEnhancer** method <a href="https://www.dynamsoft.com/camera-enhancer/docs/programming/android/primary-api/camera-enhancer.html?ver=latest#setscanregion" target="_blank">`setScanRegion`</a>. When the **scanRegion** is configured via **CameraEnhancer**, the video frames will be cropped based on the **scanRegion** before being processed by the barcode reader.

## Update the Settings

### Via PublicRuntimeSettings Struct

**Code Snippet**

```java
// General settings (including barcode format, barcode count and scan region) for the instance.
// Obtain current runtime settings of instance.
PublicRuntimeSettings runtimeSettings = reader.getRuntimeSettings();
// Set the expected barcode format you want to read.
// The barcode format our library will search for is composed of BarcodeFormat group 1 and BarcodeFormat group 2.
// So you need to specify the barcode format in group 1 and group 2 individually.
runtimeSettings.barcodeFormatIds = EnumBarcodeFormat.BF_ONED | EnumBarcodeFormat.BF_PDF417 | EnumBarcodeFormat.BF_QR_CODE | EnumBarcodeFormat.BF_DATAMATRIX |EnumBarcodeFormat.BF_AZTEC;
runtimeSettings.barcodeFormatIds_2 = 0;
// Set the expected barcode count you want to read.
runtimeSettings.expectedBarcodesCount = 5;
// Apply the new settings to the instance
reader.updateRuntimeSettings(runtimeSettings);
```

### Via JSON Template

Besides using the [`PublicRuntimeSettings`]({{ site.android_api }}auxiliary-PublicRuntimeSettings.html) class, you can also upload the general barcode settings from stringified JSON data or a JSON file.

#### From JSON String

Use method [`initRuntimeSettingsWithString`]({{ site.android_api }}primary-parameter-and-runtime-settings-advanced.html#initruntimesettingswithstring) to upload the settings via a JSON string.

**Code Snippet**

```java
reader.initRuntimeSettingsWithString("{\"Version\":\"3.0\", \"ImageParameter\":{\"Name\":\"IP1\", \"BarcodeFormatIds\":[\"BF_QR_CODE\"], \"ExpectedBarcodesCount\":10}}", EnumConflictMode.CM_OVERWRITE);
```

#### From JSON File

Use method [`initRuntimeSettingsWithFile`]({{ site.android_api }}primary-parameter-and-runtime-settings-advanced.html#initruntimesettingswithfile) to upload the settings via a JSON file.

**Code Snippet**

```java
// Overwrite the settings if the settings already exist.
reader.initRuntimeSettingsWithFile("your template file path", EnumConflictMode.CM_OVERWRITE);
```

**Related APIs/Parameters**

- Class [`PublicRuntimeSettings`]({{ site.android_api }}auxiliary-PublicRuntimeSettings.html)
- Enum [`BarcodeFormat`]({{ site.mobile-enum }}barcode-format.html?lang=android)
- Enum [`BarcodeFormat_2`]({{ site.mobile-enum }}barcode-format2.html?lang=android)
