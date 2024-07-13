
A ideia principal por trás de um domínio é centralizar a administração de componentes comuns de uma rede de computadores Windows em um único repositório chamado **Active Directory** (<span style="color:rgb(146, 208, 80)">AD</span>)

O servidor que <span style="color:rgb(146, 208, 80)">executa os serviços do Active Directory</span> é conhecido como um **Domain Controller**   (<span style="color:rgb(146, 208, 80)">DC</span>)

---
#### <span style="color:rgb(0, 176, 240)">Beneficios</span>

- Todos os usuários na rede podem ser configurados a partir do Active Directory com o mínimo de esforço

- Configurar políticas de segurança diretamente do Active Directory e aplicá-las a usuários e computadores na rede, conforme necessário.


----

#### <span style="color:rgb(0, 176, 240)">Usuarios</span>

Usuários Comuns: Funcionários ou pessoas da organização

Usuários de Serviço: ISS ou MySQL. Cada serviço individual requer um usuário para ser executado, mas os usuários de serviço são diferentes dos usuários comuns, pois eles terão apenas os privilégios necessários para executar seu serviço próprio serviço.


#### <span style="color:rgb(0, 176, 240)">Máquinas</span>

Para cada computador que se junta ao domínio do Active Directory, um objeto de máquina será criado
Máquinas também são consideradas "entidades de segurança" e recebem uma conta, assim como qualquer usuário regular

Identificar contas de máquina é relativamente fácil. Elas seguem um esquema de nomenclatura específico. O nome da conta de máquina é o nome do computador seguido por um cifrão. Por exemplo, uma máquina chamada <span style="color:rgb(146, 208, 80)">DC01</span> terá uma conta de máquina chamada <span style="color:rgb(146, 208, 80)">DC01$</span>.


#### <span style="color:rgb(0, 176, 240)">Grupos de Segurança</span>

