@startuml

left to right direction
skinparam packageStyle rectangle

' 슈퍼 액터 정의
actor "사용자" as User

' 사용자 상속 액터
actor "회원" as Member
actor "관리자" as Admin

' 외부 액터
actor "문자 알림 서비스" as SMSService
actor "이메일 알림 서비스" as EmailService
actor "식당 예약 서비스" as RestaurantService

' 상속 관계 설정
User <|-- Member
User <|-- Admin

rectangle "공유 자전거 대여 시스템" {
    ' 회원 관련 유스케이스
    usecase "회원 가입" as UC1
    usecase "회원 탈퇴" as UC2
    usecase "로그인" as UC3
    usecase "로그아웃" as UC4
    
    ' 대여소 관련 유스케이스
    usecase "대여소 등록" as UC5
    usecase "대여소 조회" as UC6
    usecase "대여소 삭제" as UC7
    usecase "대여소 검색" as UC8
    usecase "대여소 상세정보 조회" as UC9
    
    ' 자전거 관련 유스케이스
    usecase "자전거 등록" as UC10
    usecase "자전거 조회" as UC11
    usecase "자전거 삭제" as UC12
    usecase "자전거 즉시대여" as UC13
    usecase "자전거 예약대기" as UC14
    usecase "자전거 대여정보 조회" as UC15
    usecase "자전거 예약대기정보 조회" as UC16
    usecase "자전거 예약대기 취소" as UC17
    usecase "자전거 반납" as UC18
    
    ' 알림 관련 유스케이스
    usecase "문자 알림 전송" as UC19
    usecase "이메일 알림 전송" as UC20
    
    ' 외부 서비스 연계
    usecase "근처 식당 예약 서비스 연결" as UC21
    
    ' 사용자와 유스케이스 연결
    User --> UC3
    User --> UC4
    
    ' 회원과 유스케이스 연결
    Member --> UC1
    Member --> UC2
    Member --> UC8
    Member --> UC9
    Member --> UC13
    Member --> UC14
    Member --> UC15
    Member --> UC16
    Member --> UC17
    Member --> UC18
    
    ' 관리자와 유스케이스 연결
    Admin --> UC5
    Admin --> UC6
    Admin --> UC7
    Admin --> UC10
    Admin --> UC11
    Admin --> UC12
    
    ' 외부 서비스와 유스케이스 연결
    UC19 --> SMSService
    UC20 --> EmailService
    UC21 --> RestaurantService
    
    ' 유스케이스 간의 관계
    UC13 ..> UC19 : <<include>>
    UC14 ..> UC19 : <<include>>
    UC18 ..> UC20 : <<include>>
    UC15 <.. UC18 : <<extend>>
    UC18 ..> UC21 : <<extend>>
}

@enduml




![Image](https://github.com/user-attachments/assets/7edd5efc-2f62-4ebe-bf63-ceb970a12193)
