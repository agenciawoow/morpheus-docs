# Serviços de personagem e de conta — Guia do Cliente

No painel administrativo este sistema aparece em **Configurações → Serviços**. Este guia explica, de forma simples, **o que são** os serviços do painel do jogador, **como o jogador usa** cada um e **como você configura** preços, regras e requisitos pelo painel administrativo. Não é necessário nenhum conhecimento técnico.

---

## O que são os serviços?

Os serviços são as **ações que o jogador faz sozinho pelo site**, sem precisar abrir ticket ou chamar um administrador: resetar o personagem, trocar de nick, mover para outro mapa, limpar o baú, transferir VIP para um amigo, alterar a senha e assim por diante.

Para o seu servidor, isso significa:

- **Menos suporte manual.** O jogador resolve as coisas do dia a dia por conta própria, no painel da conta.
- **Mais receita.** Cada serviço pode ser **grátis**, cobrado em **moeda do site** (WCoin, Goblin Point etc.) ou cobrado em **Zen** do personagem — e você pode dar preço diferente por tipo de VIP.
- **Mais valor para o VIP.** Qualquer serviço pode ser liberado **só para quem é VIP**, virando um benefício a mais dos seus pacotes.
- **Regras sob controle.** Nível mínimo para resetar, mapas permitidos para mover, classes permitidas para troca, dias mínimos para transferir VIP: tudo é configurado por você.

---

## Conceitos principais

### 1. Serviço

Cada opção do painel do jogador é um **serviço**. Os serviços ficam organizados em **dois grupos** que aparecem como menus para o jogador:

- **Minha Conta** — ações da conta: Informações, Alterar PID, Alterar Senha, Alterar E-mail, Limpar Baú, Consertar Items, Transferir VIP e Dados Pessoais.
- **Meus Personagens** — ações de um personagem específico: Informações, Mover, Alterar Nickname, Alterar Classe, Transferir Resets, Limpar Inventário, Resetar, Master Reset, Redistribuir ponto, Rebuild Master Skill e Transferir Ruud.

Esses nomes são os que vêm instalados e você pode **renomear** cada um (em todos os idiomas do site). Plugins instalados podem **acrescentar** serviços a essas listas, por exemplo um serviço de **Limpar PK**: eles aparecem na mesma lista, com preço e liberação configurados do mesmo jeito.

### 2. Taxa (o preço do serviço)

Cada serviço tem uma lista de **Taxas**. Uma taxa diz **o que é cobrado** (Zen do personagem ou uma moeda do site), **quanto** e **de quem** (todos os jogadores ou só determinados tipos de VIP).

- Serviço **sem nenhuma taxa** = **grátis**.
- Você pode ter **mais de uma taxa** no mesmo serviço: por exemplo, cobrar 500 WCoin do jogador Free e 200 WCoin do VIP Ouro.
- A cobrança acontece **no momento em que o jogador confirma** o serviço. Se ele não tiver saldo (moeda ou Zen) suficiente, o serviço não é executado e nada é descontado.

### 3. Liberação por VIP

Em cada serviço você escolhe para quem ele aparece: **Todos** ou apenas alguns tipos de VIP. Quem não está liberado **nem vê** o serviço no painel.

### 4. Regras de cada serviço

Alguns serviços têm uma **tela própria de configuração** (reset, master reset, mover, trocar classe, trocar nick, transferir resets, refazer master skill e transferir VIP). Nela você define requisitos e o que acontece com o personagem. Os demais serviços não têm regras extras: basta definir preço e liberação.

### 5. Personal ID

O **Personal ID** é a senha numérica de 7 dígitos da conta. Alguns serviços sensíveis **sempre** pedem o Personal ID para confirmar: **Limpar Inventário** e **Alterar E-mail**. Para **Alterar PID**, o jogador informa o Personal ID atual e o novo. Serviços adicionados por plugins podem ter regras próprias, definidas na tela de configuração do plugin.

---

## Como o jogador usa

