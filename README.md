# 🔗 MyLink (마이링크)

> **나를 표현하는 가장 간단하고 직관적인 프로필 링크 서비스**  
> 흩어져 있던 SNS, 포트폴리오, 작업물을 단 하나의 링크로 모아보세요.

[![Next.js](https://img.shields.io/badge/Next.js-16.3-black?style=flat-square&logo=next.js)](https://nextjs.org/)
[![React](https://img.shields.io/badge/React-19.2-blue?style=flat-square&logo=react)](https://react.dev/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-v4-38bdf8?style=flat-square&logo=tailwindcss)](https://tailwindcss.com/)
[![Firebase](https://img.shields.io/badge/Firebase-Auth_%26_Firestore-ffca28?style=flat-square&logo=firebase)](https://firebase.google.com/)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](./LICENSE)

---

## 🌐 라이브 데모 (Live Demo)

* **공식 웹 페이지**: [https://tkflrnstk.github.io/My-link-Hanyang-e-learning-2026/mylink/](https://tkflrnstk.github.io/My-link-Hanyang-e-learning-2026/mylink/)
* **풀스택 메인 저장소**: [https://github.com/tkflrnstk/mylink](https://github.com/tkflrnstk/mylink)

---

## ✨ 핵심 기능 (Features)

### 1. 토스 디자인 시스템 (TDS) 기반 UI/UX
* **정교한 인터랙션**: 부드러운 곡률(`rounded-2xl`, `rounded-3xl`), 토스 시그니처 블루(`#3182F6`), 고대비 타이포그래피.
* **모바일 퍼스트 반응형 카드 레이아웃**: 모든 모바일 기기(360px ~ 460px) 및 데스크톱 환경에서 완벽하게 최적화된 뷰 제공.
* **마이링크 주소 복사 토스트 UI**: 클릭 한 번으로 내 링크를 클립보드에 복사하고 감성적인 애니메이션 토스트 제공.

### 2. 프로필 및 링크 관리
* **인라인 프로필 커스텀**: 성명, `@아이디(displayName)`, 자기소개 실시간 수정 지원.
* **다채로운 링크 카드**: GitHub, 기술 블로그, 이메일, LinkedIn, 포트폴리오, YouTube, 노션, 오픈카카오톡 지원.
* **카테고리 뱃지 & 이모지**: 링크별 목적에 맞는 뱃지(`코드`, `기록`, `문의`, `경력` 등) 및 전용 이모지 매핑.

### 3. 풀스택 데이터 아키텍처 (Next.js + Firebase)
* **Google 소셜 로그인**: Firebase Authentication 기반의 간편 로그인 및 계정 연동.
* **Cloud Firestore 실시간 동기화**: `users/{userId}/links` 하위 컬렉션을 통한 사용자별 링크 CRUD 및 실시간 양방향 동기화.
* **낙관적 업데이트 (Optimistic Update)**: TanStack Query v5를 활용하여 지연 없는 즉각적인 UI 반응 구현.
* **보안 규칙 (Security Rules)**: `firestore.rules`를 통한 스키마 검증 및 고유 `displayNames` 중복 방지 규칙 적용.

---

## 🛠️ 기술 스택 (Tech Stack)

| 구분 | 사용 기술 |
| :--- | :--- |
| **Frontend** | Next.js 16 (App Router), React 19, TypeScript |
| **Styling** | Tailwind CSS v4, shadcn/ui, Toss Design System (TDS) |
| **State Management** | TanStack Query v5, React Context API |
| **Form & Validation** | React Hook Form, Zod |
| **Backend & Database** | Firebase Authentication, Cloud Firestore, Cloud Storage |
| **Hosting & CI/CD** | GitHub Pages, Vercel |

---

## 📂 프로젝트 구조 (Project Structure)

```text
My-link/
├── mylink/                      # 마이링크 메인 프로젝트 모듈
│   ├── index.html               # 라이브 프로필 웹 페이지 (GitHub Pages)
│   ├── src/                     # Next.js 16 소스 코드
│   │   ├── app/                 # App Router (메인, [displayName], API)
│   │   ├── components/          # UI 및 링크 컴포넌트 (TDS 스타일)
│   │   ├── context/             # AuthContext (인증 상태)
│   │   ├── hooks/               # useLinks, useUserProfile (TanStack Query)
│   │   ├── lib/                 # firebase 초기화, links CRUD 유틸
│   │   └── types/               # TypeScript 인터페이스 정의
│   ├── docs/                    # PRD 기능명세서 및 디자인 시스템 문서
│   │   ├── PRD.md               # 서비스 제품 요구사항 정의서
│   │   └── design.md            # 토스 디자인 시스템(TDS) 가이드라인
│   ├── firestore.rules          # Firestore 데이터베이스 보안 규칙
│   ├── storage.rules            # Cloud Storage 파일 보안 규칙
│   └── package.json             # 프로젝트 종속성 및 스크립트
├── index.html                   # 루트 자동 리다이렉트
└── README.md
```

---

## 🚀 로컬 실행 방법 (Getting Started)

`mylink` 디렉토리 내에서 로컬 개발 서버를 실행할 수 있습니다:

```bash
cd mylink

# 패키지 설치
npm install

# 로컬 개발 서버 실행
npm run dev
```

브라우저에서 `http://localhost:3000`에 접속하여 로컬 개발 화면을 확인하실 수 있습니다.

---

## 📄 라이선스 (License)

This project is licensed under the [MIT License](./LICENSE).
