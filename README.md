# JP-LRN-004-fullstack-next-fastapi-postgres

## -------------------------------------------------------------------------------
## backend

```
// create virtual env
python -m venv .venv

// activate virtual env
.venv\Scripts\activate

// install dependencies
pip install -r requirements.txt

// run the backend server (for local dev)
uvicorn main:app --reload

// in the cloud, use this instead:
uvicorn main:app --host 0.0.0.0 --port 8000

// view on localhost
http://127.0.0.1:8000/docs
```

## -------------------------------------------------------------------------------
## database
```
install postgresSQL

// setup alembic
alembic init alembic
alembic revision -m "create todos table"

// connect to db in terminal
psql -d tutorial
CREATE USER myuser WITH PASSWORD 'pass082724';
GRANT ALL PRIVILEGES ON DATABASE tutorial TO myuser;
GRANT ALL PRIVILEGES ON SCHEMA public TO myuser;
\q    // to quit

// run the db migration
alembic upgrade head

// verify in terminal:
psql tutorial
\dt
select * from todos
\q
```

Render.com postgres settings: see .env file


## -------------------------------------------------------------------------------
## frontend
```
// install
npm ci

// run server
npm run dev

// view on localhost
http://localhost:3000

// deployed to vercel
https://jp-lrn-004-vercel.vercel.app/

```