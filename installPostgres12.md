# Pré-requisitos

Para acompanhar este tutorial, você precisará de um servidor Ubuntu 20.04 que foi configurado seguindo nosso guia Configuração inicial do servidor para Ubuntu 20.04 .

Depois de concluir este tutorial de pré-requisito, seu servidor deve ter um usuário não root com permissões sudo e um firewall básico.

## Etapa 1 - Instalação do PostgreSQL

Para instalar o PostgreSQL, primeiro atualize o índice de pacote local do seu servidor:

digite-> sudo apt update

Em seguida, instale o pacote Postgres junto com um -contribpacote que adiciona alguns utilitários e funcionalidades adicionais:

digite -> sudo apt install postgresql postgresql-contrib

## Etapa 2 - Uso de funções e bancos de dados PostgreSQL

Por padrão, o Postgres usa um conceito chamado “funções” para lidar com a autenticação e autorização. Estes são, em alguns aspectos, semelhantes aos usuários e 

grupos regulares do estilo Unix.

Após a instalação, o Postgres é configurado para usar autenticação ident , o que significa que associa funções do Postgres a uma conta de sistema Unix / Linux 

correspondente. Se houver uma função no Postgres, um nome de usuário Unix / Linux com o mesmo nome é capaz de entrar como essa função.

O procedimento de instalação criou uma conta de usuário chamada postgres que está associada à função Postgres padrão. Existem algumas maneiras de utilizar 

essa conta para acessar o Postgres. Uma maneira é mudar para a conta postgres em seu servidor digitando:

