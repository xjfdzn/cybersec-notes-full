
Hackers atacam o [[ICMP]] para ataques de **reconhecimento** e **varredura**. 
Isso permite que eles lancem ataques de coleta de informações para:

- Mapear uma topologia de rede
- Descobrir quais hosts estão ativos
- Ver o S.O do host
- Ver o estado de um **firewall**.

![[Pasted image 20240321150150.png]]

<span style="color:#ffc000">Obs: ICMP para IPv4 (ICMPv4) e ICMP para IPv6 (ICMPv6) são suscetíveis a tipos semelhantes de ataques.</span> 



Lista de mensagens ICMP comuns de interesse para Hackers

**ICMP echo Request / echo Reply** - Usado para executar verificação de host e ataques de DoS

**ICMP Inacessível** -Isso é usado para executar ataques de reconhecimento e varredura de rede.

**Mask Reply ICMP** - Isso é usado para mapear uma rede IP interna.

**ICMP Redirect** -  Atrair um host alvo para enviar todo o tráfego através de um 
dispositivo comprometido e criar um ataque ManInTheMiddle

**ICMP Router Discovery** - Injetar entradas de rota falsas na tabela de roteamento de um host de destino.