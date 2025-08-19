# Changelog

## v1.0
- 최초 버전 릴리즈
  - Changelog.md, 빈 주피터 노트북(code.ipynb) 생성
- 모델 개발 및 학습 파라미터/구조 기록
  - Public Score : 기존 0.981353 -> 개선 0.986680
  - 모든 데이터 학습 모델(validation X)
  - Epochs=15
  - TTA 전 RuntimeError: NVML_SUCCESS == r INTERNAL ASSERT FAILED 오류 대처 방법 명시
  - 재현성 문제 검증 이전
