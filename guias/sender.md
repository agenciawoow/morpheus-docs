# Sender (notificações por WhatsApp) — Guia do Cliente

Este guia explica, de forma simples, **o que é** o Sender, **o que o jogador recebe** e **como você configura** tudo pelo painel administrativo. Não é necessário nenhum conhecimento técnico.

---

## O que é o Sender?

O Sender envia **mensagens automáticas de WhatsApp** para os jogadores do seu servidor, usando um número de WhatsApp seu, conectado ao site pelo QR code (do mesmo jeito que você conecta o WhatsApp Web).

Sempre que acontece algo importante na conta do jogador — cadastro concluído, doação confirmada, item vendido, leilão vencido, ticket respondido, assinatura renovada, saque pago — ele recebe uma mensagem no celular, com o logo do seu servidor e um texto que você mesmo pode personalizar.

Por que vale a pena:

- **Engajamento:** o jogador fica sabendo na hora que o lance dele foi superado, que ganhou um sorteio ou que o ticket foi respondido — e volta para o site.
- **Confiança:** confirmações de doação, compra e saque chegam direto no WhatsApp, reduzindo dúvidas e chamados no suporte.
- **Segurança:** o link de recuperação de senha e o aviso de "senha redefinida" chegam no telefone do dono da conta.

---

## Conceitos principais

### 1. Instância

A **instância** é o número de WhatsApp conectado ao site. Você cria a instância no painel, escaneia o QR code com o celular e pronto — a partir daí o site envia mensagens por aquele número.

Os nomes das instâncias recebem automaticamente o **nome do seu servidor** como prefixo (por exemplo, `meuservidor_notifications`). Isso isola as suas instâncias das de outros servidores. A instância com o sufixo `notifications` é a **padrão**: é por ela que saem todas as notificações automáticas, e ela aparece marcada com **★ padrão** na lista.

### 2. Eventos e templates

Cada acontecimento que gera mensagem é um **evento** (doação confirmada, leilão vencido etc.). Para cada evento existe um **template**: o texto da mensagem, com um **Título** e um **Corpo**, que já vem pronto em português e que você pode editar livremente.

Dentro do texto você usa **variáveis** entre chaves duplas, como `{{name}}` ou `{{amount}}`, que são trocadas pelo valor real na hora do envio. A lista de eventos é fixa — você edita e restaura templates, mas não cria eventos novos pelo painel.

### 3. Telefone do jogador

O Sender só consegue avisar jogadores que têm **telefone cadastrado** na conta. O número é lido de uma coluna da tabela de contas do jogo (por padrão, a coluna de telefone que já existe no cadastro de contas do MuOnline). Veja em "Como o jogador informa o telefone" como coletar esse dado.

### 4. Fila e auditoria

As mensagens **não saem na hora** da ação: elas entram na **fila de tarefas** do site e são enviadas pela tarefa agendada **Processar Fila**, que roda a cada minuto. Cada tentativa de envio fica registrada na **Auditoria de envios**, com status e detalhe do erro, se houver.

---

## Como o jogador usa

O jogador não precisa fazer nada além de **ter o telefone cadastrado na conta**. A partir daí:

1. Ele recebe uma mensagem de **boas-vindas** no WhatsApp assim que a conta é criada (ou assim que confirma o e-mail, se a confirmação estiver ligada).
2. Cada acontecimento relevante gera uma mensagem automática, com o **logo do servidor** como imagem e o texto do template.
3. Mensagens com link (recuperação de senha, ticket respondido, lance superado) levam o jogador direto para a página certa do site.

### Como o jogador informa o telefone

Existem duas formas de coletar o telefone:

