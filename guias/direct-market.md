# Mercado Direto — Guia do Cliente

No painel, a lista de vendas fica em **Mercado → Direto** e o card de configuração em **Configurações → Mercado direto**. Este guia explica, de forma simples, o que é o Mercado Direto, como o jogador usa e como você configura e acompanha tudo pelo painel administrativo.

---

## O que é o Mercado Direto?

O Mercado Direto permite que **um jogador venda um item do seu baú para outro jogador**, com o pagamento feito pelo site. É uma venda **direcionada**: o vendedor escolhe o item, define um **preço** e indica **para qual personagem** está vendendo. O comprador paga, o item é entregue no baú dele, e o vendedor recebe o valor (menos a sua taxa) em uma **carteira** do site.

- Dá aos jogadores uma forma **segura** de negociar itens entre si, sem o golpe do "dropei e sumiu".
- Mantém o dinheiro **dentro do ecossistema** do servidor: o vendedor recebe em carteira do site, não em dinheiro de fora.
- Você pode ficar com uma **taxa** sobre cada venda.

A venda é **combinada entre as duas pessoas** fora do site: o vendedor precisa saber o nome do personagem comprador. Não é uma vitrine pública onde qualquer um compra.

---

## Conceitos principais

### A venda

É o anúncio direcionado: um **item** (retirado do baú do vendedor), um **preço**, o **personagem comprador** e a **taxa** aplicada. Enquanto a venda existe, o item fica guardado pelo sistema, fora do baú do vendedor, para não ser vendido duas vezes nem usado no jogo.

### As situações

Na página do jogador, cada venda mostra uma destas situações:

- **Aguardando** — criada pelo vendedor, esperando o comprador pagar.
- **Pagando** — o comprador iniciou o pagamento.
- **Pago** — o pagamento foi confirmado e o vendedor já foi creditado; o item aguarda entrega.
- **Entregue** — o item foi colocado no baú do comprador.
- **Cancelado** — a venda foi desfeita e o item voltou para o vendedor.
- **Estornado** — o pagamento foi estornado depois da venda concluída.

Na lista do painel administrativo, as mesmas situações aparecem, na ordem, como **Pendente**, **Aguardando**, **Payed**, **Entregue**, **Cancelado** e **Refunded**.

### A taxa

Um **percentual** que o servidor retém sobre o valor da venda. Numa venda de 100 com taxa de 10, o vendedor recebe 90. Deixe em 0 para não cobrar nada.

### O preço mínimo

Valor mínimo que o vendedor é obrigado a pedir, para evitar vendas de valor simbólico. Deixe em 0 para não limitar.

### A carteira de recebimento

A **carteira do site** onde o vendedor recebe o valor da venda. É você quem escolhe qual carteira.

### As formas de pagamento

Os meios pelos quais o **comprador** paga, entre as formas de pagamento já configuradas no site. Você escolhe quais ficam disponíveis no Mercado Direto.

### O prazo de cancelamento

Quando o comprador inicia um pagamento e não conclui, a venda fica parada em **Pagando**. Depois do **Prazo de cancelamento (minutos)** que você define (padrão 1440, ou seja, 24 horas), o vendedor pode cancelar e receber o item de volta.

---

## Como o jogador usa

### Vender um item

1. Na página **Mercado direto** do site, o vendedor clica em **Vender item** e escolhe um item do **baú**.
2. Preenche **Nome do personagem** (o comprador) e **Preço**. Se houver taxa, um aviso mostra a porcentagem cobrada.
3. Confirma com o **ID pessoal** (a senha de segurança da conta).
4. O item **sai do baú** e a venda aparece para o comprador como **Aguardando**.

Por segurança, o vendedor precisa estar **fora do jogo** para vender. O personagem comprador precisa existir e ninguém pode vender **para si mesmo**.

### Comprar um item

1. Em **Mercado direto**, na seção **Suas solicitações de compra**, o comprador vê os itens à venda para ele, com o nome do **Vendedor** e o **Preço**.
2. Clica em **Pagar** e escolhe a forma de pagamento em **Pagar com ...**. Enquanto o pagamento não termina, o botão vira **Continuar pagamento**.
3. Com o pagamento confirmado, o vendedor é creditado na hora e o item vai para o **baú** do comprador, desde que ele esteja **fora do jogo** e tenha espaço no baú.
4. Se o comprador estava no jogo ou com o baú cheio, a venda fica em **Pago** e aparece o botão **Pegar item** para ele receber quando quiser. O item **nunca se perde**.

### Cancelar

Na seção **Suas vendas**, o vendedor pode clicar em **Cancelar** e receber o item de volta no baú:

- Sempre que a venda ainda estiver **Aguardando** (ninguém pagou).
- Quando estiver em **Pagando** há mais tempo que o **Prazo de cancelamento**. Até lá, a tela mostra **Cancelável em Xh Ym**.

O cancelamento também exige estar **fora do jogo** e ter espaço no baú.

### Avisos automáticos

- O comprador vê um **aviso** no menu do site enquanto tiver itens à venda para ele esperando pagamento.
- Quando a venda é confirmada, o vendedor recebe a mensagem **Item vendido** no site, com o valor bruto e o valor líquido creditado na carteira.
- Quando o item é entregue, o comprador recebe a mensagem **Item recebido**.
- Se o plugin de envio de mensagens estiver ativo, essas confirmações também podem chegar por WhatsApp.

