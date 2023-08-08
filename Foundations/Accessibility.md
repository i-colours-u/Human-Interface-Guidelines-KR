# Accessibility
[원문 링크](https://developer.apple.com/design/human-interface-guidelines/accessibility)

## 사람들은 Apple의 접근성 기능을 사용하여 자신에게 적합한 방식으로 기기와 상호 작용하는 방식을 개인화할 수 있습니다.

![](https://i.imgur.com/swqPAx8.png)

접근성이 뛰어난 앱이나 게임은 접근성 맞춤 설정을 지원하며, 기능이나 기기 사용 방식에 관계없이 모든 사람이 훌륭한 경험을 할 수 있도록 설계되었습니다.

약 7명 중 1명은 세상 및 디바이스와 상호 작용하는 방식에 영향을 미치는 장애를 가지고 있습니다. 사람들은 나이와 기간에 관계없이 다양한 수준의 장애를 경험할 수 있습니다. 예를 들어, 낙상으로 인한 손목 부상이나 과도한 사용으로 인한 음성 손실과 같은 상황적 장애는 거의 모든 사람이 다양한 시간에 디바이스와 상호 작용하는 방식에 영향을 미칠 수 있습니다.

## Best practices

- ### 접근성을 염두에 두고 디자인하세요. 
	접근성은 단순히 장애가 있는 사람이 정보를 이용할 수 있도록 하는 것이 아니라, 능력이나 상황에 관계없이 모든 사람이 정보를 이용할 수 있도록 하는 것입니다. 접근성을 염두에 두고 앱을 디자인한다는 것은 단순성과 인지 가능성을 우선시하고 모든 디자인 결정을 검토하여 다른 능력을 가지고 있거나 다른 방식으로 디바이스와 상호 작용하는 사람들을 배제하지 않도록 하는 것을 의미합니다.

- ### 단순성
	친숙하고 일관된 상호 작용을 지원하여 복잡한 작업도 간단하고 쉽게 수행할 수 있습니다.

- ### 인지 할 수 있어야 합니다.
	시각, 청각, 촉각 등 어떤 방식으로든 모든 콘텐츠를 인지할 수 있어야 합니다.

- ### 개인화를 지원하세요.
	사람들이 어떤 상황과 지원되는 모든 기기에서든 경험을 즐길 수 있도록 기기 방향, 디스플레이 크기, 해상도, 색 영역, 분할 보기 등 다양한 환경에 맞게 환경을 설계해야 합니다. 최소한의 추가 노력으로 사람들이 기기와 상호 작용하는 방식을 개인화하기 위해 사용하는 접근성 기능을 지원하도록 앱을 디자인할 수 있습니다.
	 
	표준 컴포넌트를 사용하여 인터페이스를 구현하면 텍스트와 컨트롤이 굵은 텍스트, 큰 텍스트, 색상 반전, 대비 증가와 같은 여러 접근성 설정에 자동으로 맞춰집니다.

- ### 앱 또는 게임의 접근성을 검증하고 테스트하세요.
	검증을 통해 경험의 모든 요소를 검사하고 수정해야 할 포괄적인 문제 목록을 제공합니다. 테스트를 통해 모든 사람이 기기와 상호 작용하는 방식에 관계없이 앱에서 가장 중요한 작업을 완료할 수 있도록 보장할 수 있습니다.
	 
	접근성 기능을 켠 상태에서 중요한 사용자 흐름(유저 플로우)을 테스트하면 다양한 방식으로 디바이스와 상호 작용할 때의 어려움을 이해할 수 있습니다. 또한 앱이 우수한 사용자 경험을 제공하지 못할 수 있는 부분을 발견할 수 있습니다.
	 
	예를 들어 소셜 미디어 앱의 일반적인 사용자 흐름은 "답글 달기"일 수 있습니다. 이 플로우를 구성하는 작업에는 다음이 포함될 수 있습니다:
	
	- 게시된 댓글 읽기
	- 응답할 댓글 고르기.
	- 답글 뷰 열기
	- 답글 편집 및 작성하기
	- 답글 게시하기
	  
	  앱이나 게임의 각 중요한 유저 플로우에 대해 보이스오버, 모션 줄이기(저사양 디바이스를 위한 애니메이션 줄이기) 또는 큰 텍스트 크기와 같은 접근성 기능을 켜고 앱의 모든 작업을 어려움 없이 완료할 수 있는지 확인합니다. 발견한 문제를 해결한 후에는 다른 접근성 기능을 켜고 사용자 플로우를 다시 실행합니다. 앱 또는 게임을 감사, 테스트 및 수정하는 데 도움을 받으려면 Xcode의 `Accessibility Inspector`를 사용하는 것이 좋습니다.

## 상호작용

보이스오버, 보조 터치, 포인터 제어, 스위치 제어와 같은 보조 기술은 사람들이 디바이스와 상호 작용할 수 있는 방법을 확장합니다. 이러한 기술은 시스템에서 제공하는 상호 작용과 통합되므로 앱에서 시스템 상호 작용을 올바르게 지원하는 것이 필수적입니다.

## 제스처

- ### 플랫폼 제스처를 재정의하지 마세요. 
사람들은 아래로 스와이프하여 알림 센터를 표시하는 것과 같이 시스템 기능을 대상으로 하는 제스처가 사용 중인 앱과 관계없이 작동하기를 기대합니다.

- ### 일반적인 상호 작용에는 단순화된 제스처를 선호합니다.
여러 손가락 또는 여러 손을 사용하는 제스처, 길게 누르기, 반복적인 동작이 필요한 제스처와 같은 복잡한 제스처는 많은 사람들에게 어려울 수 있습니다. 가능한 한 간단한 제스처를 사용하면 앱과 상호 작용하는 모든 사람의 경험이 향상됩니다.

- ### 제스처 기반 작업을 수행할 수 있는 대체 방법을 제공하세요. 
특정 제스처를 수행할 수 없는 사용자를 위한 옵션을 포함하세요. 예를 들어, 제스처를 사용하여 표의 행을 삭제할 수 있는 경우 편집 모드를 통해 항목을 삭제하거나 항목 세부 정보 보기에서 삭제 버튼을 제공하여 항목을 삭제할 수 있는 방법을 제공할 수도 있습니다.

| 편집 모드를 통해 항목 삭제                                                                                                                                                                                                                             | 스와이프 제스처를 통해 항목 삭제                                                                                                                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ![An illustration of a list-based app on iPhone. The list is in edit mode, and each list item displays a circular Delete button on the left.](https://docs-assets.developer.apple.com/published/0ef69eb127a1f8225ebbd5ba6786fb63/tap-to-delete@2x.png) | ![An illustration of a list-based app on iPhone. The Delete button for the first item is revealed, as if someone swiped the item to the left.](https://docs-assets.developer.apple.com/published/7180d8c6c9a19832cebdfb515b0dbfea/swipe-to-delete@2x.png) |


- ### 가능하면 두 가지 이상의 물리적 상호 작용 유형을 통해 앱의 핵심 기능에 액세스할 수 있도록 하세요.
예를 들어 iPhone 및 iPad의 카메라에서는 화면의 버튼을 탭하거나 기기의 볼륨 작게 버튼을 눌러 사진을 찍을 수 있습니다. 이러한 대체 상호 작용은 모든 사람이 더 편리하게 사진을 찍을 수 있도록 할 뿐만 아니라, 그립 강도나 손재주가 부족한 사람들에게도 옵션을 제공합니다.

- ### 사용자 지정 제스처를 정의하는 경우, 사람들이 앱과 상호 작용할 수 있는 대체 방법을 제공하는 보조 기술을 지원해야 합니다. 
예를 들어, 포인터 컨트롤을 사용하면 손목, 검지 또는 머리 기반 포인터를 사용할 수 있고, 드웰 컨트롤을 사용하면 눈만 사용하여 개체를 선택하고 활성화할 수 있습니다. 보이스오버, 드웰 컨트롤, 스위치 컨트롤과 같은 기술을 지원하는 한 가지 방법은 사용자 지정 동작(`custom action`)을 구현하는 것입니다. 자세히 알아보고 싶다면, [`UIAccessibilityCustomAction`](https://developer.apple.com/documentation/uikit/uiaccessibilitycustomaction) 개발자 문서를 참조하세요.

> 드웰 컨트롤: 드웰 제어(Dwell Control): 일반적인 제어가 아닌 시선 또는 머리등 특정 부위 추적 기술을 사용해 마우스 동작을 수행하는 것.

- ### iOS 또는 iPadOS 앱에서 드래그 앤 드롭에 액세스할 수 있도록 설정하세요.
Accessibility API를 사용하여 앱에서 특정 개체가 드래그 대상임을 식별 할 수 있도록 지정하세요. 해당 항목을 지정한다면, 보조 기술을 통해 사람들이 항목을 드래그 앤 드롭하는 데 도움을 받을 수 있습니다. 자세한 내용은 [`accessibilityDragSourceDescriptors`](https://developer.apple.com/documentation/objectivec/nsobject/2891001-accessibilitydragsourcedescripto) 문서와, [`accessibilityDropPointDescriptors`](https://developer.apple.com/documentation/objectivec/nsobject/2891048-accessibilitydroppointdescriptor) 문서를 참조하세요.

## Buttons-and-controls
- ### 모든 컨트롤과 인터랙티브 요소에 충분히 큰 타겟을 지정합니다. 
예를 들어 터치스크린 기기에서 타겟의 크기는 최소 `44x44pt`여야 하며, 비전OS에서는 컨트롤의 중심이 최소 `60pt` 간격이 되도록 배치합니다. 거동이 불편한 사람들은 앱과 상호 작용할 수 있도록 더 큰 타겟이 필요합니다. 포인터를 사용하는 경우에도 모든 플랫폼에서 너무 작은 컨트롤과 상호 작용하는 것은 불편할 수 있습니다.

- ### 사용자 지정 요소(custom elements)의 접근성을 특성화하세요.
시스템 API를 사용하여 보조 기술에 구성 요소의 동작 방식을 알려줄 수 있습니다. 예를 들어 [`button`](https://developer.apple.com/documentation/uikit/uiaccessibilitytraits/1620194-button) 또는 [`NSAccessibilityButton`](https://developer.apple.com/documentation/appkit/nsaccessibilitybutton)을 사용하여 뷰를 버튼으로 특성화하면 VoiceOver가 뷰의 설명을 말한 다음 버튼이라는 단어를 말하여 뷰가 버튼처럼 작동한다는 것을 사용자에게 알릴 수 있습니다.

- ### 일관된 스타일 계층 구조를 사용하여 버튼의 상대적 중요성을 전달합니다. 
예를 들어 iOS, iPadOS 및 tvOS에서는 뷰에서 가장 가능성이 높은 작업을 수행하는 버튼에 시각적으로 눈에 잘 띄는 채워진 스타일을 사용하고 덜 중요한 작업을 수행하는 버튼에는 회색 또는 일반과 같이 덜 눈에 잘 띄는 스타일을 사용할 수 있습니다. (개발자 지침은 [`UIButton.Configuration`](https://developer.apple.com/documentation/uikit/uibutton/configuration)을 참조하세요.) visionOS에서 시스템 제공 버튼은 일반적으로 기본적으로 보이는 배경을 포함합니다. iOS, iPadOS, visionOS 및 macOS의 일부 버튼의 경우 버튼 모양을 켜서 활성 버튼을 주변 콘텐츠와 쉽게 구분할 수 있습니다.

- ### 시스템에서 제공하는 스위치 컴포넌트를 사용해보세요. 
SwiftUI에서는 토글의 위치와 색상으로 상태를 표시하는 스위치를 제공합니다. 그러나 일부 사용자에게는 레이블을 추가하면 스위치가 켜져 있는지 꺼져 있는지 더 쉽게 알 수 있습니다. 시스템에서 제공하는 스위치를 사용하는 경우 iOS, iPadOS, tvOS, visionOS 및 watchOS는 사용자가 켜기/끄기 레이블을 켜면 그 안에 문자가 자동으로 표시됩니다.

| on/off 레이블을 끈 경우 | on/off 레이블을 킨 경우 |
| ----------------------- | ----------------------- |
|           ![An illustration of two switches. The on/off labels are turned off.](https://docs-assets.developer.apple.com/published/a8ffdabefeb92d1f9c364a973ff3a9dc/switches-without-labels@2x.png)              |          ![An illustration of two switches. The on/off labels are turned on.](https://docs-assets.developer.apple.com/published/8020de55fd585edbf1d0733b518a7a7e/switches-with-labels@2x.png)               |


## 링크에 밑줄과 같은 색상 외에 시각적 힌트(표시)를 추가하는 것도 고려해 보세요.
 색상을 사용하여 링크를 식별하는 것은 좋지만 색상을 유일한 표시로 사용하면 색맹이나 인지 또는 상황 주의력 장애가 있는 사람은 구분을 인식하지 못할 수 있습니다.

## 유저 입력(User-input)
- ### 사람들이 타이핑이나 제스처 대신 음성으로 정보를 입력할 수 있도록 하세요. 
텍스트 입력 필드에 받아쓰기 버튼을 추가하면 사람들이 선호하는 입력 방법으로 음성을 선택할 수 있습니다. 사용자 지정 키보드를 만드는 경우 받아쓰기용 마이크 키를 포함해야 합니다.

- ### 음성만으로 중요한 작업을 수행할 수 있도록 Siri 또는 바로가기를 지원하세요. 
사람들이 앱에서 Siri 상호 작용을 사용하도록 돕는 방법에 대해 자세히 알아보려면 [Siri](https://developer.apple.com/design/human-interface-guidelines/siri)를 참조하세요.

- ### 가능하면 사람들이 일반 텍스트를 선택할 수 있도록 해주세요. 
많은 사람들이 번역 및 정의에 대한 입력으로 선택한 텍스트를 사용하는 데 의존합니다.

## 햅틱(Haptics)
- ### 사용 가능한 경우 시스템 정의 햅틱을 지원하세요. 
많은 사람들이 디스플레이를 볼 수 없을 때 앱과 상호 작용하기 위해 햅틱에 의존합니다. 예를 들어, 시스템 앱은 작업이 성공 또는 실패했거나 이벤트가 곧 발생할 때 사람들에게 알리기 위해 햅틱을 재생합니다. 사람들이 혼동하지 않도록 앱에서 시스템에서 정의한 햅틱을 **일관되게** 사용해야 합니다. 지침은 햅틱 재생하기를 참조하세요.

> 참고
> 
> 햅틱을 지원하지 않는 플랫폼에서는 사람들이 사용자 지정 개체와 상호 작용할 때 사운드와 같은 다른 방법을 사용하여 피드백을 제공하세요.

## VoiceOver
보이스오버는 보이는 콘텐츠에 대한 음성 설명을 제공하여 디스플레이를 볼 수 없을 때 정보를 얻고 탐색할 수 있도록 도와줍니다. visionOS에서 VoiceOver는 공간 오디오를 사용하여 접근 가능한 개체의 위치를 알려줍니다.
> 중요
> 
> visionOS에서 VoiceOver가 켜져 있으면 사용자 지정 제스처를 정의하는 앱은 기본적으로 손 입력을 수신하지 않습니다. 대신 사용자는 앱이 손 입력을 해석하는 것에 대해 걱정할 필요 없이 VoiceOver 제스처를 수행하여 앱을 탐색할 수 있습니다. VoiceOver의 직접 제스처 모드에서는 표준 제스처를 처리하지 않고 앱이 손 입력을 직접 처리하도록 합니다. [Improving accessibility support in your visionOS app](https://developer.apple.com/documentation/visionOS/improving-accessibility-support-in-your-app) 개발자 문서를 참조하세요.

## 컨텐츠 설명
- ### 의미를 전달하는 모든 이미지에 대체 설명을 제공하세요.
콘텐츠에 의미 있는 이미지를 설명하지 않으면 VoiceOver 사용자가 앱을 충분히 경험하지 못하게 됩니다. 유용한 설명을 작성하려면 이미지를 볼 수 있는 사람에게 자명하게 설명할 수 있는 내용을 보고하는 것부터 시작하세요. 보이스오버는 이미지와 캡션을 둘러싼 텍스트를 읽으므로 이미지 자체에서 전달되는 정보에 초점을 맞춰 설명하세요.


![A partial screenshot of a summary screen in the Activity app on iPhone. The activity rings element has a frame around it, representing the active element in VoiceOver.](https://docs-assets.developer.apple.com/published/c6b54e401411a6488486e5b960f05ab5/image-with-alt-text@2x.png)
> 이 화면의 경우, 대체 설명은 "Moving: 125 percent; Exercise: zero percent; Standing: 58 percent."입니다.

- ### 인포그래픽에 완전히 액세스할 수 있도록 하세요. 
인포그래픽이 전달하는 내용을 설명하는 간결한 설명을 제공하세요. 사람들이 인포그래픽과 상호 작용하여 더 많은 정보나 다른 정보를 얻을 수 있다면 VoiceOver 사용자도 이러한 상호 작용을 사용할 수 있도록 해야 합니다. 접근성 API는 사용자 지정 대화형 요소를 표현하는 방법을 제공하므로 보조 기술을 사용하는 데 도움이 될 수 있습니다.

- ### 이미지가 순전히 장식용이고 중요한 내용을 전달하기 위한 것이 아니라면 보조 기술에서 이미지를 숨기세요. 
보이스오버가 순전히 장식적인 이미지를 설명하도록 하면 사람들의 시간을 낭비하고 아무런 이점 없이 인지 부하만 가중시킬 수 있습니다.

- ### 각 페이지에 고유한 제목을 부여하고 정보 계층 구조에서 섹션을 식별할 수 있는 제목을 제공하세요. 
  사람들이 페이지에 도착하면 제목은 보조 기술을 통해 가장 먼저 접하는 정보입니다. 사람들이 앱의 구조를 쉽게 이해할 수 있도록 각 페이지마다 콘텐츠나 목적을 간결하게 설명하는 고유한 제목을 만드세요. 마찬가지로, 사람들이 각 페이지의 정보 계층 구조에 대한 마인드맵을 구축하는 데 도움이 되는 정확한 섹션 제목이 필요합니다.

- ### 모든 사람이 비디오 및 오디오 콘텐츠를 즐길 수 있도록 지원하세요. 
폐쇄 자막(Closed captions), 오디오 설명 및 자막을 제공하면 사람들이 자신에게 적합한 방식으로 오디오 및 비디오 콘텐츠를 활용할 수 있도록 도울 수 있습니다.

> Closed Caption: 자막의 표시 여부를 설정 할 수 있는 자막을 뜻함


Closed Caption은 사람들에게 비디오의 청각적 정보를 텍스트와 동등한 수준으로 제공합니다. 또한 Closed Caption을 사용하여 동일한 콘텐츠에 대해 여러 번역을 제공함으로써 시스템이 디바이스의 현재 설정과 일치하는 버전을 선택하도록 할 수도 있습니다. Closed Caption을 항상 사용할 수 있는 것은 아니므로 자막도 함께 제공하는 것이 중요합니다.

오디오 설명은 시각적으로만 표시되는 중요한 정보를 음성 내레이션으로 제공합니다.

Transcript은 청각 및 시각 정보를 모두 포함하여 동영상에 대한 완전한 텍스트 설명을 제공하므로 사람들이 다양한 방식으로 동영상을 즐길 수 있습니다.

개발자 가이드를 보고 싶다면, [Selecting Subtitles and Alternative Audio Tracks](https://developer.apple.com/documentation/avfoundation/media_playback/selecting_subtitles_and_alternative_audio_tracks) 문서를 참조하세요.

## Navigation
- ### VoiceOver 사용자가 모든 요소를 탐색할 수 있는지 확인하세요.
VoiceOver는 UI 요소의 접근성 정보를 사용하여 사람들이 각 요소의 위치와 해당 요소가 수행할 수 있는 작업을 이해하는 데 도움을 줍니다. 시스템에서 제공하는 UI 구성 요소에는 기본적으로 이 접근성 정보가 포함되어 있지만, 사용자가 정보를 제공하지 않으면 VoiceOver가 사용자 지정 요소를 검색하고 사용하는 데 도움을 줄 수 없습니다. 개발자 지침은 [Accessibility modifiers](https://developer.apple.com/documentation/SwiftUI/View-Accessibility)을 참조하세요.

- ### 요소의 그룹화, 순서 지정 또는 연결 방법을 지정하여 VoiceOver 환경을 개선하세요.
근접성, 정렬 및 기타 문맥적 단서는 시각 장애인이 보이는 요소 간의 관계를 인식하는 데 도움이 될 수 있지만 이러한 단서는 VoiceOver 사용자에게는 잘 작동하지 않습니다. 앱에서 요소 간의 관계가 시각적으로만 표시되는 부분이 있는지 살펴보고 이러한 관계를 VoiceOver에 적용하세요.

예를 들어, 아래 레이아웃은 각 문구가 그 위에 있는 이미지의 캡션임을 암시합니다. 그러나 각 이미지가 해당 문구와 함께 그룹화되어야 한다는 것을 VoiceOver에 알려주지 않으면 VoiceOver는 "다양한 망고가 들어 있는 큰 용기. 녹색 아티초크가 많이 들어 있는 큰 용기. 망고는 망기페라 속에 속하는 나무에서 나옵니다. 아티초크는 다양한 종류의 엉겅퀴에서 나옵니다." 보이스오버는 기본적으로 요소를 위에서 아래로 읽기 때문에 이런 일이 발생합니다. 개발자 지침은 [`shouldGroupAccessibilityChildren`](https://developer.apple.com/documentation/objectivec/nsobject/1615143-shouldgroupaccessibilitychildren)을 참조하세요.

![OGggCaX.png](https://i.imgur.com/OGggCaX.png)

- ### 표시되는 콘텐츠나 레이아웃이 변경되면 VoiceOver에 알리세요. 
콘텐츠나 레이아웃이 예기치 않게 변경되면 콘텐츠에 대한 머릿속 지도가 더 이상 정확하지 않다는 것을 의미하므로 VoiceOver 사용자는 매우 혼란스러워할 수 있습니다. VoiceOver 및 기타 보조 기술이 콘텐츠에 대한 이해를 업데이트하는 데 도움이 될 수 있도록 눈에 보이는 변경 사항을 보고하는 것이 중요합니다. 개발자 지침은 [`UIAccessibility.Notification`](https://developer.apple.com/documentation/uikit/uiaccessibility/notification)(UIKit) 또는 [`NSAccessibility.Notification`](https://developer.apple.com/documentation/appkit/nsaccessibility/notification)(AppKit)을 참조하세요.

- ### 컨트롤이 다른 웹 페이지 또는 앱을 열 때 사용자가 예측할 수 있도록 지원하세요. 
컨텍스트가 예기치 않게 변경되면 혼란을 야기하고 사람들이 현재 경험에 대한 마인드 맵(정신적 모델, 추론할 수 있는 정보)을 갑자기 다시 구축해야 할 수 있습니다. 컨텍스트의 잠재적 변화에 주의를 환기시키는 한 가지 방법은 버튼의 제목에 줄임표를 추가하는 것입니다. 시스템 전체에서 제목 뒤에 줄임표를 붙이는 것은 버튼이 사람들이 작업을 완료할 수 있는 다른 창이나 보기를 연다는 것을 알리는 표준 방법입니다. 예를 들어 iOS 및 iPadOS의 Mail에서는 메시지 이동 버튼에 줄임표를 추가하여 사람들이 선택할 수 있는 대상 목록을 나열하는 별도의 보기가 열렸음을 알립니다.

- ### 모든 중요한 인터페이스 요소에 대체 텍스트 레이블을 제공하세요. 
대체 텍스트 레이블은 눈에 보이지는 않지만 VoiceOver가 앱 요소를 음성으로 설명해 주므로 시각 장애가 있는 사용자가 더 쉽게 탐색할 수 있습니다. 시스템에서 제공하는 컨트롤에는 기본적으로 유용한 레이블이 있지만 사용자 지정 요소에 대한 레이블을 만들어야 합니다. 예를 들어 사용자 지정 평점 버튼을 나타내는 접근성 요소를 만드는 경우 "Rate"이라는 레이블을 제공할 수 있습니다.

- ### 필요한 경우 VoiceOver 로터를 지원합니다.
VoiceOver 사용자는 로터라는 컨트롤을 사용하여 제목, 링크 또는 기타 섹션 유형별로 문서 또는 웹 페이지를 탐색할 수 있습니다. 로터는 점자 키보드를 불러올 수도 있습니다. 로터로 이러한 항목을 식별하여 VoiceOver 사용자가 앱에서 관련 항목 사이를 탐색할 수 있도록 도울 수 있습니다. 개발자 지침은 [`UIAccessibilityCustomRotor`](https://developer.apple.com/documentation/uikit/uiaccessibilitycustomrotor) 및 [`NSAccessibilityCustomRotor`](https://developer.apple.com/documentation/appkit/nsaccessibilitycustomrotor)를 참조하십시오.

> 로터: 실제 다이얼을 돌리는 것 처럼, iOS 또는 iPadOS 기기의 화면에서 손가락을 돌리는 것.

![](https://support.apple.com/library/content/dam/edam/applecare/images/en_US/iOS/ios13-iphone-xs-safari-voiceover-rotor-hero.jpg)

- ### iPadOS, macOS 및 visionOS에서는 키보드를 사용하여 앱의 모든 구성 요소를 탐색하고 상호 작용할 수 있도록 해야 합니다. 
전체 키보드 액세스를 켜고 키보드만 사용하여 환경의 모든 작업을 수행할 수 있는 것이 가장 이상적입니다. [accessibility keyboard shortcuts(접근성 키보드 단축키)](https://support.apple.com/en-us/HT204434) 외에도 많은 사람들이 항상 사용하는 수많은 다른 [keyboard shortcuts(키보드 단축키)](https://support.apple.com/en-us/HT201236)를 정의합니다. 모든 사용자를 지원하려면 앱에서 시스템에서 정의한 키보드 단축키를 재정의하지 않는 것이 중요합니다. 자세한 내용은 [Keyboards](https://developer.apple.com/design/human-interface-guidelines/keyboards)를 참조하세요.

## 텍스트 표기

- ### iOS, iPadOS, tvOS, visionOS 및 watchOS에서 동적 유형(Dynamic Type)을 사용하여 앱 레이아웃이 모든 글꼴 크기에 맞게 조정되는지 테스트합니다. 
동적 유형을 사용하면 사용자가 자신에게 적합한 글꼴 크기를 선택할 수 있습니다. 디자인이 크기를 조정할 수 있는지, 텍스트와 글리프가 모든 글꼴 크기에서 가독성이 있는지 확인합니다. 예를 들어 iPhone 또는 iPad의 경우 설정 > 접근성 > 디스플레이 및 텍스트 크기 > 더 큰 텍스트에서 더 큰 접근성 텍스트 크기를 켜고 앱이 편안하게 읽을 수 있는지 확인하세요. 각 플랫폼에 대한 동적 유형 크기 표는 [Apple Design Resources](https://developer.apple.com/design/resources/)에서 다운로드할 수 있습니다.





| 작은 테스트 | 큰 텍스트 |
| ----------- | --------- |
|      ![](https://i.imgur.com/b2Kcb8l.png)       |        ![](https://i.imgur.com/VyaXQfo.png)   |

- ### 글꼴 크기가 커질수록 텍스트 잘림을 최소화하세요.
 일반적으로 가장 큰 글꼴 크기를 가장 큰 접근성 글꼴 크기로 표시하는 것을 목표로 합니다. 사용자가 별도의 보기를 열어 나머지 콘텐츠를 읽을 수 있는 경우가 아니라면 스크롤 가능한 영역에서 텍스트를 잘라내지 마세요. 유용한 양의 텍스트를 표시하는 데 필요한 만큼의 줄을 사용하도록 레이블을 구성하여 레이블에서 텍스트가 잘리는 것을 방지할 수 있습니다(개발자 지침은 [`numberOfLines`](https://developer.apple.com/documentation/uikit/uilabel/1620539-numberoflines)를 참조하세요).

- ### 큰 글꼴 크기에서 레이아웃을 조정하는 것을 고려합니다. 
가로로 제한된 환경에서 글꼴 크기가 커지면 인라인 항목과 컨테이너 경계로 인해 텍스트가 혼잡해져 가독성이 떨어질 수 있습니다. 예를 들어 글리프나 타임스탬프와 같은 보조 항목과 함께 텍스트를 인라인으로 표시하는 경우 텍스트의 가로 공간이 줄어듭니다. 글꼴 크기가 큰 경우 인라인 레이아웃으로 인해 텍스트가 잘리거나 텍스트와 보조 항목이 겹칠 수 있습니다. 이 경우 텍스트가 보조 항목 위에 표시되는 스택형 레이아웃을 사용하는 것이 좋습니다. 마찬가지로 여러 열의 텍스트는 각 열이 가로 공간을 제약하기 때문에 큰 글꼴 크기에서는 가독성이 떨어질 수 있습니다. 이 경우 글꼴 크기가 커지면 열 수를 줄여 텍스트 잘림을 방지하고 전체적인 가독성을 개선하는 것이 좋습니다. 개발자 지침은 [`isAccessibilityCategory`](https://developer.apple.com/documentation/uikit/uicontentsizecategory/2897444-isaccessibilitycategory)를 참조하세요.


| 작은 텍스트 크기에서는 메일에 발신자 이름과 함께 날짜가 인라인으로 표시됩니다. | 가장 큰 접근성 텍스트 크기에서 메일은 받는 사람 이름 아래에 날짜를 표시합니다. |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
|         ![](https://i.imgur.com/VdQMbt5.png)                                                                       |                                      ![](https://i.imgur.com/uR8Eh1a.png)                                          |

- ### 글꼴 크기가 커지면 의미 있는 인터페이스 아이콘의 크기도 커집니다. 
중요한 정보를 전달하기 위해 인터페이스 아이콘을 사용하는 경우 큰 글꼴 크기로도 쉽게 볼 수 있도록 하세요. [SF Symbols](https://developer.apple.com/design/human-interface-guidelines/sf-symbols)을 사용하면 동적 유형 크기 변경에 따라 자동으로 크기가 조정되는 아이콘을 사용할 수 있습니다.

![](https://i.imgur.com/kLI9kZF.png)

- ### 현재 글꼴 크기에 관계없이 일관된 정보 계층 구조를 유지합니다. 
예를 들어 글꼴 크기가 매우 큰 경우에도 기본 요소를 뷰의 맨 위에 유지하여 사람들이 이러한 요소를 놓치지 않도록 합니다.

- ### 앱에서 일반 또는 무거운 글꼴 가중치를 선호합니다.
일반, 중간, 세미볼드 또는 굵게 글꼴 가중치를 사용하는 것이 눈에 더 잘 띄므로 이를 고려하세요. 보기 어려울 수 있는 초경량, 엷음, 옅은 글꼴 가중치는 피하세요.

- ### 사람들이 굵은 텍스트를 켰을 때 앱이 올바르게 반응하고 보기 좋게 표시되는지 확인하세요. 
iOS, iPadOS, tvOS, visionOS, watchOS에서는 굵은 텍스트 접근성 설정을 켜서 텍스트와 기호를 더 쉽게 볼 수 있도록 합니다. 이에 따라 앱은 모든 텍스트를 더 굵게 만들고 모든 글리프에 스트로크(획) 가중치를 높여야 합니다. 시스템 글꼴과 SF 기호는 굵은 텍스트 접근성 설정에 맞게 자동으로 조정됩니다.

![](https://i.imgur.com/QditMmf.png)

- ### 사용자 지정 글꼴이 읽기 쉬운지 확인하세요. 
사용자 지정 서체는 때때로 읽기 어려울 수 있습니다. 브랜딩 목적이나 몰입감 있는 게임 환경을 만들기 위해 사용자 지정 글꼴이 꼭 필요한 앱이 아니라면 일반적으로 시스템 글꼴을 사용하는 것이 가장 좋습니다. 사용자 지정 글꼴을 사용하는 경우 작은 크기라도 읽기 쉬운 글꼴인지 확인하세요.

- ### 전체 텍스트 정렬(justication)은 피하세요.
전체 정렬 텍스트에 의해 생성된 공백은 많은 사람들이 텍스트를 읽고 집중하기 어렵게 만드는 패턴을 만들 수 있습니다. 왼쪽 정렬(또는 오른쪽에서 왼쪽으로 쓰는 언어의 경우 오른쪽 정렬)은 난독증과 같은 학습 및 문해력 문제가 있는 사람들에게 프레임 참조를 제공합니다.

- ### 긴 텍스트 구절에는 이탤릭체나 모두 대문자를 사용하지 마세요. 
이탤릭체와 대문자는 가끔 강조하기에는 좋지만 이러한 스타일을 과도하게 사용하면 텍스트를 읽기 어렵게 만듭니다.

## 색상 및 효과
- ### 사물을 구분하거나 중요한 정보를 전달할 때 색상에만 의존하지 마세요.
 색상을 사용하여 정보를 전달하는 경우 모든 사람이 정보를 인식할 수 있도록 텍스트 레이블이나 글리프 모양을 제공해야 합니다.

- ### 텍스트에 시스템 색상을 선호합니다.
텍스트에 시스템 색상을 사용하면 색상 반전 및 대비 증가와 같은 접근성 설정에 올바르게 반응합니다.

- ### 두 상태 또는 값을 구분하는 유일한 방법으로 색상 조합을 사용하지 마세요. 
많은 색맹은 파란색과 주황색을 구분하기 어렵고, 빨간색과 녹색, 빨간색과 검은색, 빨간색 또는 녹색과 회색을 조합하는 것도 문제가 될 수 있습니다. 상태나 값을 전달하기 위해 색상 조합을 사용하는 것이 합리적이라면 모든 사람이 정보를 인식할 수 있도록 추가적인 시각적 표시를 포함하세요. 예를 들어 빨간색과 녹색 원을 사용하여 오프라인과 온라인을 표시하는 대신 빨간색 사각형과 녹색 원을 사용할 수 있습니다. 일부 이미지 편집 소프트웨어에는 색맹을 증명하는 데 도움이 되는 도구가 포함되어 있습니다.

| 일반 모드 | 색약 모드 |
| --------- | --------- |
|      ![A screenshot of the History view of the Activity app. The default colors of red, green, and blue are visible.](https://docs-assets.developer.apple.com/published/d543ffc547c6d078b7ff74958c641b88/color-blindness-full-color@2x.png)     |       ![A screenshot of the History view of the Activity app. The color red is replaced by dark gray, green is replaced by yellow, and blue is replaced by light gray.](https://docs-assets.developer.apple.com/published/9cca1cf0b16eaaae605b89d4c16c126c/color-blindness-protanopia@2x.png)    |

- ### View가 색상 반전에 올바르게 반응하는지 확인합니다. 
어두운 배경에서 항목을 보는 것을 선호하는 경우 색상 반전 기능을 켤 수 있습니다. 색상 반전의 스마트 반전 모드에서는 이미지, 동영상 및 풀컬러 아이콘(예: 앱 아이콘 및 테마가 없는 이미지)이 반전되지 않으며 어두운 UI는 어두운 상태로 유지됩니다. 앱 또는 게임을 테스트하여 사용자 지정 보기의 사진 등 이미지가 반전되지 않도록 해야 하는 위치를 찾아보세요.

- ### 가독성을 높이려면 대비가 강한 색상을 사용하세요. 
글꼴 크기 및 굵기, 색상 밝기, 화면 해상도, 조명 조건 등 다양한 요소가 색상을 인식하는 데 영향을 미칩니다. 텍스트, 글리프, 컨트롤과 같은 시각적 요소의 색상 대비를 높이면 더 많은 사람들이 더 많은 상황에서 앱을 사용할 수 있습니다. UI에서 인접한 색상의 대비가 최소 허용 수준을 충족하는지 확인하려면 Xcode의 접근성 검사기(Accessibility Inspector) 또는 [Web Content Accessibility Guidelines (WCAG, 웹 컨텐츠 접근성 지침)](https://www.w3.org/TR/WCAG21/) 색상 대비 공식에 기반한 온라인 색상 계산기를 사용할 수 있습니다. 일반적으로 작거나 가벼운 텍스트는 가독성을 높이기 위해 대비가 더 커야 합니다. 다음 값을 참고하세요.

| 텍스트 사이즈   | 텍스트 가중치(Weight) | 최소 명암비 |
| --------------- | --------------------- | ----------- |
| Up to 17 points | All                   | 4.5:1       |
|18 points and larger| All                   | 3:1         |
| All             | Bold                  | 3:1            |

- ### 사람들이 투명도 감소를 켤 때 흐림 및 투명도를 변경합니다. 
예를 들어 흐린 콘텐츠 및 투명도 영역을 대부분 불투명하게 만듭니다. 최상의 결과를 얻으려면 불투명 영역에 흐림 또는 반투명 영역에 사용한 원래 색상 값과 다른 색상 값을 사용하십시오.

## Motion

- ### 경험에 필수적인 경우가 아니라면 애니메이션을 요구하지 마세요.
일반적으로 사람들이 애니메이션에 의존하지 않고 앱을 사용할 수 있도록 하세요.

- ### 모션 감소가 켜져 있을 때는 애니메이션을 강화하여 재생합니다. 
확대/축소, 회전 또는 주변 동작과 같은 효과가 포함된 애니메이션을 볼 때 주의가 산만해지거나 어지러움이나 메스꺼움을 느끼는 경우 모션 감소를 설정할 수 있습니다.문제를 일으키는 애니메이션을 끄거나 줄여야 합니다(자세한 내용은 [Responsive design for motion(모션에 대한 반응형 디자인)](https://webkit.org/blog/7551/responsive-design-for-motion/)을 참조하세요). 문제가 있는 애니메이션을 사용하여 중요한 정보를 전달하는 경우 다른 대안을 설계하거나 애니메이션의 효과를 강화하여 동작을 줄이는 것이 좋습니다.

예를 들어, 다음과 같이 적용 할 수 있습니다.

- 바운스 효과를 줄이거나 제스처를 추적하기
- Z축 레이어에서 depth 변화를 애니메이션으로 처리하지 않기
- 블러효과 안팎으로 애니메이션을 적용하지 않기
- 슬라이드 효과를 fade 효과로 바꾸기

- ### 사람들이 비디오 및 기타 모션 효과를 제어할 수 있도록 합니다.
버튼이나 다른 제어 방법을 제공하지 않고 동영상이나 효과를 자동 재생하지 않도록 합니다.

- ### 움직이거나 깜박이는 요소를 표시할 때는 주의하세요. 
미묘한 움직임과 깜박임은 사람들의 주의를 끌 수 있지만, 이러한 효과는 산만할 수 있으며 시각 장애가 있는 사람에게는 유용하지 않습니다. 더 심각한 문제는 일부 깜박임 요소가 간질 발작을 유발할 수 있다는 점입니다. 어떤 경우에도 움직임과 깜빡임을 유일한 정보 전달 수단으로 사용하지 마세요.

사용자가 비전OS 앱에서 동작을 경험하는 동안 편안함을 유지하는 데 도움이 되는 추가 지침은 [Motion > visionOS](https://developer.apple.com/design/human-interface-guidelines/motion#visionOS)를 참조하세요. 개발자를 위한 지침은 [Improving accessibility support in your visionOS app](https://developer.apple.com/documentation/visionOS/improving-accessibility-support-in-your-app)를 참조하세요.

## 플랫폼 고려사항
- iOS, iPadOS, macOS, tvOS, watchOS는 해당되지 않습니다.

### visionOS
- ### 콘텐츠를 착용자의 머리에 고정하지 마세요.
콘텐츠를 머리에 고정하면 갇힌 느낌을 줄 뿐만 아니라 포인터 컨트롤을 사용하여 콘텐츠와 상호 작용하는 데 방해가 될 수 있습니다. 또한 머리에 고정된 콘텐츠는 시력이 낮은 사람이 가까이 다가가거나 확대경 안쪽에 배치할 수 없기 때문에 사용자가 콘텐츠를 읽지 못할 수도 있습니다.

#### 손으로 포인트 컨트롤하기
https://github.com/i-colours-u/Human-Interface-Guidelines-KR/assets/60260284/23c7330f-cf78-4bce-85f8-d88379c65842


#### 머리로 포인트 컨트롤하기
https://github.com/i-colours-u/Human-Interface-Guidelines-KR/assets/60260284/f84e930a-0e6a-4bee-9ca3-74982676973b

#### 확대경 (줌 렌즈)
![visionos-accessibility-zoom-lens@2x](https://github.com/i-colours-u/Human-Interface-Guidelines-KR/assets/60260284/d1241dfe-0c4b-45fa-9f2b-86328809dee7)


---

### 연관 내용
- [Inclusion](https://developer.apple.com/design/human-interface-guidelines/inclusion)

### 개발자 문서 참고
- [Accessibility](https://developer.apple.com/documentation/accessibility)
- [Accessibility for developers](https://developer.apple.com/accessibility/)
- [Accessibility modifiers](https://developer.apple.com/documentation/SwiftUI/View-Accessibility)
- [Accessibility for UIKit](https://developer.apple.com/documentation/uikit/accessibility_for_uikit)
- [Accessibility for AppKit](https://developer.apple.com/documentation/appkit/accessibility_for_appkit)

### 영상

| [Create accessible spatial experiences](https://developer.apple.com/videos/play/wwdc2023/10034) | [Design considerations for vision and motion](https://developer.apple.com/videos/play/wwdc2023/10078) | [The practice of inclusive design](https://developer.apple.com/videos/play/wwdc2021/10275) |
| -------- | -------- | -------- |
| ![](https://i.imgur.com/0vTInHi.png) |     ![](https://i.imgur.com/BOR3KFC.png) | ![](https://i.imgur.com/pRuJIGO.png) |



