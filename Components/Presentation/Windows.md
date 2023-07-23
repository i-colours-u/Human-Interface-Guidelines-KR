# Windows
[원본 링크](https://developer.apple.com/design/human-interface-guidelines/windows)

> `Window`는 앱 또는 게임의 사용자 인터페이스를 표시하는 UI 요소가 포함되어 있습니다.

  
![A stylized representation of a window with close, minimize, and full-screen buttons. The image is tinted red to subtly reflect the red in the original six-color Apple logo.](https://docs-assets.developer.apple.com/published/e678408ee6b4eb19f2cfed9a9e4cef47/components-window-intro@2x.png)

플랫폼, 디바이스 및 상황에 따라 `Window` (또는 `Scene`)가 사용자에게 감지되지 않을 수 있습니다.
예를 들어 iOS, tvOS, watchOS와 같이 기본 환경이 전체 화면인 플랫폼에서는 사람들이 `Window` 안의 콘텐츠를 보고 상호 작용할 뿐 `Window` 자체를 보거나 상호 작용하지 않습니다.
이러한 경우 앱이나 게임에서 `Window` 이나 `Scene` 자체의 모양을 디자인할 필요가 없습니다. 
개발자 지침은 [Scene](https://developer.apple.com/documentation/SwiftUI/Scene) 및 [UIWindow](https://developer.apple.com/documentation/uikit/uiwindow)를 참조하세요.

> Note
> 
> SwiftUI에서 `Scene`이라는 개념은 `Window`와 뷰 계층 구조를 모두 포함하는 앱 인터페이스의 일부 개념입니다. 
> `Window`와 `Scene` 이라는 용어는 동의어로 (특히 디자인 가이드에서) 사용되는 경우가 많습니다. 
> 하지만 여러분이 만약, 사람들에게 앱을 설명하는 도움말을 작성하는 경우 + 높은 level의 컨텐츠를 설명 해야 하는 경우, `Scene` 보다 `Window` 라는 용어를 사용하기를 권장합니다.

iOS, tvOS 및 watchOS와 달리 visionOS, iPadOS 및 macOS에서는 일반적으로 개별 `window` 을 열고, 닫고, 크기를 조정하고, 재배치할 수 있을 뿐만 아니라 동시에 여러 개의 `window`을 볼 수 있기 때문에 사람들은 `window`을 시각적으로 구분되는 개체로 인식합니다. 
또한 visionOS에서는 사람들이 어느 각도에서나 볼 수 있는 3D 콘텐츠를 표시하는 데 최적화된 컨테이너인 `volume`과 상호 작용할 수 있습니다.

아래 나와있는 가이드라인은 사용자가 별도의 개체로 보고 조작할 수 있는 `window`에 적용되는 사항입니다. 모든 플랫폼에서 `window`와 비슷하게 사용 할 수 있는 요소로는 [Alerts](https://developer.apple.com/design/human-interface-guidelines/alerts), [Panels](https://developer.apple.com/design/human-interface-guidelines/panels), [Popovers](https://developer.apple.com/design/human-interface-guidelines/popovers), [Sheets](https://developer.apple.com/design/human-interface-guidelines/sheets)가 있습니다.

`Window`또는 `Scene` 내에 콘텐츠를 배치하는 방식은 [Layout](https://developer.apple.com/design/human-interface-guidelines/layout) 문서를 참고하세요. Apple Vision Pro 공간에 콘텐츠를 배치하는 지침은 [Spatial layout](../../Foundations/Spatial-layout.md)문서를 참고하세요.

---

## visionOS
visionOS 앱은 `window` 또는 `volume`을 사용하여 컨테이너에 콘텐츠를 표시할 수 있습니다.
일반적으로 2D 또는 3D 콘텐츠를 표시하려면 Mail의 받은 편지함이나 USDZ 개체가 포함된 Safari의 웹 페이지와 같이 `window`를 사용합니다.
게임 보드나 지구본과 같은 3D 콘텐츠 및 개체를 표시하려면 일반적으로 `volume`을 사용합니다.

> USDZ: 애플과 픽사가 같이 만든 AR content를 표시하는 3D file format 입니다.

| `window` | `volume` |
| -------- | -------- |
| ![](https://i.imgur.com/R2qTH4o.png)|     ![](https://i.imgur.com/UqihxBc.png)

> Note
> 
> 시스템은 사람들이 여는 각 `window`과 `volume`의 초기 위치를 정의합니다. 공유 공간과 전체 공간 모두에서 사람들은 `window`와 `volume`을 원하는 새로운 위치로 옮길 수 있습니다.

visionOS의 `window`은 다른 플랫폼의 고유한 `window`와 모양과 동작이 비슷하기 때문에 사람들은 즉시 익숙해집니다. 
예를 들어, visionOS `window`은 직립형(바로 서 있는 형태) 평면에 정렬되고 공유 공간에서 다른 앱 `window`와  나란히 표시될 수 있습니다. 
또한, 사용자가 이동, 크기 조정, 닫을 수 있는 시스템 정의 컨트롤을 제공합니다. `window` 관리 컨트롤 외에도 `window`에는 공유 메뉴, [tab bar](https://developer.apple.com/design/human-interface-guidelines/tab-bars), [toolbar](https://developer.apple.com/design/human-interface-guidelines/toolbars) 및 하나 이상의 [Ornaments](https://developer.apple.com/design/human-interface-guidelines/ornaments)을 포함할 수 있습니다.


![](https://i.imgur.com/mULr0tq.jpg)

> `window` 1개를 띄워놓은 상황입니다.

visionOS `window`는 수정할 수 없는 배경 [material](https://developer.apple.com/design/human-interface-guidelines/materials)인 [glass](https://developer.apple.com/design/human-interface-guidelines/materials#visionOS) 를 사용하여 빛과 실제 및 가상 물체를 모두 투과할 수 있습니다. 
[glass](https://developer.apple.com/design/human-interface-guidelines/materials#visionOS)  `window`는 콘텐츠가 주변 환경의 일부처럼 느껴지도록 도와주며, 스페큘러(물체 표면에서의 반사광을 의미함) 반사와 그림자를 사용하여 `window`의 크기와 위치를 전달할 수 있습니다. 
기본 스타일을 사용하여 `window`을 만들면 자동으로 유리 배경이 적용됩니다. 개발자 지침은 [DefaultWindowStyle](https://developer.apple.com/documentation/SwiftUI/DefaultWindowStyle)을 참조하세요.

기본적으로 `window` 크기는 1306 x 734pt입니다. `window`가 처음 열리면 시스템은 착용자의 약 2미터 앞에 창을 배치하여 약 3미터의 가로 길이(width)를 제공합니다.

또한 이 시스템은 표준 `window` 내의 보기 및 컨트롤에 하이라이트와 그림자를 추가하여 [depth(깊이)](../../Foundations/Spatial-layout.md#Depth)을 부여하고 특히 사람들이 `window`를 비스듬히 볼 때 더욱 실감나게 느껴지도록 도와줍니다.
표준 창에 3D 콘텐츠를 표시할 수 있지만 콘텐츠가 `window` 표면에서 너무 멀리 확장되면 시스템에서 잘립니다. 더 깊은 3D 콘텐츠를 표시하려면 `volume`을 사용하십시오.

![](https://i.imgur.com/tDKlGkp.png)

> 3D 컨텐츠가 포함된 `window`를 띄워놓은 상황입니다.

#### 익숙한 인터페이스를 제공하고 익숙한 작업을 지원하려면 표준 `window`을 사용하는 것을 권장합니다.

사람들이 이미 익숙한 인터페이스를 표시하고 의미 있는 콘텐츠와 활동을 위해 더 몰입도 높은 경험을 예약하여 앱에서 집과 같은 편안함을 느낄 수 있도록 하세요. 
자세한 내용은 [Immersive experiences](../../Foundations/Immersive_experiences.md) 을 참조하세요. 게임 보드와 같이 경계가 있는 3D 콘텐츠를 표시하려면 `volume`을 사용하는 것이 좋습니다.

#### `window` 안의 빈 공간을 최소화 할 수 있는 초기 `window` 크기를 선택합니다.
빈 공간이 너무 많으면 `window`가 불필요하게 커 보일 뿐만 아니라 사람들의 공간에 있는 다른 콘텐츠를 가릴 수 있습니다.

#### `window`의 콘텐츠에 적합한 기본 모양을 표기 할 수 있도록 설계해야 합니다.
예를 들어 슬라이드 창은 넓기 때문에 기본 Keynote 창은 넓고,
대부분의 웹 페이지가 너비보다 훨씬 길기 때문에 기본 Safari 창은 높습니다.

#### 가능하면 사람들이 앱 `window` 크기를 조정할 수 있도록 허용해야 합니다.
사람들은 공간을 맞춤 설정할 때 `window` 크기를 조정할 수 있다는 점을 높이 평가합니다. 
적절한 경우 최소 및 최대 크기 값을 설정하여 사람들이 `window` 크기를 조정할 때 `window`가 계속 작동하고 보기 좋게 유지되도록 할 수 있습니다.

#### 앱에서 사람들이 몰입하고 싶어할 만한 순간이나 콘텐츠를 찾아보세요. 
앱이 대부분 `window`를사용하더라도 몰입형 기능을 제공 했을 때 더 효과적인 기능이 있을 수 있습니다.
예를 들어 사진 앱에서 파노라마 사진을 확장된 보기로 열면 사용자가 사진 속에 있는 것처럼 느낄 수 있습니다.
자세한 내용은 [Immersive experiences](../../Foundations/Immersive_experiences.md)을 참조하세요.

#### 항상 `window`의 시각적 경계가 포함된 `scene`의 크기와 일치하는지 확인하세요. 
`scene`이 `window`의 가시적 크기를 초과하면 `window` 컨트롤이 잘못 배치되고 `window`가 예상한 대로 표시되지 않아 상호 작용이 어려워질 수 있습니다. 
개발자 지침은 [Scene](https://developer.apple.com/documentation/SwiftUI/Scene)을 참조하십시오.


### Volumes
`volume`은 수평 베이스가 있으며 지구본처럼 사람들이 어느 각도에서나 볼 수 있는 3D 콘텐츠를 표시하는 데 도움이 됩니다.

![](https://i.imgur.com/hmvZ1yK.jpg)

`volume`과 `window`는 몇 가지 유사점이 있습니다:

공유 공간에서는 `window` 에서와 마찬가지로 시스템이 `volume`의 초기 위치를 결정합니다.

- `volume`은 사람들이 `window` 위치를 변경하거나 닫을 때 사용하는 것과 동일한 관리 제어 기능을 제공합니다.

- `volume`은 [glass](https://developer.apple.com/design/human-interface-guidelines/materials#visionOS) 배경을 사용할 수 있습니다.

하지만, `volume`과 `window`는 시스템에서 적용하는 크기 조정 유형이 다릅니다. 비전OS는 `window`에서는 동적 크기 조정을 자동으로 사용하지만 `volume`에서는 고정 크기 조정을 사용합니다.


풍부한 3D 콘텐츠를 표시하려면 `volume`을 사용하는 것이 좋습니다. 
친숙한 UI 중심의 인터페이스를 표시하려면 일반적으로 `window`을 사용하는 것이 가장 적합합니다.

---

### 연관 내용
- [Split views](https://developer.apple.com/design/human-interface-guidelines/split-views)
- [Multitasking](https://developer.apple.com/design/human-interface-guidelines/multitasking)

### 개발자 문서 참고
- [`Scene`](https://developer.apple.com/documentation/SwiftUI/Scene)
- [`WindowGroup`](https://developer.apple.com/documentation/SwiftUI/WindowGroup)
- [`NSWindow`](https://developer.apple.com/documentation/appkit/nswindow)

### 영상

| [Design for spatial user interfaces](https://developer.apple.com/videos/play/wwdc2023/10076) | [Principles of spatial design](https://developer.apple.com/videos/play/wwdc2023/10072) |
| -------- | -------- |
| ![](https://i.imgur.com/kTIL2Ke.png)|     ![](https://i.imgur.com/PD74ZGq.png)
