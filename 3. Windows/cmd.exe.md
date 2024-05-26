Para abrir a CLI do Windows, procure **cmd.exe**.

O prompt exibe o local atual dentro do sistema de arquivos. Estas são algumas coisas a serem lembradas ao usar a CLI:

- Os nomes de arquivo e caminhos não diferenciam maiúsculas de minúsculas, por padrão.
- Os dispositivos de armazenamento recebem uma letra para referência. Isto seguido por dois pontos e barra invertida (\). Isso indica a raiz, ou o nível mais alto, do dispositivo. A hierarquia de pastas e arquivos no dispositivo é indicada separando-as com a barra invertida. Por exemplo, o caminho C:∖Users∖Jim∖Desktop∖file.txt se refere a um arquivo chamado file.txt que está na pasta Desktop dentro da pasta Jim dentro da pasta Users na raiz da unidade C:.
- Comandos que têm opções opcionais usam a barra (/) para delinear entre o comando e a opção switch.
- Para alternar entre dispositivos de armazenamento, digite a letra do dispositivo, seguida de dois pontos e pressione **Enter**.

A CLI não pode funcionar em conjunto com o núcleo do Windows ou a Interface Grafica


---

#### NET
O Windows tem muitos comandos que podem ser inseridos na linha de comando. Um comando importante é o comando **net**, que é usado na administração e manutenção do SO. 

Para ver uma lista dos vários comandos **net**, digite **net help** no prompt de comando. A saída do comando mostra os comandos que o comando **net** pode usar.


NET ACCOUNTS - Define os requisitos de senha e logon para usuários
NET USER - Mostra os usuários da maquina
NET SESSION - Lista ou desconecta sessões entre um computador e outros computadores na rede
NET SHARE - Cria, remove ou gerencia recursos compartilhados
NET  START - Inicia um serviço de rede ou lista os serviços de rede em execução
NET STOP - Para um serviço de rede
NET USE - Conecta, desconecta e exibe informações sobre recursos de rede compartilhados
NET VIEW - Mostra uma lista de computadores e dispositivos de rede na rede

#### nslookup
O Sistema de Nomes de Domínio (DNS) também deve ser testado porque é essencial encontrar o endereço dos hosts traduzindo-o a partir de um nome, como uma URL. Use o comando **nslookup** para testar o DNS. Digite **nslookup cisco.com** no prompt de comando para encontrar o endereço do servidor da Web Cisco

