# 신규 아이디 추천

[프로그래머스 문제로 가기](https://programmers.co.kr/learn/courses/30/lessons/72410)

## solution

toLowerCase()
정규식표현  
slice()  
padEnd()  
repeat()

```
function solution(new_id) {
  const answer = new_id
    .toLowerCase() //1 대문자 => 소문자
    .replace(/[^\w-.]/g, '') //2 문자,숫자,-,. 제외 모두 제거
    .replace(/\.{2,}/g, '.') //3 마침표가 2개이상 중복이면 1개로
    .replace(/^\.|\.$/, '') //4 마침표가 처음이나 끝이면 제거
    .replace(/^$/, 'a') //5 공백이면 a로 대체 // 다시 찾아보기
    .slice(0, 15)
    .replace(/\.$/, '') // 6 길이가 16이상이면 16부터 제거 and 마지막이 .이면 제거

  //return answer.length <= 2 ? answer + answer.slice(-1).repeat(3 - answer.length) : answer; // repaet() 사용
  return answer.length <= 2 ? answer.padEnd(3, answer.slice(-1)) : answer // padEnd 사용
}
```