1. O jogador faz **login** no site e abre o **painel da conta**.
2. No menu **Minha Conta** ele vê os serviços da conta. Em **Meus Personagens**, ele vê os cartões de todos os personagens da conta (nome, classe, level, resets) e clica em **Gerenciar** no personagem que quer usar.
3. No menu lateral do painel aparecem apenas os serviços **ativos e liberados** para o tipo de VIP dele.
4. Ao abrir um serviço que tem taxa, um aviso mostra **quanto será cobrado** (ou creditado) antes de confirmar.
5. Nos serviços que mexem no personagem, o jogador precisa estar **fora do jogo** (deslogado). Se estiver online, aparece a mensagem "Você precisa sair do jogo".
6. Ao confirmar, a cobrança é feita, a ação é aplicada e o painel mostra o resultado. Cada uso fica registrado no **log da conta**, que você consulta no painel administrativo.

---

## Como configurar (passo a passo)

Toda a configuração fica em **Configurações → Serviços**. Dentro dessa categoria há um card para cada tela: **Serviços** (a lista geral) e os cards de regras (**Resetar**, **Master resets**, **Transferir resets**, **Refazer master skill**, **Transferir VIP**, **Mudar classe**, **Mudar nick** e **Movimentação**).

### Passo 1 — A lista de serviços

Abra **Configurações → Serviços → Serviços**. A tela mostra os dois grupos (**Minha Conta** e **Meus Personagens**) e, dentro de cada um, os serviços. Nela você pode:

- **Reordenar** arrastando pela alça à esquerda — a ordem aqui é a ordem do menu do jogador.
- Ver, ao lado de cada serviço, para quem ele está liberado (**Liberado para todos** ou os nomes dos VIPs).
- Clicar no botão **Configurar** (engrenagem) dos serviços que têm regras próprias — ele abre a tela de regras daquele serviço.
- Clicar em **Editar** (lápis) para mudar nome, liberação e taxas, ou em **Excluir** (lixeira).
- Clicar em **Adicionar** no topo para criar um serviço novo (normalmente só é necessário quando a documentação de um plugin pedir).

### Passo 2 — Editar um serviço (nome, ativo, liberação)

Ao clicar em **Editar**, o formulário mostra:

- **Nome** — o nome que o jogador vê, em cada idioma do site.
- **Ativo** — desligue para esconder o serviço do painel sem apagar a configuração.
- **Serviço** — o código interno do serviço. **Não altere** nos serviços que já vieram instalados.
- **Serviço de** — o grupo ao qual ele pertence (Minha Conta ou Meus Personagens).
- **URL** — o endereço da tela do serviço. Também não precisa mexer nos serviços instalados.
- **Liberado para** — marque **Todos** ou apenas os tipos de VIP que podem usar. (Este campo só aparece quando o sistema VIP está ativo.)

Clique em **Salvar**.

### Passo 3 — Definir o preço (Taxas)

Ainda na tela de edição, logo abaixo do formulário, está o card **Taxas**. Clique em **Adicionar taxa** e preencha:

| Campo | O que significa |
|-------|-----------------|
| **Condição** | Para quais tipos de VIP esta taxa vale. **Sem nenhum marcado = vale para todos.** Marque, por exemplo, só "Vip Ouro" para dar um preço especial a ele. |
| **Tipo** | **Zen** (desconta do Zen do personagem) ou **Moeda** (desconta do saldo de uma moeda do site). |
| **Moeda** | Aparece quando o tipo é Moeda: qual moeda será cobrada (WCoin, Goblin Point etc.). |
| **Operação** | **Remover** para cobrar do jogador. **Adicionar** credita o valor (use apenas se quiser que o serviço dê Zen como bônus). |
| **Quantidade** | O valor. |

Clique em **Adicionar**. A taxa aparece na tabela com **Tipo**, **Condição** e **Quantidade**; a lixeira remove.

