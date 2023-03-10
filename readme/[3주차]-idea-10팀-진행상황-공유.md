# Woowahan Recipe / 10팀 진행 상황 공유

## 👨‍👦‍👦팀 구성원, 개인 별 역할

### 개발 역할 분담

- 허진혁 (PM) : 팀원 역할 분담, 로그인과 비로그인 화면 구분, 로그인 인증(세션 활용), 유저 마이페이지
- 김응준 (CTO) : 레시피 재료등록기능 구현, 상세페이지에서 레시피에 해당하는 재료 출력
- 이소영 (Infra) : NGINGX 및 SSL 적용, S3 적용, 장바구니 UI, 판매자 Entity&Repository 수정
- 이다온 (기획) : 레시피 UI, 레시피 검색기능 적용, 페이징처리,  레시피 수정페이지 정보 출력, 재료 삭제
- 김미지 (개발) : 마이페이지 내가 쓴 리뷰 조회, 수정, 삭제 UI, 판매자 API
- 이수진 (개발) : 상품 CRUD와 검색 UI, 페이징 처리, 장바구니 버튼 연결, 이미지 업로드 기능

<br />

## 🔊팀 내부 회의 진행 회차 및 일자

- 1회 차(2023.01.30) Discord 회의 및 개발 진행
- 2회 차(2023.01.31) Discord 회의 및 개발 진행
- 3회 차(2023.02.01) Discord 회의 및 개발 진행
- 4회 차(2023.02.02) Discord 회의 및 개발 진행
- 5회 차(2023.02.03) Discord 회의 및 개발 진행

<br />

## 💻현재까지 개발 과정 요약

------

- 허진혁
  
  - 타임리프의 스프링 시큐리티를 활용하여 비로그인과 로그인이 볼 수 있는 부분을 다르게 할 수 있고, 더 나아가 역할에 따라 화면에 띄어지는 부분을 다르게 할 수 있다는 것을 배웠습니다.
  - Spring data jpa을 통한 페이징 처리를 더 많이 배우게 되었습니다.
  - queryDsl을 통해 동적 쿼리를 만들어 보면서, sql에 대한 이해가 많이 부족함을 깨달았습니다.
  - 수정 페이지에 들어갈 때, 이전에 있던 정보를 가져오는 방식을 알게 되었습니다.
  - 토큰을 저장하는 곳을 쿠키, 세션 웹스토리지(로컬스토리지, 세션스토리지)에 하는 것을 알게 되었고, 세션에 저장하는 방식으로 하였습니다.
- 김응준

  - List<String> 형식으로 도착하는 요청에 대한 처리를 할 수 있게 되었습니다.
  - N:N 매핑을 완전히 이해할 수 있게 되었습니다. 1:N - N:1 에서 1에서 반대편 1의 값을 어떻게 가져오는지 구조를 알게 되었습니다.
  - jpa의 기능에대해 한단계 더 깊게 이해할 수 있게 되었습니다.
  - 테스트코드를 이해하고 작성하는 실력이 늘었습니다.
  - Html과 js에 대해 아예 몰랐는데 트리 구조라는걸 알게 되었고 어느정도 메서드를 작성하고 변수를 가져오고 내보내는 방법을 배웠습니다.

- 이소영

  - NGINX 와 SSL 에 대해 많이 학습하는 시간을 갖게 된 것 같습니다. 지난번에 NGINX와 SSL 적용 후 502 에러가 발생하여 NGINX 적용을 다음 주에 다시 도전할 예정입니다.

    👉 docker-compose.yml을 새롭게 알게 되어 해당 방법으로 진행할 예정입니다.

  - 장바구니 기능을 클라이언트와 서버를 연결하는 과정에서 사용자의 관점에서 다시 생각해보게 되었고, 응답 시 필요 없다고 생각했던 데이터들에 대해 프론트 개발자의 관점에서도 생각해보는 시간을 가졌습니다.

  - Thymeleaf 와 JavaScript 모두 익숙치 않아 이를 이용한 프론트에서의 기능 개발에 조금 어려움을 겪고 있습니다.

