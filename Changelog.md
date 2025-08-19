# Changelog

## v1.0
- 최초 버전 릴리즈
  - Changelog.md, 빈 주피터 노트북(code.ipynb) 생성
- 모델 개발 및 학습 파라미터/구조 기록
  - Public Score : 기존 0.981353 -> 개선 0.986680
  - 모든 데이터 학습 모델(validation X)
  - Epochs = 15
  - TTA 전 RuntimeError: NVML_SUCCESS == r INTERNAL ASSERT FAILED 오류 대처 방법 명시
  - 재현성 문제 검증 이전
 
## v1.1
- 주요 변경/추가 사항
1. TTA 과정 메모리 문제 대처 코드 추가(try-expect)
2. 클래스 개수 변경 파라미터 추가
3. 이미지 크기 384 적용
- 모델 개발 및 학습 파라미터/구조 기록
  - Public Score : 0.99239
  - 모든 데이터 학습 모델(validation X)
  - Image Size = 384
  - Epochs = 10
  - Batch Size = 8
  - 클래스 개수 = 5
  - 메모리 문제로 model3은 앙상블에서 제외됨
  - TTA 전 RuntimeError: NVML_SUCCESS == r INTERNAL ASSERT FAILED 오류 대처 방법 명시
- 재현성 문제
  - 파이썬, 넘파이, 토치 시드 고정
  - Dataloader 시드 고정, num_workers=0 설정
  - Albumentations 시드 고정
  - 현재 찾은 모든 방법을 적용했지만 Dataloader에서 이미지를 출력할 때마다 랜덤하게 나옴
