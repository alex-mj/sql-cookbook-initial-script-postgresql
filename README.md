Hi.
There are scripts for creating EMP and DEPT tables on postgresql database

```SQL
create table dept(
  deptno   decimal(2,0) not null,
  dname    varchar(14),
  loc      varchar(13));

create table emp(
  empno    decimal(4,0) not null,
  ename    varchar(10),
  job      varchar(9),
  mgr      decimal(4,0),
  hiredate date,
  sal      decimal(7,2),
  comm     decimal(7,2),  
  deptno   decimal(2,0) not null);

INSERT INTO DEPT (DEPTNO, DNAME, LOC)
VALUES  (10, 'ACCOUNTING', 'NEW YORK'),
		(20, 'RESEARCH', 'DALLAS'),
		(30, 'SALES', 'CHICAGO'),
		(40, 'OPERATIONS', 'BOSTON');
SELECT * FROM DEPT;

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO) VALUES
	(7369, 'SMITH', 	'CLERK', 	7902, TO_DATE('17-12-1980','dd-mm-yyyy'), 	800, CAST(NULL AS integer), 20),
	(7499, 'ALLEN', 	'SALESMAN', 	7698, TO_DATE('20-2-1981','dd-mm-yyyy'), 	1600, 300, 30),
	(7521, 'WARD', 		'SALESMAN', 	7698, TO_DATE('22-2-1981','dd-mm-yyyy'), 	1250, 500, 30),
	(7566, 'JONES', 	'MANAGER', 	7839, TO_DATE('2-4-1981','dd-mm-yyyy'), 	2975, CAST(NULL AS integer), 20),
	(7654, 'MARTIN', 	'SALESMAN', 	7698, TO_DATE('28-9-1981','dd-mm-yyyy'), 	1250, 1400, 30),
	(7698, 'BLAKE', 	'MANAGER', 	7839, TO_DATE('1-5-1981','dd-mm-yyyy'), 	2850, CAST(NULL AS integer), 30),
	(7782, 'CLARK', 	'MANAGER', 	7839, TO_DATE('9-6-1981','dd-mm-yyyy'), 	2450, CAST(NULL AS integer), 10),
	(7788, 'SCOTT', 	'ANALYST', 	7566, TO_DATE('9-12-1982','dd-mm-rr'), 		3000, CAST(NULL AS integer), 20),
	(7839, 'KING', 		'PRESIDENT', 	CAST(NULL AS integer), TO_DATE('17-11-1981','dd-mm-yyyy'), 5000, CAST(NULL AS integer), 10),
	(7844, 'TURNER', 	'SALESMAN', 	7698, TO_DATE('8-9-1981','dd-mm-yyyy'), 	1500, 0, 30),
	(7876, 'ADAMS', 	'CLERK', 	7788, TO_DATE('12-1-1983', 'dd-mm-rr'), 	1100, CAST(NULL AS integer), 20),
	(7900, 'JAMES', 	'CLERK', 	7698, TO_DATE('3-12-1981','dd-mm-yyyy'), 	950, CAST(NULL AS integer), 30),
	(7902, 'FORD', 		'ANALYST', 	7566, TO_DATE('3-12-1981','dd-mm-yyyy'), 	3000, CAST(NULL AS integer), 20),
	(7934, 'MILLER', 	'CLERK', 	7782, TO_DATE('23-1-1982','dd-mm-yyyy'), 	1300, CAST(NULL AS integer), 10);

SELECT * FROM EMP ORDER BY 1;
```