- 이다온

  - 3주차는 화면 만들기를 집중적으로 많이 구현한 시간이었는데 화면에 데이터 뿌려주기 위해 Thymleaf의 문법에 대해서 알아가는 시간을 갖게 된 것 같습니다.
  - 화면에서 버튼을 눌러 삭제를 할 때에 JavaScript를 이용하여 삭제를 구현할 수 있게 되었습니다.
  - 수정 페이지에서 이전에 있던 정보를 가져오는 원리를 이해하고 처리를 할 수 있게 되었습니다.
  - 페이징처리를 하면서 조건에 따라 disabled를 구현하는 방법을 알게되었습니다.
  - 레시피 검색하는 기능을 구현하면서 repository에서 Query를 짜서 구분해내는 방법을 알게되었습니다.
  - 화면을 움직이기 위해서는 JavaScript와 jQuery가 필요해서 필요할 때마다 검색을 해서 조금씩 배우고 있지만 시간이 많이 걸려 어려움이 많은 것 같습니다.
  - 현재는 재료 등록이 이루어진 후 상세페이지에서 출력하는 과정에서 어려움이 많아 재료 등록과 관련되어있는 기능 구현에 진행중에 있습니다.

- 김미지

  - 페이지를 만들면서 처음에 가져오려고 했던 데이터가 필요 없거나 새로 필요한 데이터가 있다는 것을 발견하고 dto를 수정했습니다. 프론트와 백엔드 개발자와의 소통이 필요하다는 것을 다시 한번 느꼈습니다.
  - 사용자가 페이지에서 입력한 데이터를 db에 반영하는 방법을 배웠습니다.
  - Javascript가 익숙하지 않아 어려움을 격고 있지만 만들어 놓은 페이지에 기능들을 좀 더 추가하고 싶습니다.

- 이수진

  - 이번주에는 화면 구현 위주로 개발을 진행했습니다. 백엔드 입장에서 request/response dto를 만들어서 api 테스트를 진행했는데, 프론트엔드 개발을 하다보니 더 필요하거나 필요없어진 데이터들이 있었습니다. 또 화면을 만들 때에도 백단에서 만든 서비스 로직에 대한 이해가 필요하다는 것을 깨닫게 되었습니다. 이런 점들에서 프론트엔드와 백엔드가 어떤 소통을 해야하는지를 배웠습니다.
  - 상품을 장바구니에 넣을 때, 장바구니 버튼 없이 +, - 버튼으로 바로 담기는 기능을 구현하고 싶었는데 구현이 잘 되지 않아 시간을 많이 소비하게 되었습니다. 팀원들과 멘토님과 상의해본 결과 ajax와 같은 비동기 통신을 이용해야 해서 우선은 장바구니 버튼을 만들어서 구현을 진행하기로 결정했습니다. 처음 계획한대로 구현하지 못해서 아쉽지만 시간이 된다면 다시 도전해보고 싶습니다.
  - Thymeleaf에도 security가 있다는 것을 알게 되었고, 화면을 구현하면서 html, css, java script 기초 문법을 배웠습니다.

<br />

## ❓ 개발 과정에서 나왔던 질문 (⬜ 미해결, ✅ 해결완료)

------

✅ 회원 정보 수정, 레시피 수정 등 수정을 할 때, 이전에 있던 정보를 가져와서 화면에 띄우고 그 다음에 수정이 가능하게 하는 방법

✅  페이징 처리를 할 때 페이지가 1번이면 이전 버튼을 못 누르게 하고, 페이지가 마지막 페이지이면 다음버튼 못누르게 하기

✅  로그인과 비로그인시 보여줘야 할 버튼들을 분리하는 방법

⬜  docker-compose.yml의 위치와 사용 방법

<br />

## 📲개발 결과물 공유

------

- Gitlab Repository URL: https://gitlab.com/th42500/woowahan_recipe_team10.git
- Swagger URL: http://ec2-43-201-26-38.ap-northeast-2.compute.amazonaws.com:8080/swagger-ui/
- EC2 URL: http://ec2-43-201-26-38.ap-northeast-2.compute.amazonaws.com:8080/
- Team Notion URL : https://www.notion.so/23-01-13-23-02-16-12ddd64750ad46a0b1547e64ab6fbf5c

![image(1)](./assets/image.png)