> 💡 **Como montar preço por VIP:** crie uma taxa com a condição "Free" (ou sem condição) com o preço cheio, e outra taxa com a condição do VIP com o preço com desconto. Se um jogador se encaixa em mais de uma taxa, **todas** são cobradas — então use condições que não se sobreponham.

> ⚠️ **Zen só funciona em serviços de personagem.** Nos serviços de conta (Alterar E-mail, Limpar Baú, Consertar Items, Transferir VIP) não existe personagem selecionado, então use **Moeda** para cobrar.

### Passo 4 — Regras de cada serviço

Veja a seção **Cada serviço em detalhe** abaixo. Os serviços com regras próprias podem ser abertos pelo botão **Configurar** na lista ou pelo card correspondente em **Configurações → Serviços**.

### Passo 5 — Testar

Entre no site com uma conta de teste (de preferência uma Free e uma VIP), abra o painel e confira: os serviços certos aparecem, o aviso de preço está correto e a ação acontece como esperado.

---

## Cada serviço em detalhe

### Serviços de personagem (Meus Personagens)

#### Resetar

Regras em **Configurações → Serviços → Resetar** (tela **Configurações de reset**).

**Configurações gerais**

- **Tipo** — como os pontos do reset são tratados:
  - **Cumulativo** — a cada reset o personagem **ganha** os pontos configurados, somando aos que já tem; os atributos atuais são mantidos.
  - **Por pontos** — a cada reset os atributos voltam ao padrão da classe e o personagem recebe um **total** de pontos livres igual a *número de resets × pontos por reset*. É o modelo "reset zera tudo e devolve os pontos".
- **Max** — quantidade máxima de resets que um personagem pode ter. Ao atingir, o jogador vê "Você já possui o máximo de resets".

**Condições** (card abaixo, botão **Adicionar**)

Cada condição vale para uma **faixa de resets** (**Resets de** / **Resets até**), contando o reset que está sendo feito. Assim você pode exigir level 350 do reset 1 ao 10 e level 380 do 11 em diante. Dentro da condição, os campos se repetem **para cada tipo de VIP**:

- **Nível para resetar** — level mínimo exigido.
- **Nível após** — level com que o personagem fica depois do reset (em branco ou 0 = level 1).
- **Zen necessário** — Zen cobrado pelo reset (além das taxas do serviço).
- **Pontos** — pontos concedidos (no tipo Cumulativo, somados; no tipo Por pontos, multiplicados pelo número de resets).
- **Limpar magias** — remove as skills aprendidas.
- **Limpar itens** — remove os itens do inventário.
- **Limpar quests** — zera as quests e volta o personagem para a classe base (1ª evolução).
- **Limpar master level** — zera a árvore de master skill.
- **SQL adicional** — recurso avançado/personalizado para ações extras no reset; use com cuidado e com ajuda de quem conhece o banco do jogo.

Ao resetar, a experiência zera, o personagem volta ao mapa inicial da classe e ganha +1 reset. O jogador vê antes de confirmar os **Requisitos** e uma comparação do "antes" e "depois" (resets, level, zen, classe e o que será limpo).

#### Master Reset

Regras em **Configurações → Serviços → Master resets** (tela **Configurações de master resets**).

**Configurações gerais**

- **Apenas personagem completo** — exige que todos os atributos (Força, Agilidade, Vitalidade, Energia e Comando para Dark Lord) estejam no máximo do servidor. Caso contrário o jogador vê "Seu personagem precisa estar FULL".
- **Limpar skills** — remove as skills aprendidas.
- **Zerar nível** — volta o personagem ao level 1.
- **Resetar classe** — volta o personagem à classe base (quando ligado, substitui "Limpar skills").
- **Limpar pontos de comando** — zera o Comando do Dark Lord junto com os outros atributos.

**Requisitos & Recompensas** (um bloco para cada tipo de VIP)

