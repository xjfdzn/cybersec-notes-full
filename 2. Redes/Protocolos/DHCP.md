Os servidores DHCP fornecem dinamicamente informações de configuração de IP aos clientes. A figura mostra a sequência típica de uma troca de mensagens DHCP entre cliente e servidor.



---

Ataques DHCP

**Ataque de falsificação de DHCP**

Um ataque de spoofing de DHCP ocorre quando um servidor DHCP invasor está conectado à rede e fornece falsos parâmetros de configuração IP aos clientes legítimos. Um servidor não autorizado pode fornecer uma variedade de informações enganosas:

- **Gateway padrão errado -** O ator da ameaça fornece um gateway inválido ou o endereço IP de seu host para criar um ataque MiTM. Isso pode não ser totalmente detectado, pois o invasor intercepta o fluxo de dados pela rede.
- **Servidor DNS errado -** O agente de ameaças fornece um endereço de servidor DNS incorreto, apontando o usuário para um site malicioso.
- **Endereço IP errado -** O agente de ameaças fornece um endereço IP inválido, um endereço IP de gateway padrão inválido ou ambos. O agente de ameaça cria um ataque de negação de serviço no cliente DHCP.

Suponha que um agente de ameaça tenha conectado com êxito um servidor DHCP não autorizado a uma porta de switch na mesma sub-rede que os clientes de destino. O objetivo do servidor não autorizado é fornecer aos clientes informações falsas de configuração de IP.


DHCP utiliza por padrão o protocolo [[UDP]]



