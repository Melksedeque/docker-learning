# Meu Projeto com NGINX e Docker

Este é um projeto simples que utiliza o servidor web NGINX para servir uma aplicação estática. O projeto inclui suporte para temas claro e escuro, com base nas preferências do usuário ou do sistema operacional.

## Estrutura do Projeto

```plaintext
docker-learning/
├── meu_projeto/                # Arqivos do Projeto Estático
|   ├── img/                    # Imagens
|   |   ├── docker-dark.svg     # Logo do Docker para o tema escuro
|   |   └── docker-light.svg    # Logo do Docker para o tema claro
|   ├── js/                     # Scripts
|   |   └── script.js           # Script de validação do tema do OS
|   └── index.html              # Estrutura HTML do projeto
├── compose.yml                 # Configuração com Docker Compose
├── Dockerfile                  # Dockerflie com NGINX
├── LICENSE                     # Arquivo de Licença MIT
└── README.md                   # Readme do projeto
```

- `index.html`: Página principal do projeto.
- `script.js`: Script para alternar entre os temas claro e escuro.
- `Dockerfile`: Configuração para criar a imagem Docker com NGINX.
- `compose.yml`: Arquivo de configuração do Docker Compose.

## Pré-requisitos

- [Docker](https://www.docker.com)
- [Docker Compose](https://docs.docker.com/compose/)

## Como Executar o Projeto

1. Construa e inicie o container com o Docker Compose:
   No terminal, execute o seguinte comando na raiz do projeto:
   ```sh
   docker-compose up --build
   ```
2. Acesse o projeto no navegador:
   Após iniciar o container, o projeto estará disponível no endereço:
   ```
   http://localhost:8081
   ```

## Funcionalidades

- **Tema Claro/Escuro:** O projeto detecta automaticamente a preferência de tema do sistema operacional ou permite que o usuário altere manualmente o tema.
- **Servido com NGINX:** O conteúdo estático é servido por um servidor NGINX configurado no container Docker.

## Estrutura do Docker

- O arquivo Dockerfile copia o conteúdo da pasta meu_projeto para o diretório padrão do NGINX (/usr/share/nginx/html).
- O arquivo compose.yml expõe a porta 8081 do host para a porta 80 do container.

## Comandos Úteis

- Parar os containers:
  ```sh
  docker-compose down
  ```
- Recriar os containers sem cache:
  ```sh
  docker-compose up --build --no-cache
  ```
- Verificar os logs do container:
  ```sh
  docker-compose logs -f
  ```

## Licença

Este projeto está licenciado sob a Licença MIT. Veja o arquivo [LICENSE](https://github.com/Melksedeque/docker-learning?tab=MIT-1-ov-file) para mais detalhes.

## Autor

- GitHub - [Melksedeque Silva](https://github.com/Melksedeque/)
- FrontEndMentor - [@Melksedeque](https://www.frontendmentor.io/profile/Melksedeque)
- Twitter / X - [@SouzaMelk](https://x.com/SouzaMelk)
- LinkedIn - [Melksedeque Silva](https://www.linkedin.com/in/melksedeque-silva/)
