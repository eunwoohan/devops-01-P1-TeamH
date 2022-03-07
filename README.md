# Project-01-H [Project Link](https://grave-slug-ebc.notion.site/PROJECT-H-96d6ecc1f038467a9fcc30d956a9d101)
목표 : 쇼핑몰 구현


## 사용가능한 API 목록
1. 전체 상품조회 
2. 특정 상품조회
3. 상품 등록
4. 상품 삭제
5. 상품 내용 수정
## API디자인
|카테고리|기능|메소드|엔드포인트|요청 바디|성공시 응답|
|---|---|---|---|---|---|
|조회|전체 상품 조회|Get|/product|X|{id: productid: category: sellerinfo: price: stock: ...}|
|조회|특정 상품 조회|Get|/product/:uid|X|{id: productid:uid category: sellerinfo: price: stock:}|
|조회|장바구니 조회|Get|/cart/:uid|X|{userid : uid productid : }|
|생성|상품 등록|Post|/product|{category : sellerinfo : price : stock : }|201|
|수정|상품 정보 수정|Post|/product/:pid|{productid : pid category : [수정사항] sellerinfo :[수정사항] price :[수정사항] stock :[수정사항] }|{Ok}|
|삭제|특정 상품 삭제|Delete|/product|{productid}|200|
| | | | | | |
| | | | | | |
| | | | | | |
| | | | | | |
## .env
dotenv를 사용하여 환경값으로 DB연결을 할것이기 때문에 
"ENDPOINT" 부분에 사용할 DB값을 주어야한다.

## npm run dev
To start the app in dev mode
Open Http://localhost:3000 to view it in the browser.

## npm start
To start production mode.

## npm run test
To start test cases.
## 개발환경
Fastify-cli
node v 16
npm
mongodb

## ERD
![image](https://user-images.githubusercontent.com/62275129/157042882-3ba8faa3-33a3-4777-b825-50ef7fc591a2.png)
