##### Traceroute
Usamos o traceroute para verificar se um pacote está chegando ao alvo/host final. 
Por padrão o traceroute funciona com protocolo UDP


> $ traceroute businnesscorp.com.br

Quando o pacote demora mais de 3segs para responder, o traceroute vai nos trazer um * 
Possivelmente se o host não aceitar o protocolo UDP , irá ser mostrado * * *   


-w : Escolher o tempo de resposta para receber os pacotes
> $ traceroute businnesscorp.com.br -w 5


-m : Falar quantos hops vamos querer, até onde chegar na rota
> $ traceroute businnesscorp.com.br -m 10

-f : Para definir a partir de onde a rota irá começar
> $ traceroute businnesscorp.com.br -m 20 -f 15

-A : Exibe os AS das rotas (AS92304)
> $ traceroute businnesscorp.com.br -A

-I : Utiliza ICMP ao invés de UDP para chegar ao alvo
> $ traceroute businnesscorp.com.br -I

----

##### Firewall

##### Firewall

##### Firewall



# (#) 201 