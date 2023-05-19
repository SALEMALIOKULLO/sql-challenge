-- Data Engineering --
-- Drop Tables if Existing

DROP TABLE if exists departments;
DROP TABLE if exists dept_emp;
DROP TABLE if exists departments_managers;
DROP TABLE if exists employees;
DROP TABLE if exists salaries;
DROP TABLE if exists titles;

-- departments

CREATE TABLE "departments" (
    "dept_no" VARCHAR   NOT NULL,
    "dept_name" VARCHAR   NOT NULL,
    CONSTRAINT "pk_departments" PRIMARY KEY (
        "dept_no"
     )
);

-- dept_emp

CREATE TABLE "dept_emp" (
    "emp_no" VARCHAR,
	FOREIGN KEY (emp_no) REFERENCES employees(emp_no),
    "dept_no" VARCHAR,
	FOREIGN KEY (dept_no) REFERENCES departments(dept_no),
    "from_date" DATE,
    "to_date" DATE
);
--department_managers

CREATE TABLE "department_managers" (
    "dept_no" VARCHAR,
	FOREIGN KEY (dept_no) REFERENCES departments(dept_no),
    "emp_no" VARCHAR,
	FOREIGN KEY (emp_no) REFERENCES employees(emp_no),
    "from_date" DATE,
    "to_date" DATE
);


--employees

CREATE TABLE "employees" (
    "emp_no" INTEGER   NOT NULL,
    "emp_title" VARCHAR   NOT NULL,
    "birth_date" DATE   NOT NULL,
    "first_name" VARCHAR   NOT NULL,
    "last_name" VARCHAR   NOT NULL,
    "sex" CHAR   NOT NULL,
    "hire_date" DATE   NOT NULL,
    CONSTRAINT "pk_employees" PRIMARY KEY (
        "emp_no"
     )
);

--salaries

CREATE TABLE "salaries" (
    "emp_no" VARCHAR,
	FOREIGN KEY (emp_no) REFERENCES employees(emp_no),
    "salary" INTEGER,
    "from_date" DATE,
    "to_date" DATE
);

--titles

CREATE TABLE "titles" (
    "emp_no" VARCHAR,
	FOREIGN KEY (emp_no) REFERENCES employees(emp_no),
    "title" VARCHAR,
    "from_date" DATE,
    "to_date" DATE
);


-- Query * FROM Each Table Confirming Data
SELECT * FROM departments;
SELECT * FROM dept_emp;
SELECT * FROM department_managers;
SELECT * FROM employees;
SELECT * FROM salaries;
SELECT * FROM titles;
