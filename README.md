# Guide to Create or Update a Superuser in PocketBase (v0.23.3)

This guide explains how to create or update a superuser in PocketBase using the CLI. Specifically, this approach is useful if the token-based link shown during installation doesn't work, as it happened in my case with version `v0.23.3`.

---

## Prerequisites
- PocketBase installed and running.
- Access to PocketBase's CLI.
- If using Docker, ensure the container is running.

---

## Basic Command

Use the following command to create or update a superuser:

```
/app/pocketbase superuser upsert <email> <password>
```

### Example

To create a superuser with the email `admin@example.com` and the password `strong4a$$w0rd`, use:

```
/app/pocketbase superuser upsert admin@example.com strong4a$$w0rd
```

---

## Key Notes

1. **Email**:
   - Ensure the email address is valid.

2. **Secure Password**:
   - Use a strong password (at least 8 characters, mix of letters, numbers, and symbols).

3. **Database Location**:
   - If your database is not in the default location, specify the path using `--dir`:

     ```
     /app/pocketbase superuser upsert admin@example.com strong4a$$w0rd --dir /path/to/pb_data
     ```

4. **Docker**:
   - If running PocketBase in Docker, first access the container:
     
     ```
     docker exec -it <container_name> sh
     ```

     Then run the command inside the container.

---

## Why Use This Command?

During the installation of PocketBase v0.23.3, a launch link with a token is generated in the terminal. However, this link may not work properly (as was the case for me), making it necessary to use the CLI command above.

---

## Verification

To verify the superuser was successfully created or updated, log in with the credentials in the PocketBase admin interface.

---

That's it! You now have a working superuser. 🚀
