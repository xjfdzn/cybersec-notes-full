#### Ameças de Endpoint
O termo “**endpoint**” é definido de várias maneiras. Para fins deste curso, podemos definir endpoints como hosts na rede que podem acessar ou ser acessados por outros hosts na rede. Isso obviamente inclui computadores e servidores, no entanto muitos outros dispositivos também podem acessar a rede. Com o rápido crescimento da Internet das Coisas (IoT), outros tipos de dispositivos são agora endpoints na rede. Isso inclui câmeras de segurança em rede, controladores e até mesmo lâmpadas e aparelhos. Cada ponto de extremidade é potencialmente uma forma de software malicioso obter acesso a uma rede. Além disso, as novas tecnologias, como a nuvem, expandem os limites das redes empresariais para incluir locais na Internet pelos quais as empresas não são responsáveis.

Dispositivos que acessam redes remotamente através de VPNs também são endpoints que precisam ser considerados. Esses endpoints podem injetar malware na rede VPN a partir da rede pública.

Os pontos a seguir resumem algumas das razões pelas quais o malware continua sendo um grande desafio:

- De acordo com pesquisas da Cybersecurity Ventures, até 2021 uma nova organização será vítima de um ataque de ransomware a cada 11 segundos.
- Os ataques de ransomware custarão à economia global US$6 trilhões por ano até 2021.
- Em 2018, 8 milhões de tentativas de roubar recursos do sistema usando malware de criptografia foram observadas.
- De 2016 até o início de 2017, o volume global de spam aumentou drasticamente. De 8 a 10 por cento deste spam pode ser considerado malicioso, como mostrado na figura.
- Em 2020, prevê-se que o número médio de ataques cibernéticos por dispositivo macOS aumentará de 4.8 em 2018 para 14,2 em 2020.
- Vários tipos comuns de malware foram encontrados para alterar significativamente os recursos em menos de 24 horas, a fim de evitar a detecção.

---

Porcentagem de Spam

A Figura 1 mostra os e-mails por segundo enviados de 2012 a 2016 e o aumento de 0 ponto 5 K de volta em 20 12 para mais de 3 K em 20 16. A Figura 2 mostra a porcentagem da extensão total de cerca de 0 por cento em janeiro de 2015 para como em 2016 quase 15% contém pontos maliciosos w s f, e 25% contém ponto malicioso d o c m, perto de 40% contém arquivos zip ponto maliciosos, quase 50% contém arquivos de ponto j s maliciosos, quase 70 por cento contém arquivos de ponto malicioso percentual contém arquivos maliciosos ponto h t a, e mais de 70% contém anexos mal-intencionados baseados na pesquisa de segurança da Cisco.

![asset.description](https://contenthub.netacad.com/asset/netacad-media/media/b233ca90-bd0b-11ea-88f0-0df34fdf4f1a/assets/images/7d7b1380-bfc2-11ea-ae3e-8952c1b0fe52.png)

---
#### Segurança de Endpoint

A mídia de notícias geralmente cobre ataques de rede externa em redes corporativas. Estes são alguns exemplos de tais ataques:

- Ataques DoS na rede de uma organização para degradar ou mesmo interromper o acesso público a ela
- Violação do servidor web de uma organização para desfigurar sua presença na Web
- Violação de servidores de dados e hosts de uma organização para roubar informações confidenciais

Vários dispositivos de segurança de rede são necessários para proteger o perímetro da rede contra acesso externo. Como mostrado na figura, esses dispositivos podem incluir um roteador reforçado que está fornecendo serviços VPN, um firewall de próxima geração (ASA, na figura), um appliance IPS e um servidor de serviços de autenticação, autorização e contabilidade (AAA) (Servidor AAA, na figura).

A figura retrata uma rede de área do campus. Uma nuvem representando a Internet é conectado a um roteador, rotulado VPN. O roteador VPN está conectado a um ASA firewall. O firewall tem duas conexões adicionais; uma para um IPS e outro para um interruptor. O switch está conectado a um servidor DHCP, servidor de e-mail, e ESA/WSA. O IPS está conectado a um switch multicamadas. O switch multicamadas tem uma conexão a um servidor AAA, bem como a duas camadas 2 e um para outro switch multicamada. O segundo switch multicamadas também tem conexões com os mesmos switches de camada 2, criando redundância. Abaixo do switches de camada 2 são três laptops e três pcs que são rotulados como hosts.


No entanto, muitos ataques se originam de dentro da rede. Portanto, proteger uma LAN interna é quase tão importante quanto proteger o perímetro externo da rede. Sem uma LAN segura, os usuários de uma organização ainda são suscetíveis a ameaças de rede e paralisações que podem afetar diretamente a produtividade e a margem de lucro de uma organização. Depois que um host interno é infiltrado, ele pode se tornar um ponto de partida para um invasor obter acesso a dispositivos críticos do sistema, como servidores e informações confidenciais.

Especificamente, há dois elementos LAN internos para proteger:

- **Endpoints -** Os hosts geralmente consistem em laptops, desktops, impressoras, servidores e telefones IP, todos suscetíveis a ataques relacionados a malware.
- **Infraestrutura de rede -** Dispositivos de infraestrutura de LAN interconectam terminais e normalmente incluem switches, dispositivos sem fio e dispositivos de telefonia IP. A maioria desses dispositivos é suscetível a ataques relacionados à LAN, incluindo ataques de estouro de tabela de endereços MAC, ataques de falsificação, ataques relacionados a DHCP, ataques de tempestade de LAN, ataques de manipulação de STP e ataques de VLAN.
