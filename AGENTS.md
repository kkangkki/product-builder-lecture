# Repository Guidelines

## 프로젝트 구조 및 모듈 구성
현재 저장소는 비어 있습니다. 콘텐츠를 추가할 때는 다음과 같이 단순하고 일관된 구조를 유지하세요.
- `src/`: 애플리케이션 또는 라이브러리 코드
- `tests/`: 자동화 테스트
- `assets/`: 정적 파일(이미지, 데이터, 픽스처)
- `docs/`: 긴 형식의 문서
새로운 최상위 폴더를 추가하면 이 문서에 반영합니다.

## 빌드, 테스트, 개발 명령
아직 빌드/테스트 스크립트가 없습니다. 추가 시 아래처럼 정확한 명령을 기록하고 환경 간 일관성을 유지하세요. 예시:
- `python -m venv .venv` 및 `source .venv/bin/activate`: 로컬 개발 환경 구성
- `pip install -r requirements.txt`: 의존성 설치
- `pytest`: 테스트 실행
다른 스택을 선택하면 실제 명령으로 바꿔 주세요.

## 코딩 스타일 및 네이밍 규칙
언어/도구 체인이 정해지기 전까지는 예측 가능한 기본값을 따릅니다.
- 들여쓰기: 공백 4칸
- 파일명: 소문자 + 하이픈(예: `data-loader.py`) 또는 언어 관례에 따라 언더스코어
- 모듈/패키지명: 소문자, 공백 금지
Python 프로젝트로 확정되면 `ruff`, `black`을 추가하고 `pyproject.toml`에 설정합니다.

## 테스트 가이드
테스트는 `tests/`에 두고 대상 단위를 이름에 반영합니다(예: `tests/test_parser.py`). pytest 사용 시 픽스처는 `tests/conftest.py`에 둡니다. 테스트가 도입되면 간단한 `README` 섹션을 추가하세요.

## 커밋 및 PR 가이드
현재 Git 저장소가 아닙니다. Git을 초기화하면 `Add data ingestion pipeline`처럼 명확한 명령형 메시지를 쓰거나 Conventional Commits(예: `feat: add ingestion pipeline`)를 사용하세요. PR에는 다음을 포함합니다.
- 변경 요약
- 관련 이슈/작업 링크
- 사용자 영향이 있는 변경의 경우 스크린샷 또는 로그

## 설정 및 보안
비밀 정보는 저장소에 커밋하지 않습니다. 로컬 설정은 `.env`를 사용하고, 필요한 변수는 `docs/configuration.md` 또는 `README.md`에 문서화합니다.
