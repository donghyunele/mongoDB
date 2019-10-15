# mongoDB
---

# 2019.10.15 ~
> 클라우드와 빅데이터의 강력한 파트너 MongoDB 핵심가이드 

### Study
---
> 2019.10.15
> ## DDL(정의어)
> * CREATE / DROP / ALTER

=> CREATE [TEMPORARY] TABLE [테이블 이름]([칼럼 정의])[테이블 매개변수]
ex) CREATE TABLE employees (
      id INTEGER PRIMARY KEY,
      first_name CHAR(50) NULL,
      last_name CHAT(70) NOT NULL,
      date_of_birth DATE NULL
    )

=> DROP TABLE [테이블 이름]
ex) DROP TABLE employees;

=> ARTER [객체 타입][객체 이름][매개변수];
ex) ALTER TABLE sink ADD bubbles INTEGER;

> ## DML(조작어)
> * SELECT / INSER / UPDATE / DELETE

=> SELECT [보여줄 이름] FROM [테이블 이름]
ex) SELECT * FROM T;

=> INSERT INTO [테이블 이름](column1, column2) VALUES (value1, value2);
ex) INSERT INTO phone_book (name, number) VALUES ('John Doe', '555-1212');

=> UPDATE [테이블 이름] SET [칼럼 이름] = value [, [칼럼 이름] = value2][WHRE [조건]];
ex) UPDATE T SET C1 = 1 WHERE C2 = 'a';

=> DELETE FROM [테이블 이름][WHERE 조건]
ex) DELETE FROM pies WHERE flavour = 'Lemon Meringue';

> ## DCL(제어어)
> * GRANT / COMMIT / ROLLBACK

=> GRANT [시스템 권한 | 객체 권한]
ex) GRANT SELECT, UPDATE
      ON example
      TO some_user, another_user

=> COMMIT / ROLLBACK
START TRANSACTION;
UPDATE Account SET amount=amount-200 WHERE account_number=1234;
UPDATE Account SET amount=amount+200 WHERE account_number=2345;

IF ERRORS=0 COMMIT;
IF ERRORS<>0 ROLLBACK;
