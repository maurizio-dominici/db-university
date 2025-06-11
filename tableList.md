t# Table 1: Departments

| Name | Type         | Attributes | Index       |
| ---- | ------------ | ---------- | ----------- |
| id   | INT          | NOt NULL   | PRIMARY KEY |
| name | VARCHAR(100) | NOt NULL   |             |

# Table 2: Degree courses

| Name          | Type         | Attributes | Index       |
| ------------- | ------------ | ---------- | ----------- |
| id            | INT          | NOt NULL   | PRIMARY KEY |
| id_department | INT          | NOt NULL   | FOREING KEY |
| name          | VARCHAR(100) | NOt NULL   |             |

# Table 3: Courses

| Name             | Type         | Attributes | Index       |
| ---------------- | ------------ | ---------- | ----------- |
| id               | INT          | NOt NULL   | PRIMARY KEY |
| id_degree_course | INT          | NOt NULL   | FOREING KEY |
| name             | VARCHAR(100) | NOt NULL   |             |

# Table 4: Teachers

| Name    | Type         | Attributes        | Index       |
| ------- | ------------ | ----------------- | ----------- |
| id      | INT          | NOt NULL          | PRIMARY KEY |
| name    | VARCHAR(50)  | NOt NULL          |             |
| surname | VARCHAR(50)  | NOt NULL          |             |
| email   | VARCHAR(100) | NOt NULL , UNIQUE |             |

# Table 5: Appeal exam

| Name      | Type | Attributes | Index       |
| --------- | ---- | ---------- | ----------- |
| id        | INT  | NOt NULL   | PRIMARY KEY |
| id_course | INT  | NOt NULL   | FOREING KEY |
| date      | DATE | NOt NULL   | INDEX       |

# Table 6: Students

| Name                | Type         | Attributes       | Index       |
| ------------------- | ------------ | ---------------- | ----------- |
| id                  | INT          | NOt NULL         | PRIMARY KEY |
| id_degree_course    | INT          | NOt NULL         | FOREING KEY |
| name                | VARCHAR(50)  | NOt NULL         |             |
| surname             | VARCHAR(50)  | NOt NULL         |             |
| registration_number | CHAR(10)     | NOt NULL, UNIQUE |             |
| email               | VARCHAR(100) | NOt NULL, UNIQUE |             |

# Table 7: Exam Registration

| Name           | Type    | Attributes | Index       |
| -------------- | ------- | ---------- | ----------- |
| id             | INT     | NOt NULL   | PRIMARY KEY |
| id_student     | INT     | NOt NULL   | FOREING KEY |
| id_appeal_exam | INT     | NOt NULL   | FOREING KEY |
| vote           | TINYINT | NOt NULL   |             |
