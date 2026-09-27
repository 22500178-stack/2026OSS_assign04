# 22500178 김지원

## Key Learning: 이번 주 배운 핵심 내용 3가지
 <input>, <select>, <textarea>, <datalist> 등 다양한 form 입력 요소의 역할과 사용법을 배웠다.

 <fieldset>과 <legend>를 사용해 관련된 입력 필드들을 의미 있게 그룹화하는 방법을 익혔다.

 Pseudo-class에서 :focus와 :hover 속성을 사용하여 사용자의 입력 동작에 반응하는 인터랙티브한 UI 스타일링을 구현했다.

## Form Elements: 사용한 Form 요소와 용도
 <fieldset>, <legend>: 청구지 주소, 결제 방식 등 관련 있는 입력 항목들을 테두리로 묶고 제목을 표시하는 용도로 사용했다.

 <input type="text/email">: 이름, 주소, 이메일 등 단답형 텍스트 데이터를 입력받기 위해 사용했다.

 <select>, <option>: 국가나 주 선택 시 드롭다운 목록에서 하나의 항목을 선택하도록 적용했다.

 <datalist>: 배송 요청사항 입력 시 기본 추천 옵션을 제공하면서, 사용자가 직접 텍스트를 입력할 수 있도록 구현했다.

 <input type="radio">, <input type="checkbox">: 결제 수단 중 하나만 선택하거나, 정보 저장 동의 여부를 체크하는 용도로 활용했다.

 <input type="color">: 사용자가 원하는 테마 강조 색상을 직접 선택할 수 있도록 색상 선택 기능을 제공했다.

 <textarea>: 주문 메모 등 긴 텍스트를 입력받기 위해 사용했다.

 <input type="submit">: form에 입력한 모든 데이터를 최종적으로 제출하는 버튼으로 활용했다.

## HTML vs CSS: form1.html과 form1_css.html의 차이
form1.html은 디자인 요소를 완전히 배제하고, 브라우저 기본 스타일만 적용된 웹페이지의 구조와 입력 요소 배치에만 집중했다. form1_css.html는 css를 적용한 html파일로, form1.html 구조에 내부 스타일시트<style>를 추가하여 여백, 테두리, 색상을 입히고, 클릭 시 입력창 강조, 버튼 마우스 오버 등 시각적 완성도를 향상시켰다.

## Problem & Solution: 문제와 해결 과정
문제: <select> 드롭다운 항목에서 사용자가 선택하지 않아도 기본값이 그냥 제출되었다. Country와 State를 선택할 때, 사용자가 아무것도 고르지 않고 넘어가도 기본값(choose...)으로 설정되거나 선택 검사가 되지 않고 그대로 제출된다.
원인: <option> 태그에 selected 속성이 붙어 있어 자동으로 값이 선택되었고, 필수 선택 속성인 required가 누락되어 있었기 때문이다.
해결: 첫 안내 문구 옵션(<option value="">Choose...</option>)을 빈값(value="")으로 두고, <select required> 속성을 추가한 뒤 다른옵션의 selected를 제거하여 사용자가 반드시 choose...가 아닌 다른 항목을 선택하도록 고쳤다.

## Reflection: 새롭게 알게 된 점 또는 궁금한 점
실제 웹 서비스에서 form의 데이터를 제출할 때, 입력되지 않은 필수 항목이나 잘못된 이메일 형식을 어떻게 실시간으로 유효성 검사를 하는지 궁금해졌다.