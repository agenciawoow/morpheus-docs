# Configurações → Geral — Guia do Cliente

No painel, a tela aparece como **Configurações gerais**, acessada pelo card **Geral** em **Configurações** (categoria **Site**).

Este guia explica, de forma simples, **cada card e cada campo** da tela **Configurações → Geral** — a tela que define a identidade do seu servidor e do site, a conexão com o jogo, o envio de e-mails e as opções de segurança. É a primeira tela que você deve preencher depois de instalar.

---

## O que é a tela Geral?

É o "cartão de identidade" da sua instalação. Nela você informa quem é o seu servidor (equipe, season, rates), como o site mostra os servidores e os jogadores online, por onde os e-mails saem, onde o site busca o baú dos jogadores, e as opções que valem para o site inteiro (idioma, fuso horário, moeda, manutenção, HTTPS e 2FA).

Preencher corretamente garante que:

- as telas do site mostrem os dados certos (nome, rates, nível máximo, servidores);
- cadastro, recuperação de senha e notificações cheguem por e-mail;
- doações e relatórios usem a moeda e o fuso horário corretos;
- o painel fique protegido com HTTPS e, se quiser, com autenticação em dois fatores.

---

## Como configurar (card por card)

A tela é um formulário único, dividido em cards. Preencha e clique em **Salvar** no final. A confirmação é "Configurações salvas com sucesso!".

### Card Servidor

Dados do seu MuOnline. **Equipe** e **Season** são obrigatórios.

| Campo | O que informar |
|------|------|
| **Equipe** | A equipe/desenvolvedor dos arquivos do seu servidor (Louis, IGCN...). Define como o site lê contas, personagens e itens. |
| **Season** | A season que o seu MuServer usa. A lista muda conforme a **Equipe**. |
| **Nome da versão** | Texto livre mostrado aos jogadores (ex.: "97d" ou "Season 20"). |
| **Nome do servidor** | O nome do seu servidor, usado nos títulos e textos do site. |
| **Experiência** | A rate de experiência (ex.: "500x"). Só informativo, aparece no site. |
| **Drop** | A rate de drop (ex.: "60%"). Só informativo. |
| **Level máximo** | Nível máximo dos personagens (ex.: 400). Usado em serviços e rankings. |
| **Status máximo** | Pontos máximos por atributo (ex.: 65000). Usado na distribuição de pontos pelo site. |

> **Equipe** e **Season** já vêm preenchidos pela instalação. Só altere se você trocou os arquivos do servidor — e, nesse caso, revise também as demais configurações do jogo.

### Card Servidores

Lista dos servidores (ou sub-servidores) que o site exibe, com status online/offline e contagem de jogadores. Clique em **Adicionar** para cada linha e preencha:

| Campo | O que informar |
|------|------|
| **Servidor** | Identificador curto do servidor (ex.: `server1`). É o "código" interno; não aparece para o jogador. |
| **Nome** | Nome exibido aos jogadores (ex.: "Arena", "PvP 1000x"). |
| **IP** | Endereço do servidor de jogo, usado para verificar se está online (o site tenta se conectar a esse IP e porta). |
| **Porta** | Porta do servidor de jogo. |
| **Máx. usuários** | Capacidade máxima de jogadores, usada para a barra de lotação. |

As linhas podem ser **reordenadas arrastando**. Uma linha só é salva quando **Servidor**, **Nome** e **Máx. usuários** estão preenchidos.

### Card Site

| Campo | O que informar |
|------|------|
| **Título** | O título do site (aba do navegador, cabeçalho, e-mails). |
| **Logo** | Envie a imagem do logo. Recomendado PNG com fundo transparente. Se não enviar nada, o logo atual é mantido. |
| **Jogadores online** | Como o site mostra os jogadores online: **Não mostrar nada**, **Somente total** ou **Mostrar tudo** (total e por servidor). |
| **Duração do cache (segundos)** | Por quantos segundos a contagem de jogadores online fica guardada antes de ser recalculada. Valores maiores aliviam o banco em servidores cheios (60 é um bom padrão). |

### Card SMTP

Dados da conta de e-mail que o site usa para **enviar** mensagens (confirmação de cadastro, recuperação de senha, notificações). Sem isso, nenhum e-mail sai.

