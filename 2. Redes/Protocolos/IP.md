### Endereço IP

O endereço IP é formado por 4 octetos, representados de forma **decimal**.

Existem várias classificações de endereço IP e cada uma serve para definir o uso em uma rede de acordo com a necessidade


```
192.168.0.200
```

 **192.168.0.         200**     
   Rede             Host

---

Podemos usar o aplicativo **ipcalc** para ver os detalhes das classes de IP
```
ipcalc <ip>/<mascara>
```

![[Pasted image 20240316154907.png]]

---

### Protocolo IP
O protocolo IP trabalha com endereços lógicos. 

É responsável por realizar a **entrega dos pacotes** entre máquinas, apenas isso
Ele não é confiável, apenas entrega o pacote sem nenhuma verificação depois da entrega.

IP + [[TCP]] = Confiabilidade
IP + [[UDP]] = Velocidade

---
### Vulnerabilidades de IP
- **Ataques ICMP** - Os hackers usam pacotes de eco (pings) do ICMP (Internet Control Message Protocol) para descobrir sub-redes e hosts em uma rede protegida, gerar ataques de inundação de DoS e alterar as tabelas de roteamento de hosts.

- **DoS** - Os atores da ameaça tentam impedir que usuários legítimos acessem informações ou serviços.

- **DDoS** - Semelhante a um ataque DoS, mas apresenta um ataque simultâneo e coordenado de várias máquinas de origem.

- **Falsificação de Endereços** | Address Spoofing- Os atores da ameaça falsificam o endereço IP de origem na tentativa de executar falsificação cega ou não cega.

- **ManInTheMiddle** - Os agentes de ameaças se posicionam entre uma fonte e um destino para monitorar, capturar e controlar de forma transparente a comunicação. Eles poderiam simplesmente espiar inspecionando os pacotes capturados ou alterando os pacotes e encaminhando-os ao seu destino original.

- **Sequestro de Sessão** | Session Hijacking - Os atores da ameaça obtêm acesso à rede física e, em seguida, usam um ataque MiTM para sequestrar uma sessão.

---

#### IPv4
![[Pasted image 20240321160901.png]]


Padrão de Classes IP e Mascaras
![[Pasted image 20240504204739.png]]





#### IPv6
![[Pasted image 20240321160915.png]]


Limite de Saltos - Usado pelo roteador para determinar se um pacote expirou e deve ser descartado