# computacao-em-nuvem-prova-1
index. html
# prova1 de computaçao em nuvem

nome: carine mesquita freitas
ra: fbf36d5fb8a75b9ea4b

##O que fiz
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
EOF

Subi uma página com mensagem "Treinamento ativo" em contêiner Docker nginx:alpine mapeado na porta 8083.


executei uma pagina web em um conteiner docker chamado treinamento usei a imagem nginnx:
docker run -d --name treinamento -p 8083:80 nginx:alpine
docker cp index.html treinamento:/usr/share/nginx/html/index.html
docker ps
curl http://localhost:8083


index.html - cole só o HTML de <!DOCTYPE html> até </html>README.md - use este modelo:
cat > index.html <<'EOF'
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
EOF

cat > index.html <<'EOF'
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
EOF

docker run -d --name treinamento -p 8083:80 nginx:alpine
docker cp index.html treinamento:/usr/share/nginx/html/index.html
docker ps
curl http://localhost:8083

## Explicação
A imagem nginx:alpine é o molde somente leitura. O contêiner treinamento é a instância em execução dela. O mapeamento 8083:80 liga a porta 80 do contêiner onde o Nginx escuta com a porta 8083 do host, permitindo acesso via localhost:8083.

