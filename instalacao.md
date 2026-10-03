# Instalação e primeiros passos — Guia do Cliente

Este guia explica, de forma simples, **o que você precisa ter pronto** antes de instalar o Morpheus MuWeb, **como funciona o assistente de instalação** (tela por tela) e **o que fazer logo depois** para o site e o painel ficarem prontos para os jogadores. Não é necessário conhecimento de programação — só acesso ao servidor onde o site vai ficar e ao banco de dados do seu MuOnline.

---

## O que é a instalação?

O Morpheus MuWeb é o site e o painel administrativo do seu servidor de MuOnline. A instalação é feita por um **assistente visual no navegador**, que:

- confere se o servidor web atende aos requisitos;
- conecta o site ao banco de dados do jogo;
- cria as tabelas e os dados iniciais do site;
- define a equipe/season do seu servidor, fuso horário, moeda e o primeiro usuário do painel.

Ao final, você já consegue entrar no painel e começar a configurar o site.

---

## Antes de começar: requisitos

O assistente mostra uma lista de verificações na etapa **Requisitos**. Cada item aparece com um sinal verde (ok) ou vermelho (falta). Garanta que o seu servidor web tenha:

| Verificação (como aparece na tela) | O que significa |
|------|------|
| **PHP Version 8.3+** | PHP na versão 8.3 ou mais recente. |
| **PDO Driver (sqlsrv)** | O conector do PHP para SQL Server. Sem ele o site não conversa com o banco do jogo. |
| **ionCube Loader** | Componente obrigatório para rodar o Morpheus. |
| **JSON PHP Extension** | Extensão do PHP. |
| **OpenSSL PHP Extension** | Extensão do PHP (segurança e licença). |
| **GD PHP Extension** | Extensão do PHP (imagens de itens, avatares, logo). |
| **ZIP PHP Extension** | Extensão do PHP (instalar plugins e temas por arquivo ZIP, atualizações). |
| **cURL PHP Extension** | Extensão do PHP (pagamentos, licença, atualizações). |
| **Intl PHP Extension** | Extensão do PHP (formatação de datas e moedas). |
| **SimpleXML PHP Extension** | Extensão do PHP. |
| **Mbstring PHP Extension** | Extensão do PHP (textos em vários idiomas). |
| **exif PHP Extension** | Extensão do PHP (imagens enviadas). |

Além disso, você precisa de:

- **SQL Server** com o banco do jogo (normalmente `MuOnline`) e um usuário com permissão de leitura e escrita nele. Se quiser guardar as tabelas do site em um banco separado, leia o guia **Banco de dados do site** (`banco-de-dados.md`).
- **Acesso à internet a partir do servidor web**, porque o site valida a licença e busca atualizações automaticamente.
- O **domínio** do site já apontando para o servidor. A licença é vinculada ao domínio informado na compra.

> No topo da etapa **Requisitos** a tela mostra **Your IPs Address** com o(s) IP(s) do seu servidor. Guarde essa informação: é o IP que a sua licença precisa conhecer (veja o guia **Atualização, licença e Morpheus Market**).

---

## Como instalar (passo a passo)

### Passo 0 — Enviar os arquivos

Envie os arquivos do Morpheus para a pasta do site no servidor web (a raiz do domínio, por exemplo `www.seuservidor.com`). Em seguida, abra o endereço do site no navegador: enquanto o sistema não estiver instalado, ele abre o **assistente de instalação** automaticamente (também acessível em `www.seuservidor.com/install/`).

O assistente é dividido em etapas, listadas na lateral esquerda. Use os botões **Próximo** e **Voltar** para navegar.

### Etapa 1 — Bem-vindo

Escolha o tipo de instalação:

- **Instalação Nova** — para um site novo. Cria todas as tabelas e dados iniciais.
- **Upgrade** — para quem já tem o Morpheus MuWeb instalado em uma versão anterior e está trocando para esta versão. Mantém os dados existentes (pedidos, carteiras, configurações) e só cria o que é novo. Veja a seção **Atualizar uma instalação existente**, mais abaixo.

