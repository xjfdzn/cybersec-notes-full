UDP é comumente usado por DNS, DHCP, TFTP, NFS e SNMP. Também é usado com aplicações em tempo real, como streaming de mídia ou VoIP. UDP é um protocolo de camada de transporte não orientado à conexão. Ele tem uma sobrecarga muito mais baixa que o TCP, porque não é orientado a conexão e não oferece retransmissão, sequenciamento e mecanismos de controle de fluxo sofisticados que fornecem confiabilidade. A estrutura de segmentos UDP, mostrada na figura, é muito menor que a estrutura de segmentos da TCP.

**Nota:** UDP realmente divide dados em datagramas. No entanto, o termo genérico “segmento” é comumente usado

----

Protocolo UDP, assim como o TCP, é um protocolo de transporte de dados, no entanto ele não é confiavel, pois **NÃO** garante a entrega dos dados

UDP não é necessário estabelecer uma conexão antes de começar a transmitir dados

Ele é um protocolo de entrega muito mais rápido e amplamente usado com **Streaming** de vídeo, áudio e comunicações, onde o **foco é velocidade**

---

Cabeçalho UDP

![[Pasted image 20240321155759.png]]


---

#### Ataques UDP

**Flood UDP** - Um programa envia uma inundação de pacotes UDP de um host falsificado para um servidor na sub-rede varrendo todas as portas UDP conhecidas que procuram portas fechadas. Isso fará com que o servidor responda com uma mensagem inacessível da porta ICMP