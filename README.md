# <div align="center">Algorithm-Study</div>
### <div align="center">PS에 자주 활용되는 알고리즘의 스니펫과 활용법을 정리한 레포</div>

</br></br></br>

## 📦 레퍼런스 공유

<details>
<summary>⚙️ 백준 풀기 전 환경 설정</summary>
<div markdown="1">

---

- [BOJ Extended](https://chromewebstore.google.com/detail/boj-extended/mfcaadoifdifdnigjmfbekjbhehibfel?hl=ko) &nbsp; &nbsp; &nbsp; : 타이머 기능 추가; 문제 풀 때 질문게시판 옆에 메뉴가 생김 + 테마 설정 등 가능 

- [백준허브(BaekjoonHub)](https://chromewebstore.google.com/detail/백준허브baekjoonhub/ccammcjdkpgjmcpijpahlehmapgmphmk?hl=ko) &nbsp; &nbsp; &nbsp;  : 문제 풀고 “맞았습니다”가 뜰 때 자동으로 Github에 push해줌

- [보기 설정](https://www.acmicpc.net/modify) &nbsp; &nbsp; &nbsp; : 3번째 그룹에서 "보기" -> "solved.ac 티어", "solved.ac 티어 이름", "알고리즘 분류", "런타임 에러 이유" 모두 "보지 않기"   
![보기 설정](https://github.com/fsm12/Algorithm-Study/assets/74345771/f5510c38-1890-41e1-b1f6-539175c6a604)

- 연습 소스 코드 공개 설정 &nbsp; &nbsp; &nbsp; : 가입한 그룹 -> 설정 -> 연습 소스 코드 공개 -> 모든 멤버에게 공개
![연습 소스 코드 공개 설정](https://github.com/fsm12/Algorithm-Study/assets/74345771/d9ee5260-0234-49fd-8102-fabca36c3255)

---

</div>
</details>

<details>
<summary>💻 코딩테스트 유형</summary>
<div markdown="1">

---

- 구현 (완전탐색) ⭐⭐
- 백트래킹 ⭐⭐⭐
- 정렬 (기본정렬, 투포인터, 이분탐색)
- 자료구조 (스택, 큐, 힙, 트리, 그래프) ⭐
- 트리 (이진트리, 인덱스트리, 트라이) ⭐
- 그래프 (집합연산, 위상정렬, MST, LCA, 단절점, 최단경로) ⭐⭐
- 정수론 (유클리드호제법)
- 조합론 (순열, 조합) ⭐
- DP ⭐⭐

---

</div>
</details>

<details>
<summary>🔎 학습을 위한 단계별 자료 추천</summary>
<div markdown="1">
  
---

### 1. 알고리즘 유형 숙지 X

- 알고리즘 유형별 개념 설명 및 관련 문제 풀기 좋음
- [BaaaaaaaarkingDog - 실전 알고리즘 강좌](https://blog.encrypted.gg/919)

</br>

### 2. 알고리즘 유형 숙지 O, 유형별 문제 연습 X

- ReadMe표를 보고 유형을 알고있는 채로 문제풀기 좋음
- [tony9402 - 코딩테스트 대비 문제집](https://github.com/tony9402/baekjoon)

</br>

### 3. 알고리즘 유형 숙지 O, 유형별 문제 연습 O, 무작위 문제 연습 X

- [tony9402 - 오늘의 문제](https://github.com/tony9402/baekjoon/blob/main/picked.md)
- 프로그래머스 : [카카오](https://school.programmers.co.kr/learn/challenges?order=acceptance_desc&page=1&languages=java&partIds=58464%2C37527%2C31236%2C25448%2C20069%2C17214%2C12286%2C9317%2C22586%2C18498%2C17931%2C300%2C301&levels=2%2C3%2C4%2C5)
- 백준 : [삼성](https://www.acmicpc.net/workbook/view/1152)
- Etc : [\[토스 NEXT\] 2022년 코딩테스트 기출문제](https://toss.im/career/article/next-developer-2023-sample-questions)

</br>

#### +) 어려운 문제 위주 빠른 성장 목표

- 브 : 하루 5문제, 실 : 하루 3문제, 골 : 하루 2문제, 플 : 하루 1문제 목표로 처음부터 풀어보자
- [solved.ac - 문제 › CLASS](https://solved.ac/class)

</br>

#### +) 난 영어로 PS 해보고 싶다!

- [USACO Guide](https://usaco.guide/)
- [Main Page - Algorithms for Competitive Programming](https://cp-algorithms.com/)
  
---

</div>
</details>

<details>
<summary>💡 문제 풀이 접근 노하우</summary>
<div markdown="1">
  
---

- 아직 PS가 어렵다고 느낀다면 아래 방법 **그대로 따라해보자**
- 아래 방법이 익숙해진다면 다 쓰지 않고도 풀 수 있는 문제가 늘어남
- 단, 아래 방법을 따라해도 모르는게 많다면 문제의 알고리즘 유형을 보고 공부한 뒤 다시 접근해보자

   (개념이 부족하거나 개념에만 머물러 있어 적용이 힘들어서 그런 것)
- ***바로 풀이가 생각난다고 컴퓨터 언어(Java, C…)로 작성하는 건 멀리해야함!!***

</br>

``` markdown
## [목차]
1. 문제를 읽고 이해하기
2. 문제를 익숙한 용어로 재정의와 추상화
3. 문제를 어떻게 해결할 것인가
4. 위 계획을 검증
5. 계획 수행 (실제코드 작성)
+) 셀프 피드백
```

</br>

### 1. 문제를 읽고 이해하기

- 어떤 값이 **입력**이고 **범위가 어떤지**, 그리고 **무엇을 출력해야하는지**를 먼저 보고 이해하기
- 우리는 문제에서 준 요구사항으로 문제를 풀기 위함이지 심화시킬 이유가 없음 → ***입출력값으로만 가지고 놀아야함***

</br>

### 2. 문제를 익숙한 용어로 재정의와 추상화

- 흐름을 그림으로 그려보거나 나만의 말로 풀어보는 등 **긴 문제를 한번에 이해할 수 있게 요약**하기
- 이 과정을 제대로 하지 않으면 직접 코드로 다 구현했을 때 조건을 놓쳐 **맞왜틀**을 시전할 가능성이 높음

</br>

### 3. 문제를 어떻게 해결할 것인가

- 문제를 보고 생각나는 솔루션을 **넘버링으로 나열**해보기
- 솔루션이 생각나지 않는다면 **완탐부터** 생각해보고 **어떻게 효율적으로 관리할 수 있을지**를 생각하기
- 각 솔루션은 **직접 한글로 "의사코드"를 작성**해보고 흐름을 이해하기

</br>

### 4. 위 계획을 검증

- 입력값의 **범위와 시간/메모리 제한**을 보고 그 안에 실행이 될 건지 확인하기
- 엣지케이스(보통은 입력의 양 끝값)을 넣어보고 괜찮은지 검증해보기

</br>

### 5. 계획 수행 (실제코드 작성)

- 3 <-> 4 를 반복하고 실행이 될 것 같은 코드라면 "의사코드"를 "Java"로 **그대로 치환**하기
- 코드를 작성하고 제출시 결과에 따라 다시 3<->4를 반복하면 됨

</br>

### +) 셀프 피드백

- 문제 풀때 걸린 시간, 아쉽다고 느낀점, 잘한점 을 간략하게라도 회고로 남기는게 좋음
- 나중에 같은 문제를 풀어봤을 때 실력향상을 가장 체감할 수 있음

---

</div>
</details>

</br></br>

## 📋 컨벤션
***커밋***
``` markdown
커밋컨벤션[#이슈번호]: 상세내용(영어)
```

|타입|설명|
|-------|--------|
|<div align="center">**add**</div>|새로운 파일 등 추가|
|<div align="center">**feat**</div>|새로운 기능 추가 -> 후에 웹사이트 구축 시 이용| 
|<div align="center">**fix**</div>|버그 수정|
|<div align="center">**docs**</div>|문서 수정|
|<div align="center">**refactor**</div>|코드 리팩토링|
|<div align="center">**remove**</div>|사용하지 않는 파일 또는 폴더 삭제|
|<div align="center">**rename**</div>|파일 또는 폴더명 수정|
|<div align="center">**move**</div>|폴더 및 파일 이동|

</br>

***예시***
``` markdown
feat[#1] : set overall file structure and create README file
feat[#2] : add topological sort with image
```

</br></br>

## 📌 목차 바로가기

### 🛠︎ Algorithm-Study   
├─ 📁 [들어가기 (Intro)](https://github.com/fsm12/Algorithm-Study/tree/main/Intro)         
│ &nbsp;  &nbsp;  &nbsp; ├─ 📁 복잡도 (Complexity)         
│ &nbsp;  &nbsp;  &nbsp; │ &nbsp;  &nbsp;  &nbsp; └─ 📄 시간-공간 복잡도 분석 방법.md (Time-Space Complexity Analysis Method)         
│ &nbsp;  &nbsp;  &nbsp; └─ 📁 파일 입출력 (File IO)         
├─ 📁 [자료 구조 (Data Structure)](https://github.com/fsm12/Algorithm-Study/tree/main/Data%20Structure)         
│ &nbsp;  &nbsp;  &nbsp; ├─ 📁 배열 (Array)         
│ &nbsp;  &nbsp;  &nbsp; ├─ 📁 리스트 (List)         
│ &nbsp;  &nbsp;  &nbsp; ├─ 📁 연결 리스트 (LinkedList)         
│ &nbsp;  &nbsp;  &nbsp; ├─ 📁 맵 (Map)         
│ &nbsp;  &nbsp;  &nbsp; ├─ 📁 셋 (Set)         
│ &nbsp;  &nbsp;  &nbsp; ├─ 📁 스택 (Stack)         
│ &nbsp;  &nbsp;  &nbsp; ├─ 📁 큐 (Queue)         
│ &nbsp;  &nbsp;  &nbsp; ├─ 📁 덱 (Deque)         
│ &nbsp;  &nbsp;  &nbsp; └─ 📁 트리 (Tree)         
├─ 📁 [조합-순열 (Combination-Permutation)](https://github.com/fsm12/Algorithm-Study/tree/main/Combination-Permutation)         
│ &nbsp;  &nbsp;  &nbsp; ├─ 📁 조합 (Combination)         
│ &nbsp;  &nbsp;  &nbsp; ├─ 📁 중복 조합 (Combination with Repetition)         
│ &nbsp;  &nbsp;  &nbsp; ├─ 📁 순열 (Permutation)         
│ &nbsp;  &nbsp;  &nbsp; └─ 📁 중복 순열 (Permutation with Repetition)         
├─ 📁 [구현 (Implementation)](https://github.com/fsm12/Algorithm-Study/tree/main/Implementation)         
│ &nbsp;  &nbsp;  &nbsp; ├─ 📁 DFS (Depth First Search)         
│ &nbsp;  &nbsp;  &nbsp; ├─ 📁 BFS (Breadth First Search)
│ &nbsp;  &nbsp;  &nbsp; ├─ 📁 브루트 포스 (Brute Force)         
│ &nbsp;  &nbsp;  &nbsp; └─ 📁 백트래킹 (Backtracking)         
├─ 📁 [알고리즘 (Algorithm)](https://github.com/fsm12/Algorithm-Study/tree/main/Algorithm)         
│ &nbsp;  &nbsp;  &nbsp; ├─ 📁 이분 탐색 (Binary Search)         
│ &nbsp;  &nbsp;  &nbsp; ├─ 📁 투 포인터 (Two Pointer)         
│ &nbsp;  &nbsp;  &nbsp; ├─ 📁 탐욕 알고리즘 (Greedy)         
│ &nbsp;  &nbsp;  &nbsp; ├─ 📁 [재귀 (Recursion)](https://github.com/fsm12/Algorithm-Study/tree/main/Algorithm/Recursion)         
│ &nbsp;  &nbsp;  &nbsp; │ &nbsp;  &nbsp;  &nbsp; ├─ 📄 재귀 함수 작성 방법.md (Writing Recursive Function)         
│ &nbsp;  &nbsp;  &nbsp; │ &nbsp;  &nbsp;  &nbsp; ├─ 📁 정렬 (Sorting)         
│ &nbsp;  &nbsp;  &nbsp; │ &nbsp;  &nbsp;  &nbsp; └─ 📁 분할 정복 (Divide and Conquer)         
│ &nbsp;  &nbsp;  &nbsp; ├─ 📁 [문자열 (String)](https://github.com/fsm12/Algorithm-Study/tree/main/Algorithm/String)         
│ &nbsp;  &nbsp;  &nbsp; │ &nbsp;  &nbsp;  &nbsp; ├─ 📁 문자열 검색 알고리즘 (KMP)         
│ &nbsp;  &nbsp;  &nbsp; │ &nbsp;  &nbsp;  &nbsp; └─ 📁 트라이 (Trie)         
│ &nbsp;  &nbsp;  &nbsp; └─ 📁 유니온-파인드 (Union-Find)         
├─ 📁 [그래프 (Graph)](https://github.com/fsm12/Algorithm-Study/tree/main/Graph)         
│ &nbsp;  &nbsp;  &nbsp; ├─ 📁 그래프 표현 방법 (Graph-Representation)         
│ &nbsp;  &nbsp;  &nbsp; ├─ 📁 [최소신장트리 (MST)](https://github.com/fsm12/Algorithm-Study/tree/main/Graph)         
│ &nbsp;  &nbsp;  &nbsp; │ &nbsp;  &nbsp;  &nbsp; ├─ 📁 크루스칼 (Kruskal)         
│ &nbsp;  &nbsp;  &nbsp; │ &nbsp;  &nbsp;  &nbsp; └─ 📁 프림 (Prim)         
│ &nbsp;  &nbsp;  &nbsp; ├─ 📁 [최단경로 (Shortest Path)](https://github.com/fsm12/Algorithm-Study/tree/main/Graph)         
│ &nbsp;  &nbsp;  &nbsp; │ &nbsp;  &nbsp;  &nbsp; ├─ 📁 다익스트라 (Dijkstra)         
│ &nbsp;  &nbsp;  &nbsp; │ &nbsp;  &nbsp;  &nbsp; ├─ 📁 벨만-포드 (Bellman Ford)         
│ &nbsp;  &nbsp;  &nbsp; │ &nbsp;  &nbsp;  &nbsp; └─ 📁 플로이드-워셜 (Floyd Warshall)         
│ &nbsp;  &nbsp;  &nbsp; ├─ 📁 단절점 (Articulation Points)         
│ &nbsp;  &nbsp;  &nbsp; ├─ 📁 위상 정렬 (Topological sort)         
│ &nbsp;  &nbsp;  &nbsp; └─ 📁 최소 공통 조상 (Lowest Common Ancestor)         
├─ 📁 [정수론 (Number Theory)](https://github.com/fsm12/Algorithm-Study/tree/main/Number%20Theory)         
│ &nbsp;  &nbsp;  &nbsp; ├─ 📁 소수 (Prime Number)         
│ &nbsp;  &nbsp;  &nbsp; └─ 📁 기하학 (Geometry)         
│ &nbsp;  &nbsp;  &nbsp; │ &nbsp;  &nbsp;  &nbsp; └─ 📁 유클리드호제법 (Euclidean Algorithm)         
├─ 📁 [동적 계획법 (Dynamic Programming)](https://github.com/fsm12/Algorithm-Study/tree/main/Dynamic%20Programming)         
│ &nbsp;  &nbsp;  &nbsp; ├─ 📁 누적합 (Prefix Sum)         
│ &nbsp;  &nbsp;  &nbsp; ├─ 📁 가장 긴 증가하는 부분 수열 (Longest Increasing Subsequence)         
│ &nbsp;  &nbsp;  &nbsp; └─ 📁 트리 DP (Dynamic Programming On Trees)         
├─ 📄 Template Page.md         
└─ 📄 README.md

</br></br></br>