- **Campo personalizado no cadastro** (recomendado): em **Configurações → Acessos → Cadastro**, no bloco **Custom fields**, clique em **Adicionar** e crie um campo apontando para a coluna de telefone da tabela de contas (**Column**), com um rótulo amigável (**Label**, ex.: "WhatsApp") e marque **Required** se quiser torná-lo obrigatório. O campo passa a aparecer no formulário de cadastro do site.
- **Widget de aceite do plugin**: o Sender oferece um bloco pronto (caixa "Aceito receber notificações via WhatsApp em meu número de telefone" + seleção do país + campo de telefone) que um tema personalizado pode incluir no formulário de cadastro. Se o seu tema foi feito sob medida, peça a quem o mantém para usar esse bloco.

O número é guardado **só com dígitos**, com o código do país na frente. Números brasileiros com 10 ou 11 dígitos (DDD + número) recebem o código **55** automaticamente. Números fora do padrão (menos de 12 ou mais de 15 dígitos no total) são considerados inválidos e aparecem na auditoria com o status `invalid_phone`.

---

## Como configurar (passo a passo)

Toda a configuração fica no menu lateral **Sender**, que tem quatro telas: **Auditoria de envios**, **Templates**, **Instâncias** e **Configurações**. O card **Configurações → Sender** também leva à tela de configurações.

### Passo 0 — Confira o nome do servidor

O Sender usa o **nome do servidor** (configurado nas configurações gerais do site) para nomear as instâncias. Se ele estiver vazio, a tela de instâncias mostra o aviso **O nome do servidor não está configurado** e não deixa continuar. Preencha o nome antes de seguir.

### Passo 1 — Conectar o número de WhatsApp

1. Abra **Sender → Instâncias**.
2. No bloco **Nova instância**, digite o sufixo no campo **Nome da instância**. Use `notifications` para criar a instância **padrão** (é por ela que as notificações automáticas saem). Só letras minúsculas, números, underscore ou hífen.
3. Clique em **Criar e escanear QR**. Abre a janela **Escanear no WhatsApp** com o QR code e os passos:
   - Abra o WhatsApp no celular;
   - Toque em Aparelhos conectados e depois em Conectar um aparelho;
   - Aponte a câmera para o QR acima.
4. Quando o celular ler o código, a janela confirma **Instância conectada com sucesso!** e a instância aparece na lista **Instâncias deste site** com a marcação **conectada**.

Se o QR expirar antes de você escanear (aviso **Tempo esgotado. Feche e clique em Ver QR para tentar de novo.**), feche a janela e use o botão **Ver QR** da instância na lista. Esse botão só aparece enquanto a instância está desconectada.

Para remover uma instância, use o botão de excluir na linha dela. A instância é desconectada e removida — a ação não pode ser desfeita.

> 💡 Use um número dedicado ao servidor (um chip só para isso). Se você desconectar o aparelho pelo celular, basta voltar em **Instâncias**, clicar em **Ver QR** e escanear de novo.

### Passo 2 — Configurar a origem dos telefones

1. Abra **Sender → Configurações**.
2. No bloco **Origem dos dados de contas**, confira:
   - **Banco de dados** — o banco do jogo onde fica a tabela de contas;
   - **Tabela de contas** — a tabela de contas do MuOnline;
   - **Coluna da conta** — a coluna que identifica o login;
   - **Coluna do telefone** — a coluna onde o telefone é gravado.
3. Os valores padrão já atendem a maioria dos servidores. Só mude se o seu banco guarda o telefone em outro lugar — e, nesse caso, com ajuda de quem conhece o banco do jogo.
4. Clique em **Salvar**.

O campo personalizado do cadastro precisa gravar na mesma coluna informada em **Coluna do telefone** (o widget de aceite do plugin já usa essa coluna automaticamente) — ver "Como o jogador informa o telefone".

### Passo 3 — Revisar os templates

1. Abra **Sender → Templates**. A lista mostra, para cada evento: **Evento**, **Descrição**, **Tipo** e **Status** (`padrão` quando o texto nunca foi alterado, `editado` quando você personalizou).
2. Clique em editar no evento desejado. Na tela de edição você vê:
   - **Tipo** — a categoria da mensagem (`urgent`, `status`, `update` ou `news`), apenas informativa;
   - **Variáveis disponíveis** — as variáveis daquele evento; clique em uma para copiar;
   - **Título** — vai em negrito na primeira linha da mensagem;
   - **Corpo** — o texto da mensagem;
   - **Pré-visualização** — mostra como a mensagem vai ficar enquanto você digita.
