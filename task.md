# 사전학습 모델을 활용하여 멀티모달 감정 분류 모델을 설계하고 성능을 개선하시오

# 데이터셋

사용 데이터:
MDER-MA Multimodal Emotion Recognition Dataset for
ㄴ ERD-MA
----ㄴ ERD-MA Audio
--------ㄴ Angry
------------ㄴ .wav
--------ㄴ Happy
------------ㄴ .wav
--------ㄴ Neutral
------------ㄴ .wav
--------ㄴ Sad
------------ㄴ .wav
----ㄴ ERD-MA Mel-Spectrograms\_
--------ㄴ Angry
------------ㄴ .jpg
--------ㄴ Happy
------------ㄴ .jpg
--------ㄴ Neutral
------------ㄴ .jpg
--------ㄴ Sad
------------ㄴ .jpg
----ㄴ ERD-MA Spectrogram
--------ㄴ Angry
------------ㄴ .jpg
--------ㄴ Happy
------------ㄴ .jpg
--------ㄴ Neutral
------------ㄴ .jpg
--------ㄴ Sad
------------ㄴ .jpg
----ㄴ ERD-MA Text
--------ㄴ Angry
------------ㄴ .txt
--------ㄴ Happy
------------ㄴ .txt
--------ㄴ Neutral
------------ㄴ .txt
--------ㄴ Sad
------------ㄴ .txt

데이터셋 정보 : dataset_description.txt

감정 클래스:
happy / sad / angry / neutral

# 과제

텍스트 + 스펙트로그램 이미지를 이용한 감정 분류 모델을 구축하고,
성능을 극대화하시오

1. 데이터 전처리 및 분석
   단순 적용이 아닌 “왜 이 전처리가 필요한지” 설명 필수

2. 사전학습 멀티모달 모델 설계 구축
   텍스트 encoder + 이미지 encoder 결합
   최소 2가지 fusion 방식 구현 및 비교

3. 성능 향상 전략
   데이터 증강 (image augmentation)
   dropout / regularization
   learning rate scheduling
   class imbalance 처리 (weighted loss 등)

4. 출력 요구
   학습 곡선 (loss/accuracy)
   모델별 성능 비교 표
   confusion matrix

## 제출 형식

ipynb

데이터 분석 및 전처리
모델 구조 설명
실험 결과
성능 개선 전략 및 결과
분석 및 결론
