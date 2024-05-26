
Os ataques de falsificação de endereço IP / Address Spoofing ocorrem quando um Hacker cria pacotes com **informações falsas de endereço [[IP]]** para ocultar a identidade do remetente ou para se passar por outro usuário legítimo. 

O Hacker pode obter acesso a dados inacessíveis ou burlar as configurações de segurança. A falsificação é geralmente incorporada a outro ataque, como um ataque Smurf.

Os ataques de falsificação podem ser cegos ou não cegos (Blind ou Non Blinding)

- **Non-blind spoofing -** O Hacker pode ver o tráfego que está sendo enviado entre o host e o destino. Ele usa a falsificação não cega para inspecionar o pacote de resposta da vítima alvo. A falsificação não cega determina o estado de um firewall e prever número de sequência. 

	Também pode sequestrar uma sessão autorizada.


- **Blind spoofing -** O Hacker não pode ver o tráfego que está sendo enviado entre o host e o destino. A falsificação cega é usada em ataques de [[DoS]].

Os ataques de falsificação de endereço MAC são usados quando hackers têm acesso à rede interna. 
Os agentes de ameaças alteram o endereço MAC de seu host para corresponder a outro endereço MAC conhecido de um host de destino, conforme mostrado na figura. 

![[Pasted image 20240321153017.png]]


O host atacante envia um quadro pela rede com o endereço MAC recém-configurado. Quando o switch recebe o quadro, ele examina o endereço MAC de origem 

O switch substitui a entrada atual da tabela CAM e atribui o endereço MAC à nova porta, como mostrado na figura. Em seguida, encaminha os quadros destinados ao host de destino para o host atacante.