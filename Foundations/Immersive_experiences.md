# Immersive experiences
[원본 링크](https://developer.apple.com/design/human-interface-guidelines/immersive-experiences)

>  visionOS에서는 `window`과 `volume`을 넘어 확장되는 앱과 게임을 디자인하고 사람들이 콘텐츠에 몰입할 수 있도록 할 수 있습니다.

![](https://i.imgur.com/97QVR3r.png)

`visionOS`에서는 공유 공간에서 여러 앱을 동시에 실행하거나 전체 공간에서 한 번에 하나의 앱에 집중할 수 있습니다. 기본적으로 앱은 공유 공간에서 실행되며, 사용자는 Mac에서와 마찬가지로 실행 중인 여러 앱 간에 전환할 수 있습니다.

보다 몰입감 있는 환경을 원할 경우 다른 앱은 숨겨지고 앱은 어디서나 콘텐츠를 표시할 수 있는 전체 공간으로 앱을 전환할 수 있습니다.

## Immersion-and-passthrough
visionOS는 사람들이 앱이나 게임을 경험할 수 있는 다양한 방법을 제공하는 데 도움이 되는 몰입도 스펙트럼을 지원합니다. 이 스펙트럼에서 사람들의 물리적 환경의 가시성은 경험의 몰입도에 중요한 역할을 합니다.

https://github.com/i-colours-u/HIG-Korean/assets/60260284/5a9d6552-23d9-4eca-89f5-463d0fcec303

Apple Vision Pro를 착용한 상태에서는 기기의 외부 카메라에서 실시간 비디오를 제공하는 패스스루를 사용하여 주변 환경을 볼 수 있습니다.

주변 환경을 얼마나 많이 볼 수 있는지 변경하려면 [Digital Crown](https://developer.apple.com/design/human-interface-guidelines/digital-crown)을 사용하여 [Passthrough](https://developer.apple.com/design/human-interface-guidelines/immersive-experiences#Immersion-and-passthrough)의 양을 조정합니다. 예를 들어, 근처의 물리적 물체와 상호 작용하거나 다른 디바이스에서 텍스트를 읽고 싶을 때는 [Passthrough](https://developer.apple.com/design/human-interface-guidelines/immersive-experiences#Immersion-and-passthrough)를 늘리고, 환경을 불러오고 싶을 때는 [Passthrough](https://developer.apple.com/design/human-interface-guidelines/immersive-experiences#Immersion-and-passthrough)를 줄일 수 있습니다.

https://github.com/i-colours-u/HIG-Korean/assets/60260284/f57aeba7-29d9-4619-ac45-680669c54538


> **중요**
> 
> 앱은 현재 비전프로에서 투과되는 수준이나 사용자 위치 시점에 대한 직접적인 정보를 수신하지 않으므로 사용자가 기기 주변 환경을 얼마나 잘 볼 수 있는지 알 수 없습니다.

## 사람들이 경험에 몰입하고 콘텐츠에 참여하도록 돕기 위해 다음과 같은 기술을 고려하세요.

- ### 공유 공간에 있는 동안 Passthrough를 사용해 주변 환경을 어둡게 하세요.
> 시스템에 Passthrough 및 기타 보이는 콘텐츠를 미묘하게 어둡게 하여 다른 앱을 숨기지 않고 방해 요소를 최소화하고 특정 창이나 볼륨을 강조하도록 요청할 수 있습니다. [SurroundingsEffect(주변 환경 효과)](https://developer.apple.com/documentation/SwiftUI/SurroundingsEffect) 개발자 문서를 참조하세요.

- ### 주변 환경과 통합된 환경을 제공하세요.
> 전체 공간에서 실행할 때 앱은 주변의 실제 물체 및 공간 레이아웃에 대한 정보에 대한 액세스를 요청하여 사람들의 주변 환경과 조화를 이루는 가상 콘텐츠를 표시할 수 있습니다. [mixed](https://developer.apple.com/documentation/SwiftUI/ImmersionStyle/mixed) 및 [ARKit](https://developer.apple.com/documentation/arkit) 개발자 문서를 참조하세요.

- ### Portal을 제공하세요.
> 전체 공간에서 실행되는 앱은 `Portal`을 사용하여 사람들을 주변 환경으로부터 완전히 분리하지 않으면서 더욱 몰입감 있는 경험을 제공할 수 있습니다. `Portal`이 열리면 사람들은 몰입형 콘텐츠를 대략 180도로 볼 수 있으며, 디지털 크라운을 사용하여 포털의 크기를 조정할 수 있습니다. [progressive](https://developer.apple.com/documentation/SwiftUI/ImmersionStyle/progressive) 개발자 문서를 참조하세요.

- ### 완전히 몰입형 환경(Immersive experience)를 제공하세요.
>  완전한 몰입형 환경(Immersive experience)를 제공하기 위해 전체 공간에서 실행되는 앱은 사람들을 완전히 둘러싸는 콘텐츠를 표시하여 새로운 장소로 이동하는 동안 시스템에 `Passthrough`를 숨기도록 요청할 수 있습니다. [full](https://developer.apple.com/documentation/SwiftUI/ImmersionStyle/full) 개발자 문서를 참조하세요.


## visionOS는 사람들이 앱을 사용하는 동안 다음과 같은 기능을 제공합니다.

- #### 사람이 약 1미터 이상 움직이면 시스템이 자동으로 표시되는 모든 콘텐츠를 반투명하게 만들어 주변 환경을 탐색할 수 있도록 도와줍니다.
- #### 완전 몰입형 환경이 시작되면 시스템은 착용자 머리의 초기 위치에서 1.5m까지 확장되는 보이지 않는 영역을 정의합니다. 머리가 이 영역을 벗어나면 체험이 자동으로 중지되고 패스스루로 돌아가 실제 주변 환경의 물체와 충돌을 피할 수 있습니다.
- #### 이 시스템은 사용자가 실제 물체에 너무 가까이 다가가거나 너무 빠르게 움직이면 몰입형 경험을 중단할 수 있습니다.


## Best practices
#### 다양한 앱 사용 방법을 제공하세요
사람들이 자신의 경험을 자유롭게 선택할 수 있도록 하는 것 외에도, 사람들이 기기와 상호 작용하는 방식을 개인화할 수 있도록 [Accessibility](https://developer.apple.com/design/human-interface-guidelines/accessibility) 기능을 앱에 설계하는 것이 중요합니다. [Accessibility](https://developer.apple.com/design/human-interface-guidelines/accessibility) 개발자 문서를 참조하세요.

#### 의미 있는 순간과 콘텐츠를 위해 Immersion(몰입) 상황을 잘 설계하세요.
앱에서 모든 상황에서 몰입(Immersion)을 제공한다고 해서 이점을 누릴 수 있는 것은 아닙니다.

사람들은 때때로 다른 세계로 들어가기를 원하지만, 앱을 사용하는 동안에는 주변 환경에 집중하고 싶어 할 수 있습니다. 만약 해당 앱이 이러한 기능을 제공한다면, 다른 앱과 시스템 기능을 동시에 사용할 수 있다는 점을 높이 평가할 수 있습니다.

앱의 모든 상황에서 몰입(Immersion) 상태에 들어가야 한다고 설계하기 보다는, 사람들이 앱의 고유한 개별 작업과 콘텐츠에 몰입할 수 있는 방법을 설계하세요. 

예를 들어, 사용자는 공유 공간에서 익숙한 앱 창을 사용하여 사진에서 앨범을 탐색할 수 있지만, 사진 한 장을 살펴보고 싶을 때는 사진을 확장하고 세부 정보를 감상할 수 있는 전체 공간에서 일시적으로 더 몰입감 있는 환경으로 전환할 수 있습니다.


#### 몰입도에 관계없이 사람들이 앱의 주요 순간에 몰입할 수 있도록 도와주세요.
디밍, [motion(모션)](https://developer.apple.com/design/human-interface-guidelines/motion), [scale(스케일)](https://developer.apple.com/design/human-interface-guidelines/spatial-layout#Scale), [Spatial Audio(공간 오디오)](https://developer.apple.com/design/human-interface-guidelines/playing-audio#visionOS)와 같은 요소를 사용해서 사용자에게 힌트를 제공하세요.

힌트를 제공한다면, 공유 공간의 `window`나 전체 공간의 완전 몰입형 경험 등 콘텐츠의 특정 영역에 사람들의 주의를 끌 수 있습니다. 사람들의 주의를 부드럽게 유도하는 미묘한 단서(힌트)부터 시작하여 앱의 중요한 순간에서 힌트를 더 강조하세요.

> 디밍(dimming): 빛의 세기를 조절하는 것

#### 몰입도 높은 환경으로 전환할 시기를 사용자가 선택할 수 있도록 하는 것이 좋습니다.
사용자의 동의 없이 더 몰입도 높은 환경으로 이동시키거나 예기치 않게 큰 창이나 물체를 표시하여 사용자를 압도하고 싶지 않을 것입니다. 

대신 명확한 진입 및 종료 제어 기능을 제공하여 사람들이 콘텐츠에 더 몰입할 수 있는 시기를 결정할 수 있도록 하세요.

#### 자연스럽고, 예측 가능한 전환이 되도록 설계하세요. 

사람들이 시각적으로 변화를 추적할 수 있는 자연스러운 전환을 제공하여 다양한 경험에 대비할 수 있도록 하세요. 방향을 잃게 하거나 불편함을 줄 수 있는 갑작스럽고 혼란스러운 전환은 피하세요.

#### 몰입형 경험을 쉽게 종료할 수 있도록 하세요.
예를 들어, Keynote는 사람들이 극장 경험을 종료하고 슬라이드 보기 창으로 돌아갈 수 있도록 눈에 잘 띄는 종료 버튼을 제공합니다. 

버튼이 사용자를 이전의 덜 몰입적인 컨텍스트로 되돌리는지 아니면 게임과 같은 경험을 종료하는 것인지 명확하게 표시해야 합니다.

몰입형 경험을 종료하면 앱도 종료되는 경우, 종료하기 전에 진행 상황을 저장할 수 있는 위치로 돌아가거나 일시 중지할 수 있는 컨트롤을 제공하는 것을 고려하세요.

#### 완전 몰입형 환경에서는 사람들이 움직이도록 유도하지 마세요.
완전 몰입형 환경에서는 시스템이 `Passthrough`를 숨기므로 사람들이 콘텐츠에 몰입하는 동안 주변 상황을 파악하지 못할 수 있습니다.

사람들이 앱을 사용하는 동안 안전하고 편안한 상태를 유지하도록 유도하는 것이 중요합니다. 

사람들이 한 곳에 머무르도록 돕는 한 가지 방법은 사람들이 콘텐츠를 향해 이동하도록 설계하는 방법보다, 직접적인 콘텐츠를 제공하는 것입니다.

#### 앱 콘텐츠를 사용자의 주변 환경과 혼합하려면 ARKit을 채택하세요
예를 들어, 가상 콘텐츠를 사용자의 주변 환경에 통합하거나 착용자의 손 위치를 사용하여 사용자에게 경험을 제공하고자 할 수 있습니다. 

이러한 유형의 민감한 데이터에 액세스해야 하는 경우 반드시 사용자의 허가를 요청해야 합니다. 

자세한 내용은 [Privacy(개인정보 보호)](https://developer.apple.com/design/human-interface-guidelines/privacy)를 참조하고 [SceneReconstructionProvider](https://developer.apple.com/documentation/arkit/scenereconstructionprovider) 개발자 문서를 참조하세요.

#### 가상 객체를 주변 환경과 혼합할 수 있는 앱에서는 `PassThrough`가 완전히 가려지지 않도록 도와주세요. 
사람들은 종종 `PassThrough`의 존재를 통해 주변에서 조심스럽게 움직일지 여부를 결정합니다.

가상 객체를 주변에 있는 실제 객체가 보이지 않도록 배치할 수 있다면 사람들은 주변에서 이동하는 것이 어려울 수 있다는 사실을 깨닫지 못할 수 있습니다.

이러한 상황을 피하려면 올바른 API를 사용하여 몰입형 환경을 구현해야 사람들이 움직일 때 시스템이 적절하게 반응할 수 있습니다. [ImmersionStyle](https://developer.apple.com/documentation/SwiftUI/ImmersionStyle) 개발자 문서를 참조하세요.

#### 사람들의 시각적 편안함을 염두에 두어야 합니다.
예를 들어, 앱이 전체 공간에서 실행되는 동안 3D 콘텐츠를 어디에나 배치할 수 있지만, 사람들의 [field of view(시야)](https://developer.apple.com/design/human-interface-guidelines/spatial-layout#Field-of-view) 내에 배치하는 것을 선호합니다.

또한 앱이 전체 공간에서 실행되는 동안에는 사람들이 익숙한 기준 프레임에 익숙하지 않을 수 있으므로 모션을 편안한 방식으로 표시해야 합니다. 자세한 내용은 [Motion](https://developer.apple.com/design/human-interface-guidelines/motion)을 참조하세요.

### 플랫폼 지원 사항
- iOS, iPadOS, macOS, tvOS, watchOS 에서는 해당 내용이 제공되지 않습니다.

---

### 연관 내용
- [Spatial layout](https://developer.apple.com/design/human-interface-guidelines/spatial-layout)
- [Motion](https://developer.apple.com/design/human-interface-guidelines/motion)

### 개발자 문서 참고
- [Creating fully immersive experiences in your app](https://developer.apple.com/documentation/visionOS/creating-fully-immersive-experiences)
- [Incorporating real-world surroundings in an immersive experience](https://developer.apple.com/documentation/visionOS/incorporating-surroundings-in-an-immersive-experience)
- [Immersive spaces](https://developer.apple.com/documentation/SwiftUI/Immersive-spaces)

### 영상

| [Principles of spatial design](https://developer.apple.com/videos/play/wwdc2023/10072) | [Explore immersive sound design](https://developer.apple.com/videos/play/wwdc2023/10271) | [Design spatial SharePlay experiences](https://developer.apple.com/videos/play/wwdc2023/10075)
| -------- | -------- | -------- |
| ![](https://i.imgur.com/PD74ZGq.png) | ![](https://i.imgur.com/TjJ9YrZ.png) |  ![](https://i.imgur.com/7zOSV1g.png) |