# ✨ Lottery Machine
https://user-images.githubusercontent.com/114633506/212263253-ce7f1ccf-996e-4e82-a1c1-c8ed6696848a.mp4

<br>

## 🍯 About
- **작업기간** : 2022.11.29 - 2022.11.30  
- **참여도** : 100%  
- **기술** : 바닐라 자바스크립트  

<br>

## 🌹 기능
- 로또 발행일, 추첨일, 지급기한일을 알 수 있습니다.
- 시작 버튼을 누르면 5개의 로또 번호가 생성됩니다.

### 업데이트
- 2023/01/13 : 시작 버튼 누를 시 텍스트가 흔들리는 현상 수정👍 (*영상은 수정 이전 버전*)

### 주요 코드
<details>
<summary>로또번호 생성</summary>  
  
```c
$startBtn.addEventListener("click", () => {
  for(let i = 0; i < 5; i++) {
      ball[i].innerHTML = generate();
  }
});
    
function generate() {
  let answer = [];

  for (let i = 0; i < 6; i++){
      let check = false;
      while (check == false){
          let randNum = Math.floor(Math.random() * 45) + 1;
          if (answer.includes(randNum) == false){
              answer.push(randNum);
              check = true;
          }
      }
  }

  answer.sort(function(a, b){
      return a - b;
  });

  return answer.join(', ');
} // generate

```

</details>

<br>

## 💬 느낀점
단순히 로또번호 6자리를 한 개 생성하는 건 쉬운데, 다섯 개의 로또번호를 생성하는 방법이 어려웠다. 
계속 헤매다가 이래도는 안되겠다 싶어서, 처음부터 다시 만든다는 마음가짐으로 HTML 구조를 바꾸고 코드를 짜니 정말 금방 해결됐다. 
역시 해도해도 안되면 구조가 문제라는 걸 다시 한번 느꼈다.



