# 모의고사

[프로그래머스 문제로 가기](https://programmers.co.kr/learn/courses/30/lessons/42840)

## solution
  filter(),Math.max()
```
function solution(answers) {
    const answer = [];
    const arr0 = [ 1, 2, 3, 4, 5];
    const arr1 =  [2, 1, 2, 3, 2, 4, 2, 5];
    const arr2 = [ 3, 3, 1, 1, 2, 2, 4, 4, 5, 5];
    const score = [[0] ,[0] ,[0]];
     
    score[0] = answers.filter((num,index) => num === arr0[index % arr0.length]).length
    score[1] = answers.filter((num,index) => num === arr1[index % arr1.length]).length
    score[2] = answers.filter((num,index) => num === arr2[index % arr2.length]).length
    const result = score.flatMap(e => e)
    const max = Math.max(result)
    for(let index in result){
        result[index] === max && answer.push(parseInt(index)+1)
    }
                    
    return answer;
}
```