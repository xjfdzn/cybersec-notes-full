# Ataques em Apps

## XSS
1. Os criminosos exploram a vulnerabilidade XSS ao injetar scripts que contêm código mal-intencionado em uma página da Web.
2. A página da Web é acessada pela vítima, e os scripts mal-intencionados passam inadvertidamente para o navegador.
3. O script mal-intencionado pode acessar cookies, tokens de sessão ou outras informações confidenciais sobre o usuário, que são enviadas de volta ao criminoso digital.
4. Com essas informações, o criminoso digital pode se passar por um usuário.


Nem todos os ataques são iniciados do lado do servidor. Cross-Site Scripting (XSS) é onde as páginas da Web executadas no lado do cliente, dentro de seu próprio navegador da Web, são injetadas com scripts mal-intencionados. Esses scripts podem ser usados pelo Visual Basic, JavaScript e outros para acessar um computador, coletar informações confidenciais ou implantar mais ataques e espalhar malware. Tal como acontece com a injeção de SQL, isso é muitas vezes devido ao invasor postar conteúdo em um site confiável com falta de validação de entrada. Os futuros visitantes do Web site fidedigno serão expostos ao conteúdo fornecido pelo intruso.

Estes são os dois tipos principais de XSS:

- **Armazenado (persistente) -** Isso é armazenado permanentemente no servidor infectado e é recebido por todos os visitantes da página infectada.
- **Refletido (não persistente) -** Isso requer apenas que o script mal-intencionado esteja localizado em um link e os visitantes devem clicar no link infectado para se infectarem.

Estas são algumas maneiras de prevenir ou reduzir ataques XSS:

- Certifique-se de que os desenvolvedores de aplicativos da Web estejam cientes das vulnerabilidades XSS e de como evitá-las.
- Use uma implementação IPS para detectar e evitar scripts mal-intencionados.
- Use um proxy da Web para bloquear sites mal-intencionados.
- Use um serviço como o Cisco Umbrella para impedir que os usuários naveguem para sites conhecidos por serem mal-intencionados.
- Tal como acontece com todas as outras medidas de segurança, certifique-se de educar os usuários finais. Ensine-os a identificar ataques de phishing e notificar o pessoal da Infosec quando suspeitar de qualquer coisa relacionada à segurança.


---

## **Code Injection**

- XML Injection
    
    Um ataque de injeção de XML pode corromper os dados no banco de dados XML e ameaçar a segurança do site.
    
    Ele funciona ao interferir no processamento de dados XML ou na consulta de uma aplicação inserida por um usuário.
    
    Hackers podem manipular essa consulta ao programá-la para atender às suas necessidades. Isso concederá a eles acesso a todas as informações confidenciais armazenadas no banco de dados e permitirá que eles façam qualquer alteração no site.
    
- [[SQL Injection]]
    
    É possível realizar um ataque de injeção de SQL em sites ou em qualquer banco de dados SQL inserindo uma instrução SQL mal-intencionada em um campo de entrada.
    
    Esse ataque aproveita uma vulnerabilidade na qual o aplicativo não filtra corretamente os dados inseridos por um usuário por caracteres em uma instrução SQL.
    
    Como resultado, o criminoso digital pode obter acesso não autorizado a informações armazenadas no banco de dados, das quais pode falsificar uma identidade, modificar dados atuais, destruir dados ou até mesmo se tornar um administrador do próprio servidor de banco de dados.



	Um dos ataques de banco de dados mais comuns é o ataque de injeção SQL. O ataque de injeção SQL consiste em inserir uma consulta SQL através dos dados de entrada do cliente para o aplicativo. Uma exploração de injeção SQL bem-sucedida pode ler dados confidenciais do banco de dados, modificar dados do banco de dados, executar operações de administração no banco de dados e, às vezes, emitir comandos para o sistema operacional.

	A menos que um aplicativo use validação rigorosa de dados de entrada, ele será vulnerável ao ataque de injeção SQL. Se um aplicativo aceitar e processar dados fornecidos pelo usuário sem qualquer validação de dados de entrada, um ator de ameaça poderá enviar uma string de entrada criada com intuito malicioso para acionar o ataque de injeção SQL.

	Os analistas de segurança devem ser capazes de reconhecer consultas SQL suspeitas para detectar se o banco de dados relacional foi submetido a ataques de injeção SQL. Eles precisam ser capazes de determinar qual ID de usuário foi usado pelo ator da ameaça para fazer login e, em seguida, identificar qualquer informação ou acesso adicional que o ator da ameaça poderia ter aproveitado após um login bem-sucedido.






    
- DLL Injection
    
    Um arquivo Dynamic Link Library (DLL) é uma biblioteca que contém um conjunto de códigos e dados para realizar uma determinada atividade no Windows. Os aplicativos usam esse tipo de arquivo para adicionar funcionalidades não incorporadas, quando precisam realizar essa atividade.
    
    A injeção de DLL permite que um criminoso digital engane um aplicativo para chamar um arquivo DLL mal-intencionado, que é executado como parte do processo de destino.
    
