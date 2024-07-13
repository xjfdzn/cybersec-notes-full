### Introdução

A maioria dos protocolos de rede são compostos por um cabeçalho e uma área de dados

Header
> Cada header tem uma estrutura especifica

Payload
> Contem as informações que o protocolo carrega (dados), um payload pode também carregar dentro dele outro protocolo

![[Pasted image 20240217214858.png]]

----

#### Estrutura do Protocolo Ethernet

![[Pasted image 20240217214936.png]]

Mac de destino → Mac Address da placa de rede de destino
Mac de origem → Mac Address da placa de rede de origem
Tipo                  → Codigo do tipo do protocolo (0800 = IP) ↔ (0806 = ARP)
Payload             → Dados a serem transportados (ARP/IP)
Checksum         → Verificação de erros
Broadcast (ff:ff:ff:ff:ff) → Mensagem para todos os hosts da rede

----
#### ARP 

Tem a habilidade de descobrir qual endereço MAC está associado a um determinado IP
- Utiliza ARP Request e ARP Reply
Para o servidor enviar uma resposta de uma request ele precisa conhecer o Mac Address do cliente.
Caso ele não conheça o Mac Address o servidor irá disparar um ARP Request para toda a rede do clliente e a maquina cliente irá retornar um ARP Reply

----
#### IP

Fragmentação
Identification - more fragments - 0
47706 - MF - 0 (começo do pacote)
47706 - MF - 185
47706 - 0 - 370 (ultimo fragmento do pacote)

----
#### TCP

TCP é orientado a conexão. ele só transmite dados se garantir que a conexão foi feita com sucesso (Three Way Handshake)

----
#### UDP

Não garante a entrega dos dados, apenas envia e foda-se. Além de não ser orientado a conexão, não precisa estabelecer conexão antes de transmitir.
Usado em streaming de vídeo, áudio e comunicações de velocidade.

----

#### HTTP
É usado sempre que você visualiza um site, desenvolvido por Tim Berners-Lee e sua equipe entre 1989-1991. HTTP é o conjunto de regras utilizadas para comunicação com servidores web para transmissão de dados de páginas web, sejam HTML, imagens, vídeos, etc.

HTTPS 
é a versão segura do HTTP. Os dados HTTPS são criptografados, portanto, não apenas impedem que as pessoas vejam os dados que você está recebendo e enviando, mas também oferecem garantias de que você está se comunicando com o servidor da Web correto e não com algo que se faz passar por ele.


GET 
> Isso é usado para obter informações de um servidor web.

POST 
 > Usado para enviar dados ao servidor web e potencialmente criar novos registros

HEAD 
>

PUT 
> Enviar dados a um servidor web para atualizar informações

DELETE 
> Excluir informações/registros de um servidor web.

Códigos de Status: https://http.cat

---
#### TTL
O TTL é um campo de protocolo IP e cada sistema operacional tem um valor padrão de TTL

- Windows → TTL de 128
- Linux → TTL de 64
- Unix → TTL de 255

Ambos os valores de TTL podem ser alterados
Descobrir a rota que um pacote percorre

$ traceroute <ip/website>
$ traceroute -n <ip/website>

----
#### ### TELNET e SSH

Telnet é mais antigo | não tem criptografia | porta 23

SSH - mais indicado para servidores | porta 22

----
#### EMAIL
- SMTP 
	 Baseado no tcp, o protocolo SMTP envia os emails do cliente pro servidor e envia emails entre servidores | Porta 25/587
	
- POP3
	Leitura dos emails | Porta 110

- IMAP
	Serviço de email usado em mobile/webmail | Porta 143

----
### SMB, NFS e NTP

- SMB
    SMB é um protocolo que roda no servidor SAMBA (Linux) pra fazer a troca de arquivos entre servidores Linux e máquinas Windows e vice-versa | Porta 445
    
- NFS
    Montagem dos sistemas de arquivos remotos
    
- NTP
    Protocolo de armazenamento de acessos e sincronização de horário das maquinas da rede

----
