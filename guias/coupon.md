# Cupons (Coupon) — Guia do Cliente

Este guia explica, de forma simples, **o que são** os Cupons, **como o jogador usa** e **como você configura** tudo pelo painel administrativo. Não é necessário conhecimento técnico.

---

## O que são os Cupons?

Os Cupons são **códigos de desconto** que o jogador aplica na hora de pagar — na **Loja (WebShop)**, no **mercado**, na **doação** e em outros lugares do site que aceitem cupom. Em vez de pagar o valor cheio, ele digita o código e ganha um **abatimento**.

É uma ferramenta de **marketing e fidelização**: serve para promoções ("BLACKFRIDAY"), para recompensar influenciadores/parceiros (cada um com o seu código) e para incentivar a primeira compra de novos jogadores.

---

## Conceitos principais

### O código

Cada cupom tem um **código** único (ex.: `BEMVINDO`, `NATAL2025`) que o jogador digita na compra. Maiúsculas/minúsculas não importam.

### Onde o cupom vale (Escopo)

O **Escopo** define **em qual área** do site o cupom funciona — por exemplo, só na **Loja**, só no **mercado** ou só na **doação**. Deixando o escopo **em branco**, o cupom vale em **todas** as áreas que aceitam cupom.

> As áreas disponíveis aparecem na lista de escopo conforme os recursos instalados no seu site (Loja, mercado, doação etc.).

### Tipo de desconto

- **Percentual:** abate uma **porcentagem** do valor (ex.: 10%). Você pode definir um **Desconto máximo** para limitar o valor abatido em pedidos grandes (ex.: "10%, no máximo R$ 20").
- **Valor fixo:** abate uma **quantia fixa** (ex.: 50 créditos), independentemente do tamanho do pedido. O desconto nunca passa do valor do próprio pedido.

### Cashback (opcional)

Além do desconto, o cupom pode devolver uma **porcentagem do valor** de volta para o jogador, como **saldo em uma carteira** que você escolhe (ex.: "5% de volta em Créditos"). É um incentivo a mais para usar o cupom e continuar comprando.

### Limites e regras

- **Pedido mínimo:** o cupom só funciona se a compra atingir um valor mínimo.
- **Usos por conta:** quantas vezes **cada jogador** pode usar aquele cupom.
- **Quantidade:** total de usos do cupom **somando todos os jogadores** (estoque do cupom).
- **Somente primeira compra:** o cupom só vale para quem **ainda não comprou** — ideal para atrair novos jogadores.
- **Começa em / Termina em:** janela de validade do cupom (a data de início é obrigatória; a de término é opcional).
- **Ativo:** liga/desliga o cupom sem precisar excluí-lo.

### Dono (cupons de parceiro/influenciador)

O campo **Dono** vincula o cupom a uma **conta**. Útil para dar um código a cada streamer/parceiro. O **dono não pode usar o próprio cupom**, e os cupons que pertencem a um jogador aparecem para ele na área **Meus cupons** da conta.

---

## A experiência do jogador

1. Durante uma compra (Loja, mercado, doação…), o jogador digita o **código do cupom**.
2. O site valida: se está ativo, dentro da validade, dentro do escopo, se atinge o pedido mínimo e se ele ainda tem usos disponíveis.
3. Sendo válido, o **desconto é aplicado na hora** e o jogador vê o valor já abatido.
4. Se houver **cashback**, o valor combinado volta como saldo na carteira escolhida.
5. Códigos vinculados ao jogador (quando ele é o **dono**) ficam visíveis em **Meus cupons**, na conta dele.

---

## Como configurar (passo a passo)

Tudo é feito no menu **Cupons** do painel administrativo.

### 1. Criar o cupom

1. Vá em **Cupons** e clique em **Adicionar**.
2. Defina o **código** (ex.: `BEMVINDO`).
3. Escolha o **Escopo** (área onde vale) — ou deixe em branco para valer em todas.
4. Escolha o **Tipo de desconto** (Percentual ou Valor fixo) e informe o **Desconto**.
   - No percentual, opcionalmente defina o **Desconto máximo**.
5. Ajuste as **regras**: pedido mínimo, usos por conta, quantidade total, somente primeira compra.
6. Defina **Começa em** e (opcional) **Termina em**.
7. Se quiser, configure **Cashback** (%) + a **Carteira** que receberá o valor.
8. Se for um cupom de parceiro, informe o **Dono**.
9. Marque como **Ativo** e salve.

### 2. Acompanhar o uso

Na lista de **Cupons** você vê o desconto, a validade e quantas vezes cada cupom já foi **usado**.

### 3. Ver as estatísticas

Em **Estatísticas** (botão no topo da lista) você acompanha o **total de usos**, **cupons ativos**, o **valor processado** (quanto de compra passou por cupons), o **cashback pago** e o ranking dos **cupons mais usados**.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|------------------------|-----------------|
| Criar/editar cupons | **Cupons → Adicionar / Editar** |
| Limitar a área de uso | Campo **Escopo** |
| Definir desconto % ou fixo | Campos **Tipo de desconto** e **Desconto** |
| Limitar o desconto em pedidos grandes | Campo **Desconto máximo** (percentual) |
| Exigir valor mínimo de compra | Campo **Pedido mínimo** |
| Limitar usos por jogador / no total | Campos **Usos por conta** e **Quantidade** |
| Atrair novos jogadores | **Somente primeira compra** |
| Devolver parte do valor | **Cashback** + **Carteira** |
| Dar código a um parceiro | Campo **Dono** |
| Definir validade | **Começa em** / **Termina em** |
| Acompanhar desempenho | **Cupons → Estatísticas** |
| Excluir um cupom | Botão de excluir na lista |

---

## Dicas e boas práticas

- Use **códigos curtos e memoráveis** (`NATAL`, `VIP10`) — são mais fáceis de divulgar.
- Para campanhas grandes, combine **Quantidade** (estoque total) com **Usos por conta** para evitar abuso.
- **Somente primeira compra** é ótimo para converter jogadores novos sem dar desconto a quem já compra.
- No desconto **percentual**, sempre considere um **Desconto máximo** para proteger a margem em pedidos altos.
- Cupons de **parceiro** (com Dono) facilitam medir o resultado de cada streamer/divulgador.
- Mantenha cupons antigos **desativados** em vez de excluir — o histórico de uso continua nas estatísticas.

---

## Perguntas frequentes

**O jogador pode usar o mesmo cupom várias vezes?**
Depende do que você configurar em **Usos por conta**. Sem limite definido, ele segue valendo enquanto houver **Quantidade** (estoque total) e a validade não expirar.

**Posso restringir o cupom só para a Loja?**
Sim. Basta escolher o **Escopo** correspondente. Em branco, o cupom vale em todas as áreas que aceitam cupom.

**Como funciona o cashback?**
Além do desconto na compra, uma porcentagem do valor volta como **saldo** para o jogador, na **carteira** que você escolher.

**Por que o dono não consegue usar o próprio cupom?**
Cupons com **Dono** são feitos para o parceiro **divulgar**, não para ele mesmo se beneficiar — por isso o sistema bloqueia o uso pelo próprio dono.

**O desconto pode ficar maior que o valor da compra?**
Não. O abatimento nunca passa do valor do pedido.

**Posso pausar um cupom sem perder o histórico?**
Sim. Basta desmarcar **Ativo**. Ele para de funcionar, mas continua na lista e nas estatísticas.
