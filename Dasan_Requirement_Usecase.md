## Requirement - Use Case 매핑표

| No. | Requirement | Use Case(s) |
|----|----------------------------------|----------------------------|
| 1  | 사용자는 ID/PW로 로그인하여 시스템에 접속할 수 있어야 한다. | Login |
| 2  | 사용자는 로그아웃하여 시스템 접속을 종료할 수 있어야 한다. | Logout |
| 3  | 회원은 ID, PW, 전화번호, 결제수단, 선호 자전거 유형을 입력하여 회원 가입 할 수 있어야 한다. | Register Member |
| 4  | 회원이 회원 탈퇴를 요청하면 모든 권한, 데이터를 삭제해야 한다. | Delete Member |
| 5  | 관리자는 대여소 이름, 위치, 보관수량, 운영시간을 입력하여 대여소를 등록할 수 있어야 한다. | Register Station |
| 6  | 관리자는 대여소 조회 및 상세정보 확인을 할 수 있어야 한다. | View Station |
| 7  | 관리자는 등록된 대여소를 삭제할 수 있어야 한다. | Delete Station |
| 8  | 관리자는 자전거 ID, 제품명, 유형, 소속 대여소, 상태 등을 입력하여 자전거 등록을 할 수 있어야 한다. | Register Bicycle |
| 9  | 관리자는 등록된 자전거를 조회, 상세 확인할 수 있어야 한다. | View Bicycle |
| 10 | 관리자는 등록된 자전거를 삭제할 수 있어야 한다. | Delete Bicycle |
| 11 | 회원은 대여소 이름을 입력하여 대여소 검색을 할 수 있어야 한다. | Search Station |
| 12 | 회원은 특정 대여소를 선택하여 상세정보화면을 볼 수 있어야 한다. | View Detail Station |
| 13 | 대여 가능한 자전거가 있으면 즉시 자전거 대여를 할 수 있어야 한다. | Rent Bicycle |
| 14 | 자전거가 없을 때 예약대기 신청을 할 수 있어야 한다. | Rent Reserve Bicycle |
| 15 | 회원은 현재 대여 중인 자전거를 대여 정보 조회 할 수 있어야 한다. | View Current Rentals |
| 16 | 회원은 선택한 자전거를 지정 대여소에 반납 할 수 있어야 한다. | Return Bicycle |
| 17 | 회원은 자신의 예약대기 조회를 할 수 있어야 한다. | View Rent Reservation |
| 18 | 회원은 자신의 예약대기 취소를 할 수 있어야 한다. | Cancel Rent Reservation |
| 19 | 자전거 반납 직후, 회원은 위치 기반 외부 식당 예약 서비스 연계 를 선택할 수 있어야 한다. | Book Restaurant |



## Actor - Description 매핑표

| Actor | Description |
|-------|-------------|
| **User** | Member 및 Administrator의 상위 액터. 로그인/로그아웃 등 공통 기능을 갖는 모든 이용자. |
| **Member** | 자전거 렌탈 서비스에 가입한 일반 회원. 자전거 검색, 대여, 반납, 예약 등의 기능을 사용한다. |
| **Administrator** | 자전거 렌탈 서비스 운영 담당자. 대여소, 자전거를 관리하며 회원보다 높은 권한을 가진다. |
| **E-mail System** | 자전거 렌트, 예약대기, 반납 시 이메일을 사용자에게 전송하는 외부 시스템. |

![Image](https://github.com/user-attachments/assets/f7972d36-1dfb-4a49-a941-cdec6522606f)
