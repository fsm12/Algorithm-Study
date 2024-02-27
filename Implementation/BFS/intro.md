# 너비 우선 탐색 (BFS, Breadth First Search)

</br>

## 개념

### 알고리즘 정의

시작 노드부터 인접한 노드를 먼저 탐색하는 방식

***"인접한 노드들 중 먼저 보는 노드는 코드에 따라 다름"***

<img src="https://github.com/fsm12/Algorithm-Study/assets/74345771/36ba7077-5cb0-4717-87cc-0ceef43bc38e" alt="[그림 1. BFS 탐색 예시]" width=650 hegiht=200 >

</br>
</br>

**시간복잡도 : O(V+E)**

</br>
</br>

## 구현
### 동작방식

<img src="https://github.com/fsm12/Algorithm-Study/assets/74345771/461db3d5-14e4-4414-9e2d-b0a0bd04d60e" alt="[그림 2. 큐로 BFS 탐색 시 변화]" width=700 >

먼저 들어온 노드가 하나씩 나가고 연결된 노드들이 들어오는 형식

</br>

### 1. 큐
#### 큐에 "방문할 곳"을 저장


***코드 설계***
```
큐를 선언하고, 시작노드를 하나 넣는다.
큐에 값이 있는 동안{
	하나를 꺼내서 A라 칭한다.
	A가 목적지이면{
		목적지에 대한 처리를 해주고,
		나간다.
	}
	A와 연결되어 있는 노드들 중에{
		A에서 연결된 노드로 갈 수 있는 노드가 있다면{
			큐에 넣고,
			방문처리를 한다.
		}
	}
}
```

***실제 코드 (Java)***
```java
public static void main(String[] args) {
	
	// 인접리스트 초기화
	adjList = new ArrayList[SIZE];
	for(int n=1; n<SIZE; n++) {
		adjList[n] = new ArrayList<>();
	}
	adjList[1].add(2);
	adjList[1].add(3);
	adjList[2].add(4);
	adjList[2].add(5);
	adjList[3].add(6);
	adjList[3].add(7);

	// 방문"할" 순서를 담는 배열
	visOrder = new ArrayList<>();

	// 노드 방문 처리 배열
	vis = new boolean[SIZE];

	/* ------- MAIN CODE ------- */
	Queue<Integer> q = new LinkedList<>();
	q.add(1);
	visOrder.add(1);
	vis[1] = true;
	
	while(!q.isEmpty()) {
		int cur = q.poll();
		
		for(int next : adjList[cur]) {
			if(!vis[next]) {
				q.add(next);
				visOrder.add(next);
				vis[next] = true;
			}
		}
	}
	
	System.out.println(visOrder.toString());
}
```

</br>
</br>

## 활용
### A. 최단경로
> `BFS`를 구현할 때 보통 `while` 반복을 사용하는데, 해당 반복이 끝날 때 마다 `Queue`에는 같은 depth만큼 이동한 결과값이 저장된다. 
> 
> <img src="https://github.com/fsm12/Algorithm-Study/assets/74345771/2818ddee-8b5e-4a0d-b322-1b14ca14f3ff" alt="[그림 2. while문의 주기]" width=700 >
>
> 이를 이용하면 `if문`하나만으로 현재 좌표를 비교해 목적지라면 탈출할 수 있음

### B. 위상정렬

</br>
</br>

## 해당 알고리즘을 사용해 푸는 문제

| 난이도 | 사이트 | 번호 | 문제이름 | 아이디어 | 회고 |
| ----- | ----- | ----- | ----- | ----- | ----- |
|   |   |   | <div align="center">[]()</div> | | |
|   |   |   |   |   |   |   |
|   |   |   |   |   |   |   |
|   |   |   |   |   |   |   |
