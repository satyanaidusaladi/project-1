# Smart Library Management System

React + Node/Express + MySQL + Python Flask + Java Spring Boot.

Roles: ADMIN, TEACHER, STUDENT.
Storage: MySQL BLOB for book covers/documents.
No multi-branch support.

Default admin:
Username: Naidu
Password: 1234

Seed users: Naidu (ADMIN), Ravi (STUDENT), Priya (STUDENT), Kumar (TEACHER).
Seed books: 10 coding books.

## Start
1. Run database/schema.sql then database/seed.sql in MySQL.
2. In backend: copy .env.example .env, edit MySQL password, run `npm install` then `npm run dev`.
3. In frontend: run `npm install` then `npm run dev`.
4. In python-service: create venv, install requirements, run app.py.
5. In java-service: `mvn spring-boot:run`.

See docs/GITHUB_STEPS.md.

## Book details
Each of the 10 coding books now has detailed metadata: summary, description, topics, language, page count and publication year. Click a book card in the React UI to open its full details.

If you already created the original database, run `database/update_book_details.sql` once. If creating the database from scratch, use the updated `schema.sql` and `seed.sql`.


## Book Reader
Each seeded coding book includes a 10-page original study guide. Click a book, choose **Read 10-page guide**, and use Previous/Next to read page by page. The reader content is original educational material and is not a reproduction of copyrighted books.

For an existing database, run `database/update_book_details.sql` if needed, then run `database/book_reader.sql`. For a fresh database, `schema.sql` and `seed.sql` create the reader table and seed the 100 study-guide pages.
