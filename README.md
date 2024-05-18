# 키친포스

## 퀵 스타트

```sh
cd docker
docker compose -p kitchenpos up -d
```

## 요구 사항

### 상품

- 상품을 등록할 수 있다.
- 상품의 가격이 올바르지 않으면 등록할 수 없다.
    - 상품의 가격은 0원 이상이어야 한다.
- 상품의 이름이 올바르지 않으면 등록할 수 없다.
    - 상품의 이름에는 비속어가 포함될 수 없다.
- 상품의 가격을 변경할 수 있다.
- 상품의 가격이 올바르지 않으면 변경할 수 없다.
    - 상품의 가격은 0원 이상이어야 한다.
- 상품의 가격이 변경될 때 메뉴의 가격이 메뉴에 속한 상품 금액의 합보다 크면 메뉴가 숨겨진다.
- 상품의 목록을 조회할 수 있다.

### 메뉴 그룹

- 메뉴 그룹을 등록할 수 있다.
- 메뉴 그룹의 이름이 올바르지 않으면 등록할 수 없다.
    - 메뉴 그룹의 이름은 비워 둘 수 없다.
- 메뉴 그룹의 목록을 조회할 수 있다.

### 메뉴

- 1 개 이상의 등록된 상품으로 메뉴를 등록할 수 있다.
- 상품이 없으면 등록할 수 없다.
- 메뉴에 속한 상품의 수량은 0 이상이어야 한다.
- 메뉴의 가격이 올바르지 않으면 등록할 수 없다.
    - 메뉴의 가격은 0원 이상이어야 한다.
- 메뉴에 속한 상품 금액의 합은 메뉴의 가격보다 크거나 같아야 한다.
- 메뉴는 특정 메뉴 그룹에 속해야 한다.
- 메뉴의 이름이 올바르지 않으면 등록할 수 없다.
    - 메뉴의 이름에는 비속어가 포함될 수 없다.
- 메뉴의 가격을 변경할 수 있다.
- 메뉴의 가격이 올바르지 않으면 변경할 수 없다.
    - 메뉴의 가격은 0원 이상이어야 한다.
- 메뉴에 속한 상품 금액의 합은 메뉴의 가격보다 크거나 같아야 한다.
- 메뉴를 노출할 수 있다.
- 메뉴의 가격이 메뉴에 속한 상품 금액의 합보다 높을 경우 메뉴를 노출할 수 없다.
- 메뉴를 숨길 수 있다.
- 메뉴의 목록을 조회할 수 있다.

### 주문 테이블

- 주문 테이블을 등록할 수 있다.
- 주문 테이블의 이름이 올바르지 않으면 등록할 수 없다.
    - 주문 테이블의 이름은 비워 둘 수 없다.
- 빈 테이블을 해지할 수 있다.
- 빈 테이블로 설정할 수 있다.
- 완료되지 않은 주문이 있는 주문 테이블은 빈 테이블로 설정할 수 없다.
- 방문한 손님 수를 변경할 수 있다.
- 방문한 손님 수가 올바르지 않으면 변경할 수 없다.
    - 방문한 손님 수는 0 이상이어야 한다.
- 빈 테이블은 방문한 손님 수를 변경할 수 없다.
- 주문 테이블의 목록을 조회할 수 있다.

### 주문

- 1개 이상의 등록된 메뉴로 배달 주문을 등록할 수 있다.
- 1개 이상의 등록된 메뉴로 포장 주문을 등록할 수 있다.
- 1개 이상의 등록된 메뉴로 매장 주문을 등록할 수 있다.
- 주문 유형이 올바르지 않으면 등록할 수 없다.
- 메뉴가 없으면 등록할 수 없다.
- 매장 주문은 주문 항목의 수량이 0 미만일 수 있다.
- 매장 주문을 제외한 주문의 경우 주문 항목의 수량은 0 이상이어야 한다.
- 배달 주소가 올바르지 않으면 배달 주문을 등록할 수 없다.
    - 배달 주소는 비워 둘 수 없다.
