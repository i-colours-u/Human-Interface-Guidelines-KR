# Layout

## 다양한 상황에 맞게 조정되는 일관된 레이아웃은 사용자 경험을 더욱 즐겁게 만들고 많은 사람들이 모든 기기에서 좋아하는 앱과 게임을 즐길 수 있도록 도와줍니다.

![A sketch of a small rectangle in the upper-left quadrant of a larger rectangle, suggesting the position of a user interface element within a window. The image is overlaid with rectangular and circular grid lines and is tinted yellow to subtly reflect the yellow in the original six-color Apple logo.](https://docs-assets.developer.apple.com/published/fe3e14f290a6986d2490634a9e2fab0c/foundations-layout-intro@2x.png)

다음 가이드라인은 모든 플랫폼에 맞는 콘텐츠 레이아웃을 디자인하는 데 도움이 됩니다. Apple Vision Pro 공간 전체에 윈도우 및 기타 콘텐츠를 표시하는 방법에 대해 알아보려면 [공간 레이아웃](./Spatial-layout.md)을 참조하세요.

## Safe Area 및 레이아웃 가이드
레이아웃 가이드는 화면에 내용을 위치, 정렬 및 간격을 조절하는 데 도움을 주는 직사각형 영역을 정의합니다. 시스템에는 내용 주변에 표준 여백을 적용하고 최적의 가독성을 위해 텍스트의 너비를 제한하기 쉽게 만드는 미리 정의된 레이아웃 가이드가 포함되어 있습니다. 커스텀 레이아웃 가이드도 만들 수 있습니다.

Safe Area는 보기 내에서 네비게이션 바, 탭 바, 툴바 또는 윈도우가 제공할 수 있는 다른 UI 요소에 의해 가려지지 않는 영역을 정의합니다. Safe Area는 iPhone의 Dynamic Island이나 일부 Mac 모델의 카메라 하우징과 같은 기기들의 요소들을 피하기 위해 중요합니다.

iOS, iPadOS, tvOS 및 visionOS에서 시스템은 앱의 시각적 요소에 영향을 미칠 수 있는 시스템 환경 요소들을 정의하고 있습니다. SwiftUI 또는 Auto Layout을 사용하여 인터페이스가 다양한 특성과 상황에 동적으로 적용하도록 할 수 있습니다. 
다음과 같은 상황에 적용이 가능합니다 :

- 다양한 기기 화면 크기, 해상도 및 색 공간
- 다른 기기 방향 (세로/가로)
- 스플릿 뷰 (아이패드)
- iPad에서의 외부 디스플레이 지원, 디스플레이 줌 및 멀티태스킹 모드
- Dynamic Type 텍스트 크기 변경
- 로컬라이징 기반 국제화 기능, 왼쪽에서 오른쪽 또는 오른쪽에서 왼쪽 레이아웃 방향(LTR, RTL), 날짜/시간/숫자 형식, 글꼴 변형 및 텍스트 길이
- 시스템에서 제공하는 기능이 적용 될 때


## Best practices

### - 사용자 경험을 원활하게 유지하면서 콘텐츠가 최대한 동일하게 표시되는 일관된 레이아웃을 설계해야 합니다. 
기기를 회전하거나 window 크기를 조절하거나 다른 디스플레이를 추가하거나 다른 기기로 전환하는 경우에도 사용자는 여전히 잘 작동하고 익숙한 경험을 기대합니다. 시스템에서 정의한 Safe Area, 여백 및 가이드를 존중하고 (사용 가능한 경우) 레이아웃을 조절하기 위한 modifier를 명확하게 지정하여 적응 가능한 인터페이스를 구축하는 데 도움을 줄 수 있습니다.


### - 각 플랫폼에서 중요한 디스플레이 및 시스템 기능을 고려하세요. 
Safe Area는 다양한 기기의 코너 반경 및 센서 하우징과 같은 기능을 고려하고 iPhone의 Dynamic Island 또는 iPhone 및 iPad의 홈 인디케이터 및 앱 전환과 같은 시스템 요소와의 간섭을 피하는 데 도움이 됩니다. 또한 Safe Area의 크기가 변경되면 콘텐츠를 동적으로 재배치하여 상호작용하는 구성 요소를 고려하는 데 도움이 됩니다.

### - 상대적인 중요성을 전달하기 위해 배치를 활용하세요. 
사람들은 일반적으로 위에서 아래로, 왼쪽에서 오른쪽으로 항목을 읽는 경향이 있으므로 주요 항목을 윈도우, 디스플레이 또는 [시야](https://developer.apple.com/design/human-interface-guidelines/spatial-layout#Field-of-view)의 상단 및 왼쪽에 배치하는 것이 효과적일 수 있습니다.

### - 중요한 정보에 충분한 공간을 제공하여 쉽게 찾을 수 있도록 하세요. 
사람들은 가장 중요한 정보를 즉시 보고 싶어하므로 중요하지 않은 세부 사항으로 지저분하게 만들지 않도록 주의해야 합니다. 보조 정보는 window나 디스플레이의 다른 부분에서 사용할 수 있도록 만들 수 있습니다.

### - 사람들이 원하는 정보를 찾는 데 도움이 되도록 시각적 그룹을 만드세요. 
예를 들어 빈 공간, 배경 모양, 색상, 소재 또는 구분선을 사용하여 요소가 관련되어 있는 때를 나타내고 정보를 구분 짓는 데 도움이 됩니다.

### - 정렬을 사용하여 시각적 스캐닝을 용이하게 하고 조직과 계층을 표현하세요. 
정렬은 앱을 깔끔하고 조직적으로 보이게 만들며, 사람들이 스크롤하거나 눈을 이동하면서 콘텐츠를 추적하는 데 도움을 줄 수 있어 정보를 쉽게 찾을 수 있습니다. 들여쓰기와 함께 정렬은 정보 계층을 이해하는 데도 도움을 줄 수 있습니다.

  
### - 텍스트 크기 변경에 대비하세요.
사용자는 다른 텍스트 크기를 선택할 때 대부분의 앱이 응답할 것으로 기대합니다. 텍스트 크기 변경을 수용하기 위해 레이아웃을 조정해야 할 수도 있습니다. 앱에서 텍스트를 표시하는 가이드에 대한 지침은 [Typography](https://developer.apple.com/design/human-interface-guidelines/typography)를 참조하세요.

### - 사람들이 현재 숨겨진 콘텐츠를 찾을 수 있도록 시각적 힌트를 제공하는 것을 고려하세요. 
예를 들어 큰 컬렉션에 모든 항목을 한 번에 표시할 수 없는 경우 현재 보이지 않는 추가 항목이 있다는 것을 나타내야 합니다. 플랫폼에 따라 사람들이 뷰와 상호작용함으로써 추가 콘텐츠를 공개할 수 있다는 힌트를 제공하기 위해 항목 일부를 표시할 수도 있습니다.

### - 상호작용하는 구성 요소 주변에 충분한 공간을 제공함으로써 사용자가 이를 쉽게 발견할 수 있도록 하세요. 
상호작용하는 구성 요소가 너무 가까이 있거나 다른 콘텐츠가 구성 요소를 가리면 구성 요소를 식별하기 어려울 수 있으며, 이로 인해 앱이나 게임을 사용하기 어려워질 수 있습니다.


### - 여러 기기에서 앱을 미리 보고, 다양한 방향, 로컬라이제이션(언어 및 지역 설정), 텍스트 크기를 사용해 테스트하세요.
일반적으로 와이드 컬러 같은 기능은 실제 기기에서 미리 보는 것이 가장 좋지만, Xcode Simulator를 사용하여 자르기 및 레이아웃 문제를 확인할 수도 있습니다. 예를 들어 iOS 앱이 가로 모드를 지원하는 경우, 시뮬레이터를 사용하여 기기가 왼쪽 또는 오른쪽으로 회전하는지에 관계없이 레이아웃이 훌륭하게 보이는지 확인할 수 있습니다.

### - 필요한 경우 디스플레이 변경에 대응하여 아트워크를 조절하세요.
예를 들어 다른 환경에서 앱을 보는 경우 - 예를 들어 화면의 종횡비가 다른 경우 - 아트워크가 잘려 보이거나 레터박스(letterboxed) 또는 필러박스(pillarboxed) 모양으로 나타날 수 있습니다. 이런 경우에 아트워크의 종횡비를 변경하지 말고 중요한 시각적 콘텐츠가 보이도록 아트워크를 조절하세요. visionOS에서는 window가 z-축을 따라 이동할 때 시스템이 자동으로 창을 축소합니다.


> 레터박스: 상단 하단에 여백이 생기는 현상
> 필러박스: 레터박스와 반대로, 좌우에 여백이 생기는 현상
> 
> 디스플레이 크기와 컨텐츠 비율이 맞지 않아서 두 현상이 일어나게 됨.

## 플랫폼 별 고려사항
## iOS, iPadOS
### - 세로 및 가로 방향을 모두 지원하도록 노력하세요.
사람들은 다양한 이유로 다른 방향을 선택하며, 일반적으로 앱이 모든 상황에서 잘 작동하기를 기대합니다. 앱이 특정 방향에서만 실행되어야 하는 경우에는 사용자에게 디바이스를 맞추도록 지시하지 마세요. 만약 지원되지 않는 방향으로 디바이스를 들고 있을 때 앱이 자동으로 회전하지 않는다면, 사용자는 직감적으로 회전시키라고 판단할 것입니다. 앱이 가로 방향만 지원하는 경우, 사용자가 디바이스를 왼쪽 또는 오른쪽으로 회전시킬 때 모두 잘 작동하도록 확인하세요.


### - 앱이 특정 디바이스에서 실행되는 경우 해당 디바이스의 모든 화면 크기에서 작동함을 보장하세요. 
다시 말해, iPhone 전용 앱은 모든 iPhone 화면 크기에서 작동해야 하며 iPad 전용 앱은 모든 iPad 화면 크기에서 작동해야 합니다. 자세한 내용은 [Device screen sizes and orientations](https://developer.apple.com/design/human-interface-guidelines/layout#Device-screen-sizes-and-orientations)을 참조하세요.

### - 전체 너비(full width) 버튼에 여백을 추가하세요. 
전체 너비 버튼 측면에 표준 시스템 정의 여백을 적용하세요. 화면 하단에 있는 전체 너비 버튼은 일반적으로 둥근 모서리를 가짐과 동시에 Safe Area 하단에 정렬되는 것이 가장 좋으며, 이렇게 함으로써 홈 인디케이터와 충돌하지 않도록 할 수 있습니다.

### - 시각적 콘텐츠를 화면 가득 채우도록 하세요. 
배경이 디스플레이 가장자리까지 확장되고, 횡스크롤 가능한 레이아웃(표 및 컬렉션과 같은)이 하단까지 계속되도록 하세요.

### - iPad에서는 가로 방향에서 화면 양쪽에 컨트롤을 배치하는 것을 고려하세요. 
화면의 왼쪽과 오른쪽에 컨트롤을 배치하면 사용자가 디바이스를 들고 있는 동안 양손으로 쉽게 접근할 수 있습니다.

### - 가능한 경우 화면 하단 가장자리에 상호작용형 요소를 배치하지 마세요. 
방향과 관계없이 사람들은 디스플레이 하단 가장자리에서 시스템 제스처를 사용하여 홈 화면 및 앱 전환기와 같은 기능에 액세스합니다. 이러한 제스처는 이 영역에 구현한 사용자 정의 제스처를 취소할 수 있으므로 주의해야 합니다. 
또한 화면의 모서리에 컨트롤을 배치하는 것은 사용자가 편안하게 접근하기 어려울 수 있으므로 피하세요. 게임에서 컨트롤을 화면 하단 Safe Area 아래에 배치해야 하는 경우 상단과 하단에 배치할 때 일치하는 여백을 사용하세요.
사용자가 컨트롤과 상호 작용하려고 할 때 실수로 홈 인디케이터를 클릭하지 않도록 충분한 공간을 남겨 두세요.

###  - Status bar(상태바) 높이가 달라지는 상황에 대비하세요. 
상태 바 아래에 콘텐츠를 표시하는 경우, 필요에 따라 콘텐츠를 동적으로 재배치하는 데 안전 영역을 사용할 수 있습니다.

### - 특정한 이점을 주거나 사용자 경험을 향상시킬 때에만 상태창을 숨기세요. 
상태 바는 사람들이 유용하게 여기는 정보를 표시하며 대부분의 앱이 완전히 활용하지 않는 화면 영역을 차지하기 때문에 일반적으로 보이도록 유지하는 것이 좋습니다.

## iOS, iPadOS Safe Area

Safe Area는 뷰 내에서 네비게이션 바, 탭 바, 툴바와 같이 뷰 컨트롤러 자체적인 UI요소들에 의해 가려지지 않는 영역을 정의합니다.

| iPhone 세로 모드 | iPhone 가로 모드 |
| ---------------- | ---------------- |
|![An illustration of an iPhone in portrait orientation that displays a shaded rectangle, representing the safe area, and two vertical red strips at the left and right edges of the rectangle that represent margins.](https://docs-assets.developer.apple.com/published/d0c4b02329ef3e73ef068c00dd9aba3e/layout-guides-portrait@2x.png) |          ![An illustration of an iPhone in landscape orientation that displays a shaded rectangle, representing the safe area, and two vertical red strips at the left and right edges of the rectangle that represent margins.](https://docs-assets.developer.apple.com/published/3ac1ce8a02dc0a3babc7931748d62964/layout-guides-landscape@2x.png)


| iPad 세로 모드 | iPad 가로 모드 |
| -------------- | -------------- |
|      ![An illustration of an iPad in portrait orientation that displays a shaded rectangle, representing the safe area, and two vertical red strips at the left and right edges of the rectangle that represent margins.](https://docs-assets.developer.apple.com/published/3f8a6632514396967be535fd7ec6e77d/safe-area-portrait@2x.png)          |   ![An illustration of an iPad in landscape orientation that displays a shaded rectangle, representing the safe area, and two vertical red strips at the left and right edges of the rectangle that represent margins.](https://docs-assets.developer.apple.com/published/1bdc77161228ce6ed4fb5ef4105add66/safe-area-landscape@2x.png)             |

## iOS 키보드 레이아웃 가이드
iOS 15 이후 버전에서는 현재 키보드가 차지하는 공간을 나타내고 안전 영역 여백을 고려하는 키보드 레이아웃 가이드를 제공합니다. 이 가이드를 사용하면 사용자가 어떤 유형의 키보드를 사용하거나 어디에 위치시키더라도 키보드가 앱의 중요한 부분처럼 느껴지도록 도와줍니다. 개발자 가이드는 [`UIKeyboardLayoutGuide`](https://developer.apple.com/documentation/uikit/uikeyboardlayoutguide)에서 확인할 수 있습니다.


| ![An illustration of an iPhone in portrait orientation. A shaded box labeled 'Safe area' appears over the top half of the screen. A shaded box labeled 'Keyboard layout guide' appears over the bottom half of the screen.](https://docs-assets.developer.apple.com/published/c4839fd59dcda19187412f2e7a68ff79/keyboard-layout-guide-keyboard-visible@2x.png) | ![An illustration of an iPhone in portrait orientation. A shaded box labeled 'Safe area' appears over most of the screen. A shaded box labeled 'Keyboard layout guide' appears over the very bottom of the screen.](https://docs-assets.developer.apple.com/published/a6497b7e936917ab450d89501add1cc6/keyboard-layout-guide-keyboard-dismissed@2x.png) |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|    키보드가 표시될 때 레이아웃 가이드는 해당 영역과 위치를 나타냅니다.                                                                                                                                                                                                                                                                                                                                                           |                 키보드가 해제될 때, 키보드 레이아웃 가이드의 상단은 Safe Area 레이아웃 가이드의 하단과 일치합니다.                                                                                                                                                                                                                                                                                                                                        |

## macOS
### - Window의 하단에 컨트롤 또는 중요한 정보를 배치하는 것을 피하세요. 
사람들은 종종 창을 이동하여 하단 가장자리가 화면 하단 아래로 이동하는 경우가 있습니다. 이렇게 하면 컨트롤이나 중요한 정보가 화면의 하단 가장자리 밖으로 벗어나지 않도록 합니다.


## tvOS

텔레비전의 크기는 다양합니다. Apple TV에서 앱 레이아웃은 iPhone이나 iPad에서처럼 화면 크기에 자동으로 적응하지 않습니다. 대신, 앱은 모든 디스플레이에서 동일한 인터페이스를 보여줍니다. 따라서 레이아웃을 설계할 때 다양한 화면 크기에서 훌륭하게 보이도록 특별한 주의를 기울이세요.

### - 화면의 Safe Area를 준수하세요. 
주요 콘텐츠를 화면 위 아래에서 60픽셀, 양쪽에서는 80픽셀 내로 들어가도록 설계하세요. 화면 가장자리에 가까운 콘텐츠는 사람들이 볼 때 어려울 수 있으며, 오래된 텔레비전에서 오버스캐닝으로 인해 의도하지 않은 컨텐츠 잘림이 발생할 수 있습니다. 부분적으로 표시되는 화면 밖 콘텐츠 및 의도적으로 화면 밖으로 흐르는 요소만 이 영역 외부에 나타나도록 허용하세요.

> 오버스캐닝: 텔레비전 화면에서 화면의 가장자리 부분이 잘리는 현상 

![An illustration of a TV with a safe zone border on all sides. In width, the top and bottom borders measure 60 points, and the side borders both measure 80 points.](https://docs-assets.developer.apple.com/published/d70b487ffcb4619669866e367ef3abd4/visual-design-safe-zone@2x.png)

### 포커스 가능한 UI 요소들 사이에 적절한 간격을 포함시키세요. 
UIKit과 포커스 API를 사용할 때 UI 요소는 포커스를 받을 때 크기가 커집니다. UI 요소가가 포커스를 받았을 때 요소들이 어떻게 보이는지 고려하고, 중요한 정보와 의도치 않게 겹치지 않도록 주의하세요.

![An illustration that uses vertical shaded rectangles to show padding between focusable items.](https://docs-assets.developer.apple.com/published/77f8f9af61ff8a2ccedf54808192c41b/visual-design-padding@2x.png)

### 미디어 중심 앱을 만들 때 레이아웃 템플릿을 사용하고 컨텐츠의 모음을 제공하기 위해 그리드를 사용하세요.
만약 미디어 앱의 레이아웃이 최소한의 레이아웃 사용자 정의로 아름답게 콘텐츠를 표시하기만 하면, 사전 설계된 레이아웃 템플릿을 사용하세요. 만약 앱이 컨텐츠의 모음을 보여줘야 한다면, 원격 제어로 쉽게 탐색하고 빠르게 이동할 수 있도록 콘텐츠를 그리드로 표시하세요.


## 레이아웃 템플릿(Layout templates)

### - 애플 TV 템플릿은 깔끔하고 일관된 레이아웃을 제공하여 콘텐츠가 중심에 놓이도록 합니다. 
이러한 템플릿들은 JavaScript와 Apple TV 마크업 언어 (TVML)를 기반으로 하며, 사람들이 앱을 열 때 동적으로 콘텐츠를 로드하고 채웁니다. 이러한 템플릿은 TV 화면에서 멋지게 보이며 스트리밍 미디어에 이상적인 미리 정의된 레이아웃을 가지고 있어서 콘텐츠가 중요한 앱을 만드는 데 유용합니다.

### 템플릿을 선택할 때 그 목적을 고려하세요.
템플릿의 배경, 색상, 크기, 레이아웃 등을 사용자 정의할 수 있지만, 사용자 정의 사항이 템플릿을 불편하게 만들거나 알아보기 어렵게 만든다면 다른 템플릿을 사용하거나 사용자 정의 인터페이스를 디자인하는 것을 고려하세요.

(tvOS 문서 번역 진행 중)

---

## visionOS

  
아래의 지침은 visionOS 앱 또는 게임의 window 내에서 콘텐츠를 배치하는 데 도움이 되며, 사용자에게 익숙하고 사용하기 쉽게 느끼게 할 수 있습니다. 공간에 window을 표시하고 visionOS 앱에서 깊이, 크기 및 시야를 사용하는 데 대한 지침과 최선의 방법에 대한 내용은 [공간 레이아웃(Spatial Layout)](./Spatial-layout.md)을 참조하세요. visionOS window 구성 요소에 대해 더 자세히 알아보려면 [Windows > visionOS](https://developer.apple.com/design/human-interface-guidelines/windows#visionOS)를 참조하세요

> 참고
>   
   표준 window에 깊이를 추가할 때, 콘텐츠는 z-축을 따라 window의 경계를 벗어납니다. 그러나 콘텐츠가 z-축을 따라 너무 멀리 확장되면 시스템이 이를 자르게 됩니다.


### - Window의 콘텐츠를 window의 경계 내에 유지하세요. 
visionOS에서 시스템은 window의 XY 평면을 따라 window의 경계 바로 밖에 window 컨트롤을 표시합니다. 예를 들어, 공유 메뉴는 window 위에 나타나고 window 크기 조정, 이동 및 닫기 컨트롤은 그 아래에 나타납니다. 2D 또는 3D 콘텐츠가 이러한 영역을 침범하게 되면, 특히 Window 아래에 있는 컨트롤을 사용하기 어렵게 만들 수 있습니다.

### - 일반적으로, Window의 모서리에 중요한 콘텐츠와 컨트롤을 배치하는 것을 피하세요. 
콘텐츠가 Window의 중심으로부터 멀어질수록, 특히 window이 큰 경우 사용자가 해당 콘텐츠를 보고 상호 작용하기 어려워질 수 있습니다.

### - Window의 인터렉티브형 구성 요소를 사용자가 쉽게 집중할 수 있도록 만드세요. 
대화형 구성 요소 주변에 충분한 공간을 포함하여 포커스를 쉽고 편안하게 할 수 있도록하고, 시스템에서 제공하는 호버 효과가 다른 콘텐츠를 가리지 않도록하세요. 예를 들어, 버튼을 배치할 때 버튼의 중심이 최소한 60 포인트 떨어져 있도록 하세요. 지침은 [Eyes](https://developer.apple.com/design/human-interface-guidelines/eyes), [Spatial layout](https://developer.apple.com/design/human-interface-guidelines/spatial-layout), [Buttons > visionOS](https://developer.apple.com/design/human-interface-guidelines/buttons#visionOS)을 참조하세요.


### - window 내에 속하지 않는 추가적인 컨트롤을 표시해야 하는 경우, 오너먼트(ornament)를 사용하세요. 
오너먼트를 사용하면 시스템에서 제공하는 컨트롤과 충돌하지 않으면서 window와 시각적으로 연결된 앱 컨트롤을 제공할 수 있습니다. 예를 들어, window의 툴바와 탭 바는 오너먼트로 나타납니다. 지침은 [Ornaments](https://developer.apple.com/design/human-interface-guidelines/ornaments)를 참조하세요.

## watchOS

### - 화면의 한 가장자리부터 다른 가장자리까지 콘텐츠를 확장하도록 디자인하세요. 
Apple Watch 베젤은 콘텐츠 주위에 자연스러운 시각적 패딩을 제공합니다. 소요되는 공간을 최소화하려면 요소 사이의 패딩을 최소화하는 것을 고려하세요.

![An illustration of the Workout app’s main list of workouts on Apple Watch. A callout indicates that the currently focused workout item spans the full width of the available screen area.](https://docs-assets.developer.apple.com/published/180d82ec20b9f85908474cc931d4707e/layout-full-width@2x.png)


### - UI 인터페이스에는 두 개 이상 또는 세 개 이상의 컨트롤을 나란히 배치하지 않도록 하세요. 
일반적으로, 한 행에는 글리프를 포함하는 버튼을 최대 세 개나 텍스트를 포함하는 버튼을 최대 두 개까지만 표시하는 것이 좋습니다. 텍스트 버튼이 화면 전체 너비에 걸쳐 있는 것이 일반적으로 더 나은 방법이지만, 짧은 텍스트 레이블을 가진 두 개의 옆에 나란히 있는 버튼도 화면이 스크롤되지 않는 한 잘 작동할 수 있습니다.


![A diagram of an Apple Watch screen showing two side-by-side buttons beneath three lines of text.](https://docs-assets.developer.apple.com/published/aa5904c73a0b5295604bb551c164325c/layout-controls@2x.png)


### - 사람들이 다른 사람에게 보여주려고 할 수 있는 뷰에서 자동 회전을 지원하세요. 
손목을 뒤로 젖힐 때 앱은 일반적으로 디스플레이를 슬립 상태로 전환하게 되지만, 어떤 경우에는 콘텐츠를 자동으로 회전하는 것이 합리적일 수 있습니다. 예를 들어, 착용자가 친구에게 이미지를 보여주거나 QR 코드를 리더에게 표시하려고 할 수 있습니다. 개발자 가이드는 [`isAutorotating`](https://developer.apple.com/documentation/watchkit/wkextension/2868464-isautorotating)을 참조하세요.


## 제품 스펙

### iOS, iPadOS

|Device|Dimensions (portrait)|
|---|---|
|12.9” iPad Pro|1024x1366 pt (2048x2732 px @2x)|
|11” iPad Pro|834x1194 pt (1668x2388 px @2x)|
|10.5” iPad Pro|834x1194 pt (1668x2388 px @2x)|
|9.7” iPad Pro|768x1024 pt (1536x2048 px @2x)|
|7.9” iPad mini|768x1024 pt (1536x2048 px @2x)|
|10.5” iPad Air|834x1112 pt (1668x2224 px @2x)|
|9.7” iPad Air|768x1024 pt (1536x2048 px @2x)|
|10.2” iPad|810x1080 pt (1620x2160 px @2x)|
|9.7” iPad|768x1024 pt (1536x2048 px @2x)|
|iPhone 15 Pro Max|430x932 pt (1290x2796 px @3x)|
|iPhone 15 Pro|393x852 pt (1179x2556 px @3x)|
|iPhone 15 Plus|430x932 pt (1290x2796 px @3x)|
|iPhone 15|393x852 pt (1179x2556 px @3x)|
|iPhone 14 Pro Max|430x932 pt (1290x2796 px @3x)|
|iPhone 14 Pro|393x852 pt (1179x2556 px @3x)|
|iPhone 14 Plus|428x926 pt (1284x2778 px @3x)|
|iPhone 14|390x844 pt (1170x2532 px @3x)|
|iPhone 13 Pro Max|428x926 pt (1284x2778 px @3x)|
|iPhone 13 Pro|390x844 pt (1170x2532 px @3x)|
|iPhone 13|390x844 pt (1170x2532 px @3x)|
|iPhone 13 mini|375x812 pt (1125x2436 px @3x)|
|iPhone 12 Pro Max|428x926 pt (1284x2778 px @3x)|
|iPhone 12 Pro|390x844 pt (1170x2532 px @3x)|
|iPhone 12|390x844 pt (1170x2532 px @3x)|
|iPhone 12 mini|375x812 pt (1125x2436 px @3x)|
|iPhone 11 Pro Max|414x896 pt (1242x2688 px @3x)|
|iPhone 11 Pro|375x812 pt (1125x2436 px @3x)|
|iPhone 11|414x896 pt (828x1792 px @2x)|
|iPhone XS Max|414x896 pt (1242x2688 px @3x)|
|iPhone XS|375x812 pt (1125x2436 px @3x)|
|iPhone XR|414x896 pt (828x1792 px @2x)|
|iPhone X|375x812 pt (1125x2436 px @3x)|
|iPhone 8 Plus|414x736 pt (1080x1920 px @3x)|
|iPhone 8|375x667 pt (750x1334 px @2x)|
|iPhone 7 Plus|414x736 pt (1080x1920 px @3x)|
|iPhone 7|375x667 pt (750x1334 px @2x)|
|iPhone 6s Plus|414x736 pt (1080x1920 px @3x)|
|iPhone 6s|375x667 pt (750x1334 px @2x)|
|iPhone 6 Plus|414x736 pt (1080x1920 px @3x)|
|iPhone 6|375x667 pt (750x1334 px @2x)|
|4.7” iPhone SE|375x667 pt (750x1334 px @2x)|
|4” iPhone SE|320x568 pt (640x1136 px @2x)|
|iPod touch 5th generation and later|320x568 pt (640x1136 px @2x)|

> 참고
> 위의 표에 나와 있는 모든 스케일 배율(scale factor)는 UIKit 기준 배율이며, 기본 스케일 팩터와 다를 수 있습니다. 개발자 지침은 [`scale`](https://developer.apple.com/documentation/uikit/uiscreen/1617836-scale) 및 [`nativeScale`](https://developer.apple.com/documentation/uikit/uiscreen/1617825-nativescale)을 참조하세요.

## Device size classes
각각 다른 디바이스에서는 화면 크기를 기준으로 전체 화면에 대한 다른 size 클래스 들이 적용됩니다.
![An illustration of an iPad and an iPhone in both portrait and landscape orientations. Each device in each orientation includes a red screen and arrowed lines that indicate the full height and width of the screen.](https://docs-assets.developer.apple.com/published/ea27d20bc28241ad815bbca4b92b9b71/layout-size-classes@2x.png)



|Device|Portrait orientation|Landscape orientation|
|---|---|---|
|12.9” iPad Pro|Regular width, regular height|Regular width, regular height|
|11” iPad Pro|Regular width, regular height|Regular width, regular height|
|10.5” iPad Pro|Regular width, regular height|Regular width, regular height|
|9.7” iPad|Regular width, regular height|Regular width, regular height|
|7.9” iPad mini|Regular width, regular height|Regular width, regular height|
|iPhone 15 Pro Max|Compact width, regular height|Regular width, compact height|
|iPhone 15 Pro|Compact width, regular height|Compact width, compact height|
|iPhone 15 Plus|Compact width, regular height|Regular width, compact height|
|iPhone 15|Compact width, regular height|Compact width, compact height|
|iPhone 14 Pro Max|Compact width, regular height|Regular width, compact height|
|iPhone 14 Pro|Compact width, regular height|Compact width, compact height|
|iPhone 14 Plus|Compact width, regular height|Regular width, compact height|
|iPhone 14|Compact width, regular height|Compact width, compact height|
|iPhone 13 Pro Max|Compact width, regular height|Regular width, compact height|
|iPhone 13 Pro|Compact width, regular height|Compact width, compact height|
|iPhone 13|Compact width, regular height|Compact width, compact height|
|iPhone 13 mini|Compact width, regular height|Compact width, compact height|
|iPhone 12 Pro Max|Compact width, regular height|Regular width, compact height|
|iPhone 12 Pro|Compact width, regular height|Compact width, compact height|
|iPhone 12|Compact width, regular height|Compact width, compact height|
|iPhone 12 mini|Compact width, regular height|Compact width, compact height|
|iPhone 11 Pro Max|Compact width, regular height|Regular width, compact height|
|iPhone 11 Pro|Compact width, regular height|Compact width, compact height|
|iPhone 11|Compact width, regular height|Regular width, compact height|
|iPhone XS Max|Compact width, regular height|Regular width, compact height|
|iPhone XS|Compact width, regular height|Compact width, compact height|
|iPhone XR|Compact width, regular height|Regular width, compact height|
|iPhone X|Compact width, regular height|Compact width, compact height|
|iPhone 8 Plus|Compact width, regular height|Regular width, compact height|
|iPhone 8|Compact width, regular height|Compact width, compact height|
|iPhone 7 Plus|Compact width, regular height|Regular width, compact height|
|iPhone 7|Compact width, regular height|Compact width, compact height|
|iPhone 6s Plus|Compact width, regular height|Regular width, compact height|
|iPhone 6s|Compact width, regular height|Compact width, compact height|
|iPhone SE|Compact width, regular height|Compact width, compact height|
|iPod touch 5th generation and later|Compact width, regular height|Compact width, compact height|

아이패드에서는 app 혹은 게임을 실행할 때, [multitasking](https://developer.apple.com/design/human-interface-guidelines/multitasking) 상태에서도 size class가 적용이 됩니다.


![](https://i.imgur.com/GYJzSld.png)


| 2/3 split view                                                                                                                                                                                                  | 1/2 split view                                                                                                                                                                                      | 1/3 split view                                                                                                                                                                                             |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ![An illustration of iPad in landscape orientation with the left two-thirds of its screen shaded.](https://docs-assets.developer.apple.com/published/e2c436a11b4dd3636828c6c3844465b2/layout-two-thirds@2x.png) | ![An illustration of iPad in landscape orientation with the left half of its screen shaded.](https://docs-assets.developer.apple.com/published/976669fb0a060433ac179c23d4728186/layout-half@2x.png) | ![An illustration of iPad in landscape orientation with the left one-third of its screen shaded.](https://docs-assets.developer.apple.com/published/f25f319072f994822c92d9ffa63bf9c8/layout-thirds@2x.png) |

|Device|Mode|Portrait orientation|Landscape orientation|
|---|---|---|---|
|12.9” iPad Pro|2/3 split view|Compact width, regular height|Regular width, regular height|
||1/2 split view|N/A|Regular width, regular height|
||1/3 split view|Compact width, regular height|Compact width, regular height|
|11” iPad Pro|2/3 split view|Compact width, regular height|Regular width, regular height|
||1/2 split view|N/A|Compact width, regular height|
||1/3 split view|Compact width, regular height|Compact width, regular height|
|10.5” iPad Pro|2/3 split view|Compact width, regular height|Regular width, regular height|
||1/2 split view|N/A|Compact width, regular height|
||1/3 split view|Compact width, regular height|Compact width, regular height|
|9.7” iPad|2/3 split view|Compact width, regular height|Regular width, regular height|
||1/2 split view|N/A|Compact width, regular height|
||1/3 split view|Compact width, regular height|Compact width, regular height|
|7.9” iPad mini 4|2/3 split view|Compact width, regular height|Regular width, regular height|
||1/2 split view|N/A|Compact width, regular height|
||1/3 split view|Compact width, regular height|Compact width, regular height|

### watchOS

|Series|Screen size|Width (pixels)|Height (pixels)|
|---|---|---|---|
|Apple Watch Ultra (1st and 2nd generation)|49mm|410|502|
|7 and later|41mm|352|430|
|7 and later|45mm|396|484|
|4, 5, 6, and SE|40mm|324|394|
|4, 5, 6, and SE|44mm|368|448|
|1, 2, and 3|38mm|272|340|
|1, 2, and 3|42mm|312|390|

---

## 관련 문서
- [Right to left](https://developer.apple.com/design/human-interface-guidelines/right-to-left)

### 개발자 문서

- [`UITraitCollection`](https://developer.apple.com/documentation/uikit/uitraitcollection)
- [`UITraitEnvironment`](https://developer.apple.com/documentation/uikit/uitraitenvironment)
- [Responding to changing display modes on Apple TV](https://developer.apple.com/documentation/uikit/app_and_environment/responding_to_changing_display_modes_on_apple_tv)


### 영상

| [What's New in iOS Design](https://developer.apple.com/videos/play/wwdc2019/808)                                           | [Essential Design Principles](https://developer.apple.com/videos/play/wwdc2017/802)                                       |
| -------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- | 
| ![](https://devimages-cdn.apple.com/wwdc-services/images/48/0F960683-D91F-4CA9-9658-6FBB11F0683D/3272_wide_250x141_1x.jpg) | ![](https://devimages-cdn.apple.com/wwdc-services/images/7/2546ECBD-6443-41EC-921D-6429026F8B67/1700_wide_250x141_1x.jpg) |


