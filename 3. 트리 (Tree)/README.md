## 트리 (Tree)
- 노드들이 나무 가지처럼 연결된 비선형 계층적 자료구조입니다.

![](https://images.velog.io/images/wjddk97/post/6684351a-b79b-4cb4-aeb0-7736e3991424/image.png)

![](https://images.velog.io/images/wjddk97/post/7bb7d9d2-3a00-4c2c-9cd6-56b219bdc5df/image.png)

---

### 1. 순서 트리와 무순서 트리
- 형제 노드의 순서 관계가 있으면 순서 트리
- 구별하지 않으면 무순서 트리
<br>

### 2. 순서 트리의 검색 
순서 트리의 노드를 스캔하는 방법은 크게 2가지이다.

**너비 우선 검색** : 낮은 레벨부터 **왼쪽에서 오른쪽으로 검색**하고, 한 레벨에서 검색을 마치면 **다음 레벨로 내려가는 방법**, <br>
즉 맨 위에서부터 왼쪽에서 오른쪽, 왼쪽에서 오른쪽으로 검색하는법

![](https://images.velog.io/images/wjddk97/post/7f3406ad-a602-4204-a656-f872a117b2fc/image.png)
<br>
<br>

**깊이 우선 검색** : **리프에 도달할 때까지 아래쪽으로 내려가면서 검색**하는 것을 우선으로 하는 방법, <br>
리프에 도달해서 **더 이상 검색할 곳이 없으면 일단 부모 노드로 돌아가고 그 뒤 다시 자식 노드로 내려간다.**

![](https://images.velog.io/images/wjddk97/post/fa3b06a8-a04f-4964-9777-23c03f622204/image.png)

**전위순회** : 노드 방문 -> 왼쪽 자식 -> 오른쪽 자식 <br>
**중위순회** : 왼쪽 자식 -> 노드 방문 -> 오른쪽 자식 <br>
**후위순회** : 왼쪽 자식 -> 오른쪽 자식 -> 노드 방문 <br>
![](https://images.velog.io/images/wjddk97/post/4fdfec01-0427-4a0d-b276-0fd1e3076e39/image.png)
<br>

### 3. 이진 트리
- 노드가 왼쪽 자식과 오른쪽 자식을 갖는 트리
- 왼쪽과 오른쪽 자식을 구분한다.
- 각 노드의 자식은 2명 이하

![](https://images.velog.io/images/wjddk97/post/dbdccf9c-b554-4ba2-9165-90fd1d22798a/image.png)

### 4. 완전 이진 트리
- 루트부터 노드가 채워져 있으면서 같은 레벨에서는 왼쪽에서 오른쪽으로 노드가 채워져 있는 이진트리

![](https://images.velog.io/images/wjddk97/post/8cece59c-a361-4d03-aee9-e1181f52c362/image.png)

### 5. 이진 검색 트리
- 왼쪽 서브트리 노드의 키값은 자신의 노드 키값보다 작아야 한다.
- 오른쪽 서브트리 노드의 키값은 자신의 노드 키값보다 커야 한다.

![](https://images.velog.io/images/wjddk97/post/9123ed8b-83b7-45b3-a8ea-1eec869b7fdb/image.png)

**중위 순휘**의 깊이 우선 검색으로 스캔하면 키값을 오름차순으로 얻을 수 있다.
1 - 4 - 5 - 6 - 7 - 9 - 11 - 12 - 13 - 14 - 15 - 18
