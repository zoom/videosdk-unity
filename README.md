# Zoom Video SDK for Unity (wrapper)

This repository contains the **C# wrapper** for Zoom Video SDK for Unity (Android, iOS, macOS, and Windows), plus sample Prefabs and Resources.

For **native** Video SDK binaries: those stay on the Marketplace. The sample scene, TextMesh Pro, and Editor build scripts are not in this repository.

## Prerequisites

- A Zoom Video SDK app on the [Zoom App Marketplace](https://marketplace.zoom.us/)
- Unity Editor (see [Video SDK for Unity get started](https://developers.zoom.us/docs/video-sdk/unity/get-started/))

## Native libraries (Marketplace)

Download the **matching version** of Video SDK for Unity and the platform Video SDK packages from the Marketplace. Copy native files into your Unity project:

| Platform | Place files here |
|---|---|
| Windows | `Assets/Plugins/Windows/bin/` and `lib/` — copy **native** Video SDK (`videosdk.dll` and other Zoom binaries). `ZMWinUnityVideoSDK.dll` / `ZMWinUnityVideoSDK.lib` are the Unity C# P/Invoke bridge and are included in this repo. |
| macOS | `Assets/Plugins/macOS/` — copy **native** `ZMVideoSDK.framework` from the macOS Video SDK. `libZMMacUnityVideoSDK.dylib` is the Unity bridge (it links that framework) and is included in this repo. |
| iOS | `Assets/Plugins/iOS/` — copy **native** Video SDK frameworks from the iOS package. `libiOSStaticLib.a` (device and Simulator) is the Unity `__Internal` wrap library and is included in this repo. |
| Android | `Assets/Plugins/Android/` — copy **native** Video SDK `.aar` from Marketplace. This repo includes `ZoomVideoSDKNotificationService-debug.aar`, `AndroidManifest.xml`, and the gradle templates. |


## Wrapper source

Copy `Assets/Scripts/Common` plus the platform folders you need (`Android`, `iOS`, `macOS`, `Windows`) into your Unity project’s `Assets` tree, or clone this repo and keep only those folders. Also keep the Unity bridge binaries and Android helper files under `Assets/Plugins/` that are listed above.

Sample UI assets live in `Assets/Prefab/` and `Assets/Resources/`. Sample screen scripts live in `Assets/Scripts/Screens/`. The sample scene, TextMesh Pro, and Editor build scripts are not in this tree. 

## Documentation

- [Get started](https://developers.zoom.us/docs/video-sdk/unity/get-started/)
- [Integrate](https://developers.zoom.us/docs/video-sdk/unity/integrate/)
- [API reference](https://marketplacefront.zoom.us/sdk/custom/unity/index.html)

## License

Use of Zoom Video SDK is subject to Zoom’s [Video SDK Terms](https://www.zoom.com/en/trust/video-sdk-terms/) and Marketplace terms. This wrapper does not grant rights to redistribute the native SDK.
