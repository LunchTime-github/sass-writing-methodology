## Scss File Setting
-	variable
	index - import childFile
	variable_color - Color Value
	variable_default - default style (width, height , border, border-radius, box ...)
	variable_layout - Value Data of mediaQuery and layout
-	base
	index - import childFile
	media_query - mixin
	layout_setting - function
	reset - reset css
	font - fontFamily, WebFont, fontSize
-	component
	index - import childFile
	- lo - SMACSS Title Folder (Layout)
	index - import childFile
    StyleTitle - Folder (Class Name)
        index - import childFile
        StyleTitle-layout - Contents Size
        StyleTitle-style - Contents Style Detail
	......
	- ct - SMACSS Title Folder (Main Contentes)
	index - import childFile
    StyleTitle - Folder (Class Name)
        index - import childFile
        StyleTitle-layout - Contents Size
        StyleTitle-style - Contents Style Detail
	......
	- cp - SMACSS Title Folder (Components (Button, table...))
	index - import childFile
    StyleTitle - Folder (Class Name)
        index - import childFile
        StyleTitle-layout - Contents Size
        StyleTitle-style - Contents Style Detail
        ......

## Layout Setting

-   _variable_layout 에 변수 구성
-   "", sm, md, lg, xl 구성, 각 요소별 사이즈 수정 -> $mq_width 에서 수정
-	mq_width, mq_data의 첫번째 배열의 공백 유지
-   16 단 그리드 Default 설정
-   media (min-width: $SIZE)
-   layout Wrap class 에 "@extend %__row_${영문 사이즈}" 작성 
-   layout 을 적용시키고 싶은 class 에 "@extend %__layout_${영문 사이즈}_${숫자 사이즈}" 작성
-   @extend 는 -layout 파일에만 적용, 이후 자식 생성 금지

## Media Query Setting

-	_media_query 에 mixin 구성
-	media (min-width: $SIZE)
-	@include mq(${영문 사이즈})로 Mixin 작성