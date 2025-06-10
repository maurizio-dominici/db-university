# Table 1: Departments

| Name | Type         | Attributes | Index       |
| ---- | ------------ | ---------- | ----------- |
| id   | INT          | NO NULL    | PRIMARY KEY |
| name | VARCHAR(100) | NO NULL    |             |

# Table 2: Degree courses

| Name          | Type         | Attributes | Index       |
| ------------- | ------------ | ---------- | ----------- |
| id            | INT          | NO NULL    | PRIMARY KEY |
| id_department | INT          | NO NULL    | FOREING KEY |
| name          | VARCHAR(100) | NO NULL    |             |

# Table 3: Courses

| Name             | Type         | Attributes | Index       |
| ---------------- | ------------ | ---------- | ----------- |
| id               | INT          | NO NULL    | PRIMARY KEY |
| id_degree_course | INT          | NO NULL    | FOREING KEY |
| name             | VARCHAR(100) | NO NULL    |             |

# Table 4: Teachers

| Name    | Type         | Attributes       | Index       |
| ------- | ------------ | ---------------- | ----------- |
| id      | INT          | NO NULL          | PRIMARY KEY |
| name    | VARCHAR(50)  | NO NULL          |             |
| surname | VARCHAR(50)  | NO NULL          |             |
| email   | VARCHAR(100) | NO NULL , UNIQUE |             |

# Table 5: Appeal exam

| Name      | Type | Attributes | Index       |
| --------- | ---- | ---------- | ----------- |
| id        | INT  | NO NULL    | PRIMARY KEY |
| id_course | INT  | NO NULL    | FOREING KEY |
| date      | DATE | NO NULL    | INDEX       |

# Table 6: Students

| Name                | Type         | Attributes      | Index       |
| ------------------- | ------------ | --------------- | ----------- |
| id                  | INT          | NO NULL         | PRIMARY KEY |
| id_degree_course    | INT          | NO NULL         | FOREING KEY |
| name                | VARCHAR(50)  | NO NULL         |             |
| surname             | VARCHAR(50)  | NO NULL         |             |
| registration_number | CHAR(10)     | NO NULL, UNIQUE |             |
| email               | VARCHAR(100) | NO NULL, UNIQUE |             |

# Table 7: Exam Registration

| Name           | Type    | Attributes | Index       |
| -------------- | ------- | ---------- | ----------- |
| id             | INT     | NO NULL    | PRIMARY KEY |
| id_student     | INT     | NO NULL    | FOREING KEY |
| id_appeal_exam | INT     | NO NULL    | FOREING KEY |
| vote           | TINYINT | NO NULL    |             |
