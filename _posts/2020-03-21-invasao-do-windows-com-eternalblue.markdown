---
layout: post
title:  "Invasão do Windows com Eternalblue (Metasploit)"
date:   2020-03-21 22:56:00
categories: Tutorial
---

**O que é EternalBlue?**

O EternalBlue é um exploit desenvolvido pela NSA a partir de um zero day encontrado nos servidores Windows 2008 r2 e no Windows 7.
Este exploit foi roubado da NSA pelo um grupo de hackers chamado Shadow Brokers em 2017.

O EternalBlue, também é conhecido como MS17-010, é uma vulnerabilidade no protocolo SMB (Server Message Block) da Microsoft.
O SMB permite que os sistemas compartilhem o acesso a arquivos, impressoras e outros recursos na rede.
A vulnerabilidade ocorre porque as versões anteriores do SBM contêm falhas de segurança.

**OBS**: Para prosseguir com o tutorial você deve ter conhecimentos básicos do [Metasploit Framework](https://metasploit.help.rapid7.com/docs/msf-overview)

**Como usar o EternalBlue?**

**Passo 1** – *Encontrar o exploit*

Primeiro precisas de abrir o terminal e iniciar o Metasploit.

A seguir usar o comando **search** para encontra o exploit *MS17*

Existe um scanner auxiliar que podemos executar para determinar se o nosso alvo é vulnerável ao MS17.
É sempre boa ideia realizar o reconhecimento caso contrário podemos acabar perdendo muito tempo se o alvo não for vulnerável.
Depois de determinarmos que o alvo é vulnerável ao EternalBlue podemos usar o exploit da seguinte maneira.




**Passo 2** – *Executar o exploit*

Podemos olhar as configurações usando o comando **options**

Primeiro, precisamos de especificar o ip do alvo.

Próximo passo é adicionar um payload que nos dará o controlo da máquina 

Por fim adicionar o ip da nossa máquina local

E adicionar a porta em que vai rodar

Agora é so usar o comando **run** para executar




**Passo 3** – *verificar se hackeamos o nosso alvo*

Para verificar isso basta usar o comando **sysinfo** e vamos obter as informações do sistema
