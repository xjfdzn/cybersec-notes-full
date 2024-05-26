# Aplicação
A camada de aplicação é a camada mais próxima do usuário. Ela define como o usuário interage com a rede. Ela contém a lógica da aplicação e não tem consciência da implementação de rede. Por exemplo, caso tenha um sistema de reserva com calendário na sua empresa, essa camada gerencia a lógica de reserva, como o envio de convites, a conversão de fusos horários e muito mais.
##### Sistema de nomes

- **DNS** - *Converte nomes de domínio*, como `cisco.com`, em *endereços IP*.
##### DHCP (Configuração de hosts)
- **DHCPv4** - Configuração de *Host Dinâmico para IPv4*. Um servidor DHCPv4 atribui dinamicamente informações de endereçamento IPv4 aos clientes DHCPv4 na inicialização e permite que os endereços sejam *reutilizados* quando não forem mais necessários.
- **DHCPv6** - Configuração do *Host Dinâmico para IPv6*. DHCPv6 é semelhante ao DHCPv4. Um servidor DHCPv6 *atribui dinamicamente* informações de endereçamento IPv6 aos clientes DHCPv6 na inicialização.
- **SLAAC** - Configuração automática de *endereço sem estado*. Um método que permite que um dispositivo obtenha suas informações de endereçamento IPv6 sem usar um servidor DHCPv6.
##### E-mail
- **SMTP** -Protocolo de *transferência de correio simples*. Permite que os clientes enviem e-mails para um servidor de e-mail e permite que os servidores enviem e-mails para outros servidores.
- **POP3** - Post Office Protocol versão 3. Permite que os clientes *recuperem e-mails* de um servidor de e-mail e *baixem o e-mail* para o aplicativo de e-mail local do cliente.
- **IMAP** - Protocolo de *Acesso à Mensagem na Internet*. Permite que os clientes acessem o e-mail armazenado em um servidor de e-mail e também mantenham o e-mail no servidor.
##### Transferência de arquivos
- **FTP** - Protocolo de *transferência de arquivos*. Define as regras que permitem que um usuário em um host acesse e transfira arquivos para e de outro host em uma rede. O FTP é um protocolo de *entrega de arquivos confiável*, orientado a conexão e reconhecido.
- **SFTP** - Protocolo de *transferência de arquivos SSH*. Como uma extensão do protocolo Secure Shell (SSH), o SFTP pode ser usado para estabelecer uma *sessão segura* de transferência de arquivos na qual a *transferência é criptografada*. SSH é um método para login remoto seguro que normalmente é usado para acessar a linha de comando de um dispositivo.
- **TFTP** - Protocolo de *Transferência de Arquivos Trivial*. Um protocolo de transferência de arquivos simples e sem conexão com entrega de arquivos não confirmada e de melhor esforço. Ele *usa menos sobrecarga* que o FTP. (FTP )
##### Web e serviço Web
- **HTTP** - Protocolo de *transferência de hipertexto*. Um conjunto de regras para a troca de texto, imagens gráficas, som, vídeo e outros arquivos multimídia na World Wide Web.
- **HTTPS** - *HTTP seguro*. Uma forma segura de HTTP que criptografa os dados que são trocados pela World Wide Web.
- **REST** - *Representational State Transfer*. Um serviço Web que utiliza interfaces de programação de aplicações (APIs) e pedidos HTTP para criar aplicações Web.
- **SSL** - *Secure Sockets Layer* é um protocolo de segurança baseado em criptografia
	SSL criptografa os dados, realiza a autenticação e assina os dados digitalmente pra garantir a integridade. Um site que implementa SSL/TLS apresenta um "HTTPS" na URL em vez de um "HTTP".
##### Tradução de domínio 
- **DNS**  - Protocolo de *Sistema de nome de domínio*. Converte os endereços IP legíveis pela máquina como (172.456.0.12) em nomes de domínio legíveis por humanos como por exemplo "www,amazon.com"
##### Acesso Remoto
- **SSH** - Protocolo *Secure Shell* é utilizado para login remoto de utilizadores a sistemas de computadores. O SSH fornece um canal seguro sobre uma rede insegura em uma arquitetura cliente-servidor, conectando uma aplicação cliente SSH com um servidor SSH.
- **Telnet** - Protocolo *Teletype Network*. O Telnet <span style="color:#ff0000">NÃO</span> possui criptografia. Ele envia as mensagens em texto puro. Dessa forma caso alguém intercepte esses dados conseguirá ver o conteúdo. É possível invadir o Telnet através de <span style="color:#eb1e96">Man In the Middle</span> ou usando um <span style="color:#eb1e96">Sniffer</span> 


