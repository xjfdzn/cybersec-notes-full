O Protocolo TCP é confiável para transmissão de dados pois ele garante a entrega das informações

O TCP é orientado a conexão, isso significa que ele só transmite se garantir que uma conexão foi estabelecida com sucesso (**Three-way Handshake**)

O TCP se comunica diretamente com Portas
Cabeçalho TCP

![[Pasted image 20240321154104.png]]


Flags
- **URG** - Campo de ponteiro urgente significativo
- **ACK** - Campo de confirmação significativo
- **PSH** - Função Push
- **RST** - Redefinir a conexão
- **SYN** - Sincroniza os números da sequência
- **FIN** - Não há mais dados do remetente

---

#### Three-way Handshake

1. O host requisita uma sessão de comunicação com o servidor.
2. O servidor reconhece a sessão de comunicação e solicita uma sessão de comunicação servidor
3. O host reconhece a sessão de comunicação servidor

![[tcpack 1.png]]

---

#### Ataques TCP

**Flood de SYN** - O ataque de inundação SYN TCP explora o Three-way Handshake. 

A figura mostra um agente de ameaça enviando continuamente pacotes de solicitação de sessão TCP SYN com um endereço IP de origem falsificado aleatoriamente para um destino. O dispositivo de destino responde com um pacote TCP SYN-ACK ao endereço IP falsificado e aguarda um pacote TCP ACK. Essas respostas nunca chegam. Eventualmente, o host de destino é sobrecarregado com conexões TCP semi-abertas e os serviços TCP são negados a usuários legítimos.

1. O Hacker envia várias solicitações SYN para o servidor web.
2. O servidor web responde com SYN-ACK's para cada solicitação SYN e espera completar o handshake. O ator de tratamento não responde aos SYN-ACK's.
3. O usuário comum não pode acessar o servidor web porque o servidor web tem muitas conexões TCP semi-abertas.


**Session Hijacking TCP** - Embora seja difícil de conduzir, um Hacker assume um host já autenticado quando ele se comunica com o alvo. 

O agente de ameaça deve falsificar o endereço IP de um dos hosts, prever o próximo número de sequência e enviar um ACK para o outro host. Se for bem-sucedido, o agente da ameaça poderá enviar, mas não receber, dados do dispositivo de destino

	Resumo: quando o agente de ameaça falsifica o endereço IP de um host, prevê o próximo número de sequência e envia um ACK para o outro host