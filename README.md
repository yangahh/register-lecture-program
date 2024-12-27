### 같은 사용자가 동일한 특강에 대해 신청 성공하지 못하도록 하는 기능 설계 및 구현

1. DB에서 제어 
   - DB에서 특강 신청 테이블에 사용자 ID와 특강 ID를 multiple unique key로 설정하여 DB 레벨에서 제어   
   - ![image](https://github.com/user-attachments/assets/c51c652d-7947-475e-b656-fb8fa9bd9844)
2. 애플리케이션에서 제어
   - 도메인 서비스 계층에서 비즈니스 로직으로 제어
   - 특강 신청 테이블에서 사용자 ID로 특강 ID를 조회하여 이미 신청한 특강이 있는지 확인하고, 있으면 예외를 발생시키는 방식으로 제어
   - ![image](https://github.com/user-attachments/assets/e06b423d-a9f4-40c9-be3e-f13dade75ade)
   - <img width="819" alt="image" src="https://github.com/user-attachments/assets/43392af4-e779-4786-af16-db4b4f848e0f" />

