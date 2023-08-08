# Motion
## 모든 플랫폼에서 아름답고 유연한 모션은 인터페이스에 생동감을 불어넣어 상태를 전달할 수 있습니다. 또한, 모션은 피드백과 가이드를 제공하며, 사용자의 시각적 경험을 풍부하게 합니다.![A sketch of three overlapping diamonds, suggesting the movement of an element from left to right. The image is overlaid with rectangular and circular grid lines and is tinted yellow to subtly reflect the yellow in the original six-color Apple logo.](https://docs-assets.developer.apple.com/published/1a0efd7807cfcba7a5821be86b20bafc/foundations-motion-intro@2x.png)

많은 시스템 구성 요소에 모션이 자동으로 포함되므로 앱이나 게임 전체에서 친숙하고 일관된 경험을 제공할 수 있습니다. 사용자 지정 모션을 디자인할 때는 사람들이 방향을 잃지 않고 편안하게 사용할 수 있도록 의도적인 애니메이션을 선호하고, 사용자의 행동에 대한 명확한 피드백을 제공하며, 사용자가 부담스럽지 않게 인터페이스를 익힐 수 있도록 도와야 합니다.

## Best practices

### - 사소한 디테일을 담은 애니메이션을 사용하여 소통하세요. 
모션은 상황이 어떻게 변화하는지, 사람들이 어떤 작업을 수행하면 어떤 일이 일어나는지, 다음에 무엇을 할 수 있는지 보여줌으로써 피드백과 이해도를 높일 수 있는 좋은 방법입니다. 예를 들어, macOS에서 윈도우을 최소화하면 바탕화면에서 Dock으로 부드럽게 이동하여 윈도우이 어디로 갔는지 정확히 알 수 있고, Face ID를 설정하면 시스템이 스캔하는 동안 얼굴을 둘러싼 체크 표시를 시각적으로 변경하여 사용자가 해야 할 일을 간략하게 설명하고 도움을 주며, visionOS에서는 사용자가 초점을 맞추면 창 컨트롤이 부드럽게 확장됩니다.

- ###  사용자 경험을 해치지 않는 선에 모션을 추가하세요.
모션을 추가하기 위해 모션을 추가하지 마세요. 불필요하거나 과도한 애니메이션은 사람들의 주의를 분산시키고 단절감을 느끼거나 신체적으로 불편하게 만들 수 있습니다.

