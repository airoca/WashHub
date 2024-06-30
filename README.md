### 개발환경

- Kotlin, Node.js, MySQL

# WashHub

기숙사 학생들을 위한 세탁기 관리 어플리케이션

---

![Main](https://github.com/cypsyco/MadFacility/assets/137145628/214fe22c-b3ed-4cd1-9e77-c7a1ee683ae9)

> 오늘 꼭 돌려야 할 빨래가 있지만, 공용 세탁기 자리가 없었던 경험 있으신가요? WashHub는 기숙사에서 지내는 학생들이 실시간으로 세탁기 사용 현황을 확인하고, 예약할 수 있도록 하는 서비스입니다.
> 

---

## PROJECT DESCRIPTION

1. **SPLASH ACTIVITY**
    
    > **어플리케이션 로딩 애니메이션**
    > 
    
    <div align="center">
        <img src="https://github.com/cypsyco/MadFacility/assets/137145628/33f9357b-d7dc-419e-b6dd-64b545c165c0" width="300" alt="splash">
    </div>
    
    어플리케이션을 처음 실행할 경우, 위와 같이 로딩 화면이 생성됩니다.
    
    Splash 애니메이션은 After Effect를 통해 구현되었습니다.
    
---
    
2. **로그인 & 회원 가입** 
    
    > **Server와 DB 기반 로그인, 회원 가입 기능**
    > 
    
    <div align="center">
        <img src="https://github.com/airoca/WH/assets/137145628/820a31e3-8e71-4a08-961f-9b1f9beb923f" width="300" alt="로그인 화면">
    </div>
    
    Node.js Server와 MySQL DB를 기반으로 회원 정보를 저장하고, 불러오는 부분입니다.
    
    <div align="center">
        <img src="https://github.com/airoca/WH/assets/137145628/86484c8e-adbf-487a-99b1-0e834a8914cf" width="300" alt="회원 가입 화면">
    </div>
    
    **회원 가입 기본 기능**
    
    - 프로필 사진을 클릭하면, 갤러리에서 프로필 사진 선택 가능
    - 모든 필드를 입력해야 회원 가입 가능
    
    **회원 가입 추가 기능**
    
    - ID 중복 확인 (모든 필드를 입력하고, 중복 확인도 성공해야 가입 가능)
    - Password 노출/가리기
    - 성별에 따라 선택할 수 있는 기숙사를 다르게 설정
    
---
    
3. **세탁기 & 건조기 선택 화면**
    
    > **(성별에 따라) 세탁기를 이용할 기숙사 선택 가능**
    > 
    
    <div align="center">
        <img src="https://github.com/airoca/WH/assets/137145628/c4c77340-fa6d-4053-b497-52eb5f0b0bc8" width="300" alt="세탁기 & 건조기 선택 화면">
    </div>
    
    로그인이 성공하면, 세탁기를 선택할 수 있는 화면으로 이동하게 됩니다.
    
    상단 메뉴를 확인하면, 좌측에는 프로필 보기 버튼, 우측에는 기숙사 옵션 메뉴 버튼을 확인할 수 있습니다.

    날씨는 기본적으로 수원의 날씨를 나타내도록 구현되었습니다.
    
    세탁기 버튼은 현재 기숙사에서 이용 가능한 개수를 표시해주고 있습니다.
    
    기숙사 선택 화면은 기본적으로 사용자의 기숙사로 설정되어 있는데, 옵션 메뉴를 클릭하여 다른 기숙사의 현황도 볼 수 있습니다. 이 경우, 사용자의 성별에 따라 같은 성별의 기숙사만 선택할 수 있도록 메뉴를 구성하였습니다.
    
---

4. **세탁기 선택 화면**
    
    > **사용 가능, 사용 중, 예약 중, 수리 중 현황 공유**
    > 
    
    <div align="center">
        <img src="https://github.com/airoca/WH/assets/137145628/3371f8af-8772-417b-a4d1-942e1be44ea1" width="300" alt="세탁기 선택 화면">
    </div>
    
    세탁기 선택 화면에서는 현재 세탁기의 현황을 확인한 후, 세탁기를 사용, 혹은 예약할 수 있습니다.
    
    **세탁기 상태**
    
    - **사용 가능:** 즉시 사용이 가능합니다.
    - **사용 중:** 해당 세탁기가 사용 중입니다. 예약을 추가할 수 있습니다.
    - **예약 중:** 해당 세탁기가 사용 중이지 않지만, 예약되어 있습니다. 이 경우에도 예약을 추가할 수 있습니다.
    - **수리 중:** 해당 세탁기가 수리 중으로, 사용할 수 없습니다.  

---

5. **시간 설정 화면**

    <div align="center">
        <img src="https://github.com/airoca/WH/assets/137145628/9f9cff64-5d3b-496a-955e-5a71669311bf" width="300" alt="시간 설정 화면">
    </div>
    
    “사용 가능” 세탁기를 선택하면 시간 설정 화면으로 이동하게 됩니다.
    
    사용할 시간을 설정한 이후, “사용 시작” 버튼을 누르면 세탁기 사용이 시작되고, 세탁기 선택 화면으로 이동하게 됩니다. 세탁기 선택 화면에서는 세탁이 완료될 때까지 남은 시간을 실시간으로 확인할 수 있습니다.
    
    <div align="center">
        <img src="https://github.com/airoca/WH/assets/137145628/193db641-7bc6-452d-a4f5-08fce17b271a" width="300" alt="세탁기 선택 화면 (세탁기 사용 시작 이후)">
    </div>
    
---

6. **예약 화면**
    
    <div align="center">
        <img src="https://github.com/airoca/WH/assets/137145628/ebb161e7-0300-426b-a154-8c80e132081c" width="300" alt="예약 화면">
    </div>
    
    “사용 중” 또는 “예약 중” 세탁기를 선택하면 예약 추가 화면으로 이동하게 됩니다.
    
    예약 화면에서는 현재 해당 세탁기를 예약한 사람들의 명단이 보이게 됩니다.
    
    “+” 버튼을 누르면, 예약 명단에 사용자가 추가되고, 해당 세탁기를 예약할 수 있습니다.
    
    예약한 시간에 따라 예약 순위가 자동으로 설정됩니다.
    
    사용 중이거나, 예약 중인 세탁기의 현황은 이후 설명될 프로필 화면에서 확인할 수 있습니다.
    
---

7. **프로필 화면**
    
    <div align="center">
        <img src="https://github.com/airoca/WH/assets/137145628/c678f75b-b080-4d4b-8db5-0d01f0e23d7e" width="300" alt="프로필 화면">
    </div>
    
    로그인 이후, 상단 메뉴의 좌측 버튼을 누르면 프로필 화면으로 이동할 수 있습니다.
    
    해당 화면에서는 4가지 메뉴로 이동할 수 있습니다.
    
    - 시설물: 로그인 이후 초기 화면인, 세탁기 & 건조기 화면으로 이동합니다.
    - 사용 중: 현재 사용 중인 세탁기의 현황을 확인합니다.
    - 예약 중: 현재 예약 중인 세탁기의 현황을 확인합니다.
    - 연필 버튼: 사용자의 프로필을 수정할 수 있는 수정 화면으로 이동합니다.
    
    하단에는 로그아웃 버튼이 위치해 있습니다.
    
---

8. **프로필 메뉴 - 사용 중인 세탁기**
    
    <div align="center">
        <img src="https://github.com/airoca/WH/assets/137145628/48f07dcc-9280-4f94-a399-26316fd99e6c" width="300" alt="사용 중인 세탁기 화면">
    </div>
    
    프로필 메뉴에서 사용 중인 세탁기로 이동하면, 현재 사용자가 사용하고 있는 세탁기의 현황을 실시간으로 확인할 수 있습니다.
    
    세탁이 종료될 때까지 남은 시간을 확인할 수 있습니다.
    
---

9. **프로필 메뉴 - 예약 중인 세탁기**
    
    <div align="center">
        <img src="https://github.com/airoca/WH/assets/137145628/41c5738b-3846-45b9-a692-fdef19466139" width="300" alt="예약 중인 세탁기 화면">
    </div>
    
    프로필 메뉴에서 예약 중인 세탁기로 이동하면, 현재 사용자가 예약하고 있는 세탁기의 현황을 실시간으로 확인할 수 있습니다.
    
    해당 세탁기의 현재 사용이 종료될 때까지 남은 시간을 확인할 수 있고, 사용자 본인의 예약 순번을 확인할 수 있습니다.
    
    사용자의 예약 순번이 1인 상태에서 세탁기 사용이 종료되면, 화면이 슬라이드 형식으로 바뀌게 되면서 아래와 같은 창이 나오게 됩니다.

    <div align="center">
    <img src="https://github.com/airoca/WH/assets/137145628/90c6f4f9-4fef-4be7-b183-7182da7017b5" width="300" alt="예약 알림 동영상">
    </div>
    
    해당 창에서 “사용 시작” 버튼을 누르면, 즉시 시간 선택 화면으로 이동하게 되고, 바로 세탁기 사용을 시작할 수 있습니다.
    
---

10. **프로필 메뉴 - 프로필 정보 수정**
    
    <div align="center">
        <img src="https://github.com/airoca/WH/assets/137145628/a26c2a20-edb6-4e48-a08d-85302af16b4f" width="300" alt="회원 정보 수정 화면">
    </div>

    <회원 정보 수정 화면>
    
    프로필 메뉴에서 회원 정보 수정 화면으로 이동하면, 사용자의 정보를 수정할 수 있습니다.
    
    기본적으로 사용자의 ID와 성별은 변경할 수 없고, 사진, 이름, 비밀번호, 그리고 기숙사를 변경할 수 있습니다.
    
    회원 정보를 수정할 경우, 기존 비밀번호를 입력해야 합니다. 만약 기존 비밀번호를 맞게 입력하지 않으면, 회원 정보 수정이 거부됩니다.