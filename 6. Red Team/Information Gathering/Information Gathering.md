Abaixo estão alguns métodos e ferramentas para se utilizar com objetivo de encontrar informações valiosas de um serviço ou site para ajudar durante um Pentest
#### Ferramentas de senhas
Karma
> [https://github.com/jdiazmx/karma](https://github.com/jdiazmx/karma)

Pwndb
> [https://github.com/jxlil/pwndb](https://github.com/jxlil/pwndb)


#### Pastebin
Pode ser usado para buscar Leaks
[Pastebin.com - #1 paste tool since 2002!](https://pastebin.com)


#### Trello
Para buscar leaks de alguma empresa que estiver publico
[Gerencie os projetos do time em qualquer lugar | Trello](https://trello.com/pt-BR)


Podemos buscar usando google Hacking, por exemplo, se pesquisamos por

site:trello.com “[businesscorp.com.br](http://businesscorp.com.br)“
site:trello.com “senhas”


#### WaybackMachine
Para vermos versões antigas de um site e encontrar algo valioso, ou não
[Wayback Machine](http://web.archive.org)

---

---
#### BING
ip: “28.111.20.18”


#### GHDB
[OffSec’s Exploit Database Archive](https://www.exploit-db.com/google-hacking-database)






#### Dork Script
    
    ```bash
    #!/bin/bash
    SEARCH=”firefox”
    ALVO=”$1”
    
    echo “Pesquisa no Pastebin”
    $SEARCH "<https://google.com/search?q=site:pastebin.com+$ALVO>" 2>/dev/null
    
    echo “Pesquisa no Trello”
    $SEARCH "<https://google.com/search?q=site:trello.com+$ALVO>" 2>/dev/null
    
    echo “Pesquisa por arquivos”
    $SEARCH "<https://google.com/search?q=site:$ALVO+ext:php+OR+ext:txt>" 2>/dev/null
    
    ---
    chmod +x <script.sh>
    ./<script.sh> <site>
    ```
    

#### theHarvester
Script pra automação de coleta de informação


> $ theHarvester -d [businesscorp.com.br](http://businesscorp.com.br) -l 100 -b bing

*** Configurar a ferramenta na /etc/theHarvester/ adicionando as keys de busca ***

#### Metadados
Contem informações sobre o hardware ou software que foi gerado o documento


$ apt install exiftool
$ exiftool <arquivo>


