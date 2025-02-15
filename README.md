| 구분       | 기능        | 설명                    | URL                  |
|:---:|------------------|-----------------------|----------------------|
| 로그인 |    인증/인가   | JWT 기반 로그인         | `/auth/login`        |
|               | 계정찾기    | PW 재설정               | `/auth/login/find`   |
|               | 로그아웃    | JWT 삭제 및 세션 초기화  | `/auth/logout`       |
|               | JWT 토큰 갱신 | 자동 로그인 유지        |N/A (백엔드 처리)  |
| 관리자        | 사원관리   | 사원 조회               | `/admin/users`       |
|               |             | 사원 등록               | `/admin/add`         |
|               |             | 사원 정보수정           | `/admin/edit`        |
|               |             | 사원 삭제               | `/admin/delete`      |


|        | 세부 기능       | 설명                          | 개발 시 주의할 사항                                      |
|--------|-----------------|-----------------------------|------------------------------------------------------|
| `/auth/login` | 로그인폼        | 이메일/비밀번호 입력 후 로그인 | - JWT 토큰 저장 (LocalStorage 또는 HttpOnly Cookie) <br /> - 보안 강화를 위해 CORS 및 CSRF 설정 필요    |
|        | 로그인 상태 유지 | 로그인 유지 기능 (토큰 자동 갱신) | - 토큰이 만료되었을 때 자동 로그아웃 처리               |
|        | 계정찾기 <br /> `/auth/login/find`        | 비밀번호 재설정                | - 정보양식에 맞도록 유효성검사 처리                  |                      



