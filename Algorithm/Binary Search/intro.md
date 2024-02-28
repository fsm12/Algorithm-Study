# 이분 탐색 (Binary Search)

</br>

## 개념

### 알고리즘 정의

정렬된 나열에서 반씩 쪼개며 찾는 방법

모든 자료가 정렬된 형태가 아니더라도, 대소구분이 명확하고 연산으로 값을 구할 수 있을 경우에도 사용 가능함

***"즉, 모든 값이 구해진 상태가 아니어도 대소관계만 명확하다면 이분탐색은 가능하다"***

<img src="https://github.com/fsm12/Algorithm-Study/assets/74345771/5b8c4859-631f-4fcd-ac53-4fdc81a25621" alt="[그림 1. 이분탐색 예시]" width=650 hegiht=200 >


</br>
</br>

**시간복잡도 : 정렬되어있다는 가정 하에 O(logN)**

</br>
</br>

## 구현
### 동작방식

</br>

### 1. 반복문
#### `while문` 이용

**💡 *코드 설계***
```
처음 인덱스와 마지막 인덱스를 각각 s와 e라 하자.

반으로 쪼갤 수 있는 동안 {
	중앙값을 구해본다.

	중앙값이 찾을 값과 같다면{
		찾은 것.
		더 이상의 탐색은 필요 없으므로 나간다.
	} 중앙값 < 찾을 값{
		찾을 값보다 작은 영역은 보지 않아도 되므로,
		오름차순이라면 s값을 mid+1로 설정한다.
	} 찾을 값 < 중앙값 {
		찾을 값보다 큰 영역은 보지 않아도 되므로,
		오름차순이라면 e값을 mid-1로 설정한다.
	}
}
```

**📝 *실제 코드 (Java)***

인덱스 값을 return하는 것도 가능하다.

```java
/* 클래스 및 변수 선언 생략 */

/* ------- MAIN CODE (반복문)  ------- */
public static boolean binarySearchImpl(int key) {
	int start = 0;
	int end = arr.length-1;
	
	while (start <= end) {
		int mid = (start + end) >>> 1;
		int midVal = arr[mid];
	
		if (midVal < key)
			start = mid + 1;
		else if (key < midVal)
			end = mid - 1;
		else
			return true;
	}
	return false;
}

/* ------- MAIN CODE (재귀) ------- */
public static boolean binarySearchImpl(int start, int end, int key) {
	if(end < start)
		return false;
	
	int mid = (start + end) >>> 1;
	int midVal = arr[mid];
	
	if (midVal < key)
		return binarySearchImpl(mid+1, end, key);
	else if (key < midVal)
		return binarySearchImpl(start, mid-1, key);
	else
		return true;
}
```

=> `start`와 `end`가 엇갈릴 때 종료조건임을 잘 알아두자

</br>
</br>

## 활용
### A. Lower Bound & Upper Bound
> - Lower Bound : 원하는 값이 첫번째로 나타나는 위치를 찾기
> - Upper Bound : 원하는 값이 마지막으로 나타나는 위치를 찾기
>
> ※ 자세한 내용은 구현에 따라 달라질 수 있음
>
> <img src="https://github.com/fsm12/Algorithm-Study/assets/74345771/dba12575-6b75-437a-8ee9-c70d6b2d91bb" alt="[그림 2. lowerBound, upperBound]" width=1000 >
>
> 값을 찾았을때 값(mid)를 리턴하는 과정을 삭제하고 값 비교에 등호를 추가한 뒤 start를 리턴하면 됨
> 
> </br>
> 
> **📝 *실제 코드 (Java)***
>
> ```java
> /* 클래스 및 변수 선언 생략 */
> 
> /* ------- MAIN CODE (Lower Bound)  ------- */
> public static int lowerBoundImpl(int key) {
> 	int start = 0;
> 	int end = arr.length-1;
> 		
> 	while (start <= end) {
> 		int mid = (start + end) >>> 1;
> 		int midVal = arr[mid];
> 		
> 		if (midVal < key)
> 			start = mid + 1;
> 		else if (key <= midVal)
> 			end = mid - 1;
> 	}
> 		return start;
> }
> /* ------- MAIN CODE (Upper Bound)  ------- */	
> public static int upperBoundImpl(int key) {
> 	int start = 0;
> 	int end = arr.length-1;
> 		
> 	while (start < end) {
> 		int mid = (start + end) >>> 1;
> 		int midVal = arr[mid];
> 		
> 		if (midVal <= key)
> 			start = mid + 1;
> 		else if (key < midVal)
> 			end = mid - 1;
> 	}
> 	return start;
> }
> ```

</br>

### B. 추가예정

</br>
</br>

## 해당 알고리즘을 사용해 푸는 문제

| 난이도 | 사이트 | 번호 | 문제이름 | 아이디어 | 회고 |
| ----- | ----- | ----- | ----- | ----- | ----- |
|   |   |   | <div align="center">[]()</div> | | |
|   |   |   |   |   |   |   |
|   |   |   |   |   |   |   |
|   |   |   |   |   |   |   |
