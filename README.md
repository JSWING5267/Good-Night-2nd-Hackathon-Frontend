---
# 📽️ 영화 리뷰 앱 📽️
---

<br>

## 안내사항

- 본 레포지토리를 fork하여 과제를 수행하고, 완료시 PR을 보냅니다.
- 과제의 소스코드는 본인의 GitHub 레포지토리에 **Public**으로 올려주세요.
- 진행 간 문의사항은 이 레포지토리의 Issue로 등록해주세요.
- 구현 내용은 README.md 하단에 이어서 작성해 주세요.

<br>

## 기본 요구사항

- 아래 제시된 라이브러리, 프레임워크를 활용하여 영화 리뷰 앱을 구현합니다.
- 일관된 코딩 컨벤션을 유지해주세요.
- 기능 당 커밋은 필수입니다.

<br>

## 기술스택별 요구사항

### 1. Kotlin + Springboot

- 빌드 도구는 gradle를 사용해주세요.
- Spring data JPA를 사용해주세요.

### 2. Typescript + Nest.JS

- TypeORM을 사용해주세요.

### 3. Golang

- 프레임워크 사용은 자유입니다.
- Gorm이라는 ORM이 있지만 사용은 자유입니다.

<br>

## 도메인

- Movie
- Review

<br>

---

# 기능

## [📽️ 영화]

### 1. 영화 등록

- 제목, 장르, 개봉일, 상영 종료일, 상영 중 여부 정보를 포함해야 합니다.
- 등록 일자를 저장해야 합니다.
- 장르는 스릴러, 로맨스, 코믹, 액션 네 가지만 등록 가능합니다.
- 제목을 null로 등록하려고 할 때 예외를 처리합니다. (추가기능)

<br>
 
### 2. 영화 삭제
  - soft delete로 구현하여 영화 삭제시 리뷰 정보가 삭제 되지 않도록 합니다.
  - 조회 기능에서 삭제 처리된 영화는 조회하지 않도록 합니다.

<br>
 
### 3. 영화 수정
  - 제목, 장르, 개봉일, 상영 종료일, 상영 중 여부를 수정합니다.
  - 수정 일자가 업데이트되어야 합니다.

 <br>

### 4. 영화 단일 조회

- 제목, 장르, 개봉일, 상영 종료일, 상영 중 여부 정보를 반환합니다.
- 존재하지 않는 영화를 조회할 경우의 예외를 처리합니다. (추가기능)

 <br>

### 5. 영화 목록 조회

- 하나의 API에서 전체 조회와 장르, 현재 상영중 여부 조건을 선택하여 조회할 수 있어야 합니다. (쿼리 파라미터)
- 개봉일 순으로 정렬합니다.

 <br>
    
### 6. 영화 목록 평점 순 조회 (추가기능)
  - 페이지네이션이 가능합니다.
  - 영화 정보와 영화별 평점평균을 반환합니다.

<br> <br>

## [📝 리뷰]

### 7. 리뷰 등록

- 영화에 대한 리뷰 등록이 가능해야 합니다.
- 평점 (5점 만점), 리뷰 내용을 포함해야 합니다.

<br>

### 8. 리뷰 목록 조회

- 영화별로 리뷰 목록 조회가 가능해야 합니다.
- 등록일의 역순으로 정렬되어 있어야 합니다.
- 평점 n점 이상만 조회하도록 필터링 조건을 추가할 수 있어야 합니다. (추가기능)
  예) 평점 3.5이상 리뷰 조회

<br><br>

## [✅ 유닛 테스트]

- 유닛 테스트 코드를 작성합니다. (추가기능)

<br><br>

---

# 기여해주신 분

- [김영준](https://github.com/0BVer) 🦫
- [김하린](https://github.com/kimhalin) 🦦
- [김정현](https://github.com/kjeongh) 🦌

---

# 개발환경

- Go 1.20
- Gorm
- Gin
- MySQL 8.0
- Docker
- Docker-compose
- Swagger

# 📝 실행 방법

### 실행

```shell
docker-compose up -d
```

### Swagger

```
http://localhost:8080/api/v1/swagger/index.html#/
```

### 주의사항

- 모든 파라미터는 항상 필수이지만, 공백 가능입니다.
- pagination 파라미터의 페이지는 0번 부터 시작됩니다.