| Campo | O que informar |
|------|------|
| **Servidor** | Endereço do servidor de envio (ex.: `smtp.seuprovedor.com`). |
| **Porta** | Porta do envio (ex.: 587 ou 465). |
| **Segurança** | **TLS** (normalmente com a porta 587) ou **SSL** (normalmente com a 465). |
| **Usuário** | Usuário da conta de e-mail (geralmente o endereço completo). |
| **Senha** | Senha da conta de e-mail. |
| **De** | O endereço que aparece como remetente (ex.: `no-reply@seuservidor.com`). |

> Os textos de cada e-mail são editados em **Configurações → E-mails**. O envio em si acontece pela fila (veja o guia **Tarefas agendadas e Fila**).

### Card Castle Siege

Aparece apenas quando a equipe/season do seu servidor tem Castle Siege.

| Campo | O que informar |
|------|------|
| **Próximo confronto** | Texto livre com a data ou descrição do próximo evento, exibido na página do Castle Siege. |

### Card Connect Server & Join Server

Endereços que o site usa para se comunicar com o Connect Server e o Join Server do seu jogo (por exemplo, para obter a lista de servidores).

| Campo | O que informar |
|------|------|
| **Connect Server** | IP do Connect Server (ex.: `192.168.1.100`). |
| **Porta** (ao lado) | Porta do Connect Server (ex.: 44405). |
| **Join Server** | IP do Join Server. |
| **Porta** (ao lado) | Porta do Join Server (ex.: 55970). |

### Card Baú

Controla de onde o site lê o **baú (warehouse)** das contas — usado pelo mercado de itens, leilão, loja e demais recursos que entregam ou retiram itens.

- **Baú externo** — deixe **desligado** na maioria dos servidores: o site usa o baú padrão do jogo.
- Ligue apenas se os arquivos do seu servidor guardam o baú em outro lugar (baú estendido/externo). Ao ligar, aparecem os campos para escolher o banco, a tabela e as colunas: **Coluna da conta**, **Coluna de itens**, **Coluna de número** e **Coluna de dinheiro**.

> Recurso avançado: preencha somente com ajuda de quem conhece o banco do seu jogo. Uma escolha errada faz o site não encontrar os itens dos jogadores.

### Card Morpheus

Opções que valem para o site e o painel inteiros.

| Campo | O que faz |
|------|------|
| **Idioma** | Idioma padrão do site e do painel. O jogador ainda pode trocar o idioma no site. |
| **Fuso horário** | Fuso usado em datas de pedidos, eventos, rankings e tarefas agendadas. A lista mostra a diferença em horas para facilitar. |
| **Moeda padrão** | Moeda principal das doações, dos preços e dos relatórios financeiros (ex.: `BRL — Brazilian Real`). |
| **Manutenção** | Quando ligado, os jogadores veem uma página de manutenção em vez do site. Quem está logado no painel continua acessando o site normalmente para testar. |
| **Depuração** | Quando ligado, o site mostra mensagens de erro detalhadas. Use só para diagnosticar um problema e **desligue em seguida** — as mensagens expõem detalhes internos. |
| **Forçar HTTPS** | Redireciona automaticamente todo acesso por `http://` para `https://`. Ligue depois que o certificado estiver instalado e funcionando. |
| **Forçar 2FA** | Obriga todos os usuários do **painel** a usar autenticação em dois fatores. No próximo acesso, cada usuário vê a tela **2FA verification**: escaneia o QR code com o aplicativo autenticador (Google Authenticator, Authy etc.) e informa o **Code**. A partir daí, todo login no painel pede o código do aplicativo. |