### Etapa 2 — Termos de uso

Leia os termos e marque **Aceito os termos de uso**. Não é possível avançar sem aceitar.

### Etapa 3 — Requisitos

Confira a lista de verificações (tabela acima). Se algum item estiver vermelho, peça para a sua hospedagem ou para quem administra o servidor web instalar o componente que falta e **recarregue a página** antes de continuar.

### Etapa 4 — Database

Aqui você conecta o site ao SQL Server do jogo:

| Campo | O que informar |
|------|------|
| **Servidor** | Endereço do SQL Server (ex.: `localhost` ou o IP da máquina do banco). |
| **Porta** | Porta do SQL Server (padrão `1433`). |
| **Usuário** | Usuário do SQL Server (ex.: `sa`). |
| **Senha** | Senha desse usuário. |
| **Banco de dados** | Banco do jogo (ex.: `MuOnline`). |
| **Banco de dados para contas** | Banco onde ficam as contas dos jogadores. Na maioria dos servidores é o mesmo banco do jogo; alguns usam um banco separado (ex.: `Me_MuOnline`). |
| **Banco de dados do site (opcional)** | Deixe em branco para criar as tabelas do site dentro do banco do jogo. Informe um nome (ex.: `MorpheusWeb`) para usar um banco separado. Detalhes no guia **Banco de dados do site**. Fica desabilitado no modo **Upgrade**. |
| **MD5** | Marque se o seu servidor guarda as senhas das contas criptografadas em MD5. Em dúvida, pergunte a quem montou os arquivos do seu servidor — o site precisa usar o mesmo formato para o login funcionar. |

Logo abaixo há a seção **Columns**, com os nomes das colunas do personagem que o seu servidor usa para alguns recursos:

- **Character Avatar** — coluna da imagem de avatar (se não existir, o instalador cria).
- **Character Resets** — coluna de resets (ex.: `ResetCount`).
- **Character Master Resets** — coluna de master resets (ex.: `MasterResetCount`).
- **Character PK** — coluna de contagem de PK usada pelo site (ex.: `PkCountWeb`).
- **Character Hero** — coluna de contagem de Hero usada pelo site (ex.: `HeroCountWeb`).

Os valores padrão atendem a maioria dos servidores. Só altere se os arquivos do seu servidor usam nomes diferentes.

### Etapa 5 — Configurações

- **Team** — a equipe/desenvolvedor dos arquivos do seu servidor (ex.: Louis, IGCN...).
- **Season** — a season que o seu servidor usa. A lista muda conforme a equipe escolhida.

Seção **Geral**:

- **Base Path** — deixe em branco quando o site fica na raiz do domínio (o caso mais comum).
- **Timezone** — fuso horário do servidor (ex.: `America/Sao_Paulo`). Afeta datas de pedidos, rankings, eventos e as tarefas agendadas.
- **Moeda** — moeda principal das doações e relatórios (ex.: `BRL — Brazilian Real`).

Seção **Acesso Admin** (só aparece na **Instalação Nova**):

- **Usuário** e **Senha** do primeiro usuário do painel administrativo. Esse usuário é o **Super usuário** da instalação. **Troque a senha sugerida por uma senha forte** — ela dá acesso total ao painel.

### Etapa 6 — Resumo

A tela mostra tudo o que você preencheu, com um aviso do tipo de instalação (**Nova instalação** ou **Atualizar web**). Revise com calma; se precisar corrigir algo, clique na etapa correspondente na lateral.

Clique em **Instalar**. Enquanto roda, o botão mostra **Instalando...**. Ao terminar, aparece a mensagem de sucesso (**Success! Morpheus MuWeb has been installed. Thank you, and enjoy!**).

Se der erro, a tela mostra **Falha na instalação** com a descrição do problema e o botão **Tentar novamente**. Veja as **Perguntas frequentes** no fim deste guia.

### O que o instalador faz por você

