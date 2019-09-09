여기는
======


## 구글 코랩에서, TF2.0-beta1 기준으로, 케라스에 포함된 데이터셋만 다룬다

### TF2.0 beta1

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


### 기본팁: 

- 구글 코랩에서 인라인 도움말을 보려면, 함수 괄호 다음에 캐럿을 위치시키고 탭 키를 누른다.
  (주피터의 shift+tab은 코랩에서 동작하지 않는다)
  
  

