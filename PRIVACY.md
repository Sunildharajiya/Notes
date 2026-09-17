# Privacy Notes

This repository contains educational notes and example code. Please follow these practices when adding personal or project data.

## Do not commit sensitive information

Never add the following to notes, source files, screenshots, or examples:

- Passwords, API keys, access tokens, or private keys
- Personal identification numbers or financial information
- Private email addresses, phone numbers, or home addresses
- Confidential company, customer, or classroom data
- Database connection strings or production configuration

Use placeholders such as `YOUR_API_KEY`, `example@email.com`, and `https://example.com` instead.

## Safer example code

```text
API_KEY = read_from_environment("API_KEY")
```

Keep real secrets in environment variables or a trusted secret manager. Do not place them directly in Markdown files or commit them to Git.

## If a secret is committed accidentally

1. Revoke or rotate the secret immediately.
2. Remove it from the current file and commit the safe replacement.
3. Check repository history and remove the secret from history if necessary.
4. Review access logs and notify the affected owner.

Deleting a secret from the latest commit does not make an exposed credential safe; assume it may already have been copied.

## Privacy checklist

- Use fictional data in examples.
- Share only the minimum information needed.
- Review screenshots for visible tokens and personal details.
- Keep dependencies and tools updated.
- Use a `.gitignore` file for local environment files such as `.env`.
- Check repository visibility before adding content.

These notes are general educational guidance and are not a substitute for legal or organizational privacy requirements.