- Cria as tabelas e os dados iniciais do site (configurações, modelos de mensagens de WhatsApp e estrutura do financeiro).
- Registra as tarefas agendadas do módulo financeiro (sincronização de moedas e pedidos e busca de cotações).
- Grava a equipe e a season escolhidas.
- Cria a coluna de avatar no personagem, se ela ainda não existir.
- Cria o usuário administrador (instalação nova).

---

## Logo depois de instalar

### 1. Remover a pasta de instalação

Depois da mensagem de sucesso, **apague a pasta `install` do servidor**. O assistente se recusa a rodar de novo em um site já instalado, mas remover a pasta é a prática recomendada.

### 2. Entrar no painel

O painel fica em `www.seuservidor.com/admin`. Entre com o usuário e a senha definidos na etapa **Configurações**. O primeiro que você vê é o **Painel** (visão geral do servidor, alertas e avisos da equipe Morpheus).

### 3. Preencher Configurações → Geral

Abra **Configurações → Geral** e preencha os dados do servidor (nome, rates, servidores/sub-servidores, Connect Server), a identidade do site (título e logo), o e-mail de envio (SMTP) e as opções gerais (idioma, fuso horário, moeda). Esse é o passo mais importante — está detalhado no guia **Configurações → Geral** (`configuracoes-gerais.md`).

### 4. Agendar as tarefas automáticas

O site depende de uma rotina que roda **a cada minuto** no servidor para enviar e-mails e notificações, liberar banimentos vencidos, atualizar o financeiro, premiar rankings e muito mais. Sem ela, várias funções ficam paradas. Veja o guia **Tarefas agendadas e Fila** (`tarefas-agendadas.md`), que mostra como agendar e quais tarefas criar em **Configurações → Tarefas**.

### 5. Ativar os plugins

No menu lateral, abra **Plugins** e clique em **Ativar** nos plugins que a sua licença inclui (loja, leilão, rankings premiados, suporte etc.). Cada plugin ativo ganha o botão **Configurar** e as próprias telas no painel. Plugins que não fazem parte da sua licença não podem ser ativados.

### 6. Escolher o tema

Em **Configurações → Templates** você vê os temas instalados e pode clicar em **Ativar** no que quiser usar. Novos temas podem ser baixados em **Mercado da Morpheus → Templates** ou instalados por arquivo ZIP (veja o guia **Atualização, licença e Morpheus Market**).

### 7. Revisar e-mails e pagamentos

- **Configurações → E-mails** — modelos das mensagens que o site envia (confirmação de cadastro, recuperação de senha etc.).
- **Configurações → Gateways** e **Configurações → Contas bancárias** — meios de pagamento das doações.
- **Configurações → Usuários** e **Configurações → Grupos** — crie outros usuários do painel com permissões limitadas, em vez de compartilhar o Super usuário.

---

## Atualizar uma instalação existente (Upgrade)

O modo **Upgrade** do assistente é para quem **já usa o Morpheus MuWeb em uma versão anterior** e quer passar para esta versão **mantendo os dados** (contas, pedidos, carteiras, notícias, configurações).

Como funciona:

1. Faça **backup completo** do banco de dados e dos arquivos do site.
2. Envie os arquivos da nova versão para o servidor, seguindo as orientações do suporte sobre quais pastas da instalação antiga preservar (por exemplo, a pasta de uploads e as configurações de conexão).
3. Abra o assistente, escolha **Upgrade** na etapa **Bem-vindo** e siga as etapas normalmente.
4. Na etapa **Database**, informe o mesmo banco da instalação antiga. O campo **Banco de dados do site (opcional)** fica desabilitado, porque as tabelas do site já existem no banco do jogo.
5. Na etapa **Configurações** não há seção **Acesso Admin**: os usuários do painel são mantidos.
6. No **Resumo** aparece o aviso **Atualizar web** — o sistema reconhece as tabelas que já existem e cria apenas o que é novo.

