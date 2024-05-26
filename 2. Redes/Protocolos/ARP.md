
O protocolo de resolução de endereço (<span style="color:#27d5ec">ARP</span>) é um protocolo ou procedimento que conecta um endereço de protocolo de internet ([[IP]]) em constante mudança a um endereço de máquina físico (MAC) em uma rede local (LAN).


Tem a habilidade de descobrir qual endereço MAC está associado a um determinado IP
- Utiliza ARP Request e ARP Reply

**ARP Request** - Pergunta em **Broadcast** (Rede toda) quem tem um determinado IP e qual seu endereço MAC

**ARP Reply** - Resposta do host que tem o IP solicitado pelo ARP, enviando o endereço MAC

![[Pasted image 20240321161901.png]]


O cache ARP mantém um registro de cada endereço IP e seu endereço MAC correspondente. O cache ARP é dinâmico, mas os usuários em uma rede também podem configurar uma [tabela ARP](https://docs.fortinet.com/document/fortigate/6.4.0/administration-guide/473534/arp-table)estática contendo endereços IP e endereços MAC.

---
No Linux podemos usar o seguinte comando para vermos os ARPs conhecidos

```
arp -an
```

---

Qualquer cliente pode enviar uma resposta ARP não solicitada denominada "ARP gratuito". Isso geralmente é feito quando um dispositivo é inicializado para informar todos os outros dispositivos na rede local o endereço MAC do novo dispositivo. Quando um host envia um ARP gratuito, outros hosts na sub-rede armazenam o endereço MAC e o endereço IP contidos no ARP gratuito em suas tabelas ARP.

No entanto, esse recurso do ARP também significa que qualquer host pode reivindicar ser o proprietário de qualquer IP / MAC que escolher. Um ator de ameaça pode envenenar o cache ARP de dispositivos na rede local, criando um ataque MiTM para redirecionar o tráfego. O objetivo é associar o endereço MAC do ator de ameaça ao endereço IP do gateway padrão nos caches ARP dos hosts no segmento LAN. Isso posiciona o agente de ameaça entre a vítima e todos os outros sistemas fora da sub-rede local.

---

#### ARP Cache Poisoning
O envenenamento do cache ARP pode ser usado para iniciar vários ataques do tipo **man-in-the-middle.**

Um Hacker envia duas respostas ARP gratuitas falsificadas usando seu próprio endereço MAC para os endereços IP de destino indicados. 

O PC-A atualiza seu cache ARP com seu gateway padrão, que agora está apontando para o endereço MAC do host do agente da ameaça. O R1 também atualiza seu cache ARP com o endereço IP do PC-A apontando para o endereço MAC do agente da ameaça.

O host do ator de ameaça está executando um ataque de envenenamento ARP. O ataque de envenenamento ARP pode ser passivo ou ativo. O envenenamento ARP passivo é onde os atores de ameaças roubam informações confidenciais. O envenenamento ARP ativo é onde os agentes de ameaças modificam dados em trânsito ou injetam dados maliciosos.

Existem muitas ferramentas disponíveis na Internet para criar ataques ARP MITM, incluindo **dsniff**, **Cain & Abel**, **ettercap**, **Yersinia** e outros.