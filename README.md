# SpaceCrypto Bot

------------

Este é uma automação (bot) para jogar o jogo SpaceCrypto, esse bot automaticamente loga no jogo, coloca os heróis para trabalhar, atualiza o jogo para não cair por tempo de resposta, checa novos mapas, etc. Bot baseado no bot de bombcrypto criado por mpcabete

Se você achou que esse bot foi uma ajuda para você, por favor faça uma doação com as opções abaixo, assim podemos continuar a melhorar o grande trabalho que gastei e por tantas horas gastas 🤯.


**Donations options:**

- **BUSD/BCOIN/BNB (BEP20):** 0x953955ffE6BD6D0a8Fe2c91068501F20c19D39ae

## Principais etapas

De uma forma resumida vai precisar fazer:

1. Baixar `Python`
2. Instalar pacotes do python atráves do `requirements.txt`
3. Ajustar a `escala do monitor` para `100%` se necessário
4. Baixar o navegador `Brave` (melhor opção)
5. Alterar as configurações no arquivo `config.yaml` se necessário
6. Criar bot do `Telegram` se necessário

## Estrutura do projeto
    .
    └── Spacecrypto-bot
        ├── main.py                    # inicia nosso app
        ├── bot.py                     # todos os movimentos e mecânicas para o bot
        ├── controllers.py             # todos os controles para ajudar o bot a rodar
        ├── config.yaml                # todas as configurações para ajudar o bot a rodar
        └── logs                       # todos os arquivos log são salvos aqui
        └── static
            ├── img
                ├── game               # todas as imagens relacionadas ao jogo estarão aqui
                ├── readme             # todas as imagens relacionadas ao repositório
                ├── screenshot         # todas as imagens tiradas da tela (pasta será criada automaticamente)


#### Algumas configurações podem ser alteradas no arquivo config.yaml. Caso mude, não se esqueça de reiniciar o bot para que as novas configurações sejam ativadas.


## Requisitos

Browser: `Brave: Versão 1.34.81 Chromium: 97.0.4692.99`

#### ⚠️ Eu realmente aconselho você a usar o navegador Brave em vez de outros, por vários motivos, especialmente se você quiser usar várias contas.


------------
Versão do Windows:
- `Windows 10`

- `Windows 11`

Versão do Python:
```python
Python 3.9.9
```

Os requisitos também podem ser encontrados no arquivo `requirements.txt`.
Este projeto utiliza os seguintes requisitos:

    APScheduler==3.6.3
    asyncio==3.4.3    
    numpy==1.21.4
    opencv-python==4.5.4.60
    pandas==1.1.5
    pathlib==1.0.1
    Pillow==8.4.0
    PyAutoGUI==0.9.53
    python-telegram-bot==13.9
    pywin32==303
    pywinauto==0.6.8
    PyYAML==6.0
    requests==2.26.0
    tzlocal==4.1

Escala do monitor: `100%`

## Observações

- Todas as images foram tiradas do jogo de uma tela Full HD e a escala selecionada em 100%. Caso seu bot não esteja funcionando, certifique-se que a escala do seu monitor também esteja em 100%. Após isso, salve todas as imagens novamente e salve elas com o formato `.png`.

## Funcionalidades

- Agende a atualização do jogo em um período de tempo
- Agende o envio de naves para batalhar em um período de tempo
- Exclua arquivos e pastas antigos se desejar automaticamente
- Conecta na carteira
- Conecte-se, faça login e desbloqueie o Metamask
- Verifique se há novo mapa disponível
- Faça captura de tela de erros e novos mapas
- Envia mensages para o bot do seu Telegram
- Funciona com a quantidade de contas que você precisar

## YAML file configurations and options explained

**1. bot_options**
- **create_logfiles**: Você pode habilitar a criação de arquivos de log disponíveis na pasta `logs`
- **delete_old_logfiles**: Você pode habilitar a exclusão de arquivos de log antigos e manter o arquivo de data de hoje.
- **delete_old_folders**: Você pode habilitar a exclusão de pastas mais antigas e manter as pastas de datas de hoje.
- **enable_multiaccount**: Você pode habilitar o recurso multiconta.
- **multiaccount_names**: Você pode definir os nomes de contas/perfis do navegador Brave em cada linha.
- **refresh_browser_time**: Você pode definir o horário em que o navegador será atualizado pelas teclas: CTRL + SHIFT + R.
**1.1 metamask_options**
	- **enable_login_metamask**: Você pode habilitar o login no Metamask quando estiver bloqueado e precisa de senha para desbloquear.
	- **metamask_password**: Se a opção `enable_login_metamask` estiver definida como `True`, você pode passar a senha para desbloquear o Metamask.

**2. telegram_options**
- **telegram_integration**: Você também pode habilitar a integração de mensagens de log para mensagens do Telegram.
- **telegram_token**: Se `telegram_integration` estiver definido como `True`, você pode passar o token do seu bot do Telegram.
- **telegram_chatid**: Se `telegram_integration` estiver definido como `True`, você pode passar o número chat_id do seu bot do Telegram. Uma vez que o número é escrito, ele não muda mais.

**3. heroes_options**
- **work_heroes_options**: Você pode definir o modo de trabalho para seus heróis. A opção `all` envia todos os heróis para o trabalho.
- **work_heroes_time**: Você pode definir a hora em que o bot os enviará para trabalhar automaticamente.
- **refresh_heroes_time**: Você pode definir a hora em que o bot apenas atualizará o jogo voltando ao menu principal e indo para o jogo Caça ao Tesouro.
- **refresh_heroes_only**: Você pode habilitar apenas a atualização do jogo voltando ao menu principal e indo para o jogo Caça ao Tesouro, com esta opção o bot *não* enviará heróis para trabalhar ou fazer outras funcionalidades.
- **chest_screenshot_time**: Você pode definir a hora em que o bot fará uma captura de tela de suas moedas do jogo.
- **clicks_count**: Você pode definir quantos navios você tem, para que o bot não continue clicando mais do que o necessário.
- **drag_count**: Você pode definir quantas vezes deseja que o bot arraste a lista procurando por navios que tenham munição.