- **Resets** — resets exigidos. Esses resets são **descontados** do personagem ao fazer o master reset.
- **Level** — level mínimo exigido.
- **Master Level** — master level mínimo (só aparece em servidores com árvore de master skill).
- **Limpar resets** — em vez de descontar só os exigidos, zera **todos** os resets.
- **SQL** — recurso avançado/personalizado para entregar a recompensa do master reset; use com cuidado e com ajuda de quem conhece o banco do jogo.

Em todo master reset os atributos voltam ao padrão da classe, pontos e experiência zeram, o personagem volta ao mapa inicial e ganha +1 master reset. Se um tipo de VIP ficar sem requisitos configurados, o jogador daquele VIP recebe uma mensagem pedindo para contatar a administração.

#### Rebuild Master Skill

Regras em **Configurações → Serviços → Refazer master skill** (tela **Configurações de refazer master skill**).

- **Modo** — **Limpar** apaga a árvore de master skill por completo; **Resetar** devolve os pontos para o jogador redistribuir.
- **Pontos por nível** — no modo Resetar, quantos pontos são devolvidos por master level.
- **Zerar nível** — no modo Resetar, se o master level também volta a zero.

O personagem precisa estar pelo menos na **terceira classe**. O jogador vê o aviso "este comando irá limpar sua árvore de skill" antes de confirmar.

#### Transferir Resets

Regras em **Configurações → Serviços → Transferir resets** (tela **Configurações de transferir resets**).

- **Zerar pontos** — ao transferir, os pontos e atributos do personagem que **envia** voltam ao padrão da classe (evita que ele fique com os pontos dos resets que já não tem).

O jogador informa a **Quantidade de resets** e escolhe o **personagem destino**, que precisa ser **da mesma conta**. Não é possível transferir mais resets do que o personagem tem.

#### Transferir Ruud

Sem tela de regras: só preço e liberação. O jogador informa a **Quantidade** e o nome do personagem destino, que pode ser de **qualquer conta**. A conta de destino também precisa estar fora do jogo. Aparece apenas em servidores com Ruud.

#### Mover

Regras em **Configurações → Serviços → Movimentação** (tela **Configurações de movimentação**).

- **Quando PK** — permite mover mesmo com status de PK. Desligado, o jogador PK vê "Você não pode se mover enquanto estiver PK".
- **Mapas permitidos** — marque os mapas que podem ser escolhidos. Só eles aparecem na lista do jogador, e o personagem é levado ao ponto de nascimento de cada mapa.

#### Alterar Nickname

Regras em **Configurações → Serviços → Mudar nick** (tela **Configurações de mudar nick**).

- **Validação regex** — a regra de caracteres aceitos. O padrão aceita letras, números e sublinhado. Só altere se souber escrever esse tipo de regra.

Além disso, sempre valem: o nick tem de 4 a 10 caracteres, não pode conter as palavras reservadas (webzen, adm, gm, md, nt, dv), não pode estar em uso por outro personagem e o personagem **não pode estar em guild**.

#### Alterar Classe

Regras em **Configurações → Serviços → Mudar classe** (tela **Configurações de mudar classe**).

- **Equalizar pontos** — ao trocar para classes que já nascem com atributos maiores (Magic Gladiator, Dark Lord, Rage Fighter, Grow Lancer e similares), uma parte dos atributos acima do padrão é descontada para manter o equilíbrio.
- **Resetar master level** — zera o master level na troca (só aparece em servidores com árvore de master skill).
- **Classes permitidas** — marque as classes que o jogador pode escolher.

O personagem precisa estar **sem nenhum item equipado** e fora do jogo.

#### Redistribuir ponto

Sem tela de regras. Todos os pontos distribuídos em Força, Agilidade, Vitalidade, Energia (e Comando) voltam ao padrão da classe e a soma vira **pontos livres**. O jogador vê o **Total de pontos** que terá antes de confirmar.

#### Limpar Inventário

Sem tela de regras. Remove **todos** os itens do inventário do personagem. Pede sempre o **Personal ID** e mostra o aviso "CUIDADO! este comando irá deletar todos os itens de seu personagem".

#### Limpar PK (serviço de plugin)

