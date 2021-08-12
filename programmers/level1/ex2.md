# 직사각형 별찍기

[프로그래머스 문제로 가기](https://programmers.co.kr/learn/courses/30/lessons/12969)

## 문제 설명

이 문제에는 표준 입력으로 두 개의 정수 n과 m이 주어집니다.  
 별(\*) 문자를 이용해 가로의 길이가 n, 세로의 길이가 m인 직사각형 형태를 출력해보세요.

### 제한 조건

n과 m은 각각 1000 이하인 자연수입니다.

### 예시입력

5 3

### 출력

```
*****
*****
*****
```

## solution

for를 사용해서 반복하며 2차원 배열에 접근하여 \* 과 ""을 넣어준다

```
process.stdin.setEncoding('utf8')
process.stdin.on('data', (data) => {
  const n = data.split(' ')
  const a = Number(n[0]),
    b = Number(n[1])

  let star = ''
  for (let i = 0; i < b; i++) {
    for (let j = 0; j < a; j++) {
      star += '*'
    }
    star += '\n'
  }
  console.log(star)
})
```
