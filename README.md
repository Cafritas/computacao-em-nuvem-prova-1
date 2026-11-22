# Prova 1 - Computação em Nuvem

**Aluna:** Carine Mesquita Freitas

## O que foi feito

Subi uma página com a mensagem "Treinamento ativo" em um contêiner Docker, usando a imagem nginx:alpine, mapeado na porta 8083.

## Arquivo index.html

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<title>Treinamento</title>
</head>
<body>
<h1>Treinamento ativo</h1>
</body>
</html>
```

## Comandos executados

```bash
docker run -d --name treinamento -p 8083:80 nginx:alpine
docker cp index.html treinamento:/usr/share/nginx/html/index.html
docker ps
curl http://localhost:8083
```

## Explicação

A imagem nginx:alpine é o molde somente leitura. O contêiner treinamento é a instância em execução dela. O mapeamento 8083:80 liga a porta 80 do contêiner, onde o Nginx escuta, com a porta 8083 do host, permitindo acesso via localhost:8083.
