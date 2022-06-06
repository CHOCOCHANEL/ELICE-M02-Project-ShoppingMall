# ELICE-M02-Project-ShoppingMall
Personal Project using learning materials such as HTML5, CSS3, JavaScript, NodeJS, MongoDB etc during the last 2 months in Elice. <br />
Search for Products, Add to Shopping Cart, and Order New Product in this shopping mall Web Service. <br />
<br>

## Backend API Description

쇼핑몰 웹 서비스를 구현하기 위해서 백엔드 작업을 진행했습니다.
>- 다음 5가지 API가 존재합니다.
>- 각 API는 CRUD를 지원하며, 관리자 모드와 일반 유저 모드가 분리되어 있습니다.

API의 설명은 다음과 같습니다.
* Category API
>- 카테고리는 상품을 분류합니다.
>- 상품을 분류하는 카테고리에 대한 CRUD를 지원합니다.
>- Read를 제외하고, 관리자만 접근 가능합니다.
>- 일반 유저(basic-user)는 카테고리 조회만 가능합니다.

* Item API
>- 주문된 상품의 CRUD를 지원합니다.
>- Item API는 주문과 장바구니에 활용될 수 있습니다.
>- 주문 정보와 상품 정보를 참조(populate)합니다.

* Order API
>- 상품 주문에 대한 CRUD를 지원합니다.
>- Order API는 주문한 유저의 아이디와 주문 정보와 배송 상태 등을 담고 있습니다.

* Product API
>- 상품 정보에 대한 CRUD를 지원합니다.
>- 판매될 상품을 등록합니다.
>- 일반 유저(basic-user)도 판매자가 될 수 있습니다.
>- 추후 기능 업데이트를 통해, 판매자 권한을 부여할 수 있습니다.

* User API
>- 회원 관리의 CRUD를 지원합니다.
>- 모든 회원에 대한 접근은 관리자(admin)만 가능합니다.
>- 회원가입, 로그인, 회원정보수정, 회원탈퇴 등을 지원합니다.


API 문서는 [다음](https://documenter.getpostman.com/view/20944788/Uz5Gmuyh)을 참조하십시오. <br />
* 보다 상세한 설명과 예시 코드 및 DB 데이터 스키마 등을 확인할 수 있습니다.


## 주요 기능 설명
1. 회원가입, 로그인, 회원정보 수정 등 **유저 정보 관련 CRUD** 
2. **제품 목록**을 조회 및, **제품 상세 정보**를 조회 가능함. 
3. 장바구니에 제품을 추가할 수 있으며, **장바구니에서 CRUD** 작업이 가능함.
4. 장바구니는 서버 DB가 아닌, 프론트 단에서 저장 및 관리됨 (sessionStorage)
5. 장바구니에서 주문을 진행하며, **주문 완료 후 조회 및 삭제**가 가능함.

## 주요 사용 기술

### 1. 프론트엔드

- **Vanilla javascript**, html, css (**Bulma css**)
- Font-awesome 
- Daum 도로명 주소 api 
- 이외

### 2. 백엔드 

- **Express** (nodemon, babel-node로 실행됩니다.)
- Mongodb, Mongoose
- cors
- 이외

## 폴더 구조
- 프론트: `src/views` 폴더 
- 백: src/views 이외 폴더 전체
- 실행: **프론트, 백 동시에, express로 실행**



## 설치 방법

1. **.env 파일 설정 (MONGODB_URL 환경변수를, 개인 로컬 혹은 Atlas 서버 URL로 설정해야 함)**

2. express 실행

```bash
# npm 을 쓰는 경우 
npm install
npm run start

# yarn 을 쓰는 경우
yarn
yarn start
```

<br>

---

본 프로젝트에서 제공하는 모든 코드 등의는 저작권법에 의해 보호받는 ㈜엘리스의 자산이며, 무단 사용 및 도용, 복제 및 배포를 금합니다.
Copyright 2022 엘리스 Inc. All rights reserved.
