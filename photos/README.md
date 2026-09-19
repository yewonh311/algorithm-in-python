# photos

사진은 이제 HTML 안에 base64로 박혀 있지 않고 이 폴더에 파일로 있습니다.
(그래서 `index.html`이 1.4MB → 89KB로 줄었고, 사진 교체가 파일 하나 바꾸는 일이 됐습니다.)

## 지금 쓰이는 사진

| 파일 | 쓰이는 곳 | 권장 비율 |
|---|---|---|
| `portrait-1.jpg` | 히어로(첫 화면) 오른쪽 + About 섹션 | 세로 4:5 (예: 1200×1500) |
| `portrait-2.jpg` | About 섹션에서 5.2초마다 교차 페이드 | 세로 4:5 |

## 바꾸는 법

같은 이름으로 덮어쓰면 끝입니다. HTML은 건드릴 필요 없습니다.

```
photos/portrait-1.jpg   ← 새 사진으로 교체
photos/portrait-2.jpg   ← 새 사진으로 교체
```

## 사진을 더 넣고 싶을 때

About 섹션 슬라이드쇼는 `.photo` 안의 `<img>` 개수만큼 자동으로 돌아갑니다.
`index.html`의 `<div class="photo">` 안에 한 줄 더 추가하면 됩니다.

```html
<div class="photo">
  <img class="on" src="photos/portrait-1.jpg" alt="Yewon Hong">
  <img src="photos/portrait-2.jpg" alt="Yewon Hong">
  <img src="photos/portrait-3.jpg" alt="Yewon Hong">   <!-- 추가 -->
</div>
```

> 첫 번째 `<img>`에만 `class="on"`을 둡니다.

## 톤

사진은 원래 색 그대로 나옵니다. 흑백 필터는 걸지 않았습니다.

## 아직 없는 파일

`resume.pdf` 와 `portfolio.pdf` 는 저장소 루트에 놓으면 상단 CV 버튼과
About 섹션의 다운로드 링크가 바로 동작합니다. (지금은 링크만 있고 파일이 없는 상태)