| **Grupo de Segurança**     | **Descrição**                                                                                                                                                   |
| -------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Administradores de domínio | Usuários deste grupo têm privilégios administrativos sobre todo o domínio. Por padrão, eles podem administrar qualquer computador no domínio, incluindo os DCs. |
| Operadores de Servidor     | Usuários neste grupo podem administrar Controladores de Domínio. Eles não podem alterar nenhuma associação de grupo administrativo.                             |
| Operadores de backup       | Usuários neste grupo têm permissão para acessar qualquer arquivo, ignorando suas permissões. Eles são usados ​​para executar backups de dados em computadores.  |
| Operadores de conta        | Usuários neste grupo podem criar ou modificar outras contas no domínio.                                                                                         |
| Usuários de domínio        | Inclui todas as contas de usuário existentes no domínio.                                                                                                        |
| Computadores de Domínio    | Inclui todos os computadores existentes no domínio.                                                                                                             |
| Controladores de Domínio   | Inclui todos os DCs existentes no domínio.                                                                                                                      |
Lista completa de grupos de segurança padrão na [documentação da Microsoft](https://docs.microsoft.com/en-us/windows/security/identity-protection/access-control/active-directory-security-groups) 


#### <span style="color:rgb(0, 176, 240)">Usuários e computadores do Active Directory</span>

Isso abrirá uma janela onde você pode ver a hierarquia de usuários, computadores e grupos que existem no domínio. Esses objetos são organizados em **Unidades Organizacionais (<span style="color:rgb(146, 208, 80)">OU</span>)

<span style="color:rgb(146, 208, 80)">OU</span>: São objetos de contêiner que permitem classificar usuários e máquinas. OUs são usadas principalmente para definir conjuntos de usuários com requisitos de policiamento semelhantes
- Um usuário só pode fazer parte de uma única OU por vez

![[Pasted image 20240713152801.png]]

Você provavelmente já notou que há outros contêineres padrão além do THM OU . Esses contêineres são criados pelo Windows automaticamente e contêm o seguinte:

- **Integrado:** contém grupos padrão disponíveis para qualquer host Windows.
- **Computadores:** Qualquer máquina que se junte à rede será colocada aqui por padrão. Você pode movê-las se necessário.
- **Controladores de domínio:** UO padrão que contém os DCs na sua rede.
- **Usuários:** usuários e grupos padrão que se aplicam a um contexto de todo o domínio.
- **Contas de serviço gerenciadas:** contém contas usadas por serviços no seu domínio do Windows.


- <span style="color:rgb(146, 208, 80)">OUs</span> são úteis para  aplicar políticas a usuários e computadores, que incluem configurações específicas que pertencem a conjuntos de usuários dependendo de sua função específica na empresa. Lembre-se, um usuário só pode ser membro de uma única OU por vez, pois não faria sentido tentar aplicar dois conjuntos diferentes de políticas a um único usuário.

- <span style="color:rgb(146, 208, 80)">Security Groups</span> , por outro lado, são usados ​​para conceder permissões sobre recursos . Por exemplo, você usará grupos se quiser permitir que alguns usuários acessem uma pasta compartilhada ou impressora de rede. Um usuário pode fazer parte de muitos grupos, o que é necessário para conceder acesso a vários recursos.


#### <span style="color:rgb(0, 176, 240)">Deletar OUs</span>

Por padrão, as OUs são protegidas contra exclusão acidental. Para excluir a OU , precisamos habilitar os **Recursos Avançados** no menu <span style="color:rgb(146, 208, 80)">View</span>

Após isso, clique com o botão direito do mouse na OU e vá para <span style="color:rgb(146, 208, 80)">Propriedades</span>. Você encontrará uma caixa de seleção na guia <span style="color:rgb(146, 208, 80)">Objeto</span> para desabilitar a proteção, e então consegue excluir a OU


#### <span style="color:rgb(0, 176, 240)">Delegação</span>

Delegação é permitir que você conceda a usuários privilégios específicos para executar tarefas avançadas em OUs sem precisar de um Administrador de Domínio para intervir.

Por exemplo: Um dos casos de uso mais comuns para isso é conceder a OU `IT support`privilégios para redefinir senhas de outros usuários com privilégios baixos. De acordo com nosso organograma, Phillip é responsável pelo suporte de TI, então provavelmente gostaríamos de delegar a ele o controle de redefinição de senhas sobre as OUs de Vendas, Marketing e Gerenciamento.

![[Pasted image 20240713165819.png]]

Em seguida você seleciona o usuário ou grupo para Delegation

![[Pasted image 20240713170000.png]]

Seleciona as permissões que ele vai ter perante a essa OU

![[Pasted image 20240713165949.png]]
Clique em next e Finish

Alterar senha de usuário via Powershell

```
Set-ADAccountPassword [nome_do_usuario] -Reset -NewPassword (Read-Host -AsSecureString -Prompt 'New Password') -Verbose
```


#### <span style="color:rgb(0, 176, 240)">Gerenciamento de Computadores no AD</span>

Embora não haja uma regra de ouro sobre como organizar suas máquinas, um excelente ponto de partida é segregar dispositivos de acordo com seu uso. Em geral, você esperaria ver dispositivos divididos em pelo menos as três categorias a seguir:

**1. <span style="color:rgb(0, 176, 240)">Estações de trabalho</span>

As estações de trabalho são um dos dispositivos mais comuns dentro de um domínio do Active Directory. Cada usuário no domínio provavelmente fará login em uma estação de trabalho. Este é o dispositivo que eles usarão para fazer seu trabalho ou atividades normais de navegação. Esses dispositivos nunca devem ter um usuário privilegiado conectado a eles.  

**2. <span style="color:rgb(0, 176, 240)">Servidores</span>

Servidores são o segundo dispositivo mais comum dentro de um domínio do Active Directory. Servidores são geralmente usados ​​para fornecer serviços a usuários ou outros servidores.

**3. <span style="color:rgb(0, 176, 240)">Controladores de Domínio</span>

Controladores de Domínio são o terceiro dispositivo mais comum dentro de um domínio do Active Directory. Controladores de Domínio permitem que você gerencie o Domínio do Active Directory. Esses dispositivos são frequentemente considerados os dispositivos mais sensíveis dentro da rede, pois contêm senhas com hash para todas as contas de usuário dentro do ambiente.

Já que estamos arrumando nosso AD, vamos criar duas OUs separadas para `Workstations`e `Servers`(Controladores de Domínio já estão em uma OU criada pelo Windows). Nós os criaremos diretamente sob o `thm.local`contêiner de domínio. No final, você deve ter a seguinte estrutura de OU :