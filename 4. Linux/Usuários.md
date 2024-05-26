
Diretório de usuários no Linux

```
/etc/passwd
```

<span style="color:#00b0f0">! Para o usuário ter acesso no sistema ele precisar ter o /bin/bash no passwd !</span>


Adicionando um usuário no sistema
$ sudo adduser <nome>


Deletando um usuário no sistema
$ sudo deluser<nome>

Adicionando com useradd, especificando diretorio e shell
$ useradd -d /opt/desec -s /bin/bash zillow


Para definir a nova senha do usuario
$passwd zillow

Para impersonar o usuario no sistema
$ su zillow

Sair do usuario
$ exit


Conceder permissões de adm a um usuário comum
adduser <user> <grupo>
$ adduser zillow sudo

Revogar permissoes de adm a um usuário comum
$ deluser zillow sudo

