# 🚗 법인차량 예약 시스템

효율적인 법인차량 예약 관리 시스템입니다. 관리자와 사용자 전용 페이지를 분리하여 제공하며, 모바일 우선 반응형 디자인으로 구현되었습니다.

## ✨ 주요 기능

### 👤 사용자 기능
- **예약 관리**: 차량 예약 생성, 수정, 취소, 연장 (최대 60분)
- **동승 시스템**: 다른 사용자 예약에 동승 요청 및 승인/거절
- **실시간 모니터링**: 내 예약 현황 및 상태 확인
- **대시보드**: 현재 예약 상태 및 최근 예약 내역

### 👨‍💼 관리자 기능
- **전체 예약 관리**: 모든 예약 조회, 수정, 취소
- **차량 관리**: 차량 추가, 수정, 삭제, 현황 모니터링
- **사용자 관리**: 사용자 정보 조회 및 수정
- **통계 대시보드**: 시스템 전체 현황 및 이용률 분석

## 🚀 기술 스택

- **Frontend**: Vue 3 + Composition API
- **Router**: Vue Router 4
- **Styling**: CSS3 (모바일 우선 반응형)
- **Build Tool**: Vite
- **PWA**: Progressive Web App 지원

## 📱 모바일 최적화

- 모바일 우선 반응형 디자인
- 터치 친화적 UI/UX
- PWA 지원으로 앱처럼 사용 가능
- 빠른 로딩 및 부드러운 애니메이션

## 🛠️ 설치 및 실행

```bash
# 의존성 설치
npm install

# 개발 서버 실행
npm run dev

# 프로덕션 빌드
npm run build

# 빌드 미리보기
npm run preview
```

## 📋 API 엔드포인트

### 인증
- `POST /api/auth/sessions` - 로그인

### 예약 관리
- `GET /api/reservations` - 예약 목록 조회
- `POST /api/reservations` - 새 예약 생성
- `PUT /api/reservations/{id}` - 예약 수정
- `PATCH /api/reservations/{id}/cancel` - 예약 취소
- `PATCH /api/reservations/{id}/extend` - 예약 연장

### 동승 관리
- `POST /api/reservations/{id}/rideshare` - 동승 요청
- `PATCH /api/rideshare/{id}/respond` - 동승 요청 응답

### 차량 관리
- `GET /api/vehicles` - 차량 목록 조회
- `POST /api/vehicles` - 새 차량 추가 (관리자)
- `PUT /api/vehicles/{id}` - 차량 정보 수정 (관리자)
- `DELETE /api/vehicles/{id}` - 차량 삭제 (관리자)
- `GET /api/vehicles/status` - 차량 현황 조회
- `GET /api/vehicles/available` - 사용 가능한 차량 조회

### 사용자 관리
- `GET /api/users/me` - 현재 사용자 정보 조회
- `GET /api/users` - 사용자 목록 조회 (관리자)

### 대시보드
- `GET /api/dashboard/stats` - 대시보드 통계
- `GET /api/dashboard/recent-reservations` - 최근 예약 현황
- `GET /api/dashboard/vehicle-utilization` - 차량 이용률

## 🎯 데모 계정

### 일반 사용자
- **사원번호**: EMP001
- **비밀번호**: password

### 관리자
- **사원번호**: ADMIN001
- **비밀번호**: admin

## 📱 모바일 사용법

1. 브라우저에서 접속
2. "홈 화면에 추가" 선택 (PWA 설치)
3. 앱처럼 사용 가능

## 🔧 개발 환경 설정

```bash
# 프로젝트 클론
git clone [repository-url]

# 의존성 설치
npm install

# 개발 서버 실행
npm run dev
```

## 📄 라이선스

MIT License


