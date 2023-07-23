# Spatial layout
[원문 링크](https://developer.apple.com/design/human-interface-guidelines/spatial-layout)

## Spatial Layout을 사용하면 Apple Vision Pro의 무한한 캔버스를 활용하고 콘텐츠를 매력적이고 편안한 방식으로 표현할 수 있습니다.

![](https://i.imgur.com/5BDRZ2y.png)

## Field-of-view
시야(field of view)는 고개를 움직이지 않고 볼 수 있는 공간입니다. Vision Pro를 착용한 상태에서 개인의 시야 크기는 라이트 씰을 구성하는 방식과 주변 시력의 정도와 같은 요인에 따라 달라집니다.

![](https://i.imgur.com/90AcD8V.png)

> 중요
> 
> 시스템은 사용자의 시야 (field of view) 정보를 제공하지 않습니다.


- ### 중요한 콘텐츠를 시야 중앙에 배치하세요
기본적으로 visionOS는 앱을 사용자 바로 앞에서 실행하여 사용자의 시야 내에 배치합니다. 사람들이 장시간 콘텐츠와 상호 작용해야 하는 경우, 콘텐츠를 시야 내에 편안하게 배치하고 싶을 것입니다.


#### 똑바로 봤을 경우
https://github.com/i-colours-u/Human-Interface-Guidelines-KR/assets/60260284/f9f1f040-a75c-4aee-8da5-0c3889795780

#### 비스듬히 봤을 경우
https://github.com/i-colours-u/Human-Interface-Guidelines-KR/assets/60260284/5c556f03-8c65-4efa-a7bc-96b214e75720

- ### 콘텐츠를 착용자의 머리에 고정하지 마세요. 
일반적으로 앱이 시야에 들어오는 것을 원하지만, 콘텐츠를 고정시켜 정면에 고정된 상태로 유지하면 특히 콘텐츠가 시야를 많이 가리고 주변 환경의 안정성을 떨어뜨리는 경우 사용자가 갇힌 느낌, 답답함, 불편함을 느낄 수 있습니다. 

대신 콘텐츠를 사람들의 공간에 고정하여 자연스럽게 주변을 둘러보고 다양한 위치에서 다양한 사물을 볼 수 있는 자유를 제공하세요.


## Depth
사람들은 거리, 오클루전(occlusion), 그림자와 같은 시각적 단서에 의존하여 깊이를 인식하고 주변 환경을 이해합니다. 

Vision Pro에서는 시스템이 색온도, 반사, 그림자와 같은 시각 효과를 자동으로 사용하여 사람들이 가상 콘텐츠의 깊이를 인식할 수 있도록 지원합니다. 

공간에서 가상 오브젝트를 움직이거나 오브젝트에 대한 상대적인 위치를 변경하면 시각 효과가 오브젝트의 겉보기 깊이를 변경하여 더욱 생생한 경험을 제공합니다.

> 오클루전(occlusion): 빛의 차폐 정도를 의미함. 예를 들어, 방의 구석 부분은 훨씬 더 어둡고, 중앙 부분은 훨씬 더 밝은 현상을 의미함


사람들은 어떤 각도에서든 콘텐츠를 볼 수 있으므로 표준 창에서도 인터페이스 전체에 약간의 깊이를 더하면 더욱 자연스럽게 보일 수 있습니다.

SwiftUI를 사용하면 2D 창에서 보기에 시각 효과를 추가하여 깊이감이 있는 것처럼 보이도록 합니다. 더 자세히 보고 싶다면 [Adding 3D content to your app(앱에 3D 컨텐츠 추가하기)](https://developer.apple.com/documentation/visionOS/adding-3d-content-to-your-app) 개발자 문서를 참조하세요.

![](https://i.imgur.com/i4Z3rAK.jpg)


추가 깊이가 있는 콘텐츠를 표시해야 하는 경우 [RealityKit](https://developer.apple.com/documentation/RealityKit)을 사용하여 3D 객체를 만들 수 있습니다.
3D 객체를 어디에나 표시하거나 3D 콘텐츠를 표시하는 컴포넌트인 `volume`을 사용할 수 있습니다. 
volume은 창과 비슷하지만 눈에 보이는 프레임이 없습니다. 자세한 내용은 [Volumes](../Components/Presentation/Windows#Volumes)을 참조하십시오.

https://github.com/i-colours-u/Human-Interface-Guidelines-KR/assets/60260284/7b2f11fb-68fe-4748-a371-57b6968ed516


- ### 콘텐츠의 깊이를 정확하게 전달할 수 있는 시각적 단서를 제공하세요. 
시각적 단서가 누락되거나 실제 경험과 충돌하면 사람들은 시각적으로 불편함을 느낄 수 있습니다.

- ### 깊이를 사용하여 계층 구조를 전달하세요.
깊이는 개체가 주변 콘텐츠에서 눈에 띄게 보이도록 하여 더 눈에 띄게 만듭니다. 예를 들어 시트가 창 위에 나타나면 창이 Z축을 따라 뒤로 물러나면서 시트가 앞으로 나와 시각적으로 눈에 띄게 되는 등 사람들은 깊이의 변화를 알아차리는 경향이 있습니다.

- ### 일반적으로 텍스트에 깊이를 추가하지 마십시오.
배경 위에 떠 있는 것처럼 보이는 텍스트는 읽기 어렵기 때문에 속도가 느려지고 때때로 시력에 불편함을 줄 수 있습니다.

- ### 깊이가 가치를 더하는지 확인하세요. 
일반적으로 깊이는 명확하고 즐거움을 주기 위해 사용하는 것이지 모든 곳에 사용할 필요는 없습니다. 

디자인에 깊이를 더할 때는 사물의 크기와 상대적 중요도에 대해 생각해 보세요. 깊이는 tab bar나 toolbar를 창에서 돋보이게 만드는 등 앱에서 크고 중요한 요소를 시각적으로 구분하는 데 유용하지만, 작은 개체에는 잘 작동하지 않을 수 있습니다. 

예를 들어, 배경에서 버튼의 기호를 돋보이게 하기 위해 깊이를 사용하면 버튼의 가독성이 떨어지고 사용하기가 어려워질 수 있습니다. 또한 앱 전체에서 얼마나 자주 다른 깊이를 사용하는지 검토하세요. 사람들은 각각의 깊이 차이를 인식하기 위해 눈의 초점을 다시 맞춰야 하는데, 너무 자주 또는 빠르게 초점을 맞추면 피곤할 수 있습니다.

## Scale
visionOS는 두 가지 유형의 scale을 정의하여 깊이감을 유지하면서 사용성을 최적화합니다.

`Dynamic scale(동적 배율)`은 콘텐츠가 사람과의 거리에 관계없이 편안하게 가독성을 유지하고 상호 작용할 수 있도록 도와줍니다. 특히, visionOS는 window가 착용자로부터 멀어지면 자동으로 창 배율을 높이고 창이 가까워지면 배율을 낮추어 모든 거리에서 window가 동일한 크기를 유지하는 것처럼 보이도록 합니다.

https://github.com/i-colours-u/Human-Interface-Guidelines-KR/assets/60260284/4242f82f-ea9b-47e3-9313-9dac8d167c19

---

`Fixed scale(고정 배율)`은 물체가 사람과의 거리에 관계없이 동일한 배율을 유지한다는 의미입니다. 고정 배율 객체는 Z축을 따라 뷰어에서 멀어질수록 더 작게 표시되며, 이는 사람의 실제 주변 환경에 있는 객체가 가까이 있을 때보다 멀리 있을 때 더 작게 보이는 것과 유사합니다.

https://github.com/i-colours-u/Human-Interface-Guidelines-KR/assets/60260284/1c0c73df-c329-4ae1-8062-50816d638081

---

visionOS가 아닌 다른 플랫폼에서는 2D 디스플레이의 [resolution(해상도)](https://developer.apple.com/design/human-interface-guidelines/images#Resolution)에 따라 달라질 수 있는 픽셀 수로 점(point)을 정의하고 있지만, visionOS에서는 동적 스케일링 및 깊이 표현을 지원하기 위해 점(point)을 각도로 정의합니다.

#### 가상 객체를 실제 객체와 똑같이 보이게 하려면 고정 배율을 사용하는 것이 좋습니다.
예를 들어, 사람들이 자신의 공간에서 제품을 볼 때 더욱 사실적으로 보이도록 제공하는 제품의 실제 크기 축척을 유지하고 싶을 수 있습니다. 

인터랙티브 콘텐츠는 가까워지거나 멀어질 때 사용성을 유지하기 위해 스케일을 조정해야 하므로 고정 스케일을 적게 적용하고 필요한 비인터랙티브 객체를 위해 남겨 두는 것이 좋습니다.

## Best practices

- ### 너무 많은 창을 표시하지 마세요. 
	창이 너무 많으면 주변 환경이 가려져 사람들이 압도당하고 답답함을 느끼며 심지어 불편함을 느낄 수 있습니다. 또한 많은 창 크기를 조정하거나 위치를 변경하지 않고는 사람들이 원하는 콘텐츠에 집중하기 어려울 수 있습니다.

- ### 표준적이고 간접적인 제스처를 우선시하세요. 
	사람들은 시야에 손을 대지 않고도 간접적인 제스처를 취할 수 있습니다. 반면 직접 제스처를 사용하려면 손가락으로 가상 개체를 터치해야 하는데, 특히 개체가 시야에 있거나 시야 위에 있는 경우 피곤할 수 있습니다. visionOS에서는 간접 제스처를 사용하여 이미 알고 있는 표준 제스처를 수행합니다. 간접 제스처를 우선순위로 지정하면 사람들은 거리에 상관없이 초점을 맞출 수 있는 모든 물체와 상호 작용할 수 있습니다. 직접 제스처를 지원하는 경우 짧은 시간 동안 자세히 살펴보거나 조작해야 하는 가까운 물체에 적용해야 합니다. 자세한 내용은 [Gestures > visionOS](https://developer.apple.com/design/human-interface-guidelines/gestures#visionOS)을 참조하세요.

- ### 디지털 크라운을 통해 사용자의 시야에 최신 창을 표시할 수 있습니다.
	사람들이 움직이거나 고개를 돌리면 원하는 위치에 콘텐츠가 더 이상 표시되지 않을 수 있습니다. 
	이 경우 사람들은 눈앞에 있는 콘텐츠를 최신 상태로 표시하고 싶을 때 [Digital Crown](../Inputs/Digital_Crown)을 누를 수 있습니다. 앱은 이 동작을 지원하기 위해 아무것도 할 필요가 없습니다.

- ### 사람들이 쉽게 집중할 수 있도록 인터랙티브 구성 요소 주변에 충분한 공간을 확보하세요. 
	사용자가 [눈](https://developer.apple.com/design/human-interface-guidelines/eyes)을 사용하여 인터랙티브 요소에 [focus(초점)](https://developer.apple.com/design/human-interface-guidelines/focus-and-selection)을 맞추면 visionOS는 시각적 호버 효과를 표시하여 원하는 요소임을 확인할 수 있도록 지원합니다. 인터랙티브 요소 주위에 충분한 공간을 확보하여 쉽고 편안하게 초점을 맞출 수 있도록 하는 동시에 호버 효과로 인해 다른 콘텐츠가 가려지는 것을 방지하는 것이 중요합니다. 예를 들어, [buttons](https://developer.apple.com/design/human-interface-guidelines/buttons#visionOS)의 중심이 60포인트 이상 떨어져 있도록 배치합니다.

- ### 사람들이 신체적 움직임을 최소화하거나 전혀 하지 않고 앱을 사용할 수 있도록 하세요. 
신체적 움직임이 필수적인 경우가 아니라면, 모든 사람이 고정된 상태에서 앱을 즐길 수 있도록 하세요.

- ### 바닥을 활용하여 대형 몰입형 경험을 배치할 수 있습니다.
몰입형 경험에 바닥에서 위로 확장되는 콘텐츠가 포함된 경우 평평한 수평면(flat horizontal)을 사용하여 콘텐츠를 배치합니다. 이 평면을 바닥과 정렬하면 주변 환경과 매끄럽게 어우러져 보다 직관적인 경험을 제공할 수 있습니다.

visionOS의 window 및 volume에 대해 자세히 알아보려면 [indows > visionOS](https://developer.apple.com/design/human-interface-guidelines/windows#visionOS)를 참조하고, 창 내에 콘텐츠를 배치하는 방법에 대한 지침은 [Layout > visionOS](https://developer.apple.com/design/human-interface-guidelines/layout#visionOS)를 참조하세요.

## 플랫폼 고려사항
- iOS, iPadOS, watchOS, tvOS, watchOS에는 해당되지 않습니다.



---

### 연관 내용
- [Eyes](https://developer.apple.com/design/human-interface-guidelines/eyes)
- [Layout](https://developer.apple.com/design/human-interface-guidelines/layout)
- [Immersive experiences](https://developer.apple.com/design/human-interface-guidelines/immersive-experiences)

### 개발자 문서 참고
- [Presenting windows and spaces](https://developer.apple.com/documentation/visionOS/presenting-windows-and-spaces)
- [Positioning and sizing windows](https://developer.apple.com/documentation/visionOS/positioning-and-sizing-windows)
- [Adding 3D content to your app](https://developer.apple.com/documentation/visionOS/adding-3d-content-to-your-app)

### 영상

| [Design for spatial user interfaces](https://developer.apple.com/videos/play/wwdc2023/10076) | [Principles of spatial design](https://developer.apple.com/videos/play/wwdc2023/10072) | [Design for spatial input](https://developer.apple.com/videos/play/wwdc2023/10073) |
| -------- | -------- | -------- |
| ![](https://i.imgur.com/kTIL2Ke.png)|     ![](https://i.imgur.com/PD74ZGq.png) | ![](https://i.imgur.com/c47Exth.png)|