3. Clique em **Salvar**. Para voltar ao texto original, use **Restaurar padrão** (as suas alterações são perdidas).

O WhatsApp aceita formatação simples no texto: `*negrito*`, `_itálico_`, `~tachado~` e ```` ```mono``` ````.

#### Variáveis disponíveis em todos os templates

| Variável | O que vira na mensagem |
|----------|------------------------|
| `{{server}}` | Nome do servidor |
| `{{url}}` | Endereço do site |
| `{{logo}}` | Endereço do logo do site |
| `{{date}}` | Data do envio |
| `{{time}}` | Hora do envio |

E, quando o destinatário é uma conta do jogo:

| Variável | O que vira na mensagem |
|----------|------------------------|
| `{{name}}` | Nome cadastrado na conta (ou o login, se não houver nome) |
| `{{login}}` | Login da conta |
| `{{pid}}` | Identificação pessoal cadastrada na conta |
| `{{email}}` | E-mail da conta |
| `{{character}}` | Primeiro personagem da conta |
| `{{characters}}` | Todos os personagens da conta, separados por vírgula |

### Passo 4 — Confirmar a tarefa agendada

As mensagens saem pela fila de tarefas. Em **Configurações → Tarefas**, confira que a tarefa **Processar Fila** está ativa (ela já vem ativa e roda a cada minuto). Sem ela, as mensagens ficam paradas na fila.

### Passo 5 — Testar

Crie uma conta de teste com telefone, ou faça uma ação que gere evento, e acompanhe em **Sender → Auditoria de envios**.

---

## Eventos disponíveis

Cada linha abaixo é um template que você pode editar. As variáveis listadas são as específicas do evento — as globais e as da conta (tabelas acima) valem em todos.

| Evento | Quando é enviado | Variáveis do evento |
|--------|------------------|---------------------|
| `welcome` | Conta criada (ou e-mail confirmado, se a confirmação de e-mail estiver ligada) | `{{server}}` |
| `password_recovery` | Jogador pediu recuperação de senha em "Esqueci a senha" | `{{link}}` (link para gerar a nova senha), `{{expires_in}}` (validade em minutos) |
| `password_reset` | Senha redefinida com sucesso | — |
| `donate_received` | Doação/compra de créditos confirmada pelo meio de pagamento | `{{amount}}` (valor), `{{method}}` (meio de pagamento) |
| `package_purchased` | Pacote comprado | `{{package}}`, `{{amount}}` |
| `mercado_item_sold` | Item do jogador vendido no Mercado de itens | `{{item}}`, `{{price}}`, `{{buyer}}` |
| `directmarket_trade_done` | Venda concluída no DirectMarket (aviso ao vendedor) | `{{item}}`, `{{price}}`, `{{buyer}}` |
| `directmarket_item_received` | Item entregue pelo DirectMarket (aviso ao comprador) | `{{item}}` |
| `directmarket_sale_refunded` | Venda do DirectMarket estornada | `{{item}}`, `{{amount}}` |
| `accountmarket_sold` | Conta vendida no AccountMarket (enviado ao telefone de contato informado no anúncio) | `{{sold_account}}`, `{{price}}`, `{{buyer}}` |
| `auction_outbid` | Lance do jogador superado no Leilão | `{{item}}`, `{{bid}}` (lance atual) |
| `auction_won` | Jogador venceu o Leilão | `{{item}}`, `{{price}}`, `{{auction}}` |
| `raffle_won` | Jogador ganhou um Sorteio (Rifa) | `{{raffle}}`, `{{number}}` |
| `rescue_requested` | Saque solicitado | `{{amount}}` |
| `rescue_paid` | Saque pago | `{{amount}}` |
| `rescue_rejected` | Saque recusado | `{{amount}}` |
| `ticket_replied` | Ticket de suporte respondido pela equipe | `{{ticket}}` (número), `{{link}}` |
| `subscription_activated` | Assinatura VIP ativada | `{{plan}}` |
| `subscription_renewed` | Assinatura VIP renovada (cobrança paga) | `{{plan}}`, `{{amount}}` |
| `subscription_canceled` | Assinatura VIP cancelada | `{{plan}}`, `{{valid_until}}` (até quando os benefícios valem) |
| `ranking_reward` | Prêmio de ranking pago | `{{prize}}`, `{{position}}`, `{{ranking}}` |
| `admin_bonus` | Bonificação enviada pelo administrador — não é disparado automaticamente pelo site; fica disponível para o disparo externo (abaixo) | `{{bonus}}`, `{{reason}}` |

