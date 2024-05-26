No Linux, a maioria das entidades do sistema são tratadas como arquivos. Para organizar o sistema e impor limites dentro do computador, o Linux usa permissões de arquivo. As permissões de arquivo são incorporadas à estrutura do sistema de arquivos e fornecem um mecanismo para definir permissões em cada arquivo. Cada arquivo no Linux carrega suas permissões de arquivo, que definem as ações que o proprietário, o grupo e outros podem executar com o arquivo. Os direitos de permissão possíveis são Ler, Gravar e Executar. O comando ls com o parâmetro -l lista informações adicionais sobre o arquivo.

```

[analyst@secOps ~]$ ls -l space.txt
-rwxrw-r-- 1 analyst staff 253 May 20 12:49 space.txt
     (1)  (2)  (3)    (4)  (5)     (6)         (7)
```

A saída fornece muitas informações sobre o arquivo space.txt.

O primeiro campo da saída exibe as permissões associadas a **space.txt (-rwxrw-r--).** As permissões de arquivo são sempre exibidas na ordem Usuário, Grupo e Outro.

O arquivo **space.txt** tem as seguintes permissões:

- O traço (-) significa que este é um arquivo. Para diretórios, o primeiro traço seria um “d”.
- O primeiro conjunto de caracteres é para permissão de usuário (**rwx**). O usuário, **analista**, que possui o arquivo pode **R**ead, **W**rite e e**X**ecute o arquivo.
- O segundo conjunto de caracteres é para permissões de grupo(**rw-**). O grupo, **staff**, que possui o arquivo pode **R**ead e **W**rite no arquivo.
- O terceiro conjunto de caracteres é para quaisquer outras permissões de usuário ou grupo (**r--**). Qualquer outro usuário ou grupo no computador pode apenas ler o arquivo.

O segundo campo define o número de links rígidos para o arquivo (o número 1 após as permissões). Um link rígido cria outro arquivo com um nome diferente vinculado ao mesmo lugar no sistema de arquivos (chamado de inode). Isso está em contraste com um link simbólico, que é discutido na próxima página.

O 3 e 4 campo exibem o usuário (**analista**) e o grupo (**staff**) que possui o arquivo, respectivamente.
O 5 campo exibe o tamanho do arquivo em bytes. O arquivo **space.txt** tem 253 bytes.
O 6 campo exibe a data e hora da última modificação.
O 7 campo exibe o nome do arquivo.

![[Pasted image 20240314212934.png]]