# 문제
[로또의 최고 순위와 최저 순위](https://programmers.co.kr/learn/courses/30/lessons/77484)

# 핵심
- 로또의 최고순위: 알수없는 번수가 다 맞았을때 ( 당첨번호 개수 + 알수없는번호 개수 )
- 로또의 최저순위: 알수없는 번호가 다 틀렸을때 ( 당첨번호 개수 )
- 순위 구하는 식: `(7 - 번호 일치 개수)` + `일치 개수 1개 이하는 6위`

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
1. 구매번호에서 당첨번호가 몇개인지, 알수없는번호가 몇개인지 찾아야함
2. filter로 루프를 돌면서 해당번호가 당첨인지 `win_nums.includes(num)`, 알수없는 번호인지 `num == 0` 판단 
3. 순위 구하는 식대로 push

# 풀이 ( java )
```java

```
