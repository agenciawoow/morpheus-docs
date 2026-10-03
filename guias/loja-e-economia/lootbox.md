# Caixas da Sorte (Loot Box) — Guia do Cliente

Este guia explica, de forma simples, o que são as Caixas da Sorte do seu servidor, como o jogador usa e como você configura tudo pelo painel administrativo. Não é necessário nenhum conhecimento técnico.

---

## O que é uma Caixa da Sorte?

A Caixa da Sorte é um sistema de **abertura de caixas com prêmios aleatórios**. O jogador paga com uma moeda do site para **abrir uma caixa** e recebe **um item sorteado** entre os prêmios que você cadastrou — cada um com a sua **chance de sair**.

É um sistema clássico de **engajamento e monetização**:

- Gera receita contínua com a moeda do site (cada abertura tem um custo).
- Cria emoção e expectativa com a **animação de abertura** e os itens raros.
- Permite **presentear** outros jogadores e até **dar caixas grátis** para novos cadastros.

---

## Conceitos principais

Cada **caixa** que você cria tem:

- Um **Nome**, uma **Descrição** e uma **Imagem**.
- Um **custo por abertura** (uma **Moeda** e uma **Quantidade**).
- Um **Tipo de abertura** (a animação que o jogador vê).
- Uma **lista de itens** que podem ser sorteados, cada um com o seu **Percentual do item**.
- Opcionalmente, uma **Data de expiração** e uma **Quantidade para novos cadastros**.

Ao abrir, o sistema **sorteia um item** respeitando as chances configuradas e o **entrega no baú** do jogador.

### Tipos de abertura

O seletor **Tipo de abertura** aparece com as opções em inglês:

| Opção | Como é |
|--------|--------|
| **Wheel** | Uma roleta gira e para no item sorteado. |
| **Case** | Uma esteira de itens desliza e para no prêmio, no estilo "abertura de caixa". |

### Itens e chances

Para cada item dentro da caixa você define o **Percentual do item** (a chance de ele ser o sorteado). Além disso, o item sorteado pode vir com **atributos aleatórios** — também com percentuais que você controla:

- **Percentuais dos levels** — chance de cada nível.
- **Percentuais das options** e **Percentual de luck**, **Percentual da skill**.
- **Percentuais de excellent**, **Percentual de harmony**, **Percentual de refine**, **Percentuais de socket**.
- **Percentual de ancient** — uma chance para cada variação ancient que o item possui.
- **Durabilidade** — para itens empilháveis (ex.: jóias), define a quantidade entregue.
- Para itens específicos: **Element percentage**, **Pentagram percentage** e **Errtel percentage** (esses rótulos aparecem em inglês).

Ou seja, você pode ter o mesmo item saindo com qualidades diferentes a cada abertura — desde uma versão simples até uma versão "perfeita" e rara.

### Raridade

A **raridade** (nome e cor) que o jogador vê na lista de prêmios **não é definida na caixa**: ela vem do cadastro do item no catálogo do site, em **Itens → Raridades**. Defina a raridade de cada item lá e todas as caixas passam a exibi-la.

---

## Como o jogador usa

1. O jogador acessa a página **Caixas da sorte** no site e vê as caixas ativas, com o **Preço** de cada uma.
2. Em **Visualizar**, ele vê o **Preço**, o seu **Saldo** e a lista de **Itens possíveis** com a raridade de cada um.
3. Clica em **Abrir essa caixa**, confirma, vê a **animação** (roleta ou esteira) e descobre o item ganho.
4. O item vai direto para o **baú** do jogador (em servidores com mais de um baú, a mensagem informa em qual).

> ⚠️ **O jogador precisa estar fora do jogo** para abrir uma caixa, para que o item possa ser entregue ao baú com segurança.

### Presentear

Em **Enviar como presente**, o jogador informa a **Conta** do amigo e clica em **Enviar**. O custo da caixa é debitado de quem envia; o presenteado recebe um aviso de **Presente recebido** e pode abrir a caixa quando quiser, sem pagar.

---

## Caixas grátis no cadastro

No campo **Quantidade para novos cadastros**, você define quantas caixas daquele tipo cada novo jogador ganha ao se registrar. Ele as abre sem pagar. É uma ótima forma de dar as boas-vindas e já apresentar o sistema.

---

## Como configurar (passo a passo)

Tudo é feito no menu lateral **Caixas da sorte**.

### Passo 1 — Criar a caixa