Quando o plugin estiver instalado, aparece em **Meus Personagens** como qualquer outro serviço: o preço e a liberação são definidos em **Configurações → Serviços → Serviços**, e as regras próprias (como exigir Personal ID) ficam na tela de configuração do plugin.

### Serviços de conta (Minha Conta)

#### Informações

A página inicial do painel: nome, e-mail, VIP e vencimento, saldos de carteiras e moedas, Ruud total, última conexão (personagem, servidor, IP e horário), botão de ativar/desativar **2FA** e os cartões dos personagens. Se a conta estiver banida, mostra o **motivo** e **até quando**.

#### Alterar PID

O jogador informa o **Personal ID atual**, o **Novo Personal ID** (exatamente 7 dígitos) e repete o novo.

#### Alterar Senha

Pede a **senha atual**, a nova e a confirmação (1 a 10 caracteres). Ao trocar, as **outras sessões** da conta são encerradas, incluindo o "lembrar de mim".

#### Alterar E-mail

Pede o novo **E-mail**, a **senha atual** e o **Personal ID**. O e-mail não pode estar em uso por outra conta.

#### Limpar Baú

O jogador escolhe o baú (**Todos**, o principal ou um baú estendido, quando o servidor tem baús estendidos) e marca o que limpar: **Limpar itens** e/ou **Limpar zen**. Mostra o aviso "ATENÇÃO! este serviço é irreversível!".

#### Consertar Items

Repara a durabilidade de **todos os itens do baú principal**. Sem opções.

#### Transferir VIP

Regras em **Configurações → Serviços → Transferir VIP** (tela **Configurações de transferir VIP**).

- **Dias mínimos** — quantidade mínima de dias por transferência.
- **Opções de dias** — lista de opções fixas, cada uma com **Dias** e **Nome** (ex.: "7" / "1 semana"). Com opções cadastradas, o jogador escolhe numa lista; sem opções, ele digita a quantidade.

O jogador informa a **Conta** de destino e os **Dias**. Regras automáticas: não pode ser a própria conta; a conta de origem precisa ter VIP; a conta de destino precisa estar **sem VIP** ou com o **mesmo tipo** de VIP; os dias são descontados do vencimento de quem envia e somados ao de quem recebe. As duas contas recebem o registro no log.

#### Dados Pessoais

O jogador preenche **Nome** (obrigatório, até 50 caracteres), **Documento** (CPF), **Telefone**, **Tipo de Pix** e **Chave Pix**. Esses dados são usados por recursos que precisam identificar ou pagar o jogador, como alguns meios de pagamento e os resgates em dinheiro.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|-----------------------|-----------------|
| Ver todos os serviços, reordenar o menu do jogador, abrir as regras de cada um | **Configurações → Serviços → Serviços** |
| Renomear um serviço, desativar, liberar para todos ou só para VIPs | **Configurações → Serviços → Serviços**, botão **Editar** do serviço |
| Definir o preço (grátis, Zen ou moeda), inclusive por tipo de VIP | **Configurações → Serviços → Serviços**, botão **Editar** → card **Taxas** → **Adicionar taxa** |
| Nível, Zen, pontos e limpezas por faixa de resets; máximo de resets; tipo de reset | **Configurações → Serviços → Resetar** |
| Requisitos e efeitos do master reset por VIP | **Configurações → Serviços → Master resets** |
| Modo e pontos devolvidos ao refazer a master skill | **Configurações → Serviços → Refazer master skill** |
| Zerar pontos ao transferir resets | **Configurações → Serviços → Transferir resets** |
| Dias mínimos e opções de dias do Transferir VIP | **Configurações → Serviços → Transferir VIP** |
| Classes permitidas, equalizar pontos na troca de classe | **Configurações → Serviços → Mudar classe** |
| Regra de caracteres do nick | **Configurações → Serviços → Mudar nick** |
| Mapas permitidos e permissão para PK no Mover | **Configurações → Serviços → Movimentação** |
| Nomes dos tipos de VIP usados nas condições e liberações | **Configurações → Economia → Sistema VIP** |
| Moedas disponíveis para cobrança | **Configurações → Economia → Moedas** |
| Ver o que um jogador fez (resets, trocas, transferências) | **Contas → Todas contas**, abrir a conta → botão **Logs** |
| Registrar um serviço de plugin que não apareceu | **Configurações → Serviços → Serviços**, botão **Adicionar** (siga a documentação do plugin) |

