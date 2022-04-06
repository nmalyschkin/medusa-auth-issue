# Authentication Cookie bug

When set to production the set-cookie header is missing when trying to login.

## steps to reproduce

```sh
docker-compose up --build -d
docker-compose exec backend bash
# inside the container
medusa seed -f data/seed.json
exit
# outside the container
```

Credentials:

- email: "admin@medusa-test.com"
- password: "supersecret"
