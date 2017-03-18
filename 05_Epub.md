# Epub
epub은 Electronic Publication의 줄임말입니다.
확장자는 .epub 을 사용합니다.
전자책의 기술표준 포멧입니다.
실제로 내부를 보면 특별한 기술을 사용하지 않습니다.
기존에 사용해오던 HTML, CSS, Javascript로 구성되어있습니다.
Pandoc이 epub파일을 생성할 때는 기본적으로 epub2 포멧으로 생성됩니다.
epub2는 전자책을 생성할때 필요한 기술이 구현되어있는 포멧입니다.
epub2 포멧에서 epub3 포멧으로 넘어가고 있는 시기입니다.

만약 epub3 형태로 epub파일을 생성하려면 -t 옵션에 epub3 값을 넣어주세요.
아래는 epub3으로 파일을 생성할 때의 예제입니다.

	$ pandoc -t epub3

epub3은 epub2에서 지원하지 않는 기능들을 지원하기위해서 고안된 다음 포멧입니다.
epub3의 특징을 알아보겠습니다.

#### Epub3의 특징
- 오디오와 비디오 지원
- 스크립트 지원
- 메타데이터 추가가능
- MathML을 직접 작성가능
	- 예전에는 수식을 Latex유틸리티로 이미지로 표현하였습니다.
	- MathML에 대한 자세한 설명은 뒤에 다룹니다.
- CSS3 지원
	- CSS3를 지원함에 따라 디테일한 문서 스타일링이 가능합니다.
- OTF, WOFF 지원
	- 글꼴을 epub파일에 포함할 수 있습니다.
- SVG 지원
	- 벡터 그래픽 표현이 가능해졌습니다.
	- SVG에 대한 자세한 설명은 뒤에 다룹니다.