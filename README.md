# LaravelRoom

## Descrição do Projeto
LaravelRoom é uma aplicação API para encontrar locais para alugar, desenvolvida com Laravel e Docker.

## Pré-requisitos
- Git
- Docker
- Docker Compose

## Clonando o Projeto
```bash
git clone https://github.com/rodrigocostarcs/laravelroom.git
cd laravelroom
```

## Configuração do Ambiente

### 1. Copiar Arquivo de Ambiente
```bash
cp .env.example .env
```

### 2. Construir e Iniciar Containers
```bash
docker-compose up -d --build
```

### 3. Instalar Dependências do Composer
```bash
docker-compose exec app composer install
```

### 4. Gerar Chave do Laravel
```bash
docker-compose exec app php artisan key:generate
```

### 5. Configurar Banco de Dados
```bash
# Criar tabelas
docker-compose exec app php artisan migrate

# (Opcional) Popular banco de dados
docker-compose exec app php artisan db:seed
```

## Acessando a Aplicação

### URL da Aplicação
- Acesse: `http://localhost`

### Acessar Container da Aplicação
```bash
docker-compose exec app bash
```

### Banco de Dados
- Host: `localhost`
- Porta: `3306`
- Database: `laravelroom`
- Usuário: `laravelroom`
- Senha: `laravelroom`

## Comandos Úteis

### Parar Containers
```bash
docker-compose down
```

### Reiniciar Containers
```bash
docker-compose restart
```

### Verificar Logs
```bash
# Logs de um serviço específico
docker-compose logs app

# Logs em tempo real
docker-compose logs -f app
```

## Desenvolvimento

### Rodar Testes
```bash
docker-compose exec app php artisan test
```

### Limpar Cache
```bash
docker-compose exec app php artisan config:clear
docker-compose exec app php artisan cache:clear
```

## Contribuição
1. Faça um fork do projeto
2. Crie sua feature branch (`git checkout -b feature/MinhaFeature`)
3. Commit suas mudanças (`git commit -m 'Adiciona MinhaFeature'`)
4. Push para a branch (`git push origin feature/MinhaFeature`)
5. Abra um Pull Request

## Licença
[Especificar a licença do projeto]

## Contato
Rodrigo Costa - [Seu email ou link do GitHub]
