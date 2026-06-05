# voting-app-vote

Python frontend для голосування. Частина Docker Voting App.

## Сервіс

- Мова: Python (Flask)
- Порт: 80
- Залежності: Redis (черга голосів)

## Docker

```bash
docker build -t voting-app-vote .
docker run -p 8080:80 voting-app-vote
```

## Multi-arch збірка

```bash
docker buildx build --platform linux/amd64,linux/arm64 \
  -t <registry>/voting-app-vote:latest --push .
```
