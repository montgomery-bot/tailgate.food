# Database Setup

This project uses Drizzle ORM with PostgreSQL.

## Setup

1. Install dependencies:
   ```bash
   npm install
   ```

2. Copy environment variables:
   ```bash
   cp .env.example .env
   ```

3. Update `.env` with your database credentials.

4. Run migrations:
   ```bash
   npm run db:migrate
   ```

## Available Commands

- `npm run db:generate` - Generate migration files
- `npm run db:migrate` - Run migrations
- `npm run db:studio` - Open Drizzle Studio

## Schema

### Users Table

| Column        | Type         | Description          |
|---------------|--------------|----------------------|
| id            | serial       | Primary key          |
| email         | varchar(255) | Unique, not null     |
| name          | varchar(255) | Not null             |
| password_hash | varchar(255) | Hashed password      |
| created_at    | timestamp    | Auto-generated       |
| updated_at    | timestamp    | Auto-generated       |
