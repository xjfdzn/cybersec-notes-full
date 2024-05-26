Uma WAN, ou rede de longa distância, é um *conjunto de LANs conectadas*. É uma ampla rede de redes locais. Uma WAN pode ter qualquer tamanho, até mesmo milhares de quilômetros de largura; ela não está restrita a uma determinada área.

Tipos comuns de conexões:

**Linhas alugadas** - Uma linha alugada é conexão de rede direta. É possível alugá-la de um grande provedor de rede, como um provedor de serviços de Internet (ISP). Ela pode conectar dois endpoints de LAN. As linhas alugadas não são necessariamente linhas físicas. Elas podem ser conexões virtuais nas quais os provedores de serviços implementam sobre outra infraestrutura de rede.

**Tunelamento** - Maneira de criptografar os pacotes de dados conforme eles transitam na Internet pública. No túnel, a conexão da Internet é usada para acessar os servidores da empresa e um outro país. Contudo, os dados são enviados em pacotes encapsulados e, assim, a própria rede privada virtual (VPN) é formada.

**Multiprotocol Label Switching** - Técnica que roteia o tráfego de dados baseado em rótulos pré-determinados. Ele tenta rotear o tráfego de dados críticos entre os caminhos de rede mais curtos e rápidos, o que melhora a performance da rede. Ele trabalha entre as camadas 2 e 3 do modelo OSI. É possível usá-lo para criar uma rede unificada na infraestrutura existente, como IPv6, frame relay, ATM ou ethernet. É possível usar linhas alugadas MPLS ou MPLS com VPNs para criar redes eficientes e seguras.

**WAN definida por software** - A rede de longa distância definida por software (SD-WAN) é a evolução da tecnologia MPLS. Ela abstrai as funções MPLS em uma camada de software. Uma vez que a SD-WAN funciona em conexões de Internet de banda larga estáveis, é possível reduzir os custos de rede e oferecer uma maior flexibilidade em relação a uma conexão fixa.

**MPLS** *X* **SD-WAN** - A MPLS pode desacelerar a integração com a nuvem, pois ela roteia o tráfego entre as matrizes corporativas, as quais funcionam como pontos de centrais de gargalo. Por outro lado, a SD-WAN é voltada para a nuvem e faz a integração mais eficaz com as modernas infraestruturas de nuvem. A SD-WAN também é econômica. Ela pode funcionar sobre a MPLS para que seja possível usar a largura de banda de forma mais eficiente em linhas caras e alugadas MPLS.


---

As WLANs usam **Frequências de Rádio (RF)** em vez de cabos na camada física e na subcamada MAC da camada de enlace de dados. As WLANs compartilham uma origem semelhante com as LANs Ethernet. O IEEE adotou o portfólio 802 LAN/MAN de padrões de arquitetura de rede de computadores. Os dois grupos de trabalho dominantes 802 são 802.3 Ethernet, que definiu Ethernet para LANs com fio, e [[Quadro 802.11]] que definiu Ethernet para WLANs. Existem diferenças importantes entre os dois.

As WLANs também diferem das LANs com fio da seguinte forma:

- WLANs conectam clientes à rede por meio de um ponto de **acesso sem fio** (*AP*) ou **roteador sem fio**, em vez de um switch Ethernet.
- WLANs conectam dispositivos móveis que geralmente são alimentados por bateria, em vez de dispositivos LAN conectados. As placas de rede sem fio tendem a reduzir a duração da bateria de um dispositivo móvel.
- WLANs suportam hosts que disputam acesso na mídia de RF (bandas de frequência). O 802.11 prescreve a prevenção de colisões (CSMA/CA) em vez de detecção de colisões (CSMA/CD) para acesso à mídia para evitar colisões proativamente dentro da mídia.
- WLANs usam um formato de quadro diferente das LANs Ethernet com fio. As WLANs exigem informações adicionais no cabeçalho da Camada 2 do quadro.
- WLANs levantam mais problemas de privacidade porque as frequências de rádio podem chegar fora das instalações.

---

Diferenças entre LAN sem fio e com fio

![[Pasted image 20240323222231.png]]

---

#### Descoberta Passiva
No modo passivo, o ponto de acesso anuncia abertamente seu serviço enviando periodicamente quadros de beacon de transmissão contendo o [[SSID]], padrões suportados e configurações de segurança. 
O objetivo principal do **beacon** é permitir que os clientes sem fio aprendam quais redes e pontos de acesso estão disponíveis em uma determinada área. Isso permite que os clientes sem fio escolham qual rede e ponto de acesso usar.

#### Descoberta Ativa

No modo ativo, os clientes sem fio **devem saber o nome do SSID**. O cliente sem fio inicia o processo transmitindo um quadro de solicitação de análise em vários canais. A solicitação de análise inclui o nome SSID e os padrões suportados. Os pontos de acesso configurados com o SSID enviarão uma resposta do probe que inclui o SSID, os padrões suportados e as configurações de segurança. O modo ativo pode ser necessário se um ponto de acesso ou roteador sem fio estiver configurado para não transmitir quadros de beacon.

Um cliente sem fio também pode enviar uma solicitação de análise sem um nome SSID para descobrir redes WLAN próximas. Os pontos de acesso configurados para transmitir quadros de beacon responderiam ao cliente sem fio com uma resposta do probe e forneceriam o nome SSID. Os pontos de acesso com o recurso SSID de transmissão desativado não respondem.

---
