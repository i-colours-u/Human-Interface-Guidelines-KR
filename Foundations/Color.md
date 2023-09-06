# Color
## 색상을 신중하게 사용하면 커뮤니케이션을 강화하고, 브랜드를 연상시키며, 시각적 연속성을 제공하고, 상태와 피드백을 전달하고, 사람들이 정보를 이해하는 데 도움이 될 수 있습니다.

![A sketch of a paint palette, suggesting the use of color. The image is overlaid with rectangular and circular grid lines and is tinted yellow to subtly reflect the yellow in the original six-color Apple logo.](https://docs-assets.developer.apple.com/published/10ec5551985c77cabaeaaaff016cdfd8/foundations-color-intro@2x.png)

시스템은 다양한 배경과 모드(라이트/다크)에 잘 어울리는 색상을 정의하고, vibrancy(블러와 같은 시각적 효과) 및 접근성 설정에 맞게 조정됩니다. 사람들은 시스템 색상에 익숙하며, 이를 사용하는 것은 디바이스에서 경험이 익숙하고,편안하게 만드는 편리한 방법입니다.


또한 사용자 지정 색상을 사용하여 앱이나 게임의 시각적 경험을 향상시키고 고유한 개성을 표현할 수도 있습니다. 다음 가이드라인은 시스템 정의 색상을 사용하든 사용자 지정 색상을 사용하든 관계없이 사람들이 좋아하는 방식으로 색상을 사용하는 데 도움이 될 수 있습니다.


여러분도 앱이나 게임의 시각적 경험을 강화하고 그것의 독특한 개성을 표현하기 위해 커스텀(시스템이 아닌 직접 고른) 색상을 사용하고 싶을 수 있습니다.
아래 가이드라인은 여러분이 시스템 정의 컬러/커스텀 컬러등 어떤 컬러를 사용하든 간에, 사용자들이 만족 할 수 있는 지침을 안내할 것입니다.

## Best practices

### - 게임이 아닌 앱에서는 색상을 절제하여 사용하세요. 
게임이 아닌 앱에서 색상의 과도한 사용은 소통을 덜 명확하게 만들고 사용자의 주의를 산만하게 할 수 있습니다. 중요한 정보에 주목을 받게 하거나 UI간의 관계를 보여주기 위해 적은 수의 색상을 사용하는 것을 권장합니다.

### - 같은 색상을 다른 의미로 사용하는 것을 피하세요. 
인터페이스 전반에 걸쳐 색상을 일관되게 사용하세요, 특히 상태나 상호작용과 같은 정보를 전달하는 데 도움을 줄 때 그렇게 합니다. 예를 들어, 앱은 텍스트를 탭하여 더 많은 내용을 볼 수 있다는 것을 나타내기 위해 파란색을 사용할 수 있습니다(하이퍼링크처럼).  앱에서 색상과 관련없는 시각적 기호 — 예를 들면 화살표 아이콘 —를 사용하여 상호작용성을 알릴 때에도, 상호작용 텍스트에 파란색 이외의 다른 색상을 사용하는 것은 사용자에게 혼란스러움을 야기할 수 있습니다.

### - 여러분의 앱 색상이 라이트 모드와 다크 모드 모두에서 잘 작동하는지 확인하세요.
대부분의 플랫폼은 기본 라이트 모드 대신 사용 할 수 있는 [Dark Mode(다크 모드)](https://developer.apple.com/design/human-interface-guidelines/dark-mode)를 제공합니다.
다크 모드는 모든 화면, 뷰, 메뉴, 그리고 컨트롤에 대해 더 어두운 색상 팔레트를 사용하며, 밝은 UI들이 다크 모드의 배경에 더 잘 돋보이게 하기 위해 `vibrancy` — (전경과 배경 색상을 동적으로 혼합하는 미묘한 효과, 블러) — 를 증가시킬 수 있습니다(자세한 정보는 [Materials](https://developer.apple.com/design/human-interface-guidelines/materials)를 참조하세요). visionOS나 watchOS에는 다크 모드가 없습니다. visionOS는 주변 물체와 색상의 빛반사에 자동으로 적응하는 'glass'라는 특수한 환경을 사용합니다. watchOS에서는 앱이 일반적으로 다크 모드 배경을 사용하지만, 뷰의 내용을 잘 보이게 하기 위해 전체 배경 색상 그라디언트 효과나 그래픽을 사용할 수도 있습니다. 모든 플랫폼은 시스템 색상은 필요에 따라 라이트 모드와 다크 모드를 자동으로 지원합니다. 만약 사용자 정의 색상을 사용한다면 두 가지 버전 모두를 제공해야 합니다.

### - 앱의 색상 구성을 다양한 조명 조건에서 테스트하세요. 
예를 들어, 햇빛 아래에서나 어두운 빛에서 앱을 실행할 때 색상이 다르게 보일 수 있습니다. visionOS에서는 사람의 물리적 환경에 있는 벽이나 물체의 색상 및 어떻게 빛을 반사하는지에 따라 색상이 다르게 보일 수 있습니다. 
대부분의 사용 환경에서 최적의 시청 경험을 제공하도록 앱 색상을 조절하세요.

### - 다양한 장치에서 앱을 테스트하세요.
예를 들어, True Tone 디스플레이(특정 iPhone, iPad, Mac 모델에서 사용 가능)는 주변 조명 센서를 사용하여 디스플레이의 화이트 포인트를 현재 환경의 조명 조건에 맞게 자동으로 조절합니다. 주로 읽기, 사진, 비디오, 게임에 중점을 둔 앱은 `White Point Adaptivity Style`([`UIWhitePointAdaptivityStyle`](https://developer.apple.com/documentation/bundleresources/information_property_list/uiwhitepointadaptivitystyle) 를 참조하세요.)을 지정하여 이 효과를 강화하거나 약화시킬 수 있습니다. 다양한 브랜드의 HD 및 4K TV에서 tvOS 앱을 테스트하고, 다른 디스플레이 설정으로도 테스트하세요. Mac에서 시스템 설정 > 디스플레이에서 프로필을 선택하여 — 예를 들면 P3와 표준 RGB (sRGB) — 앱의 모양을 테스트할 수도 있습니다. 가이드를 원하면 [Color management(색상 관리)](https://developer.apple.com/design/human-interface-guidelines/color#Color-management)를 참조하세요.

### - 아트워크와 반투명이 주변 색상에 어떻게 영향을 주는지 고려하세요. 
아트워크의 색상 차이는 때로 인터페이스의 일관성을 유지하기 위해 주변 색상을 조절해야 할 필요가 생길 수 있습니다. 예로 들면, '지도' 앱은 지도 모드일 때는 밝은 색상 구성을 사용하지만, 위성 모드로 변경될 때 어두운 색상 구성으로 바뀝니다. 또한, 색상은 툴바와 같은 반투명한 요소 뒤나 그 요소에 적용될 때 다르게 보일 수 있습니다.

### - 사용자가 직접 색상을 고르는 기능이 있을 경우, 시스템에서 제공하는 색상 컨트롤(system color controls)을 사용해보세요.
내장된 컬러 피커를 사용하면 일관된 사용자 경험을 제공할 뿐만 아니라 사용자가 어떤 앱에서든 접근할 수 있는 색상 세트를 저장하게 할 수 있습니다. 개발자 지침은 [`ColorPicker`](https://developer.apple.com/documentation/SwiftUI/ColorPicker)를 참조하세요.


## 포괄적인 색상 사용 (Inclusive color)
색상만으로 물체를 구별하거나 상호 작용을 나타내거나 필수적인 정보를 전달하는 데 너무 의존하지 말아야 합니다. 정보를 전달하기 위해 색상을 사용할 때 색맹 또는 시각 장애를 가진 사람들도 이해할 수 있도록 대체 수단으로 동일한 정보를 제공해야 합니다. 예를 들어, 물체나 상태를 식별하기 위해 라벨 또는 글리프 모양을 사용할 수 있습니다.

앱에서 내용을 인식하기 어렵게 만드는 색상을 사용하지 않도록 주의해야 합니다. 충분한 대비가 부족하면 아이콘과 텍스트가 배경과 어울려 내용을 읽기 어렵게 만들 수 있으며, 색맹인 사람들은 일부 색상 조합을 구분하기 어려울 수 있습니다. 지침을 참조하려면 [Color and effects](https://developer.apple.com/design/human-interface-guidelines/accessibility#Color-and-effects)를 참고하세요.

사용하는 색상이 다른 국가와 문화에서 어떻게 인식될 수 있는지 고려해야 합니다. 예를 들어, 일부 문화에서 빨간색은 위험을 나타내지만 다른 문화에서는 긍정적인 의미를 가질 수 있습니다. 앱의 색상이 의도한 메시지를 전달하도록 해야 합니다.

## 시스템 색상
### - 앱에서 시스템 색상 값을 하드 코딩하는 것을 피하세요. 
문서화된 색상 값은 앱 디자인 프로세스 중 참고용입니다. 실제 색상 값은 환경 변수의 다양한 요소에 따라 릴리스 간에 변동할 수 있습니다. 시스템 색상을 적용하기 위해 [`Color`](https://developer.apple.com/documentation/SwiftUI/Color)와 같은 API를 사용하세요.

iOS, iPadOS, macOS 및 visionOS는 또한 표준 UI 구성 요소의 색상 계획과 자동으로 밝은 및 어두운 환경 모두에 적응하는 동적 시스템 색상 집합을 정의합니다. 각 동적 색상은 모양이나 색상 값이 아니라 그 목적에 따라 정의됩니다. 예를 들어, 일부 색상은 계층 구조의 다른 수준에서 뷰 배경을 나타내며 다른 색상은 레이블, 링크 및 구분선과 같은 콘텐츠를 나타내는데 사용합니다.

### - 동적 시스템 색상을 복제하는 것을 피하세요. 
동적 시스템 색상 중 일부는 패턴일 수 있으며, 환경 변수의 다양한 요소에 따라 색상이 변경 될 수 있습니다.

### - 동적 시스템 색상의 의미를 재정의하는 것을 피하세요. 
일관된 경험을 보장하고 플랫폼의 외관이 변경될 때 인터페이스가 훌륭하게 보이도록 하려면 동적 시스템 색상을 의도대로 사용하세요.

## Color management
  
색상 공간(Color Space)은 RGB 또는 CMYK와 같은 색상 모델에서 색상을 표현하는 것입니다. 일반적인 색상 공간(때로는 "색영역"이라고도 함)으로는 sRGB와 Display P3가 있습니다.

![Diagram showing the colors included in the sRGB space, compared to the larger number of colors included in the P3 color space.](https://docs-assets.developer.apple.com/published/080494c70f63b88c8646f75aad962673/color-graphic-wide-color@2x.png)



색상 프로필(Color Profile)은 색상 공간 내의 색상을, 예를 들어 수학적인 공식이나 데이터 테이블을 사용하여 숫자 표현에 매핑하는 방식으로 설명합니다. 이미지는 자체 색상 프로필을 포함하여 장치가 이미지의 색상을 올바르게 해석하고 디스플레이에서 정확하게 재현할 수 있도록 합니다.

### - 이미지에 색상 프로필(color profile)을 적용하세요. 
색상 프로필을 사용하면 앱의 색상이 다른 디스플레이에서 의도한 대로 나타날 수 있도록 도와줍니다. sRGB 색상 공간은 대부분의 디스플레이에서 정확한 색상을 생성합니다.

### - 호환 가능한 디스플레이에서 시각적 경험을 향상시키기 위해 와이드 색상(Wide Color)을 사용하세요. 
와이드 색상 디스플레이는 P3 색상 공간을 지원하며 sRGB보다 더 풍부하고 채도 높은 색상을 생성할 수 있습니다. 따라서 와이드 색상을 사용하는 사진과 비디오는 더 생동감 있고, 와이드 색상을 사용하는 시각 데이터와 상태 표시기는 더 의미 있을 수 있습니다. 적절한 경우, 16 비트(채널당)의 Display P3 색상 프로필을 사용하고 이미지를 PNG 형식으로 내보냅니다. 와이드 색상 이미지를 디자인하고 P3 색상을 선택하려면 와이드 색상 디스플레이를 사용해야 함에 유의하세요.

### - 필요한 경우 색상 공간별 이미지와 색상 변형을 제공하세요.
일반적으로 P3 색상과 이미지는 sRGB 디스플레이에서도 잘 나타납니다. 때로는 sRGB 디스플레이에서 매우 비슷한 두 가지 P3 색상을 구별하기 어려울 수 있습니다. P3 색상을 사용하는 그라데이션은 sRGB 디스플레이에서 종종 자르게 보일 수도 있습니다. 이러한 문제를 피하고 와이드 색상과 sRGB 디스플레이에서 의도된 대로 정확하게 보여지기 하기 위해 Xcode의 에셋 카탈로그를 사용하여 각 색상 공간에 대한 이미지와 색상의 다른 버전을 제공할 수 있습니다.

자세한 내용을 확인하려면, [How to start designing assets in Display P3](https://developer.apple.com/news/?id=5cda5ipr) 문서를 참조하세요.

## 플랫폼 고려사항

## iOS, iPadOS

iOS는 2가지의 동적 배경 색상 집합을 정의합니다. (system/grouped)
각각의 집합은 정보를 목적에 맞게 전달하기 위해, 주요(primary), 보조(secondary), 그리고 제 3의(tertiary) 등의 계층을 가지고 있습니다.

일반적으로 그룹화된 테이블 뷰가 있는 경우 그룹화된 배경 색상([`systemGroupedBackground`](https://developer.apple.com/documentation/uikit/uicolor/3173145-systemgroupedbackground), [`secondarySystemGroupedBackground`](https://developer.apple.com/documentation/uikit/uicolor/3173138-secondarysystemgroupedbackground), [`tertiarySystemGroupedBackground`](https://developer.apple.com/documentation/uikit/uicolor/3173155-tertiarysystemgroupedbackground))을 사용하고, 그 외의 경우에는 시스템 배경 색상([`systemBackground`](https://developer.apple.com/documentation/uikit/uicolor/3173140-systembackground), [`secondarySystemBackground`](https://developer.apple.com/documentation/uikit/uicolor/3173137-secondarysystembackground), [`tertiarySystemBackground`](https://developer.apple.com/documentation/uikit/uicolor/3173154-tertiarysystembackground))을 사용합니다.

두 개의 배경 색상 집합을 모두 사용할 때, 계층을 다음과 같은 기준으로 분류합니다.

- 주요(primary): 전체 뷰에 대한 것
- 보조(secondary): 전체 뷰 내에서 콘텐츠 또는 요소를 그룹화하기 위한 것
- 제 3의(tertiary): 보조 요소 내에서 콘텐츠 또는 요소를 그룹화하기 위한 것

UI 콘텐츠의 경우, iOS는 다음과 같은 동적 색상을 정의합니다.

|색상|사용되는 곳|UIKit API|
|---|---|---|
|Label|주요 컨텐츠를 포함하는 텍스트 라벨|[`label`](https://developer.apple.com/documentation/uikit/uicolor/3173131-label)|
|Secondary label|보조적인 컨텐츠를 포함하는 텍스트 라벨|[`secondaryLabel`](https://developer.apple.com/documentation/uikit/uicolor/3173136-secondarylabel)|
|Tertiary label|그 이외의, 제 3의(tertiary) 컨텐츠를 포함하는 텍스트 라벨|[`tertiaryLabel`](https://developer.apple.com/documentation/uikit/uicolor/3173153-tertiarylabel)|
|Quaternary label|제 4의, 사소한 컨텐츠를 포함하는 텍스트 라벨|[`quaternaryLabel`](https://developer.apple.com/documentation/uikit/uicolor/3173135-quaternarylabel)|
|Placeholder text|텍스트 뷰에 사용되는 플레이스 홀더 텍스트|[`placeholderText`](https://developer.apple.com/documentation/uikit/uicolor/3173134-placeholdertext)|
|Separator|구분선을 표현하는 뷰|[`separator`](https://developer.apple.com/documentation/uikit/uicolor/3173139-separator)|
|Opaque separator|불투명한 구분선을 표현하는 뷰|[`opaqueSeparator`](https://developer.apple.com/documentation/uikit/uicolor/3173133-opaqueseparator)|
|Link|링크로 작동하는 텍스트|[`link`](https://developer.apple.com/documentation/uikit/uicolor/3173132-link)|


## macOS
macOS는 다음과 같은 동적 시스템 색상을 정의합니다 (이 색상들은 개발자 문서의 palette 문서에서도 확인이 가능합니다.)

| 색상 | 사용되는 곳 | AppKit API |
|-----------------------------|--------------------------------------------------------------------|----------------------------------|
| Alternate selected control text color | 선택된 목록 또는 테이블의 선택된 표면의 텍스트 | [`alternateSelectedControlTextColor`](https://developer.apple.com/documentation/appkit/nscolor/1527413-alternateselectedcontroltextcolo) |
| Alternating content background colors | 목록, 테이블 또는 컬렉션 뷰의 번갈아가는 행 또는 열의 배경 | [`alternatingContentBackgroundColors`](https://developer.apple.com/documentation/appkit/nscolor/2998825-alternatingcontentbackgroundcolo) |
| Control accent | 사용자가 시스템 설정에서 선택하는 강조 색상 | [`controlAccentColor`](https://developer.apple.com/documentation/appkit/nscolor/3000782-controlaccentcolor) |
| Control background color | 브라우저나 테이블과 같은 큰 인터페이스 요소의 배경 | [`controlBackgroundColor`](https://developer.apple.com/documentation/appkit/nscolor/1531948-controlbackgroundcolor) |
| Control color | 컨트롤의 표면 | [`controlColor`](https://developer.apple.com/documentation/appkit/nscolor/1524856-controlcolor) |
| Control text color | 사용 가능한 컨트롤의 텍스트 | [`controlTextColor`](https://developer.apple.com/documentation/appkit/nscolor/1535230-controltextcolor) |
| Current control tint | 시스템에서 정의한 컨트롤 틴트 | [`currentControlTint`](https://developer.apple.com/documentation/appkit/nscolor/1526377-currentcontroltint) |
| Unavailable control text color | 사용할 수 없는 컨트롤의 텍스트 | [`disabledControlTextColor`](https://developer.apple.com/documentation/appkit/nscolor/1530573-disabledcontroltextcolor) |
| Find highlight color | 검색 인디케이터의 색상 | [`findHighlightColor`](https://developer.apple.com/documentation/appkit/nscolor/2998827-findhighlightcolor) |
| Grid color | 테이블과 같은 인터페이스 요소의 그리드 라인 | [`gridColor`](https://developer.apple.com/documentation/appkit/nscolor/1527240-gridcolor) |
| Header text color | 테이블의 헤더 셀의 텍스트 | [`headerTextColor`](https://developer.apple.com/documentation/appkit/nscolor/1531237-headertextcolor) |
| Highlight color | 화면상의 가상 빛의 소스 | [`highlightColor`](https://developer.apple.com/documentation/appkit/nscolor/1527697-highlightcolor) |
| Keyboard focus indicator color | 키보드를 사용하여 인터페이스를 탐색할 때 현재 포커스된 컨트롤 주변에 나타나는 링 | [`keyboardFocusIndicatorColor`](https://developer.apple.com/documentation/appkit/nscolor/1532031-keyboardfocusindicatorcolor) |
| Label color | 주요 콘텐츠를 포함하는 레이블의 텍스트 | [`labelColor`](https://developer.apple.com/documentation/appkit/nscolor/1534657-labelcolor) |
| Link color | 다른 콘텐츠로 이어지는 링크 | [`linkColor`](https://developer.apple.com/documentation/appkit/nscolor/2998828-linkcolor) |
| Placeholder text color | 컨트롤이나 텍스트 뷰에서의 플레이스홀더 문자열 | [`placeholderTextColor`](https://developer.apple.com/documentation/appkit/nscolor/2998829-placeholdertextcolor) |
| Quaternary label color | 제 4급 레이블의 텍스트, 제 3급 레이블보다 중요도가 낮은 경우도 있으며, 워터마크 텍스트와 같은 경우도 있습니다 | [`quaternaryLabelColor`](https://developer.apple.com/documentation/appkit/nscolor/1534635-quaternarylabelcolor) |
| Scrubber textured background color | Touch Bar에서 스크러버의 배경, Touch Bar에 대한 안내는 [Touch Bar](https://developer.apple.com/design/human-interface-guidelines/touch-bar)를 참조하세요 | [`scrubberTexturedBackgroundColor`](https://developer.apple.com/documentation/appkit/nscolor/2646931-scrubbertexturedbackgroundcolor) |
| Secondary label color | 주요 레이블보다 중요도가 낮은 레이블의 텍스트, 부제목이나 추가 정보를 나타내는 레이블로 사용됩니다 | [`secondaryLabelColor`](https://developer.apple.com/documentation/appkit/nscolor/1533254-secondarylabelcolor) |
| Selected content background color | 주요 창이나 뷰에서 선택된 콘텐츠의 배경 | [`selectedContentBackgroundColor`](https://developer.apple.com/documentation/appkit/nscolor/2998830-selectedcontentbackgroundcolor) |
| Selected control color | 선택된 컨트롤의 표면 | [`selectedControlColor`](https://developer.apple.com/documentation/appkit/nscolor/1526796-selectedcontrolcolor) |
| Selected control text color | 선택된 컨트롤의 텍스트 | [`selectedControlTextColor`](https://developer.apple.com/documentation/appkit/nscolor/1535591-selectedcontroltextcolor) |
| Selected menu item text color | 선택된 메뉴의 텍스트 | [`selectedMenuItemTextColor`](https://developer.apple.com/documentation/appkit/nscolor/1526658-selectedmenuitemtextcolor) |
| Selected text background color | 선택된 텍스트의 배경 | [`selectedTextBackgroundColor`](https://developer.apple.com/documentation/appkit/nscolor/1528136-selectedtextbackgroundcolor) |
| Selected text color | 선택된 텍스트의 색상 | [`selectedTextColor`](https://developer.apple.com/documentation/appkit/nscolor/1528605-selectedtextcolor) |
| Separator color | 콘텐츠의 다른 섹션을 구분하는 구분선 | [`separatorColor`](https://developer.apple.com/documentation/appkit/nscolor/2998831-separatorcolor) |
| Shadow color | 화면상에 높이 올라간 객체가 만드는 가상 그림자 | [`shadowColor`](https://developer.apple.com/documentation/appkit/nscolor/1525121-shadowcolor) |
| Tertiary label color | 주요 레이블보다 중요도가 낮은 제 3급 레이블의 텍스트 | [`tertiaryLabelColor`](https://developer.apple.com/documentation/appkit/nscolor/1532376-tertiarylabelcolor) |
| Text background color | 텍스트 뒤의 배경 색상 | [`textBackgroundColor`](https://developer.apple.com/documentation/appkit/nscolor/1535446-textbackgroundcolor) |
| Text color | 문서 내의 텍스트 | [`textColor`](https://developer.apple.com/documentation/appkit/nscolor/1527025-textcolor) |
| Under page background color | 문서 콘텐츠 뒤의 배경 | [`underPageBackgroundColor`](https://developer.apple.com/documentation/appkit/nscolor/1534707-underpagebackgroundcolor) |
| Unemphasized selected content background color | 주요 창이나 뷰가 아닌 창이나 뷰에서 선택된 콘텐츠의 배경 | [`unemphasizedSelectedContentBackgroundColor`](https://developer.apple.com/documentation/appkit/nscolor/2998832-unemphasizedselectedcontentbackg) |
| Unemphasized selected text background color | 주요 창이나 뷰가 아닌 창이나 뷰에서 선택된 텍스트의 배경 | [`unemphasizedSelectedTextBackgroundColor`](https://developer.apple.com/documentation/appkit/nscolor/2998833-unemphasizedselectedtextbackgrou) |
| Unemphasized selected text color | 주요 창이나 뷰가 아닌 창이나 뷰에서 선택된 텍스트 | [`unemphasizedSelectedTextColor`](https://developer.apple.com/documentation/appkit/nscolor/2998834-unemphasizedselectedtextcolor) |
| Window background color | 창의 배경 | [`windowBackgroundColor`](https://developer.apple.com/documentation/appkit/nscolor/1528630-windowbackgroundcolor) |
| Window frame text color | 창의 제목 표시줄 영역에 있는 텍스트 | [`windowFrameTextColor`](https://developer.apple.com/documentation/appkit/nscolor/1524257-windowframetextcolor) |


### App accent colors (강조 색상)

macOS 11부터 앱의 버튼, 선택 강조 및 사이드바 아이콘의 외관을 사용자 정의하는 앱 강조 색상을 지정할 수 있습니다. 시스템은 현재 값이 일반 > 강조 색상 설정에서 설정값이 `multicolor`인 경우 앱 강조 색상을 적용합니다.

|     |     |
| --- | --- |
|  ![A screenshot of a window that includes a sidebar. Each item in the sidebar displays an icon at its leading edge. Each icon uses the purple accent color.](https://docs-assets.developer.apple.com/published/4d928abfd24f75ed7f73186da65acff4/app-accent-colors-podcasts@2x.png)   |   ![A screenshot of a window that includes a toolbar. The purple accent color is visible in the currently selected toolbar icon and in the content area's pop-up buttons.](https://docs-assets.developer.apple.com/published/afba54f2945b14a235f5e49125339be2/app-accent-colors-podcasts-preferences@2x.png)

  
만약 사용자가 `multicolor` 이외의 값으로 강조 설정을 변경한다면, 시스템은 해당 항목에 사용자가 선택한 색상을 적용하여 앱 전체에 걸쳐 강조 색상을 대체합니다. 예외는 지정한 고정 색상을 사용하는 사이드바 아이콘입니다. 고정 색상 사이드바 아이콘은 의미를 제공하기 위해 특정 색상을 사용하므로, 사용자가 강조 색상 설정의 값을 변경해도 시스템은 해당 아이콘의 색상을 덮어쓰지 않습니다. 자세한 내용은 [Sidebars](https://developer.apple.com/design/human-interface-guidelines/sidebars)를 참조하십시오.



![A screenshot of a window that includes a sidebar.](https://docs-assets.developer.apple.com/published/f76d78192622b89754e5ea0058327ec3/fixed-color-orange@2x.png)

_강조 색상을 주황색으로 설정하더라도, 아이클라우드 색상은 고유 색상인 파란색을 유지함._

## tvOS

### - 앱 로고와 조화를 이루는 제한된 색상 팔레트를 선택하는 것을 고려하세요. 
색상을 미묘하게 사용하면 콘텐츠에 포커스를 맞출 수 있으며, 브랜드를 전달하는 데 도움이 될 수 있습니다.

### - 포커스를 나타내기 위해 오직 색상만 사용하지 마세요. 
요소가 포커스 상태에 있을 때 상호 작용을 나타내는 주요 방법은 미묘한 크기 조정과 반응형 애니메이션입니다.


## visionOS
### - 색상 수를 적게 사용하세요. 특히나 glass material을 사용하는 경우에는 더욱 주의해야 합니다.

표준 visionOS 창은 일반적으로 시스템에서 정의한 glass [material](https://developer.apple.com/design/human-interface-guidelines/materials) 를 사용하며, 이로 인해 사용자의 물리적 환경과 공간에서 빛과 물체가 투과됩니다. 이러한 물리적 및 가상 객체의 색상은 glass를 통해 보이므로 창의 컬러풀한 앱 콘텐츠의 가독성에 영향을 미칠 수 있습니다. 색상은 주요 정보를 강조하거나 인터페이스 부분 간의 관계를 보여주는 데 도움이 될 수 있는 곳에서 사용하는 것이 좋습니다.

### - 굵은 텍스트와 큰 영역에서 색상을 사용하는 것을 선호합니다. 
가벼운 텍스트나 작은 영역에서 색상을 사용하면 이해하고 볼 때 어려워질 수 있습니다.

## watchOS

### - 배경 색상을 사용하여 기존 콘텐츠를 지원하거나 추가 정보를 제공하세요. 
배경 색상은 장소의 느낌을 정립하고 중요한 콘텐츠를 인식하는 데 도움이 될 수 있습니다. 예를 들어, Activity에서 각 움직이기, 운동하기 및 일어서기 활동 링에 대한 정보 그래픽 뷰마다 해당 사용자가 중점을 두고 있는 링의 색상과 일치하는 배경이 있습니다. 시각적 장식으로 사용하는 대신 배경 색상은 무언가 의미를 전달할 때 사용하세요.

###    사람들은 그래픽 복잡성에서 전체 색상 대신 "tinted mode"를 사용하는 것을 선호할 수 있습니다.
시스템은 그래픽 복잡성 이미지, 게이지 및 텍스트에 대한 착용자의 선택한 색상을 기반으로 한 단일 색상을 사용할 수 있습니다. 자세한 내용은 [Complications](https://developer.apple.com/design/human-interface-guidelines/complications)를 참조하세요.

> tinted mode: Apple Watch에서 배경화면의 테마 색상을 변경 할 수 있는 기능

## Specifications (색상 사양)

### iOS, iPadOS 시스템 컬러

|Name|SwiftUI API|Default (Light)|Default (Dark)|Accessible (Light)|Accessible (Dark)|
|---|---|---|---|---|---|
|Red|[`red`](https://developer.apple.com/documentation/SwiftUI/Color/red)|![R-255,G-59,B-48](https://docs-assets.developer.apple.com/published/f4aaf47d193ae2ae09d9ae3f06bce94a/ios-default-systemred@2x.png)|![R-255,G-69,B-58](https://docs-assets.developer.apple.com/published/5aa3a92a47b18889c509e57c0a6599f8/ios-default-systemreddark@2x.png)|![R-215,G-0,B-21](https://docs-assets.developer.apple.com/published/89460987eb0ea315bb660224c2e600e8/ios-accessible-systemred@2x.png)|![R-255,G-105,B-97](https://docs-assets.developer.apple.com/published/1cec2deea516f504a96f0e5efb39a8cd/ios-accessible-systemreddark@2x.png)|
|Orange|[`orange`](https://developer.apple.com/documentation/SwiftUI/Color/orange)|![R-255,G-149,B-0](https://docs-assets.developer.apple.com/published/567e9067fdcd4cea6a446fe2ee08bc73/ios-default-systemorange@2x.png)|![R-255,G-159,B-10](https://docs-assets.developer.apple.com/published/5400a1fadd4ac009aeeb7c8390094cb1/ios-default-systemorangedark@2x.png)|![R-201,G-52,B-0](https://docs-assets.developer.apple.com/published/b6b01e70055dd5e6904b76a51532f47f/ios-accessible-systemorange@2x.png)|![R-255,G-179,B-64](https://docs-assets.developer.apple.com/published/3557135c57fb4ab9fa1eeba6c684ac83/ios-accessible-systemorangedark@2x.png)|
|Yellow|[`yellow`](https://developer.apple.com/documentation/SwiftUI/Color/yellow)|![R-255,G-204,B-0](https://docs-assets.developer.apple.com/published/ab89be5f69e921aee9b9e506e18e09a1/ios-default-systemyellow@2x.png)|![R-255,G-214,B-10](https://docs-assets.developer.apple.com/published/e48454507e506681c76b3d7618b274e0/ios-default-systemyellowdark@2x.png)|![R-178,G-80,B-0](https://docs-assets.developer.apple.com/published/9aa49a5de99e6f011a6be02913d3534a/ios-accessible-systemyellow@2x.png)|![R-255,G-212,B-38](https://docs-assets.developer.apple.com/published/9a8098387d46815eb96258a39fa602e2/ios-accessible-systemyellowdark@2x.png)|
|Green|[`green`](https://developer.apple.com/documentation/SwiftUI/Color/green)|![R-52,G-199,B-89](https://docs-assets.developer.apple.com/published/c42884430d2791322b86eebacbb848e2/ios-default-systemgreen@2x.png)|![R-48,G-209,B-88](https://docs-assets.developer.apple.com/published/8ac8ac9f079b51d643538331dd5a6220/ios-default-systemgreendark@2x.png)|![R-36,G-138,B-61](https://docs-assets.developer.apple.com/published/ba763404ccea734470bf659483c3dbf4/ios-accessible-systemgreen@2x.png)|![R-48,G-219,B-91](https://docs-assets.developer.apple.com/published/da0e2166e319c61c7267ccc8987b4e80/ios-accessible-systemgreendark@2x.png)|
|Mint|[`mint`](https://developer.apple.com/documentation/SwiftUI/Color/mint)|![R-0,G-199,B-190](https://docs-assets.developer.apple.com/published/975ceb1779465b4013fd1d29ffdcc4ae/ios-default-systemmint@2x.png)|![R-102,G-212,B-207](https://docs-assets.developer.apple.com/published/a18eb488f857e96a042b37258b533a31/ios-default-systemmintdark@2x.png)|![R-12,G-129,B-123](https://docs-assets.developer.apple.com/published/068988c6c7160f99a66a047fa9c77493/ios-accessible-systemmint@2x.png)|![R-102,G-212,B-207](https://docs-assets.developer.apple.com/published/5be9b18f009bd86f83ce6318151fc22e/ios-accessible-systemmintdark@2x.png)|
|Teal|[`teal`](https://developer.apple.com/documentation/SwiftUI/Color/teal)|![R-48,G-176,B-199](https://docs-assets.developer.apple.com/published/af0174e38b64098eeae05d2575504deb/ios-default-systemteal@2x.png)|![R-64,G-200,B-224](https://docs-assets.developer.apple.com/published/9d87270543918196403773345ad173c7/ios-default-systemtealdark@2x.png)|![R-0,G-130,B-153](https://docs-assets.developer.apple.com/published/07b7bd637f59aaa1e514c2e97755ff7e/ios-accessible-systemteal@2x.png)|![R-93,G-230,B-255](https://docs-assets.developer.apple.com/published/04a731173265920ca499c893ce1fd77f/ios-accessible-systemtealdark@2x.png)|
|Cyan|[`cyan`](https://developer.apple.com/documentation/SwiftUI/Color/cyan)|![R-50,G-173,B-230](https://docs-assets.developer.apple.com/published/5d676b12b125d92673c50407afb11831/ios-default-systemcyan@2x.png)|![R-100,G-210,B-255](https://docs-assets.developer.apple.com/published/a3b2383fd844e9d9d6c4b87f65e9f0ca/ios-default-systemcyandark@2x.png)|![R-0,G-113,B-164](https://docs-assets.developer.apple.com/published/a8807f3d2e042f7f925602b9a283e09c/ios-accessible-systemcyan@2x.png)|![R-112,G-215,B-255](https://docs-assets.developer.apple.com/published/dacbef1d03e0de9c8a2a977a5cc8b627/ios-accessible-systemcyandark@2x.png)|
|Blue|[`blue`](https://developer.apple.com/documentation/SwiftUI/Color/blue)|![R-0,G-122,B-255](https://docs-assets.developer.apple.com/published/16c405dfdf1f7ebfd0b4741d012665bf/ios-default-systemblue@2x.png)|![R-10,G-132,B-255](https://docs-assets.developer.apple.com/published/cb82c8812e9d2839528e6f4e33c34398/ios-default-systembluedark@2x.png)|![R-0,G-64,B-221](https://docs-assets.developer.apple.com/published/2ec770e8fbcb32741ea684a3326b4134/ios-accessible-systemblue@2x.png)|![R-64,G-156,B-255](https://docs-assets.developer.apple.com/published/b814e52cbbdb22b5b22400ea9c188b10/ios-accessible-systembluedark@2x.png)|
|Indigo|[`indigo`](https://developer.apple.com/documentation/SwiftUI/Color/indigo)|![R-88,G-86,B-214](https://docs-assets.developer.apple.com/published/7e7de44695a4670593873b8cb20e8d66/ios-default-systemindigo@2x.png)|![R-94,G-92,B-230](https://docs-assets.developer.apple.com/published/0d50887019f663c11c3a58bbb668bf68/ios-default-systemindigodark@2x.png)|![R-54,G-52,B-163](https://docs-assets.developer.apple.com/published/60fb138bb72c4e17fb7b106f5033ebd1/ios-accessible-systemindigo@2x.png)|![R-125,G-122,B-255](https://docs-assets.developer.apple.com/published/5dcff8d5a9b01f6baa9a81b143b82e16/ios-accessible-systemindigodark@2x.png)|
|Purple|[`purple`](https://developer.apple.com/documentation/SwiftUI/Color/purple)|![R-175,G-82,B-222](https://docs-assets.developer.apple.com/published/b67701347b8a63c6d78acd8c1bb11763/ios-default-systempurple@2x.png)|![R-191,G-90,B-242](https://docs-assets.developer.apple.com/published/8d3492f6769757da4f560ebfaaafaf5e/ios-default-systempurpledark@2x.png)|![R-137,G-68,B-171](https://docs-assets.developer.apple.com/published/fe1af8a6d9a1905c46a6242b8c40a760/ios-accessible-systempurple@2x.png)|![R-218,G-143,B-255](https://docs-assets.developer.apple.com/published/a0f0e175410dad37dc18819f6fa715cb/ios-accessible-systempurpledark@2x.png)|
|Pink|[`pink`](https://developer.apple.com/documentation/SwiftUI/Color/pink)|![R-255,G-45,B-85](https://docs-assets.developer.apple.com/published/3850a6b81b62e6018d3012d75b8803c2/ios-default-systempink@2x.png)|![R-255,G-55,B-95](https://docs-assets.developer.apple.com/published/90eb0ddcff7557d24db27539f3e72c66/ios-default-systempinkdark@2x.png)|![R-211,G-15,B-69](https://docs-assets.developer.apple.com/published/51de7f55f297d1d0f1c03d85da22fa8f/ios-accessible-systempink@2x.png)|![R-255,G-100,B-130](https://docs-assets.developer.apple.com/published/b189a280c8f495ef77995bc5006c83d8/ios-accessible-systempinkdark@2x.png)|
|Brown|[`brown`](https://developer.apple.com/documentation/SwiftUI/Color/brown)|![R-165,G-132,B-94](https://docs-assets.developer.apple.com/published/cabbed007a626e981261c8343b2972e9/ios-default-systembrown@2x.png)|![R-172,G-142,B-104](https://docs-assets.developer.apple.com/published/3379b112bf35f8cb6171b88f0f51250c/ios-default-systembrowndark@2x.png)|![R-127,G-101,B-69](https://docs-assets.developer.apple.com/published/322db8338d64279a13f3ab472737a3fe/ios-accessible-systembrown@2x.png)|![R-181,G-148,B-105](https://docs-assets.developer.apple.com/published/acfd53a3c548cfd0dc338ed70a1da2d1/ios-accessible-systembrowndark@2x.png)|

### iOS, iPadOS 시스템 회색 컬러
|Name|SwiftUI API|Default (Light)|Default (Dark)|Accessible (Light)|Accessible (Dark)|
|---|---|---|---|---|---|
|Gray|[`gray`](https://developer.apple.com/documentation/SwiftUI/Color/gray)|![R-142,G-142,B-147](https://docs-assets.developer.apple.com/published/cc1289b6fd4b76c79bbeda356463232a/ios-default-systemgray@2x.png)|![R-142,G-142,B-147](https://docs-assets.developer.apple.com/published/cc1289b6fd4b76c79bbeda356463232a/ios-default-systemgraydark@2x.png)|![R-108,G-108,B-112](https://docs-assets.developer.apple.com/published/5d86cbc8b4ddef8b68954882b4c87a18/ios-accessible-systemgray@2x.png)|![R-174,G-174,B-178](https://docs-assets.developer.apple.com/published/d00617ff05181a53d2cb5ddf143d502e/ios-accessible-systemgraydark@2x.png)|
|Gray (2)|[`systemGray2`](https://developer.apple.com/documentation/uikit/uicolor/3255071-systemgray2)|![R-174,G-174,B-178](https://docs-assets.developer.apple.com/published/d00617ff05181a53d2cb5ddf143d502e/ios-default-systemgray2@2x.png)|![R-99,G-99,B-102](https://docs-assets.developer.apple.com/published/1f681e808c0f4f35a2e7642872719c8b/ios-default-systemgray2dark@2x.png)|![R-142,G-142,B-147](https://docs-assets.developer.apple.com/published/cc1289b6fd4b76c79bbeda356463232a/ios-accessible-systemgray2@2x.png)|![R-124,G-124,B-128](https://docs-assets.developer.apple.com/published/f941ec556140a435aa9556a993e57e63/ios-accessible-systemgray2dark@2x.png)|
|Gray (3)|[`systemGray3`](https://developer.apple.com/documentation/uikit/uicolor/3255072-systemgray3)|![R-199,G-199,B-204](https://docs-assets.developer.apple.com/published/bcbb9fb97382e52aa09de7239a6edcf7/ios-default-systemgray3@2x.png)|![R-72,G-72,B-74](https://docs-assets.developer.apple.com/published/d99ad33dcdd426585e7107e1b130d713/ios-default-systemgray3dark@2x.png)|![R-174,G-174,B-178](https://docs-assets.developer.apple.com/published/d00617ff05181a53d2cb5ddf143d502e/ios-accessible-systemgray3@2x.png)|![R-84,G-84,B-86](https://docs-assets.developer.apple.com/published/693c40b65e2752b3a2b7741d61ebbb3b/ios-accessible-systemgray3dark@2x.png)|
|Gray (4)|[`systemGray4`](https://developer.apple.com/documentation/uikit/uicolor/3255073-systemgray4)|![R-209,G-209,B-214](https://docs-assets.developer.apple.com/published/5e1c546e8c78d9700b1ee58ce3a39972/ios-default-systemgray4@2x.png)|![R-58,G-58,B-60](https://docs-assets.developer.apple.com/published/983cdcdfa9a664db0c5ff7c09905582a/ios-default-systemgray4dark@2x.png)|![R-188,G-188,B-192](https://docs-assets.developer.apple.com/published/93644725b33daf923f7e3a146e9b2d42/ios-accessible-systemgray4@2x.png)|![R-68,G-68,B-70](https://docs-assets.developer.apple.com/published/6439d861c1fe8a41615d5f09d3cde938/ios-accessible-systemgray4dark@2x.png)|
|Gray (5)|[`systemGray5`](https://developer.apple.com/documentation/uikit/uicolor/3255074-systemgray5)|![R-229,G-229,B-234](https://docs-assets.developer.apple.com/published/91f296b3990bfe6dcd28b1804c803581/ios-default-systemgray5@2x.png)|![R-44,G-44,B-46](https://docs-assets.developer.apple.com/published/a8b1d65979b02865c203f18019b1084d/ios-default-systemgray5dark@2x.png)|![R-216,G-216,B-220](https://docs-assets.developer.apple.com/published/616159815cf002c39f570affa027c298/ios-accessible-systemgray5@2x.png)|![R-54,G-54,B-56](https://docs-assets.developer.apple.com/published/aacb35c6af213ef544f77d26df56df39/ios-accessible-systemgray5dark@2x.png)|
|Gray (6)|[`systemGray6`](https://developer.apple.com/documentation/uikit/uicolor/3255075-systemgray6)|![R-242,G-242,B-247](https://docs-assets.developer.apple.com/published/3d60e2b1bf4771610453a31de912647b/ios-default-systemgray6@2x.png)|![R-28,G-28,B-30](https://docs-assets.developer.apple.com/published/5d86f031014f556ef2d26da001c1f639/ios-default-systemgray6dark@2x.png)|![R-235,G-235,B-240](https://docs-assets.developer.apple.com/published/82102708ad5dc7921fc0473f6ace4613/ios-accessible-systemgray6@2x.png)|![R-36,G-36,B-38](https://docs-assets.developer.apple.com/published/5dc6249020925c5ec09f88f8adc9bbaa/ios-accessible-systemgray6dark@2x.png)|



### macOS 시스템 컬러

- #### 일반 색상 (Default)

|Name|SwiftUI API|Default (Light)|Default (Dark)|Accessible (Light)|Accessible (Dark)|
|---|---|---|---|---|---|
|Red|[`red`](https://developer.apple.com/documentation/SwiftUI/Color/red)|![R-255,G-59,B-48](https://docs-assets.developer.apple.com/published/91c243d66972a42afa638268456c2c13/macos-default-systemredcolor@2x.png)|![R-255,G-69,B-58](https://docs-assets.developer.apple.com/published/5aa3a92a47b18889c509e57c0a6599f8/macos-default-systemredcolordark@2x.png)|![R-215,G-0,B-21](https://docs-assets.developer.apple.com/published/89460987eb0ea315bb660224c2e600e8/macos-accessible-systemredcolor@2x.png)|![R-255,G-105,B-97](https://docs-assets.developer.apple.com/published/1cec2deea516f504a96f0e5efb39a8cd/macos-accessible-systemredcolordark@2x.png)|
|Orange|[`orange`](https://developer.apple.com/documentation/SwiftUI/Color/orange)|![R-255,G-149,B-0](https://docs-assets.developer.apple.com/published/567e9067fdcd4cea6a446fe2ee08bc73/macos-default-systemorangecolor@2x.png)|![R-255,G-159,B-10](https://docs-assets.developer.apple.com/published/7eb7ad3812b3af3561847ba0fb59d1d2/macos-default-systemorangecolordark@2x.png)|![R-201,G-52,B-0](https://docs-assets.developer.apple.com/published/b6b01e70055dd5e6904b76a51532f47f/macos-accessible-systemorangecolor@2x.png)|![R-255,G-179,B-64](https://docs-assets.developer.apple.com/published/3557135c57fb4ab9fa1eeba6c684ac83/macos-accessible-systemorangecolordark@2x.png)|
|Yellow|[`yellow`](https://developer.apple.com/documentation/SwiftUI/Color/yellow)|![R-255,G-204,B-0](https://docs-assets.developer.apple.com/published/27a776b32f7de6250a0578cd1daf59c2/macos-default-systemyellowcolor@2x.png)|![R-255,G-214,B-10](https://docs-assets.developer.apple.com/published/ed50bf4c9242bc7e3810dae7c20ff446/macos-default-systemyellowcolordark@2x.png)|![R-160,G-90,B-0](https://docs-assets.developer.apple.com/published/d2efafc1d5dfd608d7041cf716718a43/macos-accessible-systemyellowcolor@2x.png)|![R-255,G-212,B-38](https://docs-assets.developer.apple.com/published/9a8098387d46815eb96258a39fa602e2/macos-accessible-systemyellowcolordark@2x.png)|
|Green|[`green`](https://developer.apple.com/documentation/SwiftUI/Color/green)|![R-40,G-205,B-65](https://docs-assets.developer.apple.com/published/4d007cc228344a3583a0a2b282777fc0/macos-default-systemgreencolor@2x.png)|![R-50,G-215,B-75](https://docs-assets.developer.apple.com/published/9bdbbbdfb442ffe152c62b026dede433/macos-default-systemgreencolordark@2x.png)|![R-0,G-125,B-27](https://docs-assets.developer.apple.com/published/6465fb62d689e455790cbfb86a826feb/macos-accessible-systemgreencolor@2x.png)|![R-49,G-222,B-75](https://docs-assets.developer.apple.com/published/94752fff73b113d92d6927efc7bf5303/macos-accessible-systemgreencolordark@2x.png)|
|Mint|[`mint`](https://developer.apple.com/documentation/SwiftUI/Color/mint)|![R-0,G-199,B-190](https://docs-assets.developer.apple.com/published/2cc3c6b1c89eaa723cb4780f6a724f40/macos-default-systemmintcolor@2x.png)|![R-102,G-212,B-207](https://docs-assets.developer.apple.com/published/5be9b18f009bd86f83ce6318151fc22e/macos-default-systemmintcolordark@2x.png)|![R-12,G-129,B-123](https://docs-assets.developer.apple.com/published/068988c6c7160f99a66a047fa9c77493/macos-accessible-systemmintcolor@2x.png)|![R-102,G-212,B-207](https://docs-assets.developer.apple.com/published/5be9b18f009bd86f83ce6318151fc22e/macos-accessible-systemmintcolordark@2x.png)|
|Teal|[`teal`](https://developer.apple.com/documentation/SwiftUI/Color/teal)|![R-89,G-173,B-196](https://docs-assets.developer.apple.com/published/50d7934e24daa921cdc0823bbd91a2c3/macos-default-systemtealcolor@2x.png)|![R-106,G-196,B-220](https://docs-assets.developer.apple.com/published/b37e5576baa719ef7f4e215d42aa8efd/macos-default-systemtealcolordark@2x.png)|![R-0,G-130,B-153](https://docs-assets.developer.apple.com/published/07b7bd637f59aaa1e514c2e97755ff7e/macos-accessible-systemtealcolor@2x.png)|![R-93,G-230,B-255](https://docs-assets.developer.apple.com/published/04a731173265920ca499c893ce1fd77f/macos-accessible-systemtealcolordark@2x.png)|
|Cyan|[`cyan`](https://developer.apple.com/documentation/SwiftUI/Color/cyan)|![R-85,G-190,B-240](https://docs-assets.developer.apple.com/published/716c9370b2d724896f2b56f4a23d1345/macos-default-systemcyancolor@2x.png)|![R-90,G-200,B-245](https://docs-assets.developer.apple.com/published/fb4b21abd6f04a9d88821d85ccc32895/macos-default-systemcyancolordark@2x.png)|![R-0,G-113,B-164](https://docs-assets.developer.apple.com/published/a8807f3d2e042f7f925602b9a283e09c/macos-accessible-systemcyancolor@2x.png)|![R-112,G-215,B-255](https://docs-assets.developer.apple.com/published/dacbef1d03e0de9c8a2a977a5cc8b627/macos-accessible-systemcyancolordark@2x.png)|
|Blue|[`blue`](https://developer.apple.com/documentation/SwiftUI/Color/blue)|![R-0,G-122,B-255](https://docs-assets.developer.apple.com/published/16c405dfdf1f7ebfd0b4741d012665bf/macos-default-systembluecolor@2x.png)|![R-10,G-132,B-255](https://docs-assets.developer.apple.com/published/59c184184ce168dcfe6cb45bea8ed17e/macos-default-systembluecolordark@2x.png)|![R-0,G-64,B-221](https://docs-assets.developer.apple.com/published/2ec770e8fbcb32741ea684a3326b4134/macos-accessible-systembluecolor@2x.png)|![R-64,G-156,B-255](https://docs-assets.developer.apple.com/published/b814e52cbbdb22b5b22400ea9c188b10/macos-accessible-systembluecolordark@2x.png)|
|Indigo|[`indigo`](https://developer.apple.com/documentation/SwiftUI/Color/indigo)|![R-88,G-86,B-214](https://docs-assets.developer.apple.com/published/02a7446445228244e058870f35ba80ad/macos-default-systemindigocolor@2x.png)|![R-94,G-92,B-230](https://docs-assets.developer.apple.com/published/0d50887019f663c11c3a58bbb668bf68/macos-default-systemindigocolordark@2x.png)|![R-54,G-52,B-163](https://docs-assets.developer.apple.com/published/60fb138bb72c4e17fb7b106f5033ebd1/macos-accessible-systemindigocolor@2x.png)|![R-125,G-122,B-255](https://docs-assets.developer.apple.com/published/5dcff8d5a9b01f6baa9a81b143b82e16/macos-accessible-systemindigocolordark@2x.png)|
|Purple|[`purple`](https://developer.apple.com/documentation/SwiftUI/Color/purple)|![R-175,G-82,B-222](https://docs-assets.developer.apple.com/published/b67701347b8a63c6d78acd8c1bb11763/macos-default-systempurplecolor@2x.png)|![R-191,G-90,B-242](https://docs-assets.developer.apple.com/published/8d3492f6769757da4f560ebfaaafaf5e/macos-default-systempurplecolordark@2x.png)|![R-173,G-68,B-171](https://docs-assets.developer.apple.com/published/00269577c70780f7af36524b0b46d6e5/macos-accessible-systempurplecolor@2x.png)|![R-218,G-143,B-255](https://docs-assets.developer.apple.com/published/a0f0e175410dad37dc18819f6fa715cb/macos-accessible-systempurplecolordark@2x.png)|
|Pink|[`pink`](https://developer.apple.com/documentation/SwiftUI/Color/pink)|![R-255,G-45,B-85](https://docs-assets.developer.apple.com/published/63cacf7b67ef9c503742c0d2d164650d/macos-default-systempinkcolor@2x.png)|![R-255,G-55,B-95](https://docs-assets.developer.apple.com/published/90eb0ddcff7557d24db27539f3e72c66/macos-default-systempinkcolordark@2x.png)|![R-211,G-15,B-69](https://docs-assets.developer.apple.com/published/51de7f55f297d1d0f1c03d85da22fa8f/macos-accessible-systempinkcolor@2x.png)|![R-255,G-100,B-130](https://docs-assets.developer.apple.com/published/b189a280c8f495ef77995bc5006c83d8/macos-accessible-systempinkcolordark@2x.png)|
|Brown|[`brown`](https://developer.apple.com/documentation/SwiftUI/Color/brown)|![R-162,G-132,B-94](https://docs-assets.developer.apple.com/published/cabbed007a626e981261c8343b2972e9/macos-default-systembrowncolor@2x.png)|![R-172,G-142,B-104](https://docs-assets.developer.apple.com/published/3379b112bf35f8cb6171b88f0f51250c/macos-default-systembrowncolordark@2x.png)|![R-127,G-101,B-69](https://docs-assets.developer.apple.com/published/322db8338d64279a13f3ab472737a3fe/macos-accessible-systembrowncolor@2x.png)|![R-181,G-148,B-105](https://docs-assets.developer.apple.com/published/acfd53a3c548cfd0dc338ed70a1da2d1/macos-accessible-systembrowncolordark@2x.png)|
|Gray|[`gray`](https://developer.apple.com/documentation/SwiftUI/Color/gray)|![R-142,G-142,B-147](https://docs-assets.developer.apple.com/published/cc1289b6fd4b76c79bbeda356463232a/macos-default-systemgraycolor@2x.png)|![R-152,G-152,B-157](https://docs-assets.developer.apple.com/published/3253664caeaff5e0102647fb57a6fa78/macos-default-systemgraycolordark@2x.png)|![R-105,G-105,B-110](https://docs-assets.developer.apple.com/published/ac3ab8c464acd04ea3915e4ba103bb82/macos-accessible-systemgraycolor@2x.png)|![R-152,G-152,B-157](https://docs-assets.developer.apple.com/published/3253664caeaff5e0102647fb57a6fa78/macos-accessible-systemgraycolordark@2x.png)|

- #### 강조 색상 (Vibrant)

|Name|SwiftUI API|Default (Light)|Default (Dark)|Accessible (Light)|Accessible (Dark)|
|---|---|---|---|---|---|
|Red|[`red`](https://developer.apple.com/documentation/SwiftUI/Color/red)|![R-255,G-49,B-38](https://docs-assets.developer.apple.com/published/01d934571e1abcdadfdc8efed2b1f4c3/macos-vibrant-default-systemredcolor@2x.png)|![R-255,G-79,B-68](https://docs-assets.developer.apple.com/published/779fca9031d54ca4c52ccdba7ec8535d/macos-vibrant-default-systemredcolordark@2x.png)|![R-194,G-6,B-24](https://docs-assets.developer.apple.com/published/55c8fac93cbb2967c33e98db0580c5ec/macos-vibrant-accessible-default-systemredcolor@2x.png)|![R-255,G-65,B-54](https://docs-assets.developer.apple.com/published/166a4352681b9273246f9a536e9f67c8/macos-vibrant-accessible-default-systemredcolordark@2x.png)|
|Orange|[`orange`](https://developer.apple.com/documentation/SwiftUI/Color/orange)|![R-245,G-139,B-0](https://docs-assets.developer.apple.com/published/7a7ae0fbf9b72e2f75150b0d4769c20b/macos-vibrant-default-systemorangecolor@2x.png)|![R-255,G-169,B-20](https://docs-assets.developer.apple.com/published/a410027e803fa7e441cc86aafe3a2eba/macos-vibrant-default-systemorangecolordark@2x.png)|![R-173,G-58,B-0](https://docs-assets.developer.apple.com/published/84674689dbb0b23cff7edabd4d0ae7ac/macos-vibrant-accessible-default-systemorangecolor@2x.png)|![R-255,G-179,B-64](https://docs-assets.developer.apple.com/published/3557135c57fb4ab9fa1eeba6c684ac83/macos-vibrant-accessible-default-systemorangecolordark@2x.png)|
|Yellow|[`yellow`](https://developer.apple.com/documentation/SwiftUI/Color/yellow)|![R-245,G-194,B-0](https://docs-assets.developer.apple.com/published/63f71742a8e89f9070519d11317ede70/macos-vibrant-default-systemyellowcolor@2x.png)|![R-255,G-169,B-20](https://docs-assets.developer.apple.com/published/919174e6291f665d04033f8f816e8a56/macos-vibrant-default-systemyellowcolordark@2x.png)|![R-146,G-81,B-0](https://docs-assets.developer.apple.com/published/846341ddc88138751a85bf5acbbb5da9/macos-vibrant-accessible-default-systemyellowcolor@2x.png)|![R-255,G-212,B-38](https://docs-assets.developer.apple.com/published/9a8098387d46815eb96258a39fa602e2/macos-vibrant-accessible-default-systemyellowcolordark@2x.png)|
|Green|[`green`](https://developer.apple.com/documentation/SwiftUI/Color/green)|![R-30,G-195,B-55](https://docs-assets.developer.apple.com/published/da6ab717fa48377fd8ebf17b83e35e77/macos-vibrant-default-systemgreencolor@2x.png)|![R-60,G-225,B-85](https://docs-assets.developer.apple.com/published/7f7bbe889860d3dbc62230fbad72a498/macos-vibrant-default-systemgreencolordark@2x.png)|![R-0,G-112,B-24](https://docs-assets.developer.apple.com/published/2d215054e924b5ba321d00beea260c2c/macos-vibrant-accessible-default-systemgreencolor@2x.png)|![R-49,G-222,B-75](https://docs-assets.developer.apple.com/published/94752fff73b113d92d6927efc7bf5303/macos-vibrant-accessible-default-systemgreencolordark@2x.png)|
|Mint|[`mint`](https://developer.apple.com/documentation/SwiftUI/Color/mint)|![R-0,G-189,B-180](https://docs-assets.developer.apple.com/published/70388c00b62a59131d2bc52446001cc2/macos-vibrant-default-systemmintcolor@2x.png)|![R-108,G-224,B-219](https://docs-assets.developer.apple.com/published/ac81d618f1e9c9271ab232d85590c70e/macos-vibrant-default-systemmintcolordark@2x.png)|![R-11,G-117,B-112](https://docs-assets.developer.apple.com/published/556a27bbcf7f02e0f0a02a9f4e58c4e4/macos-vibrant-accessible-default-systemmintcolor@2x.png)|![R-102,G-212,B-207](https://docs-assets.developer.apple.com/published/5be9b18f009bd86f83ce6318151fc22e/macos-vibrant-accessible-default-systemmintcolordark@2x.png)|
|Teal|[`teal`](https://developer.apple.com/documentation/SwiftUI/Color/teal)|![R-46,G-167,B-189](https://docs-assets.developer.apple.com/published/8b071d59fd73452a1f7f239503aef76e/macos-vibrant-default-systemtealcolor@2x.png)|![R-68,G-212,B-237](https://docs-assets.developer.apple.com/published/7080171ca35cc9e20f8c32abfcac0930/macos-vibrant-default-systemtealcolordark@2x.png)|![R-0,G-119,B-140](https://docs-assets.developer.apple.com/published/14b1b64f002b286cc46aac406c3cd7aa/macos-vibrant-accessible-default-systemtealcolor@2x.png)|![R-93,G-230,B-255](https://docs-assets.developer.apple.com/published/04a731173265920ca499c893ce1fd77f/macos-vibrant-accessible-default-systemtealcolordark@2x.png)|
|Cyan|[`cyan`](https://developer.apple.com/documentation/SwiftUI/Color/cyan)|![R-65,G-175,B-220](https://docs-assets.developer.apple.com/published/56c79334d675ff7c3eabb837d2a79061/macos-vibrant-default-systemcyancolor@2x.png)|![R-90,G-205,B-250](https://docs-assets.developer.apple.com/published/bdecf4096285fab8572e84da14353ee8/macos-vibrant-default-systemcyancolordark@2x.png)|![R-0,G-103,B-150](https://docs-assets.developer.apple.com/published/614e9f6a8731a2a3dbfadfc6f3438182/macos-vibrant-accessible-default-systemcyancolor@2x.png)|![R-112,G-215,B-255](https://docs-assets.developer.apple.com/published/dacbef1d03e0de9c8a2a977a5cc8b627/macos-vibrant-accessible-default-systemcyancolordark@2x.png)|
|Blue|[`blue`](https://developer.apple.com/documentation/SwiftUI/Color/blue)|![R-0,G-112,B-245](https://docs-assets.developer.apple.com/published/3a7b2c330fda125d08c8986db654fae5/macos-vibrant-default-systembluecolor@2x.png)|![R-20,G-142,B-255](https://docs-assets.developer.apple.com/published/104551cbf61516f3ecd13004a8ee420a/macos-vibrant-default-systembluecolordark@2x.png)|![R-0,G-64,B-221](https://docs-assets.developer.apple.com/published/2ec770e8fbcb32741ea684a3326b4134/macos-vibrant-accessible-default-systembluecolor@2x.png)|![R-64,G-156,B-255](https://docs-assets.developer.apple.com/published/b814e52cbbdb22b5b22400ea9c188b10/macos-vibrant-accessible-default-systembluecolordark@2x.png)|
|Indigo|[`indigo`](https://developer.apple.com/documentation/SwiftUI/Color/indigo)|![R-84,G-82,B-204](https://docs-assets.developer.apple.com/published/c8b5565db22e1049ab9e48aeea3381dd/macos-vibrant-default-systemindigocolor@2x.png)|![R-99,G-97,B-242](https://docs-assets.developer.apple.com/published/b6d84ad8c9173d547fc50ee07017d7cd/macos-vibrant-default-systemindigocolordark@2x.png)|![R-54,G-52,B-163](https://docs-assets.developer.apple.com/published/60fb138bb72c4e17fb7b106f5033ebd1/macos-vibrant-accessible-default-systemindigocolor@2x.png)|![R-125,G-122,B-255](https://docs-assets.developer.apple.com/published/5dcff8d5a9b01f6baa9a81b143b82e16/macos-vibrant-accessible-default-systemindigocolordark@2x.png)|
|Purple|[`purple`](https://developer.apple.com/documentation/SwiftUI/Color/purple)|![R-159,G-75,B-201](https://docs-assets.developer.apple.com/published/e62b6ec90d04393303fe98b71cb7151f/macos-vibrant-default-systempurplecolor@2x.png)|![R-204,G-101,B-255](https://docs-assets.developer.apple.com/published/f0cb708ae7166b1511b910d611bfbf74/macos-vibrant-default-systempurplecolordark@2x.png)|![R-173,G-68,B-171](https://docs-assets.developer.apple.com/published/00269577c70780f7af36524b0b46d6e5/macos-vibrant-accessible-default-systempurplecolor@2x.png)|![R-218,G-143,B-255](https://docs-assets.developer.apple.com/published/a0f0e175410dad37dc18819f6fa715cb/macos-vibrant-accessible-default-systempurplecolordark@2x.png)|
|Pink|[`pink`](https://developer.apple.com/documentation/SwiftUI/Color/pink)|![R-245,G-35,B-75](https://docs-assets.developer.apple.com/published/5a2a633b049141887f0079a94999f74e/macos-vibrant-default-systempinkcolor@2x.png)|![R-255,G-65,B-105](https://docs-assets.developer.apple.com/published/e3c606d8c1e4f351360be4e64844ece0/macos-vibrant-default-systempinkcolordark@2x.png)|![R-193,G-16,B-50](https://docs-assets.developer.apple.com/published/3ee4cb5cb376966d3693947641c0bac6/macos-vibrant-accessible-default-systempinkcolor@2x.png)|![R-255,G-58,B-95](https://docs-assets.developer.apple.com/published/4712bc131d86fef26ac82a27f3caab58/macos-vibrant-accessible-default-systempinkcolordark@2x.png)|
|Brown|[`brown`](https://developer.apple.com/documentation/SwiftUI/Color/brown)|![R-152,G-122,B-84](https://docs-assets.developer.apple.com/published/886cac197db9e06750e88fff00066464/macos-vibrant-default-systembrowncolor@2x.png)|![R-182,G-152,B-114](https://docs-assets.developer.apple.com/published/e5dd2e39dcee1c01e7a8d7633f753446/macos-vibrant-default-systembrowncolordark@2x.png)|![R-119,G-93,B-59](https://docs-assets.developer.apple.com/published/6b9cf9d5fe0d625586ecae266150419f/macos-vibrant-accessible-default-systembrowncolor@2x.png)|![R-181,G-148,B-105](https://docs-assets.developer.apple.com/published/acfd53a3c548cfd0dc338ed70a1da2d1/macos-vibrant-accessible-default-systembrowncolordark@2x.png)|
|Gray|[`gray`](https://developer.apple.com/documentation/SwiftUI/Color/gray)|![R-132,G-132,B-137](https://docs-assets.developer.apple.com/published/476fa41f295bfd051acc1e66f2866e4a/macos-vibrant-default-systemgraycolor@2x.png)|![R-162,G-162,B-167](https://docs-assets.developer.apple.com/published/df92418eceb6b60ea792489cc8ae9691/macos-vibrant-default-systemgraycolordark@2x.png)|![R-97,G-97,B-101](https://docs-assets.developer.apple.com/published/b34194ad2011ec3d5826572038f8a7d1/macos-vibrant-accessible-default-systemgraycolor@2x.png)|![R-152,G-152,B-157](https://docs-assets.developer.apple.com/published/3253664caeaff5e0102647fb57a6fa78/macos-vibrant-accessible-default-systemgraycolordark@2x.png)|


### visionOS 시스템 컬러

|Name|SwiftUI API|Default|
|---|---|---|
|Red|[`red`](https://developer.apple.com/documentation/SwiftUI/Color/red)|![R-255,G-69,B-58](https://docs-assets.developer.apple.com/published/4d40d6023d8ed46f41e70225e553b0c8/visionos-default-systemred@2x.png)|
|Orange|[`orange`](https://developer.apple.com/documentation/SwiftUI/Color/orange)|![R-255,G-159,B-10](https://docs-assets.developer.apple.com/published/ffda917a4aaeb55f33a7b0e03a49abb3/visionos-default-systemorange@2x.png)|
|Yellow|[`yellow`](https://developer.apple.com/documentation/SwiftUI/Color/yellow)|![R-255,G-214,B-10](https://docs-assets.developer.apple.com/published/bac06fe61f672e6cbb15c3f277d5bcb8/visionos-default-systemyellow@2x.png)|
|Green|[`green`](https://developer.apple.com/documentation/SwiftUI/Color/green)|![R-50,G-215,B-75](https://docs-assets.developer.apple.com/published/15659e4abd425084baa95709c798c119/visionos-default-systemgreen@2x.png)|
|Mint|[`mint`](https://developer.apple.com/documentation/SwiftUI/Color/mint)|![R-102,G-212,B-207](https://docs-assets.developer.apple.com/published/2514d36fd45cd186a1e0d6cccd6d2091/visionos-default-systemmint@2x.png)|
|Teal|[`teal`](https://developer.apple.com/documentation/SwiftUI/Color/teal)|![R-106,G-196,B-220](https://docs-assets.developer.apple.com/published/c1ea509967b895c4228d0f70ca994619/visionos-default-systemteal@2x.png)|
|Cyan|[`cyan`](https://developer.apple.com/documentation/SwiftUI/Color/cyan)|![R-90,G-200,B-245](https://docs-assets.developer.apple.com/published/1932eaec7b55f48450d6b20b718a9823/visionos-default-systemcyan@2x.png)|
|Blue|[`blue`](https://developer.apple.com/documentation/SwiftUI/Color/blue)|![R-10,G-132,B-255](https://docs-assets.developer.apple.com/published/eb3c5e047ad0c38811fd1ed284b7e1cc/visionos-default-systemblue@2x.png)|
|Indigo|[`indigo`](https://developer.apple.com/documentation/SwiftUI/Color/indigo)|![R-94,G-92,B-230](https://docs-assets.developer.apple.com/published/4d22f19c94205865e105bf788a4e9b7d/visionos-default-systemindigo@2x.png)|
|Purple|[`purple`](https://developer.apple.com/documentation/SwiftUI/Color/purple)|![R-191,G-90,B-242](https://docs-assets.developer.apple.com/published/d5e5ac620b6e115d21ca05b111a5ff8b/visionos-default-systempurple@2x.png)|
|Pink|[`pink`](https://developer.apple.com/documentation/SwiftUI/Color/pink)|![R-255,G-55,B-95](https://docs-assets.developer.apple.com/published/3808c4c22e1a4b57ed7fc7d74a33eb3e/visionos-default-systempink@2x.png)|
|Brown|[`brown`](https://developer.apple.com/documentation/SwiftUI/Color/brown)|![R-172,G-142,B-104](https://docs-assets.developer.apple.com/published/b5ba104b74746a19e5b0a70535bf3e0d/visionos-default-systembrown@2x.png)|
|Gray|[`gray`](https://developer.apple.com/documentation/SwiftUI/Color/gray)|![R-152,G-152,B-157](https://docs-assets.developer.apple.com/published/68bacb987c7c2b7e2da5172deffb0729/visionos-default-systemgray@2x.png)|

### watchOS 시스템 컬러

|Name|SwiftUI API|Default (Light)|Default (Dark)|Accessible (Light)|Accessible (Dark)|
|---|---|---|---|---|---|
|Red|[`red`](https://developer.apple.com/documentation/SwiftUI/Color/red)|![R-246,G-52,B-40](https://docs-assets.developer.apple.com/published/556c6c0f32b8e2504e971cbb9f855480/watchos-default-systemred@2x.png)|![R-255,G-59,B-48](https://docs-assets.developer.apple.com/published/f4aaf47d193ae2ae09d9ae3f06bce94a/watchos-default-systemreddark@2x.png)|![R-215,G-0,B-21](https://docs-assets.developer.apple.com/published/89460987eb0ea315bb660224c2e600e8/watchos-accessible-systemred@2x.png)|![R-255,G-105,B-97](https://docs-assets.developer.apple.com/published/8e868567f71e8f7f6f97e4fedd3826eb/watchos-accessible-systemreddark@2x.png)|
|Orange|[`orange`](https://developer.apple.com/documentation/SwiftUI/Color/orange)|![R-255,G-140,B-0](https://docs-assets.developer.apple.com/published/8eb6d088932981c05c893c77d8c00962/watchos-default-systemorange@2x.png)|![R-255,G-149,B-0](https://docs-assets.developer.apple.com/published/567e9067fdcd4cea6a446fe2ee08bc73/watchos-default-systemorangedark@2x.png)|![R-177,G-90,B-0](https://docs-assets.developer.apple.com/published/1f659e857c0717b754ce5164f9693416/watchos-accessible-systemorange@2x.png)|![R-255,G-179,B-64](https://docs-assets.developer.apple.com/published/8a765943f89b98ab3e8001b9066a2aac/watchos-accessible-systemorangedark@2x.png)|
|Yellow|[`yellow`](https://developer.apple.com/documentation/SwiftUI/Color/yellow)|![R-255,G-204,B-0](https://docs-assets.developer.apple.com/published/ab89be5f69e921aee9b9e506e18e09a1/watchos-default-systemyellow@2x.png)|![R-255,G-214,B-10](https://docs-assets.developer.apple.com/published/e48454507e506681c76b3d7618b274e0/watchos-default-systemyellowdark@2x.png)|![R-143,G-116,B-0](https://docs-assets.developer.apple.com/published/ee04ba216a9d47a28cef8f39a7aef18b/watchos-accessible-systemyellow@2x.png)|![R-255,G-242,B-97](https://docs-assets.developer.apple.com/published/547f9d385e3f6d478edf2e3075eee56b/watchos-accessible-systemyellowdark@2x.png)|
|Green|[`green`](https://developer.apple.com/documentation/SwiftUI/Color/green)|![R-2,G-212,B-106](https://docs-assets.developer.apple.com/published/212813cf00433f9f641f68dd42744ccd/watchos-default-systemgreen@2x.png)|![R-4,G-222,B-113](https://docs-assets.developer.apple.com/published/824a9539a365ec30b85c18711b6e05e3/watchos-default-systemgreendark@2x.png)|![R-0,G-134,B-74](https://docs-assets.developer.apple.com/published/8fa0175f2a5c05e2241cc1c253b2bdc4/watchos-accessible-systemgreen@2x.png)|![R-12,G-255,B-134](https://docs-assets.developer.apple.com/published/3aec6b4046026ca6a6529ee6be83227a/watchos-accessible-systemgreendark@2x.png)|
|Mint|[`mint`](https://developer.apple.com/documentation/SwiftUI/Color/mint)|![R-0,G-199,B-190](https://docs-assets.developer.apple.com/published/975ceb1779465b4013fd1d29ffdcc4ae/watchos-default-systemmint@2x.png)|![R-0,G-245,B-234](https://docs-assets.developer.apple.com/published/291804e9f21b9e510ea6f9470014bc15/watchos-default-systemmintdark@2x.png)|![R-12,G-129,B-123](https://docs-assets.developer.apple.com/published/5c0c8358030f57f663b16badc1442136/watchos-accessible-systemmint@2x.png)|![R-108,G-255,B-249](https://docs-assets.developer.apple.com/published/cdcdd7d0034435c77ddfc9a8396e0f06/watchos-accessible-systemmintdark@2x.png)|
|Teal|[`teal`](https://developer.apple.com/documentation/SwiftUI/Color/teal)|![R-48,G-176,B-199](https://docs-assets.developer.apple.com/published/af0174e38b64098eeae05d2575504deb/watchos-default-systemteal@2x.png)|![R-64,G-200,B-224](https://docs-assets.developer.apple.com/published/9d87270543918196403773345ad173c7/watchos-default-systemtealdark@2x.png)|![R-0,G-130,B-153](https://docs-assets.developer.apple.com/published/07b7bd637f59aaa1e514c2e97755ff7e/watchos-accessible-systemteal@2x.png)|![R-93,G-230,B-255](https://docs-assets.developer.apple.com/published/04a731173265920ca499c893ce1fd77f/watchos-accessible-systemtealdark@2x.png)|
|Cyan|[`cyan`](https://developer.apple.com/documentation/SwiftUI/Color/cyan)|![R-50,G-173,B-230](https://docs-assets.developer.apple.com/published/5d676b12b125d92673c50407afb11831/watchos-default-systemcyan@2x.png)|![R-90,G-200,B-250](https://docs-assets.developer.apple.com/published/5ac8cc4d8c276f8a5dae818faa415646/watchos-default-systemcyandark@2x.png)|![R-0,G-113,B-164](https://docs-assets.developer.apple.com/published/46d71c9ad9ba92d99279eecde3fe9b3a/watchos-accessible-systemcyan@2x.png)|![R-112,G-215,B-255](https://docs-assets.developer.apple.com/published/dacbef1d03e0de9c8a2a977a5cc8b627/watchos-accessible-systemcyandark@2x.png)|
|Blue|[`blue`](https://developer.apple.com/documentation/SwiftUI/Color/blue)|![R-0,G-122,B-255](https://docs-assets.developer.apple.com/published/16c405dfdf1f7ebfd0b4741d012665bf/watchos-default-systemblue@2x.png)|![R-32,G-148,B-250](https://docs-assets.developer.apple.com/published/eda2f818060bea0073c0feeadf4c65c0/watchos-default-systembluedark@2x.png)|![R-0,G-64,B-221](https://docs-assets.developer.apple.com/published/2ec770e8fbcb32741ea684a3326b4134/watchos-accessible-systemblue@2x.png)|![R-90,G-168,B-255](https://docs-assets.developer.apple.com/published/e18b85e07acb0c2e15b1e445c34c7880/watchos-accessible-systembluedark@2x.png)|
|Indigo|[`indigo`](https://developer.apple.com/documentation/SwiftUI/Color/indigo)|![R-88,G-86,B-214](https://docs-assets.developer.apple.com/published/7e7de44695a4670593873b8cb20e8d66/watchos-default-systemindigo@2x.png)|![R-120,G-122,B-255](https://docs-assets.developer.apple.com/published/f4ef65c862881fffb501b5ee4af801fa/watchos-default-systemindigodark@2x.png)|![R-54,G-52,B-163](https://docs-assets.developer.apple.com/published/60fb138bb72c4e17fb7b106f5033ebd1/watchos-accessible-systemindigo@2x.png)|![R-155,G-153,B-255](https://docs-assets.developer.apple.com/published/bd94219ea7cf9293dda8f0178cffdbda/watchos-accessible-systemindigodark@2x.png)|
|Purple|[`purple`](https://developer.apple.com/documentation/SwiftUI/Color/purple)|![R-175,G-82,B-222](https://docs-assets.developer.apple.com/published/b67701347b8a63c6d78acd8c1bb11763/watchos-default-systempurple@2x.png)|![R-191,G-90,B-242](https://docs-assets.developer.apple.com/published/8d3492f6769757da4f560ebfaaafaf5e/watchos-default-systempurpledark@2x.png)|![R-137,G-68,B-171](https://docs-assets.developer.apple.com/published/fe1af8a6d9a1905c46a6242b8c40a760/watchos-accessible-systempurple@2x.png)|![R-218,G-143,B-255](https://docs-assets.developer.apple.com/published/a0f0e175410dad37dc18819f6fa715cb/watchos-accessible-systempurpledark@2x.png)|
|Pink|[`pink`](https://developer.apple.com/documentation/SwiftUI/Color/pink)|![R-234,G-14,B-74](https://docs-assets.developer.apple.com/published/e01844ec36528cd8d0211efbe6e80666/watchos-default-systempink@2x.png)|![R-250,G-17,B-79](https://docs-assets.developer.apple.com/published/47f9dd0ba04726ffe392d0195a88bc9e/watchos-default-systempinkdark@2x.png)|![R-211,G-15,B-69](https://docs-assets.developer.apple.com/published/bfcefde8909ccef96c6726b020e80a4c/watchos-accessible-systempink@2x.png)|![R-255,G-100,B-130](https://docs-assets.developer.apple.com/published/b189a280c8f495ef77995bc5006c83d8/watchos-accessible-systempinkdark@2x.png)|
|Brown|[`brown`](https://developer.apple.com/documentation/SwiftUI/Color/brown)|![R-162,G-132,B-94](https://docs-assets.developer.apple.com/published/cabbed007a626e981261c8343b2972e9/watchos-default-systembrown@2x.png)|![R-172,G-142,B-104](https://docs-assets.developer.apple.com/published/3379b112bf35f8cb6171b88f0f51250c/watchos-default-systembrowndark@2x.png)|![R-127,G-101,B-69](https://docs-assets.developer.apple.com/published/322db8338d64279a13f3ab472737a3fe/watchos-accessible-systembrown@2x.png)|![R-219,G-178,B-124](https://docs-assets.developer.apple.com/published/69bceb6c031c8cdc2a33e393a6bf31e1/watchos-accessible-systembrowndark@2x.png)|

---

### 관련 문서

- [Dark Mode](https://developer.apple.com/design/human-interface-guidelines/dark-mode)
- [Accessibility](https://developer.apple.com/design/human-interface-guidelines/accessibility)

### 개발자 문서
- [Color](https://developer.apple.com/documentation/SwiftUI/Color)
- [UI element colors](https://developer.apple.com/documentation/uikit/uicolor/ui_element_colors)

### 참고 영상
| [What's New in iOS Design](https://developer.apple.com/videos/play/wwdc2019/808) | [Get Started with Display P3](https://developer.apple.com/videos/play/wwdc2017/821) | [Implementing Dark Mode on iOS](https://developer.apple.com/videos/play/wwdc2019/214) |
| ------------------------ | --------------------------- | ----------------------------- |
|       ![](https://devimages-cdn.apple.com/wwdc-services/images/48/0F960683-D91F-4CA9-9658-6FBB11F0683D/3272_wide_250x141_1x.jpg)                   |            ![](https://devimages-cdn.apple.com/wwdc-services/images/7/09438FDD-3E8B-42A3-A364-78E1A7F2CE6B/1915_wide_250x141_1x.jpg)                 |       ![](https://devimages-cdn.apple.com/wwdc-services/images/48/174747D6-8723-4194-A932-7765179F1108/2949_wide_250x141_1x.jpg)                        |

