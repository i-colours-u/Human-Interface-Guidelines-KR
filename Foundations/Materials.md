
## Apple 플랫폼에서 Material 특성은 기본 시각적 콘텐츠의 색상 값을 흐리게 하거나 수정하여 반투명도를 부여합니다.


![](https://docs-assets.developer.apple.com/published/b47eb524ca1170cd60312070b9822dd4/foundations-materials-intro~dark@2x.png)



반투명은 전경 요소(Foreground) 와 배경(Background) 요소의 통합을 개선하여 레이어 간의 구분을 시각적으로 전달하고 사람들이 장소감을 유지할 수 있도록 도와줍니다. 반투명도를 높이기 위해 Material 특성을 생동감과 같이 사용 할 수 있습니다. 생동감은 소재의 뒤쪽에서 색상을 앞으로 당겨 텍스트, 기호 및 채우기와 같은 전경 콘텐츠의 깊이감을 증폭시킵니다.


> 참고
> 생동감은 모든 앱과 게임, 심지어 생동감 을 지원하는 UI를 표시하지 않는 앱과 게임에도 영향을 미칠 수 있습니다. macOS의 menu, 비전OS의 window, iOS의 labels과 같은 일부 구성 요소는 기본적으로 생동감이 있으므로 생동감은 모든 앱과 게임에 영향을 미칠 수 있습니다.

## Best practices

시스템은 밝고 어두운 외관에 자동으로 적응할 수 있는 여러 가지 Material 특성을 제공합니다. 또한 시스템에서 제공하는 흐림 및 생동감 효과를 UI 컴포넌트에 적용하여 Material 특성과 잘 통합되고 원하는 눈에 잘 띄도록 할 수 있습니다. 시스템에서 정의한 Material 특성과 효과를 사용하면 앱이나 게임에 일관된 시각적 요소를 부여하고 사용자가 앱 간에 전환할 때 부드러운 전환을 만들 수 있습니다.

- #### 맥락과 권장 사용법에 따라 시스템 Material 특성 및 효과를 선택하세요.
시스템 설정에 따라 인터페이스의 모양과 동작이 달라질 수 있으므로 Material 이나 효과가 인터페이스에 부여하는 겉으로 보이는 색을 기준으로 선택하지 마세요. 대신 특정 사용 사례에 맞게 Material 특성 또는 생동감 스타일을 일치시키세요. 예를 들어, 비전OS 앱의 대화형 구성 요소를 강조하려면 밝은 Material 특성을 사용하고, macOS 앱의 메뉴에는 [menu](https://developer.apple.com/documentation/appkit/nsvisualeffectview/material/menu) Material 특성을, iOS 앱의 기본 레이블에는 [label](https://developer.apple.com/documentation/uikit/uivibrancyeffectstyle/label) 생동감 스타일을, tvOS 앱의 적응형 전체 화면 배경에는 [prominent](https://developer.apple.com/documentation/uikit/uiblureffect/style/prominent) Material 특성을 사용하세요.

- #### Material 특성 위에 강조 색상을 사용하여 가독성을 높일 수 있습니다.
시스템에서 정의한 생생한 색상을 사용하면 다양한 상황에서 색상이 너무 어둡거나, 밝거나, 채도가 높거나, 대비가 낮게 보일까 걱정할 필요가 없습니다. 예를 들어, iOS에서는 텍스트, 채우기, 기호 및 구분 기호에 대해 동적 시스템 색상을 정의하여 반투명 배경에서 이러한 항목이 멋지게 보이도록 합니다. macOS에서는 모든 표준 시스템 색상에 생생한 버전이 있습니다. 비전OS에서는 macOS에서 사용하는 것과 동일한 어둡고 생생한 색상을 사용하여 다양한 시각적 컨텍스트에서 대비를 유지하도록 자동으로 조정합니다. 자세한 지침은 [색상](https://developer.apple.com/design/human-interface-guidelines/color)을 참조하세요.

- #### 흐림 및 생동감 효과와 결합할 Material을 선택할 때는 대비와 시각적 분리를 고려하세요. 

예를 들어 다음과 같이 생각해 보세요:

두꺼운 Material 특성은 텍스트 및 미세한 특징이 있는 기타 요소에 더 나은 대비를 제공할 수 있습니다.

반투명은 배경에 있는 콘텐츠를 눈에 잘 띄게 하여 사람들이 맥락을 유지하는 데 도움이 될 수 있습니다.

시스템에서는 콘텐츠를 방해하지 않으면서 깊이감과 계층 구조를 전달하는 데 사용할 수 있는 여러 가지 Material 특성을 제공합니다. 일부 Material은 다크/라이트 모드에 맞게 조정되며 일부 Material은 항상 밝거나 항상 어둡습니다. 어떤 재질을 선택하든 그 위에 생동감 없는 색상을 사용하지 않는 것이 좋습니다.

개발자 지침은 [UIBlurEffect.Style](https://developer.apple.com/documentation/uikit/uiblureffect/style)을 참조하십시오.

### 플랫폼별 고려사항

### iOS, iPadOS

iOS 및 iPadOS는 각 Material에 맞게 특별히 설계된 레이블, 채우기 및 구분 기호에 대한 생동감 값을 정의하며, 표준 시스템 색상은 생동감(vibrant) 버전으로 제공되지 않습니다.

레이블과 색상 채우기 요소는 각각 여러 단계의 생동감을 제공하며 구분선은 한 단계의 생동감을 제공합니다. 레벨의 이름은 요소와 배경 사이의 상대적인 대비 정도를 나타냅니다: 기본 수준은 대비가 가장 높은 반면, 4번째 단계(존재하는 경우)는 대비가 가장 낮습니다.

4번째 단계를 제외한 모든 자료의 레이블에 다음 생동감 값을 사용할 수 있습니다. 일반적으로 얇거나 매우 얇은 재질에는 대비가 너무 낮으므로 4번째 단계를 사용하지 않는 것이 좋습니다.

1. [UIVibrancyEffectStyle.label](https://developer.apple.com/documentation/uikit/uivibrancyeffectstyle/label) (기본 값)

2. [UIVibrancyEffectStyle.secondaryLabel](https://developer.apple.com/documentation/uikit/uivibrancyeffectstyle/secondarylabel)

3. [UIVibrancyEffectStyle.tertiaryLabel](https://developer.apple.com/documentation/uikit/uivibrancyeffectstyle/tertiarylabel)

4. [UIVibrancyEffectStyle.quaternaryLabel](https://developer.apple.com/documentation/uikit/uivibrancyeffectstyle/quaternarylabel)

모든 Material 특성의 색상 채우기 요소에 다음 vibrant(강조) 색상값을 사용할 수 있습니다.

1. [UIVibrancyEffectStyle.fill](https://developer.apple.com/documentation/uikit/uivibrancyeffectstyle/fill) (기본 값)

2. [UIVibrancyEffectStyle.secondaryFill](https://developer.apple.com/documentation/uikit/uivibrancyeffectstyle/secondaryfill)

3. [UIVibrancyEffectStyle.tertiaryFill](https://developer.apple.com/documentation/uikit/uivibrancyeffectstyle/tertiaryfill)

시스템은 모든 Material 특성에서 어울리는 구분자(separator)에 사용하기 위한 기본 vibrant 값을 제공합니다.

### macOS

macOS는 모든 표준 색상의 생생한 버전을 제공하며, 인터페이스에 적용되는 반투명도, 흐림 및 생동감의 정도를 정의하는 Material을 제공합니다. 시스템에서는 각각 지정된 용도가 있는 여러 가지 표준 재질을 제공합니다. 예를 들어 창, 메뉴, 팝오버, 사이드바, 제목 표시줄 등의 기본 모양과 일치하는 재질을 선택할 수 있습니다. 개발자 가이드는 [NSVisualEffectView.Material](https://developer.apple.com/documentation/appkit/nsvisualeffectview/material)을 참조하세요.


| 라이트 모드                                                                                                                | 다크 모드                                                                                                                 |
| -------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| ![The sidebar, window background, and selection materials display different amounts of transparency and blending in a light appearance.](https://docs-assets.developer.apple.com/published/904108c5cb735b367707dc286d473417/macos-light-appearance@2x.png) | ![The sidebar, window background, and selection materials display different amounts of transparency and blending in a dark appearance.](https://docs-assets.developer.apple.com/published/dbf9234c84a8b4193936b2336a2b9165/macos-dark-appearance@2x.png) |



#### 사용자 지정 보기 및 제어에서 생동감(vibrant)을 허용할 시기를 선택하세요.
 구성 및 시스템 설정에 따라 시스템 보기 및 컨트롤은 vibrant을 사용하여 전경 콘텐츠를 어떤 배경에서도 돋보이게 합니다. 다양한 상황에서 인터페이스를 테스트하여 vibrant 요소가 언제 외관을 개선하고 사용자 경험을 향상 시키는지 확인해 보세요.

#### 인터페이스 디자인을 보완하는 배경 블렌딩 모드를 선택하세요. 
macOS는 배경 콘텐츠를 블렌딩하는 두 가지 모드, 즉 behind window / within window 을 정의합니다. 개발자 지침은 [NSVisualEffectBlendingMode](https://developer.apple.com/documentation/appkit/nsvisualeffectblendingmode)를 참조하십시오.

![](https://docs-assets.developer.apple.com/published/288b0f72176d3b99b5a453c0c51619e7/macos-behind-window-blending~dark@2x.png)

#### Behind window 블렌딩 모드

이 모드에서는 창 뒤의 콘텐츠가 표시되어 사람들이 앱이나 게임을 둘러싼 컨텍스트의 일부를 유지할 수 있습니다. 메뉴, 시트, 사이드바 등의 컴포넌트는 이 모드를 자동으로 사용합니다.


![](https://docs-assets.developer.apple.com/published/93a6509635727880b77d6d72863511e4/macos-in-window-blending~dark@2x.png)

#### In-window 블렌딩 모드

이 모드를 사용하면 창 콘텐츠를 다른 창 구성 요소를 통해 표시할 수 있습니다. 예를 들어, 툴바에서 이 모드를 사용하면 콘텐츠가 툴바 아래로 스크롤될 때 연속성을 느낄 수 있습니다.



https://developer.apple.com/design/human-interface-guidelines/materials#tvOS


### tvOS

#### 더 밝고 반투명한 소재를 사용하여 콘텐츠를 돋보이게 하고 신선한 느낌을 줄 수 있습니다.
어두운 Material은 그림자를 숨겨 깊이가 줄어들고 콘텐츠를 명확하게 구분하기 어렵게 만드는 경향이 있습니다. 더 무거운 느낌을 주거나 콘텐츠가 오래되었음을 암시하려는 경우 어두운 Material을 사용하는 것이 좋습니다.

예를 들어 다음과 같은 방식으로 시스템 자료를 사용하는 것을 고려해 보세요:


|Material|권장 |반응형 효과|
|---|---|---|
|Prominent|Full-screen 배경|라이트 모드에서는 밝은 material 효과를 제공하며, 다크 모드에서는 어두운 material 효과를 제공합니다.|
|Regular|화면 컨텐츠를 부분적으로 가리는 overlay 형태|라이트 모드에서는 밝은 material을, 다크 모드에서는 어두운 material을 표기합니다.|
|Extra light|밝은 색상 테마를 사용하는 full-screen 배경 |–|
|Light|밝은 색상 테마를 사용하며, 화면 컨텐츠를 부분적으로 가리는 overlay 형태|–|
|Extra dark|다크 색상 테마를 사용하는 full-screen 배경|–|
|Dark|다크 색상 테마를 사용하며, 화면 컨텐츠를 부분적으로 가리는 overlay 형태|–|

### visionOS

비전OS에서 window는 일반적으로 빛, 현재 환경, 가상 콘텐츠, 주변 사물이 잘 보이도록 하여 사용자가 중심을 잡을 수 있도록 도와주는 시스템 타입 재질(Material)인 유리를 사용합니다. 글라스는 배경색 정보의 범위를 제한하는 적응형 재질로, window가 앱 콘텐츠의 대비를 계속 제공하면서 사용자의 물리적 환경과 기타 가상 콘텐츠에 따라 더 밝아지거나 어두워질 수 있도록 합니다.


https://github.com/i-colours-u/Human-Interface-Guidelines-KR/assets/60260284/a7201d95-3098-4c1d-ac34-8de1d6298dfb

> 참고
> 비전OS에는 별도의 다크 모드 설정이 없습니다. 대신, Glass Material는 그 뒤에 있는 물체와 색상의 휘도에 따라 자동으로 조정됩니다.

### Window에 불투명한 색상을 사용하지 마세요.
불투명한 영역은 사람들의 시야를 가려서 답답함을 느끼게 하고 주변의 가상 및 실제 물체에 대한 인식을 떨어뜨릴 수 있습니다.

### 필요한 경우 앱에서 시각적 구분을 만들거나 상호 작용을 나타내는 데 도움이 되는 재질(Material)을 선택하세요.
사용자 지정 컴포넌트를 만들어야 하는 경우 시스템 Material을 지정해야 할 수도 있습니다. 다음 예시를 참고하세요.

- 밝은 소재는 버튼이나 선택한 항목과 같은 인터랙티브 요소에 주의를 집중시킵니다.
- 어두운 머티리얼은 사이드바 또는 그룹화된 테이블 보기와 같이 앱의 섹션을 시각적으로 구분하는 데 도움이 될 수 있습니다.
- 가장 어두운 머티리얼은 텍스트 필드와 같은 구성 요소에 텍스트 입력을 허용하는 영역임을 나타내는 오목한 모양을 줄 수 있습니다.

> 참고
>비전OS 앱은 흰색 텍스트도 사용하지만 기본적으로 밝은 색상의 콘텐츠를 사용합니다.


전경(foreground) 콘텐츠가 Material 위에 표시될 때 가독성을 유지하기 위해 비전OS는 텍스트, 기호 및 색상 채우기 요소에 생동감을 적용합니다. 생동감은 가상 환경과 실제 환경 모두에서 빛과 색을 앞으로 끌어내어 깊이감을 향상시킵니다.

비전OS는 텍스트, 심볼, 채우기의 계층 구조를 전달하는 데 도움이 되는 세 가지 생동감 값을 정의합니다.

- 표준 텍스트에는 [`UIVibrancyEffectStyle.label`](https://developer.apple.com/documentation/uikit/uivibrancyeffectstyle/label)을 사용합니다.
- 각주 및 자막과 같은 설명 텍스트에는 [`UIVibrancyEffectStyle.secondaryLabel`](https://developer.apple.com/documentation/uikit/uivibrancyeffectstyle/secondarylabel)을 사용합니다.
- 텍스트의 가독성이 높을 필요가 없는 경우에만 비활성 요소에 [`UIVibrancyEffectStyle.tertiaryLabel`](https://developer.apple.com/documentation/uikit/uivibrancyeffectstyle/tertiarylabel)을 사용합니다.

### watchOS

### Material을 사용하여 전체 화면 모달 보기에서 컨텍스트를 제공하세요. 
전체 화면 모달 보기는 watchOS에서 일반적이므로 Material 레이어가 제공하는 대비를 통해 앱에서 사용자의 방향을 파악하고 컨트롤 및 시스템 요소를 다른 콘텐츠와 구분할 수 있습니다. 모달 시트의 Material 배경이 기본적으로 제공되는 경우 제거하거나 바꾸지 마십시오.

---

### 관련 문서

[Color](./color.md)
[Accessibility](./Accessibility.md)


### 개발자 문서

[`Material`](https://developer.apple.com/documentation/SwiftUI/Material) — SwiftUI
[`UIVisualEffectView`](https://developer.apple.com/documentation/uikit/uivisualeffectview) — UIKit
[`NSVisualEffectView`](https://developer.apple.com/documentation/appkit/nsvisualeffectview) — AppKit


### 관련 영상

| What's New in iOS Design |
| ------------------------ |
|     ![](https://devimages-cdn.apple.com/wwdc-services/images/48/0F960683-D91F-4CA9-9658-6FBB11F0683D/3272_wide_250x141_1x.jpg)                     |

