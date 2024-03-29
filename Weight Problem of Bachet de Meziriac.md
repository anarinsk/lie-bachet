**Weighing Problem of Bachet de Méziriac**

2018-09-17
Jun Sok Huhh | :house:[lostineonomics.com](http://lostineconomics.com)


# Problem 

수리 퍼즐로 유명한 제수이트파 수도사 바셰(Bachet de Méziriac)의 저울 문제를 함 풀어보자. 문제는 다음과 같다. 
* 1~40 사이의 임의의 무게를 지니는 어떤 짐이 있다고 하자. 
* 이 짐의 무게를 저울에 달아 무게를 파악하는 것이 목적이다. 
* 자연수 스케일을 지니는 임의의 추를 이용할 수 있다. 
* 추를 달 때 저울 양쪽을 모두 이용할 수 있다. 즉, 무게를 파악하는 데 짐을 단 쪽도 추를 올려 놓을 수 있다. 

이때 1~40 사이의 임의의 무게를 지닌 짐의 무게를 측정하기 위해 필요한 최소한 추는 어떤 것인가? 

# Key insight 

사실 일종의 인덕션 문제다. 그런데 문제의 핵심에 접근하기는 쉽지는 않다. 우선 표기법부터 정하고 가자. 자연수 $x$라는 무게를 지닌 추는 $x$W으로 표기한다. 즉, $10$W는 10이라는 무게를 지닌 추를 의미한다. 필요한 경우 W앞에 괄호를 붙여 사용하도록 하자. 아래에서 $n$은 해당 상황에서 적절하게 큰 자연수를 나타낸다. 

* 이제, $\{ 1, 2, \dotsc, n \}$의 무게를 모두 표현할 수 있는 추의 집합 $\omega$가 있다고 하자. 
* 여기에 $2n+1$의 무게를 지닌 추 $(2n+1)$W 하나를 추가해보자. 추 집합 $\omega$에 $(2n+1)$W 라는 추 하나를 추가했을 때 추가로 표현할 수 있는 무게는 얼마나 확장될까? 먼저 $\omega$에 이 새로운 추를 추가한 추 집합을 $\omega'$이라고 하자. 즉, 

$$
\omega^+ = \{ w | w \in \omega \cup \{ (2n+1) {\rm W} \} \}
$$

* $(2n+1)$W를 추가해 더 측정할 수 있는 무게는 다음과 같다. 
	 * 당연히 무게 $2n+1$이 추가된다. 
	 * $\{ 2n+2, 2n+3, \dotsc, 3n+1 \}$의 무게를 이 추 조합으로 측정할 수 있다. 짐이 해당 범위의 무게를 지닌다면, 짐을 왼쪽에 그리고 오른쪽에 $(2n+1)$W와 $\omega$를 적절하게 올리면 된다. 
	* 다음으로 짐의 무게가 $\{ n+1, n+2, \dotsc, 2n\}$에 속한 경우에도 $\omega$ 그리고 $(2n+1)$W의 조합으로 무게 측정이 가능하다. 이는 $(2n+1)$W를 오른쪽에 두고, 왼쪽에 짐과 $\omega$를 조합함으로써 저울의 균형을 맞출 수 있다.  
* 결론적으로 추 집합 $\omega^+$으로 $\{ 1,2, \dotsc, n, n+1, n+2, \dotsc, 2n, 2n+1, 2n+2, \dotsc, 3n+1\}$ 무게를 측정할 수 있다.  

# Induction 

위의 사실을 알고 있는 상태에서 이제 induction을 통해 해법을 알아보자. 위의 예에서 무게 $n$ 까지 측정할 수 있는 추의 조합 $\underline\omega$가 무게의 측정을 위해 필요한 추의 최소 집합이라면, 하나를 추가해 측정할 수 있는 $3n+1$의 무게까지는 기존 $\underline\omega$ 에 $(2n+1)$W가 원소로 추가된 집합, 즉 추 집합 $\underline\omega^+$가 최소 추의 조합이 된다. $\underline\omega$에  더해진 추는 단 하나이기 때문이다. 

- 만일, $n+1$ 무게까지의 $\underline\omega$ 추 조합으로 측정이 가능했다면 이는 애초에 $n$까지 측정하는 최소 추 집합이라는  $\underline\omega$의 정의에 위배된다. 
- 만일 어떤만일 $w^*$가 $\{ 1, 2, \dotsc, n, n+x\} (x = 1, 2, ..., 2n+1)$를 표현하는 최소의 추 조합이고, 라면? 이런 경우는 어떻게 생각해야 할까? 이 경우 $\underline\omega$은 $n+1$까지 측정하는 최소의 추 조합이은 될 수 없다고 가정하자.어야 한다. 그렇다면, $n+1$의 무게를 측정하기 위해서는 최소한 하나 이상의 추가 필요하다. 이때 앞서 보았듯이 $(2n+1)$W의 추를 추가함으로써 $n+1$, $n+x$를 모두 표시했다. 즉, 1부터 $n+x$까지 순차적으로 존재하는 자연수 무게를 측정하기 위해 필요한 최소 추 집합의 집합에는 $\underline\omega^+$가 반드시 속한포함된다. 

이제 인덕션을 전개해보자. 
* 무게 $1$을 재기 위한 최소한의 추 조합은 $1$W이다. 
* $2*1+1$의 무게를 지니는 $3$W의 추를 추가하면, $1$W, $3$W의 조합은 $\{1,2,3,4\}$ 무게를 측정할 수 있다. 여기서 $4$는 $3*1+1$에서 비롯한다. 
* $2*4+1$의 무게를 지니는 $9$W의 추를 추가하면, $1$W, $3$W, $9$W의 조합은 $\{1,2,\dotsc, 13\}$ 무게를 측정할 수 있다. $13$은 $3*4+1$에서 나온다. 
* 여기에 $2*13+1$의 무게를 지니는 $27$W의 추를 추가하면, $1$W, $3$W, $9$W, $27$W의 조합은  $\{1,2,\dotsc, 40\}$의 무게를 측정할 수 있다. 표로 정리해보자. 

|추가로 필요한 추의 무게| 측정 가능한 무게 상한  |
|--|--|
| $1$ | $1$ |
| $2\times 1 + 1 = 3$ | $3 \times 1 + 1 = 4$  |
| $2\times 4 + 1 = 9$ | $3 \times 4 + 1 = 13$  |
| $2\times 13 + 1 = 27$ | $3 \times 13 + 1 = 40$  |


:feet:Jun Sok Huhh | :house:[lostineonomics.com](http://lostineconomics.com)
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTc4ODQxMzAxMyw0MjMyOTIyMzcsLTEwOT
U2MTMwOCwxMzA2ODI4NDg5XX0=
-->