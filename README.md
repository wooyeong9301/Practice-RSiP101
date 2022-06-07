# Practice-RSiP101

https://www.kaggle.com/code/gspmoreira/recommender-systems-in-python-101/notebook   
Recommender Systems in Python 101 따라하기   
사용자들에게 개인 추천을 제공할 때, Python을 통한 **Collaborative Filtering, Content-Based Filtering과 Hybrid methods**의 수행 방법을 제시합니다.   
Dataset : Articles sharing and reading from CI&T DeskDrop (from kaggle)


### Conclusion
지금까지의 결과에서 articles에 대한 추천에선, content-based filtering과 hybrid 방법이 개별적인 Collaborative filtering보다 더 좋은 결과를 낸 것을 볼 수 있다.   
이 결과는 아래의 팁들을 참고하여 더 발전시킬 가능성이 있다.
- 모든 article이 언제 어느 때나 추천될 수 있음을 가정했지만, 주어진 시간에 유저가 볼 수 있는 article만 걸러 사용하는 것이 더 바람직하다.
- 사용 가능한 맥락 정보-시간(기간, 요일, 월), 지역(나라, 주) 그리고 기기(브라우저, 모바일)-를 활용할 수 있다.   
이런 정보들은 쉽게 **Learn-to-Rank**(XGBoost, Gradient Boosting Decision Trees with ranking objective), **Logistic**(with categorical features) 그리고 **Wide&Deep** 모델에 포함될 수 있다.   
-- https://en.wikipedia.org/wiki/Learning_to_rank   
-- https://ai.googleblog.com/2016/06/wide-deep-learning-better-together-with.html   

- 발전된 Matrix Factorization과 Deep Learning models에 대해 RecSys 리서치 커뮤니티에 더 좋은 방법들이 있다.   

최신의 Recommender Systems는 https://recsys.acm.org/ 에서 더 찾아볼 수 있다.   
리서치보다 실습을 원하면, 사용한 데이터셋에 surprise, mrec, python-recsys, Spark ALS Matrix Factorization같은 Collaborative Filtering 프레임워크들을 시도해볼 수 있다.   

아래의 사이트에서 Content-Based Filtering과 Topic Modeling 기술에 집중한 recommender system에 대한 설명을 볼 수 있다.
https://www.slideshare.net/gabrielspmoreira/discovering-users-topics-of-interest-in-recommender-systems-tdc-sp-2016
