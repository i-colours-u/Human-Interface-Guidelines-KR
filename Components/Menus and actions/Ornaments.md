# Ornaments
[원본 링크](https://developer.apple.com/design/human-interface-guidelines/ornaments)

### 비전OS에서 `Ornaments`는 `window` 내용을 복잡하게 만들거나 가리지 않고 `window`과 관련된 제어 및 정보를 표시합니다.

![](https://i.imgur.com/ieNE6jN.png)


`ornaments`은 연결된 `window`와 평행한 평면에서 Z축을 따라 약간 앞쪽에 떠 있습니다. 연결된 `window`가 이동하면 `ornaments`도 함께 이동하여 상대적인 위치를 유지하며, `window`의 콘텐츠가 스크롤되는 경우 `ornament`의 컨트롤이나 정보는 변경되지 않고 유지됩니다.

`ornament`는 `window`의 모든 가장자리에 표시할 수 있으며 버튼, 세그먼트 컨트롤 및 기타 보기와 같은 UI 구성 요소를 포함할 수 있습니다. 시스템 `ornament`를 사용하여 [toolbars](https://developer.apple.com/design/human-interface-guidelines/toolbars), [tab bars](https://developer.apple.com/design/human-interface-guidelines/tab-bars), 비디오 재생 컨트롤과 같은 구성 요소를 만들고 관리하며, `ornament`를 사용하여 사용자 지정 구성 요소를 만들 수 있습니다.


## Best practices

- ### 자주 사용하는 컨트롤이나 정보를 `window`을 어지럽히지 않는 일관된 위치에 표시하려면 `ornament`를 사용하는 것이 좋습니다. 
	`ornament`는 `window` 가까이에 있기 때문에 사람들은 항상 어디에서 찾을 수 있는지 알 수 있습니다. 예를 들어 음악에서는 `ornament`를 사용하여 지금 재생 중 컨트롤을 제공함으로써 이러한 컨트롤이 찾기 쉬운 예측 가능한 위치에 유지되도록 합니다.

- ### 보조 컨트롤과 정보를 제공하려면 별도의 `window`이 아닌 `ornament`를 선호합니다. 
	`ornament`를 사용하여 관련 기능을 제공하면 사용자가 별도로 관리해야 하는 추가 `window`을 열지 않아도 됩니다.

- ### 일반적으로 `ornament`을 계속 표시합니다. 
	동영상을 보거나 사진을 볼 때와 같이 사람들이 `window`의 콘텐츠에 몰입할 때는 `ornament`을 숨기는 것이 합리적일 수 있지만, 대부분의 경우 사람들은 `ornament`을 통해 일관되게 컨트롤에 액세스할 수 있는 것을 좋아합니다.

- ### `ornament`의 너비를 관련 `window`의 너비와 같거나 좁게 유지하는 것을 목표로 하세요. 
	`ornament`을 `window`보다 넓게 만들면 `window` 옆의 탭 표시줄이나 기타 세로 콘텐츠를 가릴 수 있습니다.

- ### `ornament`에 테두리가 없는 버튼을 사용하는 것이 좋습니다. 
	기본적으로 `ornament`의 배경은 [glass](https://developer.apple.com/design/human-interface-guidelines/materials#visionOS)이므로 버튼을 배경에 직접 배치하면 테두리가 보이지 않을 수 있습니다. 사람들이 `ornament`에서 테두리가 없는 버튼을 보면 시스템에서 자동으로 호버 효과를 적용합니다(자세한 내역은 [Eyes](https://developer.apple.com/design/human-interface-guidelines/eyes)을 참조하세요).

- ### 사용자 지정 구성 요소를 만들어야 하는 경우가 아니라면 시스템에서 제공하는 `toolbar`과 `tab bar`을 사용하세요. 
	visionOS에서는 `toolbar`과 `tab bar`가 자동으로 `ornament`으로 표시되므로 이러한 구성 요소를 만들기 위해 추가적으로 `ornament` 요소를 사용할 필요가 없습니다. [Toolbars](https://developer.apple.com/documentation/SwiftUI/Toolbars)와 [TabView](https://developer.apple.com/documentation/SwiftUI/TabView) 개발자 문서를 참조하세요.


### 플랫폼 고려 사항
- iOS, iPadOS, macOS, watchOS, tvOS는 해당되지 않습니다.

---
### 연관 내용
- [Layout](https://developer.apple.com/design/human-interface-guidelines/layout)

### 개발자 문서 참고
- [ornament(visibility:attachmentAnchor:contentAlignment:ornament:)](https://developer.apple.com/documentation/SwiftUI/View/ornament(visibility:attachmentAnchor:contentAlignment:ornament:))

### 영상

| [Design for spatial user interfaces](https://developer.apple.com/videos/play/wwdc2023/10076) | [Principles of spatial design](https://developer.apple.com/videos/play/wwdc2023/10072) |
| -------- | -------- |
| ![](https://i.imgur.com/kTIL2Ke.png)|     ![](https://i.imgur.com/PD74ZGq.png) 

