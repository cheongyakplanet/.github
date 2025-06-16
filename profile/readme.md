# 청약플래닛 (CheonYakPlanet) 🏠
&nbsp; **청약플래닛**은 공공 분양 정보를 쉽게 찾고 관리할 수 있는 플랫폼입니다.<br>
사용자가 관심 지역의 청약 정보를 효율적으로 추적하고, 주변 인프라와 금융 정보를 함께 제공하여 더 나은 주거 선택을 돕습니다.

***부동산 정보 플랫폼***&nbsp;으로 성장하여, 사람들이 부동산 정보에 스마트하게 접근할 수 있도록 지원하겠다는 비전을 갖고 있습니다.<br>

## 🚀 주요 기능

### 📍 청약 정보 서비스
- **실시간 청약 정보**: 공공데이터 기반 최신 분양 정보 제공
- **지역별 검색**: 시/도, 구/군 단위 세부 검색 기능
- **관심 지역 설정**: 최대 5개 지역 관심 등록 및 알림
- **상세 정보**: 분양가, 공급 일정, 특별공급 대상 등 종합 정보

### 🗺️ 위치 기반 인프라 정보
- **주변 인프라 조회**: 반경 1km 내 지하철역, 학교, 공공시설 정보
- **거리 계산**: 하버사인 공식 기반 정확한 거리 측정
- **지도 연동**: 카카오맵 API를 통한 시각적 위치 정보

### 👥 커뮤니티
- **게시판**: 청약 관련 정보 공유 및 토론
- **댓글/답글**: 계층형 댓글 시스템
- **좋아요/싫어요**: 게시글 평가 시스템

### 🤖 AI 채팅 어시스턴트
- **Gemini 2.0 Flash 연동**: 청약 관련 실시간 상담
- **일일 사용 제한**: 사용자당 15회 메시지 제한
- **WebSocket 기반**: 실시간 채팅 환경

