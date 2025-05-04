#  CSS 선택자 & 배경 스타일 정리

##  선택자

###  하위 선택자 (공백)
```css
부모요소 자식요소 { ... }
```
- 부모 요소에 포함된 **모든 하위 요소**를 선택

---

###  자식 선택자 (`>`)
```css
부모요소 > 자식요소 { ... }
```
- **직계 자식**만 선택 (자손 X)

---

###  인접 형제 선택자 (`+`)
```css
요소1 + 요소2 { ... }
```
- 요소1 **바로 다음에 오는 형제 요소** 선택  
예:  
```css
h1 + p { ... }
```

---

###  일반 형제 선택자 (`~`)
```css
요소1 ~ 요소2 { ... }
```
- 요소1 뒤에 나오는 **모든 형제 요소2**를 선택

---

##  HTML 엔티티 코드

| 문자 | 코드  |
|------|--------|
| `<`  | `&lt;` |
| `>`  | `&gt;` |

> 기호를 직접 쓰면 HTML 해석 오류 발생 가능 → 엔티티 코드 사용

---

##  gnb에 padding 주의

- `gnb`에 `padding`을 주면 서브 메뉴가 닫힐 수 있음  
- `hover` 시 마우스가 영역 벗어나면서 **서브 메뉴가 닫히는 현상** 발생 가능

---

##  배경 스타일 (Background)

###  기본 배경 이미지
```css
background-image: url(../images/book-icon.png);
```
- 기본: 배경 전체에 반복됨
- 배경은 `border` 안쪽에 생김 → `padding`으로 밀리지 않음

---

###  반복 설정

| 속성 | 설명 |
|------|------|
| `background-repeat: no-repeat;` | 반복 안 함 |
| `repeat-x` | 가로 방향 반복 |
| `repeat-y` | 세로 방향 반복 |

---

###  위치 설정

```css
background-position: left center;
/* 또는 background-position: 50% 50%; */
```
- 하나만 지정 시 → 가로만 지정됨

---

###  고정 / 스크롤

```css
background-attachment: fixed; /* 고정 */
```

---

##  `background-origin`

| 값 | 설명 |
|-----|------|
| `padding-box` | (기본값) 패딩까지 포함 |
| `border-box` | 테두리까지 포함 |
| `content-box` | 내용만 포함 |

---

##  `background-size`

| 값 | 설명 |
|------|------|
| `auto` | 원본 이미지 크기 |
| `100%` | 너비 100% |
| `100% 100%` | 가로세로 100% |
| `contain` | 요소에 비율 유지하며 맞춤 (남는 공간 생김) |
| `cover` | 요소를 덮되 이미지 잘릴 수 있음 (비율 유지) |

---

##  `background-clip`

| 값 | 설명 |
|-----|--------|
| `border-box` | 테두리까지 (기본값) |
| `padding-box` | 패딩까지 |
| `content-box` | 콘텐츠만 |

---

##  한 줄로 쓰기 (주의)

```css
background: url('../images/bg4.jpg') no-repeat left top;
```

- `background-position`과 `background-size`를 같이 쓸 땐 `/`로 구분

```css
background: url(bg.jpg) no-repeat center/cover;
```

---

##  linear-gradient (그라데이션)

###  방향 설정

```css
background: linear-gradient(to right bottom, blue, white);
```

- `to 방향` or `각도`

###  각도 설정

```css
background: linear-gradient(45deg, #f00, #fff);
```

###  색상 중지점 설정

```css
background: linear-gradient(to bottom, red, white 30%, blue);
```

- 여러 중지점 지정하여 **색상 전환 범위 조절** 가능

```css
background: linear-gradient(to bottom, red, white 30%, white 70%, blue);
```

---

