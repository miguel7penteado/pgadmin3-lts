
Introdução
------------

pgAdmin3 é uma administração de código aberto popular e rica em recursos e
plataforma de desenvolvimento para PostgreSQL, o banco de dados Open Source mais avançado do mundo.
o mundo.

O pgAdmin3 foi projetado para atender às necessidades de todos os usuários, desde escrever simples
Consultas SQL para desenvolvimento de bancos de dados complexos. A interface gráfica suporta
todos os recursos do PostgreSQL e facilita a administração. O aplicativo também
inclui um editor SQL de realce de sintaxe, um editor de código do lado do servidor, um
Agente de agendamento de tarefas SQL/batch/shell, suporte para replicação Slony-I
motor e muito mais. A conexão do servidor pode ser feita usando TCP/IP ou Domínio Unix
Sockets (em plataformas *nix) e podem ser criptografados em SSL para segurança. Não
drivers adicionais são necessários para se comunicar com o servidor de banco de dados.

pgAdmin3 é um software livre lançado sob a licença PostgreSQL.

**# As mudanças do Postgres até a versão 15 #**

O código foi alterado para adaptar as alterações internas do PostgreSQL até a versão 15.2:
- Não tem mais relhasoids em pg_class.
- Não tem mais cache_value, is_cycled, is_called no objeto de sequência (desde PostgreSQL 11).
- Não tem mais adsrc em pg_attrdef, ele deve ser calculado como pg_catalog.pg_get_expr(adbin, adrelid) em vez disso.
- DDL de particionamento de tabela declarativa.
- Não tem mais datlastsysoid em pg_database.

Se você está com preguiça de ler as instruções em [INSTALL](./INSTALL), faça isso Debian/Ubuntu/Mint modo instalação manual:
------------------------
```bash
# apt-get install chrpath libwxgtk-gl3.2-1 libwxgtk-media3.2-1 libwxgtk-media3.2-dev libwxgtk-webview3.2-1 libwxgtk-webview3.2-dev libwxgtk3.2-1 libwxgtk3.2-dev wx3.2-doc devscripts libxml2 libxml2-dev libxml2-utils libxml2-doc libxslt1.1 libxslt1-dev libgcrypt20 libgcrypt20-dev libgcrypt20-doc libssh2-1 libssh2-1-dev python3-sphinx python3-sphinxcontrib.htmlhelp

# apt-get install libssh2-1 libssh2-1-dev libgcrypt20 libgcrypt20-dev libjson-perl libpq-dev #postgresql-15 postgresql-contrib-15 postgresql-client-15

#Debian
# systemctl restart postgresql || true

#Devuan
# service postgresql restart

$ bash bootstrap
$ ./configure --prefix=/opt/pgadmin3bigsql --with-libgcrypt --with-wx-version=3.0  CFLAGS=-fPIC CXXFLAGS=-fPIC #--with-pgsql=/usr/lib/postgresql/15 --without-sphinx-build
$ make -j8
$ sudo make install
```


Criação de Pacotes Debian/Ubuntu/Mint modo instalação manual:
------------------------
```bash
# apt-get install chrpath libwxgtk-gl3.2-1 libwxgtk-media3.2-1 libwxgtk-media3.2-dev libwxgtk-webview3.2-1 libwxgtk-webview3.2-dev libwxgtk3.2-1 libwxgtk3.2-dev wx3.2-doc devscripts libxml2 libxml2-dev libxml2-utils libxml2-doc libxslt1.1 libxslt1-dev libgcrypt20 libgcrypt20-dev libgcrypt20-doc libssh2-1 libssh2-1-dev python3-sphinx python3-sphinxcontrib.htmlhelp

# apt-get install libssh2-1 libssh2-1-dev libgcrypt20 libgcrypt20-dev libjson-perl libpq-dev #postgresql-15 postgresql-contrib-15 postgresql-client-15

#Debian
# systemctl restart postgresql || true

#Devuan
# service postgresql restart

mkdir -p /tmp/1

cd /tmp/1

git clone https://github.com/miguel7penteado/pgadmin3-lts

cd pgadmin3-lts

sudo mk-build-deps -i

dpkg-buildpackage -us -uc

cd ..

dpkg -i pgadmin3_1.22.2-5_amd64.deb pgadmin3-data_1.22.2-5_all.deb pgadmin3-dbgsym_1.22.2-5_amd64.deb

pgadmin3

```




for Centos/RedHat:
------------------------
```
yum install wxGTK3 wxGTK3-devel
yum install libssh2 libssh2-devel libxml2 libxml2-devel libxslt libxslt-devel openssl-devel #postgresql15 postgresql15-devel postgresql15-libs

$ bash bootstrap
$ ./configure --prefix=/opt/pgadmin3bigsql --with-wx-version=3.0  CFLAGS=-fPIC CXXFLAGS=-fPIC --with-pgsql=/usr/pgsql-15 --without-sphinx-build
$ make -j8
$ sudo make install
```
