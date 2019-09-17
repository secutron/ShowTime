여기는
======


## DP : 구글 코랩에서, TF2.0-beta1 기준으로, 케라스에 포함된 데이터셋만 다룬다

- 코랩인가 콜랩인가?  공교롭게도 내가 근무하는 곳에서 콜랩이라 발음하면.. 다들 아틀라시안의 컨플루언스를 떠올린다. 


## DP-APP : 구글 코랩에서 동작 가능한 다양한 응용들만 다룬다 

![Alt text](/baby.jpg)








### TF2.0 beta1 특징

eager execution을 디폴트로 지원: 

- eager excution에 대한 기본 개념은 [여기](https://developers-kr.googleblog.com/2018/05/eager-execution.html)를 참조한다

- 즉, eager execution이 지원되는 경우 아래와 같이 (대화형으로!!) tf를 사용할 수 있다

~~~
x = [[2.]]
m = tf.matmul(x, x)

print(m)
~~~

- 이런 것도 가능하다

~~~
# 예전엔...
# outputs = session.run(f(placeholder), feed_dict={placeholder: input})
#
# TF2.0에서는
outputs = f(input)
~~~

- 그 외 장점은 매우 많다. 필요하면 구글링해서 찾아 본다.


### 구글 코랩 기본팁: 

- 구글 코랩에서 인라인 도움말을 보려면, 함수 괄호 다음에 캐럿을 위치시키고 탭 키를 누른다.
  (주피터의 shift+tab은 코랩에서 동작하지 않는다)
  
- tf2.0-beta1  vs.  tf2.0-rc0

~~~
### beta1
###
!pip install tensorflow-gpu==2.0.0-beta1
### beta1


### rc0
###
from __future__ import absolute_import, division, print_function, unicode_literals

try:
  # %tensorflow_version only exists in Colab.
  %tensorflow_version 2.x
except Exception:
  pass
### rc0

import tensorflow as tf
print(tf.__version__)
~~~

