## **1. 데모 영상**

![(https://ifh.cc/g/p0k9dY.jpg)]

👉 [영상 보러가기](https://ifh.cc/v/oppC60.mp4)

## **2. 프로젝트 소개**

- [마이라얼트립](https://www.myrealtrip.com/) 사이트 클론 프로젝트
- '국내 숙소' 카테고리를 한정으로 구현하였습니다.
- 배경으로 video태그를 사용하여 동영상 효과를 구현하였습니다.
- querystring을 이용해 필터링기능을 구현하였습니다.
- react library를 사용해 컴포넌트 형태로 다양한 기능(모달창, slider, carousel, calendar, rate 등)을 구현하였습니다.
- 카카오 API를 통한 소셜로그인 기능을 구현하였습니다.

### **1) 프로젝트 선정이유**

- 세세한 기능이 많은 사이트이다.
- 다양한 UI, 기능, 통신 등을 구현할 수 있어 성장에 도움이 될 것이라고 판단했다.

### **2) 개발 인원 및 기간**

- 개발기간 : 2022/07/04 ~ 2022/07/15
- 개발 인원

  - 프론트엔드(4명) : 김인태, 정현준, 조예지 , 장류광
  - 백엔드(2명) : 박민하, 정진관

- 담당파트
  - 김인태 : 로그인 회원가입 / 장바구니
  - 정현준 : 상세페이지
  - 조예지 : 검색 리스트 페이지
  - 장류광 : Nav / footer / Main 페이지
- [백엔드 github 링크](https://github.com/wecode-bootcamp-korea/34-2nd-Fake-Trip-backend)

## **3. 적용 기술 및 구현 기능**

### **적용 기술**

- Front-End : HTML, Styled-component, Javascript , React , React Router, Slider, Carousel, antd, axios, Rangepicker, calender, dropdown

### **구현 기능**

[Login]
- 카카오톡 로그인을 구현했습니다. 전 프로젝트와 공통되는 부분은 제거했습니다. (회원가입을 이메일로 하는 것)
- ![kakao원리](https://user-images.githubusercontent.com/62875596/179350634-e15adbd0-8819-4d91-b1a6-3a79ef449a3c.PNG)
- 원리는 이러합니다. 저희 팀은 Rest API를 사용해서 만들었습니다. axios를 이용한 통신을 했고, 카카오에서 발급하는 토큰을 가지고, 백엔드에 전달했을 떄 백엔드의
서비스 토큰을 받아서 회원이 되었을 때 기능들을 사용할 수 있게 하였습니다.
- 개인정보 유출을 방지하기위해서 .env 파일을 만들어서 APIKEY들을 관리했습니다.
![인태님로그인](https://user-images.githubusercontent.com/62875596/179350913-ec2797de-12d2-47ea-b51c-199414b662ef.gif)

[Booking]
- new Date 함수를 사용해서 몇박인지 계산해서 렌더링했습니다.
- 결제화면 전에 있는 URL을 가져오기 위해서 location.search 메소드를 사용했습니다.
- 결제할 때는 토큰이 필요하기 때문에 fetch할 때 헤더에 토큰을 담아줬습니다.
- 핸드폰 번호만 입력할 수 잇게 해놓은 이유는 카카오로 로그인 할 떄 받을 정보를 정할 수 있는데 핸드폰 번호는 얻을 수 없기 때문에
입력하는 칸을 만들었고 method PATCH로 백엔드 데이터에 접근해 등록해줬습니다.
- 결제 버튼을 누를 때도 마찬가지로 헤더에 토큰을 담아줬고 body에 정보들을 담아서 보내줬습니다.

![인태님예약화면](https://user-images.githubusercontent.com/62875596/179351279-9c0e212f-27b9-4c9b-a6a6-8f90c06a7818.gif)

### **아쉬웠던 점**
- 기한 날짜까지 완벽했다고 생각했는데 자꾸 우리쪽 서비스 토큰이 담기지 않아서 발급된 토큰을 넣어서 썼던 것이 아쉬웠습니다.
- 결제버튼을 누르면 user의 크레딧이 깎여야하는데 정보수정이 제대로 안되어서 아쉬웠습니다.
- 다른 소셜로그인(네이버, 구글등), 여타 추가기능을 시간상 구현 못한 것이 아쉬웠습니다.
- 새로운 hooks를 써보고 싶었는데 크게 필요한 부분이 없었던 것이 아쉬웠습니다.

## **Reference**

- 이 프로젝트는 [마이리얼트립](https://www.myrealtrip.com/) 사이트를 참조하여 학습 목적으로 만들었습니다.
- 실무수준의 프로젝트이지만 학습용으로 만들었기 때문에 이 코드를 활용하여 이득을 취하거나 무단 배포할 경우 법적으로 문제될 수 있습니다.
