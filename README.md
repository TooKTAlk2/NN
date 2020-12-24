# numpy만으로 단순 신경망 구현하기

- SGD
- Xavier Initialization
- sigmoid
- forwardPropagation
- backpropagation
- mini batch hard coding
- plot loss function



## dataset

[google drives](https://drive.google.com/drive/folders/19qmf3ndwrkAHEvgLaj2wT2YSuiFmSEoi?usp=sharing)





## Xavier Initialization 에 관하여

이 값에 대하여 몇몇 블로그가 잘못된 경우가 있어 정확한 안내가 필요할 것 같아 레퍼런스 답니다. 제가 강의중 알려드린 Xavier 초기화도 실수가 있었습니다.

특정 블로그에서 분산과 표준편차를 잘못 표기해서 제가 documentation을 제대로 잡아 전달드립니다. 밑에 수식 마크다운이 표시되어 있지 않은데 밑 링크에 텐서 플로우나 파이토치 공식홈페이지에 정확히 적혀있습니다.

이에 따라 제 코드도 수정됨을 알려드립니다.

논문 1개, 파이토치, 텐서플로우 레퍼런스 답니다. 

- https://excelsior-cjh.tistory.com/177
- https://pytorch.org/docs/stable/nn.init.html
- https://www.tensorflow.org/api_docs/python/tf/keras/initializers/GlorotNormal
- https://arxiv.org/pdf/1704.08863.pdf


$$
std=   sqrt( 2/(fan\_in+fan\_out_))
$$

`fan_in` is the number of input units in the weight tensor and `fan_out` is the number of output units in the weight tensor.
