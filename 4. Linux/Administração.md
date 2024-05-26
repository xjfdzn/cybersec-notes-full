
Arquivos de configuração de serviço

No Linux, os serviços são gerenciados usando arquivos de configuração. As opções comuns nos arquivos de configuração são o número da porta, a localização dos recursos hospedados e os detalhes da autorização do cliente. Quando o serviço é iniciado, ele procura seus arquivos de configuração, carrega-os na memória e se ajusta de acordo com as configurações nos arquivos. As modificações do arquivo de configuração geralmente exigem a reinicialização do serviço antes que as alterações entrem em vigor.

Como os serviços geralmente exigem privilégios de superusuário para serem executados, os arquivos de configuração de serviço geralmente exigem privilégios de superusuário para editar.

A saída do comando mostra uma parte do arquivo de configuração do Nginx, que é um servidor web leve para Linux.

