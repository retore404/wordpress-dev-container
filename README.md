# wordpress-dev-container
WordPressのTheme開発のための環境

## 起動

docker compose up -d

## 管理ページ

- http://localhost:8000/wp-admin/about.php

## PHP Code Sniffer

### 初回のみ

```
docker-compose run composer composer require wp-coding-standards/wpcs
docker-compose run composer ./vendor/bin/phpcs --config-set installed_paths /app/vendor/wp-coding-standards/wpcs
```

### コード静的解析

```
docker-compose run composer ./vendor/bin/phpcs --standard=WordPress /code/${ThemeName}/*
```
