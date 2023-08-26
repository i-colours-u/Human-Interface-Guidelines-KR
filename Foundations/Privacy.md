# Privacy

## 개인 정보 보호는 매우 중요합니다. 필요한 개인 정보 관련 데이터와 자원에 대해 투명하게 공개하는 것이 중요하며, 유저들이 허용한 데이터를 보호하는 것이 필수적입니다.


![A sketch of an upright hand, suggesting protection. The image is overlaid with rectangular and circular grid lines and is tinted yellow to subtly reflect the yellow in the original six-color Apple logo.](https://docs-assets.developer.apple.com/published/161fec1d77c705ccf076fb4c67d32f5c/foundations-privacy-intro@2x.png)
사람들은 매우 개인적인 방식으로 기기를 사용하며, 앱이 유저들의 개인 정보를 보호하는 데 도움을 줄 것을 기대합니다.

새로운 앱이나 업데이트된 앱을 제출할 때, App Store가 귀하의 제품 페이지에 정보를 표시할 수 있도록 여러분 앱의 개인 정보 관련 지침과 개인 정보 관련 데이터 수집에 대한 세부 사항을 제공해야 합니다. (이 정보는 [App Store Connect](https://help.apple.com/app-store-connect/#/dev1b4647c5b)에서 언제든지 관리할 수 있습니다.) 사람들은 귀하의 제품 페이지의 개인 정보 세부 사항을 사용하여 앱을 다운로드하기 전에 정보를 기반으로 한 결정을 내립니다. 자세한 내용은 [App privacy details on the App Store(앱스토어의 앱 개인 정보 지침))](https://developer.apple.com/app-store/app-privacy-details/)을 참고하세요.

![A screenshot of the App Privacy screen in an app’s App Store product page. The top card in the screen is titled Data Used to Track You and lists contact info, location, and identifiers. The bottom card is titled Data Linked to You and lists financial and contact info, location, purchases, identifiers, and browsing history.](https://docs-assets.developer.apple.com/published/6b45cc81a35043309fac0da19d280cd5/privacy-practices@2x.png)

_앱의 앱 스토어 제품 페이지는 사람들이 앱을 다운로드하기 전에 앱의 개인정보 처리방침을 이해하는 데 도움이 됩니다._



## Best practices

### - 실제로 필요한 데이터에만 접근을 요청하세요. 
기능이 필요로 하는 것보다 더 많은 데이터를 요청하거나, 사람들이 기능에 관심을 보이기 전에 데이터를 요청하는 것은 사람들이 여러분의 앱을 신뢰하기 어렵게 만듭니다. 권한 요청을 최대한 구체적으로 하여 사람들이 데이터에 대한 정확한 제어권을 갖게 하세요.

### - 앱이 어떻게 사람들의 데이터를 수집하고 사용하는지에 대해 투명하게 공개하세요. 
여러분이 데이터를 어떻게 사용할 계획인지 정확하게 이해하지 못한다면 사람들은 앱과 데이터를 공유하는데 불편함을 느낄 수 있습니다. 애플 로그인 시, 'Hide My Email'과 'Mail Privacy Protection'과 같은 시스템 기능을 사용하는 사람들의 선택을 항상 존중하고, 앱 추적과 관련하여 권장 사항들을 지켜주세요. Apple의 개인 정보 보호 기능에 대해 더 알고 싶다면 [Privacy](https://www.apple.com/privacy/)를 참고하고, 개발자 지침에 대해서는 [User privacy and data use](https://developer.apple.com/app-store/user-privacy-and-data-use/)를 참조하세요.

### - 가능한 경우 기기 내에서 데이터를 처리하세요. 
예를 들어 iOS에서는 Apple Neural Engine과 custom CreateML 모델을 활용하여 기기 내에서 직접 데이터를 처리할 수 있습니다. 이로 인해 원격 서버로의 긴 및 잠재적으로 위험한 왕복을 피할 수 있습니다.

### - 시스템에서 정의한 개인 정보 보호를 채택하고 보안 모범 사례를 따르세요. 
예를 들어, iOS 15 이후 버전에서는 CloudKit을 사용해서 문자열, 숫자 및 날짜와 같은 추가 데이터 유형에 대한 암호화 및 키 관리를 제공받을 수 있습니다.

## 권한 요청하기

#### 다음은 접근 권한을 요청해야 하는 여러 예시입니다:

- 개인 데이터, 위치, 건강, 금융, 연락처 및 기타 개인 식별 정보 포함
- 사용자가 생성한 내용, 이메일, 메시지, 캘린더 데이터, 연락처, 게임 플레이 정보, Apple Music 활동, HomeKit 데이터, 오디오, 비디오, 사진 콘텐츠 등
- Bluetooth 주변 기기, 홈 자동화 기능, Wi-Fi 연결 및 로컬 네트워크와 같은 보호된 리소스
- 카메라 및 마이크와 같은 기기 기능
- Full Space에서 실행되는 visionOS 앱에서의 ARKit 데이터, 손 추적, 평면 추정, 이미지 앵커링 및 월드 추적 등
- 앱 추적을 지원하는 기기의 광고 식별자

시스템은 사용자가 여러분의 각 요청을 볼 수 있게 표준 알림을 제공합니다. 앱이 접근 권한이 필요한 이유를 설명하는 복사본을 제공하면, 시스템은 알림에 설명을 표시합니다. 사용자는 또한 설정 >> 개인 정보 보호에서 설명을 보고 권한 설정 선택을 업데이트할 수 있습니다.

### -데이터나 리소스에 접근이 명확히 필요할 때만 권한을 요청하세요. 
개인 정보나 기기 기능에 대한 접근 권한을 요청받을 때, 그것이 명백히 필요하지 않다면 사람들은 의심스러워 할 것입니다. 이상적으로는, 접근이 필요한 앱 기능을 실제로 사용할 때까지 권한을 요청하는 것이 좋습니다. 예를 들어, 위치 정보가 필요한 기능에 관심을 보인 후에 그들의 위치를 공유할 방법으로 위치 버튼을 사용할 수 있습니다.

### - 앱이 작동하기 위해 데이터나 리소스가 필수적이지 않다면 앱 시작 시 권한을 요청하는 것을 피하세요. 
권한 요청의 이유가 명확할 경우 시작 시 요청에 불편함을 느끼지 않을 가능성이 높습니다. 예를 들어, 내비게이션 앱이 위치 정보에 접근해야만 사용자들은 해당 권한을 허용했을 때 스스로 이점을 볼 수 있음을 사람들은 이해합니다. 마찬가지로, 주변의 벽에 가상 물체를 튕기는 visionOS 게임을 하려면 그들의 주변 환경 정보에 접근할 권한을 부여해야 합니다

### - 앱이 요청하는 기능, 데이터 또는 리소스를 어떻게 사용하는지 명확하게 설명하는 내용을 작성하세요.
표준 알림은 앱 이름 다음, 권한을 승인하거나 거부하는 버튼 전에 여러분의 내용("_purpose string_" 또는 "_usage description string_"이라고 함)을 표시합니다. 간결하고, 구체적이며 이해하기 쉬운 완전한 문장을 목표로 하세요. 문장 형식을 사용하고, 수동태를 피하며 (영어 한정), 마지막에 마침표를 포함하세요. 개발자 지침에 대해서는 [Requesting access to protected resources(보호된 리소스에 대한 접근 요청)](https://developer.apple.com/documentation/uikit/protecting_the_user_s_privacy/requesting_access_to_protected_resources) 및 [App Tracking Transparency(앱 추적 투명성)](https://developer.apple.com/documentation/apptrackingtransparency)을 참조하세요.

|                                                                                                                                                                | 문구 예시                                              | 참고                                                                  |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------ | --------------------------------------------------------------------- |
| ![A checkmark in a circle to indicate a correct example.](https://docs-assets.developer.apple.com/published/88662da92338267bb64cd2275c84e484/checkmark@2x.png) | 앱에서 밤 동안 코골이 소리를 감지하기 위해 녹음합니다. | 앱이 데이터를 수집하는 방법과 이유를 명확하게 설명하는 문장입니다.    |
| ![An X in a circle to indicate an incorrect example.](https://docs-assets.developer.apple.com/published/209f6f0fc8ad99d9bf59e12d82d06584/crossout@2x.png)      | 더 나은 사용자 경험을 위해 마이크 권한이 필요합니다.   | 모호하고 제대로 목적이 정의되지 않았으며, 정당성이 부족한 설명입니다. |
| ![An X in a circle to indicate an incorrect example.](https://docs-assets.developer.apple.com/published/209f6f0fc8ad99d9bf59e12d82d06584/crossout@2x.png)      | 마이크 권한을 사용합니다.                              | 어떤 목적 및 정당성도 없는 명령형 문장입니다.                         | 


#### 다음은 표준 시스템 알림 메세지 몇 가지 예시입니다.

| 예시 1                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | 예시 2                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | 예시 3 |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------ |
| ![A screenshot of a permission alert for the Pal About app displaying a purpose string that reads Allow Pal About to access your location? Turning on location services allows us to show you when pals are nearby. Below the string is a small map image containing the Precise On notice and below the map are three buttons in a stack. From the top, the buttons are titled Allow Once, Allow While Using App, and Don’t Allow.](https://docs-assets.developer.apple.com/published/7606b1f491c09048bf8bd03b45ed36f8/permission-request-1@2x.png) | ![A screenshot of a permission alert for the Pal About app displaying a purpose string that reads Pal About would like to access your photos. Allow access to photos to upload photos from your library. The string is followed by three buttons in a stack. From the top, the buttons are titled Select Photos, Allow Access to All Photos, and Don’t Allow.](https://docs-assets.developer.apple.com/published/6c22cace0599c2630e86cebb50f28ba8/permission-request-2@2x.png) |   ![A screenshot of a permission alert for the Pal About app displaying a purpose string that reads Allow Pal About to access your contacts? Find friends using Pal About and add them to your pal network. The string is followed by two side-by-side buttons: Don’t Allow and Allow.](https://docs-assets.developer.apple.com/published/7e87848e5908661a78eb73aee3976e73/permission-request-3@2x.png)


### 사전 알림 화면, 창 또는 뷰 (Pre-alert screens, windows or views)
이상적으로 현재 앱 내에서 사람들에게 권한을 요청하는 이유를 이해시켜야 합니다. 추가적인 세부사항을 제공하는 것이 필수적이라면, 시스템 알림이 나타나기 전에 사용자 정의(직접 만든) 뷰 또는 window를 표시할 수 있습니다. 다음 가이드 라인은 카메라, 마이크, 위치, 연락처, 캘린더, 추적을 포함하여 보호된 데이터와 리소스에 대한 접근 권한을 요청하는 시스템 알림 앞에 표시되는 사용자 정의 뷰에 적용 할 수 있습니다.

### - 버튼은 하나만 포함하고, 이 버튼을 눌렀을 때 시스템 권한 허용 알림이 발생한다는 맥락을 정확하게 전달하세요.
사용자 정의 뷰 또는 창에 있는 버튼을 눌렀을 때 시스템 권한 허용 알림이 뜨지 않을 경우, 평소 경험에서 벗어나는 느낌을 받아 혼란을 야기할 수 있습니다. 

또 좋지 않은 예시 중 하나는, 버튼의 타이틀로 "허용"과 같은 용어를 사용하는 것입니다. 사용자 정의 버튼이 시각적으로 알림 내의 허용 버튼과 유사한 의미와 중량을 가진 것처럼 보이면, 사람들은 의도하지 않게 알림의 허용 버튼을 선택할 가능성이 더 높아집니다. "계속" 또는 "다음"과 같은 용어를 사용하여 사용자 정의 화면 또는 창의 단일 버튼의 제목을 지정하고, 그것의 동작이 시스템 알림을 열 것임을 명확히 하세요.

| ![A checkmark in a circle to indicate a correct example.](https://docs-assets.developer.apple.com/published/88662da92338267bb64cd2275c84e484/checkmark@2x.png) | ![A checkmark in a circle to indicate a correct example.](https://docs-assets.developer.apple.com/published/88662da92338267bb64cd2275c84e484/checkmark@2x.png) |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|    ![A screenshot of an app’s pre-alert screen that reads Allow tracking on the next screen for special offers and promotions just for you, advertisements that match your interests, an improved personalized experience over time. You can change this option later in the Settings app. Below the text is a button titled Continue.](https://docs-assets.developer.apple.com/published/fc7f233de9ee89f9dbdb48c175225a59/custom-messaging-correct-1@2x.png)                                                                                                                                                            |      ![A screenshot of the Pal About app’s pre-alert screen that reads Turning on location services allows us to provide features like: alerts when your pals are nearby, news of events happening near you, tagging and sharing your location. Below the text is a button titled Next and below the button is text that reads You can change this later in the Settings app.](https://docs-assets.developer.apple.com/published/237274110e00048cc265d0f0042dd0c8/custom-messaging-correct-2@2x.png)


### - 화면에  추가적인 동작을 넣지 마세요.
예를 들어, 시스템 알림을 띄우지 않고 화면이나 창을 떠나는 방법을 제공하지 마세요. (종료나 취소 옵션을 제공하는 것)


| ![An X in a circle to indicate an incorrect example.](https://docs-assets.developer.apple.com/published/209f6f0fc8ad99d9bf59e12d82d06584/crossout@2x.png) | ![An X in a circle to indicate an incorrect example.](https://docs-assets.developer.apple.com/published/209f6f0fc8ad99d9bf59e12d82d06584/crossout@2x.png)|
| -------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|    ![A screenshot of an app’s pre-alert screen highlighted to show a button titled Cancel that appears below the Continue button.](https://docs-assets.developer.apple.com/published/6ff09ed38ef7b3823347bc240c48b347/custom-messaging-incorrect-5@2x.png)                                                                                                                                                            |   ![A screenshot of an app’s pre-alert screen highlighted to show a Close button in the top-left corner and a More button in the top-right corner. The Continue button appears near the bottom of the screen.](https://docs-assets.developer.apple.com/published/6910c5e5f213833465fb3d06c6e9689a/custom-messaging-incorrect-6@2x.png)

## 트래킹 요청 (Tracking)

앱 추적은 민감한 문제입니다. 경우에 따라 추적의 이점을 설명하는 커스텀 화면이나 창을 표시하는 것이 타당할 수 있습니다. 앱을 시작하는 즉시 앱 추적을 수행하려면 추적 데이터를 수집하기 전에 시스템에서 제공하는 알림을 표시해야 합니다.

### 사람들을 혼란스럽게 하거나 오해하게 할 수 있는 커스텀 화면이 시스템 알림보다 먼저 나와서는 안됩니다.
사람들은 때로 빠르게 알림을 읽지 않고 닫기 위해 탭하기도 합니다. 그러한 행동을 이용하여 선택을 영향을 주려는 커스텀 메시지 화면, 창이 있다면 앱 스토어 리뷰에 의해 거부될 것입니다.

거절되는 몇 가지 예시는 하단을 참고해주세요. 

- 사용자에게 특정 이익을 제공
- 요청처럼 보이는 화면을 제공
- 시스템 알림 창 이미지 제공
- 시스템 알림 창 설명 및 주석 달기

의 경우들을 피해야 합니다.

자세한 지침을 참고하고 싶다면, [앱스토어 리뷰 가이드 5.1.1(iv)](https://developer.apple.com/app-store/review/guidelines/#data-collection-and-storage)을 참조해주세요.

#### 1. 금전적 이익 제공


![A screenshot of an app’s pre-tracking message that reads Allow tracking and get a $100 credit toward your next purchase. Below the text is an image of a dollar sign inside a circle. Below the image is a button titled Get $100 credit.](https://docs-assets.developer.apple.com/published/cd97429e2555ad384979258c510fcf30/custom-messaging-incorrect-1@2x.png)

요청을 승인하는 대가로 인센티브를 제공하지 마세요. 사람들이 권한을 부여하는 것에 대한 보상을 제공할 수 없으며, 사람들이 추적을 허용할 때까지 기능이나 콘텐츠를 보류하거나 앱을 사용할 수 없게 만들어선 안됩니다.

#### 2. 요청처럼 보이는 화면을 제공
![A screenshot of an app’s pre-tracking message that reads Allow tracking for a better experience. Below the text is a bar graph image that shows four bars increasing in height from left to right. Below the graph is a button titled Allow Tracking.](https://docs-assets.developer.apple.com/published/754adf94fd632793b649b54acaac0ecd/custom-messaging-incorrect-2@2x.png)


시스템 알림의 기능을 반영하는 커스텀 화면을 표시하지 마세요. 특히, 사전 알림 화면에서는 어떠한 허용도 이루어지지 않기 때문에 "허용" 또는 유사한 용어를 사용해서 버튼 타이틀을 작성하지 마세요.


#### 3. Alert 이미지 제공



![A screenshot of an app’s pre-tracking message that reads Choose Allow when prompted. Below the text is an image of the system-provided alert. Below the image is a button titled Continue. An Allow button in the system-provided alert image is circled.](https://docs-assets.developer.apple.com/published/7a5177d4bc1460b472577ea5e93ae61e/custom-messaging-incorrect-3@2x.png)

표준 알림의 이미지를 표시해서는 안되며, 어떤 방식으로든 해당 이미지를 수정하지 마세요.


#### 4. Alert 화면 설명 및 주석 달기

![A screenshot of an app’s pre-tracking message that reads Allow tracking for a better experience. The app’s custom screen also includes an upward-pointing arrow and the words Choose Allow in the lower third of the screen. Because the system-provided alert displays on top of the custom screen, the arrow appears to be pointing to the alert’s Allow button.](https://docs-assets.developer.apple.com/published/e3f463b819afea891f0e7cab188e466b/custom-messaging-incorrect-4@2x.png)

시스템 알림의 허용 버튼에 사람들의 주의를 끌 수 있는 시각적 단서를 표시하지 마세요.


## 위치 버튼


iOS, iPadOS 및 watchOS에서는 Core Location 프레임워크가 버튼을 제공하여 작업이 필요한 순간에 앱이 사용자의 위치에 임시로 접근할 수 있는 권한을 부여받게 합니다. 위치 버튼의 모양은 앱의 UI와 일치하도록 다양해질 수 있고, 이는 항상 위치 공유의 동작을 즉시 인식할 수 있는 방식으로 전달합니다.
![An image of a lozenge-shaped blue button that displays a white location indicator — that is, a narrow arrow head shape that points to the top right — followed by the text Current Location.](https://docs-assets.developer.apple.com/published/2d4e44adec80170cec96d3446617e700/location-button@2x.png)

  
사용자가 처음으로 앱을 열고 위치 버튼을 탭하면, 시스템은 표준 알림을 팝업으로 보여줍니다. 이 알림은 앱의 위치 접근 권한을 어떻게 제한하는지 사용자에게 안내합니다. 또한, 공유가 시작될 때 나타나는 위치 아이콘을 통해 사용자의 위치를 알려줍니다.


![A screenshot of the alert displayed by the location button that appears on top of a background image showing a partial map of Northern California. The alert reads Park Finder can only access your location when you choose to share it. When you share your location with this app, a blue location indicator will appear in the status bar. Below this text the alert displays a small image of the map, zoomed in to show part of Cupertino. Below the map are two buttons; from the top the titles are OK and Not Now.](https://docs-assets.developer.apple.com/published/465bee128d71f71d03d20d6d9bb175db/location-button-alert@2x.png)
  
버튼의 동작에 대해 사용자가 이해를 확인한 후, 위치 버튼을 간단히 탭하는 것만으로 앱에 사용자의 위치에 대한 일회성 권한이 부여됩니다. 사용자가 앱 사용을 중단할 때마다 일회성 권한은 만료되지만, 앱에서 사용자들에게 버튼의 목적을 설명할 필요는 없습니다.

> 참고
> 
> 앱의 권한이 없는 경우 위치 버튼을 탭하면 - 시스템 권한 허용 창에서 "한 번만 허용"을 선택했을 때와 동일한 효과가 있습니다. 이전에 사용자가 "앱 사용 중에는 위치 권한 허용"을 선택한 경우, 위치 버튼을 탭해도 앱의 상태가 변경되지 않습니다. 개발자 지침은 [`LocationButton`](https://developer.apple.com/documentation/corelocationui/locationbutton)(SwiftUI) 및 [`CLLocationButton`](https://developer.apple.com/documentation/corelocationui/cllocationbutton)(Swift)을 참조하세요.


특정 앱 기능에 대해 사용자에게 위치 정보를 간편하게 공유할 수 있는 방법을 제공하기 위해 위치 버튼의 사용을 고려하세요. 예를 들면, 앱을 통해 사용자가 메시지나 게시물에 자신의 위치를 첨부하거나, 매장을 찾거나, 자신의 위치에서 마주한 건물, 식물 또는 동물을 식별하는 데 도움을 줄 수 있습니다. 사용자가 자주 '한 번만 위치 권한 허용' 권한을 앱에 부여하는 경우, 알림과 반복적으로 상호작용하지 않고도 위치 공유의 이점을 누릴 수 있도록 위치 버튼을 사용하는 것을 고려하세요.

UI와 조화를 이루도록 위치 버튼을 커스텀하는 것을 고려하세요. 구체적으로 다음과 같이 할 수 있습니다:

- 기능과 가장 잘 어울리는 제목을 선택합니다. ex) “현재 위치” 또는 “내 현재 위치 공유”.
- 색이 채워지거나 (fill), 테두리가 있는 (outlined) 위치 아이콘을 사용하세요.
- 배경색 및 제목 색상을 선택합니다.
- 버튼의 corner Radius 반경을 조절합니다.


위치 버튼을 인식하고 신뢰하기 위해, 버튼의 다른 시각적 속성은 커스텀 할 수 없습니다. 위치 버튼이 읽기 쉬운지 확인하기 위해 낮은 대비 색상 조합이나 지나치게 투명한 문제에 대해 시스템에서 경고 메세지를 제공합니다. 또한, 텍스트가 버튼에 맞게 들어가도록 조정을 해야 합니다. 접근성 모드 및 다른 언어를 사용했을 때에도, 버튼 안에 모든 텍스트가 표기되도록 확인해야 합니다. 

> 중요
> 
> 시스템이 커스텀한 위치 버튼에 지속적인 문제가 있다고 판단하면, 사용자가 그것을 탭할 때 앱에 기기의 위치에 대한 접근 권한을 부여하지 않습니다. 이러한 버튼은 다른 앱 특정 작업을 수행할 수 있지만, 위치 버튼이 사용자의 예상대로 작동하지 않으면 사용자는 앱에 대한 신뢰를 잃을 수 있습니다.

## 데이터 보호

사람들의 정보를 보호하는 것은 매우 중요합니다. 로컬에 정보를 저장하거나, 특정 작업에 대한 권한을 부여하거나, 네트워크를 통해 정보를 전송할 때 시스템 제공 보안 기술을 활용하여 사용자들의 개인 정보를 보호하세요.

다음은 몇가지 가이드 라인입니다.

### - 인증을 위해 비밀번호에만 의존하지 마세요. 
가능한 경우 [passkeys](https://developer.apple.com/documentation/authenticationservices/public-private_key_authentication/supporting_passkeys/)를 사용하여 비밀번호를 대체하세요. 인증을 위해 비밀번호 사용을 계속해야하는 경우, 두 단계 인증을 필요로 함으로써 보안을 강화하세요(개발자 가이드를 위해서는 [Securing Logins with iCloud Keychain Verification Codes(iCloud Keychain 검증 코드로 로그인 보호하기)](https://developer.apple.com/documentation/authenticationservices/securing_logins_with_icloud_keychain_verification_codes)를 참조하세요). 기기에서 로그인 상태를 유지하는 앱에 대한 접근을 추가로 보호하기 위해 Face ID, Optic ID 또는 Touch ID와 같은 생체 인식을 사용하세요. 개발자 가이드를 위해서는 [Local Authentication](https://developer.apple.com/documentation/localauthentication)을 참조하세요.

### - 민감한 정보는 키체인에 저장하세요. 
키체인은 누군가의 개인 정보를 처리할 때 안전하고 예측 가능한 사용자 경험을 제공합니다. 개발자 가이드를 위해서는 [Keychain Services](https://developer.apple.com/documentation/security/keychain_services)을 참조하세요.

### - 비밀번호나 기타 보안 내용을 일반 텍스트 파일에 저장하지 마세요. 
파일 권한을 사용하여 접근을 제한하더라도 민감한 정보는 암호화된 키체인에서 훨씬 안전합니다.

### - 사용자 정의 인증 체계를 만드는 것을 피하세요. 
앱이 인증을 필요로 할 경우, [passkeys](https://developer.apple.com/documentation/authenticationservices/public-private_key_authentication/supporting_passkeys/), [Sign in with Apple(애플 로그인)](https://developer.apple.com/design/human-interface-guidelines/sign-in-with-apple) 또는 [Password AutoFill(비밀번호 자동입력)](https://developer.apple.com/documentation/security/password_autofill)과 같은 시스템 제공 기능을 사용하세요. 관련 가이드를 위해서는 계정 관리를 참조하세요.


## 플랫폼 별 고려사항
- iOS, iPadOS, tvOS, watchOS는 해당 사항이 없습니다.

## macOS
### - 유효한 개발자 ID로 앱에 서명을 등록해야 합니다.
스토어 외부에 앱을 배포하기로 선택한 경우 개발자 ID로 앱에 서명하면 Apple 개발자로 식별되고 앱이 안전하게 사용할 수 있음을 확인할 수 있습니다. 개발자 지침은 [Xcode Help](https://developer.apple.com/go/?id=ios-app-distribution-guide)을 참조하십시오.

### - 앱 샌드 박스를 활용해서 유저들의 데이터 보호하세요.
샌드박싱은 악성 코드로부터 앱을 보호하면서 시스템 리소스 및 사용자 데이터에 대한 접근 권한을 앱에 제공합니다. Mac App Store에 제출되는 모든 앱에는 샌드박싱이 필요합니다. 개발자 지침은 [Configuring the macOS App Sandbox](https://developer.apple.com/documentation/Xcode/configuring-the-macos-app-sandbox)을 참조하세요.

### - 로그인한 사용자를 추측하지 마세요. 
사용자 전환이 빠르기 때문에 여러 사람이 동일한 시스템에서 활동할 수 있습니다.

## visionOS
기본적으로, visionOS는 지속성, 월드 맵핑, 세그멘테이션, 매팅, 환경 조명과 같은 기능을 처리하기 위해 ARKit 알고리즘을 사용합니다. 이러한 알고리즘은 항상 실행되어 있어 앱과 게임이 Shared Space(공유 공간)에서 ARKit의 장점을 자동으로 누릴 수 있습니다.

ARKit은 Shared Space 내의 앱에 데이터를 전송하지 않습니다; ARKit API에 접근하려면 앱이 Full Space를 열어야 합니다. 또한, Plane 추정, Scene 재구성, Image 앵커링, Hand 추적과 같은 기능은 정보에 접근하기 위해 유저들의 권한 허용을 필요로 합니다. 개발자 가이드를 위해서는 [Setting up access to ARKit data(ARKit 데이터에 대한 접근 설정)](https://developer.apple.com/documentation/visionOS/setting-up-access-to-arkit-data)을 참조하세요.

visionOS에서는 사용자 입력이 디자인에 의해 개인적으로 처리됩니다. 시스템은 자동으로 사람들이 SwiftUI 또는 RealityKit을 사용하여 만든 컴포넌트에 초점을 맞출 때 호버 효과를 표시하여, 탭하기 전에 그들의 시선 방향을 노출하지 않고 필요한 시각적 피드백을 제공합니다. 가이드를 위해서는 [Focus and selection](https://developer.apple.com/design/human-interface-guidelines/focus-and-selection) 및 [Gestures > visionOS](https://developer.apple.com/design/human-interface-guidelines/gestures#visionOS)를 참조하세요.

개발자의 장치 카메라 접근 방식은 visionOS에서 다른 플랫폼에서와는 다르게 작동합니다. 구체적으로, 후면 카메라는 빈 입력을 제공하며 호환성 편의성으로만 사용할 수 있습니다; 전면 카메라는 Spatial Personas의 입력을 제공하지만 유저들이 권한 허용을 한 이후에만 가능합니다. iOS 또는 iPadOS 앱을 visionOS로 가져오려는데 카메라 접근이 필요한 기능이 포함되어 있다면, 그것을 제거하거나 대체할 수 있는 옵션으로 교체하세요. 개발자 가이드를 위해서는 [Checking whether your existing app is compatible with visionOS(visionOS와 호환되는 기존 앱을 확인하는 방법)](https://developer.apple.com/documentation/visionOS/checking-whether-your-app-is-compatible-with-visionos)을 참조하세요.

---

## 참고

### 개발자 문서

- [Requesting access to protected resources](https://developer.apple.com/documentation/uikit/protecting_the_user_s_privacy/requesting_access_to_protected_resources)
- [Security](https://developer.apple.com/documentation/security)

### 영상

| [Design for location privacy](https://developer.apple.com/videos/play/wwdc2020/10162) | [Meet the Location Button](https://developer.apple.com/videos/play/wwdc2021/10102) | [Apple's privacy pillars in focus](https://developer.apple.com/videos/play/wwdc2021/10085) |
| ------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| ![](https://devimages-cdn.apple.com/wwdc-services/images/49/B39F07BE-4E7A-4530-8BB9-B1C319F262EE/3354_wide_250x141_1x.jpg) | ![4998_wide_250x141_1x.jpg](https://devimages-cdn.apple.com/wwdc-services/images/119/03EB5BF9-AF52-4140-BBCA-4B3D4DD99C96/4998_wide_250x141_1x.jpg) | ![](https://devimages-cdn.apple.com/wwdc-services/images/119/A6395752-EED6-4F4D-9910-6D7B5867BC28/4978_wide_250x141_1x.jpg) |

