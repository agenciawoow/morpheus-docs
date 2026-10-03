# Passe de Batalha (Battle Pass) — Guia do Cliente

No painel administrativo o sistema aparece como **Battle Pass**; no site, o serviço é chamado de **Passe de Batalha**.

Este guia explica, de forma simples, **o que é** o Passe de Batalha do seu servidor, **como o jogador usa** e **como você configura** tudo pelo painel administrativo. Não é necessário nenhum conhecimento técnico.

---

## O que é o Passe de Batalha?

O Passe de Batalha é um sistema de **progressão por temporada**. Os jogadores **acumulam XP** (pontos de experiência do passe) realizando ações no site e, a cada faixa de XP atingida, **desbloqueiam recompensas**.

É uma ferramenta poderosa de **engajamento e monetização**:

- Mantém os jogadores ativos durante toda a temporada, sempre buscando o próximo tier.
- Oferece uma **faixa Grátis** (para todos) e uma **faixa Premium** (paga ou liberada pelo VIP), gerando receita.
- Premia quem joga com frequência com coins, VIP, itens e recompensas exclusivas.

---

## Conceitos principais

Antes de configurar, vale entender as quatro peças do sistema:

### 1. Temporada

A **temporada** é o "ciclo" do passe, com **data de início** e **data de término**. Normalmente você mantém **uma temporada ativa por vez** (por exemplo, uma temporada por mês). Quando uma temporada termina, você cria uma nova com recompensas diferentes para renovar o interesse.

Cada temporada tem título e descrição próprios (em todos os idiomas do site), o seu **Preço de compra** do Passe Premium e o **VIP mínimo para premium grátis**.

### 2. XP e Fontes de XP

O **XP** é o que move o jogador para frente no passe. Ele é ganho através das **Fontes de XP** que você configurar na temporada — por exemplo, *login diário no site*, *lance em leilão*, *compra de pacote*, etc.

Cada fonte de XP define:

- O **Tipo de ação** que concede XP.
- A **Quantidade de XP** concedida por ocorrência.
- **Limite diário** e **Limite total** (opcionais): quantas vezes por dia e/ou na temporada inteira o jogador pode ganhar aquele XP.
- Um **Nome** amigável (em vários idiomas), exibido ao jogador na seção "Como ganhar XP" da página do passe.
- O estado **Ativo** — fontes inativas não concedem XP nem aparecem para o jogador.

### 3. Tiers

Os **tiers** são as faixas de progresso da temporada. Cada tier tem um **Nível** (1, 2, 3...) e exige uma quantidade de **XP Necessário** acumulado para ser desbloqueado (por exemplo: Nível 1 = 100 XP, Nível 2 = 250 XP, e assim por diante).

Quando o XP do jogador alcança o exigido por um tier, ele **desbloqueia as recompensas** daquele tier.

### 4. Recompensas

Cada tier pode ter **uma ou mais recompensas**. Toda recompensa pertence a uma das duas opções do campo **Faixa**:

- 🆓 **Grátis** — disponível para **todos** os jogadores.
- ⭐ **Premium** — disponível apenas para quem possui o **Passe Premium** daquela temporada.

O jogador **resgata** cada recompensa manualmente quando o tier está desbloqueado. Cada recompensa só pode ser resgatada **uma vez** por jogador.

---

## Como o jogador usa

Do ponto de vista do jogador, a experiência é bem direta:

1. Ele acessa a página **Battle Pass** no site. Se não houver temporada em andamento, a página avisa que não há temporada ativa no momento.
2. No topo vê o **título**, a **descrição** e o **período** da temporada.
3. Logado, vê a sua **barra de progresso** com o **Nível** atual e o **XP** acumulado.
4. A trilha mostra, tier a tier, as recompensas da faixa **Grátis** (acima) e da faixa **Premium** (abaixo), com o XP exigido de cada tier.
5. Quando um tier é desbloqueado, aparece o botão **Resgatar** na recompensa. Se o tier tiver mais de uma recompensa na mesma faixa, um único clique em **Resgatar** entrega todas elas de uma vez. Recompensas já resgatadas ficam marcadas como **Resgatado**.
6. Recompensas da faixa **Premium** aparecem bloqueadas até ele ter o Passe Premium.
7. No fim da página, a seção **Como ganhar XP** lista as fontes de XP ativas, com o XP de cada uma e o limite diário quando houver (ex.: "Até 1×/dia").

