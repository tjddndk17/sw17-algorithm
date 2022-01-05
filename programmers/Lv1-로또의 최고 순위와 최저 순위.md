# 문제
<a href="https://programmers.co.kr/learn/courses/30/lessons/77484" targer="_blank">로또의 최고 순위와 최저 순위</a>


# 핵심


# 풀이 ( javascript )
```javascript
function solution(lottos, win_nums) {
    const answer = [];
    
    let min = 0;
    let max = lottos.filter(num => {
        if(win_nums.includes(num)) min++;
        return num == 0;
    }).length + min;
    
    answer.push(max > 1 ? 7-max : 6);
    answer.push(min > 1 ? 7-min : 6);
    
    return answer;
}
```


# 풀이 ( java )
```java

```