# Apresentação
A camada de apresentação prepara os dados para a transmissão na rede. Por exemplo, ela adiciona criptografia para que os cybercriminosos que espionam a WAN não sejam capazes de ter acesso aos dados confidenciais.
##### Codificação de Dados
- **XDR** -  *eXternal Data Representation* é um padrão que permite que dados sejam empacotados de forma independente da arquitetura de computadores. Isso facilita a transferência de dados entre sistemas diferentes. A conversão dos dados locais para o formato XDR é chamada de codificação, enquanto a conversão do XDR de volta para os dados locais é chamada de decodificação. O XDR é implementado como uma biblioteca de funções que pode ser usada em diferentes sistemas operacionais e não depende da camada de transporte.

	O XDR suporta vários tipos de dados, incluindo *booleanos, inteiros de 32 bits, inteiros de 64 bits, números decimais, enumerações, estruturas, strings, arrays de tamanho fixo, arrays de tamanho variável, uniões e dados opacos.*
# Sessão
A camada de sessão gerencia as conexões ou as sessões entre as aplicações locais e remotas. Ela abre, fecha ou encerra a conexão entre dois dispositivos. Por exemplo, o sistema de reservas está localizado em um servidor web no escritório central, e o usuário está trabalhando em casa. A camada de sessão abre uma conexão entre o computador do usuário e o servidor web depois da autenticação. Essa conexão é uma conexão lógica, e não uma conexão física.
##### NetBIOS
**NetBIOS** - é *Sistema Básico de Entrada/Saída de Rede*. É uma API que fornece serviços relacionados com a [camada de sessão](https://pt.wikipedia.org/wiki/Camada_de_sess%C3%A3o "Camada de sessão") do [modelo OSI](https://pt.wikipedia.org/wiki/Modelo_OSI "Modelo OSI"), permitindo que os aplicativos em computadores separados se comuniquem em uma [rede local](https://pt.wikipedia.org/wiki/Rede_de_%C3%A1rea_local "Rede de área local"), não podendo ser confundido, portanto, como um [protocolo de rede](https://pt.wikipedia.org/wiki/Protocolo_de_rede "Protocolo de rede"). [Sistemas operacionais](https://pt.wikipedia.org/wiki/Sistema_operacional "Sistema operacional") mais antigos executavam o NetBIOS sobre o [IEEE 802.2](https://pt.wikipedia.org/wiki/IEEE_802.2 "IEEE 802.2") e o [IPX/SPX](https://pt.wikipedia.org/wiki/IPX/SPX "IPX/SPX") usando os protocolos [NetBIOS Frames](https://pt.wikipedia.org/w/index.php?title=NetBIOS_Frames&action=edit&redlink=1 "NetBIOS Frames (página não existe)") (NBF) e [NetBIOS sobre IPX/SPX](https://pt.wikipedia.org/w/index.php?title=NetBIOS_sobre_IPX/SPX&action=edit&redlink=1 "NetBIOS sobre IPX/SPX (página não existe)") (NBX), respectivamente. Em redes modernas, o NetBIOS normalmente é executado sobre [TCP/IP](https://pt.wikipedia.org/wiki/TCP/IP "TCP/IP") através do protocolo [NetBIOS sobre TCP/IP](https://pt.wikipedia.org/w/index.php?title=NetBIOS_sobre_TCP/IP&action=edit&redlink=1 "NetBIOS sobre TCP/IP (página não existe)") (NBT). Isso resulta que cada computador na rede possua um [endereço IP](https://pt.wikipedia.org/wiki/Endere%C3%A7o_IP "Endereço IP") e um nome NetBIOS correspondente a um (possivelmente diferente) nome de hospedeiro.


# Transporte
A camada de transporte define as funções e procedimentos para a transmissão de dados. Ela classifica e despacha os dados para transferência. Ela também empacota os dados em pacotes de dados. Por exemplo, ao visitar um site de reservas, o protocolo de controle de transmissão (TCP) gerencia a comunicação ao classificá-la em pacotes de requisição e resposta. 

Usa os protocolos TCP e UDP
# Rede
A camada de rede gerencia como os pacotes de dados trafegam na rede. Por exemplo, ela define as regras para o roteamento de pacotes, balanceamento de carga e perda de pacotes utilizando o protocolo IP
# Enlace
A camada de ligação de dados é responsável pelo estabelecimento das regras de comunicação ou protocolos nas operações da camada física. Por exemplo, ela decide quando iniciar ou terminar uma conexão direta. 

A função dessa camada é encaminhar os pacotes de um dispositivo para o outro até chegar ao destino. 
Usando muito o MAC Address
# Fisica
A camada física gerencia a transferência dos dados brutos nas formas de bits digitais, sinais óticos ou ondas eletromagnéticas entre as diferentes mídias de transmissão de rede, como as tecnologias de fibra ótica e redes sem fio.