
# Designing for visionOS
[원본 링크](https://developer.apple.com/design/human-interface-guidelines/designing-for-visionos)

### `Apple Vision Pro`를 착용하면 무한한 3D 공간에 들어가 주변 환경과 연결 상태를 유지하면서 앱과 게임을 즐길 수 있습니다.

![](https://i.imgur.com/bqt0iGU.jpg)

`visionOS`용 앱이나 게임 디자인을 시작할 때는 플랫폼을 구분하는 기본적인 디바이스 특성과 패턴을 이해하는 것부터 시작하세요. 이러한 특성과 패턴을 활용하여 디자인 결정을 내리고 몰입도 높고 매력적인 경험을 제작할 수 있습니다.

### Space
Apple Vision Pro는 [Windows](Windows.md#Windows), [Volumes](Windows.md#Volumes), 3D 물체와 같은 가상 콘텐츠를 볼 수 있는 무한한 캔버스를 제공하며, 다른 장소로 이동할 수 있는 [Immersive experiences(몰입도 높은 경험)](Immersive-experiences.md)을 선택할 수 있습니다.

### Immersion
visionOS 앱에서 사람들은 서로 다른 수준의 [immersion(몰입도)](Immersive-experiences.md) 사이를 유동적으로 전환할 수 있습니다. 
기본적으로 앱은 여러 앱을 나란히 실행할 수 있는 공유 공간에서 실행되며 사용자는 `window`를 열고, 닫고, 재배치할 수 있습니다. 또한 하나의 앱만 실행되는 전체 공간으로 전환하도록 선택할 수도 있습니다. 전체 공간 앱에서 사람들은 주변 환경과 혼합된 3D 콘텐츠를 보거나 포털을 열어 다른 장소를 보거나 다른 세계로 들어갈 수 있습니다.

### Passthrough
[Passthrough](Immersive-experiences.md#Immersion-and-passthrough)는 기기의 외부 카메라에서 라이브 비디오를 제공하며, 사람들이 실제 주변 환경을 보면서 가상 콘텐츠와 상호 작용할 수 있도록 도와줍니다. 사람들이 주변 환경을 더 많이 또는 더 적게 보고 싶을 때 [Digital Crown](Digital-Crown.md)을 사용하여 `Passthrough`의 양을 조절할 수 있습니다.

### Spatial Audio
비전 프로는 음향 및 시각 감지 기술을 결합하여 주변 환경의 음향 특성을 모델링하여 자동으로 공간에서 자연스러운 오디오 사운드를 만들어냅니다. 앱이 사용자의 주변 환경에 대한 정보 액세스 권한을 받으면 [Spatial Audio](../Patterns/Playing-audio.md#visionOS)를 미세 조정하여 맞춤형 경험을 생생하게 구현할 수 있습니다.

### Focus and gestures
일반적으로 사람들은 [눈](../Inputs/Eyes.md)과 [손](https://developer.apple.com/design/human-interface-guidelines/gestures.md#visionOS)을 사용하여 Vision Pro와 상호 작용합니다. 사람들은 가상 개체를 바라보며 [focus](https://developer.apple.com/design/human-interface-guidelines/focus-and-selection)을 맞추고 탭과 같은 간접적인 제스처를 취하여 활성화하는 방식으로 대부분의 작업을 수행합니다. 또한 직접 제스처를 사용하여 손가락으로 터치하여 가상 객체와 상호 작용할 수도 있습니다.

### Ergomics
Vision Pro를 착용하는 동안 사람들은 현실과 가상의 모든 것을 기기의 카메라에 전적으로 의존하기 때문에 시각적 편안함을 유지하는 것이 가장 중요합니다. 이 시스템은 사용자의 키나 앉은 자세, 서 있는 자세, 누워 있는 자세에 관계없이 콘텐츠를 착용자의 머리에 맞춰 자동으로 배치하여 편안함을 유지하도록 도와줍니다. visionOS는 사용자가 콘텐츠에 도달하기 위해 움직이지 않고 콘텐츠를 사용자에게 제공하기 때문에 사용자는 앱과 게임에 몰입하는 동안 편안하게 휴식을 취할 수 있습니다.
### **Accessibility**
Apple Vision Pro는 보이스오버, 스위치 제어, 드웰 제어, 가이드 액세스, 헤드 포인터 등과 같은 [Accessibility(접근성)](https://developer.apple.com/design/human-interface-guidelines/accessibility) 기술을 지원하므로 사용자가 자신에게 적합한 상호작용을 사용할 수 있습니다. 모든 플랫폼과 마찬가지로 비전OS에서도 시스템에서 제공하는 UI 구성 요소는 기본적으로 접근성을 지원하며, 시스템 프레임워크는 앱이나 게임의 접근성을 향상시킬 수 있는 방법을 제공합니다.

> 드웰 제어(Dwell Control): 시선 또는 머리 추적 기술을 사용해 마우스 동작을 수행하는 것


---

## Best practices

훌륭한 visionOS 앱과 게임은 친숙하고 접근하기 쉬우면서도 아름다운 콘텐츠, 확장된 기능, 매혹적인 모험으로 사람들에게 특별한 경험을 제공합니다.

### Apple Vision Pro의 고유한 기능을 활용하세요.
공간, 공간 오디오 및 몰입감을 활용하여 경험에 생동감을 불어넣는 동시에 [Passthrough](Immersive-experiences.md#Immersion-and-passthrough), [focus](https://developer.apple.com/design/human-interface-guidelines/focus-and-selection) 및 제스처를 기기에서 집처럼 편안한 방식으로 통합할 수 있습니다.

### 앱의 가장 특별한 순간을 표현하는 방법을 설계할 때 몰입감의 전체 스펙트럼을 고려하세요.
`window` 중심의 UI 중심 컨텍스트, 완전 몰입형 컨텍스트 또는 그 중간 정도의 컨텍스트에서 경험을 제공할 수 있습니다. 앱의 각 주요 순간에 대해 가장 적합한 최소 [immersion(몰입도)](Immersive-experiences.md)를 찾아야 합니다. 모든 순간이 완전 몰입형이어야 한다고 가정하지 마세요.

### UI를 중심으로 구성된 경험을 제공하고 싶다면 `window`를 사용하세요.
사람들이 표준 작업을 수행할 수 있도록 공간에서 평면으로 표시되고 익숙한 컨트롤이 포함된 표준 [windows](Windows.md#Windows)를 선호합니다. visionOS에서는 사용자가 원하는 위치에 `window`를 재배치할 수 있으며, 시스템의 [dynamic scaling](../Foundations/Spatial-layout.md#Scale) 기능을 통해 `window` 콘텐츠가 가까이 있든 멀리 있든 가독성을 유지할 수 있습니다.

### 편안함을 우선시하세요.
사람들이 앱이나 게임과 상호 작용할 때 편안하고 신체적으로 안정된 상태를 유지할 수 있도록 다음 기본 사항을 염두에 두세요.

- 콘텐츠를 사람의 [filed of view(시야)](../Foundations/Spatial-layout.md#Field-of-view) 내에 표시하고 머리를 기준으로 배치합니다. 콘텐츠와 상호 작용하기 위해 고개를 돌리거나 자세를 바꿔야 하는 위치에 콘텐츠를 배치하지 마세요.
- 압도적이거나, 흔들리거나, 너무 빠르거나, 정지된 기준 프레임이 누락된 [motion(모션)](https://developer.apple.com/design/human-interface-guidelines/motion#visionOS)을 표시하지 마세요.
- 사용자가 무릎이나 옆구리에 손을 얹은 상태에서 앱과 상호 작용할 수 있는 [indirect gestures(간접 제스처)](https://developer.apple.com/design/human-interface-guidelines/gestures#visionOS)를 지원하세요.
- 직접 제스처를 지원하는 경우, 인터랙티브 콘텐츠가 너무 멀리 떨어져 있지 않고 사람들이 장시간 인터랙션할 필요가 없는지 확인하세요.
- 완전하게 [Immersive experiences(몰입도 높은 경험)](Immersive-experiences.md)에 있는 경우,사람들이 너무 많이 움직이도록 유도하지 마세요.

### 사람들이 다른 사람들과 활동을 공유할 수 있도록 지원하세요.
[SharePlay](../Technologies/SharePlay.md)를 사용하여 공유 활동을 지원하면 사람들은 다른 참가자의 공간 페르소나를 볼 수 있어 모두가 같은 공간에 함께 있는 것처럼 느낄 수 있습니다.

### 연관 내용
- [Apple Design Resources](https://developer.apple.com/design/resources/#visionOS-apps)

### 개발자 문서 참고
- [Creating your first visionOS app](https://developer.apple.com/documentation/visionOS/creating-your-first-visionos-app)

### 영상

| [Design for spatial user interfaces](https://developer.apple.com/videos/play/wwdc2023/10076) | [Principles of spatial design](https://developer.apple.com/videos/play/wwdc2023/10072) | [Design for spatial user interfaces](https://developer.apple.com/videos/play/wwdc2023/10072) |
| -------- | -------- | -------- |
| ![](https://i.imgur.com/kTIL2Ke.png)|     ![](https://i.imgur.com/PD74ZGq.png) | ![](https://i.imgur.com/lqNmxbv.png) |