### - 모션을 선택 사항으로 설정하세요. 
사람들이 앱에서 모션을 경험하지 못할 수 있는 이유는 여러 가지가 있으므로 중요한 정보를 전달하는 유일한 방법으로 모션을 사용하지 않는 것이 중요합니다. 예를 들어 사용자가 수동으로 모션 접근성 감소 설정을 켜서 애니메이션을 최소화하거나 제거할 수 있습니다. 자세한 내용은 [Accessibility >> 모션](./Accessibility.md#Motion)을 참조하세요.

### - 사용자가 납득이 되는 모션을 사용하세요.
게임 앱이 아닌 경우 정확하고 사실적인 모션은 사람들이 작동 방식을 이해하는 데 도움이 되지만, 현실적이지 않거나 물리 법칙을 거스르는 듯한 모션은 방향 감각을 잃게 만들 수 있습니다. 예를 들어, 위에서 아래로 슬라이드하여 뷰를 표시할 때 옆으로 슬라이드하면 뷰가 사라질 것이라고 사람들은 쉽게 예상하지 못합니다.

### - 사용자는 짧고 정확한 애니메이션을 선호합니다. 
간결함과 정확성을 결합한 애니메이션은 더 가볍고 방해가 덜 되는 경향이 있으며, 종종 정보를 더 효과적으로 전달하는 경향이 있습니다. 예를 들어, iPhone의 날씨에서 목록 버튼을 탭하면 현재 도시의 전체 화면 보기가 목록 보기로 빠르게 전환되어 목록에서 해당 도시의 위치를 정확히 알려줍니다. 비전OS에서는 사용자가 사진에서 파노라마를 탭하면 보기가 부드럽게 확장되어 앞쪽 공간을 채우므로 시각적으로 화면 전환을 추적할 수 있습니다.

### - 일반적으로 자주 발생하는 상호작용에 모션을 추가하는 것은 피하세요. 
시스템에서는 이미 표준 UI 요소와의 상호작용을 위한 미니멀한 애니메이션을 제공하고 있습니다. 사람들이 콘텐츠와 상호 작용할 때마다 불필요한 동작에 주의를 기울이지 않도록 하는 것을 권장합니다.

### - 적절한 경우 애니메이션 심볼을 사용하는 것이 좋습니다.
`SF Symbol 5` 이상을 사용하는 경우 `SF Symbol` 또는 사용자 정의 심볼에 애니메이션을 적용할 수 있습니다. 자세한 내용은 [애니메이션](https://developer.apple.com/design/human-interface-guidelines/sf-symbols#Animations)을 참조하세요.


## 플랫폼 별 고려사항
- iOS, iPadOS, macOS, tvOS는 해당 사항이 없습니다.

## visionOS
visionOS에서 모션은 현재 상황(컨텍스트)을 미묘하게 전달하고, 정보에 주의를 집중시키고, 몰입형 경험을 풍부하게 만들 수 있습니다. [깊이](./Spatial-layout.md#Depth)와 결합된 모션은 사람들이 요소에 [집중(focus)](https://developer.apple.com/design/human-interface-guidelines/focus-and-selection)할 때 필수적인 피드백도 제공합니다. 주의 분산, 혼란, 불편함을 유발하지 않으면서도 사람들이 받아들일 수 있는 방식으로 모션을 사용하는 것이 중요합니다.

사람들은 Apple Vision Pro를 착용한 상태에서 [패스스루](./Immersive-experiences.md#Immersion-and-passthrough)를 사용하여 가상 콘텐츠와 상호 작용하는 동안 실제 주변 환경을 볼 수 있습니다. 주변 환경과 앱 콘텐츠를 동시에 볼 수 있기 때문에 가상 콘텐츠의 움직임으로 인해 자신이나 주변 환경이 움직이는 것처럼 느껴지면 불편함을 느낄 수 있습니다. 일반적으로 움직이는 가상 물체의 크기가 클수록 안정감을 유지하기가 더 어려울 수 있습니다.

### - 큰 가상 객체의 움직임을 보여줄 때 사람들이 편안함을 느낄 수 있도록 도와주세요.
물체가 [시야](./Spatial-layout.md#Field-of-View)의 대부분 또는 전부를 가릴 정도로 충분히 커서 시야를 가득 채우면 사람들은 자연스럽게 그 물체를 주변 환경의 일부로 인식할 수 있습니다. 사람들이 자신이나 주변 환경이 움직인다고 생각하지 않고 물체의 움직임을 인식하도록 하려면 물체의 반투명도를 높여 사람들이 물체를 투과하여 볼 수 있도록 하거나 대비를 낮추어 물체의 움직임이 덜 눈에 띄게 만들 수 있습니다. 큰 물체 사이의 전환을 표시해야 하는 경우 fade out/fade in (밝기가 어두워지고 밝아지는 효과) 또는 콘텐츠의 초점이 들어오고 나가는 효과를 사용하여 방향 감각을 잃을 위험성을 최소화하는 것이 좋습니다.


> 참고
> 
> 사람들은 window와 같은 큰 가상 물체를 움직이는 경우에도 불편함을 느낄 수 있습니다. 이 경우에서도 반투명도와 대비를 조정하면 조금 불편함을 해소 할 수 있지만, window 크기를 상당히 작게 유지하는 것이 좋습니다.

### - Window 대부분을 차지하는 움직이는 콘텐츠를 표시할 때는 주의하세요. 
이 경우에서는 사람들은 때때로 window의 콘텐츠를 주변 세계로 인식하고 움직임을 자신의 것으로 인식할 수 있습니다. window에 움직이는 콘텐츠를 표시해야 하는 경우 사람들이 주변 환경을 계속 볼 수 있도록 window 또는 콘텐츠 영역의 크기를 제한하는 것이 좋습니다. Window에 표시되는 모션을 만들 때는 수평을 유지하고, 속도를 낮게 유지하며, 갑작스럽거나 예상치 못한 카메라 움직임을 피하는 것이 좋습니다. 또한 대비가 낮은 텍스처를 사용하면 모션이 덜 눈에 띄게 만들 수 있습니다.

> 여기서 언급하는 Window는 visionOS의 [Window](../Components/Presentation/Windows.md) 링크를 참고하세요.


### - 회전 동작은 부드럽게 하세요.
카메라를 회전하거나 사람 주위의 큰 가상 물체를 회전하는 등 가상 세계를 회전할 때, 특히 회전이 빠르거나 너무 오래 지속되면 사람의 안정감을 깨뜨릴 수 있습니다. 대신 빠른 페이드 아웃 중에 즉각적인 방향 전환을 사용하는 것이 좋습니다.

### - 지속적으로 진동하는 물체를 표시하지 마세요. 
특히 진동 주파수가 약 0.2Hz인 진동은 사람들이 이 주파수에 매우 민감하게 반응할 수 있으므로 표시하지 않는 것이 좋습니다. 진동하는 물체를 표시해야 하는 경우 진폭을 낮게 유지하고 콘텐츠를 반투명하게 만드는 것을 고려하세요.

### - 불필요한 모션을 제거합니다. 
사람들은 상호 작용하려는 물체를 바라보기 때문에 한 눈을 팔게 할 수 있는 곳에 모션을 표시하면 불쾌감을 줄 수 있습니다. 사람들이 중요한 것을 보도록 유도해야 할 때만 모션을 사용하는 것이 좋습니다.

### - 가급적 사람의 시야 가장자리에는 모션을 표시하지 마세요. 
사람들은 주변 시야에서 발생하는 움직임에 특히 민감할 수 있습니다. 주변부 움직임은 주의를 산만하게 할 뿐만 아니라 자신이나 주변 환경이 움직이는 것처럼 느껴져 불편함을 유발할 수도 있습니다.

### - 사람들에게 고정된 기준 프레임을 제공하는 것이 좋습니다. 
시각적 움직임이 움직이지 않는 영역에 포함되면 사람들이 시각적 움직임을 처리하기가 더 쉬워질 수 있습니다. 반대로 주변의 모든 것이 움직이는 것처럼 보이면 사람들은 불쾌감을 느낄 수 있습니다.

### - 시각적 회전을 경험하는 동안 고개를 움직이도록 유도하지 마세요. 
가상 물체가 주변에서 회전하는 것처럼 보일 때 사람들은 일반적으로 불쾌감을 느끼지 않기 위해 눈을 일정한 방향으로 유지해야 합니다.

### - 물체의 위치를 변경해야 할 때는 페이드 기능을 사용하는 것이 좋습니다. 
물체가 한 위치에서 다른 위치로 이동하면 사람들은 자연스럽게 그 움직임을 주시하게 됩니다. 이러한 움직임이 사람들에게 유용한 정보를 전달하지 않는다면 물체를 이동하기 전에 fade-out 했다가 새 위치에 도착한 후 다시 fade-in할 수 있습니다.

## watchOS
SwiftUI는 앱에 모션을 추가할 수 있는 강력하고 간소화된 방법을 제공합니다. WatchKit을 사용하여 레이아웃 및 모양 변경에 애니메이션을 적용하거나 애니메이션 이미지 시퀀스를 만들어야 하는 경우 [`WKInterfaceImage`](https://developer.apple.com/documentation/watchkit/wkinterfaceimage#1652345) 참조하세요.

> 참고
> 
> 모든 레이아웃 및 모양 기반 애니메이션에는 애니메이션의 시작과 끝에서 재생되는 easing(애니메이션 완화) 기능이 자동으로 포함됩니다.  easing(애니메이션 완화)를 끄거나 사용자 지정할 수 없습니다.

---


### 연관 내용
- [Feedback](https://developer.apple.com/design/human-interface-guidelines/feedback)
- [Accessibility](https://www.apple.com/accessibility/)
- [Spatial layout](./Spatial-layout.md)
- [Immersive experiences](./Immersive-experiences.md)

### 개발자 문서
[Animating Views and Transitions](https://developer.apple.com/tutorials/SwiftUI/animating-views-and-transitions)

### 영상

| [Design considerations for vision and motion](https://developer.apple.com/videos/play/wwdc2023/10078) | [Principles of spatial design](https://developer.apple.com/videos/play/wwdc2023/10072) | [Designing Fluid Interfaces](https://developer.apple.com/videos/play/wwdc2018/803) |
| -------- | -------- | -------- |
| ![](https://devimages-cdn.apple.com/wwdc-services/images/D35E0E85-CCB6-41A1-B227-7995ECD83ED5/2C47B638-090D-4CBB-9E9E-EBE8114536D9/8132_wide_250x141_1x.jpg)| ![](https://devimages-cdn.apple.com/wwdc-services/images/D35E0E85-CCB6-41A1-B227-7995ECD83ED5/15489B11-8744-483D-AD38-EF78D8962FF4/8126_wide_250x141_1x.jpg) | ![](https://devimages-cdn.apple.com/wwdc-services/images/42/E55D60D2-C7D7-4F96-9A9D-8AF4C7D6BB49/2247_wide_250x141_1x.jpg) |