As recompensas caem direto para o jogador ao resgatar — coins vão para a conta, o VIP é ativado, os itens vão para o **armazém** da conta, e assim por diante. Se o armazém estiver cheio, o resgate não é concluído e o jogador recebe o aviso para liberar espaço e tentar de novo.

> 💡 O XP de **Login diário no site** é concedido quando o jogador, logado, **abre a página do Battle Pass**. Vale divulgar a página para os jogadores criarem o hábito de visitá-la.

---

## O Passe Premium

A faixa Premium é a parte **paga** do sistema. Existem **duas formas** de um jogador obter o Passe Premium de uma temporada:

1. **Comprando** — pelo botão **Comprar Premium** na página do passe (exibido com o valor), que leva à tela **Passe Premium** com a lista de meios de pagamento já configurados no seu site ("Pagar com ..."). O valor é o **Preço de compra** definido na temporada. Com o preço em **0**, a compra fica desabilitada e o botão não aparece.
2. **Automaticamente pelo VIP** — você pode definir o **VIP mínimo para premium grátis** na temporada. Jogadores com aquele VIP ou superior recebem o Passe Premium **sem custo adicional** ao abrir a página do passe, como um benefício do VIP.

> 💡 O preço e o VIP mínimo são definidos **por temporada**, então você pode ajustar a estratégia a cada ciclo. Deixando o preço em 0 e sem VIP mínimo, a lista de temporadas mostra **Acesso livre** na coluna Premium.

---

## Como configurar (passo a passo)

Toda a configuração é feita no painel administrativo, em **Battle Pass → Temporadas**. O fluxo recomendado é:

### Passo 1 — Criar a Temporada

1. Acesse **Battle Pass → Temporadas** no menu lateral.
2. Clique em **Adicionar** e preencha o card **Temporada**:
   - **Título** (em todos os idiomas do site), ex.: "Temporada de Verão".
   - **Ativo** — ligue quando estiver pronta para começar.
   - **Descrição** (em todos os idiomas), exibida ao jogador no topo da página.
   - **Data de início** e **Data de término** (data e hora).
3. No card **Passe Premium**, defina:
   - **VIP mínimo para premium grátis** (opcional): jogadores com este VIP ou superior recebem premium automaticamente.
   - **Preço de compra**: o valor cobrado pelo Passe Premium. Defina como 0 para desabilitar a compra.
4. Clique em **Salvar**.

Na lista, a temporada que está dentro do período e ativa recebe a marca **Em andamento**. As colunas mostram **Período**, **Premium** (VIP mínimo, preço ou "Acesso livre") e **Status**.

### Passo 2 — Criar os Tiers

Na lista de temporadas, clique no botão **Tiers** da temporada (também disponível no topo da tela de edição). Depois:

1. Clique em **Adicionar**.
2. Informe o **Nível** (número do tier: 1, 2, 3...) e o **XP Necessário** (XP total para desbloquear).
3. Clique em **Salvar** e repita para cada tier.

A tabela de Tiers mostra, para cada nível, o XP necessário e quantas recompensas **Grátis** e **Premium** ele já tem. Os tiers podem ser **reordenados** arrastando pela alça à esquerda de cada linha.

> Dica: deixe os primeiros tiers **fáceis** (XP baixo) para o jogador sentir progresso rápido, e aumente a exigência gradualmente.

### Passo 3 — Adicionar as Recompensas

Ainda na tela de Tiers, clique em **Adicionar Recompensa** na linha do tier e configure:

- **Faixa**: Grátis ou Premium.
- **Tipo de recompensa**: Coins, VIP, Item ou Personalizado (veja a seção abaixo).
- Os campos específicos do tipo escolhido.

Você pode colocar **várias recompensas no mesmo tier** — por exemplo, uma grátis e uma premium. Cada recompensa aparece como uma linha abaixo do seu tier, com a marcação da faixa e botões de editar e excluir.

