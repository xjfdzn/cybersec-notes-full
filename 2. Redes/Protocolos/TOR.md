### Acesso a Rede Tor

A rede Tor funciona roteando a comunicação do usuário através de uma série de Relays (*computadores voluntários*) espelhados pelo mundo todo, criptografando a informação em múltiplas camadas

![[Pasted image 20240224120409.png]]

Cada camada tem uma key/chave para abrir a próxima camada, e então é feito a troca de Relayy

### Relays
Para acessar a rede Tor, temos os Relays, que são basicamente os *nós de rede*.
Cada um dos relays é referente a um IP/localização aleatorio no mundo

Tipos de relays:
- Entrada/guarda
- Intermediário (*Mais Seguro!*)
- Saída

- O Relay de guarda sempre irá saber de onde veio a fonte da conexão, seu primeiro IP e passará isso ao Intermediário. 
- O intermediário não sabe a origem do trafego e nem o destino final. é o nó que menos sabe.
- Saída enviará seu tráfego final ao website, logo, o website final não saberá quem é você, apenas de onde veio o ultimo nó.
### Circuito da Rede Tor
![[Pasted image 20240224120501.png]]






### Acesso ao .onion

Abaixo temos o funcionamento da rede Tor ao acessar um website .onion, dentro da Dark Web.

Você passa pelas relays normalmente, porém o website .onion vai fornecer as proprias relays para você acessar o site, como por exemplo, um ponto de encontro.

> Imagine que você irá se encontrar com um vendedor desconhecido, então para ninguém saber o endereço de ninguém, vocês marcam para se encontrar no shopping, então cada um percorre seu próprio caminho e após isso voltam pra suas respectivas casas.

Com o acesso ao .onion é a mesma coisa, ao você dar um GET no website ele irá fornecer as melhores relays dele e vocês irão se conectar

![[Pasted image 20240224115204.png]]


[[Dark Web]]