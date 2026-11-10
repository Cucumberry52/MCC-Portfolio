# 개인 기여와 검증 기록

[← 프로젝트 소개](../README.md) · [챗봇 설계](chatbot-design.md)

## 담당 범위

Gemini AI 챗봇 백엔드와 채팅 화면 연동을 중심으로 개발했습니다. 자연어 요청을 서비스 데이터 조회와 변경안으로 연결하고, 사용자가 확인한 뒤 서버가 검증·실행하도록 구성했습니다.

건강 문서 분석, 인증, 루틴 생성, 분석실과 기록 기능은 팀 서비스의 전체 맥락으로 소개합니다. 이 문서는 해당 기능 전체를 개인 구현 성과로 주장하지 않고, 챗봇과 연결하거나 함께 수정한 범위를 구분합니다.

## 주요 커밋

| 시점 | 작업 | 근거 |
| --- | --- | --- |
| 2026.08.15 | Gemini 연결, 정보 조회와 변경안 처리의 초기 구조, 관련 테스트 추가 | [초기 챗봇 구현](https://github.com/likelion-team3-main-hackathon/backend/commit/c988d7d91a33678382c6527651bb657d5f3e88b6) |
| 2026.08.16 | 대화방·메시지 저장과 조회 연결 | [대화 이력 구현](https://github.com/likelion-team3-main-hackathon/backend/commit/ffd2ff3dd0319d9becd69330ecae45e8b2c9232e) |
| 2026.08.16 | 채팅 화면과 요청 API 연결 | [Frontend 연동](https://github.com/likelion-team3-main-hackathon/frontend/commit/285c480) |
| 2026.08.17 | 복합 요청과 여러 변경 작업 처리, 관련 통합 테스트 보완 | [복합 요청 처리](https://github.com/likelion-team3-main-hackathon/backend/commit/556f39f9a21ba4441fd5d5beeec77f95e7bdd518) |
| 2026.08.18 | 챗봇의 조회·변경 범위와 대화 기능 확장 | [기능 확장](https://github.com/likelion-team3-main-hackathon/backend/commit/a1220438195947382936c41c06e16cbca9277e1f) |

팀 기능이 변경될 때 챗봇 브랜치에 병합하고 연동을 조정한 기록도 있습니다. 커밋 수나 변경 줄 수를 개인 기여율로 환산하지 않았습니다.

## 테스트에서 다룬 사례

| 확인 영역 | 작성한 테스트 사례 |
| --- | --- |
| 질문 처리 | 정보 선택·조회·최종 응답으로 이어지는 호출 흐름 |
| 사용자 범위 | 타인 식별자가 입력되어도 본인 정보 범위를 벗어나지 않는지 |
| 변경 실행 | 변경안 저장, 사용자 승인과 실제 DB 반영 |
| 상태 재검증 | 제안 이후 대상 상태가 바뀌면 실행을 거부하는지 |
| 취소·재실행 | 취소한 변경안이나 이미 처리한 변경안의 실행을 거부하는지 |
| 복합 요청 | 여러 항목의 변경을 하나의 승인 흐름으로 반영하는지 |
| 데이터 일관성 | 식단 제목 수정 시 관련 식단 내용도 함께 반영하는지 |

## 보관된 실행 결과

| 항목 | 확인 내용 |
| --- | --- |
| 보고서 기록 시각 | 2026.08.18 12:13:25 UTC · 21:13:25 KST |
| 실행 대상 | 챗봇 변경 흐름 통합 테스트 클래스 |
| 테스트 수 | 7 |
| 실패 / 오류 | 0 / 0 |
| 근거 | 로컬 프로젝트에 보관된 JUnit XML 실행 보고서 |

당시 실행 보고서의 결과입니다. 포트폴리오 작성 시 새로 실행한 결과, 전체 테스트 결과 또는 실제 Gemini 품질 평가 결과로 해석하지 않습니다.

## 코드와 자료

- [팀 Backend Repository](https://github.com/likelion-team3-main-hackathon/backend)
- [팀 Frontend Repository](https://github.com/likelion-team3-main-hackathon/frontend)
- [공개용 프로젝트 소개](MCC_project_public.pdf)
- [공개용 챗봇 설명](MCC_chatbot_public.pdf)

개인 계정 정보, 테스트 계정, 배포 주소와 상세 운영 설정은 공개용 자료에서 제외했습니다.
