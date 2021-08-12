# 핸드폰 번호 가리기

## 문제

[프로그래머스 문제로 가기](https://programmers.co.kr/learn/courses/30/lessons/12948)

## solution

replace()를 사용하여 뒤의 4자리를 뺸 나머지 숫자는 \* 치환

```
function solution(phone_number) {
    let answer = '';
    const start = phone_number.substr(0,phone_number.length - 4).replace(/[0-9]/gi,"*")
    const last = phone_number.slice(phone_number.length - 4, phone_number.length)
    const result = start + last;
    answer = result
    return answer;
}
```
