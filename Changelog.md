# Changelog

## v1.0
- 최초 버전 릴리즈
  - Changelog.md, 빈 주피터 노트북(code.ipynb) 생성

## v1.1
- 데이터 업로드 및 코드 추가
- 모델 개발 및 학습 파라미터/구조 기록
  - MODEL_NAME: resnet34(output_stride=16)
  - IMG_SIZE: 224 x 224
  - EPOCHS: 80
  - LEARNING_RATE: 2e-3
  - BATCH_SIZE: 64
  - Scheduler: get_linear_schedule_with_warmup
  - Optimizer: AdamW(weight_decay=0.01)
  - Loss Function: CrossEntropyLoss
  - 라벨: 양품선, 양품외로 클래스 불균형 예방
  - 데이터 증강(augmentation) 적용
    - 기본 변형: 224x224 픽셀 통일, 좌우/상하 반전
    - 기하학적 변형: 회전, 이동, 크기 조절
    - 색상/밝기 변형: 밝기/대비 조절, 색상 변형
    - 추가 노이즈/손상 변형: 일부 가리기(CoarseDropout)
  - Enhanced Model 2.ipynb 삭제
