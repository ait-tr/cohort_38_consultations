### Ограничения

CREATE TABLE department (id serial PRYMARY KEY, department_title VARCHAR(75));

---

CREATE TABLE
  employee (
    id serial PRIMARY KEY,
    employee_name VARCHAR(75),
    start_data DATE,
    department_id INT REFERENCES department(id)
  );

---

INSERT INTO
  department (department_title)
VALUES
  ('analitics'),
  ('manager'),
  ('statistic'),
  ('QA');

---

INSERT INTO
  employee (id, employee_name, start_data, department_id)
VALUES
  (001, 'Bob', '1901-07-02', 1 ),
  (002, 'Nick', '2002-03-01', 2 ),
  (003, 'Sarha', '2017-02-28', 3 ),
  (004, 'Sandra', '2003-12-12', 3),
	(005, 'Micharl', '2003-12-11', null);

---

CREATE TABLE
  employee (
    id serial PRIMARY KEY,
    employee_name VARCHAR(75),
    start_data DATE,
    age_employee SMALLINT CHECK (age_employee > 18), 
    department_id INT REFERENCES department(id)
  );

---

CREATE TABLE
  employee (
    id serial PRIMARY KEY,
    employee_name VARCHAR(75),
    start_data DATE,
    age_employee SMALLINT CHECK (age_employee > 18) NOT NULL, 
    department_id INT REFERENCES department(id),
    CHECK (age_employee < 90)
  );

---

INSERT INTO
  employee (employee_name, start_data, department_id, age_employee)
VALUES
  ( 'Bob', '1901-07-02', 1, 22 ),
  ( 'Nick', '2002-03-01', 2, 21 ),
  ( 'Sarha', '2017-02-28', 3, 19 ),
  ( 'Sandra', '2003-12-12', 3, 31),
	( 'Micharl', '2003-12-11', null, 89),
  ( 'Tom', '2004-02-21', 4, 23);
 
 ---

CREATE TABLE
  employee (
    id serial PRIMARY KEY,
    employee_name VARCHAR(75),
    start_data DATE,
    age_employee SMALLINT NOT NULL, 
    department_id INT REFERENCES department(id),
    CONSTRAINT invalide_age CHECK (age_employee > 18 OR age_employee < 90) 
  );

---

CREATE TABLE
  employee (
    id serial PRIMARY KEY,
    employee_name VARCHAR(75),
    start_data DATE,
    age_employee SMALLINT NOT NULL, 
    department_id INT REFERENCES department(id),
    CONSTRAINT invalide_age CHECK (age_employee > 18 AND age_employee < 90) 
  );

---


