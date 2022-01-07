## 1. 연결리스트 (Linked-list)

- 노드와 노드가 연결된 형태
- **데이터와 주소값, 두 요소로 이루어진 묶음 하나를 노드** 라고 부른다.
- 리스트의 **첫번째 노드를 헤드(Head)**,  **마지막 노드를 테일(Tail)** 이라고 합니다.

![](https://images.velog.io/images/wjddk97/post/2ab95c22-4fb0-44a4-94ec-28f82e12c88d/image.png)

---
### 단순 연결 리스트(Singly Linked List)

리스트의 가장 기본적인 형태입니다. <br>
**tail의 포인터 변수가 NULL을 가리키는게 특징**입니다. <br>

![](https://images.velog.io/images/wjddk97/post/0aaaefa9-33af-4486-853f-35fe2bbd6435/image.png)
<br>
<br>

### 원형 단순 연결리스트(Circular Singly Linked List)
단순 연결 리스트(Singly Linked List)의 마지막 노드의 포인터가 <br>
**NULL이 아닌 헤드를 가리키는 형태**의 리스트 입니다. <br>
따라서 리스트의 끝이 존재하지 않습니다.<br>

![](https://images.velog.io/images/wjddk97/post/f0d33fb5-1eae-4619-ac10-8a2bc246b555/image.png)
<br>
<br>

### 이중 연결리스트(Doubly Linked List)
단순 연결 리스트(Singly Linked List)는 next로 <br>
현재 노드에서 다음 노드로 갈 수 있지만 이전 노드로는 갈 수 없습니다. <br>
이러한 단점을 해결하기 위해 노드에 **앞 노드의 메모리 주소를 보관하는 <br>포인터 prev를 만들어준 형태**를 이중 연결 리스트(Doubly Linked List) 입니다.

![](https://images.velog.io/images/wjddk97/post/56491b93-2db3-42f4-8d24-110a9efc3e20/image.png)
<br>
<br>


### 원형 이중 연결 리스트 (Circular Doubly Linked List)
이중 연결 리스트 **헤드의 prev 포인터를 마지막 노드로, <br>
마지막 노드의 next 포인터를 헤드로 지정해준 형태**입니다. <br>
아래와 같은 구성을 통해 최소한의 노드를 거치며 <br>
기존의 연결 리스트 보다 조금 더 효율적으로 노드를 추가/제거 할 수 있습니다.

![](https://images.velog.io/images/wjddk97/post/befbc778-801c-4005-bb25-58424bfdb9a4/image.png)
<br>

## 2.배열과 연결리스트 차이 

![](https://images.velog.io/images/wjddk97/post/5399146f-a516-45ef-83e6-717f3a3112f1/image.png)