# CRUD DE ESCOLAS

Aplicação Web do tipo monolitica criada com:
- PHP para o backend ^7.4
- HTML, CSS e Javascript pro frontend
- MySQL/MariaDB para o banco de dados

## Funcionalidades
- CRUD de Alunos
- CRUD de Professores
- CRUD de Cursos
- CRUD de Categorias
- CRUD de Usuários


## Passo a passo para rodar o projeto 
- Certifique-se que seu computador tem od softwares
 - PHP
 - MySQL ou MariaDB
 - Editor de texto (Por exemplo VS Code)
 - navegador Web
 - Composer (Gerenciador de pacotes do PHP)

### Clone o projeto
Baixe ou faça o clone do repositório:
`git clone ....`

Após isso, entre no diretório que foi gerado
`cd crud-php-oo`

#### Habilitar as extensões do PHP
Abra o deretório de instalação de PHP, encontre o arquivo *php.ini-production*, renomeie-o para **php.ini** e abra-o com algum tipo de editor de texto.

encontre as seguintes linhas e descomente-as, removendo ; que precede a linha.

- pdo_mysql
- curl
- mb_string
- openssl

#### Instalar as dependencias
Dentro do diretório da aplicação execute no terminal:

`composer install`

Certifique-se que um chamado **/vendor** foi criado.

### Banco de Dados

O banco de dados é o tipo relacional e contem as tabelas com até 2 níveis de normatização.

...
#### Criando o banco de dados
```sql
CREATE DATABASE db_escola
```

#### Migrar a estrutura do banco de dados
Ainda dentro do cliente de banco de dados, copie e cole o conteúdo do arquivo
**db.sql** e execute.

Certifique-se que as tabelas foram criadas, executando o conteudo:

```sql
SHOW TABLES;
```

Se o resultado for a lista de tables existentes, então pronto!


#### Configure  as credenciais de acesso
Encontre o arquivo **/config/database.php** e edite-o conforme as credenciais do seu usuário do banco de dados.

### Crie o primeiro usuário de acesso
Dentro de diretório da aplicação, execute no terminal o comando
`php config/create-admin.php`

Isso criará um usuário com as credenciais:
|Nome|Email|Senha|
|  - |  -  |  -  |
|Administrador| admin@admin.com | 123456 |

### Executando a aplicação
Para executaar e testar a aplicação, dentro do terminal execute:
`php -S localhost:8000 -t public`

Agora acesse o endereço http://localhost:8000 em seu navegador
