
## Instalação

Antes de tudo lembre-se de atualizar o sistema

```
sudo apt update && sudo apt ugrade -y
```


Vamos a instalação do Proxychains

1. No terminal, instale o Proxychains:

```
sudo apt install proxychains4
```

2. Baixe o serviço do tor

```
sudo apt install tor
```

3. Verificar se o Tor está rodando

```
sudo service tor status
```

4. Iniciar o Tor

```
sudo service tor start
```

5. Ir para o arquivo de configurações do Proxychains

```
nano /etc/proxychains4.conf
```

6. Desmarcar o dynamic_chain - Para o Socks5 pegar o próximo Proxy da lista
![[Pasted image 20240314202347.png]]

7. Desmarcar Proxy DNS Requests