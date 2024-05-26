







## Spoofing
Spoofing é um ataque de representação e tira proveito de uma relação de confiança entre os dois sistemas.

- A falsificação de endereço MAC ocorre quando um invasor disfarça seu dispositivo como um dispositivo válido na rede e, portanto, pode ignorar o processo de autenticação.
- O ARP spoofing envia mensagens ARP falsificadas através de uma LAN. Isso vincula o endereço MAC de um invasor ao endereço IP de um dispositivo autorizado na rede.
- O spoofing de IP envia pacotes IP com um endereço de origem falsificado para se disfarçar.

## **DNS Spoofing**
A falsificação de DNS ou o envenenamento de cache DNS é um ataque no qual dados falsos são introduzidos em um cache de resolvedor de DNS - o banco de dados temporário no sistema operacional de um computador que registra visitas recentes a sites e outros domínios da Internet.

Esses ataques de veneno exploram uma fraqueza no software DNS que faz com que os servidores DNS redirecionem o tráfego de um domínio específico para o computador do invasor.


## Sequestro de Dominio
Quando um invasor obtém, por engano, o controle das informações de DNS de um alvo, ele pode fazer alterações não autorizadas. Isso é conhecido como sequestro de domínio.

A maneira mais comum de sequestrar um nome de domínio é alterar o endereço de e-mail de contato do administrador por meio de engenharia social ou invadir a conta de e-mail do administrador. O endereço de e-mail do administrador pode ser facilmente encontrado pelo registro WHOIS do domínio, que é de registro público.


## MAC Flooding
Os dispositivos em uma rede são conectados por um switch de rede usando o switching de pacote para receber e encaminhar dados para o dispositivo de destino. A inundação de MAC (MAC Flooding) compromete os dados transmitidos para um dispositivo. Um invasor inunda a rede com endereços MAC falsos, comprometendo a segurança do switch de rede.



## Man In The Middle
Esse ataque acontece quando um criminoso digital assume o controle de um dispositivo sem o conhecimento do usuário. Com esse nível de acesso, um invasor pode interceptar, manipular e retransmitir informações falsas entre o remetente e o destino pretendido.

## Man In The Mobile
Quando infectado, o dispositivo móvel é instruído a capturar informações confidenciais do usuário e enviá-las aos invasores.

O ZeuS é um exemplo de pacote de malware com recursos MitMo. Ele permite que os invasores capturem silenciosamente as mensagens SMS de verificação em duas etapas enviadas aos usuários.




## Zero Day
Um ataque de dia zero ou ameaça de dia zero explora vulnerabilidades de software antes que elas se tornem conhecidas ou antes de serem divulgadas pelo fornecedor do software.

Uma rede é extremamente vulnerável a ataques entre o momento em que um exploit é descoberto (zero hora) e o tempo que leva para o fornecedor do software desenvolver e lançar um patch que corrija esse exploit.



## Keylogger
É guardado em log as teclas digitadas por meio de software instalado em um sistema de computador ou por dispositivos de hardware fisicamente conectados a um computador, e configuram o software keylogger para enviar o arquivo de log para o criminoso. Como gravou todas as teclas digitadas, esse arquivo de log pode revelar nomes de usuários, senhas, sites visitados e outras informações confidenciais.

Muitos pacotes anti-spyware podem detectar e remover keyloggers não autorizados.




## Ransomware





**Como se defender**: Os funcionários devem ser treinados para identificar e-mails de phishing e as ações que devem ser tomadas para evitar danos. Além disso, as empresas podem configurar firewalls, sistemas de prevenção contra invasões e outros dispositivos de segurança e software para bloquear e-mails de phishing antes de entrar na rede. Algumas empresas assinam serviços que compilam e mantêm listas de sites mal-intencionados. Os dispositivos de segurança da empresa podem, então, usar essas listas para atualizar automaticamente os filtros para bloquear o tráfego mal-intencionado.





---

# Defesa contra Ataques

As organizações podem tomar várias medidas para se defender contra vários ataques. Estes incluem o seguinte:

- Configure firewalls para remover quaisquer pacotes de fora da rede que tenham endereços indicando que eles se originaram de dentro da rede.
- Verifique se as correções e atualizações estão atualizadas.
- Distribuir a carga de trabalho nos sistemas de servidor.
- Os dispositivos de rede usam pacotes do Internet Control Message Protocol (ICMP) para enviar mensagens de erro e controle, como se um dispositivo pode ou não se comunicar com outro na rede. Para evitar ataques de DoS e DDoS, as empresas podem bloquear pacotes externos de ICMP com seus firewalls.

---