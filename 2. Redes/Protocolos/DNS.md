DNS utiliza por padrão o protocolo [[UDP]]

A proteção do DNS geralmente é ignorada. No entanto, é crucial para a operação de uma rede e deve ser protegido adequadamente.

Os ataques de DNS incluem os seguintes:

- Ataques de resolvedor aberto de DNS
- Ataques furtivos de DNS
- Ataques de sombreamento de domínio DNS
- Ataques de tunelamento de DNS

---
#### Ataques DNS

Ataques de *resolvedor aberto* de DNS
	Muitas organizações usam os serviços de servidores DNS abertos ao público, como o GoogleDNS (**8.8.8.8**), para fornecer respostas às consultas. Esse tipo de servidor DNS é chamado de resolvedor aberto. 
	Um resolvedor aberto de DNS responde a consultas de clientes fora de seu domínio administrativo. 
Os resolvedores abertos de DNS são vulneráveis a esses ataques:

- DNS Cache Poisoning
	Hackers enviam informações de recurso de registro **falsificado** e falsificado (RR) a um resolvedor de DNS para redirecionar usuários de sites legítimos para sites maliciosos. 

- Amplificação e Reflexão DNS
	Hackers usam ataques **DoS** ou **DDoS** em resolvedores abertos do DNS para aumentar o volume de ataques e **ocultar** a verdadeira **fonte** de um ataque. 
	Enviam mensagens DNS para os resolvedores abertos usando o endereço IP de um host de destino. Esses ataques são possíveis porque o resolvedor aberto responderá às perguntas de qualquer pessoa que faça uma pergunta.
	
- Ataque de uso de recurso DNS
	Um ataque de **DoS** que consome os recursos dos resolvedores abertos do DNS. 
	Esse ataque do DoS consome todos os recursos disponíveis para afetar negativamente as operações do resolvedor aberto do DNS. 
	O impacto desse ataque de DoS pode exigir que o resolvedor aberto do DNS seja **reinicializado** ou que os serviços sejam interrompidos e reiniciados.





Ataques *furtivos* de DNS
	Para ocultar sua identidade, os Hackers também usam as técnicas furtivas de DNS descritas na tabela para realizar seus ataques.

- Fluxo Rápido
	Hackers usam essa técnica para ocultar seus sites de entrega de phishing e malware atrás de uma rede que muda rapidamente de hosts DNS comprometidos. Os endereços IP do DNS são alterados continuamente em minutos. As redes de bots geralmente empregam técnicas do Fast Flux para impedir a detecção eficaz de servidores mal-intencionados.

- Fluxo de IP Duplo
	Hackers usam essa técnica para alterar rapidamente o nome do host para os mapeamentos de endereço IP e também para alterar o servidor de nomes autoritativo. Isso aumenta a dificuldade de identificar a fonte do ataque.
	
- Algoritmos de Geração de Dominio
	Hackers usam essa técnica em malware para gerar aleatoriamente nomes de domínio que podem ser usados como pontos de encontro para seus servidores de comando e controle (C&C).





Ataques de *sombreamento de domínio* DNS
	O sombreamento de domínio envolve o agente de ameaças coletando credenciais de conta de domínio para criar silenciosamente vários subdomínios a serem usados durante os ataques. Esses subdomínios normalmente apontam para servidores mal-intencionados sem alertar o proprietário real do domínio pai.





*Tunelamento* DNS
	Botnets se tornaram um método de ataque popular de atores ameaçadores. Na maioria das vezes, os botnets são usados para espalhar malware ou iniciar ataques de DDoS e phishing.

O DNS na empresa às vezes é negligenciado como um protocolo que pode ser usado por botnets. Por isso, quando o tráfego DNS é determinado como parte de um incidente, o ataque geralmente já acabou. É necessário que o analista de segurança cibernética seja capaz de detectar quando um invasor está usando tunelamento DNS para roubar dados e prevenir e conter o ataque. Para isso, o analista de segurança deve implementar uma solução que possa bloquear as comunicações de saída dos hosts infectados.

Hackers usam o tunelamento DNS colocam tráfego que não é de DNS, dentro do tráfego DNS. Esse método geralmente contorna soluções de segurança. Para que o agente da ameaça use o túnel DNS, os diferentes **tipos de registros DNS**, como **TXT**, **MX**, **SRV**, **NULL**, **A** ou **CNAME**, são alterados. Por exemplo, um registro TXT pode armazenar os comandos enviados para os bots de host infectados como respostas DNS. Um ataque de tunelamento DNS usando TXT funciona assim:

1. Os dados são divididos em vários blocos codificados.
2. Cada pedaço é colocado em um rótulo de nome de domínio de nível inferior na consulta DNS.
3. Como não há resposta do DNS local ou em rede para a consulta, a solicitação é enviada aos servidores DNS recursivos do ISP.
4. O serviço DNS recursivo encaminhará a consulta para o servidor de nomes autorizado do invasor.
5. O processo é repetido até que todas as consultas contendo os chunks sejam enviadas.
6. Quando o servidor de nomes autoritativo do invasor recebe as consultas DNS dos dispositivos infectados, ele envia respostas para cada consulta DNS, que contém os comandos encapsulados e codificados.
7. O malware no host comprometido recombina os pedaços e executa os comandos ocultos.

Para poder interromper o túnel DNS, um filtro que inspecione o tráfego DNS deve ser usado. Preste atenção especial às consultas DNS que são mais longas do que a média, ou aquelas que têm um nome de domínio suspeito. Além disso, as soluções de segurança de DNS, como Cisco Umbrella (anteriormente Cisco OpenDNS), bloqueiam grande parte do tráfego de túnel DNS ao identificar domínios suspeitos. Domínios associados a serviços DNS dinâmicos devem ser considerados altamente suspeitos.

![[Pasted image 20240321163631.png]]



---
