|카테고리|기능|메소드|엔드포인트|요청 바디|성공시 응답|
|---|---|---|---|---|---|
|조회|전체 상품 조회|Get|/product|X|{id: productid: category: sellerinfo: price: stock: ...}|
|조회|특정 상품 조회|Get|/product/:uid|X|{id: productid:uid category: sellerinfo: price: stock:}|
|조회|장바구니 조회|Get|/cart/:uid|X|{userid : uid productid : }|
|생성|상품 등록|Post|/product|{category : sellerinfo : price : stock : }|201|
|수정|상품 정보 수정|Post|/product/:pid|{productid : pid category : [수정사항] sellerinfo :[수정사항] price :[수정사항] stock :[수정사항] }|{Ok}|
|삭제|특정 상품 삭제|Delete|/product|{productid}|200|
|수정|장바구니에 있는 특정상품에 대한 수량이 변경|Post|/cart|put /mylistt?=userid {productid : ordercount : }|res code(201)header(’Content-type’, ‘application/json’)send(|
|조회|구매내역 조회|Get|/purchaselist/userid|Get /mylist?=purchaselist/userid|res.code(200).header(’Content-type’, ‘application/json’, ‘Content-encoding’, ‘gzip’)).send({purchaselist})|
|생성|구매리뷰를 작성|Post|/review?=productid/{userid}|Post{content : “     “}|res .code(201) |