### Passo 4 — Configurar as Fontes de XP

Clique em **Fontes de XP** no topo da tela de Tiers (ou da tela de edição da temporada) e cadastre as formas de o jogador ganhar XP:

1. Clique em **Adicionar**.
2. Preencha o **Nome** exibido ao jogador (em todos os idiomas do site).
3. Escolha o **Tipo de ação**.
4. Deixe **Ativo** ligado.
5. Defina a **Quantidade de XP** por ocorrência.
6. Defina o **Limite diário** e o **Limite total**, se quiser evitar abuso. Em branco = **Sem limite**.
7. Clique em **Salvar**.

A lista mostra Tipo de ação, Quantidade de XP, Limite diário, Limite total e Status, e também pode ser reordenada arrastando.

> Comece com algo simples, como **Login diário no site**, e vá adicionando mais fontes conforme quiser.

### Passo 5 — Revisar e Publicar

Confira a página pública do passe, verifique se os tiers e recompensas estão como você planejou, ligue o **Ativo** da temporada e está pronto! Os jogadores já começam a acumular XP.

---

## Tipos de recompensa

Ao cadastrar uma recompensa, no campo **Tipo de recompensa** você escolhe entre:

| Tipo | Campos | O que entrega |
|------|--------|---------------|
| 💰 **Coins** | **Tipo de coin**, **Quantidade** | Uma quantidade da moeda escolhida (WCoin, Goblin Point, etc.), creditada direto na conta. |
| ⭐ **VIP** | **Tipo de VIP**, **Dias** | Um período de VIP (em dias) do tipo escolhido, somado ao que o jogador já tiver. |
| 🎁 **Item** | Busca do item + opções | Um item do jogo, entregue no armazém da conta. Você escolhe o item e as suas opções (level, Luck, Skill, Option, Excellent, Ancient, Harmony, Socket, etc.) por um seletor visual com **pré-visualização**. |
| ⚙️ **Personalizado** | **Título de exibição** + ação personalizada | Uma recompensa avançada, com um título próprio (em vários idiomas) e uma ação executada no banco do jogo no momento do resgate. **Use com cuidado e com ajuda de quem conhece o banco do seu servidor.** |

> Ao escolher um **Item**, você verá uma prévia de como ele ficará — com a imagem e a descrição do item, igual ao jogo — enquanto ajusta as opções.

---

## Tipos de ação das Fontes de XP

No campo **Tipo de ação** você escolhe qual ação do jogador concede o XP. O sistema concede o XP automaticamente quando a ação acontece:

| Tipo de ação | Quando concede XP |
|--------------|-------------------|
| **Login diário no site** | Quando o jogador logado abre a página do Battle Pass (use o Limite diário = 1). |
| **Compra de pacote (Packages)** | Ao comprar um pacote. |
| **Recarga de coins (Exchange)** | Ao recarregar coins. |
| **Conversão de coins (Exchange)** | Ao converter coins. |
| **Compra no WebShop** | Ao comprar no WebShop. |
| **Compra de bilhete de rifa** | Ao comprar bilhete de rifa. |
| **Lance em leilão** | Ao dar um lance em leilão. |
| **Abertura de LootBox** | Ao abrir uma LootBox. |
| **Consulta SQL personalizada** | Opção avançada: concede XP com base em uma verificação personalizada no banco do jogo (ex.: ter um personagem acima de certo level). **Use com cuidado e com ajuda de quem conhece o banco do seu servidor.** |

> Os tipos ligados a outros plugins (Packages, Exchange, WebShop, rifa, leilão, LootBox) só concedem XP se o plugin correspondente estiver instalado e em uso no seu site.

---

## Estatísticas

Na lista de temporadas, o botão **Estatísticas** no topo mostra:

