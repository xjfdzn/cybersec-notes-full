
## NTFS

O sistema de arquivos usado nas versões modernas do  Windows  é o **New Technology File System** ou simplesmente  [NTFS](https://docs.microsoft.com/en-us/windows-server/storage/file-server/ntfs-overview) .

Antes do NTFS, havia  **FAT16/FAT32** (tabela de alocação de arquivos) e **HPFS** (sistema de arquivos de alto desempenho).

Você ainda vê partições FAT em uso hoje. Por exemplo, você normalmente vê partições FAT em dispositivos USB, cartões MicroSD, etc.,  mas tradicionalmente não em computadores/laptops Windows pessoais ou servidores Windows.

NTFS é conhecido como sistema de arquivos com registro em diário. Em caso de falha, o sistema de arquivos pode reparar automaticamente as pastas/arquivos no disco usando informações armazenadas em um arquivo de log. Esta função não é possível com FAT.

O NTFS aborda muitas das limitações dos sistemas de arquivos anteriores; como:

- Suporta arquivos maiores que 4 GB
- Defina permissões específicas em pastas e arquivos
- Compactação de pastas e arquivos
- Criptografia ( [sistema de arquivos criptografados](https://docs.microsoft.com/en-us/windows/win32/fileio/file-encryption) ou **EFS)**

Documentação oficial da Microsoft sobre FAT, HPFS e NTFS [aqui](https://learn.microsoft.com/en-us/troubleshoot/windows-client/backup-and-storage/fat-hpfs-and-ntfs-file-systems) .




## ADS **Alternate Data Streams**

Alternate Data Streams (ADS) é um atributo de arquivo específico para Windows NTFS (New Technology File System).

Cada arquivo possui pelo menos um fluxo de dados ( $DATA) e o ADS permite que os arquivos contenham mais de um fluxo de dados. Nativamente, o Window Explorer não exibe ADS para o usuário. Existem executáveis de terceiros que podem ser usados para visualizar esses dados, mas o Powershell oferece a capacidade de visualizar ADS para arquivos.

Do ponto de vista da segurança, os criadores de malware usaram ADS para ocultar dados.

Nem todos os seus usos são maliciosos. Por exemplo, quando você baixa um arquivo da Internet, existem identificadores gravados no ADS para identificar que o arquivo foi baixado da Internet.

Para saber mais sobre ADS, consulte o seguinte link do MalwareBytes [aqui](https://www.malwarebytes.com/blog/news/2015/07/introduction-to-alternate-data-streams) .



## Informações do Sistema (msinfo32)

Esta ferramenta reúne informações sobre o seu computador e exibe uma visão abrangente do hardware, dos componentes do sistema e do ambiente de software, que você pode usar para diagnosticar problemas do computador


## **Monitor de recursos (resmon)**

Exibe CPU por processo e agregada, memória, disco e informações de uso da rede, além de fornecer detalhes sobre quais processos estão usando identificadores e módulos de arquivos individuais.

## Regedit

É um banco de dados hierárquico central usado para armazenar informações necessárias para configurar o sistema para um ou mais usuários. aplicativos e dispositivos de hardware.

O registro contém informações que o Windows faz referência continuamente durante a operação, como:

- Perfis para cada usuário
- Aplicativos instalados no computador e os tipos de documentos que cada um pode criar
- Configurações da folha de propriedades para pastas e ícones de aplicativos
- Qual hardware existe no sistema
- As portas que estão sendo usadas.

Consulte a seguinte documentação da Microsoft [aqui](https://docs.microsoft.com/en-us/troubleshoot/windows-server/performance/windows-registry-advanced-users) para saber mais sobre o Registro do Windows.




## Firewall

É o que controla o que pode e o que não pode passar pelas portas

(como se fosse um segurança parado na porta, verificando a identificação de tudo que entra e sai)

De acordo com a Microsoft, o Windows Firewall oferece três perfis de firewall

- Domínio - O perfil de domínio se aplica a redes onde o sistema host pode se autenticar em um controlador de domínio.
- Privado - O perfil privado é um perfil atribuído pelo usuário e é usado para designar redes privadas ou domésticas.
- Público - O perfil padrão é o perfil público, usado para designar redes públicas, como pontos de acesso Wi-Fi em cafeterias, aeroportos, e outros locais.

Configurar o **Windows Defender Firewall** destina-se a usuários avançados do Windows. Consulte a seguinte documentação da Microsoft sobre práticas recomendadas [aqui](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-firewall/best-practices-configuring).

Comando para abrir o Firewall do Windows Defender é WF.msc


### Trusted Platform Module (TPM)

Um chip TPM é um processador criptográfico seguro projetado para realizar operações criptográficas. O chip inclui vários mecanismos de segurança física para torná-lo resistente a violações, e o software malicioso não consegue interferir nas funções de segurança do TPM




## **BitLocker**

A Criptografia de Unidade de Disco [[BitLocker]] é um recurso de proteção de dados que se integra ao sistema operacional e aborda as ameaças de roubo ou exposição de dados perdidos, roubados ou desativados inadequadamente

O BitLocker oferece maior proteção quando usado com um Trusted Platform Module (TPM) versão 1.2 ou posterior



## Powershell
O [[Powershell]] é uma solução de automação de tarefas multiplataforma que consiste em um shell de linha de comando, em uma linguagem de script e uma estrutura de gerenciamento de configuração. O PowerShell pode ser executado no Windows, Linux e macOS.



## Netstat

[[netstat]]

## Cmd

[[cmd.exe]]



## Volume Shadow Copy Service

As cópias de sombra de volume são armazenadas na pasta System Volume Information em cada unidade com proteção habilitada.

Se o VSS estiver ativado (Proteção do sistema ativada), você poderá executar as seguintes tarefas em configurações avançadas do sistema.

- Crie um ponto de restauração
    
- Execute a restauração do sistema
    
- Definir configurações de restauração
    
- Excluir pontos de restauração
    

---

- [Antimalware Scan Interface](https://docs.microsoft.com/en-us/windows/win32/amsi/antimalware-scan-interface-portal)
- [Credential Guard](https://docs.microsoft.com/en-us/windows/security/identity-protection/credential-guard/credential-guard-manage)
- [Windows 10 Hello]([https://support.microsoft.com/en-us/windows/learn-about-windows-hello-and-set-it-up-dae28983-8242-bb2a-d3d1-87c9d265a5f0#:~:text=Windows 10,in with just your PIN.)](https://support.microsoft.com/en-us/windows/learn-about-windows-hello-and-set-it-up-dae28983-8242-bb2a-d3d1-87c9d265a5f0#:~:text=Windows%2010,in%20with%20just%20your%20PIN.))
- [CSO Online - The best new Windows 10 security features](https://www.csoonline.com/article/3253899/the-best-new-windows-10-security-features.html)