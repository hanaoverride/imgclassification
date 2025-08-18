# Changelog

## v1.0
- 최초 버전 릴리즈
  - Changelog.md, 빈 주피터 노트북(code.ipynb) 생성
- 모델 개발 및 학습 파라미터/구조 기록
  - MODEL_NAME: CNN
  - NN Layer: kernel_size=3, padding=2 - BatchNorm2d - LeakyReLU - MaxPool2d(kernel_size=2) / AvgPool2d(kernel_size=4) / fc1 - dropout - fc2
  - IMG_SIZE: 224 x 224, RGB
  - EPOCHS: 39
  - LEARNING_RATE: 0.00006, 
  - BATCH_SIZE: 16
  - Scheduler: get_cosine_schedule_with_warmup(transformers)
  - Optimizer: AdamW(weight_decay=0.0001)
  - Loss Function: CrossEntropyLoss
  - 라벨: '양품', '스크래치', '부풀음', '도막떨어짐', '이물질포함'
  - 데이터 증강(augmentation) 적용
    - 기본 변형: Pad(224, padding_mode='symmetric') 적용, 좌우/상하 반전
    - 기하학적 변형: RandomRotation(30)
