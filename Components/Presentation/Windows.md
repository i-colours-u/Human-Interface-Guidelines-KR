> `Window`는 앱 또는 게임의 사용자 인터페이스를 표시하는 UI 요소가 포함되어 있습니다.

  
![A stylized representation of a window with close, minimize, and full-screen buttons. The image is tinted red to subtly reflect the red in the original six-color Apple logo.](https://docs-assets.developer.apple.com/published/e678408ee6b4eb19f2cfed9a9e4cef47/components-window-intro@2x.png)

Depending on the platform, device, and context, a window (or _scene_) can be undetectable to people. For example, in platforms where the default experience is full screen, like iOS, tvOS, and watchOS, people view and interact with the content inside a window — they don’t view or interact with the window itself. In these cases, you don’t need to design the appearance of the window or scene itself in your app or game. For developer guidance, see [`Scene`](https://developer.apple.com/documentation/SwiftUI/Scene) and [`UIWindow`](https://developer.apple.com/documentation/uikit/uiwindow).

Note

In SwiftUI, a scene is a part of an app’s interface that can contain windows and view hierarchies. The terms _window_ and _scene_ are often used synonymously, especially in design guidance, but in help and other content that describes your app to people, use _window_ — not _scene_ — if you need to refer to these high-level content containers.

In [visionOS](https://developer.apple.com/design/human-interface-guidelines/windows#visionOS), [iPadOS](https://developer.apple.com/design/human-interface-guidelines/windows#iPadOS), and [macOS](https://developer.apple.com/design/human-interface-guidelines/windows#macOS) — in contrast to iOS, tvOS, and watchOS — people are aware of windows as visually distinct objects, because they can typically open, close, resize, and relocate individual windows, as well as view multiple windows at the same time. In visionOS, people can also interact with a _volume_, which is a container optimized for displaying 3D content that people can view from any angle; for guidance, see [Volumes](https://developer.apple.com/design/human-interface-guidelines/windows#Volumes).

The guidance below applies to windows that people can view and manipulate as separate objects. For guidance on other types of window-like views in all platforms, see [Alerts](https://developer.apple.com/design/human-interface-guidelines/alerts), [Panels](https://developer.apple.com/design/human-interface-guidelines/panels), [Popovers](https://developer.apple.com/design/human-interface-guidelines/popovers), and [Sheets](https://developer.apple.com/design/human-interface-guidelines/sheets).

For guidance laying out content within a window or scene, see [Layout](https://developer.apple.com/design/human-interface-guidelines/layout); for guidance laying out content in Apple Vision Pro space, see [Spatial layout](https://developer.apple.com/design/human-interface-guidelines/spatial-layout).