# 🌳 공부의 숲 (Forest of Study)

**함께 공부하고, 꾸준한 습관을 만들어 가는 스터디 관리 서비스**

[![공부의 숲 배너](./img/banner.png)](https://forest-of-study-app.netlify.app/)

>공부의 숲은 스터디를 생성하고 매일의 학습 습관과 집중 시간을 기록할 수 있는 웹 서비스입니다.
>
>반복할 습관을 설정하고 달성 여부를 기록하며, 집중 타이머를 통해 목표한 공부 시간을 채우면 포인트를 획득할 수 있습니다. 또한 스터디별 학습 기록을 확인하고 응원 이모지를 남기며 서로의 학습을 응원할 수 있습니다.

**🔗 [서비스 바로가기](https://forest-of-study-app.netlify.app/)**

---

## 📑 목차

1. [프로젝트 소개](#1-프로젝트-소개)
2. [주요 기능 및 화면](#2-주요-기능-및-화면)
3. [서비스 아키텍처](#3-서비스-아키텍처)
4. [기술 스택](#4-기술-스택)
5. [팀 소개](#5-팀-소개)
6. [관련 문서](#6-관련-문서)

---

## 1. 프로젝트 소개

### 프로젝트 개요

| 항목 | 내용 |
| --- | --- |
| 프로젝트명 | 공부의 숲 (Forest of Study) |
| 프로젝트 유형 | 스터디 관리 및 학습 습관 형성 웹 서비스 |
| 개발 인원 | 3명 |
| 개발 기간 |  2026.10. 07 ~ 2026.10. 26 (20일) |
| 지원 환경 | PC / 태블릿 / 모바일 |
| 배포 환경 | Netlify / Render / Neon |

### 핵심 특징

- **스터디 중심의 학습 관리:** 스터디를 생성하고 학습 기록과 누적 포인트를 관리할 수 있습니다.
- **일일 습관 기록:** 반복할 습관을 설정하고 매일 달성 여부를 기록할 수 있습니다.
- **집중 시간 관리:** 집중 타이머로 공부 시간을 측정하고 목표 달성 시 포인트를 획득할 수 있습니다.
- **응원과 공유:** 다른 스터디에 응원 이모지를 남기거나 스터디 링크를 공유할 수 있습니다.

---

## 2. 주요 기능 및 화면

### 사이트맵

[사이트맵 이미지]

### 주요 화면

#### ① 홈 — 스터디 탐색

`/`

[홈 화면 이미지]

- 스터디 목록 조회 및 검색
- 최신순, 오래된순, 포인트순 정렬
- 더보기를 통한 스터디 추가 조회
- 최근 조회한 스터디 확인

#### ② 스터디 생성 및 수정

`/reg` · `/reg?id={id}`

[스터디 생성 및 수정 화면 이미지]

- 닉네임, 스터디 이름, 소개 및 배경 설정
- 스터디 비밀번호 설정
- 비밀번호 확인 후 스터디 정보 수정

#### ③ 스터디 상세

`/dashboard/{id}`

[스터디 상세 화면 이미지]

- 스터디 정보 및 누적 포인트 조회
- 주간 습관 달성 기록 확인
- 응원 이모지 등록 및 상위 반응 조회
- 스터디 링크 공유
- 비밀번호 확인 후 스터디 삭제

#### ④ 오늘의 습관

`/routines?id={id}`

[오늘의 습관 화면 이미지]

- 매일 반복할 습관 생성 및 관리
- 습관별 달성 여부 체크 및 해제
- 날짜별 학습 기록 관리
- 비밀번호 확인을 통한 접근

#### ⑤ 오늘의 집중

`/challenge?id={id}`

[오늘의 집중 화면 이미지]

- 집중 시간 설정 및 타이머 실행
- 일시정지, 재개 및 초기화
- 집중 상태 및 남은 시간 복원
- 목표 시간 달성 시 포인트 획득

---

## 3. 서비스 아키텍처

[서비스 아키텍처 다이어그램]

공부의 숲은 React 기반 프론트엔드와 Express 기반 백엔드로 구성된 웹 서비스입니다.

- **Frontend:** React를 사용하여 화면과 사용자 상호작용을 구현하고, Axios를 통해 백엔드 API와 통신합니다.
- **Backend:** Express를 기반으로 스터디, 습관, 집중 시간 및 포인트 관련 요청을 처리합니다.
- **Database:** PostgreSQL을 사용하여 서비스 데이터를 관리하며, Prisma ORM을 통해 데이터베이스에 접근합니다.
- **Deployment:** 프론트엔드는 Netlify, 백엔드는 Render, 데이터베이스는 Neon을 사용합니다.

스터디별 보호 기능은 별도의 회원 로그인 없이 스터디 비밀번호를 검증하는 방식으로 동작합니다.

---

## 4. 기술 스택

| 구분 | 기술 |
| --- | --- |
| Language / Runtime | JavaScript, Node.js 24.19.0, npm |
| Frontend | React, React Router |
| Build | Vite |
| Styling | Sass |
| HTTP Client | Axios |
| UI | emoji-picker-react |
| Mock Server | json-server 0.17.4 |
| Backend | Express 5, cors |
| Validation | Zod |
| ORM | Prisma 7 |
| Database | PostgreSQL 18 |
| Password Hashing | bcrypt |
| Local Database | Docker Compose |
| Deployment | Netlify, Render, Neon |

---

## 5. 팀 소개

| 이름 | 역할 | 담당 업무 | GitHub |
| --- | --- | --- | --- |
| 강교진 | [역할] | [담당 업무] | [GitHub](https://github.com/kj37kang) |
| 강재성 | [역할] | [담당 업무] | [GitHub](https://github.com/jellybrian12) |
| 고민선 | [역할] | [담당 업무] | [GitHub](https://github.com/min8808) |

---

## 6. 관련 문서

프로젝트의 상세 구현 및 설계 내용은 저장소에서 확인할 수 있습니다.

| 문서 | 설명 |
| --- | --- |
| [Repository](https://github.com/codeit-fs-16-part2-team1/forest-of-study) | 소스 코드 및 로컬 실행 안내 |
| [요구사항 명세](https://github.com/codeit-fs-16-part2-team1/forest-of-study/docs/brief.md) | 프로젝트 초기 요구사항 |
| [API 명세](https://github.com/codeit-fs-16-part2-team1/forest-of-study/docs/API.md) | API 요청 및 응답 규격 |
| [DB 설계](https://github.com/codeit-fs-16-part2-team1/forest-of-study/docs/DB.md) | 데이터베이스 구조 및 ERD |
| [기술 의사결정 기록](https://github.com/codeit-fs-16-part2-team1/forest-of-study/docs/ADR.md) | 주요 설계 결정 및 변경 이력 |
