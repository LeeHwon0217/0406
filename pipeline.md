# 셀 구성

1. 환경 설정

- 라이브러리 설치 (transformers, torch, torchvision, Pillow 등)
- 현재 환경 점검. torch로 cuda 확인.

2. 데이터 전처리

- 데이터 상태 점검
  - 클래스별 샘플 수 확인 → class imbalance 여부 파악 (6번 전략 근거)
  - 텍스트 길이 분포 확인 → max_length 설정 근거
  - 스펙트로그램 이미지 크기 확인
- 데이터 전처리
  - 이유

3. 가설 수립

- Late Fusion
- MBT Bottleneck Fusion

4. 사전 학습 멀티모달 모델 설계

- 텍스트 encoder (aubmindlab/bert-base-arabertv02)
- 이미지 encoder (ResNet / ViT)
- Late Fusion
- MBT Bottleneck Fusion
- 캐싱 파이프라인
  - 텍스트 토크나이징 + 이미지 텐서 변환을 1회만 수행 후 .pt로 저장
  - 학습 시 .pt 파일만 로드하여 CPU 병목 제거
- 커스텀 Dataset 클래스 / DataLoader
  - train / val / test split
  - num_workers, pin_memory 설정

5. 가설 점검

- 학습 루프 (Late Fusion / MBT Bottleneck Fusion 공통)
  - optimizer, loss function, lr scheduler 설정
  - 학습 → 검증 반복
- Late Fusion
  - 학습 곡선
    - loss/accuracy
  - confusion matrix
- MBT Bottleneck Fusion
  - 학습 곡선
    - loss/accuracy
  - confusion matrix
- 모델별 성능 비교
  - 표

6. 성능 향상 전략

- Late Fusion
  - 전략
- MBT Bottleneck Fusion
  - 전략
- 성능 향상 수행
  - 결과 비교

7. 결과

- 우수 모델
  - 이유
- 분석 및 결론