- 빈 테이블에는 매장 주문을 등록할 수 없다.
- 숨겨진 메뉴는 주문할 수 없다.
- 주문한 메뉴의 가격은 실제 메뉴 가격과 일치해야 한다.
- 주문을 접수한다.
- 접수 대기 중인 주문만 접수할 수 있다.
- 배달 주문을 접수되면 배달 대행사를 호출한다.
- 주문을 서빙한다.
- 접수된 주문만 서빙할 수 있다.
- 주문을 배달한다.
- 배달 주문만 배달할 수 있다.
- 서빙된 주문만 배달할 수 있다.
- 주문을 배달 완료한다.
- 배달 중인 주문만 배달 완료할 수 있다.
- 주문을 완료한다.
- 배달 주문의 경우 배달 완료된 주문만 완료할 수 있다.
- 포장 및 매장 주문의 경우 서빙된 주문만 완료할 수 있다.
- 주문 테이블의 모든 매장 주문이 완료되면 빈 테이블로 설정한다.
- 완료되지 않은 매장 주문이 있는 주문 테이블은 빈 테이블로 설정하지 않는다.
- 주문 목록을 조회할 수 있다.

## 용어 사전

### 공통
#### 단어
| 한글명 | 영문명        | 설명                      |
|-----|------------|-------------------------|
| 사장님 | owner      | 손님에게 메뉴를 판매하는 사용자       |
| 손님  | customer   | 사장님이 제공하는 메뉴를 구매하는 사용자  |
| 라이더 | rider      | 손님이 주문한 메뉴를 배달하는 사용자    |
| 매장  | restaurant | 매장 주문한 손님이 메뉴를 제공받는 장소  |

#### 행위
| 한글명  | 영문명      | 설명                                        |
|------|----------|-------------------------------------------|
| 등록하다 | register | 데이터를 등록하는 행위 <br> 예시) 상품을 등록하다. 메뉴를 등록하다. |
| 조회하다 | retrieve | 데이터를 조회하는 행위 <br> 예시) 상품을 조회하다. 메뉴를 조회하다. |
| 수정하다 | update   | 데이터를 수정하는 행위 <br> 예시) 상품을 수정하다. 메뉴를 수정하다. |

### 상품
#### 단어
| 한글명 | 영문명     | 설명             |
|-----|---------|----------------|
| 상품  | product | 메뉴를 구성하는 최소 단위 |


### 메뉴
#### 단어
| 한글명   | 영문명              | 설명                    |
|-------|------------------|-----------------------|
| 메뉴    | menu             | 사장님이 판매하고 손님이 구매하는 대상 |
| 노출 상태 | display status   | 메뉴가 손님에게 보여지는지 여부     |
| 메뉴 상품 | menu product     | 특정 메뉴에 포함된 상품         |
| 상품 수량 | product quantity | 특정 메뉴에 포함된 각각의 상품의 수량 |


### 메뉴 그룹
#### 단어
| 한글명   | 영문명        | 설명        |
|-------|------------|-----------|
| 메뉴 그룹 | menu group | 메뉴가 속한 그룹 |

### 주문
#### 단어
| 한글명   | 영문명            | 설명                       |
|-------|----------------|--------------------------|
| 주문    | menu group     | 손님이 사장님의 메뉴를 구매 신청한 행위   |
| 주문 유형 | order type     | 주문의 유형                   |
| 배달주문  | DELIVERY       | 손님에게 메뉴를 배달 장소로 배달하는 주문  |
| 포장주문  | TAKEOUT        | 손님이 매장에 방문해서 메뉴를 가져가는 주문 |
| 매장내주문 | EAT_IN         | 손님이 매장에서 메뉴를 제공받는 주문     |
| 주문 상태 | order status   | 주문의 상태                   |
| 대기중   | WAITING        | 주문 등록 후 접수 대기 상태         |
| 접수    | ACCEPTED       | 사장님이 주문을 수락한 상태          |
| 전달    | SERVED         | 손님에게 메뉴를 전달한 상태          |
| 배달중   | DELIVERING     | 라이더에게 메뉴를 전달한 상태         |
| 배달완료  | DELIVERED      | 라이더가 배달을 완료 상태           |
| 주문완료  | COMPLETED      | 주문이 완료됐을때의 상태            |

#### 행위
| 한글명  | 영문명      | 설명                           |
|------|----------|------------------------------|
| 제공하다 | serving  | 매장 내에서 사장님이 손님에게 메뉴를 제공하는 행위 |
| 배달하다 | delivery | 라이더가 배달장소로 손님에게 전달하는 행위      |
| 수락하다 | accept   | 사장님이 주문을 수락한 행위              |


### 주문 테이블
#### 단어
| 한글명       | 영문명                | 설명                        |
|-----------|--------------------|---------------------------|
| 주문 테이블    | order table        | 손님이 매장 내에서 메뉴를 제공받는 테이블   |
| 주문 테이블 상태 | order table status | 주문 테이블에서 주문을 할 수있는 있는지 여부 |


## 모델링
