
SQL> CREATE TABLE EMPLOYEE2 (
  2      emp_no INT PRIMARY KEY,
  3      emp_name VARCHAR(20),
  4      emp_sal INT,
  5      emp_comm INT,
  6      dept_no INT
  7  );
CREATE TABLE EMPLOYEE2 (
             *
ERREUR Ó la ligne 1 :
ORA-00955: ce nom d'objet existe dÚjÓ


SQL> INSERT INTO EMPLOYEE VALUES (101,'Smith',800,NULL,20);

1 ligne crÚÚe.

SQL> INSERT INTO EMPLOYEE VALUES (102,'Snehal',1600,300,25);

1 ligne crÚÚe.

SQL> INSERT INTO EMPLOYEE VALUES (103,'Adama',1100,0,20);

1 ligne crÚÚe.

SQL> INSERT INTO EMPLOYEE VALUES (104,'Aman',3000,NULL,15);

1 ligne crÚÚe.

SQL> INSERT INTO EMPLOYEE VALUES (105,'Anita',5000,5000,10);

1 ligne crÚÚe.

SQL> INSERT INTO EMPLOYEE VALUES (106,'Sneha',2450,2450,10);

1 ligne crÚÚe.

SQL> INSERT INTO EMPLOYEE VALUES (107,'Anamika',2975,NULL,30);

1 ligne crÚÚe.

SQL> SELECT * FROM employee
  2  WHERE name LIKE 'A%';
WHERE name LIKE 'A%'
      *
ERREUR Ó la ligne 2 :
ORA-00904: "NAME" : identificateur non valide


SQL> SELECT * FROM EMPLOYEE;

    EMP_NO EMP_NAME                EMP_SAL   EMP_COMM    DEPT_NO
---------- -------------------- ---------- ---------- ----------
       101 Smith                       800                    20
       102 Snehal                     1600        300         25
       103 Adama                      1100          0         20
       104 Aman                       3000                    15
       105 Anita                      5000       5000         10
       106 Sneha                      2450       2450         10
       107 Anamika                    2975                    30
       101 Smith                       800                    10
       102 Snehal                     1600        300         25
       103 NewName                    1100          0         20
       104 Aman                       3000                    10

    EMP_NO EMP_NAME                EMP_SAL   EMP_COMM    DEPT_NO
---------- -------------------- ---------- ---------- ----------
       105 Anita                      5000       5000         10
       106 Sneha                      2450       2450         10
       107 Anamika                    2975                    30
       101 Smith                       800                    10
       102 Snehal                     1600        300         25
       103 NewName                    1100          0         20
       104 Aman                       3000                    10
       105 Anita                      5000       5000         10
       106 Sneha                      2450       2450         10
       107 Anamika                    2975                    30

21 lignes sÚlectionnÚes.

SQL> COMMIT;

Validation effectuÚe.

SQL> INSERT INTO EMPLOYEE VALUES (101,'Smith',800,NULL,20);

1 ligne crÚÚe.

SQL> INSERT INTO EMPLOYEE VALUES (102,'Snehal',1600,300,25);

1 ligne crÚÚe.

SQL> INSERT INTO EMPLOYEE VALUES (103,'Adama',1100,0,20);

1 ligne crÚÚe.

SQL> INSERT INTO EMPLOYEE VALUES (104,'Aman',3000,NULL,15);

1 ligne crÚÚe.

SQL> INSERT INTO EMPLOYEE VALUES (105,'Anita',5000,5000,10);

1 ligne crÚÚe.

SQL> INSERT INTO EMPLOYEE VALUES (106,'Sneha',2450,2450,10);

1 ligne crÚÚe.

SQL> INSERT INTO EMPLOYEE VALUES (107,'Anamika',2975,NULL,30);

1 ligne crÚÚe.

SQL> INSERT INTO EMPLOYEE VALUES (108,'Milan',2000,500,20);

1 ligne crÚÚe.

SQL> SELECT * FROM EMPLOYEE
  2  WHERE emp_name LIKE 'A%';

    EMP_NO EMP_NAME                EMP_SAL   EMP_COMM    DEPT_NO
---------- -------------------- ---------- ---------- ----------
       103 Adama                      1100          0         20
       104 Aman                       3000                    15
       105 Anita                      5000       5000         10
       107 Anamika                    2975                    30
       103 Adama                      1100          0         20
       104 Aman                       3000                    15
       105 Anita                      5000       5000         10
       107 Anamika                    2975                    30
       104 Aman                       3000                    10
       105 Anita                      5000       5000         10
       107 Anamika                    2975                    30

    EMP_NO EMP_NAME                EMP_SAL   EMP_COMM    DEPT_NO
---------- -------------------- ---------- ---------- ----------
       104 Aman                       3000                    10
       105 Anita                      5000       5000         10
       107 Anamika                    2975                    30

14 lignes sÚlectionnÚes.

SQL> SELECT * FROM EMPLOYEE
  2  WHERE emp_name LIKE '_n%';

    EMP_NO EMP_NAME                EMP_SAL   EMP_COMM    DEPT_NO
---------- -------------------- ---------- ---------- ----------
       102 Snehal                     1600        300         25
       105 Anita                      5000       5000         10
       106 Sneha                      2450       2450         10
       107 Anamika                    2975                    30
       102 Snehal                     1600        300         25
       105 Anita                      5000       5000         10
       106 Sneha                      2450       2450         10
       107 Anamika                    2975                    30
       102 Snehal                     1600        300         25
       105 Anita                      5000       5000         10
       106 Sneha                      2450       2450         10

    EMP_NO EMP_NAME                EMP_SAL   EMP_COMM    DEPT_NO
---------- -------------------- ---------- ---------- ----------
       107 Anamika                    2975                    30
       102 Snehal                     1600        300         25
       105 Anita                      5000       5000         10
       106 Sneha                      2450       2450         10
       107 Anamika                    2975                    30

16 lignes sÚlectionnÚes.

SQL> SELECT * FROM EMPLOYEE
  2  WHERE emp_name LIKE '__a%';

    EMP_NO EMP_NAME                EMP_SAL   EMP_COMM    DEPT_NO
---------- -------------------- ---------- ---------- ----------
       103 Adama                      1100          0         20
       104 Aman                       3000                    15
       107 Anamika                    2975                    30
       103 Adama                      1100          0         20
       104 Aman                       3000                    15
       107 Anamika                    2975                    30
       104 Aman                       3000                    10
       107 Anamika                    2975                    30
       104 Aman                       3000                    10
       107 Anamika                    2975                    30

10 lignes sÚlectionnÚes.

SQL> SELECT * FROM EMPLOYEE
  2  WHERE emp_name LIKE 'S_e%';

    EMP_NO EMP_NAME                EMP_SAL   EMP_COMM    DEPT_NO
---------- -------------------- ---------- ---------- ----------
       102 Snehal                     1600        300         25
       106 Sneha                      2450       2450         10
       102 Snehal                     1600        300         25
       106 Sneha                      2450       2450         10
       102 Snehal                     1600        300         25
       106 Sneha                      2450       2450         10
       102 Snehal                     1600        300         25
       106 Sneha                      2450       2450         10

8 lignes sÚlectionnÚes.

SQL> SELECT * FROM EMPLOYEE
  2  WHERE emp_name LIKE '___n%';

    EMP_NO EMP_NAME                EMP_SAL   EMP_COMM    DEPT_NO
---------- -------------------- ---------- ---------- ----------
       104 Aman                       3000                    15
       104 Aman                       3000                    15
       104 Aman                       3000                    10
       104 Aman                       3000                    10

SQL> SELECT * FROM EMPLOYEE
  2  WHERE emp_name LIKE '__a_i%';

    EMP_NO EMP_NAME                EMP_SAL   EMP_COMM    DEPT_NO
---------- -------------------- ---------- ---------- ----------
       107 Anamika                    2975                    30
       107 Anamika                    2975                    30
       107 Anamika                    2975                    30
       107 Anamika                    2975                    30

SQL> SELECT * FROM EMPLOYEE
  2  WHERE emp_name LIKE 'A__m_k%';

    EMP_NO EMP_NAME                EMP_SAL   EMP_COMM    DEPT_NO
---------- -------------------- ---------- ---------- ----------
       107 Anamika                    2975                    30
       107 Anamika                    2975                    30
       107 Anamika                    2975                    30
       107 Anamika                    2975                    30

SQL> SELECT * FROM EMPLOYEE
  2  WHERE emp_name LIKE 'M%';

    EMP_NO EMP_NAME                EMP_SAL   EMP_COMM    DEPT_NO
---------- -------------------- ---------- ---------- ----------
       108 Milan                      2000        500         20

SQL> SELECT * FROM EMPLOYEE
  2  WHERE emp_name LIKE 'A%';

    EMP_NO EMP_NAME                EMP_SAL   EMP_COMM    DEPT_NO
---------- -------------------- ---------- ---------- ----------
       103 Adama                      1100          0         20
       104 Aman                       3000                    15
       105 Anita                      5000       5000         10
       107 Anamika                    2975                    30
       103 Adama                      1100          0         20
       104 Aman                       3000                    15
       105 Anita                      5000       5000         10
       107 Anamika                    2975                    30
       104 Aman                       3000                    10
       105 Anita                      5000       5000         10
       107 Anamika                    2975                    30

    EMP_NO EMP_NAME                EMP_SAL   EMP_COMM    DEPT_NO
---------- -------------------- ---------- ---------- ----------
       104 Aman                       3000                    10
       105 Anita                      5000       5000         10
       107 Anamika                    2975                    30

14 lignes sÚlectionnÚes.

SQL> COMMIT ;

Validation effectuÚe.

SQL>