- LDAP Injection
    
    O Protocolo de acesso ao diretório leve (LDAP) é um protocolo aberto para autenticar o acesso do usuário a serviços de diretório.
    
    Um ataque de injeção de LDAP explora vulnerabilidades de validação de entrada ao injetar e executar consultas a servidores LDAP, dando aos criminosos digitais a oportunidade de extrair informações confidenciais do diretório LDAP de uma empresa.
    

## Outros Ataques

- **Cross-Site-Request-Forgery (CSRF)**
    O CSRF descreve a exploração mal-intencionada de um site onde os comandos não autorizados são enviados do navegador de um usuário para um aplicativo da Web confiável.
    
    Um site mal-intencionado pode transmitir esses comandos por meio de marcas de imagem, formulários ocultos ou solicitações de JavaScript especialmente criadas, que podem funcionar sem o conhecimento do usuário.
    
- **Race Condition Attack**
    Também conhecido como TOC (tempo de verificação) ou tempo de uso (TOU), um ataque de condição de corrida acontece quando um sistema de computação projetado para lidar com tarefas em uma sequência específica é forçado a executar duas ou mais operações simultaneamente.
    
    Por exemplo, os sistemas operacionais são compostos de segmentos, a menor sequência de instruções do programa necessária para realizar um processo. Quando dois ou mais encadeamentos acessam dados compartilhados e tentam alterá-los ao mesmo tempo, ocorre um ataque de condição de corrida.
    
- **Improper input handling Attack**
    Os dados inseridos por um usuário que não é validado corretamente podem afetar o fluxo de dados de um programa e causar vulnerabilidades críticas em sistemas e aplicativos que resultam em estouro de buffer ou ataques de injeção de SQL.
    
- **Error handling Attack**
    Os invasores podem usar mensagens de erro para extrair informações específicas, como nomes de host de sistemas internos e diretórios ou arquivos que existem em um determinado servidor Web, bem como nomes de bancos de dados, tabelas e campos que podem ser usados para criar ataques de injeção de SQL.
    
- **API Attack**
    Uma API fornece uma resposta do usuário para um sistema e envia a resposta do sistema de volta para o usuário. Um ataque de API ocorre quando um criminoso digital abusa de um endpoint de API.
    
- **Replay Attack**
    Isso descreve uma situação em que uma transmissão de dados válida é repetida ou retardada de forma mal-intencionada ou fraudulenta por um invasor, que intercepta, altera e reenvia os dados para que o destinatário faça o que quiser.
    
- **Directory Traversal Attack**
    A passagem de diretório ocorre quando um invasor é capaz de ler arquivos no servidor da Web fora do diretório do site. Um invasor pode usar essas informações para baixar arquivos de configuração do servidor que contêm informações confidenciais, expor potencialmente mais vulnerabilidades do servidor ou até mesmo assumir o controle do servidor!
    
- **Resource Exhausting Attack**
    Esses ataques são exploits de segurança de computadores que travam, paralisam ou interferem em um programa ou sistema específico. Em vez de sobrecarregar a largura de banda de rede como um ataque de DoS, os ataques de exaustão de recursos sobrecarregam os recursos de hardware disponíveis no servidor de destino.


# **Defesa Contra Ataques de Aplicativos**

Existem várias ações que você pode tomar para se defender contra um ataque de aplicativo. Você encontrará alguns deles descritos aqui.

- A primeira linha de defesa contra um ataque de aplicativo é escrever um código sólido.
- Prática prudente de programação envolve tratar e validar todas as entradas de fora de uma função como se fosse hostil.
- Mantenha todos os softwares atualizados, incluindo os sistemas operacionais e aplicativos, e não ignore os prompts de atualização. Nem todos os programas são atualizados automaticamente.

---

## SPAM

## Phishing
O phishing ocorre quando um usuário é contatado por e-mail ou mensagem instantânea - ou de qualquer outra forma - por alguém que se disfarça de pessoa ou empresa legítima. A intenção é induzir o destinatário a instalar malware em seu dispositivo ou compartilhar informações pessoais, como credenciais de login ou informações financeiras.

Por exemplo, você recebe um e-mail parabenizando você por ganhar um prêmio. Parece que ele foi enviado de uma loja conhecida e pede para você clicar em um link para reivindicar o prêmio. Na verdade, esse link pode redirecioná-lo para um site falso que solicita a inserção de seus dados pessoais ou até mesmo instalar um vírus no seu dispositivo.

## Spear Phishing
Um ataque altamente direcionado, o spear phishing envia e-mails personalizados para uma pessoa específica com base nas informações que o invasor conhece sobre elas, que podem ser seus interesses, preferências, atividades e projetos de trabalho.













---
### Vishing
Muitas vezes chamado de phishing de voz, esse tipo de ataque faz com que os criminosos usem a tecnologia de comunicação por voz para incentivar os usuários a divulgar informações, como detalhes do cartão de crédito.

Os criminosos podem imitar chamadas telefônicas usando o protocolo de voz sobre internet (VoIP) ou deixar mensagens gravadas para dar a impressão de que são chamadas legítimas.

### Pharming
Esse tipo de ataque direciona deliberadamente os usuários para uma versão falsa de um site oficial. Enganados com a crença de que estão conectados a um site legítimo, os usuários inserem suas credenciais no site fraudulento.

### Whaling
Whaling é um ataque de phishing que buscam vítimas de alto perfil em uma empresa, como executivos seniores.

---