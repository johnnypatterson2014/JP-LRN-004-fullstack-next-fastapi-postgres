

python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt

run backend app:
uvicorn main:app --reload

http://127.0.0.1:8000/docs

---

install postgresSQL
admin password

run postgres windows app: pgAdmin

---

setup database:
 - alembic init alembic
 - alembic revision -m "create todos table"

connect to db in terminal:
psql -d tutorial
CREATE USER myuser WITH PASSWORD 'pass082724';
GRANT ALL PRIVILEGES ON DATABASE tutorial TO myuser;
GRANT ALL PRIVILEGES ON SCHEMA public TO myuser;
\q    // to quit

alembic upgrade head      // run the db migration

// verify in terminal:
psql tutorial
\dt
select * from todos
\q

