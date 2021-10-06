# 정지문제

H 기계는 특정 기계의 청사진과 그 청사진 기계에 넣을 입력값을 입력받아 청사진 기계가 멈추는지 멈추지 않는지 결정한다.
  ex) 산수를 푸는 A기계의 청사진과 '3+5'라는 입력값을 넣으면 Not Stuck이라고 결정하여 출력.

P 기계는 받은 입력값을 두 장의 복사본으로 출력한다.

N 기계는 '멈추지 않음'을 입력 받으면 멈추고. '멈춤'을 입력 받으면 멈추지않고 웃는 얼굴을 출력한다.

위 기계들을 위에서부터 P기계, H기계, N기계 순으로 연결하여 X기계라고 정의한다.
#

X기계에 X기계의 청사진을 입력하면, P기계가 입력받은 청사진을 두 장의 복사본으로 출력하고 그것을 H기계가 입력받는다.

H기계가 두장의 청사진을 입력받았을 때의 서로 다른 두 가지를 가정해보자.

- H기계가 X기계의 청사진을 입력받으면 '멈추지 않음'을 출력했을 때,
  N기계는 H기계의 출력값인 '멈추지 않음'을 입력받고 X기계를 멈추게 한다.
  
  여기서 X기계는 멈추는데, H기계는 '멈추지 않음'을 출력하였으니 모순이 된다.
  

- H기계가 X기계의 청사진을 입력받으면 '멈춤'을 출력했을 때,
  N기계는 H기계의 출력값인 '멈춤'을 입력받고 X기계를 멈추지 않고 웃는 얼굴을 출력한다..
  
  여기서 X기계는 멈추지 않는데, H기계는 '멈춤'을 출력하였으니 모순이 된다.
#

위를 이해하는데 조금 시간이 걸렸으니 더 자세히 이해해 보자.

첫번째 가정인 H기계가 '멈추지 않음'을 출력했을 때, N기계가 '멈추지 않음'을 받으면 X기계를 멈추게 한다고 했다.

그런데 H기계는 '멈추지 않음'이라고 출력했었다. H기계가 X기계가 멈추지 않는다고 반환한 것이다. 

하지만 X기계는 멈췄기 때문에 이러한 점이 모순이 된 것이다. 

두번째 가정도 첫번째 가정과 비슷하다.

H기계가 '멈춤'을 출력했는데, X기계는 멈추지 않고 웃는얼굴을 출력했다.

H기계는 멈춘다고 반환하였지만, 실제로는 멈추지 않고 웃는 얼굴을 출력했기 때문에 모순이 된 것이다.
#

결국, H기계는 자신이 속한 기계에서 H기계라는 자신만 정합성(공리계에 논리적 모순이 없는 것)을 보여준다.

H기계의 답을 반대로 행동하는 기계(N기계)가 연결되어 있으면,

H기계는 항상 모순이 될 수 밖에 없다.
