# 7. 이벤트란?

- 웹 페이지에서 발생하는 사건을 의미
- 이벤트를 처리하는 함수를 event handler 또는 event listner

## 7.1 이벤트 핸들러

- 마우스 클릭이나 이동
- 페이지 로드
- 이미지 로드
- 입력창에 데이터 입력
- 키보드 누르기 등

```html
<body>
  <button onclick="changeText(this)">클릭하세요!</button>

  <script>
    const changeText = (elem) => {
      elem.innerHTML = "OK!";
    };
  </script>
</body>
```

## 7.2 이벤트 리스너

```html
<body>
  <button id="btn">클릭하세요!</button>
  <p id="show"></p>

  <script>
    let text = "";

    const btn = document.getElementById("btn");
    btn.addEventListener("click", () => {
      text += `안녕하세요!<br>`;
      document.getElementById("show").innerHTML = text;
    });

    btn.addEventListener("click", () => {
      text += `반갑습니다!<br>`;
      document.getElementById("show").innerHTML = text;
    });
  </script>
</body>
```
