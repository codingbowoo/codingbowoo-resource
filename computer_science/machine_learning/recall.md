## Recall

오늘의 의문은, 도대체 machine learning에서 이야기하는 'recall'이란 무엇인가? 이다.

##### 찾아보게 된 이유
요즘 Peter Flach의 [*Machine Learning:The Art and Science of Algorithms that Make Sense of Data*](https://www.amazon.com/Machine-Learning-Science-Algorithms-Sense/dp/1107422221)을 읽고 있다. 
52 - 61쪽에 걸쳐 Classification에 대한 이야기를 하고 있는데, 어찌어찌 True/False Positive/Negative 까지는 이해를 했다.
그런데 갑자기 **average recall**이라는 말이 나오는 것이 아닌가. 읽다보면 이해하겠지, 하고 넘겼더니 61쪽이 나오기까지 이해를 못했다! 
<br>도와줘! 구글링!

##### recall이 무엇인고 하니 

[다크 프로그래머 - precision, recall의 이해](http://darkpgmr.tistory.com/162)와
[테리의 딥러닝 토크 #1.5. Accuracy, Precision, Recall](https://youtu.be/1jboC7nWnfM)를 참고했다.

짧게 말하면 정확도와는 별도의 개념인 **검출율**이라고 한다. 

###### 예시
10명의 사람 중에 안경을 쓴 사람이 3명이라고 하자.
(편의상 사람 이름을 일,이,삼,사,...,구,십 이라고 했을때 일,이,삼이 안경을 썼다고 하자.)

내가 안경 쓴 사람을 데려와! 라고 했을 때,
일, 이, 삼만 데려오면 검출율 100%가 맞다.
그런데 검출율이라는게 골때리는게, 일, 이, 삼, ... , 구, 십을 다 데려와도 검출율은 100%다. <br>

다크 프로그래머의 블로그에 있는 수식을 잘 이해하면 좋을 것 같다.

```
recall = (detected TRUE)/(total number of existing TRUE)
precision = (TRUE detections)/(whole detections of an algorithm)
```

위의 예시에 따르면, 
일, 이, 삼만 데려오면 recall 100% (3 out of 3), precision 100% (3 out of 3)<br>
일, 이, 삼, ... , 구, 십을 다 데려오면 recall 100% (3 out of 3) precision 30%(3 out of 10) 이다.<br>

그러나 어떤 알고리즘을 단순히 recall이 얼마고 precision이 얼마여서 성능이 좋고 나쁘다고는 말하기 어렵다고 한다!
오늘은 여기까지!


+ 다음날 덧붙이는 말: 그래서 ROC curve를 놓고 해당 커브를 이해하는 작업이 필요했다고 한다..... 
