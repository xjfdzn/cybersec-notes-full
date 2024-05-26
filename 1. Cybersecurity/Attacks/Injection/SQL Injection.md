É possível realizar um ataque de injeção de SQL em sites ou em qualquer banco de dados SQL inserindo uma instrução SQL mal-intencionada em um campo de entrada.

Esse ataque aproveita uma vulnerabilidade na qual o aplicativo não filtra corretamente os dados inseridos por um usuário por caracteres em uma instrução SQL.

Como resultado, o criminoso digital pode obter acesso não autorizado a informações armazenadas no banco de dados, das quais pode falsificar uma identidade, modificar dados atuais, destruir dados ou até mesmo se tornar um administrador do próprio servidor de banco de dados.



Um dos ataques de banco de dados mais comuns é o ataque de injeção SQL. O ataque de injeção SQL consiste em inserir uma consulta SQL através dos dados de entrada do cliente para o aplicativo. Uma exploração de injeção SQL bem-sucedida pode ler dados confidenciais do banco de dados, modificar dados do banco de dados, executar operações de administração no banco de dados e, às vezes, emitir comandos para o sistema operacional.

A menos que um aplicativo use validação rigorosa de dados de entrada, ele será vulnerável ao ataque de injeção SQL. Se um aplicativo aceitar e processar dados fornecidos pelo usuário sem qualquer validação de dados de entrada, um ator de ameaça poderá enviar uma string de entrada criada com intuito malicioso para acionar o ataque de injeção SQL.

Os analistas de segurança devem ser capazes de reconhecer consultas SQL suspeitas para detectar se o banco de dados relacional foi submetido a ataques de injeção SQL. Eles precisam ser capazes de determinar qual ID de usuário foi usado pelo ator da ameaça para fazer login e, em seguida, identificar qualquer informação ou acesso adicional que o ator da ameaça poderia ter aproveitado após um login bem-sucedido.





----

O que seria o comando modificado abaixo?

```
1' OR 1=1 UNION SELECT null, column_name FROM INFORMATION_SCHEMA.columns WHERE table_name='users'
```

R: O banco de dados responderia com uma saída muito mais curta filtrada pela ocorrência da palavra “usuários”.



consulta em uma caixa de pesquisa UserID no destino 10.0.2.15 para obter nomes de usuário e hashes de senha!
```
1'ou 1=1 union select user, password from users#
```



Site para quebrar Hash de Senha
https://crackstation.net

----

Dicas para evitar SQL Injection

- Filtrar a entrada do usuário
 - Implantar um firewall de aplicativo Web
 - Desativar recursos/recursos desnecessários do banco de dados
 - Monitorar instruções SQL
 - Usar parâmetros com procedimentos armazenados 
 - Usar parâmetros com SQL dinâmico.