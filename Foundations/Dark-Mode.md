# Dark Mode

다크 모드는 어두운 색상 팔레트를 사용하여 저조도 환경에 맞는 편안한 시청 환경을 제공하는 시스템 설정입니다.![A sketch of concentric circles with half-filled areas, suggesting the presence of light and dark. The image is overlaid with rectangular and circular grid lines and is tinted yellow to subtly reflect the yellow in the original six-color Apple logo.](https://docs-assets.developer.apple.com/published/f354bd96f1890df83e7f8e31835f80bc/foundations-dark-mode-intro@2x.png)

iOS, iPadOS, macOS 및 tvOS에서 사람들은 기본 인터페이스 스타일로 다크 모드를 선택하는 경우가 많으며, 일반적으로 모든 앱과 게임이 다크 모드에 대응하기를 기대합니다. 다크 모드에서는 모든 화면, 보기, 메뉴 및 컨트롤에 어두운 색상 팔레트를 사용하며, 어두운 배경에서 메인 콘텐츠를 돋보이게 하기 위해 더 큰 배경 대비를 사용할 수도 있습니다.


## Best practices

### - 앱 내에서 모드(라이트/다크) 설정을 제공하지 마세요.
앱내에서 모드 옵션을 제공하면, 사용자들은  원하는 스타일을 세팅하기 위해 두 가지 이상의 설정을 조정해야 하므로 사용자에게 더 많은 작업을 유발합니다. 더 나쁜 것은 시스템 전체에서 선택한 모드에 반응하지 않아 앱이 고장났다고 생각할 수 있다는 것입니다.

- ### 앱이 두 가지 모드(라이트/다크) 모두에서 보기 좋게 표시되는지 확인하세요. 
단순히 다크/라이트 모드를 사용하는 것 외에도, 하루 종일 또는 앱이 실행되는 동안 조건이 변할 때 밝게 또는 어둡게 표시되도록 전환하는 자동 표시 설정을 선택할 수 있습니다.

- ### 콘텐츠를 테스트하여 두 가지 표시 모드에서 모두 편안하게 읽을 수 있는지 확인합니다.
예를 들어, 다크 모드에서 대비 증가와 투명도 감소를 설정 했을 경우, 어두운 배경에 어두운 텍스트가 있을 때 가독성이 떨어지는 부분을 발견할 수 있습니다. 또한 다크 모드에서 대비 증가를 켜면 어두운 텍스트와 어두운 배경 사이의 시각적 대비가 감소할 수 있습니다. 시력이 좋은 사람은 여전히 대비가 낮은 텍스트를 읽을 수 있지만, 많은 사람이 이러한 텍스트를 읽을 수 없을 수도 있습니다. 자세한 내용은 [Color and effects(색상 및 효과)](https://developer.apple.com/design/human-interface-guidelines/accessibility#Color-and-effects)를 참조하세요.

### - 드문 경우지만 인터페이스에 어두운 UI만 사용하는 것도 고려해 보세요.
예를 들어, 몰입형 미디어 시청을 지원하는 앱의 경우 UI가 사라지고 사람들이 미디어에 집중할 수 있도록 영구적으로 어두운 UI 요소를 사용하는 것이 좋습니다.

## 다크 모드 색상

다크모드의 색상 팔레트에는 더 어두운 배경색과 더 밝은 메인 색이 포함되어 있습니다. 이러한 색상이 반드시 밝은 색상과 반전되는 것은 아니며, 반전되는 색상도 많지만 반전되지 않는 색상도 있다는 점을 알아두는 것이 중요합니다. 자세한 내용은 [Specifications](https://developer.apple.com/design/human-interface-guidelines/color#Specifications)을 참조하세요.

### - 현재 모양에 맞는 색상을 사용하세요. 
시맨틱 색상(예: macOS의 [`labelColor`](https://developer.apple.com/documentation/appkit/nscolor/1534657-labelcolor) 및 [`controlColor`](https://developer.apple.com/documentation/appkit/nscolor/1524856-controlcolor) 또는 iOS 및 iPadOS의 [`separator`](https://developer.apple.com/documentation/uikit/uicolor/3173139-separator))은 현재 모양에 맞게 자동으로 조정됩니다. 사용자 지정 색상이 필요한 경우 Xcode에서 앱의 에셋 카탈로그에 색상 세트 에셋을 추가하고 색상의 밝고 어두운 변형을 지정합니다. 하드 코딩된 색상 값이나 적응되지 않는 색상을 사용하지 마십시오.

### - 모든 UI요소에서 충분한 색상 대비를 목표로 합니다. 
시스템에서 정의한 색상을 사용하면 메인 컨텐츠와 배경 콘텐츠 간의 대비 비율을 적절하게 맞출 수 있습니다. 최소한 색상 간의 대비 비율이 4.5:1 이상이어야 합니다. 사용자 정의 메인 색상(foreground color)과 배경색의 경우, 특히 작은 텍스트의 경우 대비 비율이 7:1이 되도록 노력하세요. 이 비율은 메인 콘텐츠가 배경에서 눈에 잘 띄도록 하고 콘텐츠가 권장 접근성 가이드라인을 충족하는 데 도움이 됩니다.

### - 흰색 배경의 색상을 약간 어둡게 처리하세요. 
흰색 배경이 포함된 콘텐츠 이미지를 표시하는 경우 주변 다크 모드 상황에서 배경이 빛나지 않도록 이미지를 약간 어둡게 하는 것이 좋습니다.

## 아이콘 및 이미지

이 시스템은 다크 모드에 자동으로 적응하는 [SF Symbols](https://developer.apple.com/design/human-interface-guidelines/sf-symbols)과 밝은 곳과 어두운 곳 모두에 최적화된 풀컬러 이미지를 사용합니다.

### - 가능하면 SF 심볼을 사용하세요. 
심볼은 동적 색상을 사용하여 색조를 지정하거나 생동감을 더할 때 두 가지 모드(라이트/다크) 모두에서 잘 작동합니다. 지침은 [Color(색상)](https://developer.apple.com/design/human-interface-guidelines/color)을 참조하십시오.

### - 필요한 경우 라이트 모드와 다크 모드를 위한 인터페이스 아이콘을 별도로 디자인합니다. 
예를 들어 보름달을 나타내는 아이콘은 밝은 배경과 잘 대비되도록 미묘한 어두운 윤곽선이 필요하지만 어두운 배경에 표시할 때는 윤곽선이 필요하지 않을 수 있습니다. 마찬가지로 기름 한 방울을 나타내는 아이콘은 어두운 배경에서 가장자리가 잘 보이도록 약간의 테두리가 필요할 수 있습니다.

### - 풀컬러 이미지와 아이콘이 두 가지 모드 모두에서 잘 보이는지 확인하세요.
밝은 배경과 어두운 배경 모두에 잘 어울리는 경우 동일한 에셋을 사용합니다. 자산이 한 가지 모드에서만 잘 보이는 경우 이미지를 수정하거나 라이트 모드용 이미지와 다크 모드용 이미지를 별도로 만듭니다. 자산 카탈로그(asset catalogs)를 사용하여 이미지를 1개의 세트로 묶을 수 있습니다.

## 텍스트

이 시스템은 다크 모드에서 텍스트의 가독성을 유지하기 위해 생동감과 대비를 높입니다.

### - 시스템에서 제공하는 라벨 컬러를 사용합니다.
1~4 순위 (제목1,제목2,제목3,제목4) 레이블 색상은 밝고 어두운 배경에 따라 자동으로 조정됩니다.

### - 텍스트 뷰, 텍스트 필드를 사용할 때는 시스템 뷰를 활용하세요. 
시스템에서 제공하는 뷰 및 컨트롤을 사용하면 앱의 텍스트가 모든 배경에서 보기 좋게 표시되며, 생동감의 유무에 따라 자동으로 조정됩니다. 가능하면 텍스트 뷰를 직접 그리는 대신 시스템에서 제공하는 보기를 사용하여 텍스트를 표시하세요.

## 플랫폼 별 고려사항
- tvOS에는 해당사항이 없습니다.
- watchOS와 visionOS에는 다크모드가 없습니다.

## iOS, iPadOS

다크 모드에서는 어두운 인터페이스가 다른 인터페이스 위에 겹쳐져 있을 때 깊이감을 향상시키기 위해 기본 색상 (Base) 과 하이라이트 색상(Elevated) 이라는 두 가지 배경 색상 세트를 사용합니다. 기본 색상(Base)은 더 어둡기 때문에 배경 인터페이스가 뒤로 물러나는 것처럼 보이고, 하이라이트(Elevated) 색상은 더 밝기 때문에 전경 인터페이스가 앞으로 나아가는 것처럼 보입니다.


| 기본 색상(Base) | 하이라이트 색상(Elevated) | 라이트 모드 |
| ------ | -------- | -----|
| ![A diagram that shows a stack of 4 terms on top of a black background. The term at the top shows the most contrast with the background and the term at the bottom shows the least.](https://docs-assets.developer.apple.com/published/0d71ac9f5186541dce35b5f702311bd0/base-with-four-semantic-colors@2x.png) | ![A diagram that shows a stack of 4 terms on top of a nearly black background. The term at the top shows the most contrast with the background and the term at the bottom shows the least.](https://docs-assets.developer.apple.com/published/0dacc182adc819b08eb8cdcc897b08a4/elevated-with-four-semantic-colors@2x.png)|![A diagram that shows a stack of 4 terms on top of a white background. The term at the top shows the most contrast with the background and the term at the bottom shows the least.](https://docs-assets.developer.apple.com/published/cbbe9a39049fd3d3d2122876de64d207/light-with-four-semantic-colors@2x.png) |


### - 시스템 배경색을 사용하세요. 
다크 모드는 동적 모드이므로 팝오버나 모달 시트와 같이 인터페이스가 전면에 표시될 때 배경색이 기본에서 고조도로 자동 변경됩니다. 또한 멀티태스킹 환경에서 앱 간, 다중 창 환경에서 창 간 시각적 구분을 제공하기 위해 시스템에서 배경색을 높여서 사용합니다. 사용자 지정 배경색을 사용하면 사람들이 시스템에서 제공하는 이러한 시각적 구분을 인식하기 어려울 수 있습니다.

## macOS

일반 설정에서 강조 색상(graphite accent color)을 선택하면 macOS에서 창 배경이 현재 바탕 화면 사진의 색상을 선택하게 됩니다. 바탕 화면 색조라고 하는 이 효과는 창이 주변 콘텐츠와 더욱 조화롭게 어우러지도록 도와주는 미묘한 효과입니다.

### - 적절한 경우 사용자 지정 컴포넌트 배경에 투명도를 포함할 수 있습니다. 
투명도를 사용하면 바탕 화면 색조가 활성화되어 있을 때 구성 요소가 창 배경의 색상을 가져와 바탕 화면 그림이 변경되어도 시각적 조화를 유지할 수 있습니다. 이러한 조화를 이루려면 배경이나 베젤이 보이는 사용자 지정 컴포넌트에만 투명도를 추가하고 컴포넌트가 색상을 사용하지 않는 상태와 같이 중립 상태에 있을 때만 투명도를 추가하세요. 컴포넌트가 색상을 사용하는 상태일 때 투명도를 추가하면 창 배경이 바탕 화면의 다른 위치로 조정되거나 바탕 화면 그림이 변경될 때 컴포넌트의 색상이 변동될 수 있으므로 투명도를 추가하지 않으려는 것이 좋습니다.

## 연관 문서

- [Color](https://developer.apple.com/design/human-interface-guidelines/color)
- [Materials](https://developer.apple.com/design/human-interface-guidelines/materials)
- [Typography](https://developer.apple.com/design/human-interface-guidelines/typography)

## 연관 영상

| [What's New in iOS Design](https://developer.apple.com/videos/play/wwdc2019/808) | [Implementing Dark Mode on iOS](https://developer.apple.com/videos/play/wwdc2019/214) |
| ------ | ------ |
| ![](https://devimages-cdn.apple.com/wwdc-services/images/48/0F960683-D91F-4CA9-9658-6FBB11F0683D/3272_wide_250x141_1x.jpg) |  ![](https://devimages-cdn.apple.com/wwdc-services/images/48/174747D6-8723-4194-A932-7765179F1108/2949_wide_250x141_1x.jpg) |

