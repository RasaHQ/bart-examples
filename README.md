# bart-examples
Bot demoing e2e tests, tracing and metrics

## Requirements
Create .env file based on example.env

1. Run the project:
```bash
docker compose up -d
```

2. Exec into the rasa container and run tests
```bash
rasa test e2e e2e_tests/happy_paths/user_adds_contact_to_their_list.yml
```

3. check jaeger and prometheus dashboards
```yaml
http://localhost:16686/
http://localhost:9090/

```

4. Rasa inspect is available at:
```yaml
http://localhost:5005/webhooks/inspector/inspect.html
```