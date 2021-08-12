# 평균 구하기

## 문제

[프로그래머스 문제로 가기](https://programmers.co.kr/learn/courses/30/lessons/12944)

## solution

1. reduce()
2. map()

```
function solution(arr) {
    const answer = arr.reduce((acc,cur) => acc + cur) / arr.length;
    return answer ;
}
```

```
function solution(arr) {
    let answer = 0;
    arr.map(e => answer += e)
    answer = answer / arr.length;

    return answer ;
}
```
