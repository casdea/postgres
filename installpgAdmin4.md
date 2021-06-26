#
# Configure o repositório
#

# Instale a chave pública para o repositório (se não tiver feito anteriormente):
sudo curl https://www.pgadmin.org/static/packages_pgadmin_org.pub | sudo apt-key add

# Crie o arquivo de configuração do repositório:
sudo sh -c 'echo "deb https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/$(lsb_release -cs) pgadmin4 main"> /etc/apt/sources.list.d/pgadmin4.list && apt update '

#
# Install pgAdmin
#

# Instale para os modos desktop e web:
sudo apt install pgadmin4

# Instalar apenas no modo desktop:
sudo apt install pgadmin4-desktop

# Instale apenas para o modo web: 
sudo apt install pgadmin4-web 

# Configure o servidor da web, se você instalou pgadmin4-web:
sudo /usr/pgadmin4/bin/setup-web.sh
