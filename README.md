# 한국어 챗봇 모델링

## 개요
> **아이펠 GoingDeeper NLP Project** <br/> 
> **프로젝트 기간: 2024.07.10 ~ 2024.07.11** <br/>

<br>

---
## 프로젝트 소개
- 한국어 번역 데이터를 바탕으로 한국어 챗봇을 만들어보는 프로젝트틀 진행했습니다.

- `Seq2Seq for Translator From Scratch`
  - 트랜스포머 구조를 학습하고 직접 구현하는 시간을 가졌습니다.
  - [ko-en-translator-Seq2Seq.ipynb](ko-en-translator-Seq2Seq.ipynb)
- `Transformer for Translator From Scratch`
  - 앞서 구현한 Transformer 구조를 수정하여 GPT 구조를 만들었습니다.
  - [ko-en-translator-Transformer.ipynb](ko-en-translator-Transformer.ipynb)

### 데이터셋 출처

#### 한영 번역 데이터는 아래 데이터를 사용했습니다
  ```text
  https://github.com/jungyeul/korean-parallel-corpora/tree/master/korean-english-news-v1
  ```

#### 다운로드 방법은 두 가지가 있습니다
1. 첫 번째로 데이터를 다운로드 받아서 압축을 해제한뒤에 파일을 읽어서 사용합니다
   - 다운로드하여 사용하는 방법은 `ko-en-translator-Transformer.ipynb` 코드를 참고하면 됩니다
2. `Korpora` 라는 오픈소스를 이용하는 방법입니다
   - `ko-en-translator-Seq2Seq.ipynb` 코드를 보면 쉽게 알 수 있을 것입니다.
   - 아래 링크를 통해서 korpora에 대해 알 수 있습니다!
     - https://ko-nlp.github.io/Korpora/en-docs/corpuslist/korean_parallel_koen_news.html

<br>

---

## 사용 용도
- [korean-chatbot-Transformer.ipynb](Ko-Chatbots-From-Scratch/korean-chatbot-Transformer.ipynb)
  - Transformer에 대한 자세한 구조를 코드를 통해 확인해보고 싶다면 이 코드를 통해 학습할 수 있습니다
  - 또한, 이 파일에는 custom model을 저장하는 코드가 추가되어 있습니다
  - learning rate, model 구조를 customize 했을 때 어떻게 모델을 저장하고 불러오는지 참고하기 좋을 것 같습니다
- [korean-chatbot-GPT.ipynb](Ko-Chatbots-From-Scratch/korean-chatbot-GPT.ipynb)
  - 위 transformer notebook을 보고 GPT를 이해하고 싶다면 이 파일을 통해 쉽게 이해할 수 있을 것입니다

<br>

----

## 사용 기술

### Environment
![Pycharm](https://img.shields.io/badge/PyCharm-000000.svg?&style=for-the-badge&logo=PyCharm&logoColor=white)
![Github](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=GitHub&logoColor=white)

### Development
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![keras](https://img.shields.io/badge/Keras-D00000?style=for-the-badge&logo=Keras&logoColor=white)
![Tensorflow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2C2D72?style=for-the-badge&logo=pandas&logoColor=white)
![Numpy](https://img.shields.io/badge/Numpy-777BB4?style=for-the-badge&logo=numpy&logoColor=white)
![scikit](https://img.shields.io/badge/scikit_learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
<br>

----
회고 및 결론
---
### 회고
<details>
  <summary><b>Seq2Seq 구현 회고</b></summary>
  <div markdown="1">
    <li> 배운 점 </li>
      <ul>
        <li> 번역기를 만들기 위해 Seq2seq를 직접 구현하면서 구조를 파악해볼 수 있었다. </li>
      </ul>
    <li> 아쉬운 점 </li>
      <ul>
        <li>시간이 너무 오래걸려서 시각화 및 문제점을 구체적으로 파악하기 어려웠다. </li>
        <li>생각보다 좋은 결과가 나오지 않아서 아쉽다. </li>
      </ul>
    <li> 느낀 점 </li>
      <ul>
        <li>시간이 너무 오래걸리고 번역기를 만들기 위해서는 정말 많은 데이터를 통한 학습이 필요한 것 같다. </li>
      </ul>
    <li> 어려웠던 점 </li>
      <ul>
        <li>dropout layer를 어디에 두어야 할지, 어떻게 모델을 구성해야 더 좋은 성능을 낼 수 있을지 생각하는 것이 어렵다. </li>
      </ul>
  </div>
</details>

<details>
  <summary><b>Transformer 구현 회고</b></summary>
  <div markdown="1">
    <li> 배운 점 </li>
      <ul>
        <li>transformer의 구현방법을 알 수 있었다.</li>
        <li>seq2seq와 비교했을 때 확실히 더 좋은 성능이 나왔다.</li>
      </ul>
    <li> 아쉬운 점 </li>
      <ul>
        <li>데이터가 부족해서 성능이 잘 나오지 않은 것 같다. </li>
        <li>코드에 대한 이해를 좀 더 꼼꼼하게 하지 못해서 아쉬웠다. </li>
      </ul>
    <li> 느낀 점 </li>
      <ul>
        <li>shape을 바꿀때 순서를 왜 바꿨다가 하는지 고민을 하는 시간을 가졌는데 꼼꼼하게 공부하는 것이 중요하게 느껴졌다. </li>
        <li>앞으로는 좀 더 꼼꼼하게 코드나 내용을 이해하는 시간을 가져야 겠다. </li>
      </ul>
    <li> 어려웠던 점 </li>
      <ul>
        <li>transformer의 구조를 이해했다 생각했는데 다시 코드로 구현하려하니까 어려웠다. </li>
        <li>input shape 맞추는 것이 생각보다 까다롭게 느껴졌다. </li>
      </ul>
  </div>
</details>

### 결론
- 직접 Transformer와 GPT를 구현하면서 자세한 구조에 대해서 배울 수 있었습니다
- 이번 경험을 통해 Transformer, GPT 구조에 대해 잘 알 수 있게 되었습니다
<br>

---
## 디렉토리 구조
```bash
├── README.md
├── data : 데이터 셋을 여기에 다운 받아서 넣어줍니다
├── ko-en-translator-Seq2Seq.ipynb
└── ko-en-translator-Transformer.ipynb
```

