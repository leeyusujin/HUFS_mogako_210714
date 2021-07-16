# HUFS_mogako_210714


----
####활동내용
신찬수 교수님의 강의 중 selection 파트 차례였다.


먼저 선택(selection)에 대한 개념 설명과 어떠한 문제들이 있는지 문제를 소개하는 내용이 있었다. 


선택문제는 어떤 값을 찾는 것에 있어서 가장 빠른 방법이 무엇인지 알아보는 문제이다. 예를 들어 n개의 값이 저장된 리스트 A에서 k번째로 작은 입력값을 찾고 싶다는 문제가 있다.


k = n 일 경우는 가장 큰 값을 찾는 것으로 최대값을 찾는 문제이다. 이 경우는 리스트의 첫 번째 값과 첫번째부터 차례대로 오른쪽에 있는 값과 비교하여 더 큰 값을 max로 지정하다보면 가장 큰 값을 찾을 수 있다. 이 경우는 첫 번째 값과 그 값을 제외한 나머지 값들을 비교하는 것으로 n-1번 비교하면 된다.


그렇다면 이 방법 외에 다른 방법은 없을까 생각하게 된다. 다른 방법은 토너먼트 방법이다. 리스트A의 값들을 두 값씩 비교한다. 그 두 값들 중 더 큰 값들을 또 두 개씩 묶어 비교한다. 마지막으로 하나의 값이 남을 때까지 이 방법을 반복하면 결국 가장 큰 값이 남게 된다. 이를 진행하면 이 방법 역시 n-1번 비교해야함을 알 수 있다.


편의상 하나씩 비교하는 것은 방법1, 토너먼트로 구하는 것은 방법2라 한다.


k = 1 일 경우는 가장 작은 값을 찾는 것으로 최소값을 찾는 문제이다. 이 경우는 k = n 인 경우와 같은 방법으로 구할 수 있기에 방법1과 방법2로 구할 때 모두 n-1 번 비교하면 됨을 알 수 있다.


k = 1,n 은 최소값과 최대값을 같이 구하는 문제이다. 방법1로 구할 때 k = n이 n-1번 비교하면 되는 것을 알고 있다. 그럼 k = 1은 앞에서 구한 최대값을 제외한 n-1개의 값들을 방법1로 구하는 것으로 n-2번 비교하면 구할 수 있음을 알 수 있다. 이는 총 (n-1)+(n-2) = 2n-3 번이다.


하지만 이 횟수를 더 줄이는 방법은 없을까? 방법 2를 적용해보자. 먼저 k = n일 때는 n-1번의 비교가 필요함을 알고 있다. 방법 2의 가장 처음 부분에 리스트 A에서 두 개의 수 중 다음 값으로 넘어간 값들은 어떤 값보다 큰 값이므로 제외한다. 그럼 n/2개의 값들이 남는데 최소값은 이 중 있다. 따라서 이 n/2개의 값들 중 최소값을 구하려면 n/2 - 1번의 비교가 필요하다. 이는 (n-1)+(n/2-1) = 3n/2 - 2번의 비교로 줄일 수 있음을 알 수 있다.


이처럼 어떤 값을 찾을 때 더 적은 상한의 값을 찾는 방법을 모색하는 것이 selection 문제이다.


-----


####활동하며 느낀 점
활동하기 30분 전에 팀원들 모두 모여 강의를 끝내고 풀 문제를 정하기로 하였다. 하지만 아직 개념 수업을 듣기 전이고 백준 알고리즘에는 다양한 문제들이 있어 어떤 문제를 골라야 할 지, 어떤 문제가 우리가 배울 개념에 해당하는 문제인지 모르는 상황이 발생하였다. 다행히도 신찬수 교수님의 알고리즘 구름에 selection 실습 문제가 있어서 그 문제를 풀기로 결정하였다. 저번 활동에서는 활동 시간 내에 문제를 다 해결하지 못하여 다음 날에 문제를 해결하였다. 이번 활동에서는 활동 시간 내에 문제 푸는 것까지 마무리하고 싶었지만 강의를 제대로 이해하지 못한 부분이 있어 한 번 더 강의를 수강하느라 문제를 시간내에 풀 지 못하였다. 그래도 문제를 풀 때 저번보다 저 침착하게 풀었다는 점이 나아졌다. 이 문제를 풀 때도 잊고 있었지만 다음 문제를 풀 때는 문제를 어떻게 풀 지 구조를 잡고 식을 적는 방식으로 접근해야겠다는 생각이 들었다.
