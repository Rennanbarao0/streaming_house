# 🎬 Media Server Stack

## Visão Geral

Stack de servidor de mídia completo composto por:

- **Jellyfin** (porta 8096): Servidor de streaming de mídia para organizar e assistir filmes, séries e outros conteúdos
- **qBittorrent** (porta 8080): Cliente torrent com interface web para download de arquivos

Os downloads do qBittorrent são automaticamente disponibilizados no Jellyfin através do volume compartilhado `/downloads`.

## Requisitos

- Docker
- Docker Compose

## Como Executar

1. Clone ou baixe o projeto

2. Execute os containers:
```bash
docker-compose up -d
```

3. Acesse as interfaces:
   - **Jellyfin**: http://localhost:8096
   - **qBittorrent**: http://localhost:8080
     - Usuário padrão: `admin`
     - Senha padrão: `adminadmin`

4. Para parar os containers:
```bash
docker-compose down
```

## Estrutura de Pastas
```
.
├── config/          # Configurações dos serviços
├── cache/           # Cache do Jellyfin
└── downloads/       # Arquivos baixados (compartilhado entre os serviços)
```