### Estorno

Se o pagamento de uma venda concluída for estornado pela forma de pagamento, o valor creditado ao vendedor é **revertido** da carteira dele, a venda passa para **Estornado** e ele recebe uma mensagem avisando. O item já entregue ao comprador **não** é recolhido automaticamente: o caso fica registrado no histórico da conta do vendedor para o seu suporte tratar.

---

## Como configurar (passo a passo)

### 1. Ajustar as regras

1. Vá em **Configurações → Mercado direto**.
2. No card **Configurações**, defina:
   - **Preço mínimo** — valor mínimo de uma venda (0 = sem mínimo).
   - **Carteira** — a carteira do site onde os vendedores recebem.
   - **Taxa** — comissão em porcentagem (0 = sem taxa).
   - **Prazo de cancelamento (minutos)** — tempo que um pagamento iniciado pode ficar parado antes de o vendedor poder cancelar (padrão 1440).
3. No card **Gateways**, marque as formas de pagamento disponíveis.
4. Clique em **Salvar**.

### 2. Acompanhar as vendas

1. Vá em **Mercado → Direto**. A tela **Pedidos** lista cada venda com #ID, **Conta** (o vendedor), **Conta de destino** (o personagem comprador), **Item**, **Preço**, **Criado em** e **Status**.
2. Use o campo de busca por conta ou abra os filtros: **ID**, **Conta**, **Status**, **Criado a partir de** e **Criado até**. É útil no suporte para entender em que etapa uma venda parou.
3. Em vendas pagas ou entregues, o botão **Recibo** abre o comprovante do pagamento do comprador.

No topo da lista há os botões **Estatísticas** e **Configurações**.

### 3. Ver as estatísticas

Em **Estatísticas** (botão no topo da lista) você vê **Total de pedidos**, quantos foram **Vendidos**, a **Receita** das vendas pagas e entregues e quantos foram cancelados, além da tabela **Pedidos por status** com quantidade e valor por situação.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|------------------------|-----------------|
| Definir o preço mínimo | **Configurações → Mercado direto**, campo **Preço mínimo** |
| Escolher onde o vendedor recebe | **Configurações → Mercado direto**, campo **Carteira** |
| Cobrar uma comissão | **Configurações → Mercado direto**, campo **Taxa** |
| Definir quando o vendedor pode cancelar um pagamento parado | **Configurações → Mercado direto**, campo **Prazo de cancelamento (minutos)** |
| Liberar formas de pagamento | **Configurações → Mercado direto**, card **Gateways** |
| Ver e filtrar as vendas | **Mercado → Direto** |
| Ver o comprovante de um pagamento | **Mercado → Direto**, botão **Recibo** |
| Ver o desempenho do mercado | **Mercado → Direto**, botão **Estatísticas** no topo |

---

## Dicas e boas práticas

- Uma **Taxa** moderada ajuda a controlar a inflação e gera receita sem afastar os vendedores.
- Defina um **Preço mínimo** se quiser evitar vendas de valor simbólico.
- Escolha em **Carteira** uma carteira que o jogador consiga usar no site, para o valor recebido ter utilidade real.
- Deixe claro para a comunidade que a venda é **combinada entre as duas pessoas**: o vendedor precisa do nome do personagem comprador.
- Oriente os jogadores a **sair do jogo** antes de vender, receber ou cancelar. É o passo que mais gera dúvida.
- Use a lista em **Mercado → Direto** no suporte: a situação mostra exatamente onde a negociação parou.

---

## Perguntas frequentes

**O comprador paga com dinheiro de verdade?**
Sim, pelas formas de pagamento que você habilitar. O **vendedor** recebe o valor, menos a taxa, na **carteira do site**, não em dinheiro externo.

**Posso vender para qualquer um?**
A venda é direcionada: o vendedor informa o **nome do personagem comprador**, que precisa existir. Não dá para vender para si mesmo.

**Por que preciso estar fora do jogo para vender, receber ou cancelar?**
Para garantir que o item não esteja em uso no jogo e no site ao mesmo tempo. É uma proteção contra duplicação.

**O que acontece com o item enquanto está à venda?**
Ele sai do baú do vendedor e fica reservado pelo sistema. Se a venda for cancelada, volta para o baú.

**Quando o item chega para o comprador?**
Assim que o pagamento é confirmado, se o comprador estiver fora do jogo e com espaço no baú. Caso contrário, a venda fica em **Pago** e ele usa o botão **Pegar item** quando estiver pronto.

**E se o comprador nunca pagar?**
O vendedor pode cancelar e receber o item de volta: na hora, se a venda ainda estiver **Aguardando**, ou depois do **Prazo de cancelamento** se um pagamento foi iniciado e não concluído.

**O que acontece em um estorno?**
O valor é revertido da carteira do vendedor e a venda passa para **Estornado**. O item já entregue não é recolhido automaticamente; o caso fica registrado para o seu suporte.

**Como acompanho uma venda que deu problema?**
Em **Mercado → Direto**, filtrando por **ID**, **Conta** ou **Status**, você vê em qual etapa a negociação está.
