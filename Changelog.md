# Changelog

## v1.0
- 최초 버전 릴리즈
  - Changelog.md, 빈 주피터 노트북(code.ipynb) 생성
- 모델 개발 및 학습 파라미터/구조 기록
  - Public Score : 0.97485
  - Efficientnet-b1, 2, 3 : Soft-voting
  - RGB, (224, 224)
  - Data Augmentation : transforms, Train - CenterCrop(180), RandomHorizontalFlip(0.5), RandomVerticalFlip(0.2), RandomRotation(20) / Test - CenterCrop(180)
  - Fine-tuning : CNN layer, classifier
  - Validation_ratio=0.15, BS=16, Epochs=20, Val-F1(best model)
  - AdamW : lr=0.0006, weight_decay=0.001
  - LR_Scheduler : get_cosine_schedule_with_warmup
