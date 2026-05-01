# Global Banking & Transaction Settlement System - Backend (ES Modules)

## Setup

1. Copy `.env.example` to `.env` and fill in values.
2. Run `docker-compose up -d` to start PostgreSQL and Redis.
3. Run `npm install`
4. Run `npx prisma migrate dev --name init`
5. Run `npm run dev`

## API Endpoints

- `POST /api/v1/auth/register` - Register user
- `POST /api/v1/auth/login` - Login
- `POST /api/v1/transfer` - Transfer funds (requires idempotency-key header)
- `GET /api/v1/account/verify/:account_id` - Verify account
- `POST /api/v1/interest/applyInterest` - Apply interest
- `GET /api/v1/statement/statement` - Get statement

All endpoints require Bearer token except auth routes.
