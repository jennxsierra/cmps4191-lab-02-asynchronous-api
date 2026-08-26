# CMPS4191 Laboratory 2

## Measuring an Aynchronous Report API

| Key               | Value                                                                                              |
| ----------------- | -------------------------------------------------------------------------------------------------- |
| **Student Name**  | [Andres Hung](https://github.com/andreshungbz) & [Jennessa Sierra](https://github.com/jennxsierra) |
| **Student Email** | 2018118240@ub.edu.bz & 2021153908@ub.edu.bz                                                        |
| **Course**        | CMPS4191 - Advanced Web Technologies                                                               |
| **Due Date**      | August 28, 2026                                                                                    |

## Running the Application

### Docker Compose

```
docker compose up
```

### Manual Method

#### Prerequisites

- curl
- go
- golang-migrate
- make
- PostgreSQL

#### Database Setup

```
CREATE ROLE gatekeeper WITH LOGIN PASSWORD 'password';
CREATE DATABASE gatekeeper;
ALTER DATABASE gatekeeper OWNER TO gatekeeper;
```

#### Application Setup

```
cp .envrc.example .envrc
make db/migrations/up
make run
```

#### Make Script Executable and Run It

```
chmod +x measure_async.sh
./measure_async.sh
```
