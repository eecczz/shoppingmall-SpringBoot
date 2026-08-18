# 새 클론 실행 설정

## 1. 로컬 설정 파일 만들기

저장소 루트에서 `.env.example`을 `.env`로 복사합니다. `.env`는 Git에서 제외됩니다.

필수 값:

| 변수 | 넣을 값 | 비밀 여부 |
| --- | --- | --- |
| `DB_URL` | 로컬/운영 MySQL JDBC URL | 환경에 따라 민감 |
| `DB_USERNAME` | MySQL 사용자명 | 민감 |
| `DB_PASSWORD` | MySQL 비밀번호 | 비밀 |
| `IMP_CODE` | PortOne 가맹점 식별코드 | 공개 가능 |
| `IMP_API_KEY` | PortOne에서 새로 발급한 REST API 키 | 비밀 |
| `IMP_API_SECRET` | PortOne에서 새로 발급한 REST API Secret | 비밀 |

과거 Git 이력에 있던 PortOne Secret은 노출된 값이므로 재사용하지 말고 PortOne 콘솔에서 폐기·재발급합니다.

## 2. 실행

Java 17과 MySQL을 준비한 뒤 Windows에서는 `gradlew.bat bootRun`, macOS/Linux에서는 `./gradlew bootRun`을 실행합니다.

실제 값이 든 `.env`, 개인키, AWS 자격증명 파일은 커밋하지 않습니다.
