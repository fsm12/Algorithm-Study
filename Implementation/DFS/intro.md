# 깊이 우선 탐색 (DFS, Depth First Search)

</br>

## 개념

### 알고리즘 정의

최대한 깊숙하게 들어가서 확인 후 다시 돌아가 다른 경로로 탐색하는 방식

***"갈 수 있는 노드가 없을 때까지 탐색"***

<img src="https://github.com/fsm12/Algorithm-Study/assets/74345771/80563ce0-2142-4496-af5e-fe179b498ca9" alt="[그림 1. DFS 탐색 예시]" width=650 hegiht=200 >

</br>
</br>

**시간복잡도 : O(V+E)**

</br>
</br>

## 구현
### 동작방식

<img src="https://github.com/fsm12/Algorithm-Study/assets/74345771/07fcf44b-75e0-4f79-b386-a235e9a3e2a4" alt="[그림 2. 스택으로 DFS 탐색 시 변화]" width=1000 >

재귀 또한 함수호출시 쌓이고, 리턴시 삭제되는 스택의 형태를 가짐

so) `DFS`를 구현할 때 한정된 `Limit` 이상으로 쌓으면 `Stack Overflow`가 발생할 수 있으므로 주의해야 함 (보통은 무한루프)

</br>

### 1. 스택
#### 스택에 "방문한 곳"을 저장


***코드 설계***
```
스택에 (노드를 특정하는)값이 있을 때 {
	가장 마지막에 들어온 값을 A에 담는다.
	A 노드에서 연결된 B 노드가 있고 B 노드에 방문하지 않았다면 {
			방문 순서에 추가하고,
			방문했음을 체크한다.
		}
	}
	
	만약 방문하지 않은 노드가 없었다면{
		리프노드이므로 마지막에 들어온 값을 빼고 다음 값을 본다.
	}
}
```


***실제 코드 (Java)***
```java
/* 클래스 및 변수 선언 생략 */

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

	// 방문"한" 순서를 담는 배열
	visOrder = new ArrayList<>();

	// 스택 선언
	stack = new int[SIZE];
	stack[p++] = 1;
	visOrder.add(1);

	// 노드 방문 처리 배열
	vis = new boolean[SIZE];

	/* ------- MAIN CODE ------- */
	while(p!=0) {
		boolean flag = false;
		int cur = stack[p-1];
		
		for(int next : adjList[cur]) {
			if(!vis[next]) {
				stack[p++] = next;
				visOrder.add(next);
				vis[next] = true;
				
				flag = true;
				break;
			}
		}
		if(!flag)
			p--;
	}
	System.out.println(visOrder.toString());
}
```

</br>


### 2. 재귀
#### 재귀 호출의 한 depth는 방문한 노드 

***코드 설계***
```
dfs 메서드를 A라는 노드값으로 호출했다면 {
	A를 방문순서에 추가한다.
	A 노드에서 연결된 B 노드가 있고, B 노드에 방문하지 않았다면 {
			방문했음을 체크하고
			dfs 메서드를 B 노드 값으로 호출한다.
			A에서 연결된 다음 노드들도 깊숙하게 들어가야하므로 이번 분기의 방문체크를 해제한다.
		}
	}
}
```

***실제 코드 (Java)***
```java
/* 클래스 및 변수 선언 생략 */


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
	
	// 방문"한" 순서를 담는 배열
	visOrder = new ArrayList<>();

	// 노드 방문 처리 배열
	vis = new boolean[SIZE];
	
	dfs(1);
	
	System.out.println(visOrder);
}

/* ------- MAIN CODE ------- */
public static void dfs(int cur) {	
	visOrder.add(cur);	
	for(int next : adjList[cur]) {
		if(!vis[next]) {
			vis[next] = true;
			dfs(next);
			vis[next] = false;
		}
	}
}
```

</br>

=> 일반적으로 재귀함수를 이용해 구현하지만, 개발자 선호도에 따라 스택을 이용하는 여러 방식으로 구현해도 됨
완탐이기 때문에 모든 노드 및 간선을 보므로 시간복잡도 차이는 미미

</br>
</br>

## 활용
### A. 백트래킹
> 보통 `if문`으로 끝까지 보지 않고 나올 때 `DFS`를 사용함

### B. 단절선 찾기
### C. 위상정렬
### D. 사이클 찾기

</br>
</br>

## 해당 알고리즘을 사용해 푸는 문제

| 난이도 | 사이트 | 번호 | 문제이름 | 아이디어 | 회고 |
| ----- | ----- | ----- | ----- | ----- | ----- |
|   |   |   | <div align="center">[]()</div> | | |
|   |   |   |   |   |   |   |
|   |   |   |   |   |   |   |
|   |   |   |   |   |   |   |
