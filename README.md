# Infra Web Lab

Aplicacao web estatica servida pelo Apache HTTP Server em container Docker,
gerenciado pelo Docker Compose.

## Tecnologias
- Docker Engine
- Docker Compose
- Apache HTTP Server
- HTML5, CSS3 e JavaScript

## Executar

```bash
docker compose config
docker compose up -d
docker compose ps
curl -I http://localhost:8080
```

Abra http://localhost:8080 no navegador.

## Parar

```bash
docker compose down
```

## Decisoes tecnicas
- Porta 8080 do host mapeada para a porta 80 do container.
- Diretorio app montado em /usr/local/apache2/htdocs.
- Volume somente leitura (ro).
- Politica unless-stopped para reinicializacao automatica.
