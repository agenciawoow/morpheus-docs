# Mercado de Itens (Item Market) — Guia do Cliente

Este guia explica, de forma simples, o que é o Mercado de Itens, como o jogador usa e como você configura tudo pelo painel administrativo. Não é necessário conhecimento técnico.

---

## O que é o Mercado de Itens?

O Mercado de Itens é uma **loja entre jogadores**: cada um pode **anunciar itens do próprio baú** à venda, e outros jogadores **compram** pagando com o saldo do site, com zen ou até com outros itens. O item sai do baú do vendedor no momento do anúncio e **cai no baú do comprador na hora da compra**; o vendedor recebe o valor (menos a taxa, se houver).

É uma ferramenta de **economia entre jogadores**: movimenta itens raros, cria um mercado vivo dentro do site e gera receita de **taxas** sobre as vendas pagas com carteira.

---

## Conceitos principais

### O anúncio

Quando um jogador coloca um item à venda, é criado um **anúncio** com: o **item** (com todos os atributos — excellent, ancient, sockets, opção, etc.), a **forma de pagamento** (uma **moeda**, uma **carteira**, **zen** ou um **item usado como pagamento**, conforme você permitir) e o **preço**.

### Estados do anúncio

- **Disponível:** aparece no mercado e pode ser comprado.
- **Entregue:** alguém comprou; o item já está no baú do comprador.
- **Expirado:** ficou tempo demais sem vender e saiu do mercado. O jogador recupera o item na página de venda, com o botão **Remover**, que o devolve ao baú.

### A compra e a entrega

A compra é feita na hora: o comprador paga com o saldo escolhido, o item entra no baú dele e o valor vai para o **vendedor** (descontada a **taxa** que você configurar, quando o pagamento é por carteira). Para garantir a segurança do baú, a compra **só é concluída se o comprador e o vendedor estiverem fora do jogo**; caso contrário o jogador recebe um aviso para tentar de novo. Também é preciso ter espaço no baú.

### O que pode ser vendido

Você controla **quais itens e atributos** são permitidos no mercado — pode bloquear itens específicos e ligar/desligar a venda de itens com **excellent, ancient, opção, luck, harmony, refine e socket**.

### Histórico de preços

Com o histórico ligado, o site passa a usar as vendas concluídas para sugerir preços e mostrar tendências: **Preço sugerido** na hora de anunciar, gráfico e **Vendas recentes** na página do item e a página pública **Consulta de preços**, onde qualquer um pesquisa um item e vê **Preço mediano**, **Última venda** e **Itens mais vendidos**. Você define a janela de dias considerada.

---

## Como o jogador usa

1. O jogador abre **Mercado → Itens** no site e vê os itens à venda, com filtros por categoria, classe, excellent, ancient, socket, skill, luck, nível, opção, etc., e ordenação (**Mais novo**, **Mais antigo**, **Maior Preço**, **Menor Preço**).
2. Para **vender**, ele acessa **Vender item**, escolhe um item do baú, define o **Tipo de pagamento** (moeda, carteira, zen ou item), o **Preço** e confirma. O item sai do baú e entra no mercado. Se houver preço mínimo, ele aparece abaixo do campo; se o histórico estiver ligado, aparece o **Preço sugerido** com o botão **Usar este preço**.
3. Para **comprar**, abre a página do item (com **Detalhes do item** e, se habilitado, o **Histórico de preços**) e clica em **Comprar**. O valor é descontado e o item cai no baú na hora.
4. Em **Meus ítens para venda** ele acompanha os próprios anúncios e pode usar **Remover** para tirar um item do mercado (ou recuperar um expirado) — o item volta ao baú.
5. Em **Minhas Compras → Venda de itens**, na área da conta, ele vê o histórico do que comprou.

> O jogador precisa **estar fora do jogo** para anunciar, comprar e remover itens.

---

## Como configurar (passo a passo)

Tudo é feito em **Configurações → Mercado de itens**. Alguns cards dessa tela aparecem com título em inglês.

### 1. Configurações gerais

No primeiro card:
- **Minutos para expirar** — tempo (em minutos) que um anúncio fica no mercado antes de expirar. Padrão: 60. A expiração depende da tarefa agendada (veja o passo 8).
- **Offers limit** — limite de ofertas.
- **Max item per seller** — quantos anúncios ativos cada jogador pode ter ao mesmo tempo.

### 2. Histórico de preços

No card **Histórico de preços**:
- **Exibir histórico de preços** — liga a sugestão de preço na venda, o gráfico na página do item e a página de consulta de preços.
- **Janela do histórico (dias)** — quantos dias de vendas entram no cálculo. Padrão: 30.

### 3. Formas de pagamento

No card **Payments**, ligue **Carteiras** e/ou **Zen** e marque as **Moedas** aceitas. Para aceitar **itens como pagamento** (ex.: jóias), selecione-os no card **Items for Payments** — o comprador paga entregando a quantidade informada daquele item.

### 4. Taxas

No card **Taxes**, defina para cada carteira a **porcentagem** descontada do vendedor em vendas pagas com aquela carteira. É a receita do mercado.

