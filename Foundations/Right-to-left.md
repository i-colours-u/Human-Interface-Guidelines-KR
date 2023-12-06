# Right to Left

## 관련 스크립트의 읽기 방향에 맞게 필요에 따라 UI 인터페이스를 좌우로 반전하여 아랍어, 히브리어와 같은 오른쪽에서 왼쪽으로 읽는 언어를 지원합니다.

![A sketch of a right-aligned bulleted list within a window, suggesting an interface displayed in a right-to-left language. The image is overlaid with rectangular and circular grid lines and is tinted yellow to subtly reflect the yellow in the original six-color Apple logo.](https://docs-assets.developer.apple.com/published/5d683460f2af897b631f4dad86fd3473/foundations-rtl-intro@2x.png)


사람들은 자신의 기기 또는 앱이나 게임의 언어를 선택할 때 UI 인터페이스가 다양한 방식으로 적응하기를 기대합니다(자세한 내용은 [Localization](https://developer.apple.com/localization/)을 참조하세요).

시스템 제공 UI 프레임워크는 기본적으로 오른쪽에서 왼쪽으로(RTL)를 지원하므로 시스템 제공 UI 컴포넌트가 RTL 컨텍스트에서 자동으로 좌우 반전될 수 있습니다. 시스템 제공 요소와 표준 레이아웃을 사용하는 경우 앱의 자동 반전 인터페이스를 변경할 필요가 없을 수 있습니다.

RTL 언어를 사용하는 국가의 다양한 지역에서 발생할 수 있는 다양한 통화, 숫자 또는 수학 기호에 맞게 레이아웃을 미세 조정하거나 특정 로컬라이제이션을 개선하려면 다음 지침을 따르세요.

## 텍스트 정렬 (Test alignment)

시스템에서 자동으로 정렬하지 않는 경우 인터페이스 방향에 맞게 텍스트 정렬을 조정합니다. 예를 들어, 왼쪽에서 오른쪽(LTR) 컨텍스트의 콘텐츠에 텍스트를 왼쪽으로 정렬한 경우 RTL 컨텍스트에서 콘텐츠의 미러링된 위치와 일치하도록 텍스트를 오른쪽으로 정렬합니다.


| LTR 상황에서 왼쪽 정렬한 상태 | RTL 상황에서 오른쪽 정렬한 상태 |
| ----------------------------- | ------------------------------- |
|    ![An illustration showing a layout of text and images in an interface. Three bars that represent text are left-aligned above a rounded rectangle area. A placeholder image is centered in the area, above another bar at the bottom edge. The bar inside the area is left-aligned.](https://docs-assets.developer.apple.com/published/7bdc0741a96d6e2aa88b79c64e151c8a/text-alignment-ltr-screen@2x.png)                           |    ![An illustration showing a layout of text and images in an interface. Three bars that represent text are right-aligned above a rounded rectangle area. A placeholder image is centered in the area, above another bar at the bottom edge. The bar inside the area is right-aligned. The placeholder image isn't flipped.](https://docs-assets.developer.apple.com/published/10386033d677b3fd65ec33ac16d67e56/text-alignment-rtl-screen@2x.png)                             |


#### 현재 문맥이 아닌 해당 언어를 기준으로 단락을 정렬하세요.

세 줄 이상의 텍스트로 정의되는 단락의 정렬이 해당 언어와 일치하지 않으면 읽기 어려울 수 있습니다. 예를 들어 LTR 텍스트로 구성된 단락을 오른쪽으로 정렬하면 각 줄의 시작 부분이 잘 보이지 않을 수 있습니다. 가독성을 높이려면 한 줄 및 두 줄 텍스트 블록을 현재 문맥의 읽기 방향과 일치하도록 계속 정렬하되 단락을 해당 언어와 일치하도록 정렬하세요.

| ![A checkmark in a circle to indicate a correct example.](https://docs-assets.developer.apple.com/published/88662da92338267bb64cd2275c84e484/checkmark@2x.png) | ![An X in a circle to indicate an incorrect example.](https://docs-assets.developer.apple.com/published/209f6f0fc8ad99d9bf59e12d82d06584/crossout@2x.png) |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| RLT 상황에서 왼쪽으로 정렬된 단락                                                                                                                              | RLT 상황에서 오른쪽으로 정렬된 단락                                                                                                                       |
|    ![An image showing two paragraphs of placeholder copy. The first paragraph is in Arabic and is right-aligned. The second paragraph is in English and is left-aligned.](https://docs-assets.developer.apple.com/published/b32ae443b1d7daa1bb661b56b42b8a34/paragraph-alignment-correct@2x.png)                                                                                                                                                            |            ![An image showing two paragraphs of placeholder copy. The first paragraph is in Arabic and the second paragraph is in English. Both paragraphs are right-aligned.](https://docs-assets.developer.apple.com/published/738bda44c81a146b02cbd67db5985ff2/paragraph-alignment-wrong@2x.png)                                                                                                                                               |


#### 목록의 모든 텍스트 항목에 일관된 맞춤을 사용합니다. 

편안한 읽기 및 스캔 환경을 보장하려면 다른 스크립트로 표시되는 항목을 포함하여 목록의 모든 항목의 정렬을 반대로 하세요.

| ![A checkmark in a circle to indicate a correct example.](https://docs-assets.developer.apple.com/published/88662da92338267bb64cd2275c84e484/checkmark@2x.png) | ![An X in a circle to indicate an incorrect example.](https://docs-assets.developer.apple.com/published/209f6f0fc8ad99d9bf59e12d82d06584/crossout@2x.png) |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| RLT 상황에서 오른쪽으로 정렬된 단락                                                                                                                              | RLT 상황에서 정렬 순서가 섞인 상황                                                                                                                     |
|                     ![An illustration of a right-aligned list of gray bars that represent right-to-left text.](https://docs-assets.developer.apple.com/published/8e497bdc80a98b7896b492d2e5bfb57b/mixed-script-list-alignment-correct@2x.png)                                                                                                                                         |           ![An illustration of a list of gray bars. The first, third, fourth, and fifth bars represent right-to-left text. The second bar is incorrectly left-aligned.](https://docs-assets.developer.apple.com/published/8764f467c4870522419bb26fa5894c09/mixed-script-list-alignment-wrong@2x.png)                                                                                                                                               |


## 숫자 및 문자

RTL 언어마다 서로 다른 숫자 체계를 사용할 수 있습니다. 예를 들어 히브리어 텍스트는 서아랍 숫자를 사용하는 반면, 아랍어 텍스트는 서아랍 숫자 또는 동아랍 숫자를 사용할 수 있습니다. 서양 아라비아 숫자와 동방 아라비아 숫자의 사용은 국가와 지역, 심지어 같은 국가나 지역 내에서도 지역마다 다릅니다.

앱에서 수학적 개념이나 기타 숫자 중심의 주제를 다루는 경우, 지원하는 각 지역에서 이러한 정보를 표시하는 적절한 방법을 파악하는 것이 좋습니다. 반대로 숫자 관련 주제를 다루지 않는 앱은 일반적으로 시스템에서 제공하는 숫자 표현에 의존할 수 있습니다.

| 서아랍 숫자 표기법 | 동아랍 숫자 표기법 |
| ------------------ | ------------------ |
|        ![From the left, the numerals one, two, and three in Western Arabic numerals.](https://docs-assets.developer.apple.com/published/c40d3d208a9aee56d680d6915fb44fff/textformat-123-ltr@2x.png)            |       ![From the right, the numerals one, two, and three in Eastern Arabic numerals.](https://docs-assets.developer.apple.com/published/8a9f9c2f6fb291304a5d93e27be0bead/textformat-123-ar@2x.png)             |


#### 특정 번호의 숫자 순서를 바꾸지 마세요.

현재 언어나 주변 콘텐츠에 관계없이 '541', 전화번호 또는 신용카드 번호와 같은 특정 숫자의 자릿수는 항상 같은 순서로 표시됩니다.


| 라틴어 | 히브리어 |
| --------- | -------- |
|  ![From the left, the two words order and number followed by the number 123456 in Latin script.](https://docs-assets.developer.apple.com/published/e6ae8d9dab2a6da825829cf88bfb6adb/latin-numerals@2x.png)         |    ![From the right, the two words order and number followed by the number 12345 in Hebrew script.](https://docs-assets.developer.apple.com/published/587fbba724987c3fa82e88f7fe8afff5/hebrew-numerals@2x.png)      |

| 서아랍 숫자 표기법 | 동아랍 숫자 표기법 |
| ------------------ | ------------------ |
|     ![From the right, the two words order and number in Arabic script, followed by the number 12345 in Western Arabic numerals.](https://docs-assets.developer.apple.com/published/427e50992b8e4900fa7f64c73ad8c0b1/western-arabic-numerals@2x.png)               |  ![From the right, the two words order and number in Arabic script, followed by the number 12345 in Eastern Arabic numerals.](https://docs-assets.developer.apple.com/published/6edfa8597370c06b66cdbbaae728f97b/eastern-arabic-numerals@2x.png)                  |

#### 진행률 또는 카운트 방향을 표시하는 숫자 순서 자체를 뒤집어야 합니다. 숫자 자체를 뒤집지 마세요. 

진행률 표시줄, 슬라이더 및 등급 컨트롤과 같은 컨트롤에는 의미를 명확히 하기 위해 숫자가 포함되는 경우가 많습니다. 이러한 방식으로 숫자를 사용하는 경우 뒤집힌 컨트롤의 방향과 일치하도록 숫자의 순서를 뒤집어야 합니다. 또한 특정 순서를 전달하기 위해 시퀀스를 사용하는 경우 숫자 순서를 반대로 하세요.

| 라틴어 | 서아랍 숫자 표기법 |
| ------ | ------------------ |
|   ![A horizontal row of five stars. From the left, the first three and a half stars are filled. Below the stars is a row of Latin numerals, each numeral vertically aligned with a star above. From the left, the numerals are one, two, three, four, and five.](https://docs-assets.developer.apple.com/published/d249f8e9df8a8dfcf1526dc3f5c4dd5b/match-numeral-order-to-directional-controls-latin@2x.png)     |    ![A horizontal row of five stars. From the right, the first three and a half stars are filled. Below the stars is a row of Eastern Arabic numerals, each numeral vertically aligned with a star above. From the right, the numerals are one, two, three, four, and five.](https://docs-assets.developer.apple.com/published/77bb1e2c8c704fa2235bd7cc8d7acf31/match-numeral-order-to-directional-controls-eastern-arabic@2x.png)                |

| 히브리어 | 동아랍 숫자 표기법 |
| -------- | ------------------ |
|      ![A horizontal row of five stars. From the right, the first three and a half stars are filled. Below the stars is a row of Western Arabic numerals, each numeral vertically aligned with a star above. From the right, the numerals are one, two, three, four, and five.](https://docs-assets.developer.apple.com/published/164c27556e186de5aa0c0312639f1c8f/match-numeral-order-to-directional-controls-western-arabic-hebrew@2x.png)    |![A horizontal row of five stars. From the right, the first three and a half stars are filled. Below the stars is a row of Western Arabic numerals, each numeral vertically aligned with a star above. From the right, the numerals are one, two, three, four, and five.](https://docs-assets.developer.apple.com/published/164c27556e186de5aa0c0312639f1c8f/match-numeral-order-to-directional-controls-western-arabic-hebrew@2x.png)                    |

## 컨트롤 요소

#### 한 값에서 다른 값으로의 진행률을 표시하는 컨트롤을 반전시키세요. 

사람들은 앞으로의 진행 상황을 읽는 언어와 같은 방향으로 움직이는 것으로 간주하는 경향이 있으므로 슬라이더 및 진행률 표시기와 같은 컨트롤을 RTL 컨텍스트에서 뒤집는 것이 좋습니다. 이렇게 할 때는 컨트롤의 시작 값과 끝 값을 나타내는 함께 제공되는 아이콘 또는 이미지의 위치도 뒤집어야 합니다.

| LTR 상황에서 방향성이 있는 컨트롤 요소 | RLT 상황에서 방향성이 있는 컨트롤 요소 |
| -------------------------------------- | -------------------------------------- |
|        ![Partial screenshot of the Books app's display adjustment popover in English on iPhone. At the top of the popover, a slider uses a small sun glyph on the left and a large sun glyph on the right to show that moving the thumb from left to right makes the display brighter. Below the slider is a row of two buttons. The left button uses a small capital letter A to indicate the text getting smaller and the right button uses a large capital letter A to indicate the text getting larger.](https://docs-assets.developer.apple.com/published/cc05fe22979e0dfa7fd52b762bddbeb8/flipped-directional-control-ltr@2x.png)                                | ![Partial screenshot of the Books app's display adjustment popover in Arabic on iPhone. At the top of the popover, a slider uses a small sun glyph on the right and a large sun glyph on the left to show that moving the thumb from right to left makes the display brighter. Below the slider is a row of two buttons. The right button uses a small version of the letter Ain to indicate the text getting smaller and the left button uses a large version of the letter Ain to indicate the text getting larger.](https://docs-assets.developer.apple.com/published/4a3855e794433c6cab59da388bf3805b/flipped-directional-control-rtl@2x.png)                                       |

#### 플립 컨트롤은 사람들이 고정된 순서로 항목을 탐색하거나 액세스할 수 있도록 도와줍니다. 
예를 들어, RTL 컨텍스트에서 뒤로 버튼은 오른쪽을 가리켜야 화면의 흐름이 RTL 언어의 읽기 순서와 일치합니다. 마찬가지로, 정렬된 목록의 항목에 액세스할 수 있는 다음 또는 이전 버튼은 읽기 순서와 일치하도록 RTL 컨텍스트에서 플립해야 합니다.

#### 실제 방향을 가리키거나 화면의 특정 영역을 가리키는 컨트롤의 방향을 유지합니다. 
예를 들어 '오른쪽'을 의미하는 컨트롤을 제공하는 경우 현재 컨텍스트에 관계없이 항상 오른쪽을 가리켜야 합니다.

#### 필요한 경우 인접한 라틴어 스크립트와 RTL 스크립트의 시각적 균형을 조정합니다. 
버튼, 레이블 및 제목에서 아랍어와 히브리어는 대문자를 포함하지 않기 때문에 대문자로 된 라틴어 텍스트 옆에 아랍어 또는 히브리어 텍스트가 너무 작게 표시될 수 있습니다. 아랍어 또는 히브리어 텍스트와 대문자를 모두 사용하는 라틴어 텍스트의 시각적 균형을 맞추려면 RTL 글꼴 크기를 2포인트 정도 늘리는 것이 효과적입니다.


![A horizontal row of three blue oval buttons. Each button is labeled with the word download. From the left, the labels are in Latin, Arabic, and Hebrew scripts, with the English label using all capital letters. Two horizontal red lines run across all three buttons, the top line is the ascender line and the bottom line is the baseline. Every letter in the English label touches both lines. Only the last two letters in the Arabic label touch or extend below the baseline; only the last letter touches the ascender line. No letters in the Hebrew label touch either line. In comparison with the Latin label, both the Arabic and Hebrew labels look small.](https://docs-assets.developer.apple.com/published/190b48a71d8d934047905be986732fb4/download-uneven-vertical-height@2x.png)

아랍어 및 히브리어 텍스트는 글꼴 크기가 같은 라틴어 대문자 텍스트 옆에서 너무 작게 보일 수 있습니다.

![A horizontal row of three blue oval buttons. Each button is labeled with the word download. From the left, the labels are in Latin, Arabic, and Hebrew scripts, with the English label using all capital letters. Two horizontal red lines run across all three buttons, the top line is the ascender line and the bottom line is the baseline. Every letter in the English label touches both lines. The last two letters in the Arabic label touch or extend below the baseline, and the first and last letters extend above the ascender line. All letters in the Hebrew label touch the base line and the ascender line. The increased size of the Arabic and Hebrew labels make them look similar in size to the Latin label.](https://docs-assets.developer.apple.com/published/19099f313875cd49849a1ca28f1dfca4/download-even-vertical-height@2x.png)

아랍어와 히브리어 텍스트의 글꼴 크기를 약간 늘려서 라틴어 대문자와 시각적으로 균형을 맞출 수 있습니다.

## Images

#### 사진, 일러스트레이션 및 일반 아트웍과 같은 이미지를 뒤집지 마세요. 이미지를 뒤집으면 이미지의 의미가 바뀌는 경우가 많으므로 저작권이 있는 이미지를 뒤집는 것은 위반이 될 수 있습니다. 
이미지의 콘텐츠가 읽기 방향과 밀접한 관련이 있는 경우 원본을 뒤집는 대신 새 버전의 이미지를 만드는 것이 좋습니다.


| ![A checkmark in a circle to indicate a correct example.](https://docs-assets.developer.apple.com/published/88662da92338267bb64cd2275c84e484/checkmark@2x.png) | ![An X in a circle to indicate an incorrect example.](https://docs-assets.developer.apple.com/published/209f6f0fc8ad99d9bf59e12d82d06584/crossout@2x.png) |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
|          ![A simplified illustration of a globe that uses solid black shapes to show most of Africa, Europe, Asia, Australia, and Antarctica.](https://docs-assets.developer.apple.com/published/ca80fd6003c4ebff97714123a33c974e/image-displayed-right@2x.png)                                                                                                                                                      |                     ![A simplified illustration of a globe that shows a horizontally flipped Eastern hemisphere with Africa on the far right and Australia on the far left.](https://docs-assets.developer.apple.com/published/0310648a2b1ff40a796e5544d057d30b/image-displayed-wrong@2x.png)                                                                                                                                      |

#### 이미지의 순서가 의미 있는 경우 이미지의 위치를 반전시킵니다.
예를 들어 여러 이미지를 시간순, 알파벳순, 즐겨찾기와 같은 특정 순서로 표시하는 경우 이미지의 위치를 반전시켜 RTL 컨텍스트에서 순서의 의미를 유지합니다.



| LTR에서 중요한 항목 배치 | RLT에서 중요한 항목 배치 |
| ------------------------ | ------------------------ |
|       ![An illustration showing a layout of text and images within a rounded rectangle. A short bar representing text is left-aligned in the upper-left corner. Below the bar is an area that contains four squares, including a blue square with a placeholder image on the left side. From the left, a row of five square areas at the bottom of the rectangle contain the following shapes: heart, circle, star, square, and triangle.](https://docs-assets.developer.apple.com/published/f8e833e7f73aa3f6ce268dd33f174862/image-positions-ltr@2x.png)                   |   ![An illustration showing a layout of text and images within a rounded rectangle. A short bar representing text is right-aligned in the upper-right corner. Below the bar is an area that contains four squares, including a blue square with a placeholder image on the right side. From the right, a row of five square areas at the bottom of the rectangle contain the following shapes: heart, circle, star, square, and triangle.](https://docs-assets.developer.apple.com/published/5071b9cf5e2c0a2395803018149eab87/image-positions-rtl@2x.png)                       |

#### 인터페이스 아이콘

[SF Symbols](https://developer.apple.com/design/human-interface-guidelines/sf-symbols)을 사용하여 앱의 인터페이스 아이콘을 제공하면 RTL 컨텍스트에 맞는 변형과 아랍어 및 히브리어 등의 언어에 대한 현지화된 심볼을 얻을 수 있습니다. 사용자 지정 심볼을 만드는 경우 방향성을 지정할 수 있습니다. 개발자 지침은 [Creating custom symbol images for your app](https://developer.apple.com/documentation/uikit/uiimage/creating_custom_symbol_images_for_your_app)를 참조하세요.

![Three horizontal lines, stacked evenly on top of each other. Each line is preceded by a bullet on left. The shape of a closed book with its spine on the left. A rounded rectangle containing a left-aligned row of three dots. A pencil is slanted at about forty-five degrees, with its point right of the rightmost dot and its eraser extending out of the top-right corner of the rectangle. A rounded rectangle with a black bar across the top that occupies about a quarter of the rectangle's height. A left-aligned row of white dots is in the left side of the bar. A rounded rectangle that contains a smaller, solid-black rounded rectangle near the left side. Outside the rectangle and to the right is a solid-black semicircle with a vertical straight edge that's close to the vertical right side of the rectangle.](https://docs-assets.developer.apple.com/published/eec2236f5595e04904c2b5494696ec1b/directional-symbols-ltr@2x.png)
LTR 상황에서 방향성이 있는 아이콘들



![Three horizontal lines, stacked evenly on top of each other. Each line is preceded by a bullet on right. The shape of a closed book with its spine on the right. A rounded rectangle containing a right-aligned row of three dots. A pencil is slanted at about forty-five degrees, with its point left of the leftmost dot and its eraser extending out of the middle of the rectangle's top. A rounded rectangle with a black bar across the top that occupies about a quarter of the rectangle's height. A right-aligned row of white dots is in the right side of the bar. A rounded rectangle that contains a smaller, solid-black rounded rectangle near the right side. Outside the rectangle and to the left is a solid-black semicircle with a vertical straight edge that's close to the vertical left side of the rectangle.](https://docs-assets.developer.apple.com/published/9f036ccf7a0ca74375f080c94feb77a3/directional-symbols-rtl@2x.png)
RTL 상황에서 방향성이 있는 아이콘들

#### 텍스트 또는 읽기 방향을 나타내는 인터페이스 아이콘을 뒤집습니다. 
예를 들어, 인터페이스 아이콘이 왼쪽으로 정렬된 막대를 사용하여 LTR 컨텍스트에서 텍스트를 나타내는 경우 RTL 컨텍스트에서는 막대를 오른쪽으로 정렬합니다.


| LTR에서 텍스트 기호 | RTL에서 텍스트 기호 |
| ------------------- | ------------------- |
|       ![A rounded rectangle that contains three horizontal left-aligned lines.](https://docs-assets.developer.apple.com/published/298befd594e841846cd466f60d2bea6a/doc-plaintext-ltr@2x.png)              |     ![A rounded rectangle that contains three horizontal right-aligned lines.](https://docs-assets.developer.apple.com/published/bfae7054f6aec52f1a63e31b6c0db79d/doc-plaintext-rtl@2x.png)                |

#### 텍스트를 표시하는 인터페이스 아이콘의 현지화된 버전을 만들어 보세요.
일부 인터페이스 아이콘에는 글꼴 크기 선택 또는 서명과 같은 스크립트 관련 개념을 전달하는 데 도움이 되는 문자나 단어가 포함되어 있습니다. 실제 텍스트를 표시해야 하는 사용자 지정 인터페이스 아이콘이 있는 경우에는 현지화된 버전을 만드는 것이 좋습니다. 예를 들어 SF 심볼은 라틴어, 히브리어, 아랍어 텍스트 등에 사용할 수 있는 다양한 버전의 서명, 서식 있는 텍스트 및 I-빔 포인터 심볼을 제공합니다.

![A small X left-aligned above a horizontal line. A stylized signature begins at the X and finishes at the right end of the line. A rounded rectangle containing a capital letter A in the top-left corner and a stack of two horizontal lines in the top-right corner. A placeholder image appears in the bottom half of the rectangle. A large capital letter A to the left of a tall I-beam cursor.](https://docs-assets.developer.apple.com/published/431f27ff945804173931cfd38f595b2c/text-icon-localized-latin@2x.png)
라틴어 버전

![A small X right-aligned above a horizontal line. A stylized signature begins at the X and finishes at the left end of the line. A rounded rectangle containing the letter Alef in the top-right corner and a stack of two horizontal lines in the top-left corner. A placeholder image appears in the bottom half of the rectangle. A large letter Alef to the right of a tall I-beam cursor.](https://docs-assets.developer.apple.com/published/b457fc7b677ccbf085cd1ea1d8bc5601/text-icon-localized-hebrew@2x.png)

히브리어 버전

![A small X right-aligned above a horizontal line. A stylized signature begins at the X and finishes at the left end of the line. A rounded rectangle containing the letter Ain in the top-right corner and a stack of two horizontal lines in the top-left corner. A placeholder image appears in the bottom half of the rectangle. A large letter Dad to the right of a tall I-beam cursor.](https://docs-assets.developer.apple.com/published/7c91fa369eb21255aed0a545bcf9b62d/text-icon-localized-arabic@2x.png)

아랍어 버전


문자나 단어를 사용하여 읽기 또는 쓰기와 관련이 없는 개념을 전달하는 사용자 지정 인터페이스 아이콘이 있는 경우 텍스트를 사용하지 않는 대체 이미지를 디자인하는 것이 좋습니다.

#### 앞으로 또는 뒤로 움직이는 인터페이스 아이콘을 뒤집습니다. 
사람들이 읽는 방향과 같은 방향으로 무언가가 움직이면 일반적으로 그 방향을 앞으로, 반대 방향으로 움직이면 뒤로 해석하는 경향이 있습니다. 앞으로 또는 뒤로 움직이는 물체를 나타내는 인터페이스 아이콘은 동작의 의미를 유지하려면 RTL 컨텍스트에서 뒤집혀야 합니다. 예를 들어 스피커를 나타내는 아이콘은 일반적으로 스피커에서 앞으로 나오는 음파를 나타냅니다. LTR 컨텍스트에서는 음파가 왼쪽에서 나오므로 RTL 컨텍스트에서는 아이콘을 뒤집어 오른쪽에서 나오는 음파를 표시해야 합니다.

| 소리가 앞으로 나아가는 동작을 나타내는 LTR 아이콘 | 소리가 앞으로 나아가는 동작을 나타내는 RLT 아이콘 |
| ------------------------------------------------- | ------------------------------------------------- |
|  ![The outline of a speaker with three concentric curved lines emanating to the right.](https://docs-assets.developer.apple.com/published/d43d629eea61239a9268d6616551b48c/speaker-wave-3-ltr@2x.png) | ![The outline of a speaker with three concentric curved lines emanating to the left.](https://docs-assets.developer.apple.com/published/d10bb4c00b214c16a802183377134b59/speaker-wave-3-rtl@2x.png)|


#### 로고나 보편적인 기호 및 마크를 뒤집어 표시하지 마세요. 
로고를 뒤집어 표시하면 사람들에게 혼란을 주고 법적인 영향을 미칠 수 있습니다. 로고는 텍스트가 포함되어 있더라도 항상 원래 형태 그대로 표시하세요. 사람들은 체크 표시와 같은 보편적인 기호와 마크가 일관된 모양을 갖기를 기대하므로 뒤집지 마세요.

| 로고 | 일관된 의미를 가진 기호나 마크 |
| ---- | ------------------------------ |
|  ![A rounded square that contains the black Apple TV logo, which consists of a solid black apple to the left of the lowercase letters T and V.](https://docs-assets.developer.apple.com/published/7c7eb6d19b63d77412c7754893c0f65c/appletv-ltr@2x.png)    |   ![A checkmark.](https://docs-assets.developer.apple.com/published/31cfb3b8b93a1747eddac562a979a9cb/checkmark-ltr@2x.png)                             |


#### 일반적으로 실제 사물을 나타내는 인터페이스 아이콘은 뒤집지 마세요. 
개체를 사용하여 방향성을 나타내는 경우가 아니라면 익숙한 항목을 나타내는 아이콘을 뒤집지 않는 것이 가장 좋습니다. 예를 들어 시계는 모든 곳에서 동일하게 작동하므로 기존의 시계 인터페이스 아이콘은 언어 방향에 관계없이 동일하게 보여야 합니다. 일부 인터페이스 아이콘은 오른손잡이용으로 기울어진 항목을 나타내기 때문에 언어나 읽는 방향을 나타내는 것처럼 보일 수 있습니다. 그러나 대부분의 사람들은 오른손잡이이므로 오른손잡이 도구를 표시하는 아이콘을 뒤집는 것은 필요하지 않으며 오히려 혼란을 줄 수 있습니다.

|     |     |     |
| --- | --- | --- |
|  ![A black disk with two white lines in the nine o'clock position.](https://docs-assets.developer.apple.com/published/2d167db99027c9f44270a86a273f225f/clock-fill-ltr@2x.png)   |   ![A pencil with an eraser, slanted at about forty-five degrees with the point in the bottom-left.](https://docs-assets.developer.apple.com/published/6597719e77e19638bb265cd6c58f9a8a/pencil-ltr@2x.png)  |   ![The silhouette of a game controller with a white plus sign on the left and two white buttons on the right.](https://docs-assets.developer.apple.com/published/c3f51c228de248bf096aae7164836eab/gamecontroller-fill-ltr@2x.png)  |

#### 복잡한 사용자 지정 인터페이스 아이콘을 단순히 뒤집기 전에 개별 구성 요소와 전체적인 시각적 균형을 고려하세요.
배지, 슬래시 또는 돋보기와 같은 구성 요소는 localization과 관계없이 시각적 디자인 언어를 준수해야 하는 경우도 있습니다. 예를 들어 SF 심볼은 LTR 버전과 RTL 버전 모두에서 동일한 백슬래시를 사용하여 심볼의 의미에 대한 금지 또는 부정을 표현함으로써 시각적 일관성을 유지합니다.


| LTR에서 백슬래쉬를 포함한 음소거 아이콘 | RTL에서 백슬래쉬를 포함한 음소거 아이콘 |
| --------------------------------------- | --------------------------------------- |
|        ![A silhouette of a speaker pointing right with a backslash on top of it.](https://docs-assets.developer.apple.com/published/d9f54801d79a03d6abc39b665a95b00d/speaker-slash-fill-ltr@2x.png)                                 |   ![A silhouette of a speaker pointing left with a backslash on top of it.](https://docs-assets.developer.apple.com/published/42dc822fc59ebc4c8d02d6e6c7fa0959/speaker-slash-fill-rtl@2x.png)                                      |

다른 경우에는 현지화된 버전의 아이콘이 여전히 의미가 있도록 구성 요소(또는 그 위치)를 뒤집어야 할 수도 있습니다. 예를 들어, 배지가 앱에서 사용자에게 표시되는 실제 UI를 나타내는 경우 UI가 플립되면 배지도 플립되어야 합니다. 또는 배지가 인터페이스 아이콘의 의미를 수정하는 경우 배지를 뒤집어도 수정된 의미와 아이콘의 전체적인 시각적 균형이 유지되는지 고려해야 합니다. 아래 이미지에서 배지는 UI의 개체를 나타내지 않지만 오른쪽 상단에 유지하면 시각적으로 카트의 균형이 맞지 않습니다.


| ![A checkmark in a circle to indicate a correct example.](https://docs-assets.developer.apple.com/published/88662da92338267bb64cd2275c84e484/checkmark@2x.png) | ![An X in a circle to indicate an incorrect example.](https://docs-assets.developer.apple.com/published/209f6f0fc8ad99d9bf59e12d82d06584/crossout@2x.png) | ![A checkmark in a circle to indicate a correct example.](https://docs-assets.developer.apple.com/published/88662da92338267bb64cd2275c84e484/checkmark@2x.png) |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|         ![A silhouette of a wheeled shopping cart that faces right. A white plus sign inside a black disk is in the top-right corner.](https://docs-assets.developer.apple.com/published/faa9849953c7b1b1470db91ed25125d0/cart-fill-badge-plus-ltr@2x.png)                                                                                                                                                       |                   ![A silhouette of a wheeled shopping cart that faces left. A white plus sign inside a black disk is in the top-right corner.](https://docs-assets.developer.apple.com/published/c065f8369e681461bc34ea590b80994b/cart-fill-badge-rtl-unbalanced@2x.png)                                                                                                                                        | ![A silhouette of a wheeled shopping cart that faces left. A white plus sign inside a black disk is in the top-left corner.](https://docs-assets.developer.apple.com/published/97251e1850265c3b1d654d1e4631ca74/cart-fill-badge-plus-rtl@2x.png)                                                                                                                                                               |

사용자 지정 인터페이스 아이콘에 도구와 같이 손으로 만지는 것을 암시할 수 있는 구성 요소가 포함된 경우, 필요한 경우 기본 이미지를 뒤집으면서 도구의 방향을 유지하는 것이 좋습니다.

| 도구를 나타내는 LTR 아이콘 | 도구를 나타내는 RLT 아이콘 |
| -------------------------- | -------------------------- |
|   ![A rounded rectangle that contains a black dot in the top-right corner. The outline of a magnifying glass that contains a stack of two left-aligned lines is on top of the rectangle and to the left of the dot, slanted at about 135 degrees.](https://docs-assets.developer.apple.com/published/0c8dd8148be262162bb75a017e2ae197/mail-and-text-magnifyingglass-ltr@2x.png)                         |    ![A rounded rectangle that contains a black dot in the top-left corner. The outline of a magnifying glass that contains a stack of two rightt-aligned lines is on top of the rectangle and to the right of the dot, slanted at about 135 degrees.](https://docs-assets.developer.apple.com/published/f3ca739120456691b67e55d150596716/mail-and-text-magnifyingglass-rtl@2x.png)                        |

## 플랫폼별 고려사항

- iOS, iPadOS, macOS, tvOS, visionOS, watchOS 추가적인 고려사항은 없습니다.


## 관련 자료

[Layout](./Layout.md)
[Inclusion](./Inclusion.md)
[SF Symbols](https://developer.apple.com/design/human-interface-guidelines/sf-symbols)

### 개발자 참고 문서

[Preparing views for localization](https://developer.apple.com/documentation/SwiftUI/Preparing-views-for-localization) — SwiftUI

### 관련 영상

| [Design for Arabic](https://developer.apple.com/videos/play/wwdc2022/10034) | [Writing for interfaces](https://developer.apple.com/videos/play/wwdc2022/10037) | [The practice of inclusive design](https://developer.apple.com/videos/play/wwdc2021/10275) |
| --------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ |
|   ![](https://devimages-cdn.apple.com/wwdc-services/images/124/7F5167EA-F6A3-4605-83FF-FF75E802969C/6527_wide_250x141_1x.jpg)                                                                          |     ![](https://devimages-cdn.apple.com/wwdc-services/images/124/E58B8A59-15C1-4FB4-B61A-23DBA2AF6D28/6530_wide_250x141_1x.jpg)                                                                             |                                                                                         ![](https://devimages-cdn.apple.com/wwdc-services/images/119/90B67086-3A99-49A5-965A-D35DB6552AE0/5206_wide_250x141_1x.jpg)