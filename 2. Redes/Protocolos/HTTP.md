










----
#### Exploits HTTP
- **IFrames maliciosos**

Os atores de ameaças costumam usar quadros inline maliciosos (iFrames). *Um iFrame é um elemento HTML que permite que o navegador carregue outra página da Web a partir de outra fonte.* Os ataques de iFrame tornaram-se muito comuns, pois são frequentemente usados para inserir **anúncios** de outras fontes na página. Os atores de ameaças comprometem um servidor da Web e modificam páginas da Web adicionando **HTML** para o iFrame malicioso. O HTML vincula ao servidor da web do hacker. Em alguns casos, a página IFrame carregada consiste em apenas alguns pixels. Isso torna muito difícil para o usuário ver. Como o iFrame é executado na página, ele pode ser usado para fornecer uma exploração mal-intencionada, como **publicidade de spam**, um **kit de exploração e outros malwares**.

Estas são algumas das maneiras de prevenir ou reduzir iFrames maliciosos:

- Use um proxy da Web para bloquear sites mal-intencionados.
- Como os invasores geralmente alteram o HTML de origem do iFrame em um site comprometido, verifique se os desenvolvedores da Web não usam iFrames. Isso isolará qualquer conteúdo de sites de terceiros e facilitará a localização de páginas modificadas.
- Use um serviço como o Cisco Umbrella para impedir que os usuários naveguem para sites conhecidos por serem mal-intencionados.
- Certifique-se de que o usuário final entenda o que é um iFrame. Hackers costumam usar esse método em ataques baseados na Web.

----

- **Amortecimento HTTP 302** 


Outro tipo de ataque HTTP é o ataque de amortecimento HTTP 302. Os atores de ameaças usam o código de status de resposta 302 Found HTTP para direcionar o navegador da Web do usuário para um novo local. Os atores de ameaças costumam usar funções HTTP legítimas, como redirecionamentos HTTP para realizar seus ataques. HTTP permite que os servidores redirecionem a solicitação HTTP de um cliente para um servidor diferente. O redirecionamento HTTP é usado, por exemplo, quando o conteúdo da Web é movido para um URL ou nome de domínio diferente. Isso permite que URLs e marcadores antigos continuem a funcionar. Portanto, os analistas de segurança devem entender como uma função como o redirecionamento HTTP funciona e como ela pode ser usada durante ataques.

Quando a resposta do servidor é um status 302 Encontrado, ele também fornece a URL no campo de localização. O navegador acredita que o novo local é o URL fornecido no cabeçalho. O navegador é convidado a solicitar este novo URL. Esta função de redirecionamento pode ser usada várias vezes até que o navegador finalmente pouse na página que contém o exploit. Os redirecionamentos podem ser difíceis de detectar devido ao fato de que redirecionamentos legítimos ocorrem frequentemente na rede.

Estas são algumas maneiras de evitar ou reduzir ataques de amortecimento HTTP 302:

- Use um proxy da Web para bloquear sites mal-intencionados.
- Use um serviço como o Cisco Umbrella para impedir que os usuários naveguem para sites conhecidos por serem mal-intencionados.
- Certifique-se de que o usuário final entenda como o navegador é redirecionado por meio de uma série de redirecionamentos HTTP 302.

----


- **Sombreamento de domínio** 


Quando um hacker deseja criar um ataque de sombreamento de domínio, ele deve primeiro comprometer um **domínio**. Em seguida, o ator de ameaça deve criar vários subdomínios desse domínio para ser usado para os ataques. Logins de registro de domínio seqüestrados são usados para criar os muitos subdomínios necessários. Depois que esses subdomínios tiverem sido criados, os invasores podem usá-los como quiserem, mesmo que sejam encontrados domínios mal-intencionados. Eles podem simplesmente fazer mais do domínio pai. A sequência a seguir é normalmente usada por atores de ameaça:

1. Um site fica comprometido.
2. O amortecimento HTTP 302 é usado para enviar o navegador para sites maliciosos.
3. O sombreamento de domínio é usado para direcionar o navegador para um servidor comprometido.
4. Uma página inicial do kit de exploração é acessada.
5. Downloads de malware da página inicial do kit de exploração.

Estas são algumas maneiras de prevenir ou reduzir ataques de sombreamento de domínio:

- Proteja todas as contas de proprietário do domínio. Use senhas fortes e use autenticação de dois fatores para proteger essas contas poderosas.
- Use um proxy da Web para bloquear sites mal-intencionados.
- Use um serviço como o Cisco Umbrella para impedir que os usuários naveguem para sites conhecidos por serem mal-intencionados.
- Certifique-se de que os proprietários de domínio validem as suas contas de registo e procure quaisquer subdomínios que não tenham autorizado.

---
