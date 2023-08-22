
## 모든 디바이스에서 아트워크 이미지가 사용자들에게 멋지게 보이도록 하기 위해 시스템에서 콘텐츠를 표시하는 방법과 적절한 배율로 아트워크를 제공하는 방법을 알아보세요.

![A sketch of a photo, suggesting imagery. The image is overlaid with rectangular and circular grid lines and is tinted yellow to subtly reflect the yellow in the original six-color Apple logo.](https://docs-assets.developer.apple.com/published/b0a68ac859ddb098858e92609997d307/foundations-images-intro@2x.png)

## 해상도

장치마다 해상도가 다른 이미지를 표시할 수 있습니다. 예를 들어 2D 디바이스는 화면의 해상도에 따라 이미지를 표시합니다.

point(단위)는 시각적 콘텐츠가 표시되는 방식에 관계없이 일관성을 유지하는 데 도움이 되는 추상적인 측정 단위입니다. 2D 플랫폼에서 포인트는 디스플레이의 해상도에 따라 달라질 수 있는 픽셀 수에 매핑되며, visionOS에서 point는 시청자와의 거리에 따라 시각적 콘텐츠의 크기를 조정할 수 있는 각도 값입니다.

생성한 이미지의 해상도를 식별하려면 배율을 지정합니다. 다양한 해상도의 2D 디스플레이에서 포인트당 픽셀 밀도를 고려하여 배율을 시각화할 수 있습니다. 예를 들어 @1x은 1:1 픽셀 밀도를 나타내며, 여기서 1픽셀은 하나의 포인트와 같습니다. 고해상도 2D 디스플레이는 2:1 또는 3:1과 같이 픽셀 밀도가 더 높습니다. @2x의 배율은 2이고, @3x의 배율은 3입니다. 픽셀 밀도가 높기 때문에 고해상도 디스플레이는 더 많은 픽셀을 가진 이미지를 요구합니다.

| 1x (10x10) px | 2x (20x2x px) | 3x (30x30 px) |
| ------------- | ------------- | ------------- |
|      ![Image of a circle that is in standard resolution at scale factor 1 and has 10 x 10 pixels.](https://docs-assets.developer.apple.com/published/a9b04545f30aff45ca503e263c02d464/image-resolution-1x@2x.png)         |     ![Image of a circle that is in high resolution at scale factor 2 and has 20 x 20 pixels.](https://docs-assets.developer.apple.com/published/cf203acc0ee6299833fb2e5b5c4a7348/image-resolution-2x@2x.png)          |      ![Image of a circle that is in high resolution at scale factor 3 and has 30 x 30 pixels.](https://docs-assets.developer.apple.com/published/0de9ee5144fc2278682eb211ac8f571d/image-resolution-3x@2x.png)         |


## 이미지 형식
다양한 유형의 이미지를 만들 때 다음 권장 사항을 고려하세요.

| 이미지 타입                                                                   | 형식                                          |
| ----------------------------------------------------------------------------- | --------------------------------------------- |
| 비트맵/래스터 작업물                                                          | 인터레이싱 기능이 적용되지 않는 PNG 파일 형식 |
| 24비트 컬러가 필요하지 않은 PNG                                               | 8비트 컬러 팔레트                             |
| 사진                                                                          | 최적화된 JEPG 파일 또는 HEIC 파일             |
| 평면 아이콘, 인터페이스 아이콘 및 고해상도 스케일링이 필요한 기타 평면 아트워크 | PDF 또는 SVG 파일

> 인터레이싱: PNG는 기본적으로 인터레이스 기능이 포함되어 있음. 인터레이스는 이미지를 다운로드하거나, 점진적으로 로드 할 때, 이미지 전체 모습 (흐릿하게) 보여줄 수 있는 기능을 의미함.


## Best practices

지원하는 모든 디바이스에 대해 앱의 모든 아트워크에 고해상도 이미지를 제공하세요. 프로젝트의 에셋 카탈로그에 각 이미지를 추가할 때 파일 이름에 "@1x", "@2x" 또는 "@3x"를  이름 뒤에 추가하여 해당 이미지의 배율을 식별하세요. 다음 값을 참고하고, 추가적인 배율에 대한 정보를 참고하고 싶다면 [레이아웃](https://developer.apple.com/design/human-interface-guidelines/layout)을 참조하세요.

| 플랫폼                    | 스케일 배율 |
| ------------------------- | ----------- |
| iPadOS, visionOS, watchOS | @2x         |
| iOS                       | @2x, @3x    |
| macOS, tvOS               | @1x, @2x

- ### 일반적으로 이미지를 가장 낮은 해상도로 디자인한 후 스케일 업하여 고해상도 에셋을 만듭니다. 
크기 조정이 가능한 벡터화된 도형을 사용하는 경우 제어점을 전체 값으로 배치하여 1배로 깔끔하게 정렬할 수 있습니다. 

2x와 3x는 1x의 배수이므로 이 위치를 사용하면 더 높은 해상도에서 래스터 그리드에 포인트를 깔끔하게 정렬된 상태를 유지할 수 있습니다. 반대로 도형을 래스터 그리드에 완벽하게 정렬해서 맞추지 않기를 원할 수 있습니다. 예를 들어 그런 경우에는 원을 그리드에 정렬하면 위쪽과 아래쪽이 평평하게 보일 수 있습니다.

- ### 각 이미지에 색상 프로필(컬러 프로필) 을 포함하세요. 
색상 프로필을 사용하면 앱의 색상이 다양한 디스플레이에서 의도한 대로 표시되도록 할 수 있습니다. 자세한 가이드는 [Color management(색상 관리)](https://developer.apple.com/design/human-interface-guidelines/color#Color-management)를 참조하십시오.

- ### 항상 다양한 실제 기기에서 이미지를 테스트하세요.
디자인 혹은 개발 당시에는 보기 좋았던 이미지가 다양한 기기에서 보면 픽셀이 깨지거나 늘어나거나 압축된 것처럼 보일 수 있습니다.

## 플랫폼 별 고려사항

- iOS, iPadOS, macOS는 특별하 해당 사항이 없습니다.


## tvOS

레이어드 이미지(Layered Image)는 Apple TV 사용자 경험의 핵심입니다. 이 tvOS 시스템은 레이어드 이미지, 투명도, 크기 조정 및 모션을 결합하여 사람들이 화면 콘텐츠와 상호 작용할 때 사용자에게 사실감과 생동감을  느낄 수 있는 경험을 전달 할 수 있습니다.

### Parallax effect 

`Parallax`는 요소가 초점을 맞출 때 깊이와 역동성을 전달하기 위해 시스템이 사용하는 미묘한 시각 효과입니다. 요소가 초점이 맞춰지면 시스템은 해당 요소를 사용자 앞으로 끌어올려 부드럽게 흔들면서 요소의 표면이 빛나는 것처럼 보이도록 조명을 적용합니다.
일정 시간 동안 활동이 없으면 아웃 포커싱된 콘텐츠는 어두워지고 초점이 맞춰진 요소는 확장됩니다.


### Layered Images
`Layered Images`는 2~5개의 서로 다른 레이어가 모여 하나의 이미지를 형성합니다. 투명도 사용과 함께 레이어 간의 분리는 깊이감을 만들어냅니다. 사용자가 이미지와 상호 작용할 때 표면에 가까운 레이어가 위로 올라가고 크기가 조정되며, 낮은 레이어가 멀리 떨어진 레이어와 겹쳐져 3D 효과를 만들어냅니다.

> 중요
> 
> tvOS [앱 아이콘](./App-icons.md)은 레이어 이미지를 사용해야 합니다. [Top Shelf](https://developer.apple.com/design/human-interface-guidelines/top-shelf) 이미지를 포함하여 앱에서 초점을 맞출 수 있는 다른 이미지의 경우 레이어드 이미지를 사용하는 것이 좋지만 필수가 아니고 선택 사항입니다.


#### 표준 인터페이스 요소를 사용하여 레이어드 이미지를 표시합니다.
표준 보기와 시스템에서 제공하는 포커스 API(예: [`FocusState`](https://developer.apple.com/documentation/SwiftUI/FocusState))를 사용하면 레이어 이미지에 초점을 맞출 때 자동으로 시차 처리가 적용됩니다.

#### Foreground, middle 및 background 요소를 식별하세요.
- foreground 레이어에는 게임 속 캐릭터나 앨범 표지 또는 영화 포스터의 텍스트와 같이 눈에 띄는 요소를 표시합니다.
- middle 레이어는 그림자와 같은 보조 콘텐츠 및 효과에 적합합니다. 
- background 레이어는 foreground 레이어와 middle 레이어를 돋보이게 하는 불투명한 배경입니다.

#### 일반적으로 텍스트는 foreground에 배치합니다.
텍스트를 가리고 싶지 않다면 선명하게 보이도록 foreground 레이어로 가져와야 합니다.
#### Background 레이어는 불투명하게 유지합니다. 
다양한 수준의 불투명도를 사용하여 콘텐츠가 상위 레이어를 통해 빛나도록 하는 것은 좋지만 background 레이어는 불투명해야 하며 그렇지 않으면 오류가 발생합니다. 불투명한 background 레이어는 아트워크가 시차, 그림자 및 시스템 배경과 함께 멋지게 보이도록 합니다.

#### 레이어링을 단순하고 섬세하게 유지하세요. 
패럴랙스는 거의 눈에 띄지 않도록 설계되었습니다. 과도한 3D 효과는 비현실적이고 어색해 보일 수 있습니다. 콘텐츠에 생동감을 불어넣고 즐거움을 더하려면 깊이를 단순하게 유지하세요.

#### 콘텐츠 주변에 Safe Area를 두세요.
초점과 시차를 적용하면 이미지의 크기와 움직임에 따라 일부 레이어의 가장자리 주변 콘텐츠가 잘리거나 선명하게 보이지 않을 수 있습니다. 기본 콘텐츠가 항상 표시되도록 하려면 가장자리에 너무 가깝게 배치하지 마세요.Safe Area는 이미지 크기, 레이어 깊이 및 움직임에 따라 달라질 수 있으며 foreground 레이어가 background 레이어보다 더 많이 잘릴 수 있다는 점에 유의하세요.

![Image of an icon with a dotted line inside the outer border, which indicates the safe zone.](https://docs-assets.developer.apple.com/published/941fcf33660f94464f60403ad7b3dd17/icons-and-images-icon-safe-zone@2x.png)

#### 항상 레이어 이미지를 미리 테스트 해보세요. 
레이어드 이미지가 Apple TV에서 멋지게 보이도록 하려면 디자인 프로세스 전반에 걸쳐 Xcode, macOS용 Parallax Previewer 앱 또는 Adobe Photoshop용 Parallax Exporter 플러그인을 사용하여 이미지를 미리 봅니다. 
크기 조정 및 클리핑이 발생할 때 특히 주의하고, 중요한 콘텐츠를 안전하게 유지하기 위해 필요에 따라 이미지를 재조정하세요. 레이어드 이미지가 최종적으로 완성되면 실제 TV에서 미리 보고 사람들에게 가장 정확하게 표시되는지 확인하세요. 패럴랙스 미리보기 및 패럴랙스 내보내기를 다운로드하려면 [Resources](https://developer.apple.com/design/resources/#tvos-apps)를 참조하세요.

> 이미지 클리핑: 이미지가 일정 범위를 벗어나서 잘려보이는 현상

#### 초점이 맞지 않은 상태와 초점이 맞춰진 상태를 모두 사용하여 레이어 이미지의 적절한 크기를 결정합니다. 
패럴랙스 효과를 적용하는 동안 시스템에서 background 레이어가 약간 잘릴 수 있으므로 필수 콘텐츠는 Safe Area 내에 유지하고 콘텐츠가 보기 좋게 보이도록 추가 공간을 확보하세요.



![Diagram of a layered image, which shows the outermost, actual size, the inner focused or safe zone size, and the innermost unfocused size. The diagram also shows the 35 point side margins between the unfocused and focused areas.](https://docs-assets.developer.apple.com/published/51bbe8a18e9f50356087bd7b8d9692a4/layered-image-zones@2x.png)

다음 공식을 사용하면 초점이 맞지 않을 때 이미지의 크기를 기준으로 레이어 이미지의 크기를 계산할 수 있습니다.

| 이미지 Side 위치 | Focused/Safe Zone 크기                      | 실제 크기                         |
| ---------------- | ------------------------------------------- | --------------------------------- |
| 긴 부분          | unfocused 된 영역의 긴 부분+ 70pt | focused된 영역의 긴 부분 * 106% |
| 짧은 부분        | 긴 부분의 크기에 비례  | 긴 부분의 크기에 비례


레이어 이미지를 앱에 포함하거나 런타임에 콘텐츠 서버에서 검색할 수 있습니다. 앱에 포함할 레이어드 이미지를 만들려면 다음 도구 중 하나를 사용합니다:

- macOS용 Parallax previewer 앱을 사용하세요. 
	- Parallax Previewer는 PNG 파일을 가져와 개별 레이어로 사용할 수 있으며, Parallax Exporter 플러그인으로 생성한 레이어 이미지(.lsr), 레이어 Photoshop 이미지(.psd)도 사용할 수 있습니다. Parallax Previewer는 Xcode 프로젝트로 직접 가져올 수 있는 LSR 파일을 내보낼 수 있습니다.

- Parallax Exporter Adobe Photoshop 플러그인을 사용하세요.
	- 이 플러그인을 사용하여 Photoshop에서 레이어 이미지를 테스트하고 Xcode 프로젝트로 직접 가져올 수 있는 LSR 파일로 내보낼 수 있습니다.

- Xcode를 사용하세요.
	- 표준 PNG 파일을 앱의 에셋 카탈로그로 드래그하여 Xcode에서 이미지 스택의 개별 레이어로 사용할 수 있습니다. 이미지 스택은 LSR 파일로 내보낼 수 있습니다. Xcode에서 LSR 파일을 임포트할 수도 있습니다.


앱이 런타임에 콘텐츠 서버에서 레이어드 이미지를 검색하는 경우 해당 이미지를 런타임 레이어드 이미지(.lcr) 형식으로 제공해야 합니다. 런타임 레이어드 이미지는 직접 생성하지 않고 Xcode에서 제공하는 `layerutil` 명령줄 도구를 사용하여 LSR 파일 또는 Photoshop 파일에서 생성합니다. 런타임 레이어 이미지는 다운로드용이므로 앱 내에 첨부해서는 안됩니다.

## visionOS
비전OS에서 이미지가 차지하는 영역은 일반적으로 사람들이 이미지를 보는 거리와 각도에 따라 시스템이 동적으로 크기를 조정할 때 달라집니다. 즉, 다른 플랫폼에서처럼 이미지가 화면 픽셀과 1:1로 정렬되지 않습니다.

- 비전OS 앱 아이콘을 위한 다층 이미지를 만듭니다. 
	- 자세한 가이드는 [앱 아이콘](./App-icons.md) 문서를 참조하세요.

- 벡터 기반 아트워크를 권장합니다. 
	- 비트맵 콘텐츠는 시스템에서 확장할 때 보기 좋지 않을 수 있으므로 피하십시오. 핵심 애니메이션 레이어를 사용하는 경우 개발자 지침은 [Drawing sharp layer-based content in visionOS](https://developer.apple.com/documentation/visionOS/drawing-sharp-layer-based-content)를 참조하세요.

- @2x 이미지 만들기를 권장합니다. 
	- 고해상도를 사용하면 시스템에서 이미지 크기를 조정할 때 이미지가 선명하게 표시되는 데 도움이 됩니다. 자세한 내용은 [Scale](https://developer.apple.com/design/human-interface-guidelines/spatial-layout#Scale)을 참조하십시오.


## watchOS

### - 일반적으로 이미지 파일을 작게 유지하려면 투명도를 피하세요.
항상 동일한 단색 배경색에 이미지를 합성하는 경우 이미지에 배경을 포함하는 것이 더 효율적입니다. 그러나 컴플리케이션 이미지, 메뉴 아이콘, 템플릿 이미지로 사용되는 기타 인터페이스 아이콘과 같은 경우에는 시스템이 어디에 색상을 적용할지 결정하기 위해 투명도가 필요합니다.

> 컴플리케이션: 워치 페이스에 추가적인 정보나 기능을 제공하는 작은 위젯 요소
### - 자동 크기 조정 PDF를 사용하면 모든 화면 크기에 맞는 단일 이미지를 제공할 수 있습니다.
40mm 및 42mm 화면에 맞게 이미지를 2배로 디자인하세요. PDF를 로드하면 WatchKit은 아래 표시된 값을 사용하여 장치의 화면 크기에 따라 이미지의 크기를 자동으로 조정합니다:



| 스크린 사이즈 | 이미지 배율 |
| ------------- | ----------- |
| 38mm          | 90%            |
| 40mm          | 100%            |
| 41mm          | 106%            |
| 42mm          | 100%            |
| 44mm          | 110%            |
| 45mm          | 119%            |
| 49mm          | 119%            |


---
### 연관 문서
- [Apple Design Resources](https://developer.apple.com/design/resources/)
### 개발자 연관 문서
- [Drawing sharp layer-based content in visionOS](https://developer.apple.com/documentation/visionOS/drawing-sharp-layer-based-content)
- [`UIImageView`](https://developer.apple.com/documentation/uikit/uiimageview)
- [`NSImageView`](https://developer.apple.com/documentation/appkit/nsimageview)
- [`FocusState`](https://developer.apple.com/documentation/SwiftUI/FocusState)

### 영상

| [Get Started with Display P3](https://developer.apple.com/videos/play/wwdc2017/821) |
| ----------------------------------------------------------------------------------- |
|                             ![](https://devimages-cdn.apple.com/wwdc-services/images/7/09438FDD-3E8B-42A3-A364-78E1A7F2CE6B/1915_wide_250x141_1x.jpg)                                                        |




