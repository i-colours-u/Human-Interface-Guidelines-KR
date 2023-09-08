
https://developer.apple.com/design/human-interface-guidelines/icons

## 아이콘을 효과적으로 사용한다면, 특정 단일 개념을 사람들에게 효과적으로 전달 할 수 있게 됩니다.



![A sketch of the Command key icon. The image is overlaid with rectangular and circular grid lines and is tinted yellow to subtly reflect the yellow in the original six-color Apple logo.](https://docs-assets.developer.apple.com/published/e71f139e5e50d9d10d91830b0af405c1/foundations-icons-intro@2x.png)


  
앱과 게임은 사람들이 선택할 수 있는 항목, 동작 및 모드를 이해하는 데 도움이 되는 다양한 간단한 아이콘을 사용합니다. [앱 아이콘](./App-icons.md)은 앱의 개성을 나타내기 위해 그림자, 질감 및 강조와 같은 풍부한 시각적 세부 정보를 사용할 수 있지만, 인터페이스 아이콘은 일반적으로 간결한 모양과 색상의 터치를 사용하여 명확한 개념을 전달합니다.

인터페이스 아이콘 또는 글리프 또는 템플릿 이미지라고도 하는 것을 디자인하거나 SF Symbols 앱에서 심볼을 선택하여 필요에 맞게 사용하거나 사용자 정의할 수 있습니다. 인터페이스 아이콘과 심볼 모두 그림자를 정의하기 위해 검은 색과 투명한 색을 사용하며, 시스템은 각 이미지의 검은 영역에 다른 색상을 적용할 수 있습니다. 자세한 내용은 [SF Symbols](https://developer.apple.com/design/human-interface-guidelines/sf-symbols)를 참조하십시오.

## Best practices
### - 인식하기 쉽고, 간결한 디자인을 사용하세요.
너무 많은 디테일은 인터페이스 아이콘을 혼란스럽거나 읽기 어렵게 만들 수 있습니다. 대부분의 사람들이 빠르게 인식할 수 있는 간단하고 보편적인 디자인을 지향해야 합니다. 일반적으로, 아이콘은 그들이 시작하는 동작이나 표현하려는 내용과 직접적으로 관련된 익숙한 시각적 비유를 사용할 때 가장 잘 작동합니다.

### - 앱의 모든 인터페이스 아이콘에서 시각적 일관성을 유지하세요. 
사용자 정의 아이콘만 사용하든지 사용자 정의 아이콘과 시스템 제공 아이콘을 혼합하든지, 앱의 모든 인터페이스 아이콘은 일관된 크기, 디테일 수준, 선 굵기(또는 무게) 및 원근법을 사용해야 합니다. 아이콘의 시각적 무게에 따라 다른 아이콘과 시각적으로 일관되게 보이도록 아이콘의 크기를 조정하는 것을 권장합니다.


| ![Diagram of four glyphs in a row. From the left, the glyphs are a camera, a heart, an envelope, and an alarm clock. Two horizontal dashed lines show the bottom and top boundaries of the row and a horizontal red line shows the midpoint. All four glyphs are solid black; some include interior detail lines in white. Parts of the alarm clock extend above the top dashed line because its lighter visual weight requires greater height to achieve balance with the other glyphs.](https://docs-assets.developer.apple.com/published/e879a59791ad2a7f010a675cb1e91294/custom-icon-sizes@2x.png) | ![Diagram of the same four glyphs shown above and the same horizontal dashed lines at top and bottom and horizontal red line through the middle. In this diagram, all four glyphs are solid gray; the interior detail lines are black to emphasize that all lines use the same weight.](https://docs-assets.developer.apple.com/published/88adc00800efc1523a27779b952ab348/custom-icon-line-weights@2x.png) |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 시각적 일관성을 유지하기 위해, 필요한 대로 개별 아이콘 크기를 조정해주세요.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | 같은 weight의 선(stroke)를 사용해서 아이콘을 구성해주세요.                                                                                                                                                                                                                                                                                                                                                  |



### - 일반적으로, 인터페이스 아이콘과 인접한 텍스트의 두께를 일치시켜주세요. 
아이콘 또는 텍스트 중 어느 하나를 강조하려는 경우가 아니라면, 둘 다 동일한 두께를 사용하면 컨텐츠가 일관된 UI와 일관된 강조 수준을 유지할 수 있습니다.

### - 필요한 경우, 사용자 정의 인터페이스 아이콘에 패딩을 추가하여 시각적 정렬을 유지하세요.
특히 비대칭적인 아이콘 중 일부는 기하학적인 중심으로 정렬하는 대신, 시각적으로 중심 정렬하는 것이 더 균형잡힌 모습을 보일 수 있습니다. 예를 들어 아래에 나온 다운로드 아이콘은 아래쪽에 시각적 무게가 더 많기 때문에 기하학적인 중심으로 정렬하는 대신 시각적으로 중심 정렬하는 것이 좋습니다.


![Two images of a white arrow that points down to a white horizontal line segment within a black disk. The image on the right includes two horizontal pink bars — one between the top of the glyph and the top of the disk and the other between the bottom of the glyph and the bottom of the disk — that show the glyph is geometrically centered within the disk.](https://docs-assets.developer.apple.com/published/1c13eed753a1ebcfd6d35929738476c7/asymmetric-glyph@2x.png)

_비대칭적인 아이콘은 중심에 위치한 것처럼 보일 수 있지만 실제로 그렇지 않을 수도 있습니다._

이러한 경우에는 아이콘의 위치를 약간 조정하여 시각적으로 중심에 위치하도록 할 수 있습니다. 아이콘 주위를 패딩으로 조정해서 (하단 오른쪽에 표시된 아이콘과 같이), 이 아이콘을 기하학적으로 중심 정렬하여 시각적으로 중앙에 배치할 수 있습니다.


![Two images of a white arrow that points down to a white horizontal line segment within a black disk. The image on the left includes the two horizontal pink bars in the same locations as in the previous illustration, but the glyph has been moved up by a few pixels. The image on the right includes a pink rectangle overlaid on top of the glyph to represent a padding area, which includes the extra pixels below the glyph.](https://docs-assets.developer.apple.com/published/c31bce31456820badff997c95db264c6/asymmetric-glyph-optically-centered@2x.png)

_아이콘을 약간 더 위로 몇 픽셀 이동하면 시각적으로 중심에 위치시킬 수 있으며, 패딩에 포함된 픽셀은 중앙 정렬을 쉽게 할 수 있도록 도와줍니다._

시각적 중앙 정렬을 위한 조정은 일반적으로 매우 작고, 사소 할 수 있지만, 앱의 외관에 큰 영향을 미칠 수 있습니다.

![Two images of a white arrow that points down to a white horizontal line segment within a black disk. The glyph on the left is geometrically centered and the one on the right is optically centered.](https://docs-assets.developer.apple.com/published/5d9da37476ee3225a29ce3efbfd86cac/asymmetric-glyph-before-and-after@2x.png)
_왼쪽이 before, 오른쪽이 after 아이콘 예시입니다._


### - 인터페이스 아이콘의 선택된 상태는(selected) 필요한 경우에만 제공하세요. 
선택 상태를 자동으로 표시하는 컨트롤 및 영역에 사용되는 아이콘에 대해 selected / unselected 상태를 별도로 제공할 필요는 없습니다. 예를 들어, visionOS 및 iOS의 사이드바 및 탭 바, 그리고 macOS의 툴바는 앱의 강조 색상을 적용하거나 배경 외관을 추가하여 자동으로 선택 상태를 나타낼 수 있습니다.

| ![Two images of a white glyph within a solid rounded rectangle shape. The glyph shows a heart above two horizontal left-aligned lines. On the left, the rounded rectangle is blue; on the right, it’s gray.](https://docs-assets.developer.apple.com/published/be9e174b3988f2938cee0d1233ac976d/selected-deselected-right-2@2x.png) | ![Two images of an envelope glyph. On the left, the glyph uses an almost black stroke and appears within a gray rounded rectangle shape. On the right, the glyph uses a dark gray stroke.](https://docs-assets.developer.apple.com/published/001cf4adccc467ed87102eca849b27b1/selected-deselected-right-1@2x.png) |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| iOS에서는 탭바 아이콘의 선택 상태는 app 자체의 accent color를 사용합니다.                                                                                                                                                                                                                                                           | macOS에서는 selected 상태의 아이콘은 자동으로 어두운 스트로크와, 어두운 백그라운드 색상을 적용합니다                         

iOS 또는 visionOS의 툴바나 네비게이션 바에서 selected / unselected 아이콘을 직접 제공하려고 할 수 있지만, 상태에 따라 배경 외관이 변경되는 버튼을 사용하는 것이 더 일반적입니다.

### - 포괄적인 디자인을 만드세요. 
특정 성별에 대한 불필요한 참조 없이 인간 모습을 그리는 것을 선호하고, 아이콘이 모든 사람에게 환영받고 이해하기 쉬운 것이 중요합니다. 지침을 위해서 [inclusion](./Inclusion.md) 문서를 참조하세요.


### - 의미 전달에 필수적인 경우가 아니라면 디자인에 텍스트를 포함하지 마세요. 
예를 들어, 텍스트 서식을 나타내는 인터페이스 아이콘에 문자를 사용하는 것은 개념을 가장 직접적으로 전달하는 방법일 수 있습니다. 아이콘에 개별 문자를 표시해야 하는 경우, 지역화(localize)해야 합니다. 텍스트의 일부를 나타내야 하는 경우, 추상적인 표현을 디자인하고, 오른쪽에서 왼쪽으로(아랍권에서는 텍스트가 오른쪽에서 왼쪽) 환경일 때 사용할 반전된 아이콘을 포함하세요. 지침을 위해서 [Right to left](https://developer.apple.com/design/human-interface-guidelines/right-to-left)을 참조하세요.

#### 예시
| ![A partial screenshot of the SF Symbols app showing the info panel for the character symbol, which looks like the capital letter A. Below the image, the following seven localized versions of the symbol are listed: Latin, Arabic, Hebrew, Hindi, Japanese, Korean, and Thai.](https://docs-assets.developer.apple.com/published/370ee6f0af700e77278bee88e4a934b5/character-in-glyph@2x.png) | ![A partial screenshot of the SF Symbols app showing the info panel for the doc dot plaintext symbol, which looks like three left-aligned horizontal lines inside a rounded rectangle. Below the image, the left-to-right and right-to-left localized versions are shown.](https://docs-assets.developer.apple.com/published/6c9e4d5aaf8ef75e31c7ea322a370a1f/abstract-text-in-glyph@2x.png) |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 각 나라에 맞는 문자 아이콘을 사용할 수 있습니다.                                                                                                                                                                                                                                                                                                                                           | 문서 아이콘을 사용할 때, RTL(Right to Left), LTR(Left to right)에 따라 아이콘이 달라질 수 있습니다.



### - 사용자 정의 인터페이스 아이콘을 만들 때는 PDF 또는 SVG와 같은 벡터 형식을 사용하세요.
시스템은 벡터 기반의 인터페이스 아이콘을 고해상도 디스플레이에 자동으로 크기 조정하므로 고해상도 버전을 제공할 필요가 없습니다. 반면, 그림자, 질감 및 강조 효과와 같은 효과를 포함하는 앱 아이콘 및 기타 이미지에 사용되는 PNG는 크기 조정을 지원하지 않으므로 각 PNG 기반 인터페이스 아이콘에 대해 여러 버전을 제공해야 합니다. 또는 사용자 정의 SF Symbol을 만들고 해당 심볼의 강조가 인접 텍스트와 일치하도록 크기를 지정할 수 있습니다. 지침을 위해서 [SF Symbols](https://developer.apple.com/design/human-interface-guidelines/sf-symbols)을 참조하세요.

사용자 정의 인터페이스 아이콘에 대체 텍스트 레이블을 제공하세요. 대체 텍스트 레이블 또는 접근성 설명은 보이지 않지만 VoiceOver를 통해 화면 상에 있는 내용을 음성으로 설명하므로 시각 장애가 있는 사람들에게 내비게이션을 간편하게 만들어줍니다. 자세한 내용은 [Content descriptions](https://developer.apple.com/design/human-interface-guidelines/accessibility#Content-descriptions)을 참조하세요.

Apple 하드웨어 제품 모양을 사용한 아이콘을 사용하지 않도록 하세요. 하드웨어 디자인은 자주 변경되며 인터페이스 아이콘 및 기타 콘텐츠가 오래된 것처럼 보이게 할 수 있습니다. Apple 하드웨어를 표시해야 하는 경우 [Apple Design Resources](https://developer.apple.com/design/resources/) 또는 다양한 Apple 제품을 나타내는 SF Symbols에서 제공되는 이미지만 사용하세요.

## 플랫폼별 고려사항

- iOS, iPadOS, tvOS, visionOS, watchOS에 대한 특별한 고려사항은 없습니다.

## macOS
만약 macOS 앱에서 사용자 정의 문서 유형을 사용할 수 있다면, 해당 문서를 나타내는 문서 아이콘을 만들 수 있습니다. 전통적으로, 문서 아이콘은 오른쪽 위 구석이 접힌 종이 조각처럼 보입니다. 이 독특한 외관은 아이콘 크기가 작은 경우에도 사람들이 문서를 앱 및 다른 콘텐츠와 구별할 수 있도록 도와줍니다.

지원하는 파일 유형에 대한 문서 아이콘을 제공하지 않는 경우, macOS는 앱 아이콘과 파일의 확장자를 캔버스 위에 합성하여 자동으로 문서 아이콘을 생성합니다. 예를 들어, Preview는 JPG 파일을 나타내기 위해 시스템에서 생성한 문서 아이콘을 사용합니다.
![An image of the Preview document icon for a JPG file.](https://docs-assets.developer.apple.com/published/4d2bb68768914a965a16d08842109013/doc-icon-generated@2x.png)


어떤 경우에는 앱이 처리하는 파일 유형 범위를 나타내기 위해 일련의 문서 아이콘 세트를 만드는 것이 유용할 수 있습니다. 예를 들어, Xcode는 프로젝트, AR 객체 및 Swift 코드 파일을 구별하는 데 도움을 주기 위해 사용자 정의 문서 아이콘을 사용합니다.


| ![Image of an Xcode project document icon.](https://docs-assets.developer.apple.com/published/8094308ae64abe362b2b5fb9ba971adc/doc-icon-custom-1@2x.png) | ![Image of a document icon for an AR object.](https://docs-assets.developer.apple.com/published/268405d8ea0825a3ac4cebaa50314d24/doc-icon-custom-2@2x.png) | ![Image of a document icon for a Swift file.](https://docs-assets.developer.apple.com/published/fa7a4c636ef449243f13f1cbd3324838/doc-icon-custom-3@2x.png) |
| -------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
|                                                                                                                                                          |                                                                                                                                                            |                                                                                                                                                            |



사용자 정의 문서 아이콘을 만들려면 배경 채우기 / 중앙 이미지 / 텍스트의 조합을 사용할 수 있습니다. macOS 11부터 시스템은 이러한 요소들을 필요한 대로 레이어링하고 위치시키며 마스크를 적용하며, 이를 시스템 아이콘과 비슷하게 구석이 접힌 문서 아이콘 모양 위에 합성합니다.

| ![](https://docs-assets.developer.apple.com/published/2aed446834a2dc6e8275b6bd7a797ca9/doc-icon-parts-background-fill@2x.png) |  ![](https://docs-assets.developer.apple.com/published/b59c836903d1b409ab9e21f81762df3e/doc-icon-parts-center-image@2x.png) |  ![](https://docs-assets.developer.apple.com/published/b132452b7a66fabbfafc6461763cc179/doc-icon-parts-text~dark@2x.png) |
|--|--|--|
| 배경색 채우기| 중앙에 이미지 배치하기 | 텍스트 |



![A custom document icon that displays the pink heart and the word heart on top of the pink grid and white EKG line.](https://docs-assets.developer.apple.com/published/d56b7712318a95ad77f000c052a852aa/doc-icon-parts@2x.png)

macOS 11은 제공한 요소들을 결합하여 사용자 정의 문서 아이콘을 생성합니다.

[Apple Design Resources](https://developer.apple.com/design/resources/#macos-apps)는 문서 아이콘을 만들기 위해 사용할 수 있는 배경 채우기 및 중앙 이미지를 만들기 위한 템플릿을 제공합니다. 이 템플릿을 사용하면 아래의 지침을 따를 수 있습니다.

### - 문서 유형을 명확하게 전달하는 간단한 이미지를 디자인하세요.
배경 채우기, 중앙 이미지를 둘 다 사용하더라도, 복잡하지 않은 형태와 구분되는 색상 팔레트를 선호하세요. 문서 아이콘은 최소한 16x16 픽셀 크기로 표시될 수 있으므로 모든 크기에서 인식할 수 있는 디자인을 만들어야 합니다.

### - 배경 채우기 및 표현력 있는 이미지를 사용해 문서 아이콘을 디자인하는 것은 문서 유형을 이해하고 인식하는 데 큰 도움이 될 수 있는 방법입니다. 
예를 들어, Xcode와 TextEdit은 center 이미지를 포함하지 않는 풍부한 배경 이미지를 사용합니다.




| ![Image of an Xcode project document icon.](https://docs-assets.developer.apple.com/published/8094308ae64abe362b2b5fb9ba971adc/doc-icon-custom-1@2x.png) | ![Image of a TextEdit rich text document icon.](https://docs-assets.developer.apple.com/published/f32709a5ff5742e79fd03a58ae1dd9c6/doc-icon-fill-only@2x.png) |
| -------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|                                                                                                                                                          |                                                                                                                                                               |

문서 아이콘의 작은 버전에서 복잡도를 줄이는 것을 고려하세요. 큰 버전에서 명확한 아이콘 세부사항이 작은 버전에서는 흐릿하게 보이고 인식하기 어려울 수 있습니다. 예를 들어, 사용자 정의 하트 문서 아이콘의 그리드 라인이 중간 크기에서 명확하게 유지되도록 하려면 더 적은 라인을 사용하고 픽셀 그리드를 축소된 크기에 맞춰 두껍게 만들 수 있습니다. 16x16 픽셀 크기에서는 라인을 완전히 제거할 수도 있습니다.

| ![](https://docs-assets.developer.apple.com/published/1f8bc7946a75363224f373924b557a3a/doc-icon-fewer-details-1@2x.png) |  ![](https://docs-assets.developer.apple.com/published/e46ac887801d9a16393948c3f2098715/doc-icon-fewer-details-2@2x.png)  |  ![](https://docs-assets.developer.apple.com/published/fd0d2afcd76a9b25c1217ef2ffb1ad0e/doc-icon-fewer-details-3@2x.png) |
|--|--|--|
| 32x32 픽셀 아이콘은 더 적은 그리드 라인과 더 두꺼운 EKG 라인을 가지고 있습니다. | 16x16 픽셀 @2x 아이콘은 EKG 라인을 유지하지만 그리드 라인은 없습니다.  | 16x16 픽셀 @1x 아이콘은 EKG 라인과 그리드 라인이 없습니다. |

> EKG 라인 : 심전도 그래프 (예시에서 사용하고 있는 그래프 모양)

### - 중요한 내용을 배경 채우기의 오른쪽 상단 구석에 배치하지 않도록 해야 합니다. 
시스템은 이미지를 자동으로 문서 아이콘 모양에 맞게 마스크하고, 흰색으로 접힌 모서리를 배경 위에 그립니다. 다음 크기의 배경 이미지 세트를 생성하세요.

- 512x512 px @1x, 1024x1024 px @2x
- 256x256 px @1x, 512x512 px @2x
- 128x128 px @1x, 256x256 px @2x
- 32x32 px @1x, 64x64 px @2x
- 16x16 px @1x, 32x32 px @2x

### - 만약 익숙한 객체가 문서 유형이나 앱과의 연결을 나타낼 수 있다면, 해당 객체를 나타내는 중앙 이미지를 만들어보세요. 
모든 크기에서 명확하고 인식하기 쉬운 간단하고 명확한 이미지를 디자인하세요. 중앙 이미지는 전체 문서 아이콘 캔버스의 반 크기를 가집니다. 예를 들어, 32x32 px 문서 아이콘에 대한 중앙 이미지를 만들려면 16x16 px 크기의 이미지 캔버스를 사용하세요. 중앙 이미지는 다음 크기로 제공할 수 있습니다.

- 256x256 px @1x, 512x512 px @2x
- 128x128 px @1x, 256x256 px @2x
- 32x32 px @1x, 64x64 px @2x
- 16x16 px @1x, 32x32 px @2x

이미지 캔버스의 약 10%를 측정하는 여백을 정의하고 대부분의 이미지를 여백 내에 유지하세요. 시각적 정렬을 위해 이미지의 일부가 이 여백으로 확장될 수 있지만 이미지가 이미지 캔버스의 약 80%를 차지할 때 가장 좋습니다. 예를 들어, 256x256 px 캔버스의 중앙 이미지의 대부분은 205x205 px 크기의 영역에 맞을 것입니다.


![Diagram of the solid pink heart shape within blue margins that measure 10 percent of the canvas width.](https://docs-assets.developer.apple.com/published/04bd3e5a8003adb03e8c39634700c4cb/doc-icon-parts-margins@2x.png)


### - 만약 사람들이 문서 유형을 이해하는 데 도움이 되는 간결한 용어가 있다면 명시하세요.
기본적으로 시스템은 문서 아이콘의 하단 가장자리에 문서의 확장자를 표시하지만, 확장자가 익숙하지 않다면 더 구체적인 용어를 제공할 수 있습니다. 예를 들어, SceneKit 씬 파일의 문서 아이콘은 파일 확장자 scn 대신 scene이라는 용어를 사용합니다. 시스템은 확장자 텍스트를 자동으로 문서 아이콘에 맞게 크기 조정하므로 작은 크기에서도 가독성이 있는 충분히 짧은 용어를 사용하세요. 기본적으로 시스템은 텍스트의 모든 글자를 대문자로 표시합니다.

![Image of a SceneKit scene document icon.](https://docs-assets.developer.apple.com/published/c0b6383ac5c8bf64952799ebca9b950c/doc-icon-custom-extension@2x.png)

---

### 관련 문서

- [App icons](https://developer.apple.com/design/human-interface-guidelines/app-icons)
- [SF Symbols](https://developer.apple.com/design/human-interface-guidelines/sf-symbols)


### 영상
| [Designing Glyphs](https://developer.apple.com/videos/play/wwdc2017/823) |
| ------------------------------------------------------------------------ |
|    ![](https://devimages-cdn.apple.com/wwdc-services/images/7/597D59A1-F123-4B08-BEE1-6D79A4C22268/1914_wide_250x141_1x.jpg)                                                                      |

