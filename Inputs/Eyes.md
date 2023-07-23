
# Eyes
[원본 링크](https://developer.apple.com/design/human-interface-guidelines/eyes)

### visionOS에서는 사람들이 가상의 물체를 바라보며 초점을 맞추고 상호작용할 수 있는 대상으로 식별합니다.

![](https://i.imgur.com/or8kxnD.png)


사람들이 대화형 개체를 보면 visionOS가 해당 개체를 강조 표시하여, 내가 보고있는 것이 원하는 개체인지 확인할 수 있도록 시각적 피드백을 제공합니다.

시각적 피드백 또는 호버 효과는 개체에 초점이 맞춰져 있음을 나타내는 용도로 사용합니다.

사용자는 탭과 같은 [indirect gesture(간접적인 제스처)](https://developer.apple.com/design/human-interface-guidelines/gestures#visionOS)를 사용하여 해당 개체와 상호 작용할 수 있습니다. 

예를 들어 Safari에서 뒤로 버튼을 보고 초점을 맞춘 다음 탭하여 이전 웹 페이지로 돌아갈 수 있습니다. 마찬가지로 사용자는 사진 라이브러리에서 개별 사진을 보고 탭하여 열 수 있습니다.  
  
드물게는 초점을 맞춘 후 시스템이 자동으로 구성 요소의 확장된 보기를 표시할 수 있습니다. 

예를 들어 사용자가 탭 표시줄을 볼 때 컴포넌트의 크기가 조정되어 각 탭 옆에 텍스트 레이블이 표시됩니다. 

이 시나리오에서는 탭 표시줄이 확장되기 전에 개별 탭이 강조 표시되어 레이블이 표시되기 전에 사용자가 탭을 선택할 수 있습니다. 시스템에서 제공하는 버튼을 클릭하면 툴팁을 표시할 수도 있습니다.


> 중요
> 
> 사용자의 개인 정보를 보호하기 위해 visionOS는 사용자가 탭하기 전에 어디를 보고 있는지에 대한 직접적인 정보를 제공하지 않습니다. 시스템에서 제공하는 구성 요소를 사용하는 경우, 사용자가 구성 요소를 탭할 때 visionOS가 자동으로 알려줍니다. 자세한 내역은 [Adopting best practices for privacy and user preferences](https://developer.apple.com/documentation/visionOS/adopting-best-practices-for-privacy) 문서를 참조하세요.

focus에 대한 자세한 지침을 확인하고 싶은 경우, [Focus and selection](https://developer.apple.com/design/human-interface-guidelines/focus-and-selection) 문서를 참조하세요.

## Best practices

- ### 항상 사람들이 앱과 상호 작용할 수 있는 다양한 방법을 제공하세요. 
사람들이 기기와 상호 작용하는 방식을 개인화하기 위해 사용하는 접근성 기능을 지원하도록 앱을 디자인하세요. 지침은 [Accessibility(접근성)](https://developer.apple.com/design/human-interface-guidelines/accessibility)을 참조하세요.

- ### 시각적으로 편안하게 디자인하세요. 
사람들이 사용해야 하는 개체가 [filed of view(시야)](../Foundations/Spatial-layout.md#Field-of-view)내에 있는지 확인하여 사람들이 주요 작업을 수행할 수 있도록 도와주세요. 

앱이 공유 공간에서 실행되는 경우 시스템은 창과 볼륨을 편리한 위치에 자동으로 배치하고,

앱이 전체 공간에서 실행되는 경우 앱 콘텐츠를 적절하게 배치할 수 있도록 사람의 머리 자세에 대한 정보에 대한 액세스를 요청해야 할 수 있습니다. 

또한 넓은 영역이나 여러 단계의 깊이를 통해 사람들이 여러 번 빠르게 눈을 조정하지 않도록 하면 시각적으로 편안한 환경을 제공할 수 있습니다. 자세한 내용은 [Depth](..Foundations/Spatial-layout.md#Depth)를 참조하세요.

- ### 콘텐츠를 편안한 시청 거리에 배치합니다. 
예를 들어, 사람들이 오랜 시간 동안 콘텐츠를 읽거나 참여하는 동안 편안함을 유지하도록 하려면 콘텐츠를 최소 1미터 이상 떨어진 곳에 배치하세요. 

일반적으로 콘텐츠를 잠시만 보거나 상호 작용할 것이 아니라면 콘텐츠를 너무 가까이 배치하지 않는 것이 좋습니다.

- ### 아이템 주변에 충분한 공간을 확보하여 사람들이 아이템에 쉽게 집중할 수 있도록 하세요. 

시선은 자연적으로 한 곳을 바라보는 동안에도 방향을 조금씩 빠르게 조정하는 경향이 있기 때문에 UI 개체를 한데 모으면 다른 곳으로 이동하지 않고는 한 개체를 보기가 어려울 수 있습니다. 

각 항목의 경계에 최소 16포인트의 여백을 사용하거나 항목의 중심이 항상 60포인트 이상 떨어져 있도록 배치하여 대화형 항목 사이에 충분한 공간을 확보할 수 있습니다. 

추가적인 레이아웃 가이드는 [Layout](https://developer.apple.com/design/human-interface-guidelines/layout) 및 [Spatial layout](..Foundations/Spatial-layout.md)을 참조하세요.


- ### 미묘한 시각적 단서를 사용하여 사람들이 가장 원할 것 같은 항목을 보도록 유도하세요. 
예를 들어, 아이템을 시야 중앙 근처에 배치하거나 부드러운 움직임, 대비 증가, 색상이나 배율의 변화와 같은 기법을 사용하여 사람들의 주의를 끄는 것이 효과적일 수 있습니다. 

일반적으로 화려하거나 거칠지 않으면서도 눈에 띄는 단서를 선호합니다.

- ### 시각적 방해 요소를 최소화하세요. 
시각적 소음이 많으면 사람들이 원하는 물체를 찾기가 어려울 수 있습니다.
시각적 움직임은 더욱 주의력을 분산시킬 수 있습니다: 사람들은 특히 주변 시야에서 움직임을 감지하면 자동으로 반응하는 경향이 있어 관심 있는 물체에 집중하기 어렵습니다.

- ### 시야를 가득 채우는 반복되는 패턴이나 텍스처를 사용하지 마세요. 
경우에 따라 사람의 눈은 패턴이나 텍스처의 여러 요소에 고정되어 요소가 서로 다른 깊이를 가진 것처럼 보일 수 있습니다. 이러한 효과를 방지하려면 패턴을 더 작은 영역에 사용하는 것이 좋습니다.

- ### 표준 UI 컴포넌트를 사용하는 것을 선호합니다. 
시스템에서 제공하는 컴포넌트는 사용자가 볼 때 일관된 시각적 피드백을 제공하고 초점을 맞췄을 때 일관되게 작동합니다. 사용자 지정 (커스텀) 컴포넌트가 시각적 피드백을 제공하기 위해 서로 다른 시각적 단서를 사용하는 경우, 사람들이 앱에서 이러한 컴포넌트가 어떻게 작동하는지 배우고 기억하기 어려울 수 있습니다.

- ### 일반적으로 대화형 항목은 둥근 모양으로 만듭니다. 
사람들의 시선은 도형의 모서리 쪽으로 쏠리는 경향이 있어 도형의 중앙에 초점을 맞추기가 어렵습니다. 항목의 모양이 둥글수록 사람들이 더 쉽게 초점을 맞출 수 있습니다.


## 플랫폼 고려사항
- iOS, iPadOS, watchOS, tvOS, watchOS에는 해당되지 않습니다.

---


### 연관 내용
- [Focus and selection](https://developer.apple.com/design/human-interface-guidelines/focus-and-selection)
- [Immersive experiences](../Foundations/Immersive_experiences)
- [Gestures](https://developer.apple.com/design/human-interface-guidelines/gestures)
- [Spatial layout](..Foundations/Spatial-layout.md)

### 개발자 문서 참고
- [Adopting best practices for privacy and user preferences](https://developer.apple.com/documentation/visionOS/adopting-best-practices-for-privacy)
### 영상

| [Design for spatial input](https://developer.apple.com/videos/play/wwdc2023/10073) | [Design considerations for vision and motion](https://developer.apple.com/videos/play/wwdc2023/10078) | [Principles of spatial design](https://developer.apple.com/videos/play/wwdc2023/10072) |
| -------- | -------- | -------- |
| ![](https://i.imgur.com/jxMan0M.png)  |    ![](https://i.imgur.com/2HWO6zp.png) | ![](https://i.imgur.com/PD74ZGq.png) |

