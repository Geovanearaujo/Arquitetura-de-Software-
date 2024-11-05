# Arquitetura-de-Software-

Sistema de Gerenciamento de Aeroportos
Descrição do Projeto
Este projeto é uma API RESTful desenvolvida para o gerenciamento de aeroportos, voos, usuários e reservas. Ele oferece endpoints seguros para operações CRUD e autenticação de usuários, permitindo fácil integração com outras aplicações. A API foi construída usando Flask como framework principal, PostgreSQL como banco de dados para persistência e está completamente contêinerizada com Docker e Docker Compose para garantir a consistência e portabilidade do ambiente.

Principais Funcionalidades
Gerenciamento de Usuários: Endpoints para cadastro, listagem, atualização e remoção de usuários, com autenticação integrada.
Aeroportos e Voos: CRUD completo para aeroportos e voos, incluindo gerenciamento de informações como destino, companhia aérea, capacidade e ocupação de voos.
Sistema de Reservas: Possibilidade de criar e gerenciar reservas de voos, vinculando-as a usuários e gerando e-tickets.
Autenticação e Sessão: Login e logout de usuários com gerenciamento de sessões para proteger endpoints específicos.
Estrutura de Arquivos
app.py: Ponto de entrada da aplicação, inicializando o servidor Flask e configurando rotas e autenticação.
routes.py: Define todas as rotas e lógica de negócios, incluindo operações CRUD e autenticação.
database.py: Configura a conexão e as operações com o banco de dados PostgreSQL, utilizando SQLAlchemy para gerenciar as transações.
Dockerfile: Configura o ambiente Docker para a aplicação, instalando dependências e definindo o ambiente Flask.
docker-compose.yml: Orquestra os serviços da aplicação, incluindo o container do banco de dados e o da API.
requirements.txt: Lista todas as bibliotecas necessárias para execução da aplicação.
Tecnologias Utilizadas
Flask e Flask-Login: Framework web para a API e autenticação de usuários.
PostgreSQL: Banco de dados relacional para armazenamento persistente.
SQLAlchemy: ORM para manipulação de dados.
Docker e Docker Compose: Para contêinerizar a aplicação e gerenciar a rede entre os serviços.
Como Executar
Clonar o Repositório:

bash
Copiar código
git clone https://github.com/seu_usuario/sistema-de-gerenciamento-aeroportos.git
cd sistema-de-gerenciamento-aeroportos
Configurar o Ambiente: Certifique-se de que o Docker e o Docker Compose estão instalados.

Executar com Docker Compose:

bash
Copiar código
docker-compose up -d --build
Testar a API: A API estará disponível em http://localhost:5000. Utilize ferramentas como curl ou Postman para testar os endpoints.

Exemplos de Comandos curl
Cadastrar Usuário:
bash
Copiar código
curl -X POST -H "Content-Type: application/json" -d '{"nome":"Geovane","email":"geovane@example.com","senha":"1234"}' http://localhost:5000/cadastro
Listar Voos:
bash
Copiar código
curl http://localhost:5000/voo
Licença
Este projeto é distribuído sob a licença MIT. Consulte o arquivo LICENSE para obter mais informações.