Observações:

- A doação confirmada **não** gera o aviso `donate_received` quando o pedido veio do DirectMarket, do AccountMarket ou de uma assinatura — esses casos têm os seus próprios eventos.
- Eventos de plugins (Leilão, Sorteio, Saque, HelpDesk, Assinaturas, Mercados, Prêmio de ranking) só acontecem se o plugin correspondente estiver instalado e ativo.

---

## Auditoria de envios

Em **Sender → Auditoria de envios** você acompanha cada tentativa de envio, com as colunas **Data**, **Evento**, **Conta**, **Telefone**, **Instância**, **Status** e **Detalhe**. A busca filtra por qualquer um desses dados (login, telefone, evento).

| Status | Significado |
|--------|-------------|
| `sent` | Enviada com sucesso (com o logo como imagem) |
| `sent_text_fallback` | A imagem do logo foi recusada e a mensagem foi reenviada só com texto |
| `invalid_phone` | O telefone da conta está vazio ou fora do padrão — nada foi enviado |
| `error` | O envio falhou; o motivo aparece em **Detalhe** |

---

## Reenvio automático de mensagens que falharam

Como o envio acontece pela fila de tarefas, uma mensagem que **falhou** (número temporariamente indisponível, instância desconectada, instabilidade) **não se perde**: a fila tenta de novo sozinha, esperando um pouco mais a cada nova tentativa, até esgotar o limite de tentativas. Cada tentativa aparece como uma linha na auditoria.

Quando todas as tentativas falham, a tarefa é marcada como falha e você recebe um aviso no painel. Em **Configurações → Fila de Jobs** você vê o resumo por status, o detalhe de cada tarefa e pode **reprocessar** manualmente depois de corrigir a causa (por exemplo, reconectar a instância).

Mensagens com telefone inválido **não** entram em retentativa — corrija o telefone na conta.

---

## Disparo externo (integrações)

Além dos eventos automáticos, outros sistemas seus (um bot, um painel próprio, uma automação) podem pedir ao site que envie qualquer template para uma conta ou para um telefone avulso. Para isso existe um **segredo de disparo**:

1. Abra **Sender → Configurações**, bloco **Endpoint de disparo**.
2. Preencha **Segredo do disparo** (o painel sugere um valor aleatório — pode usar a sugestão) e clique em **Salvar**.
3. Repasse o segredo para quem mantém a integração: ele precisa ser enviado em cada pedido de disparo.

Enquanto o campo fica vazio, o painel exibe o aviso de que o disparo externo aceita um segredo embutido, igual em todas as instalações — e você recebe um aviso no painel cada vez que ele é usado. **Defina um segredo próprio** o quanto antes; depois de configurado, só ele é aceito.

