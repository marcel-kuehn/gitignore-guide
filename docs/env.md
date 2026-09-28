# .env file(s)

A `.env` file is a plain text file that stores environment variables for a project, usually configuration values and secrets like API keys, database passwords, and service URLs. Each line holds one variable in a `KEY=value` format, for example `DATABASE_URL=postgres://localhost:5432/mydb` or `API_KEY=abc123`.

Applications load these values at startup, typically through a library such as [dotenv](https://github.com/motdotla/dotenv), so the code can read them without hardcoding sensitive or environment-specific values. This makes it easy to use different settings for development, testing, and production by swapping out the file rather than changing the code.

## Variations

Many projects use variations of the `.env` file, such as `.env.local`, `.env.development`, `.env.test` and `.env.production`, to keep separate settings for different environments or for personal overrides.

## Should it be included in the .gitignore?

Yes. Because `.env` files often contain secrets, they should not be committed to version control. The same applies to their variants, which usually contain secrets or machine-specific values too.

Instead, commit a `.env.example` file that lists the required variable names with placeholder values, so other developers know what to set up.

### Exceptions

Some frameworks, such as Next.js and Vite, are designed to commit `.env`, `.env.development`, and `.env.production` with non-secret default values, and only ignore local overrides (`.env*.local`). If your framework follows this convention, adjust the snippet accordingly and make sure no secrets end up in the committed files.

## Snippet

```
# Environments and Secrets
.env
.env.*
!.env.example
```
​