> Para as atualizações de rotina (de uma versão 7 para outra), você **não** usa o assistente: a atualização é feita pelo próprio painel, em **Configurações → Atualizar**. Veja o guia **Atualização, licença e Morpheus Market**.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde |
|------|------|
| Instalar o site pela primeira vez | Abra o endereço do site no navegador (assistente de instalação) |
| Escolher onde ficam as tabelas do site | Assistente → etapa **Database** → **Banco de dados do site (opcional)** |
| Definir equipe e season do servidor | Assistente → etapa **Configurações** (depois, **Configurações → Geral**) |
| Trocar fuso horário, moeda ou idioma depois de instalado | **Configurações → Geral** |
| Criar o primeiro administrador | Assistente → etapa **Configurações** → **Acesso Admin** |
| Criar mais usuários do painel | **Configurações → Usuários** |
| Agendar as tarefas automáticas | Servidor (rotina a cada minuto) + **Configurações → Tarefas** |
| Ativar plugins | Menu lateral → **Plugins** |
| Escolher o tema do site | **Configurações → Templates** |
| Atualizar para uma versão nova | **Configurações → Atualizar** |
| Migrar de uma versão antiga do Morpheus | Assistente → **Upgrade** |

---

## Dicas e boas práticas

- **Confira os requisitos antes de enviar os arquivos.** A maior parte das instalações que falham é por falta do conector do SQL Server ou do ionCube Loader.
- **Use um usuário de banco com senha forte** e, se possível, exclusivo para o site.
- **Troque a senha sugerida do administrador** no mesmo dia e ative **Forçar 2FA** em **Configurações → Geral** quando a equipe estiver com o aplicativo autenticador configurado.
- **Agende a rotina automática logo após instalar.** Sem ela, e-mails de cadastro e recuperação de senha não saem.
- **Faça backup antes de qualquer Upgrade ou atualização.**
- **Deixe o site acessível pela internet** (domínio e IP corretos) — a licença é validada automaticamente.

---

## Perguntas frequentes

**A página fica em branco ou dá erro ao abrir o site.**
Quase sempre é requisito faltando (ionCube Loader, conector do SQL Server ou alguma extensão do PHP). Abra o assistente e confira a etapa **Requisitos**. Se o site já estiver instalado, ative **Depuração** em **Configurações → Geral** para ver a mensagem de erro, e desative depois.

**O instalador diz que o banco não conecta.**
Confira **Servidor**, **Porta**, **Usuário** e **Senha**. O SQL Server precisa aceitar conexões por TCP/IP na porta informada e o usuário precisa existir com autenticação do próprio SQL Server (não só do Windows). Se o banco está em outra máquina, verifique o firewall.

**Apareceu "O sistema já está instalado. Utilize o tipo upgrade para atualizar."**
Esse banco/servidor já tem uma instalação. Se você quer uma instalação limpa, remova as configurações antigas e as tabelas do site com ajuda do suporte; se quer manter os dados, volte à etapa **Bem-vindo** e escolha **Upgrade**.

**Apareceu "Installation already completed. Remove the install/ folder."**
O site já está instalado e o assistente foi bloqueado por segurança. Apague a pasta `install` e entre no painel normalmente.

**O site abre, mas é redirecionado para uma página falando de licença ilegal.**
A licença não bateu com o domínio ou com o IP do servidor. Confira se você instalou no domínio informado na compra e se o IP mostrado em **Your IPs Address** (etapa **Requisitos**) é o IP cadastrado na licença. Mais detalhes no guia **Atualização, licença e Morpheus Market**.

**Em qual idioma o site fica depois da instalação?**
O site é instalado em português do Brasil. Para trocar, use **Idioma** em **Configurações → Geral**.

**Esqueci a senha do administrador.**
Outro usuário com permissão em **Configurações → Usuários** pode redefinir a senha. Se for o único usuário, entre em contato com o suporte.

**O que fazer com a opção MD5?**
Ela precisa refletir como as senhas das contas estão guardadas no seu servidor. Se os jogadores não conseguem entrar no site com a senha do jogo (ou vice-versa), a opção provavelmente está invertida — fale com quem montou os arquivos do servidor.

---

> Precisa de ajuda para instalar? Entre em contato com o suporte com os dados da hospedagem e uma captura da etapa **Requisitos**.
