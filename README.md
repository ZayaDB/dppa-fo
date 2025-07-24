# DPPA FO (Front Office) - React Application

## 프로젝트 개요

DPPA FO는 React와 TypeScript로 구축된 현대적인 웹 애플리케이션입니다. Material-UI를 사용하여 직관적이고 반응형인 사용자 인터페이스를 제공합니다.

## 기술 스택

- **Frontend**: React 19.1.0
- **Language**: TypeScript 4.9.5
- **UI Framework**: Material-UI (MUI) 5.x
- **Routing**: React Router DOM 6.x
- **HTTP Client**: Axios
- **Build Tool**: Create React App
- **Package Manager**: npm

## 주요 기능

- 🔐 사용자 인증 및 권한 관리
- 📊 대시보드 및 통계
- 👥 회원 관리
- 📄 계약 관리
- 📈 리포트 및 분석
- ⚙️ 시스템 설정

## 개발 환경 설정

### 필수 요구사항

- Node.js 18.x 이상
- npm 9.x 이상

### 로컬 개발 환경 설정

1. **프로젝트 클론**

   ```bash
   git clone <repository-url>
   cd dppa-fo
   ```

2. **의존성 설치**

   ```bash
   npm install
   ```

3. **환경 변수 설정**

   ```bash
   # .env 파일 생성
   REACT_APP_API_URL=http://localhost:8080/api
   ```

4. **개발 서버 실행**

   ```bash
   npm start
   ```

5. **웹 접속**
   - URL: http://localhost:3000

## 프로젝트 구조

```
src/
├── components/          # 재사용 가능한 컴포넌트
│   ├── Header.tsx      # 헤더 컴포넌트
│   └── Sidebar.tsx     # 사이드바 컴포넌트
├── pages/              # 페이지 컴포넌트
│   ├── Dashboard.tsx   # 대시보드 페이지
│   └── Login.tsx       # 로그인 페이지
├── services/           # API 서비스
│   └── api.ts          # API 통신 클래스
├── types/              # TypeScript 타입 정의
│   └── index.ts        # 공통 타입들
├── utils/              # 유틸리티 함수
├── App.tsx             # 메인 앱 컴포넌트
└── index.tsx           # 앱 진입점
```

## 사용 가능한 스크립트

```bash
# 개발 서버 실행
npm start

# 프로덕션 빌드
npm run build

# 테스트 실행
npm test

# 테스트 커버리지
npm run test:coverage

# 린트 검사
npm run lint

# 타입 체크
npm run type-check
```

## 컴포넌트 구조

### 레이아웃 컴포넌트

- **Header**: 상단 네비게이션 바
- **Sidebar**: 좌측 메뉴 사이드바
- **Layout**: 전체 레이아웃 구조

### 페이지 컴포넌트

- **Dashboard**: 메인 대시보드
- **Login**: 로그인 페이지
- **Members**: 회원 관리 페이지
- **Contracts**: 계약 관리 페이지

## API 통신

### 인증 API

- `POST /api/auth/login` - 로그인
- `POST /api/auth/logout` - 로그아웃
- `GET /api/auth/me` - 현재 사용자 정보

### 대시보드 API

- `GET /api/dashboard/stats` - 대시보드 통계

### 회원 관리 API

- `GET /api/members` - 회원 목록 조회
- `POST /api/members` - 회원 생성
- `PUT /api/members/:id` - 회원 수정
- `DELETE /api/members/:id` - 회원 삭제

### 계약 관리 API

- `GET /api/contracts` - 계약 목록 조회
- `POST /api/contracts` - 계약 생성
- `PUT /api/contracts/:id` - 계약 수정
- `DELETE /api/contracts/:id` - 계약 삭제

## 개발 가이드라인

### 코딩 컨벤션

- TypeScript strict 모드 사용
- 함수형 컴포넌트와 Hooks 사용
- Material-UI 컴포넌트 우선 사용
- 일관된 네이밍 컨벤션 적용

### 상태 관리

- 로컬 상태는 useState 사용
- 전역 상태는 Context API 또는 Redux 사용
- API 상태는 React Query 고려

### 스타일링

- Material-UI의 sx prop 우선 사용
- CSS-in-JS 방식 채택
- 반응형 디자인 적용

## 배포

### 개발 환경

```bash
npm run build
npm run serve
```

### 프로덕션 환경

```bash
npm run build
# build 폴더를 웹 서버에 배포
```

## 문제 해결

### 일반적인 문제들

- **포트 충돌**: 다른 포트 사용 (`PORT=3001 npm start`)
- **의존성 문제**: `npm clean-install` 실행
- **타입 에러**: `npm run type-check` 실행
- **빌드 실패**: `npm run build` 후 에러 메시지 확인

### 개발 도구

- React Developer Tools
- Redux DevTools (상태 관리 사용 시)
- Network 탭에서 API 요청 확인

## 라이센스

이 프로젝트는 내부 사용을 위한 프로젝트입니다.
