# Environment Variables Documentation

This document lists all environment variables used across the different services and configuration files.

---

### 🛡️ Watchtower Service

| Variable              | Required | Default Value | Description                                             |
|-----------------------|----------|---------------|---------------------------------------------------------|
| `WATCHTOWER_SCHEDULE` | ❌ No     | `0 0 4 * * *` | Cron expression defining update schedule for containers |

---

### 🗄️ Database Service

| Variable            | Required | Default Value | Description                  |
|---------------------|----------|---------------|------------------------------|
| `POSTGRES_USER`     | ✅ Yes    | –             | PostgreSQL database username |
| `POSTGRES_PASSWORD` | ✅ Yes    | –             | PostgreSQL database password |
| `POSTGRES_DB`       | ✅ Yes    | –             | PostgreSQL database name     |

---

### ⚙️ API Service

| Variable                          | Required | Default Value         | Description                                                      |
|-----------------------------------|----------|-----------------------|------------------------------------------------------------------|
| `POSTGRES_USER`                   | ✅ Yes    | –                     | PostgreSQL database username                                     |
| `POSTGRES_PASSWORD`               | ✅ Yes    | –                     | PostgreSQL database password                                     |
| `POSTGRES_DB`                     | ✅ Yes    | –                     | PostgreSQL database name                                         |
| `POSTGRES_URL`                    | ❌ No     | `hopital-db`          | Hostname or URL of the PostgreSQL server                         |
| `POSTGRES_PORT`                   | ❌ No     | `5432`                | PostgreSQL server port                                           |
| `APPLICATION_URL`                 | ✅ Yes    | –                     | Base URL of the web application                                  |
| `MAIL_SMTP_HOST`                  | ✅ Yes    | –                     | SMTP server hostname                                             |
| `MAIL_SMTP_PORT`                  | ✅ Yes    | –                     | SMTP server port                                                 |
| `MAIL_ADDRESS_FROM`               | ✅ Yes    | –                     | Email address used in the "From" field of outgoing emails        |
| `MAIL_ADDRESS_SUPPORT`            | ❌ No     | `support@hnfc.fr`     | Support email address                                            |
| `MAIL_SMTP_AUTH`                  | ❌ No     | `False`               | Whether SMTP authentication is enabled (`True` or `False`)       |
| `MAIL_SMTP_USER`                  | ❌ No     | –                     | SMTP username (if authentication is enabled)                     |
| `MAIL_SMTP_PASSWORD`              | ❌ No     | –                     | SMTP password (if authentication is enabled)                     |
| `MAIL_SMTP_STARTTTLS_ENABLE`      | ❌ No     | `False`               | Whether to enable STARTTLS (`True` or `False`)                   |
| `MAIL_SMTP_STARTTTLS_REQUIRED`    | ❌ No     | `False`               | Whether STARTTLS is required (`True` or `False`)                 |
| `HOPITAL_VERSION`                 | ✅ Yes    | –                     | Deployment type: either `deploy` or `staging`                    |
| `PRE_SUBJECT_TITLE`               | ❌ No     | `Suivi de la douleur` | First part of the object for all the email sent                  |
| `PASSWORD_RESET_TOKEN_EXPIRATION` | ❌ No     | `15`                  | Period of expiration of the token for password reset (in minute) |
