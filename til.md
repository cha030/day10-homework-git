* <header> 페이지나 섹션의 소개(머리말) 역할을 하는 요소가 들어갑니다.
보통 들어가는 요소
✅ 사이트 로고
✅ 사이트 제목(h1)
✅ 내비게이션 메뉴(nav)
✅ 검색창
✅ 로그인/회원가입 버튼
✅ 프로필 아이콘
✅ 언어 선택 메뉴

* # `nav`와 페이지 내 이동(앵커 링크)
## `nav`란? `nav`는 **내비게이션(navigation)** 태그로, 사용자가 다른 페이지나 같은 페이지의 다른 위치로 이동할 수 있는 **메뉴**를 묶는 태그이다.
예시
<nav>
  <a href="#about">소개</a>
  <a href="#skills">기술</a>
  <a href="#contact">연락처</a>
</nav>

## `href="#id"`의 의미
<a href="#about">소개</a>
* `#about`는 **`id="about"`인 요소를 찾으라는 의미**이다.
* 링크를 클릭하면 해당 요소가 있는 위치로 자동으로 이동(스크롤)한다.

예시
```html id="2wg6gx"
<section id="about">
  <h2>소개</h2>
</section>

<section id="skills">
  <h2>기술</h2>
</section>

<section id="contact">
  <h2>연락처</h2>
</section>
```
### 이동 결과
* `href="#about"` → `id="about"` 섹션으로 이동
* `href="#skills"` → `id="skills"` 섹션으로 이동
* `href="#contact"` → `id="contact"` 섹션으로 이동

* 부드럽게 스크롤하기
html {  scroll-behavior: smooth;}
위 CSS를 추가하면 링크를 클릭했을 때 해당 섹션으로 **부드럽게 스크롤**된다.

* fieldset과 section
section = 페이지의 구역 나누기
fieldset = 입력창 묶기
legend = fieldset의 제목

<fieldset>
  <legend>개인 정보</legend>

  이름: <input>
  이메일: <input>
</fieldset>
→ 입력 항목을 묶음 (개인정보 입력, 배송 정보 입력, 설문 항목)

<section>
  <h2>경력</h2>
  <p>2024~2026 회사 근무</p>
</section>
->콘텐츠 영역을 나눔 (자기소개, 경력, 프로젝트, 취미)

내가 정보를 보여주는 영역 → <section>
사용자가 정보를 입력하는 영역 → <fieldset>
으로 만나는 경우가 많음

* table tr / th / td
<table border="1">
  <tr>
    <th>이름</th>
    <th>나이</th>
  </tr>
  <tr>
    <td>홍길동</td>
    <td>20</td>
  </tr>
</table>
ㄴ 좌측에도 헤드를 넣는 방법 ->> 좌측에 헤더(행 제목)를 넣고 싶다면 <th>를 첫 번째 열에 사용하면 됩니다. <th>는 보통 위쪽 제목뿐 아니라 왼쪽 제목(행 헤더)으로도 사용할 수 있음
<table border="1">
  <tr>
    <th>항목</th>
    <th>내용</th>
  </tr>
  <tr>
    <th>이름</th>
    <td>홍길동</td>
  </tr>
  <tr>
    <th>나이</th>
    <td>20</td>
  </tr>
</table>

* 선스타일
| 값        | 의미       | 모양      |
| -------- | -------- | ------- |
| `solid`  | 실선       | ━━━━━   |
| `dashed` | 점선(긴 점선) | - - - - |
| `dotted` | 점 형태 점선  | · · · · |
| `double` | 이중선      | ═════   |
| `none`   | 선 없음     |         |

* .question label:has(+ input:checked) {
  color: red;
  font-weight: bold;}
  해석:
.question → class가 question인 영역 안에서
label → label 태그를 찾고
:has() → 조건에 맞으면 선택
+ input → 바로 뒤에 있는 input 태그
:checked → 선택(체크)된 상태라면
"question 안의 label 중에서, 바로 뒤에 체크된 radio(input)가 있는 label을 찾아라."
찾은 label에:
color: red; → 글자 빨간색
font-weight: bold; → 글자 굵게
적용한다는 뜻입니다.

* 전체 페이지를 카드로 만들 때는 margin이 거의 필수에 가까워

* [Bootstrap Grid 예시]
목표: 글 왼쪽 + 사진 오른쪽
코드 구조: <div class="row">
  <div class="col-md-6">
    글
  </div>

  <div class="col-md-6">
    사진
  </div>
</div>
결과:

|     글     |     사진     |

화면 작아지면:

|    글    |
|    사진  |

* 강제로 띄어쓰기 1칸 : &nbsp;