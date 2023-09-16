# Writing

## 앱 내에서 선택하는 워딩(단어)는 사용자 경험에서 매우 큰 부분을 차지합니다.

![A sketch of a document and pencil, suggesting written content. The image is overlaid with rectangular and circular grid lines and is tinted yellow to subtly reflect the yellow in the original six-color Apple logo.](https://docs-assets.developer.apple.com/published/5bd05331c62b850b25ac62f8581b97b6/foundations-writing-intro@2x.png)


여러분이 만드는 앱은 사용자 경험의 중요한 부분입니다. 온보딩 경험을 설계하거나 경고 메시지를 작성하거나 접근성을 고려해 이미지를 설명할 때, 언어의 선택은 여러분의 앱이나 게임을 최대한 활용할 수 있도록 돕습니다.

## Getting Started

### 여러분의 앱에서 사용할 무드(어조, 톤)을 정하세요.
누구에게 말하는지 생각하여 사용할 어휘를 선택하세요. 사용자들이 익숙한 용어는 무엇인가요? 어떤 느낌을 주고 싶으세요? 은행 앱에서는 신뢰와 안정성을 나타내는 단어를 사용할 수 있고, 게임에서는 흥미와 즐거움을 전달하는 어휘를 고려할 수 있습니다. 공통 용어 목록을 만들어서 일관된 언어를 사용하고, 앱의 가치를 반영하는 어조를 유지하세요. 일관된 언어와 앱의 가치를 반영하는 어조는 모든 것이 보다 일관성 있게 느껴지도록 도와줍니다.

### 맥락에 맞게 어조를 조절하세요.
앱의 어조를 설정한 후에는 상황에 따라 어조를 다르게 적용하세요. 사용자가 앱을 사용하는 동안 물리적 세계와 앱 내부에서 무엇을 하는지 고려하세요. 그들이 운동을 하며 목표를 달성했을까요? 아니면 지불을 시도하다 오류 메시지를 받았을까요? 상황적인 요인은 말하는 내용과 화면에 표시되는 텍스트의 방식에 모두 영향을 미칩니다.

애플 워치의 2가지 예시를 비교해보세요.
첫 번째 예시에서는 상황의 심각성을 반영하여 직접적이고 단호한 어조를 사용합니다. 두 번째 예시에서는 상황의 가벼움과 축하의 느낌을 전달하기 위해 부드럽고 축하하는 어조를 사용합니다.


|     |     |
| --- | --- |
|  ![A screenshot of a Fall Detection message that reads: it looks like you've taken a hard fall.](https://docs-assets.developer.apple.com/published/58f94ca509ec5b915b6c3b8ea21aaf9f/fall-detection-message@2x.png)  |   ![A screenshot of an Activity message that reads: you set a personal record for your longest daily Move streak, 35 days!](https://docs-assets.developer.apple.com/published/54d5ea9ec7d50374459f8ab01ee6b9ea/move-streak-message@2x.png)  |


### 명확하게 표현하세요. 
이해하기 쉬운 단어를 선택하고 올바른 내용을 전달하세요. 각 단어가 필요한지 확인하고, 불필요한 단어를 줄일 수 있다면 줄이세요. 의심스러운 경우 글을 읽어 보면서 확인하세요.

### 모든 사람을 위해 문장을 작성해보세요. 
여러분의 앱이 최대한 많은 사람들에게 유용하려면 최대한 많은 사람들에게 말하도록 해야 합니다. 간단하고 명확한 언어를 선택하고 접근성과 로컬라이징을 고려하여 쓰세요. 전문 용어와 성별화된 용어를 피하고, 도움말이 필요하다면 [Writing inclusively](https://help.apple.com/applestyleguide/#/apdcb2a65d68)와 [VoiceOver](https://developer.apple.com/design/human-interface-guidelines/accessibility#VoiceOver)를 참고하세요. 개발자 안내는 [Localization](https://developer.apple.com/documentation/xcode/localization)를 참고하세요.

## Best practices

### 각 화면의 목적을 고려하세요. 
화면의 순서에 주의하고, 가장 중요한 정보를 먼저 표시하세요. 텍스트 형식을 조정하여 읽기 쉽게 만드세요. 하나 이상의 아이디어를 전달하려고 할 때, 텍스트를 여러 화면으로 나누고 그 화면 간 정보의 흐름을 고려하세요.

### 행동 중심으로 쓰세요. 
명확한 문장과 명확한 레이블은 사용자들이 한 단계에서 다음 단계로 이동하거나, 한 화면에서 다른 화면으로 앱을 탐색하는 데 도움이 됩니다. 버튼과 링크에 레이블을 달 때 동사 형태의 워딩을 사용하는 것이 가장 좋습니다. 명확성을 우선하고, 레이블을 너무 키치하거나, 귀엽거나, 재치있는 워딩을 사용하는 유혹에서 벗어나세요 😁 예를 들어, "다음"이라고 말하는 것이 "한번 해볼까요?!" 보다 더 잘 작동하는 경우가 많습니다. 링크에 대해서도 "여기를 클릭하세요" 대신 "UX Writing에 대해 자세히 알아보기"와 같은 더 구체적인 단어나 구문을 사용하세요. 특히 스크린 리더를 사용하여 앱에 접근하는 사람들에게 이것은 매우 중요합니다.

### 언어 패턴을 만드세요. 
일관성은 익숙함을 만들어주며, 여러분의 앱이 통합되고 직관적이며 신중하게 디자인되었다는 느낌을 줍니다. 또한 여러분의 앱을 위해 UX 라이팅을 쓸 때 이러한 패턴을 반복해서 사용할 수 있어서 편리합니다. 여기 몇 가지 고려해야 할 언어 패턴이 있습니다:


- #### 대문자로 시작하는 제목 혹은 문장으로 결정하세요. 
경고, 페이지 제목, 헤드라인, 버튼 레이블 및 링크에 대해 대문자로 시작하는 형태로 문장을 작성하세요. HIG에서는 특정 구성 요소에 대한 지침을 찾을 수 있지만 텍스트를 사용하는지는 여러분의 앱 스타일에 따라 달려 있습니다. 대문자로 시작하는 제목은 더 공식적인 느낌을 주며, 문장으로 시작하는 제목은 더 캐주얼한 느낌을 줍니다. 여러분의 앱에 맞는 스타일을 선택하세요.

> 해당 HIG 문서는 영어를 기반으로 작성되어, 한국어와 어느정도 맞지 않는 부분(대문자로 작성과 같은 부분)이 있습니다. 이를 감안하고 읽어주세요.


- #### 1인칭 또는 2인칭 형태의 워딩을 사용하세요. 
 여러분의 앱이 사람들에게 즐겨찾기를 저장하거나 항목을 즐겨찾기로 표시할 수 있게 한다면, 이러한 항목은 "나의 즐겨찾기" 또는 "(여러분이) 저장한 항목" 라는 워딩으로 표현 할 수 있습니다. 하지만 2가지 방식을 동시에 사용하는 것은 피하세요. 1인칭 혹은 2인칭 중에 1가지 방식만 채택해서 통일하는 것이 좋습니다.

- #### "계속하기" 혹은 "다음" 둘 중 하나만 사용하세요. (Continue or Next)
여러 화면에 걸쳐있는 앱의 흐름이 있다면, 다음 단계로 이동하는 버튼 또는 링크에 어떻게 레이블을 지정할지 결정하세요. "계속" 또는 "다음" 이라는 워딩 중 1가지만 선택해서 통일성 있게 사용하는 것으 권장합니다. 특정 화면 플로우 끝에는 "완료하기" 또는 "완료" 라는 특별한 라벨을 통해 플로우가 끝났다는 점을 사용자에게 알려주는 것이 좋습니다.


### 사람들이 휴대폰(기기)를 사용하는 방식에 따라 워딩을 다르게 사용하세요.
사람들은 여러 종류의 디바이스에서 여러분의 앱을 사용할 수 있습니다. 언어는 이러한 디바이스 간에 일관성이 있어야 합니다. 특정 디바이스에 맞게 텍스트를 조절하는 것이 여러분의 앱에 어떻게 도움이 될지 고려해보세요. 각 디바이스에서 제스처를 올바르게 설명하는지 확인하세요. 예를 들어, iPhone이나 iPad와 같은 터치 디바이스에서 "탭"을 의미하는데, "클릭"이라는 워딩을 사용하지 않도록 주의하세요.
(각 디바이스의 사용 방식에 맞춰 워딩을 작성하라는 의미)

디바이스를 사용하는 위치, 화면 크기 및 환경은 여러분의 앱을 위해 어떻게 쓸 지에 영향을 미칩니다. 예를 들어, iPhone과 Apple Watch는 맞춤화 기회를 제공하지만 작은 화면 크기로 인해 사용시에 간결함이 필요합니다. 반면 TV는 일반적으로 공용 거실에 있으며 여러 명이 화면에 표시되기 상대적으로 쉽습니다. 물론, 해당 컨텐츠를 보는 대상을 고려해야 합니다. 큰 화면도 간결함(심플함)이 필요하며, 텍스트는 멀리서 볼 수 있도록 커야 합니다.

### 빈 화면에 대한 명확한 다음 단계를 제공하세요.
완료된 할 일 목록이나 아무 것도 없는 즐겨찾기 폴더와 같은 빈 상태는 유저들에게 앱에 대해 잘 알려줄 수 있고, 안내 할 수 있는 새로운 기회를 줄 수 있습니다. 빈 상태는 여러분의 앱 어조를 강조할 수도 있지만, 콘텐츠가 유용하고 문맥에 맞는지 확인하세요. 빈 화면은 다음에 무엇을 해야 할지 명확하지 않다면 오히려 사용자들에게 어려울 수 있으므로 사람들이 할 수 있는 조치를 안내하고 가능하면 버튼이나 링크를 제공하세요. 특정 화면에서 빈 상태는 보통 일시적이므로 사라질 수 있는 중요한 정보를 표시하지 않아야 합니다.

### 명확한 오류 메시지를 작성하세요.
항상 사람들이 오류를 피하도록 돕는 것이 가장 좋습니다. 오류 메시지가 필요한 경우 문제와 가장 가까운 곳에 표시하고, 사용자가 잘못했다는 지적을 나타내기를 피하고 어떻게 고칠 수 있는지 명확하게 표시하세요. 예를 들어, "비밀번호가 너무 짧습니다"보다는 "최소 8자 이상의 비밀번호를 선택하세요"가 더 도움이 됩니다. 오류는 짜증을 유발할 수 있으므로 "어이쿠!" 또는 "우와!"와 같은 감탄사는 일반적으로 필요하지 않으며 어떻게 솔루션을 재고해야 하는지 다시 고려하는 기회로 활용할 수 있습니다.

### 적절한 메세지 전달 방법 선택하기
여러분의 앱을 활용하고 있지 않더라도, 사람들의 주의를 끄는 여러 가지 방법이 있습니다. 전달하려는 메시지의 긴급성과 중요성을 고려하세요. 앱을 사용하지 않는 사람들이 메시지를 볼 수 있는 상황을 고려해서, 즉각적인 조치가 필요한지 여부 및 지원 정보가 얼마나 필요한지 고려하세요. 이러한 상황 속에서 최대한 적절한 전달 방법을 선택하고 상황에 적절한 어조를 사용하세요. 자세한 가이드는 [Notifications](https://developer.apple.com/design/human-interface-guidelines/notifications), [Alerts](https://developer.apple.com/design/human-interface-guidelines/alerts), [Action sheets](https://developer.apple.com/design/human-interface-guidelines/action-sheets) 문서를 참조하세요.

### 설정 레이블을 명확하고 간단하게 유지하세요. 
가능한 한 실용적으로 레이블을 달아서 필요한 설정을 쉽게 찾을 수 있도록 도와주세요. 설정 레이블만으로는 충분하지 않은 경우 설명을 추가하세요. 특정 설정 옵션이 켜진 상태에서 이 설정이 무엇을 하는지 설명하면, 옵션이 꺼진 상태에서는 이 설정이 동작하지 않음을 사람들이 추론할 수 있습니다. 예를 들어 Apple Watch의 손 씻기 타이머 설정에서는 타이머가 손 씻기 중에 시작할 수 있다는 설명이 있습니다. 이 설정이 꺼져 있을 때 타이머가 시작되지 않는다는 것을 설명하는 것은 필요하지 않습니다. (굳이 부가적으로 꺼졌을 떄 어떻게 할 지에 대한 설명이 필요 없다는 뜻)
![A partial screenshot showing the Handwashing Timer description, which reads: Apple Watch can detect when you're washing your hands and start a 20-second timer.](https://docs-assets.developer.apple.com/published/d313580ca52395f9227953797ce98537/handwashing-settings@2x.png)'

만약 누군가에게 특정 설정을 안내해야 한다면, 그 위치를 설명하려고 노력하기보다는 직접 링크나 버튼을 제공하세요. 지침은 [Settings](https://developer.apple.com/design/human-interface-guidelines/settings)을 참조하세요.

### 텍스트 필드에 힌트 표시하세요. 
여러분의 앱이 사람들이 자신의 텍스트를 입력할 수 있도록 허용한다면, 모든 필드를 명확하게 레이블을 작성하고 힌트나 플레이스홀더 텍스트를 사용하여 정보를 어떻게 형식화해야 하는지 알 수 있도록 도와주세요. 힌트 텍스트에 예제를 제공할 수 있습니다. 예를 들어, "[name@example.com](mailto:name@example.com)"과 같은 예제를 힌트 텍스트에 표시하거나 "이름을 작성해주세요"과 같이 정보를 설명할 수 있습니다. 필드 옆에 오류를 표시하고 사람들에게 정보를 올바르게 입력하는 방법을 안내하세요. 해당 규칙 및 룰을 따르지 않아서 경고하거나, 강한 어투로 표현하지 말고 정보를 입력하는 방법을 알려주세요. "이름에는 문자만 사용하세요"는 "숫자나 기호를 사용하지 마세요"보다 더 좋습니다. 유용한 정보가 없는 로봇 같은 오류 메시지("잘못된 이름"과 같은)를 피하세요. 자세한 지침은 [Text fields](https://developer.apple.com/design/human-interface-guidelines/text-fields)를 참조하세요.


## 플랫폼별 고려사항
- iOS, iPadOS, watchOS, tvOS, visionOS, macOS들은 해당사항이 없습니다.

---

### 참고 문서

- [Apple Style Guide](https://help.apple.com/applestyleguide/#/)
- [Writing inclusively](https://help.apple.com/applestyleguide/#/apdcb2a65d68)
- [Inclusion](https://developer.apple.com/design/human-interface-guidelines/inclusion)
- [Accessibility](https://developer.apple.com/design/human-interface-guidelines/accessibility)
- [Color](https://developer.apple.com/design/human-interface-guidelines/color)


### 연관 영상
| [Writing for interfaces](https://developer.apple.com/videos/play/wwdc2022/10037)                                            |
| --------------------------------------------------------------------------------------------------------------------------- |
| ![](https://devimages-cdn.apple.com/wwdc-services/images/124/E58B8A59-15C1-4FB4-B61A-23DBA2AF6D28/6530_wide_250x141_1x.jpg) |


