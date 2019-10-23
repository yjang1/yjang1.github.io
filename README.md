<!DOCTYPE html>
<html>
<head>
	<title>Neural Network_Yeonwoo</title>
	<meta charset = "UTF-8">
</head>
<body>
<h1>1. Intro to Neural Network</h1>

<p>Artificial Neural Network = feedforward neural network = multiplayer perceptron = multilayer nueral network<br>
<b>Neuron</b> in biology = <b>Node</b> in artificial neural network <br>
<p style = "text-align:center"><img src = "neuron_description.png"></p>
신경망의 특성 세가지는 신경망의 작동원리를 더욱 어렵게 한다. 그래서 신경망 훈련인 두가지 방법을 더 많이 사용한다. 
<h3>신경망 훈련</h3>
<ul>
	<li>1.<b>전방향(propagation)</b> 단계: 신경망의 <b>가중치<sup>weight</sup></b>가 고정되며, 입력신호는 출력에 도달할 때까지 층별로 전파된다.</li>
	<li>2.<b>역방향(backpropagation)</b> 단계: 신경망 출력을 목표출력과 비교하여 오차신호를 생성. 그리고 오차신호는 역방향으로 층별로 전파. 이 단계에서는 가중치가 연속적으로 조성</li>
</ul>
</p>
<h1>2.Basic conepts for neural network</h1>
<h3>인공뉴런(Artificial Neuron)</h3>
<p>뉴런, 즉 노드는 각 입력에 가중치를 곱하고 합하여 임곗값을 적용하고 계산 결과는 연결된 다른 노드로 전송된다.
<p style = "text-align:center"><img src = "weights.png" width = "650" height = "350"></p>
<h4 style = "text-align:center; font-size:35px;"> <b>o = f(sum(W<sub>i</sub>*x<sub>i</sub>+b))</b> </h4>
여기서 <b>x<sub>i</sub></b>는 i번째 노드의 입력, <b>W<sub>i</sub></b>는 관련 가중치, <b>b</b>는 편향<sup>bias</sup>또는 상수항, <b>f</b>는 전달함수이다.
전달함수보다는 활성함수라는 용어를 많이 사용하기 때문에 활성함수를 살펴보자.<br>
<ul>
	<li><b>시그모이드<sup><small>sigmoid</small></sup>함수</b>
	<li><b>쌍공탄젠트<sup><small>hyperbolic tangent</small></sup>함수</b>
	<li><b>ReLu<sup><small>rectified linear unit</small></sup>함수</b>
</ul> 
노드를 위한 가장 유용한 활성함수는 미분 가능한 <b>비선형<sup><small>nonlinear</small></sup></b>함수이다.
따라서, 미분 가능한 활성화 함수들은 <b>역전파<sup><small>backpropagation</small></sup></b> 알고리즘을 이용하여 신경망 훈련을 쉽게 사용할수 있다.
</p>
<p style = "text-align:center"><img src = "activation.png" width = "650" height = "350"></p>
<h4>Charateristics of Sigmoid function</h4>
<ul>
	<li><b>함수값이 (0,1)로 제한됨</b>
	<li><b>매우 큰 값을 가지면 함수값은 거의 1이며, 매우 작은 값을 가지면 거의 0이다.</b>
</ul> 
<p>저런 특징 때문에 초기에는 많이 사용했지만 최근에는 단점들 때문에 잘 사용하지 않는다.</p>
<ul>
	<li><b>Gradient Vanishing 현상: 미분함수에 대해 x=0애서 최대값 1/4을 가지고 input 값이 일정이상 올라가면 미분값이 거의 0에 수렴하게 된다.</b>
	<li><b>매우 큰 값을 가지면 함수값은 거의 1이며, 매우 작은 값을 가지면 거의 0이다.</b>
</ul> 
<!-- Hidden comment -->


</body>
</html>
