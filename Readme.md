# 마마무 솔라와 롤의 리신의 자리를 대체하며 최근에 많은 사랑을 받고 있는 Elastic Search
인덱스, 타입, 문서, 필드 구조로 구성된다
## 구성 요소
### 인덱스
데이터 저장 공간. 하나의 타입만을 가지며. 하나의 인덱스가 여러 노드에 분산 저장되어 관리된다
### 샤드
인덱스 내부에 색인된 데이터는 물라적인 공간에 여러 개의 파티션으로 나뉘어 구성되는데, 아 파티션을 엘라스틱서치에서는 shard라고 한다
### 타입
인덱스의 논리적 구조를 의미하며, 인덱스 속성에 따라 분류하기도 한다. 인덱스 당 하나의 타입만 사용할 수 있다. 현재는 타입 사용이 권장되지 않음.      
과거에는 인덱스 아래 타입을 여러개 둬서 카테고리를 분류했지만, 이제는 여러개의 인덱스로 간다.    
### 문서
엘라스틱 서치에서 데이터가 저장되는 최소 단위. 하나의 문서는 다수의 필드로 구성돼 있는데 각 필드는   
데이터 형태에 따라 용도에 맞는 데이터 타입을 정의해야 한다. 중첩 구조를 지원한다    
문서 안에 문서를 지정하는 것도 가능하다
### 필드
문서를 구성하기 위한 속성. 필드는 좀 더 동적(Dynamic)인 데이터 타입이다
### 매핑
문서의 필드와 필드의 속성을 정의하고 그에 따른 색인 방법을 정의하는 프로세스

## 노드
### 마스터 노드
클러스터와 관련된 전반적인 작업. ex) 인덱스 생성, 삭제
### 데이터 노드
문서가 실제로 저장되는 샤드가 배치되는 노드
### 코디네이팅 노드
들어온 요청을 라운드로빈 방식으로 분산시켜 주는 노드
### 인제스트 노드
섹인에 앞서 데이터를 전처리하기 위한 노드

## 인덱스
### 인덱스 관리 API
인덱스 관리
### 문서 관리 API 
문서의 추가 / 수정 / 삭제
### 검색 API
문서 조회
### 집계 API
문서 통계

# 참고 
- https://gem1n1.tistory.com/83 velog님의 블로그는 항상 정리가 잘 되어져있다

# Issue
## Kibana
> connect ECONNREFUSED 0.0.0.0:9200
아 도커 container 자기 스스로를 찌르고 있구나...