## 🏗️ 시스템 아키텍처
![시스템아키텍처 drawio](https://github.com/user-attachments/assets/53be214e-bfd5-4a3d-83e4-88fb1f4b013e)
### 기술 스택
| Category | Subcategory | Technology | Version |
| --- | --- | --- | --- |
| **Frontend** | Core Framework | Next.js | 15.1.6 |
|  |  | React | 18.3.1 |
|  | State Management | Zustand (Client) | 5.0.3 |
|  |  | React Query (Server) | 5.65.1 |
|  | UI/UX | Radix UI | - |
|  |  | Tailwind CSS | 3.4.1 |
|  |  | Lucide React | 0.474.0 |
|  | Form Handling | React Hook Form | 7.54.2 |
|  |  | Zod Validation | 3.24.1 |
|  | API Communication | Axios | 1.7.9 |
|  | Development Tools | TypeScript | 5 |
|  |  | ESLint | 8.57.1 |
|  |  | Prettier | - |
| **Backend** | Core Platform | Spring Boot | 3.2.0 |
|  |  | Java | 17 |
|  | Security | Spring Security | - |
|  |  | JWT (JJWT) | 0.11.5 |
|  |  | OAuth2 Client | - |
|  | Data Access | Spring Data JPA | - |
|  |  | Spring Data JDBC | - |
|  |  | Spring Validation | - |
|  | API Documentation | Swagger/OpenAPI | 2.1.0 |
|  | Utility | Lombok | - |
|  |  | Logback | - |
| **Infrastructure** | Hosting | GitHub Pages (FE) | - |
|  |  | AWS EC2 (BE) | - |
|  | Database | AWS RDS | - |
|  |  | MySQL | - |
|  | Network | AWS Load Balancer | - |
|  |  | AWS Certificate Manager | - |
|  | Security | SSL/TLS | - |
|  |  | VPC | - |
| **Development** | Version Control | Git/GitHub | - |
|  | CI/CD | GitHub Actions | - |
|  | Monitoring | Spring Actuator | (예정) |

## 📁 프로젝트 구조

```
cheonyakplanet/
├── frontend/                 # Next.js 프론트엔드
│   ├── src/
│   │   ├── app/             # App Router 페이지
│   │   ├── components/      # UI 컴포넌트
│   │   ├── services/        # API 서비스 계층
│   │   ├── stores/          # Zustand 상태 관리
│   │   └── lib/             # 유틸리티 함수
│   └── package.json
├── backend/                  # Spring Boot 백엔드
│   ├── src/main/java/org/cheonyakplanet/be/
│   │   ├── application/     # 서비스 계층
│   │   ├── domain/          # 도메인 엔티티
│   │   ├── infrastructure/  # 외부 연동
│   │   └── presentation/    # 컨트롤러
│   └── build.gradle
└── docs/                    # 프로젝트 문서
```

## 🚀 시작하기

### 사전 요구사항
- Node.js 18+ (Frontend)
- Java 17+ (Backend)
- MySQL 8.0+
- Docker (선택사항)

### 로컬 개발 환경 설정

1. **저장소 클론**
```bash
git clone https://github.com/your-org/cheonyakplanet.git
cd cheonyakplanet
```

2. **백엔드 실행**
```bash
cd backend
./gradlew bootRun
```

3. **프론트엔드 실행**
```bash
cd frontend
npm install
npm run dev
```

4. **브라우저에서 확인**
- Frontend: http://localhost:3000
- Backend API: http://localhost:8082

### 환경 변수 설정

**Backend (application.yml)**
```yaml
spring:
  datasource:
    url: jdbc:mysql://${DB_URL}
    username: ${DB_USERNAME}
    password: ${DB_PASSWORD}
jwt:
  secret:
    key: ${JWT_SECRET}
```

**Frontend (.env.local)**
```env
NEXT_PUBLIC_API_URL=http://
NEXT_PUBLIC_KAKAO_MAP_KEY=
```

## 🧪 테스트

```bash
# Backend 테스트
cd backend
./gradlew test
./gradlew jacocoTestReport

# Frontend 테스트
cd frontend
npm run test
npm run test:coverage
```

## 📊 모니터링

- **Backend**: Spring Boot Actuator + Prometheus
- **Frontend**: Google Analytics + Naver Analytics
- **Coverage**: JaCoCo (Backend), Jest (Frontend)

### 커밋 메시지 규칙
- `Feat`: 새로운 기능
- `Fix`: 버그 수정
- `Refactor`: 코드 리팩토링
- `Test`: 테스트 관련
- `Docs`: 문서 변경
- `Build`: 빌드 시스템 변경


## 팀원
<table>
  <tr height="160px">
    <th align="center" width="140px">
      <a href="https://github.com/injulme"><img height="130px" width="130px" src="https://avatars.githubusercontent.com/u/54674430?v=4"/>
    </th>
    <th align="center" width="140px">
      <a href="https://github.com/Jungdaye89"><img height="130px" width="130px" src="https://avatars.githubusercontent.com/u/155501200?v=4"/></a>
    </th>
    <th align="center" width="140px">
      <a href="https://github.com/singingsandhill"><img height="130px" width="130px" src="https://avatars.githubusercontent.com/u/64348312?v=4"/></a>
    </th>
    <th align="center" width="140px">
      <a href="https://github.com/woo427"><img height="130px" width="130px" src="https://avatars.githubusercontent.com/u/170384966?v=4"/></a>
    </th>
  </tr>
  <tr>
    <td align="center" width="160px">
      <a href="https://github.com/injulme"><strong>정효진</strong></a>
    </td>
    <td align="center" width="160px">
      <a href="https://github.com/Jungdaye89"><strong>정다예</strong></a>
    </td>
    <td align="center" width="160px">
      <a href="https://github.com/singingsandhill"><strong>김지수</strong></a>
    </td>
    <td align="center" width="160px">
      <a href="https://github.com/woo427"><strong>김지우</strong></a>
    </td>
    
  </tr>
  <tr>
    <td align="center" width="160px">
      FE : 메인, 마이페이지, 청약정보
    </td>
    <td align="center" width="160px">
      BE : 마이페이지, 커뮤니티
    </td>
    <td align="center" width="160px">
      BE : 로그인, 모니터링, 청약정보
    </td>
    <td align="center" width="160px">
      FE : 로그인, 커뮤니티, 모니터링
    </td>
  </tr>
  <tr>
    <td align="center" width="160px">
       FE & UI/UX
    </td>
    <td align="center" width="160px">
       BE
    </td>
    <td align="center" width="160px">
       BE & DBA
    </td>
    <td align="center" width="160px">
       FE 
    </td>
  </tr>
</table>

## 📝 라이선스
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 문의

- 팀 이메일: cheonyakplanet@gmail.com
---

**청약플래닛**으로 더 스마트한 청약 정보를 경험해보세요! 🏠✨