Clique em **Salvar**.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|------|------|
| Trocar a equipe ou a season dos arquivos | **Configurações → Geral** → card **Servidor** |
| Mudar nome, rates, level e status máximos | **Configurações → Geral** → card **Servidor** |
| Cadastrar os servidores mostrados no site | **Configurações → Geral** → card **Servidores** |
| Trocar o título ou o logo do site | **Configurações → Geral** → card **Site** |
| Esconder ou mostrar jogadores online | **Configurações → Geral** → card **Site** → **Jogadores online** |
| Configurar o envio de e-mails | **Configurações → Geral** → card **SMTP** |
| Editar o texto dos e-mails | **Configurações → E-mails** |
| Informar a data do Castle Siege | **Configurações → Geral** → card **Castle Siege** |
| Informar Connect Server e Join Server | **Configurações → Geral** → card **Connect Server & Join Server** |
| Usar um baú externo/estendido | **Configurações → Geral** → card **Baú** → **Baú externo** |
| Trocar idioma, fuso horário ou moeda | **Configurações → Geral** → card **Morpheus** |
| Colocar o site em manutenção | **Configurações → Geral** → card **Morpheus** → **Manutenção** |
| Forçar HTTPS no site | **Configurações → Geral** → card **Morpheus** → **Forçar HTTPS** |
| Exigir 2FA no painel | **Configurações → Geral** → card **Morpheus** → **Forçar 2FA** |
| Trocar o tema do site | **Configurações → Templates** |
| Regras de cadastro e login dos jogadores | **Configurações → Cadastro** e **Configurações → Login** |
| Moedas do jogo, VIP e meios de pagamento | **Configurações → Moedas**, **Configurações → Sistema VIP**, **Configurações → Gateways** |

---

## Dicas e boas práticas

- **Preencha o card SMTP e teste** criando uma conta de teste no site: se o e-mail de confirmação chegar, está tudo certo.
- **Use "Somente total" em Jogadores online** se não quiser revelar a lotação de cada servidor à concorrência.
- **Aumente a Duração do cache** em servidores com muitos jogadores; a contagem não precisa ser em tempo real.
- **Ligue Forçar HTTPS só com o certificado funcionando**, senão o site fica inacessível. Se isso acontecer, desligue a opção pelo painel acessando-o por `https://`.
- **Ative Forçar 2FA** assim que a equipe tiver o aplicativo autenticador instalado — é a proteção mais eficaz para o painel.
- **Depuração sempre desligada em produção.**
- **Use Manutenção para atualizações grandes do servidor de jogo**: os jogadores veem o aviso e a equipe (logada no painel) continua testando o site.

---

## Perguntas frequentes

**Mudei a Equipe/Season e o site parou de ler personagens ou itens.**
A equipe e a season precisam ser exatamente as dos arquivos do seu servidor. Volte ao valor anterior e confirme com quem montou o servidor qual é a combinação correta.

**Os e-mails não chegam.**
Confira **Servidor**, **Porta** e **Segurança** no card **SMTP** (TLS com 587, SSL com 465 são as combinações mais comuns) e se a senha é a da conta de e-mail. Depois veja **Configurações → Fila de Jobs**: trabalhos com status **Falhou** mostram a mensagem de erro do envio. Lembre-se de que a fila só é processada com as tarefas agendadas ativas.

**Liguei Forçar HTTPS e o site ficou inacessível.**
O certificado não está ativo ou o servidor web não está configurado para HTTPS. Entre no painel por `https://` (se possível) e desligue a opção, ou peça para a hospedagem instalar o certificado antes de ligar de novo.

**Liguei Forçar 2FA e um usuário perdeu o celular.**
Um Super usuário pode desligar **Forçar 2FA** temporariamente para o usuário entrar e configurar o aplicativo de novo, ligando a opção em seguida. Se ninguém mais conseguir entrar no painel, fale com o suporte.

**O jogador ainda vê o site em outro idioma.**
**Idioma** define o padrão; o jogador pode escolher outro idioma pelo seletor de idiomas do site.

**O site mostra servidores "offline" mesmo com o jogo no ar.**
Confira **IP** e **Porta** de cada linha do card **Servidores** e se o servidor web consegue alcançar esses endereços (firewall). A verificação fica em cache por cerca de um minuto, então aguarde um pouco depois de corrigir.

**Preciso ligar o Baú externo?**
Só se os arquivos do seu servidor usam um baú estendido separado do padrão. Na dúvida, deixe desligado e confira com quem conhece o banco do seu jogo.

**Em Manutenção, a equipe consegue entrar no site?**
Sim. Quem estiver logado no painel administrativo acessa o site normalmente; os demais veem a página de manutenção.

---

> Alguma configuração do jogo que você não encontrou aqui? Veja os outros cards em **Configurações** (Cadastro, Login, Serviços, Rankings, Economia) e os guias de cada plugin.
