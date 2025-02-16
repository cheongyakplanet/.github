# 개요
&nbsp; **청약플래닛**은 청약 상품의 종합 가치를 간편하게 확인할 수 있는 서비스입니다.<br> 
***부동산 정보 플랫폼***&nbsp;으로 성장하여, 사람들이 부동산 정보에 스마트하게 접근할 수 있도록 지원하겠다는 비전을 갖고 있습니다.<br>

## 주요 기능
1. 청약일정 확인
2. 청약 상제 정보 확인
   * 주변 지도
   * 공급 유형 & 평수
   * 분양 가격     
4. 부동산 커뮤니티<br>

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

# 시스템 아키텍처
![시스템아키텍처 drawio](https://github.com/user-attachments/assets/53be214e-bfd5-4a3d-83e4-88fb1f4b013e)

# 기술 스택
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