### 5. Preços mínimos

No card **Preços mínimos**, defina, para cada forma de pagamento (cada moeda, cada carteira, zen e cada item usado como pagamento), o **menor preço** que um jogador pode pedir ao anunciar. Serve para evitar anúncios de R$ 0,01 ou de 1 moeda que poluem o mercado ou servem para transferir itens "de graça". Deixe em branco para não exigir mínimo.

### 6. Atributos permitidos

No card **Allowed options**, ligue ou desligue a venda de itens com **excellent**, **opções**, **ancient**, **luck**, **harmony**, **refine** e **socket**.

### 7. Itens bloqueados

No card **Ítens bloqueados**, selecione os itens que **não podem** ser anunciados (ex.: itens de evento ou exclusivos). Clique em **Salvar** ao final da tela.

### 8. Ativar a tarefa de expiração (pré-requisito para expirar)

Os anúncios só expiram se a tarefa agendada rodar. Vá em **Configurações → Tarefas**, clique em **Adicionar**, escolha no campo **Script** a tarefa **remove-expired-items** do grupo **Item market**, defina a frequência (por exemplo, a cada 5 minutos), marque **Ativo** e salve.

### 9. Acompanhar pedidos e estatísticas

- No menu lateral, **Mercado → Itens** abre a tela **Pedidos**: todos os anúncios com item, **Vendedor**, **Comprador**, **Preço**, **Pagamento**, **Anunciado em**, **Vendido em** e **Status**, com filtros por **ID**, **Status**, **Vendedor** e **Comprador**. Os botões **Estatísticas** e **Configurações** ficam no topo dessa lista.
- Em **Estatísticas** você vê o **Total de anúncios**, quantos estão **À venda**, **Vendidos** e **Expirado**, além da tabela **Anúncios por status**.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|------------------------|-----------------|
| Tempo de expiração, limite de ofertas e máximo por vendedor | **Configurações → Mercado de itens**, primeiro card |
| Ligar sugestão de preço, gráfico e consulta de preços | **Configurações → Mercado de itens → Histórico de preços** |
| Permitir moedas, carteiras e zen | **Configurações → Mercado de itens → Payments** |
| Aceitar itens como pagamento | **Configurações → Mercado de itens → Items for Payments** |
| Cobrar taxa por venda (carteiras) | **Configurações → Mercado de itens → Taxes** |
| Exigir preço mínimo por forma de pagamento | **Configurações → Mercado de itens → Preços mínimos** |
| Liberar/bloquear atributos | **Configurações → Mercado de itens → Allowed options** |
| Bloquear itens específicos | **Configurações → Mercado de itens → Ítens bloqueados** |
| Fazer os anúncios expirarem | **Configurações → Tarefas** (tarefa **remove-expired-items**) |
| Ver todos os anúncios e vendas | **Mercado → Itens** (tela **Pedidos**) |
| Acompanhar desempenho | Botão **Estatísticas** no topo de **Pedidos** ou das configurações |

---

## Dicas e boas práticas

- Comece com **poucas moedas** aceitas e vá liberando conforme entender o fluxo do mercado.
- Use os **Ítens bloqueados** para impedir a venda de itens exclusivos ou de evento.
- A **taxa** equilibra a economia (drena moeda) e gera receita — calibre para não desestimular as vendas.
- Ative a **tarefa de expiração** para evitar anúncios "fantasma" parados para sempre no mercado.
- Limite o **máximo de itens por vendedor** para evitar que poucos jogadores dominem o mercado.
- Ligue o **histórico de preços**: a sugestão de preço reduz anúncios fora da realidade e a consulta pública dá transparência ao mercado.

---

## Perguntas frequentes

**Por que a compra não foi concluída?**
A compra só acontece se **comprador e vendedor estiverem fora do jogo** e se houver espaço no baú do comprador. O jogador vê a mensagem correspondente e pode tentar de novo.

**O item comprado demora para chegar?**
Não. Quando a compra é aceita, o item entra no baú do comprador **na hora**.

**O que acontece quando um anúncio expira?**
Ele sai do mercado com o status **Expirado**. O dono recupera o item em **Meus ítens para venda**, com o botão **Remover**, que o devolve ao baú.

**Posso impedir a venda de certos itens?**
Sim. Use o card **Ítens bloqueados** nas configurações.

**Como o vendedor recebe o pagamento?**
O valor vai para o **saldo do vendedor** (moeda, carteira ou zen) ou, no pagamento com item, os itens vão para o baú dele. Em vendas por carteira, a **taxa** configurada é descontada.

**Posso aceitar mais de uma forma de pagamento?**
Sim. Você pode permitir várias **moedas**, **carteiras**, **zen** e **itens** simultaneamente; o vendedor escolhe uma delas ao anunciar.

**O que a sugestão de preço considera?**
As vendas concluídas de itens parecidos (mesmo item, nível e atributos principais) dentro da **janela do histórico**, com a mesma forma de pagamento. Ela só aparece quando há pelo menos três vendas comparáveis.
