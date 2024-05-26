## Introdução

Um Centro de Operações de Segurança (SOC) é a instalação onde a equipe de segurança da informação monitora e analisa constantemente a segurança de uma empresa. O principal objetivo da equipe SOC é detectar, analisar e responder a incidentes de segurança cibernética por meio de tecnologia, pessoas e processos. Também implementa medidas para proteger os ativos digitais da organização.

Monitoram constantemente logs, alertas e atividades suspeitas para identificar e mitigar ameaças em tempo real.

![[Pasted image 20240301122149.png]]


Tipos de SOC

- SOC Interno
    
    A empresa constrói sua própria equipe de segurança cibernética.
    
- SOC Virtual
    
    Quando a equipe de segurança não possui escritórios e muitas vezes trabalha remotamente em locais diferentes.
    
- SOC Co-Gerenciado
    
    Pessoal interno do SOC trabalhando com um provedor de serviços de segurança gerenciados (MSSP) externo. (Consultoria)
    
- Command SOC
    
    Um grupo sênior que supervisiona SOCs menores em uma grande região.


## Pessoas, Processos, Tecnologia
Construir um SOC bem-sucedido requer uma coordenação séria. Em particular, deve haver uma forte relação entre pessoas, processos e tecnologias.

### **Pessoas**
Precisamos de pessoal altamente treinado e familiarizado com alertas de segurança e cenários de ataque. Como os tipos de ataque mudam constantemente, precisamos de um companheiro de equipe que possa se adaptar facilmente a novos tipos de ataque e que esteja disposto a fazer pesquisas.

### **Processos**
Para levar sua estrutura SOC a uma boa maturidade, você precisa alinhá-la com muitos tipos diferentes de requisitos de segurança, como NIST, PCI e HIPAA. Os processos exigem extrema padronização de ações para garantir que nada seja ignorado.

### **Tecnologia**
Você precisa ter vários produtos para muitos tópicos, como testes de penetração, detecção, prevenção e análise. Você precisa acompanhar de perto o mercado e a tecnologia para encontrar a melhor solução para você. Às vezes, o melhor produto do mercado pode não ser o melhor para você. Isso pode ser devido ao seu baixo orçamento.


## Áreas do SOC

- **Analista SOC**
    
    Pode ser dividido em grupos como Nível 1, 2 e 3 de acordo com a estrutura do SOC. Um analista de segurança classifica o alerta, procura a causa e aconselha sobre medidas corretivas.
    
- **Respondente de Incidentes**
    
    O oficial de resposta a incidentes é a pessoa que participará da detecção de ameaças. Essa pessoa realiza a avaliação inicial das violações de segurança.
    
- **Threat Hunter (Caçador de Ameaças)**
    
    Um Threat Hunter é um profissional de segurança cibernética que procura e investiga proativamente ameaças e vulnerabilidades potenciais na rede ou sistema de uma organização. Eles usam uma combinação de técnicas manuais e automatizadas para detectar, isolar e mitigar ameaças persistentes avançadas (APTs) e outros ataques sofisticados que podem escapar das medidas de segurança tradicionais. Os caçadores de ameaças normalmente têm um conhecimento profundo da infraestrutura de TI e da postura de segurança da organização, bem como conhecimento de ameaças emergentes e táticas de ataque. Seu objetivo é detectar e eliminar ameaças antes que elas causem danos ou interrupções aos negócios.
    
- **Security Engineer**
    
    Os engenheiros de segurança mantêm a infraestrutura de segurança das soluções SIEM (Security Information and Event Management) e dos produtos SOC. Por exemplo, essa pessoa prepara a conexão entre os produtos SIEM e SOAR (orquestração, automação e resposta de segurança).
    
- **SOC Manager**
    
    Um gerente SOC assume responsabilidades de gerenciamento, como orçamento, elaboração de estratégias, gerenciamento de pessoal e coordenação de operações. Ele / ela lida com questões operacionais e não técnicas.



Ao longo do dia, um analista SOC geralmente examinará os alertas no SIEM e determinará quais são ameaças reais. Para chegar a uma conclusão, ele utilizará vários produtos de segurança, como EDR (Endpoint Detection and Response), Log Management e SOAR. Explicaremos em detalhes por que e como esses produtos são usados posteriormente no programa de treinamento.

Para ser um analista SOC bem-sucedido, que não dependa de produtos de segurança e possa analisar corretamente os alertas SIEM, é necessário ter as seguintes competências.

> S.O

> Redes

> Análise de Malware

---

## Gerenciamento de Logs

Como o nome indica, é uma solução de gerenciamento de log. Resumindo, permite o acesso a todos os logs de um ambiente (logs web, logs do sistema operacional, Firewall, Proxy, EDR, etc.) e permite o gerenciamento desses logs a partir de um único ponto. Assim, economiza tempo.

Se não pudermos acessar os logs de um ponto, então a mesma consulta (por exemplo, quero determinar todos os usuários em [letsdefend.io](http://letsdefend.io)) precisará ser enviada para vários dispositivos. Isso aumentaria nossa margem de erro e a quantidade de tempo que precisamos gastar.


## Erros Comums

- Dependendo excessivamente dos resultados do VirusTotal
    
    Às vezes podemos confiar no resultado exibido na tela verde do VirusTotal após analisar a URL de um arquivo e verificar se o endereço é inofensivo. Mas existe um novo software malicioso desenvolvido usando uma técnica AV (AntiVirus) Bypass que pode não ser detectado pelo VT (VirusTotal). Por esta razão, devemos aceitar o VirusTotal como uma ferramenta de apoio e conduzir as nossas análises tendo isto em mente.
    
    Aqui está uma postagem de blog detalhada relacionada ao assunto para leitura adicional: [VirusTotal não é um respondedor de incidentes](https://medium.com/maverislabs/virustotal-is-not-an-incident-responder-80a6bb687eb9)
    
- Análise apressada de malware em uma sandbox
    
    Uma análise de 3 a 4 minutos em um ambiente sandbox nem sempre pode produzir resultados precisos. Aqui estão os motivos:
    
    Malware que detecta um ambiente sandbox e não se ativa
    
    Malware que não é ativado até 10 a 15 minutos após a operação
    
    Por esta razão, a duração da análise deve ser a maior possível e, se possível, deve ocorrer num ambiente real.
    
- Análise de log insuficiente
    
    De vez em quando vemos que as análises de log não são realizadas corretamente. Por exemplo, digamos que um malware detectou um dispositivo com o nome de host “LetsDefend” e esse malware está enviando dados secretamente para o endereço “[letsdefend.io](http://letsdefend.io)”. Como analista SOC, devemos utilizar soluções de “Gerenciamento de Log” para determinar se algum outro dispositivo está tentando se conectar a este endereço.
    
- Ignorando as datas do VirusTotal
    
    Se a pesquisa que você realizou no VirusTotal já foi consultada antes, um resultado do cache será exibido.