Você também pode verificar quais portas estão abertas, onde elas estão conectadas e qual é seu status atual digitando **netstat**


Quando o malware está presente em um computador, ele geralmente abre portas de comunicação no host para enviar e receber dados. O comando **netstat** pode ser usado para procurar conexões de entrada ou saída não autorizadas. Quando usado sozinho, o comando **netstat** exibirá todas as conexões TCP ativas.

Examinando essas conexões, é possível ver quais dos programas estão escutando conexões que não estão autorizadas. 

Para facilitar esse processo, você pode vincular as conexões aos processos em execução que as criaram no Gerenciador de Tarefas. Para fazer isso, abra um prompt de comando com privilégios administrativos e digite o comando **netstat -abno**, conforme mostrado na saída do comando.


#### Documentação
https://learn.microsoft.com/pt-br/windows-server/administration/windows-commands/netstat