Os disparos externos também passam pela auditoria e têm um limite de pedidos por minuto por origem, para evitar abuso.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|-----------------------|-----------------|
| Conectar um número de WhatsApp (QR code) | **Sender → Instâncias** → **Nova instância** → **Criar e escanear QR** |
| Reconectar uma instância desconectada | **Sender → Instâncias** → botão **Ver QR** da instância |
| Remover uma instância | **Sender → Instâncias** → botão de excluir da instância |
| Editar o texto de uma mensagem | **Sender → Templates** → editar o evento → **Título** / **Corpo** → **Salvar** |
| Voltar o texto original de uma mensagem | **Sender → Templates** → editar o evento → **Restaurar padrão** |
| Ver o que foi enviado, para quem e se deu certo | **Sender → Auditoria de envios** |
| Definir de onde vem o telefone dos jogadores | **Sender → Configurações** → **Origem dos dados de contas** |
| Definir o segredo para integrações externas | **Sender → Configurações** → **Endpoint de disparo** → **Segredo do disparo** |
| Pedir o telefone no cadastro do site | **Configurações → Acessos → Cadastro** → **Custom fields** → **Adicionar** |
| Garantir que as mensagens saem da fila | **Configurações → Tarefas** → tarefa **Processar Fila** ativa |
| Reprocessar mensagens que falharam todas as tentativas | **Configurações → Fila de Jobs** |
| Definir o nome do servidor (prefixo das instâncias) | Configurações gerais do site |

---

## Dicas e boas práticas

- **Número dedicado.** Use um chip exclusivo para o servidor. Se o mesmo número for usado em outro aparelho ou desconectado pelo celular, as mensagens param até você escanear o QR de novo.
- **Crie a instância `notifications` primeiro.** É a instância padrão — sem ela, as notificações automáticas não têm por onde sair.
- **Mantenha as mensagens curtas e com cara de aviso, não de propaganda.** Textos longos ou promocionais em excesso aumentam a chance de bloqueio do número pelo WhatsApp.
- **Não apague as variáveis importantes.** Em `password_recovery`, por exemplo, o `{{link}}` é o que permite ao jogador trocar a senha. Use a **Pré-visualização** antes de salvar.
- **Peça o telefone no cadastro.** Sem telefone na conta, nenhum evento chega ao jogador. Marque o campo como obrigatório se o WhatsApp for o seu canal principal.
- **Acompanhe a auditoria nos primeiros dias.** Muitos `invalid_phone` indicam que os jogadores estão digitando o número sem DDD ou com código de país errado — ajuste o rótulo do campo no cadastro para orientar.
- **Troque o segredo de disparo** se ele vazar ou se alguém que tinha acesso sair da equipe.

---

## Perguntas frequentes

**A instância aparece como desconectada. O que faço?**
Clique em **Ver QR** na linha da instância em **Sender → Instâncias** e escaneie de novo pelo celular (Aparelhos conectados → Conectar um aparelho). As mensagens que ficaram na fila são reenviadas automaticamente nas próximas tentativas.

**Posso ter mais de um número conectado?**
Sim, você pode criar várias instâncias, mas as notificações automáticas saem sempre pela instância **padrão** (sufixo `notifications`). As demais só são usadas por disparos externos que indiquem a instância.

**O jogador não recebeu a mensagem. Por onde começo?**
Pela **Auditoria de envios**: procure pelo login. Se não há nenhuma linha, a conta não tem telefone ou o evento não aconteceu. Se o status é `invalid_phone`, o telefone está fora do padrão. Se é `error`, leia o **Detalhe** e confira a instância.

**Posso criar um evento novo?**
Não pelo painel — a lista de eventos é fixa. Você pode personalizar o texto de qualquer um deles e, para avisos manuais, usar o template `admin_bonus` por disparo externo.

**A mensagem vai com imagem?**
Sim: o logo do site é enviado como imagem, com o texto na legenda. Se o envio da imagem for recusado, a mensagem vai só com texto (status `sent_text_fallback`).

**Por que o nome da instância tem o nome do meu servidor na frente?**
Para isolar as suas instâncias das de outros servidores. O prefixo é automático e não pode ser removido — por isso o nome do servidor precisa estar configurado.

**Quanto tempo leva para a mensagem sair?**
Normalmente até um minuto, que é o intervalo da tarefa **Processar Fila**. Se demorar mais, confira em **Configurações → Tarefas** se a tarefa está ativa e rodando.

---

> Precisa de ajuda para conectar o número ou revisar os textos? Entre em contato com o suporte.
