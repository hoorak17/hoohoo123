1주차 정리.

기계를 가르치는 지도학습에 여러가지 종류가 있음.
그 중 NNC, KNN, 선형 에 대해 알아본다.

-NNC
    모든 트레이닝 데이터 값을 기억함.
    이 트레이닝 데이터를 기반으로 새로 받은 이미지를 전수비교하여 가장가까운 트레이닝 데이터와의 라벨벨을 리턴한다.
    거리를 구할 때 차이에 절댓값 혹은 차이의 제곱에 루트를 씌우는 방법 등을 다양하게 사용

-KNN
    NNC와 전반적으로 비슷, 하지만 가장 가까운 이미지를 리턴하지 않고 k개의 가까운 이미지 중 최빈값을 찾는다.
    따라서 트레이닝 데이터를 다시 넣으면 100퍼센트의 정확도가나오는 NNC와 상이한 결과가 나온다.
    거리를 구하는 식을 정하는 것 이외에 k값도 정해줘야한다. <-되도록 높은 정확도가 나오도록 설정.
    단점: 테스트 시간이 매우 길다.  
         이미지를 변형시 성능저하

-선형분류
    분류과정에서 행렬을 이용한다
    예를 들어 n*n사이즈의 이미지라면,
        1. n*n*3 (3은 RGB값)
        2. ((n^2)*3) * 1꼴로 만든다.
    단점: 색에 많이 의존한다.