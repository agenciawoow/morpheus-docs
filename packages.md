# Pacotes (Packages) — Guia do Cliente

Este guia explica, de forma simples, o que são os Pacotes, como o jogador compra e como você configura tudo pelo painel administrativo. Não é necessário conhecimento técnico.

---

## O que são os Pacotes?

Os Pacotes são **ofertas prontas** que o jogador compra com o **saldo de uma carteira** do site (normalmente o crédito de doação). Cada pacote pode entregar **moedas do site**, **VIP**, um **kit de itens** — ou uma combinação disso — tudo de uma vez.

É a sua **vitrine de monetização**: transforma o crédito do jogador em recompensas atrativas, com preços e combos definidos por você. No site, a loja aparece como **Loja de Créditos** / **Pacotes**.

---

## Conceitos principais

### O pacote

Tem um **Nome**, uma **Descrição**, uma **Imagem**, uma **Categoria** (obrigatória), um **Preço** e a **Carteira** usada no pagamento. Ao comprar, o jogador recebe o conteúdo do pacote na hora.

### O que o pacote entrega

Um pacote pode incluir, em qualquer combinação:
- **Moedas** do site (ex.: WCoin, Goblin Points) — uma ou várias, com a quantidade de cada;
- **VIP** — um **Tipo** de VIP por uma quantidade de **Dias**;
- **Kit** — um conjunto de itens entregue no baú (os kits vêm da **Loja**; esse card só aparece quando o plugin da Loja está ativo).

### Categorias

Todo pacote pertence a uma **categoria** (ex.: "Promoções", "VIP", "Moedas"). Na vitrine, o jogador navega por categoria; categorias inativas e seus pacotes não aparecem.

### Limite de vendas e visibilidade

- **Máx. vendas:** limita quantas vezes o pacote pode ser vendido (ideal para ofertas limitadas). A vitrine mostra a **Disponibilidade** e, ao atingir o limite, o pacote aparece como **Esgotado**.
- **Oculto:** mantém o pacote cadastrado, mas fora da vitrine.
- **Ativo:** liga/desliga o pacote.

### Como o VIP é entregue

Se o jogador já tem VIP, o pacote **nunca rebaixa o tipo nem zera os dias** que ele já possui: os dias são somados ao VIP de maior nível entre o atual e o do pacote. Ao comprar um pacote com um tipo de VIP diferente do atual, o jogador vê um aviso e confirma se quer continuar.

---

## Como o jogador usa

1. O jogador acessa **Pacotes** no site e vê as ofertas disponíveis, por categoria, com **Preço**, conteúdo resumido e **Disponibilidade** (quando há limite).
2. Em **Visualizar**, vê o **Preço**, o seu **Saldo** na carteira do pacote e **O que está incluído** (VIP, moedas e itens do kit).
3. Clica em **Comprar** e confirma — o valor é descontado da **carteira** dele e o conteúdo é entregue na hora.
4. Pacotes com limite de vendas ficam **Esgotado** quando atingem o teto.

> O jogador precisa **estar fora do jogo** para comprar, e precisa de **espaço no baú** quando o pacote entrega um kit — nesse caso nada é cobrado se não houver espaço.

---

## Como configurar (passo a passo)

### 1. Criar as categorias

1. No menu lateral, vá em **Pacotes → Categorias** e clique em **Adicionar**.
2. Informe o **Nome** (traduzível) e marque **Ativo**. Salve.
3. Arraste as linhas da lista para definir a ordem das categorias na vitrine.

### 2. Criar o pacote

1. Vá em **Pacotes → Pacotes** e clique em **Adicionar**.
2. No card **Pacote**: preencha o **Nome** e a **Descrição** (nos idiomas que desejar), marque **Ativo** (e **Oculto**, se quiser escondê-lo), envie a **Imagem**, escolha a **Categoria**, informe o **Preço**, a **Carteira** de pagamento e, se quiser, o **Máx. vendas**.
3. No card **VIP**: escolha o **Tipo** e os **Dias**, se o pacote entregar VIP.
4. No card **Moedas**: informe a quantidade de cada moeda que o pacote entrega (deixe em branco as que não entram).
5. No card **Kit** (só com a Loja ativa): selecione o **Kit** de itens, se aplicável.
6. Clique em **Salvar**. Nome, categoria, preço e carteira são obrigatórios.
7. Na lista de pacotes, arraste as linhas para definir a ordem na vitrine.

### 3. Texto informativo

Em **Configurações → Pacotes** há um único campo, **Informações (HTML)**, com o texto exibido na página de pacotes do site. O mesmo lugar é alcançado pelo botão **Configurações** no topo da lista de pacotes.

### 4. Acompanhar as vendas

- **Painel inicial:** com acesso ao plugin, o painel inicial mostra o card **Packages buying** (título em inglês) com o gráfico de compras no período, a participação de cada pacote e a data do último pacote comprado.
- **Estatísticas** (botão no topo da lista de pacotes): **Pacotes ativos** (sobre o total), **Total de vendas**, **Receita**, número de **Categorias** e a tabela **Pacotes mais vendidos**, com vendas e receita de cada um.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|------------------------|-----------------|
| Criar/editar/ordenar pacotes | **Pacotes → Pacotes** |
| Definir preço e carteira | Campos **Preço** e **Carteira** do pacote |
| Entregar VIP, moedas ou kit | Cards **VIP**, **Moedas** e **Kit** do pacote |
| Limitar quantidade vendida | Campo **Máx. vendas** |
| Agrupar e ordenar categorias | **Pacotes → Categorias** |
| Ocultar da vitrine sem excluir | Opção **Oculto** (ou desmarcar **Ativo**) |
| Texto da página de pacotes | **Configurações → Pacotes** (campo **Informações (HTML)**) |
| Acompanhar desempenho | Botão **Estatísticas** no topo da lista; card de compras no painel inicial |

---

## Dicas e boas práticas

- Monte **combos** (moedas + VIP + kit) com preço atrativo — vendem mais do que itens avulsos.
- Use o **Máx. vendas** para criar **ofertas limitadas** e senso de urgência.
- Capriche em **Imagem** e **Descrição**: a vitrine vende pelo apelo visual.
- Organize por **categorias** para o jogador encontrar rápido o que procura.
- Acompanhe os **Pacotes mais vendidos** nas estatísticas para ajustar preços e combos.

---

## Perguntas frequentes

**Com o que o jogador paga um pacote?**
Com o **saldo de uma carteira** do site (normalmente o crédito de doação) — definida por você em cada pacote.

**O conteúdo é entregue na hora?**
Sim. Moedas, VIP e kit caem na conta do jogador assim que a compra é confirmada.

**O pacote de VIP substitui o VIP que o jogador já tem?**
Não. Os dias são **somados** e o jogador fica com o VIP de maior nível entre o atual e o do pacote — nunca é rebaixado nem perde dias.

**Posso limitar quantas vezes um pacote é vendido?**
Sim. Use o **Máx. vendas**; ao atingir o teto, o pacote fica **Esgotado**.

**Dá para esconder um pacote sem excluí-lo?**
Sim. Marque-o como **Oculto** (sai da vitrine) ou desmarque **Ativo** (desligado), sem perder o cadastro.

**Por que o card Kit não aparece no formulário?**
Ele só aparece quando o plugin da **Loja** (WebShop) está ativo, pois os kits são cadastrados lá.

**Como sei quais pacotes vendem mais?**
Na tela de **Estatísticas**, a tabela **Pacotes mais vendidos** mostra as vendas e a receita de cada um; o painel inicial traz o gráfico do período.
