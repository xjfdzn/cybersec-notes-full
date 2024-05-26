
Media Access Control Address



Endereço fisico que vem definido de fabrica na placa de rede

MAC Addres é formado por uma sequencia de 6 bytes

Endereço MAC padrão
	A4:5E:60:B8:C1:AF


**A4:5E:60**:  = Fabricante
B8:C1:AF = Sequencia Única definida pelo fabricante
[Website para descobrir o fabricante do MAC](https://macvendors.com)


Para se conectar a um IP por exemplo, é necessário passar pelo protocolo [[ARP]]

---
No Linux é possível alterar o MAC Address utilizando o **macchanger** com os comandos

| Comando                  | Descrição                     |
| ------------------------ | ----------------------------- |
| macchanger -r eth0       | Alterar MAC para um aleatório |
| macchanger -p eth0       | Voltar ao endereço MAC padrão |
| macchanger -m >MAC< eth0 | Adicionar um MAC especifico   |


