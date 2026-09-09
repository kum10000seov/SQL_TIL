# 📘 SQL_BASIC 2주차 정규 과제

SQL_BASIC 정규 과제는 매주 정해진 분량의 `초보자를 위한 BigQuery(SQL) 입문` 강의를 듣고, 핵심 개념을 정리한 뒤 간단한 SQL 문제를 직접 풀어보는 방식으로 진행합니다.

이번 주는 저장된 데이터를 확인하는 방법과 `SELECT`, `FROM`, `WHERE`의 기본 구조를 학습합니다.

완성된 과제는 Github에 업로드하고, 링크를 스프레드시트 'SQL' 시트에 입력해 제출해주세요.

**👀 수행 인증란은 필수입니다.**

---

## 📚 SQL_BASIC_2nd_TIL

### 섹션 3. 데이터 탐색 - 조건, 추출, 요약

### 2-2. 저장된 데이터 확인하기(데이터베이스, 데이터 웨어하우스, ERD)

### 2-3. 데이터 탐색(SELECT, FROM, WHERE)

---

## ✨ 선택 강의

- 2-4. SELECT 연습 문제: SELECT, FROM, WHERE를 더 연습하고 싶을 때 선택 수강

---

## 🏁 전체 강의 수강 계획

| 주차 | 필수 강의 범위 | 선택 강의 | 완료 여부 |
| --- | --- | --- | --- |
| 1주차 | 1-1 ~ 2-1 | 1 | ✅ |
| 2주차 | 2-2 ~ 2-3 | 2-4 | ✅ |
| 3주차 | 2-5, 2-7 ~ 2-8 | 2-6 | 🍽️ |
| 4주차 | 3-2 ~ 4-3 | 3-4 | 🍽️ |
| 5주차 | 4-4 ~ 4-6 | 4-5, 4-7 | 🍽️ |
| 6주차 | 5-2 ~ 5-5 | 5-6 | 🍽️ |
| 7주차 | 필수 강의 없음 | 6-2, 6-3, 6-4, 6-5 | 🍽️ |

---

<br>

<!-- 여기까진 그대로 둬 주세요-->

---

# 1️⃣ 개념 정리

아래 키워드 중 중요하다고 생각한 개념을 2개 이상 골라 짧게 정리해주세요. 3개보다 더 많이 정리하고 싶다면 자유롭게 항목을 추가해도 좋습니다.

이번 주 키워드:
- SELECT
- FROM
- WHERE
- 조건식
- ORDER BY
- LIMIT
- 테이블 구조 확인

## 01.

```
개념 이름: FROM
개념 설명: 데이터를 확인할 Table 명시, <프로젝트id>.<데이터셋>.<테이블> 순으로 입력, 프로젝트 id는 꼭 명시할 필요는 없을 수도 있음 (프로젝트가 단일이라면!), 단 프로젝트를 여러개 사용한다면 명시하는 것이 좋음 => 쿼리를 실행할 때 어떤 프로젝트인지 확인하는 과정이 존재
예시 쿼리: FROM `inflearn-bigquery-2026.basic.pokemon` AS t1
이때, 이름이 너무 길다면 AS "별칭"으로 별칭 지정 가능 
```

## 02.

```
개념 이름: WHERE
개념 설명: FROM에 명시된 Table에 저장된 데이터를 필터링(조건 설정)
예시 쿼리: WHERE type1 = "Fire"
```

## 03.

```
개념 이름: SELECT
개념 설명: Table에 저장되어 있는 컬럼 선택, 여러 컬럼 명시 가능.
예시 쿼리: SELECT id AS pokemon_id, kor_name, type1, total
```

---

# 2️⃣ 수행 인증란

<img width="288" height="233" alt="image" src="https://github.com/user-attachments/assets/f99dafa7-f1e1-42ac-b2a5-7f753f38b470" />


---

# 3️⃣ 확인 문제

프로그래머스는 로그인이 필요하므로, 로그인 후 문제 풀이를 진행해주세요.

## 🧩 문제 1

문제 링크: [모든 레코드 조회하기](https://school.programmers.co.kr/learn/courses/30/lessons/59034)

풀이 과정:

```
- 테이블에서 확인한 컬럼: ANIMAL_ID, ANIMAL_TYPE, DATETIME, INTAKE_CONDITION, NAME, SEX_UPON_INTAKE
- SELECT와 FROM을 작성한 방식: SELECT * FROM ANIMAL_INS
- 새로 배운 점: 조건이 없다면 WHERE는 생략 가능, FROM 다음에 데이터셋 제목이 없다면 그냥 테이블명만 입력해도 됨
```
<img width="1265" height="692" alt="image" src="https://github.com/user-attachments/assets/4279946c-92c1-4f1e-9c19-9f9cfe2646e1" />



## 🧩 문제 2

문제 링크: [아픈 동물 찾기](https://school.programmers.co.kr/learn/courses/30/lessons/59036)

풀이 과정:

```
- 문제에서 요구한 조건: 아픈 동물, 즉 INTAKE_CONDITION 컬럼의 값이 'Sick'인 동물
- WHERE 절로 옮긴 방식: WHERE INTAKE_CONDITION = 'Sick'
- 정렬 기준이 있다면 사용한 기준: 아이디 순으로 정렬해달라고 했지만, 이미 데이터베이스 내부적으로 ANIMAL_ID가 오름차순으로 정렬되어 있어 별도의 정렬 구문 없이도 ID 순서대로 출력됨
- 새로 배운 점: 기본 키(Primary Key)의 개념
```
<img width="1266" height="691" alt="image" src="https://github.com/user-attachments/assets/4f4345b3-a58e-48fa-a8e9-a81901d46004" />


---

# 4️⃣ 이번 주 회고

```
1. SELECT, FROM, WHERE 중 가장 헷갈린 개념: SELECT, FROM, WHERE 순서를 반드시 지켜야 한다는 점(순서가 어그러질 경우 실행이 되지 않는다는 점)
2. 문제를 풀 때 가장 자주 확인하게 된 부분: 구두점(Punctuation)과 데이터셋의 이름, 테이블 이름 등 경로명
3. 다음 주 문제 풀이에서 의식하고 싶은 습관: WHERE 조건절에 들어가야 할 내용이 무엇인가?를 항상 염두에 두기
```

수고하셨습니다!