---

## Dicas e boas práticas

- **Comece grátis, cobre depois.** Serviços sem taxa são grátis; adicione taxas quando quiser monetizar ou frear abuso (reset em massa, troca de nick a toda hora).
- **Use condições por VIP para dar vantagem real.** Preço menor ou serviço exclusivo para VIP é um dos argumentos mais fortes para vender VIP.
- **Cuidado com taxas sobrepostas.** Uma taxa sem condição vale para **todos**, inclusive VIPs. Se quiser preço diferente por VIP, dê condição a **todas** as taxas.
- **Revise as condições de reset por faixa.** Garanta que **toda** faixa de resets (do 1 ao máximo) está coberta por alguma condição; fora de uma faixa, o reset exige apenas level 1 e não dá pontos.
- **Preencha os requisitos de master reset para todos os VIPs**, inclusive o Free; um VIP sem requisitos bloqueia o serviço para aquele grupo.
- **Serviços irreversíveis** (Limpar Inventário, Limpar Baú) já mostram avisos ao jogador, mas vale cobrar uma taxa simbólica para evitar cliques por engano.
- **Confira depois de atualizar o servidor.** Mudou de season ou de arquivos do jogo? Reveja os mapas permitidos, as classes permitidas e os máximos de level/atributo.

---

## Perguntas frequentes

**Por que o jogador precisa estar fora do jogo?**
Os serviços gravam diretamente no personagem (level, pontos, itens, mapa). Se ele estivesse online, o servidor do jogo sobrescreveria as alterações ao salvar o personagem, ou o jogador poderia duplicar itens. Por isso o painel recusa com "Você precisa sair do jogo".

**Um serviço não aparece para o jogador. O que verificar?**
Três coisas, em **Configurações → Serviços → Serviços**: se o serviço está **Ativo**, se o tipo de VIP do jogador está em **Liberado para** e se o serviço depende de recurso que o servidor não tem (Transferir Ruud só existe em servidores com Ruud; Master Level só com árvore de master skill).

**Posso cobrar em Zen e em moeda ao mesmo tempo?**
Sim. Adicione uma taxa de cada tipo no mesmo serviço; as duas são cobradas. Lembre que Zen só é cobrado em serviços de personagem.

**O jogador não tinha saldo. Ele perdeu algo?**
Não. A verificação de saldo acontece antes de qualquer alteração; sem saldo, nada é executado e nada é descontado.

**Onde vejo quem usou um serviço?**
Em **Contas → Todas contas**, abra a conta e clique em **Logs**: cada reset, troca de nick, transferência e limpeza fica registrada com data, incluindo quem recebeu resets, Ruud ou VIP.

**Posso ter requisitos diferentes para Free e VIP no reset?**
Sim. Dentro de cada condição de reset os campos (nível, Zen, pontos, limpezas) são preenchidos **por tipo de VIP**. O mesmo vale para os requisitos do master reset.

**O que acontece com os resets no master reset?**
Por padrão, os resets exigidos são **descontados** (um personagem com 60 resets, exigência de 50, fica com 10). Ligue **Limpar resets** no VIP desejado para zerar todos.

**O jogador pode transferir VIP para alguém com VIP diferente?**
Não. A conta de destino precisa estar sem VIP ou ter o mesmo tipo; caso contrário o painel mostra "A conta destino já possui" o VIP dela.

---

> Precisa de ajuda para montar a tabela de resets ou os preços por VIP? Entre em contato com o suporte — podemos sugerir uma configuração sob medida para o seu servidor.
