---
layout : post
title : "ORACLE 12c setting"
date : 2018-07-11 11:11:00 +0900
categories : db
tag:
- db
comments : true
---

# oracle 12c release2

> 오라클 12 Cloud 릴리즈2 바전 세팅


## 실행 (윈도우키 + R) -> sqlplus / as sysdba

```create user 계정 identified by 암호;```

- ORA-65096: 공통 사용자 또는 롤 이름이 부적합합니다.

  > 오라클 12c부터는 cdb의 계정명은 C## 혹은 c## (대소문을 구분함)

```create user C##계정 identified by 암호;```

- 사용자가 생성되었습니다.



## 계정을 생성한 후 권한 주기

```grant all privileges to C##계정; ```

- 권한이 부여되었습니다.

```grant EM_EXPRESS_BASIC to C##계정;```

- 권한이 부여되었습니다.
  > https://localhost:5500/em/login 위해 EM_EXPRESS_BASIC 이상의 권한을 줘야함


```grant sysdba to C##유저 container=all;```



- 권한이 부여되었습니다.


## 연습용(scott) 계정열기

```create user c##scott identified by tiger;```

```alter user c##scott default tablespace users quota unlimited on users;```

```create role c##plustrace;```

```grant select on v_$sesstat to c##plustrace;```

```grant select on v_$statname to c##plustrace;```

```grant select on v_$mystat to c##plustrace;```

```grant c##plustrace to dba with admin option;```

```grant connect, resource to c##scott;```

```grant c##plustrace to c##scott;```

```grant create view to c##scott;```

```grant create sequence to c##scott;```

### c##scott 으로 접속하기

```sqlplus
connect c##scott / tiger
```

```sqlplus
SQL>alter session set nls_date_format = 'DD-MM-YYYY';
```

```sqlplus
SQL>alter session set nls_language = 'korean';
```

```sqlplus
SQL> @E:\app\com\virtual\product\12.2.0\dbhome_1\rdbms\admin\scott.sql
```
> 에러날 경우 위에 부분 지우기)


### 테스트

```sqlplus
SQL> set linesize 280;
```

```sqlplus
SQL> set pagesize 100
```

```sqlplus
SQL> select * from emp;
```

```SQL
​     EMPNO ENAME                JOB                       MGR HIREDATE        SAL       COMM     DEPTNO

---------- -------------------- ------------------ ---------- -------- ---------- ---------- ----------

​      7369 SMITH                CLERK                    7902 80/12/17        800                    20

​      7499 ALLEN                SALESMAN                 7698 81/02/20       1600        300         30

​      7521 WARD                 SALESMAN                 7698 81/02/22       1250        500         30

​      7566 JONES                MANAGER                  7839 81/04/02       2975                    20

​      7654 MARTIN               SALESMAN                 7698 81/09/28       1250       1400         30

​      7698 BLAKE                MANAGER                  7839 81/05/01       2850                    30

​      7782 CLARK                MANAGER                  7839 81/06/09       2450                    10

​      7839 KING                 PRESIDENT                     81/11/17       5000                    10

​      7844 TURNER               SALESMAN                 7698 81/09/08       1500          0         30

​      7900 JAMES                CLERK                    7698 81/12/03        950                    30

​      7902 FORD                 ANALYST                  7566 81/12/03       3000                    20

​      7934 MILLER               CLERK                    7782 82/01/23       1300                    10

12 행이 선택되었습니다.
```

개발시작!
