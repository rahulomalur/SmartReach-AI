# SmartReach-AI Backend

## Deployment

This backend is configured to deploy on Railway.

### Environment Variables Required

Set the following environment variables in Railway:

```
# Database (auto-set by Railway if using PostgreSQL add-on)
DATABASE_URL=postgresql://...

# Django Settings
SECRET_KEY=your-django-secret-key
DEBUG=False
ALLOWED_HOSTS=your-railway-domain.railway.app

# Google OAuth
GOOGLE_OAUTH2_CLIENT_ID=your-google-client-id
GOOGLE_OAUTH2_CLIENT_SECRET=your-google-client-secret

# Database Settings (if not using DATABASE_URL)
DB_HOST=your-db-host
DB_USER=your-db-user
DB_PASSWORD=your-db-password
DB_NAME=your-db-name
DB_PORT=5432

# Test Database
TEST_DB_HOST=your-test-db-host
TEST_DB_USER=your-test-db-user
TEST_DB_PASSWORD=your-test-db-password
TEST_DB_NAME=your-test-db-name
TEST_DB_PORT=5432

# Email
SMARTREACH_EMAIL_PASSWORD=your-email-password

# Redis (auto-set by Railway if using Redis add-on)
REDIS_URL=redis://...

# Frontend URL (for CORS)
FRONTEND_URL=https://frontend-azure-iota-20.vercel.app
```

### Local Development

1. Copy `oauth_settings.example.py` to `oauth_settings.py` and fill in your credentials
2. Run `pip install -r requirements.txt`
3. Run `python manage.py migrate`
4. Run `python manage.py runserver`
