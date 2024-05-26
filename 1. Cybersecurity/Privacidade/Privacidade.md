https://www.youtube.com/watch?v=MlW-drLiOQA


#### Tails








#### Cover Your Tracks
Acessando o [Coveryourtracks](https://coveryourtracks.eff.org/) é possível descobrir o quanto de dados estão sendo vazados pelo navegador quando acessamos um site.

**Impressão Digital** é a Técnica usada pra coletar informações do nosso navegador e dispositivos de usuário, como S.O, resolução da tela, fuso horário, entre outros.. e que quando as informações são combinadas elas formam a **impressão digital**


##### Fingerprints
"Your browser fingerprint **appears to be unique** among the 222,151 tested in the past 45 days."

Isso significa o tamanho da multidão que você pode ter o navegador detectado e ser descoberto, quanto maior, melhor.


##### Bits Vazados
A teoria da informação nos diz que no meio em uma multidão de pessoas, é preciso **apenas de 33 bits** para identificar uma pessoa, quanto menor, melhor.


##### Metadados
Informações ocultas embutidas dentro de fotos, vídeos, áudios e documentos, porem registrar dados como:
- Data
- Horário de Criação
- Localização
- Dispositivo usado
- Configuração do arquivo

No **Tails** é possível remover os metadados apenas clicando com o botão direito na img e selecionar *remover metadados*.

Não é tão confiável mas também existem sites como o [Adarsus](https://www.adarsus.com/en/remove-metadata-online-document-image-video/) que faz a remoção apenas com o upload da foto


##### OnionShare
É possível compartilhar arquivos de uma máquina para a outra, sem um servidor intermediário. Tudo isso usando a arquitetura PeerToPeer (P2P). É criado um servidor local com formato .onion e assim você compartilha com outra máquina, tudo através de um link temporário.

Ao fazer o download, o servidor é fechado automaticamente, não é mais possível abrir o link.


##### Remover Arquivos com Segurança
Remover arquivos com segurança no Tails, sobrepondo com outros dados por cima para nunca serem descobertos. 

Basta selecionar o arquivo e com o botão direito clicar em Wipe, selecionar 2 ou 38.
Também é possível dar Wipe no disco inteiro.
É uma técnica muito boa para HDs porém *não* funciona com discos de Memoria Flash

Caso seja um SSD ou algo feito de memória flash as unicas formas de se livrar com os arquivos são
- Queimando o dispositivo
- Batendo com um martelo até virar poeira
- Formatar dispositivo e criptografar

1. Ao ir no menu do Tails > Utilitaries > Disks
2. Selecionar o dispositivo
3. Clicar na engrenagem
4. Format Partition
5. **Marcar Erase**
6. Marcar Internal Disk for Use with Linux systems only (**Ext4**)
7. Marcar Password protect volume (**LUKS**)
8. Next -> Format





##### Proxychains
[[Proxychains]]

##### Rede TOR
[[TOR]]





Vale ressaltar que os mesmos métodos se aplicam também para estudos na [[1.5 Dark Web]]







