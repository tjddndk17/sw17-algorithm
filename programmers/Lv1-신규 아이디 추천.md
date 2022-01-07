# 문제
[신규 아이디 추천](https://programmers.co.kr/learn/courses/30/lessons/72410)

# 핵심
- 정규식 사용할 줄 알아야함

# 풀이 ( javascript )
```javascript
function solution(new_id) {
    let answer = new_id
        .toLowerCase()
        .replace(/[^a-z0-9-_.]/g, '')
        .replace(/\.{2,}/g, '.')
        .replace(/^\.|\.$/g, '')
        .replace(/^$/, 'a')
        .slice(0, 15)
        .replace(/\.$/g, '');

    while(answer.length <= 2){
        answer += answer.charAt(answer.length-1);
    }

    return answer;
}
```
1. 간 조건에 맞는 정규식 작성
2. 마지막 조건은 정규식이 떠오르지 않아 직접작성

# 풀이 ( java )
```java

```