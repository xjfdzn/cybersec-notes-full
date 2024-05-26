## **Grayware**
Qualquer aplicativo indesejado que se comporta de maneira irritante ou indesejável. E, embora o grayware não tenha nenhum malware reconhecível, ele ainda pode representar um risco para o usuário, por exemplo, acompanhando a sua localização ou disponibilizando publicidade indesejável.

Os autores de grayware normalmente mantêm a legitimidade ao incluir esses recursos "cinzas" nas letras pequenas do contrato de licença do software. Esse fator representa uma ameaça crescente à segurança móvel, em particular, já que muitos usuários de smartphones instalam aplicativos móveis sem levar em consideração essas letras pequenas.

## **SMiShing**
Tática usada pelos invasores para enganá-lo. Mensagens de texto falsas solicitam que você acesse um site mal-intencionado ou ligue para um número de telefone fraudulento, o que pode resultar no download de malware no dispositivo ou no compartilhamento de informações pessoais.

## Access Point Not Authorized

Um invasor geralmente usa táticas de engenharia social para obter acesso físico à infraestrutura de rede de uma empresa e instalar o **access point não autorizado**.

Também conhecido como access point de criminosos, o access point pode ser configurado como um dispositivo Man In The Middle para capturar suas informações de login.

Isso funciona desconectando o access point não autorizado, que aciona a rede para enviar um quadro de autenticação e desassociar o access point. Esse processo é então explorado falsificando seu endereço MAC e enviando uma transmissão de dados de autenticação para o access point sem fio

## Evil Twin
Um ataque de **Evil Twin** descreve uma situação em que o access point do invasor é configurado para parecer uma opção de conexão melhor. Depois de se conectar ao ponto de acesso maligno, o invasor pode analisar o tráfego da rede e executar ataques Man In The Middle


## Interferência de Radiofrequência
Os sinais sem fio são suscetíveis a interferência eletromagnética (EMI), interferência de radiofrequência (RFI) e até mesmo raios ou ruído de luzes fluorescentes.

Os invasores podem aproveitar esse fato bloqueando deliberadamente a transmissão de uma estação de rádio ou satélite para impedir que um sinal sem fio chegue à estação receptora.

Para bloquear o sinal com sucesso, a frequência, a modulação e a potência do jammer de RF precisam ser iguais às do dispositivo que o invasor está tentando interromper.

---

Devido ao alcance limitado do Bluetooth, o invasor deve estar dentro do alcance do alvo. Aqui estão algumas maneiras pelas quais eles podem explorar o dispositivo de um alvo sem o conhecimento deles

## **Bluejacking**
O Bluejacking usa a tecnologia Bluetooth sem fio para enviar mensagens não autorizadas ou imagens chocantes para outro dispositivo Bluetooth

## Bluesnarfing
O Bluesnarfing ocorre quando um invasor copia informações, como e-mails e listas de contatos, de um dispositivo de destino usando uma conexão Bluetooth

---

## **Ataques Contra Protocolos Wi-Fi**
A **privacidade equivalente com fio (WEP)** e o **acesso protegido por Wi-Fi (WPA)** são protocolos de segurança projetados para proteger redes sem fio vulneráveis a ataques.

O WEP foi desenvolvido para fornecer dados transmitidos por uma rede local sem fio (WLAN) com um nível de proteção comparável ao que é normalmente esperado de uma rede com fio tradicional. Ela agregou segurança às redes sem fio ao criptografar os dados.

WEP usou uma chave para criptografia. O problema, no entanto, era que o WEP não dispunha de gerenciamento de chaves e, portanto, o número de pessoas que compartilhavam a mesma chave crescia continuamente, dando aos criminosos acesso a uma grande quantidade de dados de tráfego. Além disso, o vetor de inicialização (IV) do WEP, um dos principais componentes de sua chave de criptografia, era muito pequeno, legível e estático.

Para resolver isso e substituir o WEP, o **WPA** e o **WPA2** foram desenvolvidos como protocolos de segurança aprimorados. Ao contrário do WEP, um invasor não pode recuperar a chave de criptografia do WPA2 observando o tráfego de rede. No entanto, eles ainda podem usar um sniffer de pacotes para analisar os pacotes entre um ponto de acesso e um usuário legítimo.

![https://skillsforall.com/content/noes/1.0/m1/course/pt-BR/assets/608af6a9c337810aa6824ca1.png](https://skillsforall.com/content/noes/1.0/m1/course/pt-BR/assets/608af6a9c337810aa6824ca1.png)

# **Wi-Fi e Defesa Móvel**

Existem várias etapas que as organizações e os usuários precisam seguir para se defender contra ataques a dispositivos móveis e sem fio. Estes incluem o seguinte:

- Aproveite os recursos básicos de segurança sem fio, como autenticação e criptografia, alterando as configurações padrão.
- Restrinja o posicionamento de access point colocando esses dispositivos fora do firewall ou dentro de uma zona desmilitarizada - uma rede de perímetro que protege a LAN de uma empresa contra dispositivos não confiáveis.
- Use ferramentas WLAN como NetStumbler para detectar pontos de acesso não autorizados ou estações de trabalho não autorizadas.
- Desenvolva uma política para acesso de convidado à rede Wi-Fi de uma empresa.
- Os funcionários de uma empresa devem usar uma VPN de acesso remoto para acesso à WLAN.


- Uma rede sem fio Guest deve fornecer acesso à Internet apenas para convidados. Ele não deve permitir que os convidados acessem os dispositivos na rede local dentro de casa. Nesse caso, os convidados podem acessar a rede local. Isso indica que o roteador doméstico está configurado incorretamente.
	**Para proteger isso**: A rede de convidado deve ser desativada ou configurada com segurança básica, como autenticação forte, transmissão de SSID desabilitada e acesso aos dispositivos de rede locais desabilitados.