- **Temporadas ativas** (em relação ao total cadastrado).
- **Participantes** — jogadores que já têm progresso no passe.
- **Participantes premium** — quantos possuem o Passe Premium.
- **Recompensas resgatadas** — total de resgates.
- A tabela **Desempenho das temporadas**, com Participantes, Premium e Recompensas resgatadas de cada temporada.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|------------------------|-----------------|
| Criar/editar temporadas | **Battle Pass → Temporadas → Adicionar / Editar** |
| Título e descrição da temporada | Card **Temporada** → campos **Título** e **Descrição** |
| Período da temporada | Card **Temporada** → **Data de início** e **Data de término** |
| Ligar/desligar a temporada | Card **Temporada** → interruptor **Ativo** |
| Preço do Passe Premium | Card **Passe Premium** → **Preço de compra** (0 desabilita a compra) |
| Premium grátis pelo VIP | Card **Passe Premium** → **VIP mínimo para premium grátis** |
| Criar/reordenar tiers | Botão **Tiers** da temporada → **Adicionar** / arrastar as linhas |
| Nível e XP do tier | Formulário do tier → **Nível** e **XP Necessário** |
| Adicionar recompensa a um tier | Tela de Tiers → botão **Adicionar Recompensa** na linha do tier |
| Faixa e tipo da recompensa | Formulário da recompensa → **Faixa** e **Tipo de recompensa** |
| Formas de ganhar XP | Botão **Fontes de XP** (tela de Tiers ou edição da temporada) → **Adicionar** |
| Limites de XP | Formulário da fonte → **Limite diário** e **Limite total** |
| Acompanhar resultados | **Battle Pass → Temporadas** → botão **Estatísticas** no topo |

---

## Dicas e boas práticas

- **Planeje a temporada inteira antes de ativar.** É mais fácil montar todos os tiers e recompensas e só então ligar o **Ativo**.
- **Equilibre as recompensas Grátis e Premium.** A faixa gratuita precisa ser atraente o suficiente para engajar; a premium precisa ser claramente melhor para incentivar a compra.
- **Use os limites de XP** para que ninguém "fure" a progressão ganhando XP demais de uma única fonte.
- **Recompensas exclusivas vendem.** Itens que só existem no passe daquela temporada criam senso de urgência.
- **Renove a cada temporada.** Recompensas novas e um tema diferente mantêm o sistema sempre fresco.
- **Aproveite o VIP mínimo** para transformar o Passe Premium em mais um benefício do seu VIP, agregando valor aos pacotes.
- **Divulgue a página do Battle Pass.** O XP de login diário é concedido ao abrir a página, então quanto mais o jogador visitar, mais engajado fica.

---

## Perguntas frequentes

**O jogador perde o XP quando a temporada acaba?**
O XP e o progresso são **por temporada**. Ao iniciar uma nova temporada, o jogador recomeça — o que mantém a competição sempre renovada.

**Posso ter mais de uma temporada ativa?**
O site exibe **apenas uma** temporada: a mais recente que esteja ativa e dentro do período. Mantenha uma temporada ativa por vez para evitar confusão.

**O jogador pode resgatar a mesma recompensa duas vezes?**
Não. Cada recompensa é resgatada **uma única vez** por jogador.

**O que acontece se o jogador comprar o Premium no meio da temporada?**
Ele passa a ter acesso a **todas** as recompensas Premium dos tiers que já desbloqueou (e dos próximos), bastando resgatá-las.

**E se o jogador já for VIP?**
Se você definiu o **VIP mínimo para premium grátis** na temporada e ele atende ao requisito, o Passe Premium é liberado **automaticamente** quando ele abre a página do passe.

**Posso desabilitar a venda do Premium e deixar só pelo VIP?**
Sim. Defina o **Preço de compra** como 0 e configure o **VIP mínimo para premium grátis**. O botão de compra some e só o VIP libera a faixa Premium.

**O que acontece se o armazém do jogador estiver cheio ao resgatar um item?**
O resgate não é concluído e o jogador recebe um aviso. Ele pode liberar espaço no armazém e resgatar depois — a recompensa continua disponível.

**As recompensas de item têm risco de duplicação?**
Não. Cada item entregue recebe um identificador único no momento do resgate, então cada jogador recebe um item legítimo e individual.

---

> Precisa de ajuda para montar a sua primeira temporada? Entre em contato com o suporte — podemos sugerir uma configuração de tiers e recompensas sob medida para o seu servidor.
