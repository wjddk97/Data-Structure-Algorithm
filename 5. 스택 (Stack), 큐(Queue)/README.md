# 1. 스택 (Stack)
- **가장 나중에 들어온 자료가 가장 먼저 처리되는** LIFO(Last-In-First-Out) 후입선출 자료구조
- 데이터를 넣는 작업을 **push**라고 하며,
- 데이터를 꺼내는 작업은 **pop**이라고 한다. 

![](https://images.velog.io/images/wjddk97/post/10fe14b5-2963-446e-b365-e0e51fdd7214/image.png)<br>
이미지 출처 : https://ooeunz.tistory.com/7 
<br>

**활용 ex)**
- 웹 브라우저 방문기록 (뒤로 가기) : 가장 나중에 열린 페이지부터 다시 보여준다.
- 실행 취소 : 가장 나중에 실행된 것부터 실행을 취소한다.

<br>

## Python으로 스택 구현
```py
# push
li = [1, 2, 3, 4]
li.append(5)
print(li)
>>> [1, 2, 3, 4, 5]

#pop
pop = li.pop()
print(pop)
>>> 5

print(li)
>>> [1, 2, 3, 4]
```
<br>

------

# 2. 큐 (Queue)

- **먼저 들어온 데이터가 먼저 처리되는** FIFO(First-In First-Out) 선입선출 자료구조
<br>

**활용 ex)** 
- 은행 업무 대기 
- 콜센터 고객 대기 

![](https://images.velog.io/images/wjddk97/post/68bef825-7f4d-4859-b2db-930e3ca6efab/image.png) <br>
이미지 출처 :  https://ooeunz.tistory.com/31 
<br>

- **삽입(Enqueue)** 이 일어나는 곳을 **Rear** 라고 하며 
- **삭제(Dequeue)** 가 일어나는 곳을 **Front** 라고 한다.

![](https://images.velog.io/images/wjddk97/post/4d45ff60-f6c1-4828-94fe-41d734cde9a0/image.png) <br>
이미지 출처 : https://minosaekki.tistory.com/11
<br>


- **인큐**는 **rear**의 자리에 새로운 데이터를 저장하기만 하면 되기 때문에 이 처리의 시간복잡도는 O(1)이다.


- 하지만 **디큐**는 데이터를 꺼낸 후 **그 뒤의 요소들이 앞으로 옮겨가야한다.** 
- 따라서 복잡도는 O(N)이며, 
- 데이터를 꺼낼때마다 이런 처리를 하게 되면 효율이 떨어진다.
<br>

# 3. 링 버퍼 (Ring Buffer)

- **배열 요소를 앞쪽으로 옮기지 않는 큐**를 구현한 자료 구조


- **프런트(front)**: 맨 처음 요소의 인덱스(데이터를 디큐할 위치)
- **리어(rear)**: 맨 끝 요소의 하나 뒤의 인덱스(다음 요소를 인큐할 위치를 미리 지정)

![](https://images.velog.io/images/wjddk97/post/82fe8cbd-1f32-4aa9-9fde-2dceff36c8c8/image.png) <br>
이미지 출처 : https://sustainable-dev.tistory.com/35
<br>

위의 그림에서는 **front = 0**,  **rear = 5**이다.
<br>

**디큐할 경우** 
- 36(que[0])을 디큐한 후 front값을 que[1]로 업데이트해준다. 
<br>

**인큐할 경우**
- que[5]의 자리에 64를 저장한다. 
- rear값을 que[0]으로 업데이트해준다.

<br>

이렇게 큐를 구현하면 프런트와 리어 값을 업데이트하면서 <br>
인큐와 디큐를 수행하기 때문에 **앞의 큐에서 발생했던 요소 이동 문제를 해결**할 수 있다. <br>
물론 처리의 복잡도는 O(1)이다.