1. Em **Caixas da sorte**, clique em **Adicionar**.
2. No card **Caixa da sorte**, preencha o **Nome** (traduzível), escolha o **Tipo de abertura** (**Wheel** ou **Case**), marque **Ativo**, escreva a **Descrição** e envie a **Imagem**.
3. No card **Preço**, escolha a **Moeda**, informe a **Quantidade** cobrada por abertura e, se quiser, a **Data de expiração** e a **Quantidade para novos cadastros**.
4. Clique em **Salvar**.

> Uma caixa só fica disponível para os jogadores quando está **ativa** e tem **pelo menos um item** cadastrado.

### Passo 2 — Adicionar os itens (prêmios)

1. Na lista de caixas, clique no botão **Itens** da caixa e depois em **Adicionar**.
2. Pesquise e escolha o **Item** do jogo.
3. Defina o **Percentual do item** (a chance de ele ser sorteado).
4. Ajuste os percentuais dos atributos que o item suporta (**levels**, **options**, **luck**, **skill**, **excellent**, **ancient**, **harmony**, **refine**, **socket**, elemento/pentagrama/errtel) e a **Durabilidade** para itens empilháveis.
5. Salve e repita para cada prêmio. A lista mostra o **Drop** (percentual) de cada item.

> As chances são **relativas**: itens com percentual maior saem com mais frequência. Use isso para deixar os itens comuns frequentes e os raros realmente raros.

### Passo 3 — Revisar e publicar

Confira a página pública da caixa e a lista de **Itens possíveis** como o jogador vai ver. Na lista de caixas, arraste as linhas para definir a ordem de exibição.

### Passo 4 — Acompanhar as estatísticas

Em **Estatísticas** (botão no topo da lista de caixas) você vê **Caixas ativas** (sobre o total), **Caixas abertas**, **Pendentes de abrir** (caixas ganhas ou presenteadas que ainda não foram abertas), o total de **Prêmios** cadastrados e a tabela **Desempenho das caixas**, com prêmios e aberturas por caixa.

---

## Onde configurar cada coisa (resumo)

| O que | Onde, no painel |
|-------|----------------|
| Criar/editar/excluir caixas | **Caixas da sorte** |
| Custo, moeda e tipo de abertura | Na **edição da caixa** (cards **Caixa da sorte** e **Preço**) |
| Caixas grátis no cadastro / data de expiração | Na **edição da caixa**, card **Preço** |
| Itens (prêmios) e suas chances | Botão **Itens** da caixa |
| Atributos aleatórios e durabilidade | No cadastro de **cada item** da caixa |
| Raridade exibida nos itens | **Itens → Raridades** (catálogo de itens do site) |
| Ordenar as caixas | Arrastando na **lista de caixas** |
| Acompanhar aberturas | Botão **Estatísticas** no topo da lista de caixas |

---

## Dicas e boas práticas

- **Mostre as chances.** A transparência das probabilidades gera confiança e incentiva a participação.
- **Equilibre comuns e raros.** Itens comuns frequentes mantêm a abertura recompensadora; itens raros valiosos criam o desejo de continuar abrindo.
- **Cadastre as raridades** no catálogo de itens para destacar visualmente os prêmios de elite.
- **Caixas temáticas e por tempo limitado** (com data de expiração) criam senso de urgência.
- **Dê uma caixa grátis no cadastro** para apresentar o sistema a novos jogadores.
- **Capriche na imagem da caixa** — o apelo visual faz diferença na conversão.

---

## Perguntas frequentes

**O jogador pode abrir a caixa logado no jogo?**
Não. Ele precisa estar **fora do jogo** para que o item ganho seja entregue ao baú com segurança.

**O que acontece se o baú estiver cheio?**
A abertura é **bloqueada** e o jogador é avisado de que não há espaço — nenhuma moeda é cobrada e nenhum item se perde.

**O mesmo item pode sair com qualidades diferentes?**
Sim. Você define percentuais para os atributos (nível, excellent, sockets, etc.), então o mesmo item pode sair em versões mais simples ou mais "perfeitas".

**Posso dar caixas sem o jogador pagar?**
Sim — de duas formas: **Quantidade para novos cadastros** (automático para novos jogadores) e o **presente** entre jogadores (um paga para presentear o outro).

**Onde defino a raridade de um item?**
Em **Itens → Raridades**, no catálogo de itens do site. A caixa apenas exibe a raridade cadastrada lá.

**As chances são garantidas?**
As chances são **relativas** entre os itens da caixa. Itens com percentual maior saem com mais frequência; o sorteio é aleatório e respeita exatamente o que você configurou.

**O item ganho é único?**
Sim. Cada item entregue recebe um identificador próprio no momento da abertura, então cada jogador recebe um item legítimo e individual.
