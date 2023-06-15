## API Endpoint Routes 📌

### Intro 📌

- Hello everybody, it's Mohamed here, a computer science student, I'm excited to share with you my final year graduation project which's called Unista. It's a complete Learning Management System for universities, powered with the essential functionalities required for online learning today.

- I've built everything from scratch, including the ERD design, database, backend APIs, and a basic UI prototype. I've also implemented testing suites and a CI/CD pipeline to ensure its quality and efficiency.

- We have 5 main user roles (Master, Admin, Professor, Assistant, Student) and each role has different permissions.

    - The master is responsible for the initial setup of the system and creating professors and assistants for each college, as well as administrators for each level.

    - Admins are responsible for creating courses, assigning professors to each course, and enrolling students from each department.

    - The professor is responsible for creating assignments and exams, uploading course e-books, creating lectures and uploading lecture files, taking attendance, and performing various other tasks.

    - The assistant is responsible for creating sections and assignments for each section, uploading section files, taking attendance, and performing various other tasks.

    - The student can access and utilize all resources created by professors and assistants, such as assignments, exams, lectures, section files, attendance records, and various other materials and activities.
### How we store and fetch files (AWS S3 PRESIGNED URL) 📁

[Check my blog about different file upload solutions](https://iammo69.web.app/file-upload-solutions.html)
![AWS S3 Presigned URL System](https://i.imgur.com/RDysto9.png)


### SECURITY 🔐

- `JWT` authentication.
- `ACL` authorization.
- `Rate Limiting` protection. (Prevent brute force attacks)
- All files are accessible only by `Presigned URL` (AWS S3) which will be expired after **_n_** minutes.
- Define `CORS` policy to allow only specific domains.
- Header security using `Helmet` package.
- Passwords are hashed using in un-reversible algorithm `bcrypt`.
- Strict endpoint validation system (IDs, etc).

### API VERSIONING 📦

- All routes are versioned by default `GET - api/v1/courses`

### TECH STACK (main) 📚

- NodeJS
- ExpressJS
- MongoDB
- Mongoose
- AWS S3

### DEPLOYMENT STACK (CI/CD) 🚀

- Docker 
- Kubernetes (AWS EKS) 
- AWS EC2
- Travis CI
- Nginx 


### Code Features 📌
- [x] CRUD (Create, Read, Update, Delete) for all resources using RESTful API design
- [x] Index Pagination - Search - Sort - Select - Filter
- [x] API Versioning (v1)
- [x] Best Practices & Clean Code (MVC, SOLID, DRY, KISS)
- [x] API Documentation
- [x] Scalable System (You can add as much features as you want without breaking the system)
- [x] Error Handling System (Genaric error handler middleware with Correct HTTP Status Code & Error message)


### Unista Features 📌

- [x] Authentication login using 3 different ways (credentials, scan QR code, upload QR code)
- [x] Role based system (Master, Admin, Professor, Assistant, Student)
- [x] Smart attendace system (QR Code)
- [x] Accurate Geolocation system (GPS) for attendance
- [x] Secure Exam system (No way to cheat)
- [x] Auto genrate exam questions (MCQ, True/False, Fill in the blanks) based on uploaded course e-book.
- [x] Assignments system
- [x] Fast - secure - scalable file system (AWS S3)
- [x] Horizontal Scaling (Kubernetes add pods(EC2) to scale horizontally if CPU usage is high)
- [x] MORE TO COME...

### TODOs 📝

- [ ] Add `Redis` for caching
- [ ] Add `Jest` for testing (unit, integration)
- [ ] Add `Notification` system
- [ ] Add `Emailing` system
- [ ] Enhance `NodeJS` performance [My blog about node clustring](https://iammo69.web.app/enhance-node-performance.html)
- [ ] Add `Chat` system
- [ ] Add `Video conferencing` system
- [ ] Add `Student activities` system
- [ ] Add `Student to student learning` system
- [ ] Add `Vote` system
- [ ] Add `DOSS` protection
### STATISTICS 📈

_API-Endpoint Routes_: **157**


### Environment Variables 🌐

```bash
# ENV info
NODE_ENV="dev"
# PORT info
PORT_DEV="xxxxxxx"
PORT_PROD="xxxxxxx"
PORT_TEST="xxxxxxx"
# DB connection info
DB_USER_DEV="xxxxxxx"
DB_USER_PROD="xxxxxxx"
DB_USER_TEST="xxxxxxx"
DB_PASSWORD_DEV="xxxxxxx"
DB_PASSWORD_PROD="xxxxxxx"
DB_PASSWORD_TEST="xxxxxxx"
DB_HOST_DEV="xxxxxxx"
DB_HOST_PROD="xxxxxxx"
DB_HOST_TEST="xxxxxxx"
# CORS config
CORS_ORIGIN_DEV="xxxxxxx"
CORS_ORIGIN_PROD="xxxxxxx"
CORS_ORIGIN_TEST="xxxxxxx"
# REQ limit
REQUEST_LIMIT_TIMEOUT_DEV="xxxxxxx"
REQUEST_LIMIT_TIMEOUT_PROD="xxxxxxx"
REQUEST_LIMIT_TIMEOUT_TEST="xxxxxxx"
REQUEST_LIMIT_MAX_DEV="xxxxxxx"
REQUEST_LIMIT_MAX_PROD="xxxxxxx"
REQUEST_LIMIT_MAX_TEST="xxxxxxx"
# BCRYPT config
BCRYPT_SALT_ROUNDS_DEV="xxxxxxx"
BCRYPT_SALT_ROUNDS_PROD="xxxxxxx"
BCRYPT_SALT_ROUNDS_TEST="xxxxxxx"
BCRYPT_PEPPER_DEV="xxxxxxx"
BCRYPT_PEPPER_PROD="xxxxxxx"
BCRYPT_PEPPER_TEST="xxxxxxx"
# JWT config
JWT_SECRET_DEV="xxxxxxx"
JWT_SECRET_PROD="xxxxxxx"
JWT_SECRET_TEST="xxxxxxx"
JWT_EXPIRES_IN_DEV="xxxxxxx"
JWT_EXPIRES_IN_PROD="xxxxxxx"
JWT_EXPIRES_IN_TEST="xxxxxxx"
# URL
URL_DEV="xxxxxxx"
URL_TEST="xxxxxxx"
URL_PROD="xxxxxxx"
# SECRET KEYS
MASTER_SECRET_KEY_DEV="xxxxxxx"
MASTER_SECRET_KEY_TEST="xxxxxxx"
MASTER_SECRET_KEY_PROD="xxxxxxx"
# AWS
AWS_ACCESS_KEY_ID_DEV="xxxxxxx"
AWS_ACCESS_KEY_ID_TEST="xxxxxxx"
AWS_ACCESS_KEY_ID_PROD="xxxxxxx"
AWS_SECRET_ACCESS_KEY_DEV="xxxxxxx"
AWS_SECRET_ACCESS_KEY_TEST="xxxxxxx"
AWS_SECRET_ACCESS_KEY_PROD="xxxxxxx"
AWS_REGION_DEV="xxxxxxx"
AWS_REGION_TEST="xxxxxxx"
AWS_REGION_PROD="xxxxxxx"
AWS_BUCKET_NAME_DEV="xxxxxxx"
AWS_BUCKET_NAME_TEST="xxxxxxx"
AWS_BUCKET_NAME_PROD="xxxxxxx"
AWS_EXPIRES_IN_MINUTES_DEV="xxxxxxx"
AWS_EXPIRES_IN_MINUTES_TEST="xxxxxxx"
AWS_EXPIRES_IN_MINUTES_PROD="xxxxxxx"
RANDOM_CHARS_DEV="xxxxxxxxxxxxxxx"
RANDOM_CHARS_LENGTH_DEV="xxxxxxx"
RANDOM_CHARS_TEST="xxxxxxxxxxxxxxx"
RANDOM_CHARS_LENGTH_TEST="xxxxxxx"
RANDOM_CHARS_PROD="xxxxxxxxxxxxxxx"
RANDOM_CHARS_LENGTH_PROD="xxxxxxx"
API_ENDPOINT_DEV="xxxxxxx"
API_ENDPOINT_TEST="xxxxxxx"
API_ENDPOINT_PROD="xxxxxxx"
API_TOKEN_DEV="xxxxxxx"
API_TOKEN_TEST="xxxxxxx"
API_TOKEN_PROD="xxxxxxx"
```

### Installation 📥

```bash
# Clone the repo
git clone
# Install dependencies
npm install
# Run the app
npm start
# Run the app in development mode
npm run dev:fast
```

### Success Response Format ✅

```json
{
  "status": "success",
  "message": "Success message",
  "data": {
    "user": {
      "id": "642debe976e91123782b7f42",
      "name": "John Doe"
    }
  }
}
```

### Error Response Format ❌

```json
{
  "status": "Error",
  "message": "Error message"
}
```

### HINTS 📝

- All index routes are paginated by default, you can pass `page` and `limit` as query params to change the pagination.
  Example: `GET - api/v1/courses?page=2&limit=10`

### API DOCUMENTATION 📖
### All Endpoints (overview) 📡

#### Authentication 🔐

##### Login ⭐

- `POST - api/v1/auth/login` - Login [Details](#login-)

#### MASTER 🔑

##### UNIVERSITY ⭐

- `GET - api/v1/master/universities` - Index [Details](#index-universities-)
- `POST - api/v1/master/universities` - Create [Details](#create-university-)
- `GET - api/v1/master/universities/:id` - Show [Details](#show-university-)
- `PATCH - api/v1/master/universities/:id` - Update [Details](#update-university-)
- `DELETE - api/v1/master/universities/:id` - Delete [Details](#delete-university-)

##### COLLAGE TYPE ⭐

- `POST - api/v1/master/collage-types` - Create [Details](#create-collage-type-)
- `GET - api/v1/master/collage-types` - Index [Details](#index-collage-types-)
- `GET - api/v1/master/collage-types/:id` - Show [Details](#show-collage-type-)
- `PATCH - api/v1/master/collage-types/:id` - Update [Details](#update-collage-type-)
- `DELETE - api/v1/master/collage-types/:id` - Delete [Details](#delete-collage-type-)

##### COLLAGE ⭐

- `POST - api/v1/master/universities/:id/collages` - Create [Details](#create-collage-)
- `GET - api/v1/master/universities/:id/collages` - Index [Details](#index-collages-)
- `GET - api/v1/master/universities/:id/collages/:id` - Show [Details](#show-collage-)
- `PATCH - api/v1/master/universities/:id/collages/:id` - Update [Details](#update-collage-)
- `DELETE - api/v1/master/universities/:id/collages/:id` - Delete [Details](#delete-collage-)

##### LEVEL ⭐

- `POST - api/v1/master/universities/:id/collages/levels` - Create [Details](#create-level-)
- `GET - api/v1/master/universities/:id/collages/levels` - Index [Details](#index-levels-)
- `GET - api/v1/master/universities/:id/collages/levels/:id` - Show [Details](#show-level-)
- `PATCH - api/v1/master/universities/:id/collages/levels/:id` - Update [Details](#update-level-)
- `DELETE - api/v1/master/universities/:id/collages/levels/:id` - Delete [Details](#delete-level-)

##### PROFESSOR ⭐

- `POST - api/v1/master/universities/:id/collages/:id/professors` - Create [Details](#create-professor-)
- `GET - api/v1/master/universities/:id/collages/:id/professors` - Index [Details](#index-professors-)
- `GET - api/v1/master/universities/:id/collages/:id/professors/:id` - Show [Details](#show-professor-)
- `PATCH - api/v1/master/universities/:id/collages/:id/professors/:id` - Update [Details](#update-professor-)
- `DELETE - api/v1/master/universities/:id/collages/:id/professors/:id` - Delete [Details](#delete-professor-)

##### ADMIN ⭐

- `POST - api/v1/master/universities/:id/collages/:id/levels/:id/admins` - Create [Details](#create-admin-)
- `GET - api/v1/master/universities/:id/collages/:id/levels/:id/admins` - Index [Details](#index-admins-)
- `GET - api/v1/master/universities/:id/collages/:id/levels/:id/admins/:id` - Show [Details](#show-admin-)
- `PATCH - api/v1/master/universities/:id/collages/:id/levels/:id/admins/:id` - Update [Details](#update-admin-)
- `DELETE - api/v1/master/universities/:id/collages/:id/levels/:id/admins/:id` - Delete [Details](#delete-admin-)

#### ADMIN 👔

##### ACCESS PERMISSOIN ⭐

- `GET - api/v1/admin/:id` - Show [Details](#show-admin-)
- `PATCH - api/v1/admin/:id` - Update [Details](#update-admin-)

##### PROGRAM ⭐

- `POST - api/v1/admin/universities/:id/collages/:id/levels/:id/programs` - Create [Details](#create-program-)
- `GET - api/v1/admin/universities/:id/collages/:id/levels/:id/programs` - Index [Details](#index-programs-)
- `GET - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id` - Show [Details](#show-program-)
- `PATCH - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id` - Update [Details](#update-program-)
- `DELETE - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id` - Delete [Details](#delete-program-)

##### DEPARTMENT ⭐

- `POST - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments` - Create [Details](#create-department-)
- `GET - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments` - Index [Details](#index-departments-)
- `GET - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id` - Show [Details](#show-department-)
- `PATCH - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id` - Update [Details](#update-department-)
- `DELETE - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id` - Delete [Details](#delete-department-)

##### Student ⭐

- `POST - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id/students` - Create [Details](#create-student-)
- `GET - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id/students` - Index [Details](#index-students-)
- `GET - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id/students/:id` - Show [Details](#show-student-)
- `PATCH - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id/students/:id` - Update [Details](#update-student-)
- `DELETE - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id/students/:id` - Delete [Details](#delete-student-)

##### QUICK ACCESS ⭐

- `GET - api/v1/admin/:id/levels/:id` - Show admin level [Details](#show-admin-level-)

#### PROFESSOR 👨‍🏫

##### ACCESS PERMISSOIN ⭐

- `GET - api/v1/professor/:id` - Show [Details](#show-professor-)
- `PATCH - api/v1/professor/:id` - Update [Details](#update-professor-)

##### COURSE ⭐

- `POST - api/v1/professor/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id/courses` - Create [Details](#create-course-)
- `DELETE - api/v1/professor/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id/courses/:id` - Delete [Details](#delete-course-)
- `GET - api/v1/professor/courses` - Index [Details](#index-courses-)
- `GET - api/v1/professor/courses/:id` - Show [Details](#show-course-)
- `PATCH - api/v1/professor/courses/:id` - Update [Details](#update-course-)

##### EBOOK ⭐

- `POST - api/v1/professor/courses/:id/ebook` - Create [Details](#create-ebook-)
- `GET - api/v1/professor/courses/:id/ebook/:id` - Show [Details](#show-ebook-)
- `PATCH - api/v1/professor/courses/:id/ebook/:id` - Update [Details](#update-ebook-)
- `DELETE - api/v1/professor/courses/:id/ebook/:id` - Delete [Details](#delete-ebook-)

##### ASSISTANT ⭐

- `POST - api/v1/professor/universities/:id/collages/:id/courses/:id/assistants` - Create [Details](#create-assistant-)
- `POST -  api/v1/professor/universities/:id/collages/:id/courses/:id/assistants/:id/attach` - Attach [Details](#attach-assistant-)
- `PATCH - api/v1/professor/universities/:id/collages/:id/courses/:id/assistants/:id` - Update [Details](#update-assistant-)
- `DELETE - api/v1/professor/universities/:id/collages/:id/courses/:id/assistants/:id` - Delete [Details](#delete-assistant-)
- `GET - api/v1/professor/universities/:id/collages/:id/courses/:id/assistants/:id` - Show [Details](#show-assistant-)
- `GET - api/v1/professor/universities/:id/collages/:id/courses/:id/assistants` - Index By Course [Details](#index-assistants-by-course-)
- `GET - api/v1/professor/universities/:id/collages/:id/assistants` - Index By Collage [Details](#index-assistants-by-collage-)

##### LECTURE ⭐

- `POST - api/v1/professor/courses/:id/lectures` - Create [Details](#create-lecture-)
- `GET - api/v1/professor/courses/:id/lectures` - Index [Details](#index-lectures-)
- `GET - api/v1/professor/courses/:id/lectures/:id` - Show [Details](#show-lecture-)
- `PATCH - api/v1/professor/courses/:id/lectures/:id` - Update [Details](#update-lecture-)
- `DELETE - api/v1/professor/courses/:id/lectures/:id` - Delete [Details](#delete-lecture-)

##### LECTURE RESOURCE ⭐

- `POST - api/v1/professor/courses/:id/lectures/:id/resources` - Create [Details](#create-lecture-resource-)
- `GET - api/v1/professor/courses/:id/lectures/:id/resources` - Index [Details](#index-lecture-resources-)
- `GET - api/v1/professor/courses/:id/lectures/:id/resources/:id` - Show [Details](#show-lecture-resource-)
- `PATCH - api/v1/professor/courses/:id/lectures/:id/resources/:id` - Update [Details](#update-lecture-resource-)
- `DELETE - api/v1/professor/courses/:id/lectures/:id/resources/:id` - Delete [Details](#delete-lecture-resource-)

##### QUICK INDEX ⭐

- `GET - api/v1/professor/universities/:id/collages/:id/levels` - levels [Details](#index-levels-professor-)
- `GET - api/v1/professor/universities/:id/collages/:id/levels/:id/programs` - programs [Details](#index-programs-professor-)
- `GET - api/v1/professor/universities/:id/collages/:id/levels/:id/programs/:id/departments` - departments [Details](#index-departments-professor-)

##### ATTENDANCE ( QR CODE & LOCATION ) ⭐

- `POST - api/v1/professor/courses/:id/lectures/:id/attendance` - Create [Details](#create-attendance-)
- `GET - api/v1/professor/courses/:id/lectures/:id/attendance/:id` - Show [Details](#show-attendance-)
- `GET - api/v1/professor/courses/:id/lectures/:id/attendance/:id/students` - Index Students [Details](#index-attendance-students-)
- `DELETE - api/v1/professor/courses/:id/lectures/:id/attendance/:id/students/:id` - Delete Student [Details](#delete-attendance-student-)

##### COURSE ASSIGNMENT ⭐

- `POST - api/v1/professor/courses/:id/assignments` - Create [Details](#create-course-assignment-)
- `GET - api/v1/professor/courses/:id/assignments` - Index [Details](#index-course-assignments-)
- `GET - api/v1/professor/courses/:id/assignments/:id` - Show [Details](#show-course-assignment-)
- `PATCH - api/v1/professor/courses/:id/assignments/:id` - Update [Details](#update-course-assignment-)
- `DELETE - api/v1/professor/courses/:id/assignments/:id` - Delete [Details](#delete-course-assignment-)

##### COURSE ASSIGNMENT SUBMISSIONS ⭐

- `GET - api/v1/professor/courses/:id/assignments/:id/submissions` - Index [Details](#index-course-assignment-submissions-)
- `GET - api/v1/professor/courses/:id/assignments/:id/submissions/:id` - Show [Details](#show-course-assignment-submission-)

##### EXAM ⭐

- `POST - api/v1/professor/courses/:id/exams` - Create [Details](#create-exam-)
- `POST - api/v1/professor/courses/:id/exams/:id/start-now` - Start now [Details](#start-now-exam-)
- `GET - api/v1/professor/courses/:id/exams` - Index [Details](#index-exams-)
- `GET - api/v1/professor/courses/:id/exams/:id` - Show [Details](#show-exam-)
- `PATCH - api/v1/professor/courses/:id/exams/:id` - Update [Details](#update-exam-)
- `DELETE - api/v1/professor/courses/:id/exams/:id` - Delete [Details](#delete-exam-)

##### EXAM ENROLLMENTS ⭐

- `GET - api/v1/professor/courses/:id/exams/:id/enrollments` - Index [Details](#index-exam-enrollments-)

##### EXAM SUBMISSIONS ⭐

- `GET - api/v1/professor/courses/:id/exams/:id/submissions` - Index [Details](#index-exam-submissions-)

##### EXAM QUESTIONS ( Text and/or Image or both ) ⭐

- `POST - api/v1/professor/courses/:id/exams/:id/questions` - Create [Details](#create-exam-question-)
- `GET - api/v1/professor/courses/:id/exams/:id/questions` - Index [Details](#index-exam-questions-)
- `GET - api/v1/professor/courses/:id/exams/:id/questions/:id` - Show [Details](#show-exam-question-)
- `PATCH - api/v1/professor/courses/:id/exams/:id/questions/:id` - Update [Details](#update-exam-question-)
- `DELETE - api/v1/professor/courses/:id/exams/:id/questions/:id` - Delete [Details](#delete-exam-question-)

##### EXAM QUESTION ANSWERS ⭐

- `PATCH - api/v1/professor/courses/:id/exams/:id/questions/:id/answers/:id` - Update [Details](#update-exam-question-answer-)

#### ASSISTANT 👨‍🏫

##### ACCESS PERMISSOIN ⭐

- `GET - api/v1/assistant/:id` - Show [Details](#show-assistant-)
- `PATCH - api/v1/assistant/:id` - Update [Details](#update-assistant-)

##### COURSE ⭐

- `GET - api/v1/assistant/courses` - Index [Details](#index-courses-assistant-)
- `GET - api/v1/assistant/courses/:id` - Show [Details](#show-course-assistant-)

##### SECTION ⭐

- `POST - api/v1/assistant/courses/:id/sections` - Create [Details](#create-section-assistant-)
- `GET - api/v1/assistant/courses/:id/sections` - Index [Details](#index-sections-assistant-)
- `GET - api/v1/assistant/courses/:id/sections/:id` - Show [Details](#show-section-assistant-)
- `PATCH - api/v1/assistant/courses/:id/sections/:id` - Update [Details](#update-section-assistant-)
- `DELETE - api/v1/assistant/courses/:id/sections/:id` - Delete [Details](#delete-section-assistant-)

##### SECTION RESOURCES ⭐

- `POST - api/v1/assistant/courses/:id/sections/:id/resources` - Create [Details](#create-section-resource-assistant-)
- `GET - api/v1/assistant/courses/:id/sections/:id/resources` - Index [Details](#index-section-resources-assistant-)
- `GET - api/v1/assistant/courses/:id/sections/:id/resources/:id` - Show [Details](#show-section-resource-assistant-)
- `PATCH - api/v1/assistant/courses/:id/sections/:id/resources/:id` - Update [Details](#update-section-resource-assistant-)
- `DELETE - api/v1/assistant/courses/:id/sections/:id/resources/:id` - Delete [Details](#delete-section-resource-assistant-)

##### ATTENDANCE ( QR CODE & LOCATION ) ⭐

- `POST - api/v1/assistant/courses/:id/sections/:id/attendance` - Create [Details](#create-attendance-assistant-)
- `GET - api/v1/assistant/courses/:id/sections/:id/attendance/:id` - Show [Details](#show-attendance-assistant-)
- `GET - api/v1/assistant/courses/:id/sections/:id/attendance/:id/students` - Index Students [Details](#index-attendance-assistant-students-)
- `DELETE - api/v1/assistant/courses/:id/sections/:id/attendance/:id/students/:id` - Delete Student [Details](#delete-attendance-assistant-student-)

##### ASSIGNMENT ⭐

- `POST - api/v1/assistant/courses/:id/sections/:id/assignments` - Create [Details](#create-section-assignment-assistant-)
- `GET - api/v1/assistant/courses/:id/sections/:id/assignments` - Index [Details](#index-section-assignments-assistant-)
- `GET - api/v1/assistant/courses/:id/sections/:id/assignments/:id` - Show [Details](#show-section-assignment-assistant-)
- `PATCH - api/v1/assistant/courses/:id/sections/:id/assignments/:id` - Update [Details](#update-section-assignment-assistant-)
- `DELETE - api/v1/assistant/courses/:id/sections/:id/assignments/:id` - Delete [Details](#delete-section-assignment-assistant-)

##### ASSIGNMENT SUBMISSIONS ⭐

- `GET - api/v1/assistant/courses/:id/sections/:id/assignments/:id/submissions` - Index [Details](#index-section-assignment-submissions-assistant-)
- `GET - api/v1/assistant/courses/:id/sections/:id/assignments/:id/submissions/:id` - Show [Details](#show-section-assignment-submission-assistant-)

#### STUDENT 👨‍🎓

##### ACCESS PERMISSOIN ⭐

- `GET - api/v1/student/:id` - Show [Details](#show-student-)

##### COURSE ⭐

- `GET - api/v1/student/courses` - Index [Details](#index-courses-student-)
- `GET - api/v1/student/courses/:id` - Show [Details](#show-course-student-)
- `POST - api/v1/student/courses/:id/enroll` - Enroll [Details](#enroll-course-student-)

##### COURSE EXAM ⭐

- `GET - api/v1/student/courses/:id/exams` - Index [Details](#index-course-exams-student-)
- `POST - api/v1/student/courses/:id/exams/:id/enroll` - Enroll [Details](#enroll-course-exam-student-)
- `POST - api/v1/student/courses/:id/exams/:id/submit` - Submit [Details](#submit-course-exam-student-)

##### COURSE ASSIGNMENT ⭐

- `GET - api/v1/student/courses/:id/assignments` - Index [Details](#index-course-assignments-student-)
- `GET - api/v1/student/courses/:id/assignments/:id` - Show [Details](#show-course-assignments-student-)
- `POST - api/v1/student/courses/:id/assignments/:id/submit` - Submit [Details](#submit-course-assignment-student-)

##### COURSE ASSISTANTS ⭐

- `GET - api/v1/student/courses/:id/assistants` - Index [Details](#index-course-assistants-student-)

##### SECTION ⭐

- `GET - api/v1/student/courses/:id/assistants/:id/sections` - Index [Details](#index-sections-student-)
- `GET - api/v1/student/courses/:id/assistants/:id/sections/:id` - Show [Details](#show-section-student-)

##### SECTION RESOURCES ⭐

- `GET - api/v1/student/courses/:id/assistants/:id/sections/:id/resources` - Index [Details](#index-section-resources-student-)

##### SECTION ASSIGNMENT ⭐

- `GET - api/v1/student/courses/:id/assistants/:id/sections/:id/assignments` - Index [Details](#index-section-assignments-student-)
- `GET - api/v1/student/courses/:id/assistants/:id/sections/:id/assignments/:id` - Show [Details](#show-section-assignment-student-)
- `POST - api/v1/student/courses/:id/assistants/:id/sections/:id/assignments/:id/submit` - Submit [Details](#submit-section-assignment-student-)

##### SECTION ATTENDANCE ⭐

- `GET - api/v1/student/courses/:id/assistants/:id/sections/:id/attendance/:id` - Show [Details](#show-section-attendance-student-)
- `POST - api/v1/student/courses/:id/assistants/:id/sections/:id/attendance/:id/attend` - Attend [Details](#attend-section-attendance-student-)

##### LECTURE ⭐

- `GET - api/v1/student/courses/:id/lectures` - Index [Details](#index-lectures-student-)
- `GET - api/v1/student/courses/:id/lectures/:id` - Show [Details](#show-lecture-student-)

##### LECTURE RESOURCES ⭐

- `GET - api/v1/student/courses/:id/lectures/:id/resources` - Index [Details](#index-lecture-resources-student-)

##### LECTURE ATTENDANCE ⭐

- `GET - api/v1/student/courses/:id/lectures/:id/attendance/:id` - Show [Details](#show-lecture-attendance-student-)
- `POST - api/v1/student/courses/:id/lectures/:id/attendance/:id/attend` - Attend [Details](#attend-lecture-attendance-student-)

##### CONTACTS ⭐

- `GET - api/v1/contacts/:id` - Show [Details](#show-contact-)
- `PATCH - api/v1/contacts/:id` - Update [Details](#update-contact-)

##### STORAGE ⭐

- `POST - api/v1/storage/:id` - Upload [Details](#upload-storage-)
- `GET - api/v1/storage/:id` - Access [Details](#access-storage-)

### All Endpoints (in details) 📡

#### Authentication 🔐

##### Login 📥

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/auth/login`
- _Headers:_ `Content-Type: application/json`
- _Request Body:_

  ```json
  {
    "username": "username-UNIQUE", // MIN: 2 - MAX: 50
    "password": "Pass44#", // MIN: 5 - MAX: 50
    "role": "master" // OPTIONS - master, admin, user, student, assistant
  }
  ```

- _Success Response:_

  ```json
  {
    "status": "success",
    "message": "Master logged in successfully",
    "data": {
      "role": "master",
      "id": "642de3f48fcd08239f55f69a",
      "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8"
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    username: 'mohamed475',
    password: 'hodla475',
    role: 'master',
  });

  let response = await fetch('http://localhost:3000/api/v1/auth/login', {
    method: 'POST',
    body: bodyContent,
    headers: headersList,
  });

  let data = await response.text();
  console.log(data);
  ```

#### MASTER 🔑

##### UNIVERSITY ⭐

###### Index universities 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/master/universities`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`
  ```json
  {
    "status": "success",
    "message": "Universities retrieved successfully",
    "data": {
      "universitiesCount": 2,
      "universities": [
        {
          "_id": "642deaa976e91123782b7f16",
          "name": "alu",
          "city": "alexandria",
          "country": "egypt",
          "collages": [],
          "createdAt": "2023-04-05T21:39:53.253Z",
          "updatedAt": "2023-04-05T21:39:53.253Z",
          "id": "642deaa976e91123782b7f16"
        },
        {
          "_id": "642dea4b76e91123782b7f10",
          "name": "kfu",
          "city": "kafr elsheikh",
          "country": "egypt",
          "collages": [],
          "createdAt": "2023-04-05T21:38:19.512Z",
          "updatedAt": "2023-04-05T21:38:19.512Z",
          "id": "642dea4b76e91123782b7f10"
        }
      ]
    }
  }
  ```
- _Example - JS_:

  ```js
  let headersList = {
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MjkwOTYsImV4cCI6MTY4MzMyMTA5Nn0.I1OSJJ3RywdmodyvYvRu2bN-2tEwPWbEEyceFCYmTS0',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Create university 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/master/universities`
- _Headers:_ `Authorization`
- _Request Body:_

  ```json
  {
    "name": "ALU", // MIN: 2 - MAX: 50
    "city": "Alexandria", // MIN: 2 - MAX: 50
    "country": "egypt" // MIN: 2 - MAX: 50
  }
  ```

- _Success Response:_ `201`
  ```json
  {
    "status": "success",
    "message": "University created successfully",
    "data": {
      "university": {
        "id": "642df520c6fee003857cde93"
      }
    }
  }
  ```
- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MjkwOTYsImV4cCI6MTY4MzMyMTA5Nn0.I1OSJJ3RywdmodyvYvRu2bN-2tEwPWbEEyceFCYmTS0',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'ALU',
    city: 'Alexandria',
    country: 'Egypt',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show university 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/master/universities/:universityId`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`
  ```json
  {
    "status": "success",
    "message": "University retrieved successfully",
    "data": {
      "university": {
        "_id": "642deaa976e91123782b7f16",
        "name": "alu",
        "city": "alex",
        "country": "egypt",
        "collages": ["642deda276e91123782b7f94"],
        "createdAt": "2023-04-05T21:39:53.253Z",
        "updatedAt": "2023-04-05T21:56:24.813Z",
        "id": "642deaa976e91123782b7f16"
      }
    }
  }
  ```
- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MjkwOTYsImV4cCI6MTY4MzMyMTA5Nn0.I1OSJJ3RywdmodyvYvRu2bN-2tEwPWbEEyceFCYmTS0',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update university 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/master/universities/:universityId`
- _Headers:_ `Authorization`
- _Request Body:_

  ```json
  {
    "name": "ALU", // MIN: 2 - MAX: 50
    "city": "Alexandria", // MIN: 2 - MAX: 50
    "country": "egypt" // MIN: 2 - MAX: 50
  }
  ```

- _Success Response:_ `200`
  ```json
  {
    "status": "success",
    "message": "University updated successfully",
    "data": {
      "university": {
        "_id": "642deaa976e91123782b7f16",
        "name": "alu",
        "city": "alex",
        "country": "egypt",
        "collages": [],
        "createdAt": "2023-04-05T21:39:53.253Z",
        "updatedAt": "2023-04-05T21:41:25.137Z",
        "id": "642deaa976e91123782b7f16"
      }
    }
  }
  ```
- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MjkwOTYsImV4cCI6MTY4MzMyMTA5Nn0.I1OSJJ3RywdmodyvYvRu2bN-2tEwPWbEEyceFCYmTS0',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'alu',
    city: 'Alex',
    country: 'Egypt',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete university 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/master/universities/:universityId`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "University deleted successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MjkwOTYsImV4cCI6MTY4MzMyMTA5Nn0.I1OSJJ3RywdmodyvYvRu2bN-2tEwPWbEEyceFCYmTS0',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642df520c6fee003857cde93',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### COLLAGE TYPE ⭐

###### Create collage type 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/master/collage-types`
- _Headers:_ `Authorization`
- _Request Body:_

  ```json
  {
    "name": "Faculty of Engineering" // MIN: 2 - MAX: 50
  }
  ```

- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Collage type created successfully",
    "data": {
      "collageType": {
        "id": "642e33a399182e5e2d14ec47"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MjkwOTYsImV4cCI6MTY4MzMyMTA5Nn0.I1OSJJ3RywdmodyvYvRu2bN-2tEwPWbEEyceFCYmTS0',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'engineering',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/master/collage-types',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );
  let data = await response.text();
  console.log(data);
  ```

###### Index collage types 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/master/collage-types`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Collage types fetched successfully",
    "data": {
      "collageTypesCount": 3,
      "collageTypes": [
        {
          "_id": "642e33a399182e5e2d14ec47",
          "name": "engineering"
        },
        {
          "_id": "642debc776e91123782b7f38",
          "name": "engineering"
        },
        {
          "_id": "642deb9c76e91123782b7f35",
          "name": "computer science"
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MjkwOTYsImV4cCI6MTY4MzMyMTA5Nn0.I1OSJJ3RywdmodyvYvRu2bN-2tEwPWbEEyceFCYmTS0',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/collage-types',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show collage type 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/master/collage-types/:collageTypeId`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Collage type fetched successfully",
    "data": {
      "collageType": {
        "_id": "642debc776e91123782b7f38",
        "name": "engineering",
        "createdAt": "2023-04-05T21:44:39.114Z",
        "updatedAt": "2023-04-05T21:44:39.114Z",
        "__v": 0
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MjkwOTYsImV4cCI6MTY4MzMyMTA5Nn0.I1OSJJ3RywdmodyvYvRu2bN-2tEwPWbEEyceFCYmTS0',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/collage-types/642debc776e91123782b7f38',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update collage type 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/master/collage-types/:collageTypeId`
- _Headers:_ `Authorization`
- _Request Body:_

  ```json
  {
    "name": "Faculty of Engineering" // MIN: 2 - MAX: 50
  }
  ```

- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Collage type updated successfully",
    "data": {
      "collageType": {
        "_id": "642e33a399182e5e2d14ec47",
        "name": "type name",
        "createdAt": "2023-04-06T02:51:15.552Z",
        "updatedAt": "2023-04-06T03:11:29.284Z",
        "__v": 0
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MjkwOTYsImV4cCI6MTY4MzMyMTA5Nn0.I1OSJJ3RywdmodyvYvRu2bN-2tEwPWbEEyceFCYmTS0',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'testf',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/master/collage-types/642e33a399182e5e2d14ec47',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete collage type 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/master/collage-types/:collageTypeId`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Collage type removed successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MjkwOTYsImV4cCI6MTY4MzMyMTA5Nn0.I1OSJJ3RywdmodyvYvRu2bN-2tEwPWbEEyceFCYmTS0',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/collage-types/642e33a399182e5e2d14ec47',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### Collages ⭐

###### Create collage 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages`
- _Headers:_ `Authorization`
- _Request Body:_

  ```json
  {
    "name": "fuculty of engineering",
    "type": "642debc776e91123782b7f38"
  }
  ```

- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Collage created successfully",
    "data": {
      "collage": {
        "name": "fuculty of engineering",
        "university": "642deaa976e91123782b7f16",
        "levels": [],
        "type": "642debc776e91123782b7f38",
        "professors": [],
        "assistants": [],
        "_id": "642e3cb699182e5e2d14ec59",
        "createdAt": "2023-04-06T03:29:58.750Z",
        "updatedAt": "2023-04-06T03:29:58.750Z",
        "__v": 0,
        "id": "642e3cb699182e5e2d14ec59"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'fuculty of engineering',
    type: '642debc776e91123782b7f38',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index collages 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Collage fetched successfully",
    "data": {
      "collagesCount": 2,
      "collages": [
        {
          "_id": "642e3cb699182e5e2d14ec59",
          "name": "fuculty of engineering",
          "university": "642deaa976e91123782b7f16",
          "levels": [],
          "type": {
            "_id": "642debc776e91123782b7f38",
            "name": "engineering",
            "createdAt": "2023-04-05T21:44:39.114Z",
            "updatedAt": "2023-04-05T21:44:39.114Z",
            "__v": 0,
            "id": "642debc776e91123782b7f38"
          },
          "professors": [],
          "assistants": [],
          "createdAt": "2023-04-06T03:29:58.750Z",
          "updatedAt": "2023-04-06T03:29:58.750Z",
          "__v": 0,
          "id": "642e3cb699182e5e2d14ec59"
        },
        {
          "_id": "642deda276e91123782b7f94",
          "name": "fuculty of computer & information",
          "university": "642deaa976e91123782b7f16",
          "levels": ["642def5b76e91123782b7ff5"],
          "type": {
            "_id": "642deb9c76e91123782b7f35",
            "name": "computer science",
            "createdAt": "2023-04-05T21:43:56.305Z",
            "updatedAt": "2023-04-05T21:43:56.305Z",
            "__v": 0,
            "id": "642deb9c76e91123782b7f35"
          },
          "professors": ["642df3d32c8448c0a089af25"],
          "createdAt": "2023-04-05T21:52:34.815Z",
          "updatedAt": "2023-04-05T22:23:02.145Z",
          "__v": 6,
          "assistants": [],
          "id": "642deda276e91123782b7f94"
        }
      ],
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show collage 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Collage fetched successfully",
    "data": {
      "collage": {
        "_id": "642deda276e91123782b7f94",
        "name": "fuculty of computer & information",
        "university": "642deaa976e91123782b7f16",
        "levels": ["642def5b76e91123782b7ff5"],
        "type": {
          "_id": "642deb9c76e91123782b7f35",
          "name": "computer science",
          "createdAt": "2023-04-05T21:43:56.305Z",
          "updatedAt": "2023-04-05T21:43:56.305Z",
          "__v": 0,
          "id": "642deb9c76e91123782b7f35"
        },
        "professors": ["642df3d32c8448c0a089af25"],
        "assistants": [],
        "id": "642deda276e91123782b7f94"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642deda276e91123782b7f94',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update collage 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id`
- _Headers:_ `Authorization`
- _Request Body:_

  ```json
  {
    "name": "fuculty of computer & information",
    "type": "642deb9c76e91123782b7f35"
  }
  ```

- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Collage updated successfully",
    "data": {
      "updatedCollage": {
        "_id": "642deda276e91123782b7f94",
        "name": "fuculty of computer & information",
        "university": "642deaa976e91123782b7f16",
        "levels": ["642def5b76e91123782b7ff5"],
        "type": "642deb9c76e91123782b7f35",
        "professors": ["642df3d32c8448c0a089af25"],
        "createdAt": "2023-04-05T21:52:34.815Z",
        "updatedAt": "2023-04-05T22:23:02.145Z",
        "__v": 6,
        "assistants": [],
        "id": "642deda276e91123782b7f94"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'fuculty of computer & information',
    type: '642deb9c76e91123782b7f35',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642deda276e91123782b7f94',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete collage 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Collage removed successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642deda276e91123782b7f94',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### LEVEL ⭐

###### Create level 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id/levels`
- _Headers:_ `Authorization`
- _Request Body:_

  ```json
  {
    "name": "level 01"
  }
  ```

- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Level created successfully",
    "data": {
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'level 01',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index levels 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id/levels`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Levels fetched successfully",
    "data": {
      "levelsCount": 1,
      "levels": [
        {
          "_id": "642ee7f789a92ceeba6b7a4f",
          "name": "level 01",
          "programs": [],
          "collage": "642e3cb699182e5e2d14ec59",
          "university": "642deaa976e91123782b7f16",
          "admins": [],
          "createdAt": "2023-04-06T15:40:40.000Z",
          "updatedAt": "2023-04-06T15:40:40.000Z",
          "__v": 0,
          "id": "642ee7f789a92ceeba6b7a4f"
        }
      ],
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show level 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id/levels/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Level fetched successfully",
    "data": {
      "level": {
        "_id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01",
        "programs": [],
        "collage": "642e3cb699182e5e2d14ec59",
        "university": "642deaa976e91123782b7f16",
        "admins": [],
        "id": "642ee7f789a92ceeba6b7a4f"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update level 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id/levels/:id`
- _Headers:_ `Authorization`
- _Request Body:_

  ```json
  {
    "name": "level 01"
  }
  ```

- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Level updated successfully",
    "data": {
      "level": {
        "_id": "642eea412a5ae844ca7b8f6f",
        "name": "updated level",
        "programs": [],
        "collage": "642e3cb699182e5e2d14ec59",
        "university": "642deaa976e91123782b7f16",
        "admins": [],
        "createdAt": "2023-04-06T15:50:25.890Z",
        "updatedAt": "2023-04-06T15:50:33.105Z",
        "__v": 0,
        "id": "642eea412a5ae844ca7b8f6f"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'updated level',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642eea412a5ae844ca7b8f6f',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete level 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id/levels/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Level deleted successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642eea412a5ae844ca7b8f6f',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### ADMIN ⭐

###### Create admin 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id/levels/:id/admins`
- _Headers:_ `Authorization`
- _Request Body:_

  ```json
  {
    "name": "admin 02",
    "email": "admin02@mail.com", // UNIQUE
    "password": "adminpassword",
    "username": "uni-admin-02" // UNIQUE
  }
  ```

- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Admin created successfully",
    "data": {
      "admin": {
        "id": "642eed3c977ee3f83d97f332"
      },
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'admin 02',
    email: 'adminf02@mail.com',
    password: 'adminpassword',
    username: 'unfi-admin-02f',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/admins',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index admins 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id/levels/:id/admins`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Admins fetched successfully",
    "data": {
      "adminsCount": 2,
      "admins": [
        {
          "id": "642eed3c977ee3f83d97f332",
          "createdAt": "2023-04-06T16:03:08.499Z",
          "name": "admin 02"
        },
        {
          "id": "642eecde2a5ae844ca7b8f8a",
          "createdAt": "2023-04-06T16:01:34.509Z",
          "name": "admin 02"
        }
      ],
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/admins',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show admin 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id/levels/:id/admins/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Admin fetched successfully",
    "data": {
      "admin": {
        "id": "642eed3c977ee3f83d97f332",
        "createdAt": "2023-04-06T16:03:08.499Z",
        "name": "admin 02",
        "username": "unfi-admin-02f",
        "email": "adminf02@mail.com",
        "qrCode": "642eed3c977ee3f83d97f330"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/admins/642eed3c977ee3f83d97f332',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update admin 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id/levels/:id/admins/:id`
- _Headers:_ `Authorization`
- _Request Body:_

  ```json
  {
    "name": "admin updated name",
    "email": "newemail@gmail.com"
  }
  ```

- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Admin updated successfully",
    "data": {
      "admin": {
        "id": "642eed3c977ee3f83d97f332",
        "createdAt": "2023-04-06T16:03:08.499Z",
        "name": "admin updated name",
        "username": "unfi-admin-02f",
        "email": "newemail@gmail.com",
        "qrCode": "642eed3c977ee3f83d97f330"
      },
      "university": "alu",
      "collage": "fuculty of engineering",
      "level": "level 01"
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'admooosna-MASTER',
    email: 'dsf@gmail.com',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/admins/642eed3c977ee3f83d97f332',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete admin 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id/levels/:id/admins/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Admin deleted successfully  ",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/admins/642eed3c977ee3f83d97f332',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### PROFESSOR ⭐

###### Create professor 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id/professors`
- _Headers:_ `Authorization`
- _Request Body:_
  ```json
  {
    "name": "Mohamed Yasser",
    "password": "passCode96$",
    "username": "iammohamedyasser",
    "academicId": "120120120120"
  }
  ```
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Professor created successfully",
    "data": {
      "professor": {
        "id": "64304c1b3eea93f118839bff"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'Mohamed Yasser',
    password: 'ljslk',
    username: 'mov47f5',
    academicId: '120120120120',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/professors',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index professors 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id/professors`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Professors fetched successfully",
    "data": {
      "professorsCount": 1,
      "professors": [
        {
          "id": "64304c1b3eea93f118839bff",
          "createdAt": "2023-04-07T17:00:11.784Z",
          "name": "mohamed yasser",
          "academicId": "120120120120",
          "courses": []
        }
      ],
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/professors',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show professor 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id/professors/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Professor fetched successfully",
    "data": {
      "professor": {
        "id": "64304c1b3eea93f118839bff",
        "name": "mohamed yasser",
        "username": "mov47f5",
        "academicId": "120120120120",
        "qrCode": "64304c1b3eea93f118839bfb",
        "courses": [],
        "assistants": [],
        "contacts": "64304c1b3eea93f118839bfd"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/professors/64304c1b3eea93f118839bff',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update professor 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id/professors/:id`
- _Headers:_ `Authorization`
- _Request Body:_
  ```json
  {
    "name": "Dr. Ahmed Elashry",
    "academicId": "99999999999"
  }
  ```
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Professor updated successfully",
    "data": {
      "professor": {
        "id": "64304c1b3eea93f118839bff",
        "name": "Dr. Ahmed Elashry",
        "academicId": "99999999999"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'ali ali',
    academicId: '99999999999',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/professors/64304c1b3eea93f118839bff',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete professor 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id/professors/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Professor deleted successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/professors/64304c1b3eea93f118839bff',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

#### ADMIN 👔

##### PROGRAM ⭐

###### Create program 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/admin/universities/:id/collages/:id/levels/:id/programs`
- _Headers:_ `Authorization`
- _Request Body:_
  ```json
  {
    "name": "private", // [private, public]
    "tuitionFees": "1000",
    "currency": "EGP" // [EGP, USD, EUR]
  }
  ```
- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Program created successfully",
    "data": {
      "program": {
        "name": "private",
        "tuitionFees": {
          "value": 1000,
          "currency": "EGP"
        },
        "departments": [],
        "collage": "642e3cb699182e5e2d14ec59",
        "level": "642ee7f789a92ceeba6b7a4f",
        "university": "642deaa976e91123782b7f16",
        "_id": "643052c63eea93f118839c53",
        "createdAt": "2023-04-07T17:28:38.180Z",
        "updatedAt": "2023-04-07T17:28:38.180Z",
        "__v": 0,
        "id": "643052c63eea93f118839c53"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'private',
    tuitionFees: '1000',
    currency: 'EGP',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index programs 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/admin/universities/:id/collages/:id/levels/:id/programs`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Programs fetched successfully",
    "data": {
      "programsCount": 1,
      "programs": [
        {
          "tuitionFees": {
            "value": 1000,
            "currency": "EGP"
          },
          "_id": "643052a83eea93f118839c46",
          "name": "public",
          "departments": [],
          "collage": "642e3cb699182e5e2d14ec59",
          "level": "642ee7f789a92ceeba6b7a4f",
          "university": "642deaa976e91123782b7f16",
          "createdAt": "2023-04-07T17:28:08.091Z",
          "updatedAt": "2023-04-07T17:28:08.091Z",
          "__v": 0,
          "id": "643052a83eea93f118839c46"
        }
      ],
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show program 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Programs fetched successfully",
    "data": {
      "programsCount": 1,
      "programs": [
        {
          "tuitionFees": {
            "value": 1000,
            "currency": "EGP"
          },
          "_id": "643052a83eea93f118839c46",
          "name": "public",
          "departments": [],
          "collage": "642e3cb699182e5e2d14ec59",
          "level": "642ee7f789a92ceeba6b7a4f",
          "university": "642deaa976e91123782b7f16",
          "createdAt": "2023-04-07T17:28:08.091Z",
          "updatedAt": "2023-04-07T17:28:08.091Z",
          "__v": 0,
          "id": "643052a83eea93f118839c46"
        }
      ],
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052a83eea93f118839c46',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update program 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `name, tuitionFees`

  ```json
  {
    "name": "public", // [public, private]
    "tuitionFees": "900",
    "currency": "USD" // [USD, EGP, EUR]
  }
  ```

- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Program updated successfully",
    "data": {
      "program": {
        "id": "643052c63eea93f118839c53",
        "name": "public",
        "tuitionFees": {
          "value": 900,
          "currency": "USD"
        }
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'public',
    tuitionFees: '900',
    currency: 'USD',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052c63eea93f118839c53',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete program 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Program deleted successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052c63eea93f118839c53',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

- `POST - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments` - Create [Details](#create-department-)
- `GET - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments` - Index [Details](#index-departments-)
- `GET - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id` - Show [Details](#show-department-)
- `PATCH - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id` - Update [Details](#update-department-)
- `DELETE - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id` - Delete [Details](#delete-department-)

##### DEPARTMENT ⭐

###### Create department 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments`
- _Headers:_ `Authorization`
- _Request Body:_ `name`

  ```json
  {
    "name": "computer science",
    "extraTuitionFees": "1000",
    "currency": "USD" // [USD, EGP, EUR]
  }
  ```

- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Department created successfully",
    "data": {
      "department": {
        "id": "64305ac8ee3e783bbc680624"
      },
      "program": {
        "id": "643052a83eea93f118839c46",
        "name": "public"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'computer science',
    extraTuitionFees: '1000',
    currency: 'egp',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052a83eea93f118839c46/departments',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index departments 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Departments fetched successfully",
    "data": {
      "departmentsCount": 1,
      "departments": [
        {
          "extraTuitionFees": {
            "value": 1000,
            "currency": "EGP"
          },
          "_id": "6430596c112031c1dbfc3fd8",
          "name": "computer science",
          "courses": [],
          "program": "643052a83eea93f118839c46",
          "level": "642ee7f789a92ceeba6b7a4f",
          "collage": "642e3cb699182e5e2d14ec59",
          "university": "642deaa976e91123782b7f16",
          "students": [],
          "createdAt": "2023-04-07T17:57:00.104Z",
          "updatedAt": "2023-04-07T17:57:00.104Z",
          "__v": 0,
          "id": "6430596c112031c1dbfc3fd8"
        }
      ],
      "program": {
        "id": "643052a83eea93f118839c46",
        "name": "public"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052a83eea93f118839c46/departments',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show department 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Department fetched successfully",
    "data": {
      "department": {
        "extraTuitionFees": {
          "value": 1000,
          "currency": "EGP"
        },
        "_id": "6430596c112031c1dbfc3fd8",
        "name": "computer science",
        "courses": [],
        "program": "643052a83eea93f118839c46",
        "level": "642ee7f789a92ceeba6b7a4f",
        "collage": "642e3cb699182e5e2d14ec59",
        "university": "642deaa976e91123782b7f16",
        "students": [],
        "createdAt": "2023-04-07T17:57:00.104Z",
        "updatedAt": "2023-04-07T17:57:00.104Z",
        "__v": 0,
        "id": "6430596c112031c1dbfc3fd8"
      },
      "program": {
        "id": "643052a83eea93f118839c46",
        "name": "public"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052a83eea93f118839c46/departments/6430596c112031c1dbfc3fd8',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update department 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `name`, `extraTuitionFees`

  ```json
  {
    "name": "Information System",
    "extraTuitionFees": "100000",
    "currency": "EUR" // [EGP, USD, EUR]
  }
  ```

- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Department updated successfully",
    "data": {
      "department": {
        "id": "643059a6112031c1dbfc3fed",
        "name": "se",
        "extraTuitionFees": {
          "value": 100000,
          "currency": "EUR"
        }
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'Information System',
    extraTuitionFees: '100000',
    currency: 'EUR',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052a83eea93f118839c46/departments/643059a6112031c1dbfc3fed',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete department 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`

- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Department deleted successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052a83eea93f118839c46/departments/64305ac8ee3e783bbc680624',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### Student ⭐

###### Create student 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id/students`
- _Headers:_ `Authorization`
- _Request Body:_

  ```json
  {
    "name": "Mohamed Yasser",
    "password": "passCodee75&",
    "username": "mohamedyasser459f",
    "academicId": "9879873833"
  }
  ```

- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Student created successfully",
    "data": {
      "student": {
        "id": "6430629f9cd224306d04b332"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01"
      },
      "program": {
        "id": "643052a83eea93f118839c46",
        "name": "public"
      },
      "department": {
        "id": "6430596c112031c1dbfc3fd8",
        "name": "computer science"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'Mohamed Yasser',
    password: 'passCodee75&',
    username: 'mohamedyasser459f',
    academicId: '9879873833',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052a83eea93f118839c46/departments/6430596c112031c1dbfc3fd8/students',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index students 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id/students`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Students fetched successfully",
    "data": {
      "studentsCount": 1,
      "students": [
        {
          "id": "643061a4ee3e783bbc680640",
          "createdAt": "2023-04-07T18:32:04.111Z",
          "name": "mohamed yasser",
          "academicId": "9879873833",
          "courses": []
        }
      ],
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01"
      },
      "program": {
        "id": "643052a83eea93f118839c46",
        "name": "public"
      },
      "department": {
        "id": "6430596c112031c1dbfc3fd8",
        "name": "computer science"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052a83eea93f118839c46/departments/6430596c112031c1dbfc3fd8/students',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id/students/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Student fetched successfully",
    "data": {
      "student": {
        "id": "643061a4ee3e783bbc680640",
        "createdAt": "2023-04-07T18:32:04.111Z",
        "name": "mohamed yasser",
        "academicId": "9879873833",
        "courses": [],
        "qrCode": "643061a3ee3e783bbc68063c"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01"
      },
      "program": {
        "id": "643052a83eea93f118839c46",
        "name": "public"
      },
      "department": {
        "id": "6430596c112031c1dbfc3fd8",
        "name": "computer science"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052a83eea93f118839c46/departments/6430596c112031c1dbfc3fd8/students/643061a4ee3e783bbc680640',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update student 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id/students/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `name`, `academicId`

  ```json
  {
    "name": "mohamed yasser",
    "academicId": "9879873833"
  }
  ```

- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Student updated successfully",
    "data": {
      "student": {
        "id": "6430629f9cd224306d04b332",
        "name": "mohamed yasser",
        "academicId": "9879873833"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: '999',
    academicId: '999999999',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052a83eea93f118839c46/departments/6430596c112031c1dbfc3fd8/students/6430629f9cd224306d04b332',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete student 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id/students/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Student deleted successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052a83eea93f118839c46/departments/6430596c112031c1dbfc3fd8/students/6430629f9cd224306d04b332',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### QUICK ACCESS ⭐

###### Show admin level 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/admin/:id/levels/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Admin level fetched successfully",
    "data": {
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01",
        "programs": ["643052a83eea93f118839c46"]
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/643052073eea93f118839c3e/levels/642ee7f789a92ceeba6b7a4f',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### ACCESS PERMISSOIN ⭐

###### Show admin 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/admin/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Admin fetched successfully",
    "data": {
      "admin": {
        "id": "643052073eea93f118839c3e",
        "createdAt": "2023-04-07T17:25:27.277Z",
        "name": "admin 02",
        "username": "unfi-admin-02f",
        "email": "adminf02@mail.com",
        "qrCode": "643052073eea93f118839c3c"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/643052073eea93f118839c3e',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update admin 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/admin/:id`
- _Headers:_ `Authorization`
- _Request Body:_
  ```json
  {
    "name": "Mohamed Yasser",
    "email": "unista-ali@gmail.com"
  }
  ```
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Admin updated successfully",
    "data": {
      "admin": {
        "id": "643052073eea93f118839c3e",
        "name": "mohamed yasser",
        "email": "unista-ali@gmail.com"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'Mohamed Yasser',
    email: 'unista-ali@gmail.com',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/643052073eea93f118839c3e',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

#### PROFESSOR 👨‍🏫

- `GET - api/v1/professor/:id` - Show [Details](#show-professor-)
- `PATCH - api/v1/professor/:id` - Update [Details](#update-professor-)

##### ACCESS PERMISSOIN ⭐

###### Show professor 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Professor fetched successfully",
    "data": {
      "professor": {
        "id": "6430c7854e29a1ff8375d1e7",
        "createdAt": "2023-04-08T01:46:45.356Z",
        "name": "mohamed yasser",
        "username": "mov47f5",
        "academicId": "120120120120",
        "qrCode": "6430c7854e29a1ff8375d1e3",
        "courses": [],
        "contacts": "6430c7854e29a1ff8375d1e5"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/6430c7854e29a1ff8375d1e7',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update professor 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/professor/:id`
- _Headers:_ `Authorization`
- _Request Body:_
  ```json
  {
    "name": "Dr. Mohamed Yasser",
    "academicId": "4354353453453"
  }
  ```
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Professor updated successfully",
    "data": {
      "professor": {
        "id": "6430c7854e29a1ff8375d1e7",
        "name": "dr. mohamed yasser",
        "academicId": "4354353453453"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'Dr. Mohamed Yasser',
    academicId: '4354353453453',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/6430c7854e29a1ff8375d1e7',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### COURSE ⭐

###### Create course 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/professor/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id/courses`
- _Headers:_ `Authorization`
- _Request Body:_
  ```json
  {
    "name": "Machine Learning",
    "code": "CS45",
    "semester": "first" // [first, second, summer]
  }
  ```
- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Course created successfully",
    "data": {
      "course": {
        "id": "6430cc574e29a1ff8375d202"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'machine learning',
    code: 'CS45',
    semester: 'first',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052a83eea93f118839c46/departments/6430596c112031c1dbfc3fd8/courses',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete course 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/professor/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id/courses/:id`
- _Headers:_ `Authorization`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Course deleted successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052a83eea93f118839c46/departments/6430596c112031c1dbfc3fd8/courses/6430cc574e29a1ff8375d202',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index courses 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses`
- _Headers:_ `Authorization`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Courses fetched successfully",
    "data": {
      "coursesCount": 1,
      "courses": [
        {
          "_id": "6430ce43c3ca49b01012f8ca",
          "name": "machine learning",
          "code": "cs45",
          "semester": "first",
          "professor": "6430c7854e29a1ff8375d1e7",
          "assistants": [],
          "students": [],
          "lectures": [],
          "sections": [],
          "assignments": [],
          "exams": [],
          "department": "6430596c112031c1dbfc3fd8",
          "program": "643052a83eea93f118839c46",
          "level": "642ee7f789a92ceeba6b7a4f",
          "collage": "642e3cb699182e5e2d14ec59",
          "university": "642deaa976e91123782b7f16",
          "createdAt": "2023-04-08T02:15:31.406Z",
          "updatedAt": "2023-04-08T02:15:31.406Z",
          "__v": 0,
          "id": "6430ce43c3ca49b01012f8ca"
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch('http://localhost:3000/api/v1/professor/courses', {
    method: 'GET',
    headers: headersList,
  });

  let data = await response.text();
  console.log(data);
  ```

###### Show course 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id`
- _Headers:_ `Authorization`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Course fetched successfully",
    "data": {
      "course": {
        "_id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning",
        "code": "cs45",
        "semester": "first",
        "professor": {
          "_id": "6430c7854e29a1ff8375d1e7",
          "name": "dr. mohamed yasser"
        },
        "assistants": [],
        "students": [],
        "lectures": [],
        "sections": [],
        "assignments": [],
        "exams": [],
        "department": {
          "_id": "6430596c112031c1dbfc3fd8",
          "name": "computer science"
        },
        "program": {
          "_id": "643052a83eea93f118839c46",
          "name": "public"
        },
        "level": {
          "_id": "642ee7f789a92ceeba6b7a4f",
          "name": "level 01"
        },
        "collage": {
          "_id": "642e3cb699182e5e2d14ec59",
          "name": "fuculty of engineering"
        },
        "university": {
          "_id": "642deaa976e91123782b7f16",
          "name": "alu"
        },
        "createdAt": "2023-04-08T02:15:31.406Z",
        "updatedAt": "2023-04-08T02:15:31.406Z",
        "__v": 0
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update course 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/professor/courses/:id`
- _Headers:_ `Authorization`
- _Body:_
  ```json
  {
    "name": "updated",
    "code": "SE99",
    "semester": "second"
  }
  ```
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Course updated successfully",
    "data": {
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning",
        "code": "cs45",
        "semester": "first"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'machine learning',
    code: 'CS45',
    semester: 'first',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### EBOOK ⭐

###### Create ebook 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/professor/courses/:id/ebook`
- _Headers:_ `Authorization`
- _Body:_
  ```json
  {
    "name": "Machine Learning Course Ebook" // File should be of type pdf
  }
  ```
- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Upload successful",
    "data": {
      "eBook": {
        "path": "courses/6430ce43c3ca49b01012f8ca/eBook/e1116f01-6e04-4fb8-8f3a-c2e50ba19752.pdf",
        "type": "application/pdf",
        "name": "Machine Learning Course Ebook",
        "owner": "6430c7854e29a1ff8375d1e7",
        "_id": "6430d28595394133234b0ca5",
        "createdAt": "2023-04-08T02:33:41.785Z",
        "updatedAt": "2023-04-08T02:33:41.785Z",
        "__v": 0,
        "id": "6430d28595394133234b0ca5"
      },
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'Machine Learning Course Ebook',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/ebook',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show ebook 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/ebook/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "EBook found",
    "data": {
      "eBook": {
        "_id": "6430d28595394133234b0ca5",
        "path": "courses/6430ce43c3ca49b01012f8ca/eBook/e1116f01-6e04-4fb8-8f3a-c2e50ba19752.pdf",
        "type": "application/pdf",
        "name": "Machine Learning Course Ebook",
        "owner": "6430c7854e29a1ff8375d1e7",
        "createdAt": "2023-04-08T02:33:41.785Z",
        "updatedAt": "2023-04-08T02:33:41.785Z",
        "__v": 0,
        "id": "6430d28595394133234b0ca5"
      },
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/ebook/6430d28595394133234b0ca5',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update ebook 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/professor/courses/:id/ebook/:id`
- _Headers:_ `Authorization`
- _Body:_
  ```json
  {
    "name": "Machine Learning Course Ebook Updated"
  }
  ```
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "eBook updated",
    "data": {
      "eBook": {
        "_id": "6430d28595394133234b0ca5",
        "path": "courses/6430ce43c3ca49b01012f8ca/eBook/e1116f01-6e04-4fb8-8f3a-c2e50ba19752.pdf",
        "type": "application/pdf",
        "name": "Machine Learning Course Ebook Updated",
        "owner": "6430c7854e29a1ff8375d1e7",
        "createdAt": "2023-04-08T02:33:41.785Z",
        "updatedAt": "2023-04-08T02:43:30.478Z",
        "__v": 0,
        "id": "6430d28595394133234b0ca5"
      },
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'Machine Learning Course Ebook Updated',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/ebook/6430d28595394133234b0ca5',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete ebook 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/professor/courses/:id/ebook/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "eBook deleted",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/ebook/6430d28595394133234b0ca5',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### ASSISTANT ⭐

###### Create assistant 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/professor/universities/:id/collages/:id/courses/:id/assistants`
- _Headers:_ `Authorization`
- _Body:_

  ```json
  {
    "name": "Mohamed Yasser",
    "academicId": "9887593780045",
    "username": "mohamed-user-09",
    "password": "passCode090"
  }
  ```

- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Assistant created successfully",
    "data": {
      "assistant": {
        "id": "6430e04795394133234b0ccd"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "professor": {
        "id": "6430c7854e29a1ff8375d1e7",
        "name": "dr. mohamed yasser"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'Mohamed Yasser',
    academicId: '9887593780045',
    username: 'mohamed-user-09',
    password: 'passCode090',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/courses/6430ce43c3ca49b01012f8ca/assistants',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Attach assistant 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/professor/universities/:id/collages/:id/courses/:id/assistants/:id/attach`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assistant attached successfully",
    "data": {
      "assistant": {
        "id": "6430e04795394133234b0ccd",
        "courses": ["6430ce43c3ca49b01012f8ca", "6430e37e95394133234b0cdf"]
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "professor": {
        "id": "6430c7854e29a1ff8375d1e7",
        "name": "dr. mohamed yasser"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/courses/6430e37e95394133234b0cdf/assistants/6430e04795394133234b0ccd/attach',
    {
      method: 'POST',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update assistant 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/professor/universities/:id/collages/:id/courses/:id/assistants/:id`
- _Headers:_ `Authorization`
- _Body:_

  ```json
  {
    "name": "Mohamed Yasser",
    "academicId": "9887593780045"
  }
  ```

- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assistant updated successfully",
    "data": {
      "assistant": {
        "id": "6430e04795394133234b0ccd",
        "name": "mohamed yasser",
        "academicId": "9887593780045"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'Mohamed Yasser',
    academicId: '9887593780045',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/courses/6430ce43c3ca49b01012f8ca/assistants/6430e04795394133234b0ccd',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show assistant 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/universities/:id/collages/:id/courses/:id/assistants/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assistant fetched successfully",
    "data": {
      "assistant": {
        "id": "6430e04795394133234b0ccd",
        "name": "mohamed yasser",
        "academicId": "9887593780045",
        "username": "mohamed-user-09",
        "qrCode": "6430e04795394133234b0ccb",
        "courses": ["6430ce43c3ca49b01012f8ca", "6430e37e95394133234b0cdf"],
        "createdBy": "6430c7854e29a1ff8375d1e7",
        "contacts": "6430e04795394133234b0ccc"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "professor": {
        "id": "6430c7854e29a1ff8375d1e7",
        "name": "dr. mohamed yasser"
      },
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/courses/6430ce43c3ca49b01012f8ca/assistants/6430e04795394133234b0ccd',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete assistant 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/professor/universities/:id/collages/:id/courses/:id/assistants/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assistant deleted successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/courses/6430ce43c3ca49b01012f8ca/assistants/6430e04795394133234b0ccd',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index assistants by course 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/universities/:id/collages/:id/courses/:id/assistants`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assistants fetched successfully",
    "data": {
      "assistantsCount": 1,
      "assistants": [
        {
          "id": "6430ed28e0848ccfef40807a",
          "name": "mohamed yasser",
          "academicId": "9887593780045",
          "courses": ["6430ce43c3ca49b01012f8ca"],
          "createdBy": "6430c7854e29a1ff8375d1e7"
        }
      ],
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/courses/6430ce43c3ca49b01012f8ca/assistants',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index assistants by collage 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/universities/:id/collages/:id/assistants`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assistants fetched successfully",
    "data": {
      "assistants": [
        {
          "id": "6430ed28e0848ccfef40807a",
          "name": "mohamed yasser",
          "academicId": "9887593780045",
          "courses": ["6430ce43c3ca49b01012f8ca"]
        }
      ],
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/assistants',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### LECTURE ⭐

###### Create lecture 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/professor/courses/:id/lectures`
- _Headers:_ `Authorization`
- _Body:_

  ```json
  {
    "name": "Lecture 01",
    "number": 1
  }
  ```

- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Lecture created successfully",
    "data": {
      "lecture": {
        "id": "6431e66759a6e5eec1297319"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'Lecture 01',
    number: 1,
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/lectures',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index lectures 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/lectures`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Lectures fetched successfully",
    "data": {
      "lecturesCount": 1,
      "lectures": [
        {
          "id": "6431e66759a6e5eec1297319",
          "_id": "6431e66759a6e5eec1297319",
          "name": "lecture 01",
          "number": 1,
          "resources": [],
          "course": "6430ce43c3ca49b01012f8ca",
          "professor": "6430c7854e29a1ff8375d1e7",
          "createdAt": "2023-04-08T22:10:47.415Z",
          "updatedAt": "2023-04-08T22:10:47.415Z",
          "__v": 0
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/lectures',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show lecture 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/lectures/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Lecture found",
    "data": {
      "lecture": {
        "_id": "6431e66759a6e5eec1297319",
        "name": "lecture 01",
        "number": 1,
        "resources": [],
        "course": "6430ce43c3ca49b01012f8ca",
        "professor": "6430c7854e29a1ff8375d1e7",
        "createdAt": "2023-04-08T22:10:47.415Z",
        "updatedAt": "2023-04-08T22:10:47.415Z",
        "__v": 0,
        "id": "6431e66759a6e5eec1297319"
      },
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/lectures/6431e66759a6e5eec1297319',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update lecture 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/professor/courses/:id/lectures/:id`
- _Headers:_ `Authorization`
- _Body:_
  ```json
  {
    "name": "Lecture 03",
    "number": 3
  }
  ```
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Lecture updated successfully",
    "data": {
      "lecture": {
        "id": "6431e66759a6e5eec1297319",
        "name": "lecture 03",
        "number": 3
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'Lecture 03',
    number: 3,
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/lectures/6431e66759a6e5eec1297319',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete lecture 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/professor/courses/:id/lectures/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Lecture deleted successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/lectures/6431e66759a6e5eec1297319',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

- `POST - api/v1/professor/courses/:id/lectures/:id/resources` - Create [Details](#create-lecture-resource-)
- `GET - api/v1/professor/courses/:id/lectures/:id/resources` - Index [Details](#index-lecture-resources-)
- `GET - api/v1/professor/courses/:id/lectures/:id/resources/:id` - Show [Details](#show-lecture-resource-)
- `PATCH - api/v1/professor/courses/:id/lectures/:id/resources/:id` - Update [Details](#update-lecture-resource-)
- `DELETE - api/v1/professor/courses/:id/lectures/:id/resources/:id` - Delete [Details](#delete-lecture-resource-)

##### LECTURE RESOURCE ⭐

###### Create lecture resource 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/professor/courses/:id/lectures/:id/resources`
- _Headers:_ `Authorization`
- _Body:_

  ```json
  {
    "name": "lecture 01 - resource",
    "type": "png" // Allowed types // allowed types without mime type [jpeg, png, pdf, doc, xls, docx, xlsx, pptx, mp3, mp4]
  }
  ```

- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Lecture resource created",
    "data": {
      "storage": {
        "path": "courses/6430ce43c3ca49b01012f8ca/lecture/64322cf88becbaa1fe44e152/resources/69a736e6-a1d8-4595-8053-c5740b955ca9.png",
        "type": "image/png",
        "name": "lecture 01 - resource",
        "owner": "6430c7854e29a1ff8375d1e7",
        "_id": "64322db139cfdf68bb8fe285",
        "createdAt": "2023-04-09T03:14:57.404Z",
        "updatedAt": "2023-04-09T03:14:57.404Z",
        "__v": 0,
        "id": "64322db139cfdf68bb8fe285"
      },
      "lecture": {
        "_id": "64322cf88becbaa1fe44e152",
        "name": "lecture 01",
        "number": 1,
        "resources": ["64322db139cfdf68bb8fe285"],
        "course": "6430ce43c3ca49b01012f8ca",
        "professor": "6430c7854e29a1ff8375d1e7",
        "createdAt": "2023-04-09T03:11:52.100Z",
        "updatedAt": "2023-04-09T03:14:57.522Z",
        "__v": 1,
        "id": "64322cf88becbaa1fe44e152"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'lecture 01 - resource',
    type: 'png',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/lectures/64322cf88becbaa1fe44e152/resources',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index lecture resources 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/lectures/:id/resources`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Resources fetched successfully",
    "data": {
      "resources": [
        {
          "_id": "64322db139cfdf68bb8fe285",
          "type": "image/png",
          "name": "lecture 01 - resource",
          "id": "64322db139cfdf68bb8fe285"
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/lectures/64322cf88becbaa1fe44e152/resources',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show lecture resource 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/lectures/:id/resources/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Resource fetched successfully",
    "data": {
      "resource": {
        "_id": "64322db139cfdf68bb8fe285",
        "path": "courses/6430ce43c3ca49b01012f8ca/lecture/64322cf88becbaa1fe44e152/resources/69a736e6-a1d8-4595-8053-c5740b955ca9.png",
        "type": "image/png",
        "name": "new resource name",
        "owner": "6430c7854e29a1ff8375d1e7",
        "createdAt": "2023-04-09T03:14:57.404Z",
        "updatedAt": "2023-04-09T03:18:33.343Z",
        "__v": 0,
        "id": "64322db139cfdf68bb8fe285"
      },
      "lecture": {
        "id": "64322cf88becbaa1fe44e152",
        "name": "lecture 01"
      },
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/lectures/64322cf88becbaa1fe44e152/resources/64322db139cfdf68bb8fe285',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update lecture resource 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/professor/courses/:id/lectures/:id/resources/:id`
- _Headers:_ `Authorization`
- _Body:_ `name`

  ```json
  {
    "name": "new resource name"
  }
  ```

- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Resource updated successfully",
    "data": {
      "resource": {
        "_id": "64322db139cfdf68bb8fe285",
        "path": "courses/6430ce43c3ca49b01012f8ca/lecture/64322cf88becbaa1fe44e152/resources/69a736e6-a1d8-4595-8053-c5740b955ca9.png",
        "type": "image/png",
        "name": "new resource name",
        "owner": "6430c7854e29a1ff8375d1e7",
        "createdAt": "2023-04-09T03:14:57.404Z",
        "updatedAt": "2023-04-09T03:18:33.343Z",
        "__v": 0,
        "id": "64322db139cfdf68bb8fe285"
      },
      "lecture": {
        "id": "64322cf88becbaa1fe44e152",
        "name": "lecture 01"
      },
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'new resource name',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/lectures/64322cf88becbaa1fe44e152/resources/64322db139cfdf68bb8fe285',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete lecture resource 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/professor/courses/:id/lectures/:id/resources/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Resource removed successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/lectures/64322cf88becbaa1fe44e152/resources/64322db139cfdf68bb8fe285',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### QUICK Index ⭐

###### Index levels professor 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/universities/:id/collages/:id/levels`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Levels fetched successfully",
    "data": {
      "levels": [
        {
          "id": "642ee7f789a92ceeba6b7a4f",
          "name": "level 01"
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index programs professor 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/universities/:id/collages/:id/levels/:id/programs`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Programs fetched successfully",
    "data": {
      "programs": [
        {
          "id": "643052a83eea93f118839c46",
          "name": "public"
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index departments professor 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/universities/:id/collages/:id/levels/:id/programs/:id/departments`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Departments fetched successfully",
    "data": {
      "departments": [
        {
          "id": "6430596c112031c1dbfc3fd8",
          "name": "computer science"
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052a83eea93f118839c46/departments',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### ATTENDANCE ⭐

###### Create attendance 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/professor/courses/:id/lectures/:id/attendance`
- _Headers:_ `Authorization`
- _Body:_

  ```json
  {
    "distanceInMeters": 100,
    "durationInMinutes": 2,
    "lat": "30.9977",
    "lng": "29.7432"
  }
  ```

- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Attendance created successfully.",
    "data": {
      "attendance": {
        "students": [],
        "lecture": "64322cf88becbaa1fe44e152",
        "distanceInMeters": 100,
        "creatorCoordinates": {
          "lat": "30.9977",
          "lng": "29.7432"
        },
        "durationInMinutes": 2,
        "expiredAt": "2023-04-09T15:16:39.557Z",
        "randomAccessKey": "W0oGmjIXsW",
        "_id": "6432d65f19c58a344497f49c",
        "createdAt": "2023-04-09T15:14:39.571Z",
        "updatedAt": "2023-04-09T15:14:39.571Z",
        "__v": 0,
        "id": "6432d65f19c58a344497f49c"
      },
      "lecture": {
        "id": "64322cf88becbaa1fe44e152",
        "name": "lecture 01"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    distanceInMeters: 100,
    durationInMinutes: 2,
    lat: '30.9977',
    lng: '29.7432',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/lectures/64322cf88becbaa1fe44e152/attendance',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show attendance 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/lectures/:id/attendance/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Attendance fetched successfully",
    "data": {
      "attendance": {
        "creatorCoordinates": {
          "lat": "30.9977",
          "lng": "29.7432"
        },
        "_id": "6432d88c19c58a344497f4ba",
        "students": [],
        "lecture": "6432d85e19c58a344497f4b4",
        "distanceInMeters": 100,
        "durationInMinutes": 2,
        "expiredAt": "2023-04-09T15:25:56.657Z",
        "randomAccessKey": "yUvrasLv20",
        "createdAt": "2023-04-09T15:23:56.658Z",
        "updatedAt": "2023-04-09T15:23:56.658Z",
        "__v": 0,
        "id": "6432d88c19c58a344497f4ba"
      },
      "isExpired": true
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/lectures/6432d85e19c58a344497f4b4/attendance/6432d88c19c58a344497f4ba',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index attendance students 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/lectures/:id/attendance/:id/students`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Students fetched successfully",
    "data": {
      "students": [],
      "isExpired": true
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/lectures/6432d85e19c58a344497f4b4/attendance/6432d88c19c58a344497f4ba/students',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete attendance student 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/professor/courses/:id/lectures/:id/attendance/:id/students/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Student removed successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/lectures/6432d85e19c58a344497f4b4/attendance/6432d88c19c58a344497f4ba/students/6432d85e19c58a344497f4b4',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### COURSE ASSIGNMENT ⭐

###### Create course assignment 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/professor/courses/:id/assignments`
- _Headers:_ `Authorization`
- _Body:_

  ```json
  {
    "title": "Python CGI",
    "contentText": "In this assignment you should create a full python server side application and apply all CGI concepts we have learned in the lecture and section",
    "dueToDays": 7
  }
  ```

- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Assignment created",
    "data": {
      "assignment": {
        "id": "6432dd2ddde93cf76c5dadc8"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    title: 'Python CGI',
    contentText:
      'In this assignment you should create a full python server side application and apply all CGI concepts we have learned in the lecture and section',
    dueToDays: 7,
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/assignments',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index course assignments 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/assignments`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assignments fetched successfully",
    "data": {
      "assignmentsCount": 1,
      "assignments": [
        {
          "id": "6432dd2ddde93cf76c5dadc8",
          "_id": "6432dd2ddde93cf76c5dadc8",
          "title": "python cgi",
          "contentText": "In this assignment you should create a full python server side application and apply all CGI concepts we have learned in the lecture and section",
          "contentImage": "6432dd2ddde93cf76c5dadc7",
          "dueDate": "2023-04-16T15:43:41.808Z",
          "professor": "6430c7854e29a1ff8375d1e7",
          "course": "6430ce43c3ca49b01012f8ca",
          "submissions": [],
          "createdAt": "2023-04-09T15:43:42.052Z",
          "updatedAt": "2023-04-09T15:43:42.052Z",
          "__v": 0
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/assignments',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show course assignment 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/assignments/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assignments fetched successfully",
    "data": {
      "assignmentsCount": 1,
      "assignments": [
        {
          "id": "6432dd2ddde93cf76c5dadc8",
          "_id": "6432dd2ddde93cf76c5dadc8",
          "title": "python cgi",
          "contentText": "In this assignment you should create a full python server side application and apply all CGI concepts we have learned in the lecture and section",
          "contentImage": "6432dd2ddde93cf76c5dadc7",
          "dueDate": "2023-04-16T15:43:41.808Z",
          "professor": "6430c7854e29a1ff8375d1e7",
          "course": "6430ce43c3ca49b01012f8ca",
          "submissions": [],
          "createdAt": "2023-04-09T15:43:42.052Z",
          "updatedAt": "2023-04-09T15:43:42.052Z",
          "__v": 0
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/assignments/6432dd2ddde93cf76c5dadc8',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update course assignment 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/professor/courses/:id/assignments/:id`
- _Headers:_ `Authorization`
- _Body:_
  ```json
  {
    "title": "New title",
    "contentText": "New content text",
    "dueToDays": 10
  }
  ```
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "The assignment updated successfully",
    "data": {
      "assignment": {
        "_id": "6432dd2ddde93cf76c5dadc8",
        "title": "new title",
        "contentText": "New content text",
        "contentImage": "6432dd2ddde93cf76c5dadc7",
        "dueDate": "2023-04-19T15:52:40.136Z",
        "professor": "6430c7854e29a1ff8375d1e7",
        "course": "6430ce43c3ca49b01012f8ca",
        "submissions": [],
        "createdAt": "2023-04-09T15:43:42.052Z",
        "updatedAt": "2023-04-09T15:52:40.249Z",
        "__v": 0,
        "id": "6432dd2ddde93cf76c5dadc8"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    title: 'New title',
    contentText: 'New content text',
    dueToDays: 10,
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/assignments/6432dd2ddde93cf76c5dadc8',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete course assignment 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/professor/courses/:id/assignments/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assignment removed successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/assignments/6432dd2ddde93cf76c5dadc8',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

- `GET - api/v1/professor/courses/:id/assignments/:id/submissions` - Index [Details](#index-course-assignment-submissions-)
- `GET - api/v1/professor/courses/:id/assignments/:id/submissions/:id` - Show [Details](#show-course-assignment-submission-)

##### COURSE ASSIGNMENT SUBMISSIONS ⭐

###### Index course assignment submissions 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/assignments/:id/submissions`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Submissions fetched successfully",
    "data": {
      "submissionsCount": 0,
      "submissions": []
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/assignments/6432e0d4dde93cf76c5dade9/submissions',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show course assignment submission 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/assignments/:id/submissions/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Submission fetched successfully",
    "data": {
      "submission": {
        "grade": 0,
        "feedback": "",
        "assignment": "6432e0d4dde93cf76c5dade9",
        "student": "6430ce43c3ca49b01012f8ca",
        "createdAt": "2023-04-09T15:43:42.052Z",
        "updatedAt": "2023-04-09T15:52:40.249Z",
        "__v": 0,
        "id": "6432e0d4dde93cf76c5dade9"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/assignments/6432e0d4dde93cf76c5dade9/submissions/6432e0d4dde93cf76c5dade9',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### EXAM ⭐

###### Create exam 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/professor/courses/:id/exams`
- _Headers:_ `Authorization`
- _Body:_

  ```json
  {
    "name": "Exam 01",
    "startAtDay": "6",
    "startAtMonth": "4",
    "startAtYear": "2023",
    "startAtHour": "12",
    "startAtMinute": "30",
    "durationInMinutes": "20"
  }
  ```

- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Exam created successfully.",
    "data": {
      "exam": {
        "name": "exam 01",
        "startAt": "2023-04-10T10:30:00.000Z",
        "durationInMinutes": 20,
        "endAt": "2023-04-10T10:50:00.000Z",
        "course": "6430e37e95394133234b0cdf",
        "questions": [],
        "totalScore": 0,
        "submissions": [],
        "enrollments": [],
        "professor": "6430c7854e29a1ff8375d1e7",
        "_id": "6432e33bdde93cf76c5dae02",
        "createdAt": "2023-04-09T16:09:31.782Z",
        "updatedAt": "2023-04-09T16:09:31.782Z",
        "__v": 0
      },
      "course": {
        "id": "6430e37e95394133234b0cdf",
        "name": "image processing"
      },
      "professor": {
        "id": "6430c7854e29a1ff8375d1e7",
        "name": "dr. mohamed yasser"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'Exam 01',
    startAtDay: '10',
    startAtMonth: '4',
    startAtYear: '2023',
    startAtHour: '12',
    startAtMinute: '30',
    durationInMinutes: '20',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430e37e95394133234b0cdf/exams',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index exams 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/exams`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Exams fetched successfully",
    "data": {
      "examsCount": 1,
      "exams": [
        {
          "id": "6432e33bdde93cf76c5dae02",
          "_id": "6432e33bdde93cf76c5dae02",
          "name": "exam 01",
          "startAt": "2023-04-10T10:30:00.000Z",
          "durationInMinutes": 20,
          "endAt": "2023-04-10T10:50:00.000Z",
          "course": "6430e37e95394133234b0cdf",
          "questions": [],
          "totalScore": 0,
          "submissions": [],
          "enrollments": [],
          "professor": "6430c7854e29a1ff8375d1e7",
          "createdAt": "2023-04-09T16:09:31.782Z",
          "updatedAt": "2023-04-09T16:09:31.782Z",
          "__v": 0
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430e37e95394133234b0cdf/exams',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show exam 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/exams/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Exam fetched successfully",
    "data": {
      "exam": {
        "id": "6432e33bdde93cf76c5dae02",
        "_id": "6432e33bdde93cf76c5dae02",
        "name": "exam 01",
        "startAt": "2023-04-10T10:30:00.000Z",
        "durationInMinutes": 20,
        "endAt": "2023-04-10T10:50:00.000Z",
        "course": "6430e37e95394133234b0cdf",
        "questions": [],
        "totalScore": 0,
        "submissions": [],
        "enrollments": [],
        "professor": "6430c7854e29a1ff8375d1e7",
        "createdAt": "2023-04-09T16:09:31.782Z",
        "updatedAt": "2023-04-09T16:09:31.782Z",
        "__v": 0
      },
      "course": {
        "id": "6430e37e95394133234b0cdf",
        "name": "image processing"
      },
      "professor": {
        "id": "6430c7854e29a1ff8375d1e7",
        "name": "dr. mohamed yasser"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430e37e95394133234b0cdf/exams/6432e33bdde93cf76c5dae02',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update exam 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/professor/courses/:id/exams/:id`
- _Headers:_ `Authorization`
- _Body:_

  ```json
  {
    "name": "exam 99",
    "startAtDay": "6",
    "startAtMonth": "10",
    "startAtYear": "2023",
    "startAtHour": "15",
    "startAtMinute": "10",
    "durationInMinutes": "20"
  }
  ```

- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Exam updated successfully.",
    "data": {
      "exam": {
        "id": "6432e33bdde93cf76c5dae02",
        "name": "exam 99",
        "startAt": "2023-10-06T13:10:00.000Z",
        "endAt": "2023-10-06T13:30:00.000Z",
        "durationInMinutes": 20
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'exam 99',
    startAtDay: '6',
    startAtMonth: '10',
    startAtYear: '2023',
    startAtHour: '15',
    startAtMinute: '10',
    durationInMinutes: '20',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430e37e95394133234b0cdf/exams/6432e33bdde93cf76c5dae02',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete exam 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/professor/courses/:id/exams/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Exam deleted successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430e37e95394133234b0cdf/exams/6432e33bdde93cf76c5dae02',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Start now exam 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/professor/courses/:id/exams/:id/start-now`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Exam will start now.",
    "data": {
      "exam": {
        "id": "6432e59cdde93cf76c5dae17",
        "name": "exam 01"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430e37e95394133234b0cdf/exams/6432e59cdde93cf76c5dae17/start-now',
    {
      method: 'PATCH',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### EXAM SUBMISSIONS ⭐

###### Index exam submissions 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/exams/:id/submissions`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Exam submissions fetched successfully",
    "data": {
      "examSubmissionsCount": 0,
      "examSubmissions": [],
      "exam": {
        "id": "6432e59cdde93cf76c5dae17",
        "name": "exam 01"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430e37e95394133234b0cdf/exams/6432e59cdde93cf76c5dae17/submissions',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

- `GET - api/v1/professor/courses/:id/exams/:id/enrollments` - Index [Details](#index-exam-enrollments-)

##### EXAM ENROLLMENTS ⭐

###### Index exam enrollments 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/exams/:id/enrollments`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Exam enrollments fetched successfully",
    "data": {
      "examEnrollmentsCount": 0,
      "examEnrollments": [],
      "exam": {
        "id": "6432e59cdde93cf76c5dae17",
        "name": "exam 01"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430e37e95394133234b0cdf/exams/6432e59cdde93cf76c5dae17/enrollments',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### EXAM QUESTIONS ( Text and/or Image or both ) ⭐

###### Create exam question 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/professor/courses/:id/exams/:id/questions`
- _Headers:_ `Authorization`
- _Body:_

  ```json
  {
    "contentText": "Question 2",
    "contentImage": "true",
    "score": "7",
    "answersArray": ["answer 1", "answer 2", "answer 3"],
    "correctAnswerIndex": "1" // 0 based index [0, 1, 2, 3, ...]
  }
  ```

- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Question created successfully",
    "data": {
      "question": {
        "contentText": "Question 2",
        "contentImage": "64330490101ff077ea74633f",
        "answers": [
          "64330490101ff077ea746341",
          "64330490101ff077ea746343",
          "64330490101ff077ea746345"
        ],
        "score": 7,
        "course": "6430e37e95394133234b0cdf",
        "professor": "6430c7854e29a1ff8375d1e7",
        "exam": "6433047d101ff077ea746339",
        "_id": "64330490101ff077ea746340",
        "correctAnswer": "64330490101ff077ea746343",
        "createdAt": "2023-04-09T18:31:44.840Z",
        "updatedAt": "2023-04-09T18:31:44.840Z",
        "__v": 0,
        "id": "64330490101ff077ea746340"
      },
      "exam": {
        "id": "6433047d101ff077ea746339",
        "name": "exam 01"
      },
      "course": {
        "id": "6430e37e95394133234b0cdf",
        "name": "image processing"
      },
      "professor": {
        "id": "6430c7854e29a1ff8375d1e7",
        "name": "dr. mohamed yasser"
      }
    }
  }
  ```

- _Example - JS_:

```js
let headersList = {
  Accept: '*/*',
  Authorization:
    'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  'Content-Type': 'application/json',
};

let bodyContent = JSON.stringify({
  contentText: 'Question 2',
  contentImage: 'true',
  score: '7',
  answersArray: ['answer 1', 'answer 2', 'answer 3'],
  correctAnswerIndex: '1',
});

let response = await fetch(
  'http://localhost:3000/api/v1/professor/courses/6430e37e95394133234b0cdf/exams/6433047d101ff077ea746339/questions',
  {
    method: 'POST',
    body: bodyContent,
    headers: headersList,
  }
);

let data = await response.text();
console.log(data);
```

###### Index exam questions 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/exams/:id/questions`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Questions fetched successfully",
    "data": {
      "questionsCount": 1,
      "questions": [
        {
          "id": "64330490101ff077ea746340",
          "contentText": "Question 2",
          "score": 7
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430e37e95394133234b0cdf/exams/6433047d101ff077ea746339/questions',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show exam question 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/exams/:id/questions/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Question fetched successfully",
    "data": {
      "question": {
        "id": "64330490101ff077ea746340",
        "contentText": "Question 2",
        "contentImage": "64330490101ff077ea74633f",
        "score": 7,
        "answers": [
          {
            "id": "64330490101ff077ea746341",
            "contentText": "answer 1"
          },
          {
            "id": "64330490101ff077ea746343",
            "contentText": "answer 2"
          },
          {
            "id": "64330490101ff077ea746345",
            "contentText": "answer 3"
          }
        ],
        "correctAnswerId": "64330490101ff077ea746343"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430e37e95394133234b0cdf/exams/6433047d101ff077ea746339/questions/64330490101ff077ea746340',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update exam question 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/professor/courses/:id/exams/:id/questions/:id`
- _Headers:_ `Authorization`
- _Body:_
  ```json
  {
    "contentText": "this is a question!!",
    "score": "5",
    "correctAnswerId": "64330490101ff077ea746341"
  }
  ```
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "question updated successfully",
    "data": {
      "question": {
        "id": "64330490101ff077ea746340",
        "contentText": "this is a question!!",
        "score": 5,
        "correctAnswer": "64330490101ff077ea746341"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    contentText: 'this is a question!!',
    score: '5',
    correctAnswerId: '64330490101ff077ea746341',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430e37e95394133234b0cdf/exams/6433047d101ff077ea746339/questions/64330490101ff077ea746340',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete exam question 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/professor/courses/:id/exams/:id/questions/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Question deleted successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430e37e95394133234b0cdf/exams/6433047d101ff077ea746339/questions/64330490101ff077ea746340',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

- `PATCH - api/v1/professor/courses/:id/exams/:id/questions/:id/answers/:id` - Update [Details](#update-exam-question-answer-)

##### EXAM QUESTION ANSWERS ⭐

###### Update exam question answer 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/professor/courses/:id/exams/:id/questions/:id/answers/:id`
- _Headers:_ `Authorization`
- _Body:_
  ```json
  {
    "contentText": "new answer"
  }
  ```
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Answer updated successfully",
    "data": {
      "answer": {
        "id": "6433086febda70cf0481c977",
        "contentText": "new answer"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    contentText: 'new answer',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430e37e95394133234b0cdf/exams/6433047d101ff077ea746339/questions/6433086febda70cf0481c976/answers/6433086febda70cf0481c977',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

#### ASSISTANT 👨‍🏫

##### ACCESS PERMISSOIN ⭐

###### Show assistant 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/assistant/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "assistant fetched successfully",
    "data": {
      "assistant": {
        "id": "6430ed28e0848ccfef40807a",
        "createdAt": "2023-04-08T04:27:20.066Z",
        "name": "mohamed yasser",
        "username": "mohamed-user-09",
        "academicId": "9887593780045",
        "qrCode": "6430ed28e0848ccfef408078",
        "courses": ["6430ce43c3ca49b01012f8ca"],
        "contacts": "6430ed28e0848ccfef408079"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/6430ed28e0848ccfef40807a',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update assistant 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/assistant/:id`
- _Headers:_ `Authorization`
- _Body:_
  ```json
  {
    "name": "my new name",
    "academicId": "878978798978"
  }
  ```
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "assistant updated successfully",
    "data": {
      "assistant": {
        "id": "6430ed28e0848ccfef40807a",
        "name": "my new name",
        "academicId": "878978798978"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'my new name',
    academicId: '878978798978',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/6430ed28e0848ccfef40807a',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

- `GET - api/v1/assistant/courses` - Index [Details](#index-courses-assistant-)
- `GET - api/v1/assistant/courses/:id` - Show [Details](#show-course-assistant-)

##### COURSE ⭐

###### Index courses assistant 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/assistant/courses`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Courses fetched successfully",
    "data": {
      "coursesCount": 1,
      "courses": [
        {
          "id": "6430ce43c3ca49b01012f8ca",
          "name": "machine learning",
          "code": "cs45",
          "createdAt": "2023-04-08T02:15:31.406Z",
          "updatedAt": "2023-04-09T15:59:16.604Z"
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch('http://localhost:3000/api/v1/assistant/courses', {
    method: 'GET',
    headers: headersList,
  });

  let data = await response.text();
  console.log(data);
  ```

###### Show course assistant 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/assistant/courses/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Course fetched successfully",
    "data": {
      "course": {
        "_id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning",
        "code": "cs45",
        "semester": "first",
        "professor": {
          "_id": "6430c7854e29a1ff8375d1e7",
          "name": "dr. mohamed yasser"
        },
        "assistants": ["6430ed28e0848ccfef40807a"],
        "students": [],
        "lectures": [
          "64322cf88becbaa1fe44e152",
          "6432d82919c58a344497f4a7",
          "6432d85e19c58a344497f4b4",
          "6432e0cadde93cf76c5dade3"
        ],
        "sections": [],
        "assignments": ["6432e0d4dde93cf76c5dade9"],
        "exams": [],
        "department": {
          "_id": "6430596c112031c1dbfc3fd8",
          "name": "computer science"
        },
        "program": {
          "_id": "643052a83eea93f118839c46",
          "name": "public"
        },
        "level": {
          "_id": "642ee7f789a92ceeba6b7a4f",
          "name": "level 01"
        },
        "collage": {
          "_id": "642e3cb699182e5e2d14ec59",
          "name": "fuculty of engineering"
        },
        "university": {
          "_id": "642deaa976e91123782b7f16",
          "name": "alu"
        },
        "createdAt": "2023-04-08T02:15:31.406Z",
        "updatedAt": "2023-04-09T15:59:16.604Z",
        "__v": 12
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### SECTION ⭐

###### Create section assistant 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections`
- _Headers:_ `Authorization`
- _Body:_

  ```json
  {
    "name": "Section 02",
    "number": 2
  }
  ```

- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Section created successfully",
    "data": {
      "section": {
        "id": "64333b450ea788a84c9579e6"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'Section 02',
    number: 2,
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index sections assistant 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Sections fetched successfully",
    "data": {
      "sectionsCount": 2,
      "sections": [
        {
          "_id": "64333b450ea788a84c9579e6",
          "name": "section 02",
          "number": 2,
          "resources": [],
          "assistant": "6430ed28e0848ccfef40807a",
          "course": "6430ce43c3ca49b01012f8ca",
          "assignments": [],
          "createdAt": "2023-04-09T22:25:09.218Z",
          "updatedAt": "2023-04-09T22:25:09.218Z",
          "__v": 0
        },
        {
          "_id": "64333b152d1b672a2ee9a1a0",
          "name": "section 01",
          "number": 1,
          "resources": [],
          "assistant": "6430ed28e0848ccfef40807a",
          "course": "6430ce43c3ca49b01012f8ca",
          "assignments": [],
          "createdAt": "2023-04-09T22:24:21.364Z",
          "updatedAt": "2023-04-09T22:24:21.364Z",
          "__v": 0
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show section assistant 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Section fetched successfully",
    "data": {
      "section": {
        "_id": "64333b450ea788a84c9579e6",
        "name": "section 02",
        "number": 2,
        "resources": [],
        "assistant": "6430ed28e0848ccfef40807a",
        "course": "6430ce43c3ca49b01012f8ca",
        "assignments": [],
        "createdAt": "2023-04-09T22:25:09.218Z",
        "updatedAt": "2023-04-09T22:25:09.218Z",
        "__v": 0
      },
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update section assistant 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id`
- _Headers:_ `Authorization`
- _Body:_
  ```json
  {
    "name": "New section name",
    "number": 6
  }
  ```
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Section fetched successfully",
    "data": {
      "section": {
        "_id": "64333b450ea788a84c9579e6",
        "name": "section 02",
        "number": 2,
        "resources": [],
        "assistant": "6430ed28e0848ccfef40807a",
        "course": "6430ce43c3ca49b01012f8ca",
        "assignments": [],
        "createdAt": "2023-04-09T22:25:09.218Z",
        "updatedAt": "2023-04-09T22:25:09.218Z",
        "__v": 0
      },
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'New section name',
    number: 6,
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete section assistant 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Section fetched successfully",
    "data": {
      "section": {
        "_id": "64333b450ea788a84c9579e6",
        "name": "section 02",
        "number": 2,
        "resources": [],
        "assistant": "6430ed28e0848ccfef40807a",
        "course": "6430ce43c3ca49b01012f8ca",
        "assignments": [],
        "createdAt": "2023-04-09T22:25:09.218Z",
        "updatedAt": "2023-04-09T22:25:09.218Z",
        "__v": 0
      },
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

- `POST - api/v1/assistant/courses/:id/sections/:id/attendance` - Create [Details](#create-attendance-assistant-)
- `GET - api/v1/assistant/courses/:id/sections/:id/attendance/:id` - Show [Details](#show-attendance-assistant-)
- `GET - api/v1/assistant/courses/:id/sections/:id/attendance/:id/students` - Index Students [Details](#index-attendance-assistant-students-)
- `DELETE - api/v1/assistant/courses/:id/sections/:id/attendance/:id/students/:id` - Delete Student [Details](#delete-attendance-assistant-student-)

##### ATTENDANCE ( QR CODE & LOCATION ) ⭐

###### Create attendance assistant 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/attendance`
- _Headers:_ `Authorization`
- _Body:_
  ```json
  {
    "distanceInMeters": 100,
    "durationInMinutes": 60,
    "lat": "31.205753",
    "lng": "29.924526"
  }
  ```
- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Attendance created successfully.",
    "data": {
      "attendance": {
        "students": [],
        "section": "64333b450ea788a84c9579e6",
        "distanceInMeters": 100,
        "creatorCoordinates": {
          "lat": "31.205753",
          "lng": "29.924526"
        },
        "durationInMinutes": 60,
        "expiredAt": "2023-04-10T04:41:28.704Z",
        "randomAccessKey": "CHDC5wyn0c",
        "_id": "64338568efee0439e703eecf",
        "createdAt": "2023-04-10T03:41:28.711Z",
        "updatedAt": "2023-04-10T03:41:28.711Z",
        "__v": 0,
        "id": "64338568efee0439e703eecf"
      },
      "section": {
        "id": "64333b450ea788a84c9579e6",
        "name": "section 02"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    distanceInMeters: 100,
    durationInMinutes: 60,
    lat: '31.205753',
    lng: '29.924526',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/attendance',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show attendance assistant 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/attendance/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Attendance created successfully.",
    "data": {
      "attendance": {
        "students": [],
        "section": "64333b450ea788a84c9579e6",
        "distanceInMeters": 100,
        "creatorCoordinates": {
          "lat": "31.205753",
          "lng": "29.924526"
        },
        "durationInMinutes": 60,
        "expiredAt": "2023-04-10T04:41:28.704Z",
        "randomAccessKey": "CHDC5wyn0c",
        "_id": "64338568efee0439e703eecf",
        "createdAt": "2023-04-10T03:41:28.711Z",
        "updatedAt": "2023-04-10T03:41:28.711Z",
        "__v": 0,
        "id": "64338568efee0439e703eecf"
      },
      "section": {
        "id": "64333b450ea788a84c9579e6",
        "name": "section 02"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/attendance/64338568efee0439e703eecf',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index attendance assistant students 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/attendance/:id/students`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Students fetched successfully",
    "data": {
      "students": []
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/attendance/64338568efee0439e703eecf/students',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete attendance assistant student 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/attendance/:id/students/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Student deleted successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/attendance/64338568efee0439e703eecf/students/6430ce43c3ca49b01012f8ca',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

- `POST - api/v1/assistant/courses/:id/sections/:id/assignments` - Create [Details](#create-section-assignment-assistant-)
- `GET - api/v1/assistant/courses/:id/sections/:id/assignments` - Index [Details](#index-section-assignments-assistant-)
- `GET - api/v1/assistant/courses/:id/sections/:id/assignments/:id` - Show [Details](#show-section-assignment-assistant-)
- `PATCH - api/v1/assistant/courses/:id/sections/:id/assignments/:id` - Update [Details](#update-section-assignment-assistant-)
- `DELETE - api/v1/assistant/courses/:id/sections/:id/assignments/:id` - Delete [Details](#delete-section-assignment-assistant-)

##### ASSIGNMENT ⭐

###### Create section assignment assistant 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/assignments`
- _Headers:_ `Authorization`
- _Body:_ `title, description, dueDate, file`

  ```json
  {
    "title": "this is new assignment for the section",
    "contentText": "in this assignment you should create static website using htm, css, js",
    "dueToDays": 5
  }
  ```

- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Assignment created",
    "data": {
      "assignment": {
        "title": "this is new assignment for the section",
        "contentText": "in this assignment you should create static website using htm, css, js",
        "contentImage": "64338862b26563cf63a1934c",
        "dueDate": "2023-04-15T03:54:10.618Z",
        "assistant": "6430ed28e0848ccfef40807a",
        "course": "6430ce43c3ca49b01012f8ca",
        "section": "64333b450ea788a84c9579e6",
        "submissions": [],
        "_id": "64338862b26563cf63a1934d",
        "createdAt": "2023-04-10T03:54:10.749Z",
        "updatedAt": "2023-04-10T03:54:10.749Z",
        "__v": 0
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    title: 'this is new assignment for the section',
    contentText:
      'in this assignment you should create static website using htm, css, js',
    dueToDays: 5,
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/assignments',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index section assignments assistant 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/assignments`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assignments fetched successfully",
    "data": {
      "assignmentsCount": 1,
      "assignments": [
        {
          "id": "64338862b26563cf63a1934d",
          "_id": "64338862b26563cf63a1934d",
          "title": "this is new assignment for the section",
          "contentText": "in this assignment you should create static website using htm, css, js",
          "contentImage": "64338862b26563cf63a1934c",
          "dueDate": "2023-04-15T03:54:10.618Z",
          "assistant": "6430ed28e0848ccfef40807a",
          "course": "6430ce43c3ca49b01012f8ca",
          "section": "64333b450ea788a84c9579e6",
          "submissions": [],
          "createdAt": "2023-04-10T03:54:10.749Z",
          "updatedAt": "2023-04-10T03:54:10.749Z",
          "__v": 0
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/assignments',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show section assignment assistant 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/assignments/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assignment fetched successfully",
    "data": {
      "assignment": {
        "_id": "64338862b26563cf63a1934d",
        "title": "this is new assignment for the section",
        "contentText": "in this assignment you should create static website using htm, css, js",
        "contentImage": "64338862b26563cf63a1934c",
        "dueDate": "2023-04-15T03:54:10.618Z",
        "assistant": "6430ed28e0848ccfef40807a",
        "course": "6430ce43c3ca49b01012f8ca",
        "section": "64333b450ea788a84c9579e6",
        "submissions": [],
        "createdAt": "2023-04-10T03:54:10.749Z",
        "updatedAt": "2023-04-10T03:54:10.749Z",
        "__v": 0,
        "id": "64338862b26563cf63a1934d"
      },
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning"
      },
      "section": {
        "id": "64333b450ea788a84c9579e6",
        "name": "section 02"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/assignments/64338862b26563cf63a1934d',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update section assignment assistant 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/assignments/:id`
- _Headers:_ `Authorization`
- _Body:_

  ```json
  {
    "title": "section assignment new title",
    "contentText": "this is updated content text",
    "dueToDays": 9
  }
  ```

- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "The assignment updated successfully",
    "data": {
      "assignment": {
        "_id": "64338862b26563cf63a1934d",
        "title": "section assignment new title",
        "contentText": "this is updated content text",
        "contentImage": "64338862b26563cf63a1934c",
        "dueDate": "2023-04-19T03:56:33.568Z",
        "assistant": "6430ed28e0848ccfef40807a",
        "course": "6430ce43c3ca49b01012f8ca",
        "section": "64333b450ea788a84c9579e6",
        "submissions": [],
        "createdAt": "2023-04-10T03:54:10.749Z",
        "updatedAt": "2023-04-10T03:56:33.688Z",
        "__v": 0,
        "id": "64338862b26563cf63a1934d"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    title: 'section assignment new title',
    contentText: 'this is updated content text',
    dueToDays: 9,
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/assignments/64338862b26563cf63a1934d',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete section assignment assistant 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/assignments/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assignment removed successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/assignments/64338862b26563cf63a1934d',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### SECTION RESOURCES ⭐

###### Create section resource assistant 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/resources`
- _Headers:_ `Authorization`
- _Body:_

  ```json
  {
    "name": "section resource for the whiteboard",
    "type": "png" // Allowed types // allowed types without mime type [jpeg, png, pdf, doc, xls, docx, xlsx, pptx, mp3, mp4]
  }
  ```

- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Section resource created",
    "data": {
      "storage": {
        "path": "courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/resources/4625dabc-5a1c-4696-a7a4-1dcc1bd4499d.png",
        "type": "image/png",
        "name": "section resource for the whiteboard",
        "owner": "6430ed28e0848ccfef40807a",
        "_id": "64338b889d30e909adbe568a",
        "createdAt": "2023-04-10T04:07:36.651Z",
        "updatedAt": "2023-04-10T04:07:36.651Z",
        "__v": 0,
        "id": "64338b889d30e909adbe568a"
      },
      "section": {
        "_id": "64333b450ea788a84c9579e6",
        "name": "section 02",
        "number": 2,
        "resources": ["64338b889d30e909adbe568a"],
        "assistant": "6430ed28e0848ccfef40807a",
        "course": "6430ce43c3ca49b01012f8ca",
        "assignments": [],
        "createdAt": "2023-04-09T22:25:09.218Z",
        "updatedAt": "2023-04-10T04:07:36.769Z",
        "__v": 3,
        "attendance": "64338568efee0439e703eecf",
        "id": "64333b450ea788a84c9579e6"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'section resource for the whiteboard',
    type: 'png',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/resources',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index section resources assistant 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/resources`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Resources fetched successfully",
    "data": {
      "resources": [
        {
          "_id": "64338b889d30e909adbe568a",
          "type": "image/png",
          "name": "section resource for the whiteboard",
          "id": "64338b889d30e909adbe568a"
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/64199f7356f349d3513ab2b9/sections/641b0a475fc1040d89eb8a04/resources',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show section resource assistant 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/resources/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Resource fetched successfully",
    "data": {
      "resource": {
        "_id": "64338b889d30e909adbe568a",
        "path": "courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/resources/4625dabc-5a1c-4696-a7a4-1dcc1bd4499d.png",
        "type": "image/png",
        "name": "section resource for the whiteboard",
        "owner": "6430ed28e0848ccfef40807a",
        "createdAt": "2023-04-10T04:07:36.651Z",
        "updatedAt": "2023-04-10T04:07:36.651Z",
        "__v": 0,
        "id": "64338b889d30e909adbe568a"
      },
      "section": {
        "id": "64333b450ea788a84c9579e6",
        "name": "section 02"
      },
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/resources/64338b889d30e909adbe568a',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update section resource assistant 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/resources/:id`
- _Headers:_ `Authorization`
- _Body:_
  ```json
  {
    "name": "new resource name"
  }
  ```
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Resource updated successfully",
    "data": {
      "resource": {
        "_id": "64338b889d30e909adbe568a",
        "path": "courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/resources/4625dabc-5a1c-4696-a7a4-1dcc1bd4499d.png",
        "type": "image/png",
        "name": "new resource name",
        "owner": "6430ed28e0848ccfef40807a",
        "createdAt": "2023-04-10T04:07:36.651Z",
        "updatedAt": "2023-04-10T04:15:02.005Z",
        "__v": 0,
        "id": "64338b889d30e909adbe568a"
      },
      "section": {
        "id": "64333b450ea788a84c9579e6",
        "name": "section 02"
      },
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'new resource name',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/resources/64338b889d30e909adbe568a',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete section resource assistant 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/resources/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Resource removed successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/resources/64338b889d30e909adbe568a',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### ASSIGNMENT SUBMISSIONS ⭐

###### Index section assignment submissions assistant 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/assignments/:id/submissions`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Submissions fetched successfully",
    "data": {
      "submissionsCount": 0,
      "submissions": []
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/assignments/64338e5c9d30e909adbe56ab/submissions',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show section assignment submission assistant 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/assignments/:id/submissions/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Submission fetched successfully",
    "data": {
      "submission": {
        "id": "64338e5c9d30e909adbe56ab",
        "student": {
          "id": "6430ce43c3ca49b01012f8ca",
          "name": "Ahmed"
        },
        "assignment": {
          "id": "6430ce43c3ca49b01012f8ca",
          "name": "assignment 01"
        },
        "section": {
          "id": "6430ce43c3ca49b01012f8ca",
          "name": "section 02"
        },
        "course": {
          "id": "6430ce43c3ca49b01012f8ca",
          "name": "machine learning"
        },
        "grade": 0,
        "submittedAt": "2021-09-30T12:00:00.000Z",
        "submittedFiles": [
          {
            "id": "6430ce43c3ca49b01012f8ca",
            "name": "file 01"
          }
        ]
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/assignments/64338e5c9d30e909adbe56ab/submissions/6430ce43c3ca49b01012f8ca',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

#### STUDENT 👨‍🎓

- `GET - api/v1/student/:id` - Show [Details](#show-student-)

##### ACCESS PERMISSOIN ⭐

###### Show student access permission 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "student fetched successfully",
    "data": {
      "student": {
        "id": "64339e899d30e909adbe56cc",
        "createdAt": "2023-04-10T05:28:41.127Z",
        "name": "mohamed yasser",
        "username": "mohamedyasser459rf",
        "academicId": "9879873833",
        "qrCode": "64339e889d30e909adbe56c8",
        "courses": [],
        "contacts": "64339e899d30e909adbe56ca"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01"
      },
      "program": {
        "id": "643052a83eea93f118839c46",
        "name": "public"
      },
      "department": {
        "id": "6430596c112031c1dbfc3fd8",
        "name": "computer science"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/64339e899d30e909adbe56cc',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### COURSE ⭐

###### Index courses student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Courses fetched successfully.",
    "data": {
      "courses": [
        {
          "id": "6430ce43c3ca49b01012f8ca",
          "name": "machine learning",
          "code": "cs45",
          "professor": {
            "_id": "6430c7854e29a1ff8375d1e7",
            "name": "dr. mohamed yasser"
          },
          "isEnrolled": false
        },
        {
          "id": "6430e37e95394133234b0cdf",
          "name": "image processing",
          "code": "cs45",
          "professor": {
            "_id": "6430c7854e29a1ff8375d1e7",
            "name": "dr. mohamed yasser"
          },
          "isEnrolled": false
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch('http://localhost:3000/api/v1/student/courses', {
    method: 'GET',
    headers: headersList,
  });

  let data = await response.text();
  console.log(data);
  ```

###### Show course student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Course fetched successfully.",
    "data": {
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning",
        "code": "cs45"
      },
      "professor": {
        "id": "6430c7854e29a1ff8375d1e7",
        "name": "dr. mohamed yasser"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "department": {
        "id": "6430596c112031c1dbfc3fd8",
        "name": "computer science"
      },
      "program": {
        "id": "643052a83eea93f118839c46",
        "name": "public"
      },
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430ce43c3ca49b01012f8ca',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Enroll course student 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/student/courses/:id/enroll`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Student enrolled in course successfully.",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430ce43c3ca49b01012f8ca/enroll',
    {
      method: 'POST',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### COURSE EXAM ⭐

###### Index course exams student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses/:id/exams`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Exams fetched successfully",
    "data": {
      "exams": [
        {
          "id": "6432e59cdde93cf76c5dae17",
          "name": "exam 01",
          "startAt": "2023-04-09T16:20:00.000Z",
          "endAt": "2023-04-09T16:40:00.000Z",
          "durationInMinutes": 20,
          "isActive": false
        },
        {
          "id": "6433047d101ff077ea746339",
          "name": "exam 01",
          "startAt": "2023-04-10T10:30:00.000Z",
          "endAt": "2023-04-10T10:50:00.000Z",
          "durationInMinutes": 20,
          "isActive": false
        },
        {
          "id": "64349c56162ca94a690b312e",
          "name": "exam 01",
          "startAt": "2023-04-10T23:33:00.000Z",
          "endAt": "2023-04-11T01:33:00.000Z",
          "durationInMinutes": 120,
          "isActive": true
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({});

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/exams',
    {
      method: 'GET',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Enroll course exam student 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/student/courses/:id/exams/:id/enroll`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Enrolled in exam successfully",
    "data": {
      "exam": {
        "id": "64349c56162ca94a690b312e",
        "name": "exam 01",
        "startAt": "2023-04-10T23:33:00.000Z",
        "endAt": "2023-04-11T01:33:00.000Z",
        "questions": [
          {
            "id": "64349ca2162ca94a690b3140",
            "contentText": "Question 1",
            "contentImage": "64349ca2162ca94a690b313f",
            "score": 7,
            "answers": [
              {
                "id": "64349ca2162ca94a690b3141",
                "contentText": "answer 1"
              },
              {
                "id": "64349ca2162ca94a690b3143",
                "contentText": "answer 2"
              },
              {
                "id": "64349ca2162ca94a690b3145",
                "contentText": "answer 3"
              }
            ]
          },
          {
            "id": "64349cb4162ca94a690b314e",
            "contentText": "Question 2",
            "contentImage": "64349cb4162ca94a690b314d",
            "score": 9,
            "answers": [
              {
                "id": "64349cb4162ca94a690b314f",
                "contentText": "answer 1"
              },
              {
                "id": "64349cb4162ca94a690b3151",
                "contentText": "answer 2"
              },
              {
                "id": "64349cb4162ca94a690b3153",
                "contentText": "answer 3"
              }
            ]
          }
        ]
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzNDllMWI3MDVhMTRjMjdhYWU1MTI3Iiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTY5OTYxLCJleHAiOjE2ODM3NjE5NjF9.BwcErknbAN7_5RbJ0tqNjFehR-qCIPrI0lRr9xqZPCE',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/exams/64349c56162ca94a690b312e/enroll',
    {
      method: 'POST',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Submit course exam student 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/student/courses/:id/exams/:id/submit`
- _Headers:_ `Authorization`
- _Body:_
  ```json
  {
    "questionsWithAnswers": [
      "{question: '64349ca2162ca94a690b3140', answer: '64349ca2162ca94a690b3143'}",
      "{question: '64349cb4162ca94a690b314e', answer: '64349cb4162ca94a690b314f'}"
    ]
  }
  ```
- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Exam submitted successfully.",
    "data": {
      "totalScore": 16,
      "studentScore": 16
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzNDllMWI3MDVhMTRjMjdhYWU1MTI3Iiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTY5OTYxLCJleHAiOjE2ODM3NjE5NjF9.BwcErknbAN7_5RbJ0tqNjFehR-qCIPrI0lRr9xqZPCE',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    questionsWithAnswers: [
      "{question: '64349ca2162ca94a690b3140', answer: '64349ca2162ca94a690b3143'}",
      "{question: '64349cb4162ca94a690b314e', answer: '64349cb4162ca94a690b314f'}",
    ],
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/exams/64349c56162ca94a690b312e/submit',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### COURSE ASSIGNMENT ⭐

###### Index course assignments student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses/:id/assignments`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assignments fetched successfully",
    "assignments": [
      {
        "id": "6434a25263372d0aa8ecba3f",
        "title": "python cgi",
        "isExpired": false,
        "dueDate": "2023-04-17T23:57:06.076Z"
      }
    ]
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/assignments',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show course assignments student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses/:id/assignments/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assignment fetched successfully",
    "assignment": {
      "id": "6434a25263372d0aa8ecba3f",
      "title": "python cgi",
      "contentText": "In this assignment you should create a full python server side application and apply all CGI concepts we have learned in the lecture and section",
      "contentImage": "6434a25263372d0aa8ecba3e",
      "dueDate": "2023-04-17T23:57:06.076Z",
      "isExpired": false
    },
    "professor": {
      "id": "6430c7854e29a1ff8375d1e7",
      "name": "dr. mohamed yasser"
    },
    "course": {
      "id": "6430e37e95394133234b0cdf",
      "name": "image processing"
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/assignments/6434a25263372d0aa8ecba3f',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Submit course assignment student 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/student/courses/:id/assignments/:id/submit`
- _Headers:_ `Authorization`
- _Body:_

  ```json
  {
    "note": "this is student note",
    "fileType": "png"
  }
  ```

- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Assignment submitted successfully",
    "data": {
      "assignmentSubmission": {
        "file": "6434a2ac63372d0aa8ecba4f",
        "note": "this is student note",
        "assignment": "6434a25263372d0aa8ecba3f",
        "student": "64339e899d30e909adbe56cc",
        "course": "6430e37e95394133234b0cdf",
        "_id": "6434a2ac63372d0aa8ecba50",
        "createdAt": "2023-04-10T23:58:36.116Z",
        "updatedAt": "2023-04-10T23:58:36.116Z",
        "__v": 0,
        "id": "6434a2ac63372d0aa8ecba50"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    note: 'this is student note',
    fileType: 'png',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/assignments/6434a25263372d0aa8ecba3f/submit',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

- `GET - api/v1/student/courses/:id/assistants` - Index [Details](#index-course-assistants-student-)

##### COURSE ASSISTANTS ⭐

###### Index course assistants student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses/:id/assistants`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assistants fetched successfully.",
    "data": {
      "assistants": [
        {
          "id": "6434a4d063372d0aa8ecba6d",
          "name": "mohamed yasser"
        },
        {
          "id": "6434a4ff63372d0aa8ecba7e",
          "name": "mohamed yasser"
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/assistants',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### SECTION ⭐

###### Index sections student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses/:id/assistants/:id/sections`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Sections fetched successfully.",
    "data": {
      "sections": [
        {
          "id": "6434a6a363372d0aa8ecbaa5",
          "name": "section 02"
        }
      ],
      "assistant": {
        "id": "6434a64263372d0aa8ecba8f",
        "name": "mo"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/assistants/6434a64263372d0aa8ecba8f/sections',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show section student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses/:id/assistants/:id/sections/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Section found",
    "data": {
      "section": {
        "_id": "6434a6a363372d0aa8ecbaa5",
        "name": "section 02",
        "number": 2,
        "resources": [],
        "assistant": "6434a64263372d0aa8ecba8f",
        "course": "6430e37e95394133234b0cdf",
        "assignments": [],
        "createdAt": "2023-04-11T00:15:31.694Z",
        "updatedAt": "2023-04-11T00:15:31.694Z",
        "__v": 0
      },
      "assistant": {
        "id": "6434a64263372d0aa8ecba8f",
        "name": "mo"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/assistants/6434a64263372d0aa8ecba8f/sections/6434a6a363372d0aa8ecbaa5',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### SECTION RESOURCES ⭐

###### Index section resources student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses/:id/assistants/:id/sections/:id/resources`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Section resources fetched successfully",
    "data": {
      "resources": [
        {
          "_id": "6434abd1e7b70ce6c7e5d3af",
          "path": "courses/6430e37e95394133234b0cdf/sections/6434a6a363372d0aa8ecbaa5/resources/bc192957-fb34-4ef6-96ce-13fdb1ce0c78.png",
          "type": "image/png",
          "name": "section resource for the whiteboard",
          "owner": "6434a64263372d0aa8ecba8f",
          "createdAt": "2023-04-11T00:37:37.347Z",
          "updatedAt": "2023-04-11T00:37:37.347Z",
          "__v": 0,
          "id": "6434abd1e7b70ce6c7e5d3af"
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/assistants/6434a64263372d0aa8ecba8f/sections/6434a6a363372d0aa8ecbaa5/resources',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### SECTION ASSIGNMENT ⭐

###### Index section assignments student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses/:id/assistants/:id/sections/:id/assignments`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assignments fetched successfully",
    "assignments": [
      {
        "id": "6434ada7e7b70ce6c7e5d3cd",
        "title": "this is new assignment for the section",
        "isExpired": false,
        "dueDate": "2023-04-16T00:45:27.915Z"
      }
    ]
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/assistants/6434a64263372d0aa8ecba8f/sections/6434a6a363372d0aa8ecbaa5/assignments',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show section assignment student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses/:id/assistants/:id/sections/:id/assignments/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assignment fetched successfully",
    "assignment": {
      "id": "6434ada7e7b70ce6c7e5d3cd",
      "title": "this is new assignment for the section",
      "contentText": "in this assignment you should create static website using htm, css, js",
      "contentImage": "6434ada7e7b70ce6c7e5d3cc",
      "dueDate": "2023-04-16T00:45:27.915Z",
      "isExpired": false
    },
    "assistant": {
      "id": "6434a64263372d0aa8ecba8f",
      "name": "mo"
    },
    "section": {
      "id": "6434a6a363372d0aa8ecbaa5",
      "name": "section 02"
    },
    "course": {
      "id": "6430e37e95394133234b0cdf",
      "name": "image processing"
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/assistants/6434a64263372d0aa8ecba8f/sections/6434a6a363372d0aa8ecbaa5/assignments/6434ada7e7b70ce6c7e5d3cd',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Submit section assignment student 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/student/courses/:id/assistants/:id/sections/:id/assignments/:id/submit`
- _Headers:_ `Authorization`
- _Body:_
  ```json
  {
    "note": "this is student note",
    "fileType": "png"
  }
  ```
- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Assignment submitted successfully",
    "data": {
      "assignmentSubmission": {
        "file": "6434aeec91da347928a86084",
        "note": "this is student note",
        "assignment": "6434ada7e7b70ce6c7e5d3cd",
        "student": "64339e899d30e909adbe56cc",
        "course": "6430e37e95394133234b0cdf",
        "section": "6434a6a363372d0aa8ecbaa5",
        "_id": "6434aeec91da347928a86085",
        "createdAt": "2023-04-11T00:50:52.142Z",
        "updatedAt": "2023-04-11T00:50:52.142Z",
        "__v": 0,
        "id": "6434aeec91da347928a86085"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    note: 'this is student note',
    fileType: 'png',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/assistants/6434a64263372d0aa8ecba8f/sections/6434a6a363372d0aa8ecbaa5/assignments/6434ada7e7b70ce6c7e5d3cd/submit',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### SECTION ATTENDANCE ⭐

###### Show section attendance student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses/:id/assistants/:id/sections/:id/attendance/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Attendance fetched successfully.",
    "data": {
      "attendance": {
        "id": "6434b4e9b8a4dc5e28d1c321",
        "isAttended": true
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/assistants/6434a64263372d0aa8ecba8f/sections/6434a6a363372d0aa8ecbaa5/attendance/6434b4e9b8a4dc5e28d1c321',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Attend section attendance student 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/student/courses/:id/assistants/:id/sections/:id/attendance/:id/attend`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Attended section successfully.",
    "data": {
      "attendance": {
        "id": "6434b4e9b8a4dc5e28d1c321",
        "isAttended": true
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzNGI2ZWNjY2Q3YWIyZTUwOGIyYTliIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTc2MzE5LCJleHAiOjE2ODM3NjgzMTl9.7ezCeW-eVpO5yepCy6UH41vHQmF7Kvux8HybKeg-T_w',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    randomAccessKey: 'en0JNha0iU',
    lat: '31.205753',
    lng: '29.924526',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/assistants/6434a64263372d0aa8ecba8f/sections/6434a6a363372d0aa8ecbaa5/attendance/6434b4e9b8a4dc5e28d1c321/attend',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### LECTURE ⭐

###### Index lectures student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses/:id/lectures`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Lectures fetched successfully.",
    "data": {
      "lectures": [
        {
          "id": "6434b916ccd7ab2e508b2ac3",
          "name": "lecture 03",
          "number": 3
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/lectures',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show lecture student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses/:id/lectures/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Lecture fetched successfully.",
    "data": {
      "lecture": {
        "id": "6434b916ccd7ab2e508b2ac3",
        "name": "lecture 03",
        "number": 3,
        "resources": [],
        "createdAt": "2023-04-11T01:34:14.436Z"
      },
      "attendance": {}
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/lectures/6434b916ccd7ab2e508b2ac3',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### LECTURE RESOURCES ⭐

###### Index lecture resources student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses/:id/lectures/:id/resources`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Lecture resources fetched successfully",
    "data": {
      "resources": [
        {
          "_id": "6434be45b5d96421078c210a",
          "path": "courses/6430e37e95394133234b0cdf/lecture/6434b916ccd7ab2e508b2ac3/resources/c4e01461-414b-4f38-9c2f-a4b114ad4dc3.png",
          "type": "image/png",
          "name": "lecture 01 - resource",
          "owner": "6430c7854e29a1ff8375d1e7",
          "createdAt": "2023-04-11T01:56:21.752Z",
          "updatedAt": "2023-04-11T01:56:21.752Z",
          "__v": 0,
          "id": "6434be45b5d96421078c210a"
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/lectures/6434b916ccd7ab2e508b2ac3/resources',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

- `GET - api/v1/student/courses/:id/lectures/:id/attendance/:id` - Show [Details](#show-lecture-attendance-student-)
- `POST - api/v1/student/courses/:id/lectures/:id/attendance/:id/attend` - Attend [Details](#attend-lecture-attendance-student-)

##### LECTURE ATTENDANCE ⭐

###### Show lecture attendance student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses/:id/lectures/:id/attendance/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Attendance fetched successfully.",
    "data": {
      "attendance": {
        "id": "6434c0f21c684c5985ccaf70",
        "isAttended": true
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/lectures/6434b916ccd7ab2e508b2ac3/attendance/6434c0f21c684c5985ccaf70',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Attend lecture attendance student 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/student/courses/:id/lectures/:id/attendance/:id/attend`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Student attended successfully.",
    "data": {
      "attendance": {
        "id": "6434c0f21c684c5985ccaf70",
        "isAttended": true
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    randomAccessKey: 'lY4RWSzvxD',
    lat: '30.9977',
    lng: '29.7432',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/lectures/6434b916ccd7ab2e508b2ac3/attendance/6434c0f21c684c5985ccaf70/attend',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### CONTACTS ⭐

###### Show contact 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/contacts/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Contact updated successfully",
    "data": {
      "contact": {
        "phoneNumber": {
          "code": "20",
          "number": "1224440417"
        },
        "whatsapp": {
          "code": "20",
          "number": "1224440417"
        },
        "_id": "64339e899d30e909adbe56ca",
        "createdAt": "2023-04-10T05:28:41.012Z",
        "updatedAt": "2023-04-11T02:26:40.467Z",
        "__v": 0,
        "email": "hi@gmail.com",
        "facebook": "www.facebook.com",
        "twitter": "iammo26",
        "telegram": "iammo26"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    email: 'hi@gmail.com',
    phoneCode: '20',
    phoneNumber: '1224440417',
    facebookLink: 'www.facebook.com',
    twitterUsername: 'iammo26',
    whatsappCode: '20',
    WhatsappNumber: '1224440417',
    telegramUsername: 'iammo26',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/contacts/64339e899d30e909adbe56ca',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update contact 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/contacts/:id`
- _Headers:_ `Authorization`
- _Body:_
  ```json
  {
    "email": "hi@gmail.com",
    "phoneCode": "20",
    "phoneNumber": "1224440417",
    "facebookLink": "www.facebook.com",
    "twitterUsername": "iammo26",
    "whatsappCode": "20",
    "WhatsappNumber": "1224440417",
    "telegramUsername": "iammo26"
  }
  ```
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Contact updated successfully",
    "data": {
      "contact": {
        "phoneNumber": {
          "code": "20",
          "number": "1224440417"
        },
        "whatsapp": {
          "code": "20",
          "number": "1224440417"
        },
        "_id": "64339e899d30e909adbe56ca",
        "createdAt": "2023-04-10T05:28:41.012Z",
        "updatedAt": "2023-04-11T02:26:40.467Z",
        "__v": 0,
        "email": "hi@gmail.com",
        "facebook": "www.facebook.com",
        "twitter": "iammo26",
        "telegram": "iammo26"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    email: 'hi@gmail.com',
    phoneCode: '20',
    phoneNumber: '1224440417',
    facebookLink: 'www.facebook.com',
    twitterUsername: 'iammo26',
    whatsappCode: '20',
    WhatsappNumber: '1224440417',
    telegramUsername: 'iammo26',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/contacts/64339e899d30e909adbe56ca',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### STORAGE ⭐

###### Upload storage 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/storage/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Uploadable url generated successfully",
    "data": {
      "storage": {
        "_id": "6434be45b5d96421078c210a",
        "path": "courses/6430e37e95394133234b0cdf/lecture/6434b916ccd7ab2e508b2ac3/resources/c4e01461-414b-4f38-9c2f-a4b114ad4dc3.png",
        "type": "image/png",
        "name": "lecture 01 - resource",
        "owner": "6430c7854e29a1ff8375d1e7",
        "createdAt": "2023-04-11T01:56:21.752Z",
        "updatedAt": "2023-04-11T01:56:21.752Z",
        "__v": 0,
        "id": "6434be45b5d96421078c210a"
      },
      "uploadUrl": "https://unista-dev.s3.amazonaws.com/courses/6430e37e95394133234b0cdf/lecture/6434b916ccd7ab2e508b2ac3/resources/c4e01461-414b-4f38-9c2f-a4b114ad4dc3.png?Content-Type=image%2Fpng&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAZUKGZYJVW6D5G2HU%2F20230411%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20230411T015658Z&X-Amz-Expires=300&X-Amz-Signature=86e208064373f14210632d48731a419a6f6771291fd24a366673816d080ce92f&X-Amz-SignedHeaders=host",
      "accessUrl": "https://unista-dev.s3.amazonaws.com/courses/6430e37e95394133234b0cdf/lecture/6434b916ccd7ab2e508b2ac3/resources/c4e01461-414b-4f38-9c2f-a4b114ad4dc3.png?AWSAccessKeyId=AKIAZUKGZYJVW6D5G2HU&Expires=1681178518&Signature=7O4kzrVY1yNOz0CKi26zYqLBZLM%3D"
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjNlN2M0M2EwZTc4YmVkNzdiMGNhMzg1Iiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2Nzg5NTkzMjAsImV4cCI6MTY4MTU1MTMyMH0.kqKSNP7bBAyo2KtstKA7ESMqCmh0_4Csm6sdXy9k3-o',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/storage/6434be45b5d96421078c210a',
    {
      method: 'POST',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Access storage 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/storage/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Accessable url generated successfully",
    "data": {
      "url": "https://unista-dev.s3.amazonaws.com/courses/6430e37e95394133234b0cdf/assignments/6434ada7e7b70ce6c7e5d3cd/submissions/76941587-e0f8-495b-879f-af5941a1670b.png?AWSAccessKeyId=AKIAZUKGZYJVW6D5G2HU&Expires=1681174845&Signature=xKQ1DjxtU%2FW9OxuYQ7QVnwVzLnA%3D",
      "storage": {
        "_id": "6434aeec91da347928a86084",
        "path": "courses/6430e37e95394133234b0cdf/assignments/6434ada7e7b70ce6c7e5d3cd/submissions/76941587-e0f8-495b-879f-af5941a1670b.png",
        "type": "image/png",
        "name": "76941587-e0f8-495b-879f-af5941a1670b.png",
        "createdAt": "2023-04-11T00:50:52.021Z",
        "updatedAt": "2023-04-11T00:50:52.021Z",
        "__v": 0,
        "id": "6434aeec91da347928a86084"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjNlN2M0M2EwZTc4YmVkNzdiMGNhMzg1Iiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2Nzg5NTkzMjAsImV4cCI6MTY4MTU1MTMyMH0.kqKSNP7bBAyo2KtstKA7ESMqCmh0_4Csm6sdXy9k3-o',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/storage/6434aeec91da347928a86084',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```
## API Endpoint Routes 📌

### Intro 📌

- Hello everybody, it's Mohamed here, a computer science student, I'm excited to share with you my final year graduation project which's called Unista. It's a complete Learning Management System for universities, powered with the essential functionalities required for online learning today.

- I've built everything from scratch, including the ERD design, database, backend APIs, and a basic UI prototype. I've also implemented testing suites and a CI/CD pipeline to ensure its quality and efficiency.

- We have 5 main user roles (Master, Admin, Professor, Assistant, Student) and each role has different permissions.

    - The master is responsible for the initial setup of the system and creating professors and assistants for each college, as well as administrators for each level.

    - Admins are responsible for creating courses, assigning professors to each course, and enrolling students from each department.

    - The professor is responsible for creating assignments and exams, uploading course e-books, creating lectures and uploading lecture files, taking attendance, and performing various other tasks.

    - The assistant is responsible for creating sections and assignments for each section, uploading section files, taking attendance, and performing various other tasks.

    - The student can access and utilize all resources created by professors and assistants, such as assignments, exams, lectures, section files, attendance records, and various other materials and activities.
### How we store and fetch files (AWS S3 PRESIGNED URL) 📁

[Check my blog about different file upload solutions](https://iammo69.web.app/file-upload-solutions.html)
![AWS S3 Presigned URL System](https://i.imgur.com/RDysto9.png)


### SECURITY 🔐

- `JWT` authentication.
- `ACL` authorization.
- `Rate Limiting` protection. (Prevent brute force attacks)
- All files are accessible only by `Presigned URL` (AWS S3) which will be expired after **_n_** minutes.
- Define `CORS` policy to allow only specific domains.
- Header security using `Helmet` package.
- Passwords are hashed using in un-reversible algorithm `bcrypt`.
- Strict endpoint validation system (IDs, etc).

### API VERSIONING 📦

- All routes are versioned by default `GET - api/v1/courses`

### TECH STACK (main) 📚

- NodeJS
- ExpressJS
- MongoDB
- Mongoose
- AWS S3

### DEPLOYMENT STACK (CI/CD) 🚀

- Docker 
- Kubernetes (AWS EKS) 
- AWS EC2
- Travis CI
- Nginx 


### Code Features 📌
- [x] CRUD (Create, Read, Update, Delete) for all resources using RESTful API design
- [x] Index Pagination - Search - Sort - Select - Filter
- [x] API Versioning (v1)
- [x] Best Practices & Clean Code (MVC, SOLID, DRY, KISS)
- [x] API Documentation
- [x] Scalable System (You can add as much features as you want without breaking the system)
- [x] Error Handling System (Genaric error handler middleware with Correct HTTP Status Code & Error message)


### Unista Features 📌

- [x] Authentication login using 3 different ways (credentials, scan QR code, upload QR code)
- [x] Role based system (Master, Admin, Professor, Assistant, Student)
- [x] Smart attendace system (QR Code)
- [x] Accurate Geolocation system (GPS) for attendance
- [x] Secure Exam system (No way to cheat)
- [x] Auto genrate exam questions (MCQ, True/False, Fill in the blanks) based on uploaded course e-book.
- [x] Assignments system
- [x] Fast - secure - scalable file system (AWS S3)
- [x] Horizontal Scaling (Kubernetes add pods(EC2) to scale horizontally if CPU usage is high)
- [x] MORE TO COME...

### TODOs 📝

- [ ] Add `Redis` for caching
- [ ] Add `Jest` for testing (unit, integration)
- [ ] Add `Notification` system
- [ ] Add `Emailing` system
- [ ] Enhance `NodeJS` performance [My blog about node clustring](https://iammo69.web.app/enhance-node-performance.html)
- [ ] Add `Chat` system
- [ ] Add `Video conferencing` system
- [ ] Add `Student activities` system
- [ ] Add `Student to student learning` system
- [ ] Add `Vote` system
- [ ] Add `DOSS` protection
### STATISTICS 📈

_API-Endpoint Routes_: **157**


### Environment Variables 🌐

```bash
# ENV info
NODE_ENV="dev"
# PORT info
PORT_DEV="xxxxxxx"
PORT_PROD="xxxxxxx"
PORT_TEST="xxxxxxx"
# DB connection info
DB_USER_DEV="xxxxxxx"
DB_USER_PROD="xxxxxxx"
DB_USER_TEST="xxxxxxx"
DB_PASSWORD_DEV="xxxxxxx"
DB_PASSWORD_PROD="xxxxxxx"
DB_PASSWORD_TEST="xxxxxxx"
DB_HOST_DEV="xxxxxxx"
DB_HOST_PROD="xxxxxxx"
DB_HOST_TEST="xxxxxxx"
# CORS config
CORS_ORIGIN_DEV="xxxxxxx"
CORS_ORIGIN_PROD="xxxxxxx"
CORS_ORIGIN_TEST="xxxxxxx"
# REQ limit
REQUEST_LIMIT_TIMEOUT_DEV="xxxxxxx"
REQUEST_LIMIT_TIMEOUT_PROD="xxxxxxx"
REQUEST_LIMIT_TIMEOUT_TEST="xxxxxxx"
REQUEST_LIMIT_MAX_DEV="xxxxxxx"
REQUEST_LIMIT_MAX_PROD="xxxxxxx"
REQUEST_LIMIT_MAX_TEST="xxxxxxx"
# BCRYPT config
BCRYPT_SALT_ROUNDS_DEV="xxxxxxx"
BCRYPT_SALT_ROUNDS_PROD="xxxxxxx"
BCRYPT_SALT_ROUNDS_TEST="xxxxxxx"
BCRYPT_PEPPER_DEV="xxxxxxx"
BCRYPT_PEPPER_PROD="xxxxxxx"
BCRYPT_PEPPER_TEST="xxxxxxx"
# JWT config
JWT_SECRET_DEV="xxxxxxx"
JWT_SECRET_PROD="xxxxxxx"
JWT_SECRET_TEST="xxxxxxx"
JWT_EXPIRES_IN_DEV="xxxxxxx"
JWT_EXPIRES_IN_PROD="xxxxxxx"
JWT_EXPIRES_IN_TEST="xxxxxxx"
# URL
URL_DEV="xxxxxxx"
URL_TEST="xxxxxxx"
URL_PROD="xxxxxxx"
# SECRET KEYS
MASTER_SECRET_KEY_DEV="xxxxxxx"
MASTER_SECRET_KEY_TEST="xxxxxxx"
MASTER_SECRET_KEY_PROD="xxxxxxx"
# AWS
AWS_ACCESS_KEY_ID_DEV="xxxxxxx"
AWS_ACCESS_KEY_ID_TEST="xxxxxxx"
AWS_ACCESS_KEY_ID_PROD="xxxxxxx"
AWS_SECRET_ACCESS_KEY_DEV="xxxxxxx"
AWS_SECRET_ACCESS_KEY_TEST="xxxxxxx"
AWS_SECRET_ACCESS_KEY_PROD="xxxxxxx"
AWS_REGION_DEV="xxxxxxx"
AWS_REGION_TEST="xxxxxxx"
AWS_REGION_PROD="xxxxxxx"
AWS_BUCKET_NAME_DEV="xxxxxxx"
AWS_BUCKET_NAME_TEST="xxxxxxx"
AWS_BUCKET_NAME_PROD="xxxxxxx"
AWS_EXPIRES_IN_MINUTES_DEV="xxxxxxx"
AWS_EXPIRES_IN_MINUTES_TEST="xxxxxxx"
AWS_EXPIRES_IN_MINUTES_PROD="xxxxxxx"
RANDOM_CHARS_DEV="xxxxxxxxxxxxxxx"
RANDOM_CHARS_LENGTH_DEV="xxxxxxx"
RANDOM_CHARS_TEST="xxxxxxxxxxxxxxx"
RANDOM_CHARS_LENGTH_TEST="xxxxxxx"
RANDOM_CHARS_PROD="xxxxxxxxxxxxxxx"
RANDOM_CHARS_LENGTH_PROD="xxxxxxx"
API_ENDPOINT_DEV="xxxxxxx"
API_ENDPOINT_TEST="xxxxxxx"
API_ENDPOINT_PROD="xxxxxxx"
API_TOKEN_DEV="xxxxxxx"
API_TOKEN_TEST="xxxxxxx"
API_TOKEN_PROD="xxxxxxx"
```

### Installation 📥

```bash
# Clone the repo
git clone
# Install dependencies
npm install
# Run the app
npm start
# Run the app in development mode
npm run dev:fast
```

### Success Response Format ✅

```json
{
  "status": "success",
  "message": "Success message",
  "data": {
    "user": {
      "id": "642debe976e91123782b7f42",
      "name": "John Doe"
    }
  }
}
```

### Error Response Format ❌

```json
{
  "status": "Error",
  "message": "Error message"
}
```

### HINTS 📝

- All index routes are paginated by default, you can pass `page` and `limit` as query params to change the pagination.
  Example: `GET - api/v1/courses?page=2&limit=10`

### API DOCUMENTATION 📖
### All Endpoints (overview) 📡

#### Authentication 🔐

##### Login ⭐

- `POST - api/v1/auth/login` - Login [Details](#login-)

#### MASTER 🔑

##### UNIVERSITY ⭐

- `GET - api/v1/master/universities` - Index [Details](#index-universities-)
- `POST - api/v1/master/universities` - Create [Details](#create-university-)
- `GET - api/v1/master/universities/:id` - Show [Details](#show-university-)
- `PATCH - api/v1/master/universities/:id` - Update [Details](#update-university-)
- `DELETE - api/v1/master/universities/:id` - Delete [Details](#delete-university-)

##### COLLAGE TYPE ⭐

- `POST - api/v1/master/collage-types` - Create [Details](#create-collage-type-)
- `GET - api/v1/master/collage-types` - Index [Details](#index-collage-types-)
- `GET - api/v1/master/collage-types/:id` - Show [Details](#show-collage-type-)
- `PATCH - api/v1/master/collage-types/:id` - Update [Details](#update-collage-type-)
- `DELETE - api/v1/master/collage-types/:id` - Delete [Details](#delete-collage-type-)

##### COLLAGE ⭐

- `POST - api/v1/master/universities/:id/collages` - Create [Details](#create-collage-)
- `GET - api/v1/master/universities/:id/collages` - Index [Details](#index-collages-)
- `GET - api/v1/master/universities/:id/collages/:id` - Show [Details](#show-collage-)
- `PATCH - api/v1/master/universities/:id/collages/:id` - Update [Details](#update-collage-)
- `DELETE - api/v1/master/universities/:id/collages/:id` - Delete [Details](#delete-collage-)

##### LEVEL ⭐

- `POST - api/v1/master/universities/:id/collages/levels` - Create [Details](#create-level-)
- `GET - api/v1/master/universities/:id/collages/levels` - Index [Details](#index-levels-)
- `GET - api/v1/master/universities/:id/collages/levels/:id` - Show [Details](#show-level-)
- `PATCH - api/v1/master/universities/:id/collages/levels/:id` - Update [Details](#update-level-)
- `DELETE - api/v1/master/universities/:id/collages/levels/:id` - Delete [Details](#delete-level-)

##### PROFESSOR ⭐

- `POST - api/v1/master/universities/:id/collages/:id/professors` - Create [Details](#create-professor-)
- `GET - api/v1/master/universities/:id/collages/:id/professors` - Index [Details](#index-professors-)
- `GET - api/v1/master/universities/:id/collages/:id/professors/:id` - Show [Details](#show-professor-)
- `PATCH - api/v1/master/universities/:id/collages/:id/professors/:id` - Update [Details](#update-professor-)
- `DELETE - api/v1/master/universities/:id/collages/:id/professors/:id` - Delete [Details](#delete-professor-)

##### ADMIN ⭐

- `POST - api/v1/master/universities/:id/collages/:id/levels/:id/admins` - Create [Details](#create-admin-)
- `GET - api/v1/master/universities/:id/collages/:id/levels/:id/admins` - Index [Details](#index-admins-)
- `GET - api/v1/master/universities/:id/collages/:id/levels/:id/admins/:id` - Show [Details](#show-admin-)
- `PATCH - api/v1/master/universities/:id/collages/:id/levels/:id/admins/:id` - Update [Details](#update-admin-)
- `DELETE - api/v1/master/universities/:id/collages/:id/levels/:id/admins/:id` - Delete [Details](#delete-admin-)

#### ADMIN 👔

##### ACCESS PERMISSOIN ⭐

- `GET - api/v1/admin/:id` - Show [Details](#show-admin-)
- `PATCH - api/v1/admin/:id` - Update [Details](#update-admin-)

##### PROGRAM ⭐

- `POST - api/v1/admin/universities/:id/collages/:id/levels/:id/programs` - Create [Details](#create-program-)
- `GET - api/v1/admin/universities/:id/collages/:id/levels/:id/programs` - Index [Details](#index-programs-)
- `GET - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id` - Show [Details](#show-program-)
- `PATCH - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id` - Update [Details](#update-program-)
- `DELETE - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id` - Delete [Details](#delete-program-)

##### DEPARTMENT ⭐

- `POST - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments` - Create [Details](#create-department-)
- `GET - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments` - Index [Details](#index-departments-)
- `GET - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id` - Show [Details](#show-department-)
- `PATCH - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id` - Update [Details](#update-department-)
- `DELETE - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id` - Delete [Details](#delete-department-)

##### Student ⭐

- `POST - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id/students` - Create [Details](#create-student-)
- `GET - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id/students` - Index [Details](#index-students-)
- `GET - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id/students/:id` - Show [Details](#show-student-)
- `PATCH - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id/students/:id` - Update [Details](#update-student-)
- `DELETE - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id/students/:id` - Delete [Details](#delete-student-)

##### QUICK ACCESS ⭐

- `GET - api/v1/admin/:id/levels/:id` - Show admin level [Details](#show-admin-level-)

#### PROFESSOR 👨‍🏫

##### ACCESS PERMISSOIN ⭐

- `GET - api/v1/professor/:id` - Show [Details](#show-professor-)
- `PATCH - api/v1/professor/:id` - Update [Details](#update-professor-)

##### COURSE ⭐

- `POST - api/v1/professor/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id/courses` - Create [Details](#create-course-)
- `DELETE - api/v1/professor/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id/courses/:id` - Delete [Details](#delete-course-)
- `GET - api/v1/professor/courses` - Index [Details](#index-courses-)
- `GET - api/v1/professor/courses/:id` - Show [Details](#show-course-)
- `PATCH - api/v1/professor/courses/:id` - Update [Details](#update-course-)

##### EBOOK ⭐

- `POST - api/v1/professor/courses/:id/ebook` - Create [Details](#create-ebook-)
- `GET - api/v1/professor/courses/:id/ebook/:id` - Show [Details](#show-ebook-)
- `PATCH - api/v1/professor/courses/:id/ebook/:id` - Update [Details](#update-ebook-)
- `DELETE - api/v1/professor/courses/:id/ebook/:id` - Delete [Details](#delete-ebook-)

##### ASSISTANT ⭐

- `POST - api/v1/professor/universities/:id/collages/:id/courses/:id/assistants` - Create [Details](#create-assistant-)
- `POST -  api/v1/professor/universities/:id/collages/:id/courses/:id/assistants/:id/attach` - Attach [Details](#attach-assistant-)
- `PATCH - api/v1/professor/universities/:id/collages/:id/courses/:id/assistants/:id` - Update [Details](#update-assistant-)
- `DELETE - api/v1/professor/universities/:id/collages/:id/courses/:id/assistants/:id` - Delete [Details](#delete-assistant-)
- `GET - api/v1/professor/universities/:id/collages/:id/courses/:id/assistants/:id` - Show [Details](#show-assistant-)
- `GET - api/v1/professor/universities/:id/collages/:id/courses/:id/assistants` - Index By Course [Details](#index-assistants-by-course-)
- `GET - api/v1/professor/universities/:id/collages/:id/assistants` - Index By Collage [Details](#index-assistants-by-collage-)

##### LECTURE ⭐

- `POST - api/v1/professor/courses/:id/lectures` - Create [Details](#create-lecture-)
- `GET - api/v1/professor/courses/:id/lectures` - Index [Details](#index-lectures-)
- `GET - api/v1/professor/courses/:id/lectures/:id` - Show [Details](#show-lecture-)
- `PATCH - api/v1/professor/courses/:id/lectures/:id` - Update [Details](#update-lecture-)
- `DELETE - api/v1/professor/courses/:id/lectures/:id` - Delete [Details](#delete-lecture-)

##### LECTURE RESOURCE ⭐

- `POST - api/v1/professor/courses/:id/lectures/:id/resources` - Create [Details](#create-lecture-resource-)
- `GET - api/v1/professor/courses/:id/lectures/:id/resources` - Index [Details](#index-lecture-resources-)
- `GET - api/v1/professor/courses/:id/lectures/:id/resources/:id` - Show [Details](#show-lecture-resource-)
- `PATCH - api/v1/professor/courses/:id/lectures/:id/resources/:id` - Update [Details](#update-lecture-resource-)
- `DELETE - api/v1/professor/courses/:id/lectures/:id/resources/:id` - Delete [Details](#delete-lecture-resource-)

##### QUICK INDEX ⭐

- `GET - api/v1/professor/universities/:id/collages/:id/levels` - levels [Details](#index-levels-professor-)
- `GET - api/v1/professor/universities/:id/collages/:id/levels/:id/programs` - programs [Details](#index-programs-professor-)
- `GET - api/v1/professor/universities/:id/collages/:id/levels/:id/programs/:id/departments` - departments [Details](#index-departments-professor-)

##### ATTENDANCE ( QR CODE & LOCATION ) ⭐

- `POST - api/v1/professor/courses/:id/lectures/:id/attendance` - Create [Details](#create-attendance-)
- `GET - api/v1/professor/courses/:id/lectures/:id/attendance/:id` - Show [Details](#show-attendance-)
- `GET - api/v1/professor/courses/:id/lectures/:id/attendance/:id/students` - Index Students [Details](#index-attendance-students-)
- `DELETE - api/v1/professor/courses/:id/lectures/:id/attendance/:id/students/:id` - Delete Student [Details](#delete-attendance-student-)

##### COURSE ASSIGNMENT ⭐

- `POST - api/v1/professor/courses/:id/assignments` - Create [Details](#create-course-assignment-)
- `GET - api/v1/professor/courses/:id/assignments` - Index [Details](#index-course-assignments-)
- `GET - api/v1/professor/courses/:id/assignments/:id` - Show [Details](#show-course-assignment-)
- `PATCH - api/v1/professor/courses/:id/assignments/:id` - Update [Details](#update-course-assignment-)
- `DELETE - api/v1/professor/courses/:id/assignments/:id` - Delete [Details](#delete-course-assignment-)

##### COURSE ASSIGNMENT SUBMISSIONS ⭐

- `GET - api/v1/professor/courses/:id/assignments/:id/submissions` - Index [Details](#index-course-assignment-submissions-)
- `GET - api/v1/professor/courses/:id/assignments/:id/submissions/:id` - Show [Details](#show-course-assignment-submission-)

##### EXAM ⭐

- `POST - api/v1/professor/courses/:id/exams` - Create [Details](#create-exam-)
- `POST - api/v1/professor/courses/:id/exams/:id/start-now` - Start now [Details](#start-now-exam-)
- `GET - api/v1/professor/courses/:id/exams` - Index [Details](#index-exams-)
- `GET - api/v1/professor/courses/:id/exams/:id` - Show [Details](#show-exam-)
- `PATCH - api/v1/professor/courses/:id/exams/:id` - Update [Details](#update-exam-)
- `DELETE - api/v1/professor/courses/:id/exams/:id` - Delete [Details](#delete-exam-)

##### EXAM ENROLLMENTS ⭐

- `GET - api/v1/professor/courses/:id/exams/:id/enrollments` - Index [Details](#index-exam-enrollments-)

##### EXAM SUBMISSIONS ⭐

- `GET - api/v1/professor/courses/:id/exams/:id/submissions` - Index [Details](#index-exam-submissions-)

##### EXAM QUESTIONS ( Text and/or Image or both ) ⭐

- `POST - api/v1/professor/courses/:id/exams/:id/questions` - Create [Details](#create-exam-question-)
- `GET - api/v1/professor/courses/:id/exams/:id/questions` - Index [Details](#index-exam-questions-)
- `GET - api/v1/professor/courses/:id/exams/:id/questions/:id` - Show [Details](#show-exam-question-)
- `PATCH - api/v1/professor/courses/:id/exams/:id/questions/:id` - Update [Details](#update-exam-question-)
- `DELETE - api/v1/professor/courses/:id/exams/:id/questions/:id` - Delete [Details](#delete-exam-question-)

##### EXAM QUESTION ANSWERS ⭐

- `PATCH - api/v1/professor/courses/:id/exams/:id/questions/:id/answers/:id` - Update [Details](#update-exam-question-answer-)

#### ASSISTANT 👨‍🏫

##### ACCESS PERMISSOIN ⭐

- `GET - api/v1/assistant/:id` - Show [Details](#show-assistant-)
- `PATCH - api/v1/assistant/:id` - Update [Details](#update-assistant-)

##### COURSE ⭐

- `GET - api/v1/assistant/courses` - Index [Details](#index-courses-assistant-)
- `GET - api/v1/assistant/courses/:id` - Show [Details](#show-course-assistant-)

##### SECTION ⭐

- `POST - api/v1/assistant/courses/:id/sections` - Create [Details](#create-section-assistant-)
- `GET - api/v1/assistant/courses/:id/sections` - Index [Details](#index-sections-assistant-)
- `GET - api/v1/assistant/courses/:id/sections/:id` - Show [Details](#show-section-assistant-)
- `PATCH - api/v1/assistant/courses/:id/sections/:id` - Update [Details](#update-section-assistant-)
- `DELETE - api/v1/assistant/courses/:id/sections/:id` - Delete [Details](#delete-section-assistant-)

##### SECTION RESOURCES ⭐

- `POST - api/v1/assistant/courses/:id/sections/:id/resources` - Create [Details](#create-section-resource-assistant-)
- `GET - api/v1/assistant/courses/:id/sections/:id/resources` - Index [Details](#index-section-resources-assistant-)
- `GET - api/v1/assistant/courses/:id/sections/:id/resources/:id` - Show [Details](#show-section-resource-assistant-)
- `PATCH - api/v1/assistant/courses/:id/sections/:id/resources/:id` - Update [Details](#update-section-resource-assistant-)
- `DELETE - api/v1/assistant/courses/:id/sections/:id/resources/:id` - Delete [Details](#delete-section-resource-assistant-)

##### ATTENDANCE ( QR CODE & LOCATION ) ⭐

- `POST - api/v1/assistant/courses/:id/sections/:id/attendance` - Create [Details](#create-attendance-assistant-)
- `GET - api/v1/assistant/courses/:id/sections/:id/attendance/:id` - Show [Details](#show-attendance-assistant-)
- `GET - api/v1/assistant/courses/:id/sections/:id/attendance/:id/students` - Index Students [Details](#index-attendance-assistant-students-)
- `DELETE - api/v1/assistant/courses/:id/sections/:id/attendance/:id/students/:id` - Delete Student [Details](#delete-attendance-assistant-student-)

##### ASSIGNMENT ⭐

- `POST - api/v1/assistant/courses/:id/sections/:id/assignments` - Create [Details](#create-section-assignment-assistant-)
- `GET - api/v1/assistant/courses/:id/sections/:id/assignments` - Index [Details](#index-section-assignments-assistant-)
- `GET - api/v1/assistant/courses/:id/sections/:id/assignments/:id` - Show [Details](#show-section-assignment-assistant-)
- `PATCH - api/v1/assistant/courses/:id/sections/:id/assignments/:id` - Update [Details](#update-section-assignment-assistant-)
- `DELETE - api/v1/assistant/courses/:id/sections/:id/assignments/:id` - Delete [Details](#delete-section-assignment-assistant-)

##### ASSIGNMENT SUBMISSIONS ⭐

- `GET - api/v1/assistant/courses/:id/sections/:id/assignments/:id/submissions` - Index [Details](#index-section-assignment-submissions-assistant-)
- `GET - api/v1/assistant/courses/:id/sections/:id/assignments/:id/submissions/:id` - Show [Details](#show-section-assignment-submission-assistant-)

#### STUDENT 👨‍🎓

##### ACCESS PERMISSOIN ⭐

- `GET - api/v1/student/:id` - Show [Details](#show-student-)

##### COURSE ⭐

- `GET - api/v1/student/courses` - Index [Details](#index-courses-student-)
- `GET - api/v1/student/courses/:id` - Show [Details](#show-course-student-)
- `POST - api/v1/student/courses/:id/enroll` - Enroll [Details](#enroll-course-student-)

##### COURSE EXAM ⭐

- `GET - api/v1/student/courses/:id/exams` - Index [Details](#index-course-exams-student-)
- `POST - api/v1/student/courses/:id/exams/:id/enroll` - Enroll [Details](#enroll-course-exam-student-)
- `POST - api/v1/student/courses/:id/exams/:id/submit` - Submit [Details](#submit-course-exam-student-)

##### COURSE ASSIGNMENT ⭐

- `GET - api/v1/student/courses/:id/assignments` - Index [Details](#index-course-assignments-student-)
- `GET - api/v1/student/courses/:id/assignments/:id` - Show [Details](#show-course-assignments-student-)
- `POST - api/v1/student/courses/:id/assignments/:id/submit` - Submit [Details](#submit-course-assignment-student-)

##### COURSE ASSISTANTS ⭐

- `GET - api/v1/student/courses/:id/assistants` - Index [Details](#index-course-assistants-student-)

##### SECTION ⭐

- `GET - api/v1/student/courses/:id/assistants/:id/sections` - Index [Details](#index-sections-student-)
- `GET - api/v1/student/courses/:id/assistants/:id/sections/:id` - Show [Details](#show-section-student-)

##### SECTION RESOURCES ⭐

- `GET - api/v1/student/courses/:id/assistants/:id/sections/:id/resources` - Index [Details](#index-section-resources-student-)

##### SECTION ASSIGNMENT ⭐

- `GET - api/v1/student/courses/:id/assistants/:id/sections/:id/assignments` - Index [Details](#index-section-assignments-student-)
- `GET - api/v1/student/courses/:id/assistants/:id/sections/:id/assignments/:id` - Show [Details](#show-section-assignment-student-)
- `POST - api/v1/student/courses/:id/assistants/:id/sections/:id/assignments/:id/submit` - Submit [Details](#submit-section-assignment-student-)

##### SECTION ATTENDANCE ⭐

- `GET - api/v1/student/courses/:id/assistants/:id/sections/:id/attendance/:id` - Show [Details](#show-section-attendance-student-)
- `POST - api/v1/student/courses/:id/assistants/:id/sections/:id/attendance/:id/attend` - Attend [Details](#attend-section-attendance-student-)

##### LECTURE ⭐

- `GET - api/v1/student/courses/:id/lectures` - Index [Details](#index-lectures-student-)
- `GET - api/v1/student/courses/:id/lectures/:id` - Show [Details](#show-lecture-student-)

##### LECTURE RESOURCES ⭐

- `GET - api/v1/student/courses/:id/lectures/:id/resources` - Index [Details](#index-lecture-resources-student-)

##### LECTURE ATTENDANCE ⭐

- `GET - api/v1/student/courses/:id/lectures/:id/attendance/:id` - Show [Details](#show-lecture-attendance-student-)
- `POST - api/v1/student/courses/:id/lectures/:id/attendance/:id/attend` - Attend [Details](#attend-lecture-attendance-student-)

##### CONTACTS ⭐

- `GET - api/v1/contacts/:id` - Show [Details](#show-contact-)
- `PATCH - api/v1/contacts/:id` - Update [Details](#update-contact-)

##### STORAGE ⭐

- `POST - api/v1/storage/:id` - Upload [Details](#upload-storage-)
- `GET - api/v1/storage/:id` - Access [Details](#access-storage-)

### All Endpoints (in details) 📡

#### Authentication 🔐

##### Login 📥

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/auth/login`
- _Headers:_ `Content-Type: application/json`
- _Request Body:_

  ```json
  {
    "username": "username-UNIQUE", // MIN: 2 - MAX: 50
    "password": "Pass44#", // MIN: 5 - MAX: 50
    "role": "master" // OPTIONS - master, admin, user, student, assistant
  }
  ```

- _Success Response:_

  ```json
  {
    "status": "success",
    "message": "Master logged in successfully",
    "data": {
      "role": "master",
      "id": "642de3f48fcd08239f55f69a",
      "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8"
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    username: 'mohamed475',
    password: 'hodla475',
    role: 'master',
  });

  let response = await fetch('http://localhost:3000/api/v1/auth/login', {
    method: 'POST',
    body: bodyContent,
    headers: headersList,
  });

  let data = await response.text();
  console.log(data);
  ```

#### MASTER 🔑

##### UNIVERSITY ⭐

###### Index universities 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/master/universities`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`
  ```json
  {
    "status": "success",
    "message": "Universities retrieved successfully",
    "data": {
      "universitiesCount": 2,
      "universities": [
        {
          "_id": "642deaa976e91123782b7f16",
          "name": "alu",
          "city": "alexandria",
          "country": "egypt",
          "collages": [],
          "createdAt": "2023-04-05T21:39:53.253Z",
          "updatedAt": "2023-04-05T21:39:53.253Z",
          "id": "642deaa976e91123782b7f16"
        },
        {
          "_id": "642dea4b76e91123782b7f10",
          "name": "kfu",
          "city": "kafr elsheikh",
          "country": "egypt",
          "collages": [],
          "createdAt": "2023-04-05T21:38:19.512Z",
          "updatedAt": "2023-04-05T21:38:19.512Z",
          "id": "642dea4b76e91123782b7f10"
        }
      ]
    }
  }
  ```
- _Example - JS_:

  ```js
  let headersList = {
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MjkwOTYsImV4cCI6MTY4MzMyMTA5Nn0.I1OSJJ3RywdmodyvYvRu2bN-2tEwPWbEEyceFCYmTS0',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Create university 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/master/universities`
- _Headers:_ `Authorization`
- _Request Body:_

  ```json
  {
    "name": "ALU", // MIN: 2 - MAX: 50
    "city": "Alexandria", // MIN: 2 - MAX: 50
    "country": "egypt" // MIN: 2 - MAX: 50
  }
  ```

- _Success Response:_ `201`
  ```json
  {
    "status": "success",
    "message": "University created successfully",
    "data": {
      "university": {
        "id": "642df520c6fee003857cde93"
      }
    }
  }
  ```
- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MjkwOTYsImV4cCI6MTY4MzMyMTA5Nn0.I1OSJJ3RywdmodyvYvRu2bN-2tEwPWbEEyceFCYmTS0',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'ALU',
    city: 'Alexandria',
    country: 'Egypt',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show university 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/master/universities/:universityId`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`
  ```json
  {
    "status": "success",
    "message": "University retrieved successfully",
    "data": {
      "university": {
        "_id": "642deaa976e91123782b7f16",
        "name": "alu",
        "city": "alex",
        "country": "egypt",
        "collages": ["642deda276e91123782b7f94"],
        "createdAt": "2023-04-05T21:39:53.253Z",
        "updatedAt": "2023-04-05T21:56:24.813Z",
        "id": "642deaa976e91123782b7f16"
      }
    }
  }
  ```
- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MjkwOTYsImV4cCI6MTY4MzMyMTA5Nn0.I1OSJJ3RywdmodyvYvRu2bN-2tEwPWbEEyceFCYmTS0',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update university 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/master/universities/:universityId`
- _Headers:_ `Authorization`
- _Request Body:_

  ```json
  {
    "name": "ALU", // MIN: 2 - MAX: 50
    "city": "Alexandria", // MIN: 2 - MAX: 50
    "country": "egypt" // MIN: 2 - MAX: 50
  }
  ```

- _Success Response:_ `200`
  ```json
  {
    "status": "success",
    "message": "University updated successfully",
    "data": {
      "university": {
        "_id": "642deaa976e91123782b7f16",
        "name": "alu",
        "city": "alex",
        "country": "egypt",
        "collages": [],
        "createdAt": "2023-04-05T21:39:53.253Z",
        "updatedAt": "2023-04-05T21:41:25.137Z",
        "id": "642deaa976e91123782b7f16"
      }
    }
  }
  ```
- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MjkwOTYsImV4cCI6MTY4MzMyMTA5Nn0.I1OSJJ3RywdmodyvYvRu2bN-2tEwPWbEEyceFCYmTS0',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'alu',
    city: 'Alex',
    country: 'Egypt',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete university 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/master/universities/:universityId`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "University deleted successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MjkwOTYsImV4cCI6MTY4MzMyMTA5Nn0.I1OSJJ3RywdmodyvYvRu2bN-2tEwPWbEEyceFCYmTS0',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642df520c6fee003857cde93',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### COLLAGE TYPE ⭐

###### Create collage type 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/master/collage-types`
- _Headers:_ `Authorization`
- _Request Body:_

  ```json
  {
    "name": "Faculty of Engineering" // MIN: 2 - MAX: 50
  }
  ```

- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Collage type created successfully",
    "data": {
      "collageType": {
        "id": "642e33a399182e5e2d14ec47"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MjkwOTYsImV4cCI6MTY4MzMyMTA5Nn0.I1OSJJ3RywdmodyvYvRu2bN-2tEwPWbEEyceFCYmTS0',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'engineering',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/master/collage-types',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );
  let data = await response.text();
  console.log(data);
  ```

###### Index collage types 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/master/collage-types`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Collage types fetched successfully",
    "data": {
      "collageTypesCount": 3,
      "collageTypes": [
        {
          "_id": "642e33a399182e5e2d14ec47",
          "name": "engineering"
        },
        {
          "_id": "642debc776e91123782b7f38",
          "name": "engineering"
        },
        {
          "_id": "642deb9c76e91123782b7f35",
          "name": "computer science"
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MjkwOTYsImV4cCI6MTY4MzMyMTA5Nn0.I1OSJJ3RywdmodyvYvRu2bN-2tEwPWbEEyceFCYmTS0',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/collage-types',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show collage type 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/master/collage-types/:collageTypeId`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Collage type fetched successfully",
    "data": {
      "collageType": {
        "_id": "642debc776e91123782b7f38",
        "name": "engineering",
        "createdAt": "2023-04-05T21:44:39.114Z",
        "updatedAt": "2023-04-05T21:44:39.114Z",
        "__v": 0
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MjkwOTYsImV4cCI6MTY4MzMyMTA5Nn0.I1OSJJ3RywdmodyvYvRu2bN-2tEwPWbEEyceFCYmTS0',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/collage-types/642debc776e91123782b7f38',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update collage type 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/master/collage-types/:collageTypeId`
- _Headers:_ `Authorization`
- _Request Body:_

  ```json
  {
    "name": "Faculty of Engineering" // MIN: 2 - MAX: 50
  }
  ```

- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Collage type updated successfully",
    "data": {
      "collageType": {
        "_id": "642e33a399182e5e2d14ec47",
        "name": "type name",
        "createdAt": "2023-04-06T02:51:15.552Z",
        "updatedAt": "2023-04-06T03:11:29.284Z",
        "__v": 0
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MjkwOTYsImV4cCI6MTY4MzMyMTA5Nn0.I1OSJJ3RywdmodyvYvRu2bN-2tEwPWbEEyceFCYmTS0',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'testf',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/master/collage-types/642e33a399182e5e2d14ec47',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete collage type 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/master/collage-types/:collageTypeId`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Collage type removed successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MjkwOTYsImV4cCI6MTY4MzMyMTA5Nn0.I1OSJJ3RywdmodyvYvRu2bN-2tEwPWbEEyceFCYmTS0',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/collage-types/642e33a399182e5e2d14ec47',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### Collages ⭐

###### Create collage 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages`
- _Headers:_ `Authorization`
- _Request Body:_

  ```json
  {
    "name": "fuculty of engineering",
    "type": "642debc776e91123782b7f38"
  }
  ```

- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Collage created successfully",
    "data": {
      "collage": {
        "name": "fuculty of engineering",
        "university": "642deaa976e91123782b7f16",
        "levels": [],
        "type": "642debc776e91123782b7f38",
        "professors": [],
        "assistants": [],
        "_id": "642e3cb699182e5e2d14ec59",
        "createdAt": "2023-04-06T03:29:58.750Z",
        "updatedAt": "2023-04-06T03:29:58.750Z",
        "__v": 0,
        "id": "642e3cb699182e5e2d14ec59"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'fuculty of engineering',
    type: '642debc776e91123782b7f38',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index collages 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Collage fetched successfully",
    "data": {
      "collagesCount": 2,
      "collages": [
        {
          "_id": "642e3cb699182e5e2d14ec59",
          "name": "fuculty of engineering",
          "university": "642deaa976e91123782b7f16",
          "levels": [],
          "type": {
            "_id": "642debc776e91123782b7f38",
            "name": "engineering",
            "createdAt": "2023-04-05T21:44:39.114Z",
            "updatedAt": "2023-04-05T21:44:39.114Z",
            "__v": 0,
            "id": "642debc776e91123782b7f38"
          },
          "professors": [],
          "assistants": [],
          "createdAt": "2023-04-06T03:29:58.750Z",
          "updatedAt": "2023-04-06T03:29:58.750Z",
          "__v": 0,
          "id": "642e3cb699182e5e2d14ec59"
        },
        {
          "_id": "642deda276e91123782b7f94",
          "name": "fuculty of computer & information",
          "university": "642deaa976e91123782b7f16",
          "levels": ["642def5b76e91123782b7ff5"],
          "type": {
            "_id": "642deb9c76e91123782b7f35",
            "name": "computer science",
            "createdAt": "2023-04-05T21:43:56.305Z",
            "updatedAt": "2023-04-05T21:43:56.305Z",
            "__v": 0,
            "id": "642deb9c76e91123782b7f35"
          },
          "professors": ["642df3d32c8448c0a089af25"],
          "createdAt": "2023-04-05T21:52:34.815Z",
          "updatedAt": "2023-04-05T22:23:02.145Z",
          "__v": 6,
          "assistants": [],
          "id": "642deda276e91123782b7f94"
        }
      ],
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show collage 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Collage fetched successfully",
    "data": {
      "collage": {
        "_id": "642deda276e91123782b7f94",
        "name": "fuculty of computer & information",
        "university": "642deaa976e91123782b7f16",
        "levels": ["642def5b76e91123782b7ff5"],
        "type": {
          "_id": "642deb9c76e91123782b7f35",
          "name": "computer science",
          "createdAt": "2023-04-05T21:43:56.305Z",
          "updatedAt": "2023-04-05T21:43:56.305Z",
          "__v": 0,
          "id": "642deb9c76e91123782b7f35"
        },
        "professors": ["642df3d32c8448c0a089af25"],
        "assistants": [],
        "id": "642deda276e91123782b7f94"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642deda276e91123782b7f94',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update collage 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id`
- _Headers:_ `Authorization`
- _Request Body:_

  ```json
  {
    "name": "fuculty of computer & information",
    "type": "642deb9c76e91123782b7f35"
  }
  ```

- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Collage updated successfully",
    "data": {
      "updatedCollage": {
        "_id": "642deda276e91123782b7f94",
        "name": "fuculty of computer & information",
        "university": "642deaa976e91123782b7f16",
        "levels": ["642def5b76e91123782b7ff5"],
        "type": "642deb9c76e91123782b7f35",
        "professors": ["642df3d32c8448c0a089af25"],
        "createdAt": "2023-04-05T21:52:34.815Z",
        "updatedAt": "2023-04-05T22:23:02.145Z",
        "__v": 6,
        "assistants": [],
        "id": "642deda276e91123782b7f94"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'fuculty of computer & information',
    type: '642deb9c76e91123782b7f35',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642deda276e91123782b7f94',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete collage 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Collage removed successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642deda276e91123782b7f94',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### LEVEL ⭐

###### Create level 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id/levels`
- _Headers:_ `Authorization`
- _Request Body:_

  ```json
  {
    "name": "level 01"
  }
  ```

- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Level created successfully",
    "data": {
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'level 01',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index levels 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id/levels`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Levels fetched successfully",
    "data": {
      "levelsCount": 1,
      "levels": [
        {
          "_id": "642ee7f789a92ceeba6b7a4f",
          "name": "level 01",
          "programs": [],
          "collage": "642e3cb699182e5e2d14ec59",
          "university": "642deaa976e91123782b7f16",
          "admins": [],
          "createdAt": "2023-04-06T15:40:40.000Z",
          "updatedAt": "2023-04-06T15:40:40.000Z",
          "__v": 0,
          "id": "642ee7f789a92ceeba6b7a4f"
        }
      ],
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show level 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id/levels/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Level fetched successfully",
    "data": {
      "level": {
        "_id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01",
        "programs": [],
        "collage": "642e3cb699182e5e2d14ec59",
        "university": "642deaa976e91123782b7f16",
        "admins": [],
        "id": "642ee7f789a92ceeba6b7a4f"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update level 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id/levels/:id`
- _Headers:_ `Authorization`
- _Request Body:_

  ```json
  {
    "name": "level 01"
  }
  ```

- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Level updated successfully",
    "data": {
      "level": {
        "_id": "642eea412a5ae844ca7b8f6f",
        "name": "updated level",
        "programs": [],
        "collage": "642e3cb699182e5e2d14ec59",
        "university": "642deaa976e91123782b7f16",
        "admins": [],
        "createdAt": "2023-04-06T15:50:25.890Z",
        "updatedAt": "2023-04-06T15:50:33.105Z",
        "__v": 0,
        "id": "642eea412a5ae844ca7b8f6f"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'updated level',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642eea412a5ae844ca7b8f6f',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete level 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id/levels/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Level deleted successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642eea412a5ae844ca7b8f6f',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### ADMIN ⭐

###### Create admin 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id/levels/:id/admins`
- _Headers:_ `Authorization`
- _Request Body:_

  ```json
  {
    "name": "admin 02",
    "email": "admin02@mail.com", // UNIQUE
    "password": "adminpassword",
    "username": "uni-admin-02" // UNIQUE
  }
  ```

- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Admin created successfully",
    "data": {
      "admin": {
        "id": "642eed3c977ee3f83d97f332"
      },
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'admin 02',
    email: 'adminf02@mail.com',
    password: 'adminpassword',
    username: 'unfi-admin-02f',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/admins',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index admins 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id/levels/:id/admins`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Admins fetched successfully",
    "data": {
      "adminsCount": 2,
      "admins": [
        {
          "id": "642eed3c977ee3f83d97f332",
          "createdAt": "2023-04-06T16:03:08.499Z",
          "name": "admin 02"
        },
        {
          "id": "642eecde2a5ae844ca7b8f8a",
          "createdAt": "2023-04-06T16:01:34.509Z",
          "name": "admin 02"
        }
      ],
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/admins',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show admin 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id/levels/:id/admins/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Admin fetched successfully",
    "data": {
      "admin": {
        "id": "642eed3c977ee3f83d97f332",
        "createdAt": "2023-04-06T16:03:08.499Z",
        "name": "admin 02",
        "username": "unfi-admin-02f",
        "email": "adminf02@mail.com",
        "qrCode": "642eed3c977ee3f83d97f330"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/admins/642eed3c977ee3f83d97f332',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update admin 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id/levels/:id/admins/:id`
- _Headers:_ `Authorization`
- _Request Body:_

  ```json
  {
    "name": "admin updated name",
    "email": "newemail@gmail.com"
  }
  ```

- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Admin updated successfully",
    "data": {
      "admin": {
        "id": "642eed3c977ee3f83d97f332",
        "createdAt": "2023-04-06T16:03:08.499Z",
        "name": "admin updated name",
        "username": "unfi-admin-02f",
        "email": "newemail@gmail.com",
        "qrCode": "642eed3c977ee3f83d97f330"
      },
      "university": "alu",
      "collage": "fuculty of engineering",
      "level": "level 01"
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'admooosna-MASTER',
    email: 'dsf@gmail.com',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/admins/642eed3c977ee3f83d97f332',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete admin 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id/levels/:id/admins/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Admin deleted successfully  ",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/admins/642eed3c977ee3f83d97f332',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### PROFESSOR ⭐

###### Create professor 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id/professors`
- _Headers:_ `Authorization`
- _Request Body:_
  ```json
  {
    "name": "Mohamed Yasser",
    "password": "passCode96$",
    "username": "iammohamedyasser",
    "academicId": "120120120120"
  }
  ```
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Professor created successfully",
    "data": {
      "professor": {
        "id": "64304c1b3eea93f118839bff"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'Mohamed Yasser',
    password: 'ljslk',
    username: 'mov47f5',
    academicId: '120120120120',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/professors',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index professors 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id/professors`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Professors fetched successfully",
    "data": {
      "professorsCount": 1,
      "professors": [
        {
          "id": "64304c1b3eea93f118839bff",
          "createdAt": "2023-04-07T17:00:11.784Z",
          "name": "mohamed yasser",
          "academicId": "120120120120",
          "courses": []
        }
      ],
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/professors',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show professor 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id/professors/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Professor fetched successfully",
    "data": {
      "professor": {
        "id": "64304c1b3eea93f118839bff",
        "name": "mohamed yasser",
        "username": "mov47f5",
        "academicId": "120120120120",
        "qrCode": "64304c1b3eea93f118839bfb",
        "courses": [],
        "assistants": [],
        "contacts": "64304c1b3eea93f118839bfd"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/professors/64304c1b3eea93f118839bff',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update professor 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id/professors/:id`
- _Headers:_ `Authorization`
- _Request Body:_
  ```json
  {
    "name": "Dr. Ahmed Elashry",
    "academicId": "99999999999"
  }
  ```
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Professor updated successfully",
    "data": {
      "professor": {
        "id": "64304c1b3eea93f118839bff",
        "name": "Dr. Ahmed Elashry",
        "academicId": "99999999999"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'ali ali',
    academicId: '99999999999',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/professors/64304c1b3eea93f118839bff',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete professor 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/master/universities/:id/collages/:id/professors/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Professor deleted successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQyZGUzZjQ4ZmNkMDgyMzlmNTVmNjlhIiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2ODA3MzEyMjYsImV4cCI6MTY4MzMyMzIyNn0.WvDflGIDlExCao6mXYFjpEuD4dKpcfVd6sGxMeMo8F8',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/master/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/professors/64304c1b3eea93f118839bff',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

#### ADMIN 👔

##### PROGRAM ⭐

###### Create program 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/admin/universities/:id/collages/:id/levels/:id/programs`
- _Headers:_ `Authorization`
- _Request Body:_
  ```json
  {
    "name": "private", // [private, public]
    "tuitionFees": "1000",
    "currency": "EGP" // [EGP, USD, EUR]
  }
  ```
- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Program created successfully",
    "data": {
      "program": {
        "name": "private",
        "tuitionFees": {
          "value": 1000,
          "currency": "EGP"
        },
        "departments": [],
        "collage": "642e3cb699182e5e2d14ec59",
        "level": "642ee7f789a92ceeba6b7a4f",
        "university": "642deaa976e91123782b7f16",
        "_id": "643052c63eea93f118839c53",
        "createdAt": "2023-04-07T17:28:38.180Z",
        "updatedAt": "2023-04-07T17:28:38.180Z",
        "__v": 0,
        "id": "643052c63eea93f118839c53"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'private',
    tuitionFees: '1000',
    currency: 'EGP',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index programs 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/admin/universities/:id/collages/:id/levels/:id/programs`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Programs fetched successfully",
    "data": {
      "programsCount": 1,
      "programs": [
        {
          "tuitionFees": {
            "value": 1000,
            "currency": "EGP"
          },
          "_id": "643052a83eea93f118839c46",
          "name": "public",
          "departments": [],
          "collage": "642e3cb699182e5e2d14ec59",
          "level": "642ee7f789a92ceeba6b7a4f",
          "university": "642deaa976e91123782b7f16",
          "createdAt": "2023-04-07T17:28:08.091Z",
          "updatedAt": "2023-04-07T17:28:08.091Z",
          "__v": 0,
          "id": "643052a83eea93f118839c46"
        }
      ],
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show program 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Programs fetched successfully",
    "data": {
      "programsCount": 1,
      "programs": [
        {
          "tuitionFees": {
            "value": 1000,
            "currency": "EGP"
          },
          "_id": "643052a83eea93f118839c46",
          "name": "public",
          "departments": [],
          "collage": "642e3cb699182e5e2d14ec59",
          "level": "642ee7f789a92ceeba6b7a4f",
          "university": "642deaa976e91123782b7f16",
          "createdAt": "2023-04-07T17:28:08.091Z",
          "updatedAt": "2023-04-07T17:28:08.091Z",
          "__v": 0,
          "id": "643052a83eea93f118839c46"
        }
      ],
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052a83eea93f118839c46',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update program 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `name, tuitionFees`

  ```json
  {
    "name": "public", // [public, private]
    "tuitionFees": "900",
    "currency": "USD" // [USD, EGP, EUR]
  }
  ```

- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Program updated successfully",
    "data": {
      "program": {
        "id": "643052c63eea93f118839c53",
        "name": "public",
        "tuitionFees": {
          "value": 900,
          "currency": "USD"
        }
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'public',
    tuitionFees: '900',
    currency: 'USD',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052c63eea93f118839c53',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete program 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Program deleted successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052c63eea93f118839c53',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

- `POST - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments` - Create [Details](#create-department-)
- `GET - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments` - Index [Details](#index-departments-)
- `GET - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id` - Show [Details](#show-department-)
- `PATCH - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id` - Update [Details](#update-department-)
- `DELETE - api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id` - Delete [Details](#delete-department-)

##### DEPARTMENT ⭐

###### Create department 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments`
- _Headers:_ `Authorization`
- _Request Body:_ `name`

  ```json
  {
    "name": "computer science",
    "extraTuitionFees": "1000",
    "currency": "USD" // [USD, EGP, EUR]
  }
  ```

- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Department created successfully",
    "data": {
      "department": {
        "id": "64305ac8ee3e783bbc680624"
      },
      "program": {
        "id": "643052a83eea93f118839c46",
        "name": "public"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'computer science',
    extraTuitionFees: '1000',
    currency: 'egp',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052a83eea93f118839c46/departments',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index departments 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Departments fetched successfully",
    "data": {
      "departmentsCount": 1,
      "departments": [
        {
          "extraTuitionFees": {
            "value": 1000,
            "currency": "EGP"
          },
          "_id": "6430596c112031c1dbfc3fd8",
          "name": "computer science",
          "courses": [],
          "program": "643052a83eea93f118839c46",
          "level": "642ee7f789a92ceeba6b7a4f",
          "collage": "642e3cb699182e5e2d14ec59",
          "university": "642deaa976e91123782b7f16",
          "students": [],
          "createdAt": "2023-04-07T17:57:00.104Z",
          "updatedAt": "2023-04-07T17:57:00.104Z",
          "__v": 0,
          "id": "6430596c112031c1dbfc3fd8"
        }
      ],
      "program": {
        "id": "643052a83eea93f118839c46",
        "name": "public"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052a83eea93f118839c46/departments',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show department 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Department fetched successfully",
    "data": {
      "department": {
        "extraTuitionFees": {
          "value": 1000,
          "currency": "EGP"
        },
        "_id": "6430596c112031c1dbfc3fd8",
        "name": "computer science",
        "courses": [],
        "program": "643052a83eea93f118839c46",
        "level": "642ee7f789a92ceeba6b7a4f",
        "collage": "642e3cb699182e5e2d14ec59",
        "university": "642deaa976e91123782b7f16",
        "students": [],
        "createdAt": "2023-04-07T17:57:00.104Z",
        "updatedAt": "2023-04-07T17:57:00.104Z",
        "__v": 0,
        "id": "6430596c112031c1dbfc3fd8"
      },
      "program": {
        "id": "643052a83eea93f118839c46",
        "name": "public"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052a83eea93f118839c46/departments/6430596c112031c1dbfc3fd8',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update department 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `name`, `extraTuitionFees`

  ```json
  {
    "name": "Information System",
    "extraTuitionFees": "100000",
    "currency": "EUR" // [EGP, USD, EUR]
  }
  ```

- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Department updated successfully",
    "data": {
      "department": {
        "id": "643059a6112031c1dbfc3fed",
        "name": "se",
        "extraTuitionFees": {
          "value": 100000,
          "currency": "EUR"
        }
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'Information System',
    extraTuitionFees: '100000',
    currency: 'EUR',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052a83eea93f118839c46/departments/643059a6112031c1dbfc3fed',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete department 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`

- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Department deleted successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052a83eea93f118839c46/departments/64305ac8ee3e783bbc680624',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### Student ⭐

###### Create student 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id/students`
- _Headers:_ `Authorization`
- _Request Body:_

  ```json
  {
    "name": "Mohamed Yasser",
    "password": "passCodee75&",
    "username": "mohamedyasser459f",
    "academicId": "9879873833"
  }
  ```

- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Student created successfully",
    "data": {
      "student": {
        "id": "6430629f9cd224306d04b332"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01"
      },
      "program": {
        "id": "643052a83eea93f118839c46",
        "name": "public"
      },
      "department": {
        "id": "6430596c112031c1dbfc3fd8",
        "name": "computer science"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'Mohamed Yasser',
    password: 'passCodee75&',
    username: 'mohamedyasser459f',
    academicId: '9879873833',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052a83eea93f118839c46/departments/6430596c112031c1dbfc3fd8/students',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index students 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id/students`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Students fetched successfully",
    "data": {
      "studentsCount": 1,
      "students": [
        {
          "id": "643061a4ee3e783bbc680640",
          "createdAt": "2023-04-07T18:32:04.111Z",
          "name": "mohamed yasser",
          "academicId": "9879873833",
          "courses": []
        }
      ],
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01"
      },
      "program": {
        "id": "643052a83eea93f118839c46",
        "name": "public"
      },
      "department": {
        "id": "6430596c112031c1dbfc3fd8",
        "name": "computer science"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052a83eea93f118839c46/departments/6430596c112031c1dbfc3fd8/students',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id/students/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Student fetched successfully",
    "data": {
      "student": {
        "id": "643061a4ee3e783bbc680640",
        "createdAt": "2023-04-07T18:32:04.111Z",
        "name": "mohamed yasser",
        "academicId": "9879873833",
        "courses": [],
        "qrCode": "643061a3ee3e783bbc68063c"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01"
      },
      "program": {
        "id": "643052a83eea93f118839c46",
        "name": "public"
      },
      "department": {
        "id": "6430596c112031c1dbfc3fd8",
        "name": "computer science"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052a83eea93f118839c46/departments/6430596c112031c1dbfc3fd8/students/643061a4ee3e783bbc680640',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update student 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id/students/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `name`, `academicId`

  ```json
  {
    "name": "mohamed yasser",
    "academicId": "9879873833"
  }
  ```

- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Student updated successfully",
    "data": {
      "student": {
        "id": "6430629f9cd224306d04b332",
        "name": "mohamed yasser",
        "academicId": "9879873833"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: '999',
    academicId: '999999999',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052a83eea93f118839c46/departments/6430596c112031c1dbfc3fd8/students/6430629f9cd224306d04b332',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete student 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/admin/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id/students/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Student deleted successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052a83eea93f118839c46/departments/6430596c112031c1dbfc3fd8/students/6430629f9cd224306d04b332',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### QUICK ACCESS ⭐

###### Show admin level 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/admin/:id/levels/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Admin level fetched successfully",
    "data": {
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01",
        "programs": ["643052a83eea93f118839c46"]
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/643052073eea93f118839c3e/levels/642ee7f789a92ceeba6b7a4f',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### ACCESS PERMISSOIN ⭐

###### Show admin 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/admin/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Admin fetched successfully",
    "data": {
      "admin": {
        "id": "643052073eea93f118839c3e",
        "createdAt": "2023-04-07T17:25:27.277Z",
        "name": "admin 02",
        "username": "unfi-admin-02f",
        "email": "adminf02@mail.com",
        "qrCode": "643052073eea93f118839c3c"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/643052073eea93f118839c3e',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update admin 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/admin/:id`
- _Headers:_ `Authorization`
- _Request Body:_
  ```json
  {
    "name": "Mohamed Yasser",
    "email": "unista-ali@gmail.com"
  }
  ```
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Admin updated successfully",
    "data": {
      "admin": {
        "id": "643052073eea93f118839c3e",
        "name": "mohamed yasser",
        "email": "unista-ali@gmail.com"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMDUyMDczZWVhOTNmMTE4ODM5YzNlIiwicm9sZSI6ImFkbWluIn0sImlhdCI6MTY4MDg4ODM1NywiZXhwIjoxNjgzNDgwMzU3fQ.q2ECpclT0R9BoCeVq4korwQxVpS0D3E5AvFeH2y7kYo',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'Mohamed Yasser',
    email: 'unista-ali@gmail.com',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/admin/643052073eea93f118839c3e',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

#### PROFESSOR 👨‍🏫

- `GET - api/v1/professor/:id` - Show [Details](#show-professor-)
- `PATCH - api/v1/professor/:id` - Update [Details](#update-professor-)

##### ACCESS PERMISSOIN ⭐

###### Show professor 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/:id`
- _Headers:_ `Authorization`
- _Request Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Professor fetched successfully",
    "data": {
      "professor": {
        "id": "6430c7854e29a1ff8375d1e7",
        "createdAt": "2023-04-08T01:46:45.356Z",
        "name": "mohamed yasser",
        "username": "mov47f5",
        "academicId": "120120120120",
        "qrCode": "6430c7854e29a1ff8375d1e3",
        "courses": [],
        "contacts": "6430c7854e29a1ff8375d1e5"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/6430c7854e29a1ff8375d1e7',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update professor 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/professor/:id`
- _Headers:_ `Authorization`
- _Request Body:_
  ```json
  {
    "name": "Dr. Mohamed Yasser",
    "academicId": "4354353453453"
  }
  ```
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Professor updated successfully",
    "data": {
      "professor": {
        "id": "6430c7854e29a1ff8375d1e7",
        "name": "dr. mohamed yasser",
        "academicId": "4354353453453"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'Dr. Mohamed Yasser',
    academicId: '4354353453453',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/6430c7854e29a1ff8375d1e7',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### COURSE ⭐

###### Create course 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/professor/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id/courses`
- _Headers:_ `Authorization`
- _Request Body:_
  ```json
  {
    "name": "Machine Learning",
    "code": "CS45",
    "semester": "first" // [first, second, summer]
  }
  ```
- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Course created successfully",
    "data": {
      "course": {
        "id": "6430cc574e29a1ff8375d202"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'machine learning',
    code: 'CS45',
    semester: 'first',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052a83eea93f118839c46/departments/6430596c112031c1dbfc3fd8/courses',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete course 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/professor/universities/:id/collages/:id/levels/:id/programs/:id/departments/:id/courses/:id`
- _Headers:_ `Authorization`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Course deleted successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052a83eea93f118839c46/departments/6430596c112031c1dbfc3fd8/courses/6430cc574e29a1ff8375d202',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index courses 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses`
- _Headers:_ `Authorization`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Courses fetched successfully",
    "data": {
      "coursesCount": 1,
      "courses": [
        {
          "_id": "6430ce43c3ca49b01012f8ca",
          "name": "machine learning",
          "code": "cs45",
          "semester": "first",
          "professor": "6430c7854e29a1ff8375d1e7",
          "assistants": [],
          "students": [],
          "lectures": [],
          "sections": [],
          "assignments": [],
          "exams": [],
          "department": "6430596c112031c1dbfc3fd8",
          "program": "643052a83eea93f118839c46",
          "level": "642ee7f789a92ceeba6b7a4f",
          "collage": "642e3cb699182e5e2d14ec59",
          "university": "642deaa976e91123782b7f16",
          "createdAt": "2023-04-08T02:15:31.406Z",
          "updatedAt": "2023-04-08T02:15:31.406Z",
          "__v": 0,
          "id": "6430ce43c3ca49b01012f8ca"
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch('http://localhost:3000/api/v1/professor/courses', {
    method: 'GET',
    headers: headersList,
  });

  let data = await response.text();
  console.log(data);
  ```

###### Show course 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id`
- _Headers:_ `Authorization`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Course fetched successfully",
    "data": {
      "course": {
        "_id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning",
        "code": "cs45",
        "semester": "first",
        "professor": {
          "_id": "6430c7854e29a1ff8375d1e7",
          "name": "dr. mohamed yasser"
        },
        "assistants": [],
        "students": [],
        "lectures": [],
        "sections": [],
        "assignments": [],
        "exams": [],
        "department": {
          "_id": "6430596c112031c1dbfc3fd8",
          "name": "computer science"
        },
        "program": {
          "_id": "643052a83eea93f118839c46",
          "name": "public"
        },
        "level": {
          "_id": "642ee7f789a92ceeba6b7a4f",
          "name": "level 01"
        },
        "collage": {
          "_id": "642e3cb699182e5e2d14ec59",
          "name": "fuculty of engineering"
        },
        "university": {
          "_id": "642deaa976e91123782b7f16",
          "name": "alu"
        },
        "createdAt": "2023-04-08T02:15:31.406Z",
        "updatedAt": "2023-04-08T02:15:31.406Z",
        "__v": 0
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update course 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/professor/courses/:id`
- _Headers:_ `Authorization`
- _Body:_
  ```json
  {
    "name": "updated",
    "code": "SE99",
    "semester": "second"
  }
  ```
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Course updated successfully",
    "data": {
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning",
        "code": "cs45",
        "semester": "first"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'machine learning',
    code: 'CS45',
    semester: 'first',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### EBOOK ⭐

###### Create ebook 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/professor/courses/:id/ebook`
- _Headers:_ `Authorization`
- _Body:_
  ```json
  {
    "name": "Machine Learning Course Ebook" // File should be of type pdf
  }
  ```
- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Upload successful",
    "data": {
      "eBook": {
        "path": "courses/6430ce43c3ca49b01012f8ca/eBook/e1116f01-6e04-4fb8-8f3a-c2e50ba19752.pdf",
        "type": "application/pdf",
        "name": "Machine Learning Course Ebook",
        "owner": "6430c7854e29a1ff8375d1e7",
        "_id": "6430d28595394133234b0ca5",
        "createdAt": "2023-04-08T02:33:41.785Z",
        "updatedAt": "2023-04-08T02:33:41.785Z",
        "__v": 0,
        "id": "6430d28595394133234b0ca5"
      },
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'Machine Learning Course Ebook',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/ebook',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show ebook 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/ebook/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "EBook found",
    "data": {
      "eBook": {
        "_id": "6430d28595394133234b0ca5",
        "path": "courses/6430ce43c3ca49b01012f8ca/eBook/e1116f01-6e04-4fb8-8f3a-c2e50ba19752.pdf",
        "type": "application/pdf",
        "name": "Machine Learning Course Ebook",
        "owner": "6430c7854e29a1ff8375d1e7",
        "createdAt": "2023-04-08T02:33:41.785Z",
        "updatedAt": "2023-04-08T02:33:41.785Z",
        "__v": 0,
        "id": "6430d28595394133234b0ca5"
      },
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/ebook/6430d28595394133234b0ca5',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update ebook 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/professor/courses/:id/ebook/:id`
- _Headers:_ `Authorization`
- _Body:_
  ```json
  {
    "name": "Machine Learning Course Ebook Updated"
  }
  ```
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "eBook updated",
    "data": {
      "eBook": {
        "_id": "6430d28595394133234b0ca5",
        "path": "courses/6430ce43c3ca49b01012f8ca/eBook/e1116f01-6e04-4fb8-8f3a-c2e50ba19752.pdf",
        "type": "application/pdf",
        "name": "Machine Learning Course Ebook Updated",
        "owner": "6430c7854e29a1ff8375d1e7",
        "createdAt": "2023-04-08T02:33:41.785Z",
        "updatedAt": "2023-04-08T02:43:30.478Z",
        "__v": 0,
        "id": "6430d28595394133234b0ca5"
      },
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'Machine Learning Course Ebook Updated',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/ebook/6430d28595394133234b0ca5',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete ebook 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/professor/courses/:id/ebook/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "eBook deleted",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/ebook/6430d28595394133234b0ca5',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### ASSISTANT ⭐

###### Create assistant 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/professor/universities/:id/collages/:id/courses/:id/assistants`
- _Headers:_ `Authorization`
- _Body:_

  ```json
  {
    "name": "Mohamed Yasser",
    "academicId": "9887593780045",
    "username": "mohamed-user-09",
    "password": "passCode090"
  }
  ```

- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Assistant created successfully",
    "data": {
      "assistant": {
        "id": "6430e04795394133234b0ccd"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "professor": {
        "id": "6430c7854e29a1ff8375d1e7",
        "name": "dr. mohamed yasser"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'Mohamed Yasser',
    academicId: '9887593780045',
    username: 'mohamed-user-09',
    password: 'passCode090',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/courses/6430ce43c3ca49b01012f8ca/assistants',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Attach assistant 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/professor/universities/:id/collages/:id/courses/:id/assistants/:id/attach`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assistant attached successfully",
    "data": {
      "assistant": {
        "id": "6430e04795394133234b0ccd",
        "courses": ["6430ce43c3ca49b01012f8ca", "6430e37e95394133234b0cdf"]
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "professor": {
        "id": "6430c7854e29a1ff8375d1e7",
        "name": "dr. mohamed yasser"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/courses/6430e37e95394133234b0cdf/assistants/6430e04795394133234b0ccd/attach',
    {
      method: 'POST',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update assistant 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/professor/universities/:id/collages/:id/courses/:id/assistants/:id`
- _Headers:_ `Authorization`
- _Body:_

  ```json
  {
    "name": "Mohamed Yasser",
    "academicId": "9887593780045"
  }
  ```

- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assistant updated successfully",
    "data": {
      "assistant": {
        "id": "6430e04795394133234b0ccd",
        "name": "mohamed yasser",
        "academicId": "9887593780045"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'Mohamed Yasser',
    academicId: '9887593780045',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/courses/6430ce43c3ca49b01012f8ca/assistants/6430e04795394133234b0ccd',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show assistant 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/universities/:id/collages/:id/courses/:id/assistants/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assistant fetched successfully",
    "data": {
      "assistant": {
        "id": "6430e04795394133234b0ccd",
        "name": "mohamed yasser",
        "academicId": "9887593780045",
        "username": "mohamed-user-09",
        "qrCode": "6430e04795394133234b0ccb",
        "courses": ["6430ce43c3ca49b01012f8ca", "6430e37e95394133234b0cdf"],
        "createdBy": "6430c7854e29a1ff8375d1e7",
        "contacts": "6430e04795394133234b0ccc"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "professor": {
        "id": "6430c7854e29a1ff8375d1e7",
        "name": "dr. mohamed yasser"
      },
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/courses/6430ce43c3ca49b01012f8ca/assistants/6430e04795394133234b0ccd',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete assistant 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/professor/universities/:id/collages/:id/courses/:id/assistants/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assistant deleted successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/courses/6430ce43c3ca49b01012f8ca/assistants/6430e04795394133234b0ccd',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index assistants by course 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/universities/:id/collages/:id/courses/:id/assistants`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assistants fetched successfully",
    "data": {
      "assistantsCount": 1,
      "assistants": [
        {
          "id": "6430ed28e0848ccfef40807a",
          "name": "mohamed yasser",
          "academicId": "9887593780045",
          "courses": ["6430ce43c3ca49b01012f8ca"],
          "createdBy": "6430c7854e29a1ff8375d1e7"
        }
      ],
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/courses/6430ce43c3ca49b01012f8ca/assistants',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index assistants by collage 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/universities/:id/collages/:id/assistants`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assistants fetched successfully",
    "data": {
      "assistants": [
        {
          "id": "6430ed28e0848ccfef40807a",
          "name": "mohamed yasser",
          "academicId": "9887593780045",
          "courses": ["6430ce43c3ca49b01012f8ca"]
        }
      ],
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/assistants',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### LECTURE ⭐

###### Create lecture 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/professor/courses/:id/lectures`
- _Headers:_ `Authorization`
- _Body:_

  ```json
  {
    "name": "Lecture 01",
    "number": 1
  }
  ```

- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Lecture created successfully",
    "data": {
      "lecture": {
        "id": "6431e66759a6e5eec1297319"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'Lecture 01',
    number: 1,
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/lectures',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index lectures 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/lectures`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Lectures fetched successfully",
    "data": {
      "lecturesCount": 1,
      "lectures": [
        {
          "id": "6431e66759a6e5eec1297319",
          "_id": "6431e66759a6e5eec1297319",
          "name": "lecture 01",
          "number": 1,
          "resources": [],
          "course": "6430ce43c3ca49b01012f8ca",
          "professor": "6430c7854e29a1ff8375d1e7",
          "createdAt": "2023-04-08T22:10:47.415Z",
          "updatedAt": "2023-04-08T22:10:47.415Z",
          "__v": 0
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/lectures',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show lecture 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/lectures/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Lecture found",
    "data": {
      "lecture": {
        "_id": "6431e66759a6e5eec1297319",
        "name": "lecture 01",
        "number": 1,
        "resources": [],
        "course": "6430ce43c3ca49b01012f8ca",
        "professor": "6430c7854e29a1ff8375d1e7",
        "createdAt": "2023-04-08T22:10:47.415Z",
        "updatedAt": "2023-04-08T22:10:47.415Z",
        "__v": 0,
        "id": "6431e66759a6e5eec1297319"
      },
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/lectures/6431e66759a6e5eec1297319',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update lecture 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/professor/courses/:id/lectures/:id`
- _Headers:_ `Authorization`
- _Body:_
  ```json
  {
    "name": "Lecture 03",
    "number": 3
  }
  ```
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Lecture updated successfully",
    "data": {
      "lecture": {
        "id": "6431e66759a6e5eec1297319",
        "name": "lecture 03",
        "number": 3
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'Lecture 03',
    number: 3,
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/lectures/6431e66759a6e5eec1297319',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete lecture 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/professor/courses/:id/lectures/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Lecture deleted successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/lectures/6431e66759a6e5eec1297319',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

- `POST - api/v1/professor/courses/:id/lectures/:id/resources` - Create [Details](#create-lecture-resource-)
- `GET - api/v1/professor/courses/:id/lectures/:id/resources` - Index [Details](#index-lecture-resources-)
- `GET - api/v1/professor/courses/:id/lectures/:id/resources/:id` - Show [Details](#show-lecture-resource-)
- `PATCH - api/v1/professor/courses/:id/lectures/:id/resources/:id` - Update [Details](#update-lecture-resource-)
- `DELETE - api/v1/professor/courses/:id/lectures/:id/resources/:id` - Delete [Details](#delete-lecture-resource-)

##### LECTURE RESOURCE ⭐

###### Create lecture resource 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/professor/courses/:id/lectures/:id/resources`
- _Headers:_ `Authorization`
- _Body:_

  ```json
  {
    "name": "lecture 01 - resource",
    "type": "png" // Allowed types // allowed types without mime type [jpeg, png, pdf, doc, xls, docx, xlsx, pptx, mp3, mp4]
  }
  ```

- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Lecture resource created",
    "data": {
      "storage": {
        "path": "courses/6430ce43c3ca49b01012f8ca/lecture/64322cf88becbaa1fe44e152/resources/69a736e6-a1d8-4595-8053-c5740b955ca9.png",
        "type": "image/png",
        "name": "lecture 01 - resource",
        "owner": "6430c7854e29a1ff8375d1e7",
        "_id": "64322db139cfdf68bb8fe285",
        "createdAt": "2023-04-09T03:14:57.404Z",
        "updatedAt": "2023-04-09T03:14:57.404Z",
        "__v": 0,
        "id": "64322db139cfdf68bb8fe285"
      },
      "lecture": {
        "_id": "64322cf88becbaa1fe44e152",
        "name": "lecture 01",
        "number": 1,
        "resources": ["64322db139cfdf68bb8fe285"],
        "course": "6430ce43c3ca49b01012f8ca",
        "professor": "6430c7854e29a1ff8375d1e7",
        "createdAt": "2023-04-09T03:11:52.100Z",
        "updatedAt": "2023-04-09T03:14:57.522Z",
        "__v": 1,
        "id": "64322cf88becbaa1fe44e152"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'lecture 01 - resource',
    type: 'png',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/lectures/64322cf88becbaa1fe44e152/resources',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index lecture resources 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/lectures/:id/resources`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Resources fetched successfully",
    "data": {
      "resources": [
        {
          "_id": "64322db139cfdf68bb8fe285",
          "type": "image/png",
          "name": "lecture 01 - resource",
          "id": "64322db139cfdf68bb8fe285"
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/lectures/64322cf88becbaa1fe44e152/resources',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show lecture resource 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/lectures/:id/resources/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Resource fetched successfully",
    "data": {
      "resource": {
        "_id": "64322db139cfdf68bb8fe285",
        "path": "courses/6430ce43c3ca49b01012f8ca/lecture/64322cf88becbaa1fe44e152/resources/69a736e6-a1d8-4595-8053-c5740b955ca9.png",
        "type": "image/png",
        "name": "new resource name",
        "owner": "6430c7854e29a1ff8375d1e7",
        "createdAt": "2023-04-09T03:14:57.404Z",
        "updatedAt": "2023-04-09T03:18:33.343Z",
        "__v": 0,
        "id": "64322db139cfdf68bb8fe285"
      },
      "lecture": {
        "id": "64322cf88becbaa1fe44e152",
        "name": "lecture 01"
      },
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/lectures/64322cf88becbaa1fe44e152/resources/64322db139cfdf68bb8fe285',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update lecture resource 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/professor/courses/:id/lectures/:id/resources/:id`
- _Headers:_ `Authorization`
- _Body:_ `name`

  ```json
  {
    "name": "new resource name"
  }
  ```

- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Resource updated successfully",
    "data": {
      "resource": {
        "_id": "64322db139cfdf68bb8fe285",
        "path": "courses/6430ce43c3ca49b01012f8ca/lecture/64322cf88becbaa1fe44e152/resources/69a736e6-a1d8-4595-8053-c5740b955ca9.png",
        "type": "image/png",
        "name": "new resource name",
        "owner": "6430c7854e29a1ff8375d1e7",
        "createdAt": "2023-04-09T03:14:57.404Z",
        "updatedAt": "2023-04-09T03:18:33.343Z",
        "__v": 0,
        "id": "64322db139cfdf68bb8fe285"
      },
      "lecture": {
        "id": "64322cf88becbaa1fe44e152",
        "name": "lecture 01"
      },
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'new resource name',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/lectures/64322cf88becbaa1fe44e152/resources/64322db139cfdf68bb8fe285',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete lecture resource 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/professor/courses/:id/lectures/:id/resources/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Resource removed successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/lectures/64322cf88becbaa1fe44e152/resources/64322db139cfdf68bb8fe285',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### QUICK Index ⭐

###### Index levels professor 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/universities/:id/collages/:id/levels`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Levels fetched successfully",
    "data": {
      "levels": [
        {
          "id": "642ee7f789a92ceeba6b7a4f",
          "name": "level 01"
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index programs professor 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/universities/:id/collages/:id/levels/:id/programs`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Programs fetched successfully",
    "data": {
      "programs": [
        {
          "id": "643052a83eea93f118839c46",
          "name": "public"
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index departments professor 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/universities/:id/collages/:id/levels/:id/programs/:id/departments`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Departments fetched successfully",
    "data": {
      "departments": [
        {
          "id": "6430596c112031c1dbfc3fd8",
          "name": "computer science"
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/universities/642deaa976e91123782b7f16/collages/642e3cb699182e5e2d14ec59/levels/642ee7f789a92ceeba6b7a4f/programs/643052a83eea93f118839c46/departments',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### ATTENDANCE ⭐

###### Create attendance 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/professor/courses/:id/lectures/:id/attendance`
- _Headers:_ `Authorization`
- _Body:_

  ```json
  {
    "distanceInMeters": 100,
    "durationInMinutes": 2,
    "lat": "30.9977",
    "lng": "29.7432"
  }
  ```

- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Attendance created successfully.",
    "data": {
      "attendance": {
        "students": [],
        "lecture": "64322cf88becbaa1fe44e152",
        "distanceInMeters": 100,
        "creatorCoordinates": {
          "lat": "30.9977",
          "lng": "29.7432"
        },
        "durationInMinutes": 2,
        "expiredAt": "2023-04-09T15:16:39.557Z",
        "randomAccessKey": "W0oGmjIXsW",
        "_id": "6432d65f19c58a344497f49c",
        "createdAt": "2023-04-09T15:14:39.571Z",
        "updatedAt": "2023-04-09T15:14:39.571Z",
        "__v": 0,
        "id": "6432d65f19c58a344497f49c"
      },
      "lecture": {
        "id": "64322cf88becbaa1fe44e152",
        "name": "lecture 01"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    distanceInMeters: 100,
    durationInMinutes: 2,
    lat: '30.9977',
    lng: '29.7432',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/lectures/64322cf88becbaa1fe44e152/attendance',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show attendance 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/lectures/:id/attendance/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Attendance fetched successfully",
    "data": {
      "attendance": {
        "creatorCoordinates": {
          "lat": "30.9977",
          "lng": "29.7432"
        },
        "_id": "6432d88c19c58a344497f4ba",
        "students": [],
        "lecture": "6432d85e19c58a344497f4b4",
        "distanceInMeters": 100,
        "durationInMinutes": 2,
        "expiredAt": "2023-04-09T15:25:56.657Z",
        "randomAccessKey": "yUvrasLv20",
        "createdAt": "2023-04-09T15:23:56.658Z",
        "updatedAt": "2023-04-09T15:23:56.658Z",
        "__v": 0,
        "id": "6432d88c19c58a344497f4ba"
      },
      "isExpired": true
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/lectures/6432d85e19c58a344497f4b4/attendance/6432d88c19c58a344497f4ba',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index attendance students 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/lectures/:id/attendance/:id/students`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Students fetched successfully",
    "data": {
      "students": [],
      "isExpired": true
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/lectures/6432d85e19c58a344497f4b4/attendance/6432d88c19c58a344497f4ba/students',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete attendance student 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/professor/courses/:id/lectures/:id/attendance/:id/students/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Student removed successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/lectures/6432d85e19c58a344497f4b4/attendance/6432d88c19c58a344497f4ba/students/6432d85e19c58a344497f4b4',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### COURSE ASSIGNMENT ⭐

###### Create course assignment 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/professor/courses/:id/assignments`
- _Headers:_ `Authorization`
- _Body:_

  ```json
  {
    "title": "Python CGI",
    "contentText": "In this assignment you should create a full python server side application and apply all CGI concepts we have learned in the lecture and section",
    "dueToDays": 7
  }
  ```

- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Assignment created",
    "data": {
      "assignment": {
        "id": "6432dd2ddde93cf76c5dadc8"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    title: 'Python CGI',
    contentText:
      'In this assignment you should create a full python server side application and apply all CGI concepts we have learned in the lecture and section',
    dueToDays: 7,
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/assignments',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index course assignments 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/assignments`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assignments fetched successfully",
    "data": {
      "assignmentsCount": 1,
      "assignments": [
        {
          "id": "6432dd2ddde93cf76c5dadc8",
          "_id": "6432dd2ddde93cf76c5dadc8",
          "title": "python cgi",
          "contentText": "In this assignment you should create a full python server side application and apply all CGI concepts we have learned in the lecture and section",
          "contentImage": "6432dd2ddde93cf76c5dadc7",
          "dueDate": "2023-04-16T15:43:41.808Z",
          "professor": "6430c7854e29a1ff8375d1e7",
          "course": "6430ce43c3ca49b01012f8ca",
          "submissions": [],
          "createdAt": "2023-04-09T15:43:42.052Z",
          "updatedAt": "2023-04-09T15:43:42.052Z",
          "__v": 0
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/assignments',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show course assignment 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/assignments/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assignments fetched successfully",
    "data": {
      "assignmentsCount": 1,
      "assignments": [
        {
          "id": "6432dd2ddde93cf76c5dadc8",
          "_id": "6432dd2ddde93cf76c5dadc8",
          "title": "python cgi",
          "contentText": "In this assignment you should create a full python server side application and apply all CGI concepts we have learned in the lecture and section",
          "contentImage": "6432dd2ddde93cf76c5dadc7",
          "dueDate": "2023-04-16T15:43:41.808Z",
          "professor": "6430c7854e29a1ff8375d1e7",
          "course": "6430ce43c3ca49b01012f8ca",
          "submissions": [],
          "createdAt": "2023-04-09T15:43:42.052Z",
          "updatedAt": "2023-04-09T15:43:42.052Z",
          "__v": 0
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/assignments/6432dd2ddde93cf76c5dadc8',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update course assignment 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/professor/courses/:id/assignments/:id`
- _Headers:_ `Authorization`
- _Body:_
  ```json
  {
    "title": "New title",
    "contentText": "New content text",
    "dueToDays": 10
  }
  ```
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "The assignment updated successfully",
    "data": {
      "assignment": {
        "_id": "6432dd2ddde93cf76c5dadc8",
        "title": "new title",
        "contentText": "New content text",
        "contentImage": "6432dd2ddde93cf76c5dadc7",
        "dueDate": "2023-04-19T15:52:40.136Z",
        "professor": "6430c7854e29a1ff8375d1e7",
        "course": "6430ce43c3ca49b01012f8ca",
        "submissions": [],
        "createdAt": "2023-04-09T15:43:42.052Z",
        "updatedAt": "2023-04-09T15:52:40.249Z",
        "__v": 0,
        "id": "6432dd2ddde93cf76c5dadc8"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    title: 'New title',
    contentText: 'New content text',
    dueToDays: 10,
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/assignments/6432dd2ddde93cf76c5dadc8',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete course assignment 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/professor/courses/:id/assignments/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assignment removed successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/assignments/6432dd2ddde93cf76c5dadc8',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

- `GET - api/v1/professor/courses/:id/assignments/:id/submissions` - Index [Details](#index-course-assignment-submissions-)
- `GET - api/v1/professor/courses/:id/assignments/:id/submissions/:id` - Show [Details](#show-course-assignment-submission-)

##### COURSE ASSIGNMENT SUBMISSIONS ⭐

###### Index course assignment submissions 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/assignments/:id/submissions`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Submissions fetched successfully",
    "data": {
      "submissionsCount": 0,
      "submissions": []
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/assignments/6432e0d4dde93cf76c5dade9/submissions',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show course assignment submission 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/assignments/:id/submissions/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Submission fetched successfully",
    "data": {
      "submission": {
        "grade": 0,
        "feedback": "",
        "assignment": "6432e0d4dde93cf76c5dade9",
        "student": "6430ce43c3ca49b01012f8ca",
        "createdAt": "2023-04-09T15:43:42.052Z",
        "updatedAt": "2023-04-09T15:52:40.249Z",
        "__v": 0,
        "id": "6432e0d4dde93cf76c5dade9"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430ce43c3ca49b01012f8ca/assignments/6432e0d4dde93cf76c5dade9/submissions/6432e0d4dde93cf76c5dade9',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### EXAM ⭐

###### Create exam 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/professor/courses/:id/exams`
- _Headers:_ `Authorization`
- _Body:_

  ```json
  {
    "name": "Exam 01",
    "startAtDay": "6",
    "startAtMonth": "4",
    "startAtYear": "2023",
    "startAtHour": "12",
    "startAtMinute": "30",
    "durationInMinutes": "20"
  }
  ```

- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Exam created successfully.",
    "data": {
      "exam": {
        "name": "exam 01",
        "startAt": "2023-04-10T10:30:00.000Z",
        "durationInMinutes": 20,
        "endAt": "2023-04-10T10:50:00.000Z",
        "course": "6430e37e95394133234b0cdf",
        "questions": [],
        "totalScore": 0,
        "submissions": [],
        "enrollments": [],
        "professor": "6430c7854e29a1ff8375d1e7",
        "_id": "6432e33bdde93cf76c5dae02",
        "createdAt": "2023-04-09T16:09:31.782Z",
        "updatedAt": "2023-04-09T16:09:31.782Z",
        "__v": 0
      },
      "course": {
        "id": "6430e37e95394133234b0cdf",
        "name": "image processing"
      },
      "professor": {
        "id": "6430c7854e29a1ff8375d1e7",
        "name": "dr. mohamed yasser"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'Exam 01',
    startAtDay: '10',
    startAtMonth: '4',
    startAtYear: '2023',
    startAtHour: '12',
    startAtMinute: '30',
    durationInMinutes: '20',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430e37e95394133234b0cdf/exams',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index exams 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/exams`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Exams fetched successfully",
    "data": {
      "examsCount": 1,
      "exams": [
        {
          "id": "6432e33bdde93cf76c5dae02",
          "_id": "6432e33bdde93cf76c5dae02",
          "name": "exam 01",
          "startAt": "2023-04-10T10:30:00.000Z",
          "durationInMinutes": 20,
          "endAt": "2023-04-10T10:50:00.000Z",
          "course": "6430e37e95394133234b0cdf",
          "questions": [],
          "totalScore": 0,
          "submissions": [],
          "enrollments": [],
          "professor": "6430c7854e29a1ff8375d1e7",
          "createdAt": "2023-04-09T16:09:31.782Z",
          "updatedAt": "2023-04-09T16:09:31.782Z",
          "__v": 0
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430e37e95394133234b0cdf/exams',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show exam 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/exams/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Exam fetched successfully",
    "data": {
      "exam": {
        "id": "6432e33bdde93cf76c5dae02",
        "_id": "6432e33bdde93cf76c5dae02",
        "name": "exam 01",
        "startAt": "2023-04-10T10:30:00.000Z",
        "durationInMinutes": 20,
        "endAt": "2023-04-10T10:50:00.000Z",
        "course": "6430e37e95394133234b0cdf",
        "questions": [],
        "totalScore": 0,
        "submissions": [],
        "enrollments": [],
        "professor": "6430c7854e29a1ff8375d1e7",
        "createdAt": "2023-04-09T16:09:31.782Z",
        "updatedAt": "2023-04-09T16:09:31.782Z",
        "__v": 0
      },
      "course": {
        "id": "6430e37e95394133234b0cdf",
        "name": "image processing"
      },
      "professor": {
        "id": "6430c7854e29a1ff8375d1e7",
        "name": "dr. mohamed yasser"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430e37e95394133234b0cdf/exams/6432e33bdde93cf76c5dae02',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update exam 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/professor/courses/:id/exams/:id`
- _Headers:_ `Authorization`
- _Body:_

  ```json
  {
    "name": "exam 99",
    "startAtDay": "6",
    "startAtMonth": "10",
    "startAtYear": "2023",
    "startAtHour": "15",
    "startAtMinute": "10",
    "durationInMinutes": "20"
  }
  ```

- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Exam updated successfully.",
    "data": {
      "exam": {
        "id": "6432e33bdde93cf76c5dae02",
        "name": "exam 99",
        "startAt": "2023-10-06T13:10:00.000Z",
        "endAt": "2023-10-06T13:30:00.000Z",
        "durationInMinutes": 20
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'exam 99',
    startAtDay: '6',
    startAtMonth: '10',
    startAtYear: '2023',
    startAtHour: '15',
    startAtMinute: '10',
    durationInMinutes: '20',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430e37e95394133234b0cdf/exams/6432e33bdde93cf76c5dae02',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete exam 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/professor/courses/:id/exams/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Exam deleted successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430e37e95394133234b0cdf/exams/6432e33bdde93cf76c5dae02',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Start now exam 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/professor/courses/:id/exams/:id/start-now`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Exam will start now.",
    "data": {
      "exam": {
        "id": "6432e59cdde93cf76c5dae17",
        "name": "exam 01"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430e37e95394133234b0cdf/exams/6432e59cdde93cf76c5dae17/start-now',
    {
      method: 'PATCH',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### EXAM SUBMISSIONS ⭐

###### Index exam submissions 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/exams/:id/submissions`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Exam submissions fetched successfully",
    "data": {
      "examSubmissionsCount": 0,
      "examSubmissions": [],
      "exam": {
        "id": "6432e59cdde93cf76c5dae17",
        "name": "exam 01"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430e37e95394133234b0cdf/exams/6432e59cdde93cf76c5dae17/submissions',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

- `GET - api/v1/professor/courses/:id/exams/:id/enrollments` - Index [Details](#index-exam-enrollments-)

##### EXAM ENROLLMENTS ⭐

###### Index exam enrollments 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/exams/:id/enrollments`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Exam enrollments fetched successfully",
    "data": {
      "examEnrollmentsCount": 0,
      "examEnrollments": [],
      "exam": {
        "id": "6432e59cdde93cf76c5dae17",
        "name": "exam 01"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430e37e95394133234b0cdf/exams/6432e59cdde93cf76c5dae17/enrollments',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### EXAM QUESTIONS ( Text and/or Image or both ) ⭐

###### Create exam question 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/professor/courses/:id/exams/:id/questions`
- _Headers:_ `Authorization`
- _Body:_

  ```json
  {
    "contentText": "Question 2",
    "contentImage": "true",
    "score": "7",
    "answersArray": ["answer 1", "answer 2", "answer 3"],
    "correctAnswerIndex": "1" // 0 based index [0, 1, 2, 3, ...]
  }
  ```

- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Question created successfully",
    "data": {
      "question": {
        "contentText": "Question 2",
        "contentImage": "64330490101ff077ea74633f",
        "answers": [
          "64330490101ff077ea746341",
          "64330490101ff077ea746343",
          "64330490101ff077ea746345"
        ],
        "score": 7,
        "course": "6430e37e95394133234b0cdf",
        "professor": "6430c7854e29a1ff8375d1e7",
        "exam": "6433047d101ff077ea746339",
        "_id": "64330490101ff077ea746340",
        "correctAnswer": "64330490101ff077ea746343",
        "createdAt": "2023-04-09T18:31:44.840Z",
        "updatedAt": "2023-04-09T18:31:44.840Z",
        "__v": 0,
        "id": "64330490101ff077ea746340"
      },
      "exam": {
        "id": "6433047d101ff077ea746339",
        "name": "exam 01"
      },
      "course": {
        "id": "6430e37e95394133234b0cdf",
        "name": "image processing"
      },
      "professor": {
        "id": "6430c7854e29a1ff8375d1e7",
        "name": "dr. mohamed yasser"
      }
    }
  }
  ```

- _Example - JS_:

```js
let headersList = {
  Accept: '*/*',
  Authorization:
    'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  'Content-Type': 'application/json',
};

let bodyContent = JSON.stringify({
  contentText: 'Question 2',
  contentImage: 'true',
  score: '7',
  answersArray: ['answer 1', 'answer 2', 'answer 3'],
  correctAnswerIndex: '1',
});

let response = await fetch(
  'http://localhost:3000/api/v1/professor/courses/6430e37e95394133234b0cdf/exams/6433047d101ff077ea746339/questions',
  {
    method: 'POST',
    body: bodyContent,
    headers: headersList,
  }
);

let data = await response.text();
console.log(data);
```

###### Index exam questions 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/exams/:id/questions`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Questions fetched successfully",
    "data": {
      "questionsCount": 1,
      "questions": [
        {
          "id": "64330490101ff077ea746340",
          "contentText": "Question 2",
          "score": 7
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430e37e95394133234b0cdf/exams/6433047d101ff077ea746339/questions',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show exam question 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/professor/courses/:id/exams/:id/questions/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Question fetched successfully",
    "data": {
      "question": {
        "id": "64330490101ff077ea746340",
        "contentText": "Question 2",
        "contentImage": "64330490101ff077ea74633f",
        "score": 7,
        "answers": [
          {
            "id": "64330490101ff077ea746341",
            "contentText": "answer 1"
          },
          {
            "id": "64330490101ff077ea746343",
            "contentText": "answer 2"
          },
          {
            "id": "64330490101ff077ea746345",
            "contentText": "answer 3"
          }
        ],
        "correctAnswerId": "64330490101ff077ea746343"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430e37e95394133234b0cdf/exams/6433047d101ff077ea746339/questions/64330490101ff077ea746340',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update exam question 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/professor/courses/:id/exams/:id/questions/:id`
- _Headers:_ `Authorization`
- _Body:_
  ```json
  {
    "contentText": "this is a question!!",
    "score": "5",
    "correctAnswerId": "64330490101ff077ea746341"
  }
  ```
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "question updated successfully",
    "data": {
      "question": {
        "id": "64330490101ff077ea746340",
        "contentText": "this is a question!!",
        "score": 5,
        "correctAnswer": "64330490101ff077ea746341"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    contentText: 'this is a question!!',
    score: '5',
    correctAnswerId: '64330490101ff077ea746341',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430e37e95394133234b0cdf/exams/6433047d101ff077ea746339/questions/64330490101ff077ea746340',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete exam question 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/professor/courses/:id/exams/:id/questions/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Question deleted successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430e37e95394133234b0cdf/exams/6433047d101ff077ea746339/questions/64330490101ff077ea746340',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

- `PATCH - api/v1/professor/courses/:id/exams/:id/questions/:id/answers/:id` - Update [Details](#update-exam-question-answer-)

##### EXAM QUESTION ANSWERS ⭐

###### Update exam question answer 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/professor/courses/:id/exams/:id/questions/:id/answers/:id`
- _Headers:_ `Authorization`
- _Body:_
  ```json
  {
    "contentText": "new answer"
  }
  ```
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Answer updated successfully",
    "data": {
      "answer": {
        "id": "6433086febda70cf0481c977",
        "contentText": "new answer"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGM3ODU0ZTI5YTFmZjgzNzVkMWU3Iiwicm9sZSI6InByb2Zlc3NvciJ9LCJpYXQiOjE2ODA5MTg0MjgsImV4cCI6MTY4MzUxMDQyOH0.tsqXjcQK_OSHtX8Q9cM__7Kcj6CLCMm2u2hkp3qoMEU',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    contentText: 'new answer',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/professor/courses/6430e37e95394133234b0cdf/exams/6433047d101ff077ea746339/questions/6433086febda70cf0481c976/answers/6433086febda70cf0481c977',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

#### ASSISTANT 👨‍🏫

##### ACCESS PERMISSOIN ⭐

###### Show assistant 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/assistant/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "assistant fetched successfully",
    "data": {
      "assistant": {
        "id": "6430ed28e0848ccfef40807a",
        "createdAt": "2023-04-08T04:27:20.066Z",
        "name": "mohamed yasser",
        "username": "mohamed-user-09",
        "academicId": "9887593780045",
        "qrCode": "6430ed28e0848ccfef408078",
        "courses": ["6430ce43c3ca49b01012f8ca"],
        "contacts": "6430ed28e0848ccfef408079"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/6430ed28e0848ccfef40807a',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update assistant 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/assistant/:id`
- _Headers:_ `Authorization`
- _Body:_
  ```json
  {
    "name": "my new name",
    "academicId": "878978798978"
  }
  ```
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "assistant updated successfully",
    "data": {
      "assistant": {
        "id": "6430ed28e0848ccfef40807a",
        "name": "my new name",
        "academicId": "878978798978"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'my new name',
    academicId: '878978798978',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/6430ed28e0848ccfef40807a',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

- `GET - api/v1/assistant/courses` - Index [Details](#index-courses-assistant-)
- `GET - api/v1/assistant/courses/:id` - Show [Details](#show-course-assistant-)

##### COURSE ⭐

###### Index courses assistant 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/assistant/courses`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Courses fetched successfully",
    "data": {
      "coursesCount": 1,
      "courses": [
        {
          "id": "6430ce43c3ca49b01012f8ca",
          "name": "machine learning",
          "code": "cs45",
          "createdAt": "2023-04-08T02:15:31.406Z",
          "updatedAt": "2023-04-09T15:59:16.604Z"
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch('http://localhost:3000/api/v1/assistant/courses', {
    method: 'GET',
    headers: headersList,
  });

  let data = await response.text();
  console.log(data);
  ```

###### Show course assistant 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/assistant/courses/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Course fetched successfully",
    "data": {
      "course": {
        "_id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning",
        "code": "cs45",
        "semester": "first",
        "professor": {
          "_id": "6430c7854e29a1ff8375d1e7",
          "name": "dr. mohamed yasser"
        },
        "assistants": ["6430ed28e0848ccfef40807a"],
        "students": [],
        "lectures": [
          "64322cf88becbaa1fe44e152",
          "6432d82919c58a344497f4a7",
          "6432d85e19c58a344497f4b4",
          "6432e0cadde93cf76c5dade3"
        ],
        "sections": [],
        "assignments": ["6432e0d4dde93cf76c5dade9"],
        "exams": [],
        "department": {
          "_id": "6430596c112031c1dbfc3fd8",
          "name": "computer science"
        },
        "program": {
          "_id": "643052a83eea93f118839c46",
          "name": "public"
        },
        "level": {
          "_id": "642ee7f789a92ceeba6b7a4f",
          "name": "level 01"
        },
        "collage": {
          "_id": "642e3cb699182e5e2d14ec59",
          "name": "fuculty of engineering"
        },
        "university": {
          "_id": "642deaa976e91123782b7f16",
          "name": "alu"
        },
        "createdAt": "2023-04-08T02:15:31.406Z",
        "updatedAt": "2023-04-09T15:59:16.604Z",
        "__v": 12
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### SECTION ⭐

###### Create section assistant 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections`
- _Headers:_ `Authorization`
- _Body:_

  ```json
  {
    "name": "Section 02",
    "number": 2
  }
  ```

- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Section created successfully",
    "data": {
      "section": {
        "id": "64333b450ea788a84c9579e6"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'Section 02',
    number: 2,
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index sections assistant 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Sections fetched successfully",
    "data": {
      "sectionsCount": 2,
      "sections": [
        {
          "_id": "64333b450ea788a84c9579e6",
          "name": "section 02",
          "number": 2,
          "resources": [],
          "assistant": "6430ed28e0848ccfef40807a",
          "course": "6430ce43c3ca49b01012f8ca",
          "assignments": [],
          "createdAt": "2023-04-09T22:25:09.218Z",
          "updatedAt": "2023-04-09T22:25:09.218Z",
          "__v": 0
        },
        {
          "_id": "64333b152d1b672a2ee9a1a0",
          "name": "section 01",
          "number": 1,
          "resources": [],
          "assistant": "6430ed28e0848ccfef40807a",
          "course": "6430ce43c3ca49b01012f8ca",
          "assignments": [],
          "createdAt": "2023-04-09T22:24:21.364Z",
          "updatedAt": "2023-04-09T22:24:21.364Z",
          "__v": 0
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show section assistant 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Section fetched successfully",
    "data": {
      "section": {
        "_id": "64333b450ea788a84c9579e6",
        "name": "section 02",
        "number": 2,
        "resources": [],
        "assistant": "6430ed28e0848ccfef40807a",
        "course": "6430ce43c3ca49b01012f8ca",
        "assignments": [],
        "createdAt": "2023-04-09T22:25:09.218Z",
        "updatedAt": "2023-04-09T22:25:09.218Z",
        "__v": 0
      },
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update section assistant 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id`
- _Headers:_ `Authorization`
- _Body:_
  ```json
  {
    "name": "New section name",
    "number": 6
  }
  ```
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Section fetched successfully",
    "data": {
      "section": {
        "_id": "64333b450ea788a84c9579e6",
        "name": "section 02",
        "number": 2,
        "resources": [],
        "assistant": "6430ed28e0848ccfef40807a",
        "course": "6430ce43c3ca49b01012f8ca",
        "assignments": [],
        "createdAt": "2023-04-09T22:25:09.218Z",
        "updatedAt": "2023-04-09T22:25:09.218Z",
        "__v": 0
      },
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'New section name',
    number: 6,
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete section assistant 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Section fetched successfully",
    "data": {
      "section": {
        "_id": "64333b450ea788a84c9579e6",
        "name": "section 02",
        "number": 2,
        "resources": [],
        "assistant": "6430ed28e0848ccfef40807a",
        "course": "6430ce43c3ca49b01012f8ca",
        "assignments": [],
        "createdAt": "2023-04-09T22:25:09.218Z",
        "updatedAt": "2023-04-09T22:25:09.218Z",
        "__v": 0
      },
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

- `POST - api/v1/assistant/courses/:id/sections/:id/attendance` - Create [Details](#create-attendance-assistant-)
- `GET - api/v1/assistant/courses/:id/sections/:id/attendance/:id` - Show [Details](#show-attendance-assistant-)
- `GET - api/v1/assistant/courses/:id/sections/:id/attendance/:id/students` - Index Students [Details](#index-attendance-assistant-students-)
- `DELETE - api/v1/assistant/courses/:id/sections/:id/attendance/:id/students/:id` - Delete Student [Details](#delete-attendance-assistant-student-)

##### ATTENDANCE ( QR CODE & LOCATION ) ⭐

###### Create attendance assistant 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/attendance`
- _Headers:_ `Authorization`
- _Body:_
  ```json
  {
    "distanceInMeters": 100,
    "durationInMinutes": 60,
    "lat": "31.205753",
    "lng": "29.924526"
  }
  ```
- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Attendance created successfully.",
    "data": {
      "attendance": {
        "students": [],
        "section": "64333b450ea788a84c9579e6",
        "distanceInMeters": 100,
        "creatorCoordinates": {
          "lat": "31.205753",
          "lng": "29.924526"
        },
        "durationInMinutes": 60,
        "expiredAt": "2023-04-10T04:41:28.704Z",
        "randomAccessKey": "CHDC5wyn0c",
        "_id": "64338568efee0439e703eecf",
        "createdAt": "2023-04-10T03:41:28.711Z",
        "updatedAt": "2023-04-10T03:41:28.711Z",
        "__v": 0,
        "id": "64338568efee0439e703eecf"
      },
      "section": {
        "id": "64333b450ea788a84c9579e6",
        "name": "section 02"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    distanceInMeters: 100,
    durationInMinutes: 60,
    lat: '31.205753',
    lng: '29.924526',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/attendance',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show attendance assistant 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/attendance/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Attendance created successfully.",
    "data": {
      "attendance": {
        "students": [],
        "section": "64333b450ea788a84c9579e6",
        "distanceInMeters": 100,
        "creatorCoordinates": {
          "lat": "31.205753",
          "lng": "29.924526"
        },
        "durationInMinutes": 60,
        "expiredAt": "2023-04-10T04:41:28.704Z",
        "randomAccessKey": "CHDC5wyn0c",
        "_id": "64338568efee0439e703eecf",
        "createdAt": "2023-04-10T03:41:28.711Z",
        "updatedAt": "2023-04-10T03:41:28.711Z",
        "__v": 0,
        "id": "64338568efee0439e703eecf"
      },
      "section": {
        "id": "64333b450ea788a84c9579e6",
        "name": "section 02"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/attendance/64338568efee0439e703eecf',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index attendance assistant students 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/attendance/:id/students`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Students fetched successfully",
    "data": {
      "students": []
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/attendance/64338568efee0439e703eecf/students',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete attendance assistant student 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/attendance/:id/students/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Student deleted successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/attendance/64338568efee0439e703eecf/students/6430ce43c3ca49b01012f8ca',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

- `POST - api/v1/assistant/courses/:id/sections/:id/assignments` - Create [Details](#create-section-assignment-assistant-)
- `GET - api/v1/assistant/courses/:id/sections/:id/assignments` - Index [Details](#index-section-assignments-assistant-)
- `GET - api/v1/assistant/courses/:id/sections/:id/assignments/:id` - Show [Details](#show-section-assignment-assistant-)
- `PATCH - api/v1/assistant/courses/:id/sections/:id/assignments/:id` - Update [Details](#update-section-assignment-assistant-)
- `DELETE - api/v1/assistant/courses/:id/sections/:id/assignments/:id` - Delete [Details](#delete-section-assignment-assistant-)

##### ASSIGNMENT ⭐

###### Create section assignment assistant 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/assignments`
- _Headers:_ `Authorization`
- _Body:_ `title, description, dueDate, file`

  ```json
  {
    "title": "this is new assignment for the section",
    "contentText": "in this assignment you should create static website using htm, css, js",
    "dueToDays": 5
  }
  ```

- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Assignment created",
    "data": {
      "assignment": {
        "title": "this is new assignment for the section",
        "contentText": "in this assignment you should create static website using htm, css, js",
        "contentImage": "64338862b26563cf63a1934c",
        "dueDate": "2023-04-15T03:54:10.618Z",
        "assistant": "6430ed28e0848ccfef40807a",
        "course": "6430ce43c3ca49b01012f8ca",
        "section": "64333b450ea788a84c9579e6",
        "submissions": [],
        "_id": "64338862b26563cf63a1934d",
        "createdAt": "2023-04-10T03:54:10.749Z",
        "updatedAt": "2023-04-10T03:54:10.749Z",
        "__v": 0
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    title: 'this is new assignment for the section',
    contentText:
      'in this assignment you should create static website using htm, css, js',
    dueToDays: 5,
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/assignments',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index section assignments assistant 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/assignments`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assignments fetched successfully",
    "data": {
      "assignmentsCount": 1,
      "assignments": [
        {
          "id": "64338862b26563cf63a1934d",
          "_id": "64338862b26563cf63a1934d",
          "title": "this is new assignment for the section",
          "contentText": "in this assignment you should create static website using htm, css, js",
          "contentImage": "64338862b26563cf63a1934c",
          "dueDate": "2023-04-15T03:54:10.618Z",
          "assistant": "6430ed28e0848ccfef40807a",
          "course": "6430ce43c3ca49b01012f8ca",
          "section": "64333b450ea788a84c9579e6",
          "submissions": [],
          "createdAt": "2023-04-10T03:54:10.749Z",
          "updatedAt": "2023-04-10T03:54:10.749Z",
          "__v": 0
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/assignments',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show section assignment assistant 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/assignments/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assignment fetched successfully",
    "data": {
      "assignment": {
        "_id": "64338862b26563cf63a1934d",
        "title": "this is new assignment for the section",
        "contentText": "in this assignment you should create static website using htm, css, js",
        "contentImage": "64338862b26563cf63a1934c",
        "dueDate": "2023-04-15T03:54:10.618Z",
        "assistant": "6430ed28e0848ccfef40807a",
        "course": "6430ce43c3ca49b01012f8ca",
        "section": "64333b450ea788a84c9579e6",
        "submissions": [],
        "createdAt": "2023-04-10T03:54:10.749Z",
        "updatedAt": "2023-04-10T03:54:10.749Z",
        "__v": 0,
        "id": "64338862b26563cf63a1934d"
      },
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning"
      },
      "section": {
        "id": "64333b450ea788a84c9579e6",
        "name": "section 02"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/assignments/64338862b26563cf63a1934d',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update section assignment assistant 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/assignments/:id`
- _Headers:_ `Authorization`
- _Body:_

  ```json
  {
    "title": "section assignment new title",
    "contentText": "this is updated content text",
    "dueToDays": 9
  }
  ```

- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "The assignment updated successfully",
    "data": {
      "assignment": {
        "_id": "64338862b26563cf63a1934d",
        "title": "section assignment new title",
        "contentText": "this is updated content text",
        "contentImage": "64338862b26563cf63a1934c",
        "dueDate": "2023-04-19T03:56:33.568Z",
        "assistant": "6430ed28e0848ccfef40807a",
        "course": "6430ce43c3ca49b01012f8ca",
        "section": "64333b450ea788a84c9579e6",
        "submissions": [],
        "createdAt": "2023-04-10T03:54:10.749Z",
        "updatedAt": "2023-04-10T03:56:33.688Z",
        "__v": 0,
        "id": "64338862b26563cf63a1934d"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    title: 'section assignment new title',
    contentText: 'this is updated content text',
    dueToDays: 9,
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/assignments/64338862b26563cf63a1934d',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete section assignment assistant 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/assignments/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assignment removed successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/assignments/64338862b26563cf63a1934d',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### SECTION RESOURCES ⭐

###### Create section resource assistant 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/resources`
- _Headers:_ `Authorization`
- _Body:_

  ```json
  {
    "name": "section resource for the whiteboard",
    "type": "png" // Allowed types // allowed types without mime type [jpeg, png, pdf, doc, xls, docx, xlsx, pptx, mp3, mp4]
  }
  ```

- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Section resource created",
    "data": {
      "storage": {
        "path": "courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/resources/4625dabc-5a1c-4696-a7a4-1dcc1bd4499d.png",
        "type": "image/png",
        "name": "section resource for the whiteboard",
        "owner": "6430ed28e0848ccfef40807a",
        "_id": "64338b889d30e909adbe568a",
        "createdAt": "2023-04-10T04:07:36.651Z",
        "updatedAt": "2023-04-10T04:07:36.651Z",
        "__v": 0,
        "id": "64338b889d30e909adbe568a"
      },
      "section": {
        "_id": "64333b450ea788a84c9579e6",
        "name": "section 02",
        "number": 2,
        "resources": ["64338b889d30e909adbe568a"],
        "assistant": "6430ed28e0848ccfef40807a",
        "course": "6430ce43c3ca49b01012f8ca",
        "assignments": [],
        "createdAt": "2023-04-09T22:25:09.218Z",
        "updatedAt": "2023-04-10T04:07:36.769Z",
        "__v": 3,
        "attendance": "64338568efee0439e703eecf",
        "id": "64333b450ea788a84c9579e6"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'section resource for the whiteboard',
    type: 'png',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/resources',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Index section resources assistant 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/resources`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Resources fetched successfully",
    "data": {
      "resources": [
        {
          "_id": "64338b889d30e909adbe568a",
          "type": "image/png",
          "name": "section resource for the whiteboard",
          "id": "64338b889d30e909adbe568a"
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/64199f7356f349d3513ab2b9/sections/641b0a475fc1040d89eb8a04/resources',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show section resource assistant 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/resources/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Resource fetched successfully",
    "data": {
      "resource": {
        "_id": "64338b889d30e909adbe568a",
        "path": "courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/resources/4625dabc-5a1c-4696-a7a4-1dcc1bd4499d.png",
        "type": "image/png",
        "name": "section resource for the whiteboard",
        "owner": "6430ed28e0848ccfef40807a",
        "createdAt": "2023-04-10T04:07:36.651Z",
        "updatedAt": "2023-04-10T04:07:36.651Z",
        "__v": 0,
        "id": "64338b889d30e909adbe568a"
      },
      "section": {
        "id": "64333b450ea788a84c9579e6",
        "name": "section 02"
      },
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/resources/64338b889d30e909adbe568a',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update section resource assistant 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/resources/:id`
- _Headers:_ `Authorization`
- _Body:_
  ```json
  {
    "name": "new resource name"
  }
  ```
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Resource updated successfully",
    "data": {
      "resource": {
        "_id": "64338b889d30e909adbe568a",
        "path": "courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/resources/4625dabc-5a1c-4696-a7a4-1dcc1bd4499d.png",
        "type": "image/png",
        "name": "new resource name",
        "owner": "6430ed28e0848ccfef40807a",
        "createdAt": "2023-04-10T04:07:36.651Z",
        "updatedAt": "2023-04-10T04:15:02.005Z",
        "__v": 0,
        "id": "64338b889d30e909adbe568a"
      },
      "section": {
        "id": "64333b450ea788a84c9579e6",
        "name": "section 02"
      },
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    name: 'new resource name',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/resources/64338b889d30e909adbe568a',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Delete section resource assistant 📌

- _HTTP Method:_ `DELETE`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/resources/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Resource removed successfully",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/resources/64338b889d30e909adbe568a',
    {
      method: 'DELETE',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### ASSIGNMENT SUBMISSIONS ⭐

###### Index section assignment submissions assistant 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/assignments/:id/submissions`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Submissions fetched successfully",
    "data": {
      "submissionsCount": 0,
      "submissions": []
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/assignments/64338e5c9d30e909adbe56ab/submissions',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show section assignment submission assistant 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/assistant/courses/:id/sections/:id/assignments/:id/submissions/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Submission fetched successfully",
    "data": {
      "submission": {
        "id": "64338e5c9d30e909adbe56ab",
        "student": {
          "id": "6430ce43c3ca49b01012f8ca",
          "name": "Ahmed"
        },
        "assignment": {
          "id": "6430ce43c3ca49b01012f8ca",
          "name": "assignment 01"
        },
        "section": {
          "id": "6430ce43c3ca49b01012f8ca",
          "name": "section 02"
        },
        "course": {
          "id": "6430ce43c3ca49b01012f8ca",
          "name": "machine learning"
        },
        "grade": 0,
        "submittedAt": "2021-09-30T12:00:00.000Z",
        "submittedFiles": [
          {
            "id": "6430ce43c3ca49b01012f8ca",
            "name": "file 01"
          }
        ]
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMGVkMjhlMDg0OGNjZmVmNDA4MDdhIiwicm9sZSI6ImFzc2lzdGFudCJ9LCJpYXQiOjE2ODEwNzM5MzYsImV4cCI6MTY4MzY2NTkzNn0.OLgmho2JmORrkQ7Ct45E9NmUoDWFjd021fxnAsIIpyk',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/assistant/courses/6430ce43c3ca49b01012f8ca/sections/64333b450ea788a84c9579e6/assignments/64338e5c9d30e909adbe56ab/submissions/6430ce43c3ca49b01012f8ca',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

#### STUDENT 👨‍🎓

- `GET - api/v1/student/:id` - Show [Details](#show-student-)

##### ACCESS PERMISSOIN ⭐

###### Show student access permission 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "student fetched successfully",
    "data": {
      "student": {
        "id": "64339e899d30e909adbe56cc",
        "createdAt": "2023-04-10T05:28:41.127Z",
        "name": "mohamed yasser",
        "username": "mohamedyasser459rf",
        "academicId": "9879873833",
        "qrCode": "64339e889d30e909adbe56c8",
        "courses": [],
        "contacts": "64339e899d30e909adbe56ca"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01"
      },
      "program": {
        "id": "643052a83eea93f118839c46",
        "name": "public"
      },
      "department": {
        "id": "6430596c112031c1dbfc3fd8",
        "name": "computer science"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/64339e899d30e909adbe56cc',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### COURSE ⭐

###### Index courses student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Courses fetched successfully.",
    "data": {
      "courses": [
        {
          "id": "6430ce43c3ca49b01012f8ca",
          "name": "machine learning",
          "code": "cs45",
          "professor": {
            "_id": "6430c7854e29a1ff8375d1e7",
            "name": "dr. mohamed yasser"
          },
          "isEnrolled": false
        },
        {
          "id": "6430e37e95394133234b0cdf",
          "name": "image processing",
          "code": "cs45",
          "professor": {
            "_id": "6430c7854e29a1ff8375d1e7",
            "name": "dr. mohamed yasser"
          },
          "isEnrolled": false
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch('http://localhost:3000/api/v1/student/courses', {
    method: 'GET',
    headers: headersList,
  });

  let data = await response.text();
  console.log(data);
  ```

###### Show course student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Course fetched successfully.",
    "data": {
      "course": {
        "id": "6430ce43c3ca49b01012f8ca",
        "name": "machine learning",
        "code": "cs45"
      },
      "professor": {
        "id": "6430c7854e29a1ff8375d1e7",
        "name": "dr. mohamed yasser"
      },
      "university": {
        "id": "642deaa976e91123782b7f16",
        "name": "alu"
      },
      "collage": {
        "id": "642e3cb699182e5e2d14ec59",
        "name": "fuculty of engineering"
      },
      "department": {
        "id": "6430596c112031c1dbfc3fd8",
        "name": "computer science"
      },
      "program": {
        "id": "643052a83eea93f118839c46",
        "name": "public"
      },
      "level": {
        "id": "642ee7f789a92ceeba6b7a4f",
        "name": "level 01"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430ce43c3ca49b01012f8ca',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Enroll course student 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/student/courses/:id/enroll`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Student enrolled in course successfully.",
    "data": {}
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430ce43c3ca49b01012f8ca/enroll',
    {
      method: 'POST',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### COURSE EXAM ⭐

###### Index course exams student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses/:id/exams`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Exams fetched successfully",
    "data": {
      "exams": [
        {
          "id": "6432e59cdde93cf76c5dae17",
          "name": "exam 01",
          "startAt": "2023-04-09T16:20:00.000Z",
          "endAt": "2023-04-09T16:40:00.000Z",
          "durationInMinutes": 20,
          "isActive": false
        },
        {
          "id": "6433047d101ff077ea746339",
          "name": "exam 01",
          "startAt": "2023-04-10T10:30:00.000Z",
          "endAt": "2023-04-10T10:50:00.000Z",
          "durationInMinutes": 20,
          "isActive": false
        },
        {
          "id": "64349c56162ca94a690b312e",
          "name": "exam 01",
          "startAt": "2023-04-10T23:33:00.000Z",
          "endAt": "2023-04-11T01:33:00.000Z",
          "durationInMinutes": 120,
          "isActive": true
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({});

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/exams',
    {
      method: 'GET',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Enroll course exam student 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/student/courses/:id/exams/:id/enroll`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Enrolled in exam successfully",
    "data": {
      "exam": {
        "id": "64349c56162ca94a690b312e",
        "name": "exam 01",
        "startAt": "2023-04-10T23:33:00.000Z",
        "endAt": "2023-04-11T01:33:00.000Z",
        "questions": [
          {
            "id": "64349ca2162ca94a690b3140",
            "contentText": "Question 1",
            "contentImage": "64349ca2162ca94a690b313f",
            "score": 7,
            "answers": [
              {
                "id": "64349ca2162ca94a690b3141",
                "contentText": "answer 1"
              },
              {
                "id": "64349ca2162ca94a690b3143",
                "contentText": "answer 2"
              },
              {
                "id": "64349ca2162ca94a690b3145",
                "contentText": "answer 3"
              }
            ]
          },
          {
            "id": "64349cb4162ca94a690b314e",
            "contentText": "Question 2",
            "contentImage": "64349cb4162ca94a690b314d",
            "score": 9,
            "answers": [
              {
                "id": "64349cb4162ca94a690b314f",
                "contentText": "answer 1"
              },
              {
                "id": "64349cb4162ca94a690b3151",
                "contentText": "answer 2"
              },
              {
                "id": "64349cb4162ca94a690b3153",
                "contentText": "answer 3"
              }
            ]
          }
        ]
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzNDllMWI3MDVhMTRjMjdhYWU1MTI3Iiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTY5OTYxLCJleHAiOjE2ODM3NjE5NjF9.BwcErknbAN7_5RbJ0tqNjFehR-qCIPrI0lRr9xqZPCE',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/exams/64349c56162ca94a690b312e/enroll',
    {
      method: 'POST',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Submit course exam student 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/student/courses/:id/exams/:id/submit`
- _Headers:_ `Authorization`
- _Body:_
  ```json
  {
    "questionsWithAnswers": [
      "{question: '64349ca2162ca94a690b3140', answer: '64349ca2162ca94a690b3143'}",
      "{question: '64349cb4162ca94a690b314e', answer: '64349cb4162ca94a690b314f'}"
    ]
  }
  ```
- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Exam submitted successfully.",
    "data": {
      "totalScore": 16,
      "studentScore": 16
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzNDllMWI3MDVhMTRjMjdhYWU1MTI3Iiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTY5OTYxLCJleHAiOjE2ODM3NjE5NjF9.BwcErknbAN7_5RbJ0tqNjFehR-qCIPrI0lRr9xqZPCE',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    questionsWithAnswers: [
      "{question: '64349ca2162ca94a690b3140', answer: '64349ca2162ca94a690b3143'}",
      "{question: '64349cb4162ca94a690b314e', answer: '64349cb4162ca94a690b314f'}",
    ],
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/exams/64349c56162ca94a690b312e/submit',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### COURSE ASSIGNMENT ⭐

###### Index course assignments student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses/:id/assignments`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assignments fetched successfully",
    "assignments": [
      {
        "id": "6434a25263372d0aa8ecba3f",
        "title": "python cgi",
        "isExpired": false,
        "dueDate": "2023-04-17T23:57:06.076Z"
      }
    ]
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/assignments',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show course assignments student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses/:id/assignments/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assignment fetched successfully",
    "assignment": {
      "id": "6434a25263372d0aa8ecba3f",
      "title": "python cgi",
      "contentText": "In this assignment you should create a full python server side application and apply all CGI concepts we have learned in the lecture and section",
      "contentImage": "6434a25263372d0aa8ecba3e",
      "dueDate": "2023-04-17T23:57:06.076Z",
      "isExpired": false
    },
    "professor": {
      "id": "6430c7854e29a1ff8375d1e7",
      "name": "dr. mohamed yasser"
    },
    "course": {
      "id": "6430e37e95394133234b0cdf",
      "name": "image processing"
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/assignments/6434a25263372d0aa8ecba3f',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Submit course assignment student 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/student/courses/:id/assignments/:id/submit`
- _Headers:_ `Authorization`
- _Body:_

  ```json
  {
    "note": "this is student note",
    "fileType": "png"
  }
  ```

- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Assignment submitted successfully",
    "data": {
      "assignmentSubmission": {
        "file": "6434a2ac63372d0aa8ecba4f",
        "note": "this is student note",
        "assignment": "6434a25263372d0aa8ecba3f",
        "student": "64339e899d30e909adbe56cc",
        "course": "6430e37e95394133234b0cdf",
        "_id": "6434a2ac63372d0aa8ecba50",
        "createdAt": "2023-04-10T23:58:36.116Z",
        "updatedAt": "2023-04-10T23:58:36.116Z",
        "__v": 0,
        "id": "6434a2ac63372d0aa8ecba50"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    note: 'this is student note',
    fileType: 'png',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/assignments/6434a25263372d0aa8ecba3f/submit',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

- `GET - api/v1/student/courses/:id/assistants` - Index [Details](#index-course-assistants-student-)

##### COURSE ASSISTANTS ⭐

###### Index course assistants student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses/:id/assistants`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assistants fetched successfully.",
    "data": {
      "assistants": [
        {
          "id": "6434a4d063372d0aa8ecba6d",
          "name": "mohamed yasser"
        },
        {
          "id": "6434a4ff63372d0aa8ecba7e",
          "name": "mohamed yasser"
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/assistants',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### SECTION ⭐

###### Index sections student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses/:id/assistants/:id/sections`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Sections fetched successfully.",
    "data": {
      "sections": [
        {
          "id": "6434a6a363372d0aa8ecbaa5",
          "name": "section 02"
        }
      ],
      "assistant": {
        "id": "6434a64263372d0aa8ecba8f",
        "name": "mo"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/assistants/6434a64263372d0aa8ecba8f/sections',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show section student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses/:id/assistants/:id/sections/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Section found",
    "data": {
      "section": {
        "_id": "6434a6a363372d0aa8ecbaa5",
        "name": "section 02",
        "number": 2,
        "resources": [],
        "assistant": "6434a64263372d0aa8ecba8f",
        "course": "6430e37e95394133234b0cdf",
        "assignments": [],
        "createdAt": "2023-04-11T00:15:31.694Z",
        "updatedAt": "2023-04-11T00:15:31.694Z",
        "__v": 0
      },
      "assistant": {
        "id": "6434a64263372d0aa8ecba8f",
        "name": "mo"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/assistants/6434a64263372d0aa8ecba8f/sections/6434a6a363372d0aa8ecbaa5',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### SECTION RESOURCES ⭐

###### Index section resources student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses/:id/assistants/:id/sections/:id/resources`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Section resources fetched successfully",
    "data": {
      "resources": [
        {
          "_id": "6434abd1e7b70ce6c7e5d3af",
          "path": "courses/6430e37e95394133234b0cdf/sections/6434a6a363372d0aa8ecbaa5/resources/bc192957-fb34-4ef6-96ce-13fdb1ce0c78.png",
          "type": "image/png",
          "name": "section resource for the whiteboard",
          "owner": "6434a64263372d0aa8ecba8f",
          "createdAt": "2023-04-11T00:37:37.347Z",
          "updatedAt": "2023-04-11T00:37:37.347Z",
          "__v": 0,
          "id": "6434abd1e7b70ce6c7e5d3af"
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/assistants/6434a64263372d0aa8ecba8f/sections/6434a6a363372d0aa8ecbaa5/resources',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### SECTION ASSIGNMENT ⭐

###### Index section assignments student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses/:id/assistants/:id/sections/:id/assignments`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assignments fetched successfully",
    "assignments": [
      {
        "id": "6434ada7e7b70ce6c7e5d3cd",
        "title": "this is new assignment for the section",
        "isExpired": false,
        "dueDate": "2023-04-16T00:45:27.915Z"
      }
    ]
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/assistants/6434a64263372d0aa8ecba8f/sections/6434a6a363372d0aa8ecbaa5/assignments',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show section assignment student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses/:id/assistants/:id/sections/:id/assignments/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Assignment fetched successfully",
    "assignment": {
      "id": "6434ada7e7b70ce6c7e5d3cd",
      "title": "this is new assignment for the section",
      "contentText": "in this assignment you should create static website using htm, css, js",
      "contentImage": "6434ada7e7b70ce6c7e5d3cc",
      "dueDate": "2023-04-16T00:45:27.915Z",
      "isExpired": false
    },
    "assistant": {
      "id": "6434a64263372d0aa8ecba8f",
      "name": "mo"
    },
    "section": {
      "id": "6434a6a363372d0aa8ecbaa5",
      "name": "section 02"
    },
    "course": {
      "id": "6430e37e95394133234b0cdf",
      "name": "image processing"
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/assistants/6434a64263372d0aa8ecba8f/sections/6434a6a363372d0aa8ecbaa5/assignments/6434ada7e7b70ce6c7e5d3cd',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Submit section assignment student 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/student/courses/:id/assistants/:id/sections/:id/assignments/:id/submit`
- _Headers:_ `Authorization`
- _Body:_
  ```json
  {
    "note": "this is student note",
    "fileType": "png"
  }
  ```
- _Success Response:_ `201`

  ```json
  {
    "status": "success",
    "message": "Assignment submitted successfully",
    "data": {
      "assignmentSubmission": {
        "file": "6434aeec91da347928a86084",
        "note": "this is student note",
        "assignment": "6434ada7e7b70ce6c7e5d3cd",
        "student": "64339e899d30e909adbe56cc",
        "course": "6430e37e95394133234b0cdf",
        "section": "6434a6a363372d0aa8ecbaa5",
        "_id": "6434aeec91da347928a86085",
        "createdAt": "2023-04-11T00:50:52.142Z",
        "updatedAt": "2023-04-11T00:50:52.142Z",
        "__v": 0,
        "id": "6434aeec91da347928a86085"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    note: 'this is student note',
    fileType: 'png',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/assistants/6434a64263372d0aa8ecba8f/sections/6434a6a363372d0aa8ecbaa5/assignments/6434ada7e7b70ce6c7e5d3cd/submit',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### SECTION ATTENDANCE ⭐

###### Show section attendance student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses/:id/assistants/:id/sections/:id/attendance/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Attendance fetched successfully.",
    "data": {
      "attendance": {
        "id": "6434b4e9b8a4dc5e28d1c321",
        "isAttended": true
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/assistants/6434a64263372d0aa8ecba8f/sections/6434a6a363372d0aa8ecbaa5/attendance/6434b4e9b8a4dc5e28d1c321',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Attend section attendance student 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/student/courses/:id/assistants/:id/sections/:id/attendance/:id/attend`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Attended section successfully.",
    "data": {
      "attendance": {
        "id": "6434b4e9b8a4dc5e28d1c321",
        "isAttended": true
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzNGI2ZWNjY2Q3YWIyZTUwOGIyYTliIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTc2MzE5LCJleHAiOjE2ODM3NjgzMTl9.7ezCeW-eVpO5yepCy6UH41vHQmF7Kvux8HybKeg-T_w',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    randomAccessKey: 'en0JNha0iU',
    lat: '31.205753',
    lng: '29.924526',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/assistants/6434a64263372d0aa8ecba8f/sections/6434a6a363372d0aa8ecbaa5/attendance/6434b4e9b8a4dc5e28d1c321/attend',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### LECTURE ⭐

###### Index lectures student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses/:id/lectures`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Lectures fetched successfully.",
    "data": {
      "lectures": [
        {
          "id": "6434b916ccd7ab2e508b2ac3",
          "name": "lecture 03",
          "number": 3
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/lectures',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Show lecture student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses/:id/lectures/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Lecture fetched successfully.",
    "data": {
      "lecture": {
        "id": "6434b916ccd7ab2e508b2ac3",
        "name": "lecture 03",
        "number": 3,
        "resources": [],
        "createdAt": "2023-04-11T01:34:14.436Z"
      },
      "attendance": {}
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/lectures/6434b916ccd7ab2e508b2ac3',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### LECTURE RESOURCES ⭐

###### Index lecture resources student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses/:id/lectures/:id/resources`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Lecture resources fetched successfully",
    "data": {
      "resources": [
        {
          "_id": "6434be45b5d96421078c210a",
          "path": "courses/6430e37e95394133234b0cdf/lecture/6434b916ccd7ab2e508b2ac3/resources/c4e01461-414b-4f38-9c2f-a4b114ad4dc3.png",
          "type": "image/png",
          "name": "lecture 01 - resource",
          "owner": "6430c7854e29a1ff8375d1e7",
          "createdAt": "2023-04-11T01:56:21.752Z",
          "updatedAt": "2023-04-11T01:56:21.752Z",
          "__v": 0,
          "id": "6434be45b5d96421078c210a"
        }
      ]
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/lectures/6434b916ccd7ab2e508b2ac3/resources',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

- `GET - api/v1/student/courses/:id/lectures/:id/attendance/:id` - Show [Details](#show-lecture-attendance-student-)
- `POST - api/v1/student/courses/:id/lectures/:id/attendance/:id/attend` - Attend [Details](#attend-lecture-attendance-student-)

##### LECTURE ATTENDANCE ⭐

###### Show lecture attendance student 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/student/courses/:id/lectures/:id/attendance/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Attendance fetched successfully.",
    "data": {
      "attendance": {
        "id": "6434c0f21c684c5985ccaf70",
        "isAttended": true
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/lectures/6434b916ccd7ab2e508b2ac3/attendance/6434c0f21c684c5985ccaf70',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Attend lecture attendance student 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/student/courses/:id/lectures/:id/attendance/:id/attend`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Student attended successfully.",
    "data": {
      "attendance": {
        "id": "6434c0f21c684c5985ccaf70",
        "isAttended": true
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    randomAccessKey: 'lY4RWSzvxD',
    lat: '30.9977',
    lng: '29.7432',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/student/courses/6430e37e95394133234b0cdf/lectures/6434b916ccd7ab2e508b2ac3/attendance/6434c0f21c684c5985ccaf70/attend',
    {
      method: 'POST',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### CONTACTS ⭐

###### Show contact 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/contacts/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Contact updated successfully",
    "data": {
      "contact": {
        "phoneNumber": {
          "code": "20",
          "number": "1224440417"
        },
        "whatsapp": {
          "code": "20",
          "number": "1224440417"
        },
        "_id": "64339e899d30e909adbe56ca",
        "createdAt": "2023-04-10T05:28:41.012Z",
        "updatedAt": "2023-04-11T02:26:40.467Z",
        "__v": 0,
        "email": "hi@gmail.com",
        "facebook": "www.facebook.com",
        "twitter": "iammo26",
        "telegram": "iammo26"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    email: 'hi@gmail.com',
    phoneCode: '20',
    phoneNumber: '1224440417',
    facebookLink: 'www.facebook.com',
    twitterUsername: 'iammo26',
    whatsappCode: '20',
    WhatsappNumber: '1224440417',
    telegramUsername: 'iammo26',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/contacts/64339e899d30e909adbe56ca',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Update contact 📌

- _HTTP Method:_ `PATCH`
- _Endpoint URL:_ `api/v1/contacts/:id`
- _Headers:_ `Authorization`
- _Body:_
  ```json
  {
    "email": "hi@gmail.com",
    "phoneCode": "20",
    "phoneNumber": "1224440417",
    "facebookLink": "www.facebook.com",
    "twitterUsername": "iammo26",
    "whatsappCode": "20",
    "WhatsappNumber": "1224440417",
    "telegramUsername": "iammo26"
  }
  ```
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Contact updated successfully",
    "data": {
      "contact": {
        "phoneNumber": {
          "code": "20",
          "number": "1224440417"
        },
        "whatsapp": {
          "code": "20",
          "number": "1224440417"
        },
        "_id": "64339e899d30e909adbe56ca",
        "createdAt": "2023-04-10T05:28:41.012Z",
        "updatedAt": "2023-04-11T02:26:40.467Z",
        "__v": 0,
        "email": "hi@gmail.com",
        "facebook": "www.facebook.com",
        "twitter": "iammo26",
        "telegram": "iammo26"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjQzMzllODk5ZDMwZTkwOWFkYmU1NmNjIiwicm9sZSI6InN0dWRlbnQifSwiaWF0IjoxNjgxMTA0NzA0LCJleHAiOjE2ODM2OTY3MDR9.ov6EA3_jla0KlwXgRnx1LOKUfapQ6qbVqgFeSqGvZ2Q',
    'Content-Type': 'application/json',
  };

  let bodyContent = JSON.stringify({
    email: 'hi@gmail.com',
    phoneCode: '20',
    phoneNumber: '1224440417',
    facebookLink: 'www.facebook.com',
    twitterUsername: 'iammo26',
    whatsappCode: '20',
    WhatsappNumber: '1224440417',
    telegramUsername: 'iammo26',
  });

  let response = await fetch(
    'http://localhost:3000/api/v1/contacts/64339e899d30e909adbe56ca',
    {
      method: 'PATCH',
      body: bodyContent,
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

##### STORAGE ⭐

###### Upload storage 📌

- _HTTP Method:_ `POST`
- _Endpoint URL:_ `api/v1/storage/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Uploadable url generated successfully",
    "data": {
      "storage": {
        "_id": "6434be45b5d96421078c210a",
        "path": "courses/6430e37e95394133234b0cdf/lecture/6434b916ccd7ab2e508b2ac3/resources/c4e01461-414b-4f38-9c2f-a4b114ad4dc3.png",
        "type": "image/png",
        "name": "lecture 01 - resource",
        "owner": "6430c7854e29a1ff8375d1e7",
        "createdAt": "2023-04-11T01:56:21.752Z",
        "updatedAt": "2023-04-11T01:56:21.752Z",
        "__v": 0,
        "id": "6434be45b5d96421078c210a"
      },
      "uploadUrl": "https://unista-dev.s3.amazonaws.com/courses/6430e37e95394133234b0cdf/lecture/6434b916ccd7ab2e508b2ac3/resources/c4e01461-414b-4f38-9c2f-a4b114ad4dc3.png?Content-Type=image%2Fpng&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAZUKGZYJVW6D5G2HU%2F20230411%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20230411T015658Z&X-Amz-Expires=300&X-Amz-Signature=86e208064373f14210632d48731a419a6f6771291fd24a366673816d080ce92f&X-Amz-SignedHeaders=host",
      "accessUrl": "https://unista-dev.s3.amazonaws.com/courses/6430e37e95394133234b0cdf/lecture/6434b916ccd7ab2e508b2ac3/resources/c4e01461-414b-4f38-9c2f-a4b114ad4dc3.png?AWSAccessKeyId=AKIAZUKGZYJVW6D5G2HU&Expires=1681178518&Signature=7O4kzrVY1yNOz0CKi26zYqLBZLM%3D"
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjNlN2M0M2EwZTc4YmVkNzdiMGNhMzg1Iiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2Nzg5NTkzMjAsImV4cCI6MTY4MTU1MTMyMH0.kqKSNP7bBAyo2KtstKA7ESMqCmh0_4Csm6sdXy9k3-o',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/storage/6434be45b5d96421078c210a',
    {
      method: 'POST',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```

###### Access storage 📌

- _HTTP Method:_ `GET`
- _Endpoint URL:_ `api/v1/storage/:id`
- _Headers:_ `Authorization`
- _Body:_ `None`
- _Success Response:_ `200`

  ```json
  {
    "status": "success",
    "message": "Accessable url generated successfully",
    "data": {
      "url": "https://unista-dev.s3.amazonaws.com/courses/6430e37e95394133234b0cdf/assignments/6434ada7e7b70ce6c7e5d3cd/submissions/76941587-e0f8-495b-879f-af5941a1670b.png?AWSAccessKeyId=AKIAZUKGZYJVW6D5G2HU&Expires=1681174845&Signature=xKQ1DjxtU%2FW9OxuYQ7QVnwVzLnA%3D",
      "storage": {
        "_id": "6434aeec91da347928a86084",
        "path": "courses/6430e37e95394133234b0cdf/assignments/6434ada7e7b70ce6c7e5d3cd/submissions/76941587-e0f8-495b-879f-af5941a1670b.png",
        "type": "image/png",
        "name": "76941587-e0f8-495b-879f-af5941a1670b.png",
        "createdAt": "2023-04-11T00:50:52.021Z",
        "updatedAt": "2023-04-11T00:50:52.021Z",
        "__v": 0,
        "id": "6434aeec91da347928a86084"
      }
    }
  }
  ```

- _Example - JS_:

  ```js
  let headersList = {
    Accept: '*/*',
    Authorization:
      'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiNjNlN2M0M2EwZTc4YmVkNzdiMGNhMzg1Iiwicm9sZSI6Im1hc3RlciJ9LCJpYXQiOjE2Nzg5NTkzMjAsImV4cCI6MTY4MTU1MTMyMH0.kqKSNP7bBAyo2KtstKA7ESMqCmh0_4Csm6sdXy9k3-o',
  };

  let response = await fetch(
    'http://localhost:3000/api/v1/storage/6434aeec91da347928a86084',
    {
      method: 'GET',
      headers: headersList,
    }
  );

  let data = await response.text();
  console.log(data);
  ```
