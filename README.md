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

이 값에 대하여 몇몇 블로그가 잘못된 경우가 있어 정확한 안내가 필요할 것 같아 레퍼런스 답니다. 

특정 블로그에서 분산의 값이 

논문 1개, 파이토치, 텐서플로우 레퍼런스 답니다. 

- https://excelsior-cjh.tistory.com/177
- https://pytorch.org/docs/stable/nn.init.html
- https://www.tensorflow.org/api_docs/python/tf/keras/initializers/GlorotNormal
- https://arxiv.org/pdf/1704.08863.pdf


$$
std=   sqrt( 2/(fan\_in+fan\_out_))
$$

`fan_in` is the number of input units in the weight tensor and `fan_out` is the number of output units in the weight tensor.