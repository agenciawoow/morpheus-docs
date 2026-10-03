# Rifas (Raffle) — Guia do Cliente

Este guia explica, de forma simples, o que são as Rifas, como o jogador participa e como você configura tudo pelo painel administrativo. Não é necessário conhecimento técnico.

---

## O que são as Rifas?

As Rifas deixam o jogador **comprar números** (com o saldo de uma carteira do site) concorrendo a um **prêmio**. Quando o **último número** é vendido, o sistema **sorteia um vencedor** automaticamente.

É uma ferramenta de **engajamento e economia**: incentiva o jogador a gastar créditos, cria expectativa em torno do sorteio e dá um motivo a mais para voltar ao site.

---

## Conceitos principais

### A rifa

Tem um **Nome**, uma **Descrição** opcional, um **Total de números**, um **Preço** por número e a **Carteira** usada no pagamento (ex.: "Créditos").

### Os números

A rifa tem números de **1 até o total** que você definiu. Cada número só pode ser comprado **uma vez**; números fora da faixa ou repetidos são recusados. O jogador escolhe um ou mais números livres e paga **preço × quantidade**.

### O sorteio

Assim que **todos os números** são vendidos, o sistema sorteia um número **entre os vendidos** e o dono dele vira o **vencedor**. A rifa é encerrada e o ganhador, a data e o número ficam registrados.

### Tipo da rifa: Recompensa x Personalizado

O seletor **Tipo** tem duas opções:

- **Recompensa (automática):** ao sortear, o sistema **entrega tudo o que estiver preenchido no card Recompensas** ao vencedor — **VIP**, saldo em **carteiras**, **moedas** — e envia uma mensagem de parabéns com a lista do que ele ganhou.
- **Personalizado (manual):** nada é entregue automaticamente. O vencedor recebe a mensagem **Seu prêmio será entregue logo** e você faz a entrega por fora. O card **Recompensas** continua aparecendo, mas o que estiver preenchido nele **não é entregue** nesse tipo.

### Como o VIP é entregue

Se o vencedor já tem VIP, os dias são **somados** e ele fica com o VIP de maior nível entre o atual e o da rifa — nunca é rebaixado nem perde dias.

---

## Como o jogador usa

1. O jogador acessa **Rifas** no site e vê as rifas abertas, com **Preço** e **Total de números**; rifas encerradas mostram o **Número sorteado**.
2. Em **Visualizar**, vê o mapa de números com a legenda **Disponível**, **Selecionado**, **Meu** e **Vendido**, o progresso de vendas e, na lateral, as **Recompensas** e a **Descrição**.
3. Seleciona os números desejados, confere o **Total** e clica em **Comprar números**. O valor é descontado da carteira na hora.
4. Quando o último número é vendido, o **sorteio acontece na hora**. Quem comprou o último número já vê o aviso de que o prêmio foi sorteado; o vencedor recebe uma mensagem na conta.
5. No tipo **Recompensa**, os prêmios caem automaticamente na conta do vencedor.

---

## Como configurar (passo a passo)

Tudo é feito no menu lateral **Rifas**.

### 1. Criar a rifa

1. Vá em **Rifas** e clique em **Adicionar**.
2. No card **Rifa**: preencha o **Nome** e (opcional) a **Descrição** — nos idiomas que desejar — e marque **Ativo**.
3. Escolha o **Tipo** (**Recompensa** ou **Personalizado**), o **Total de números**, o **Preço** por número e a **Carteira** de pagamento.
4. No card **Recompensas** (usado no tipo **Recompensa**):
   - **Tipo de VIP** e **Dias de VIP**;
   - um campo para **cada carteira** do site (valor em saldo a creditar);
   - um campo para **cada moeda** do site (quantidade a creditar).
   Preencha só o que a rifa entrega.
5. O campo **Customizado** é um **recurso avançado**: permite executar comandos personalizados no banco do jogo para o vencedor (ex.: entregar um item). Só funciona no tipo **Recompensa**. Use com cuidado e com ajuda de quem conhece o banco do seu servidor; um comando errado pode causar problemas.
6. Clique em **Salvar**. Nome, tipo, total de números, preço e carteira são obrigatórios.

### 2. Acompanhar

Na lista de **Rifas** você vê o **Tipo**, o **Ganhador**, a **Data que venceu** e o **Número** sorteado de cada rifa, além do status.

### 3. Ver as estatísticas

Em **Estatísticas** (botão no topo da lista) você vê o **Total de rifas**, as **Rifas ativas**, as **Concluídas** e o total de **Números vendidos**, além da tabela com o progresso (**Vendido** / total) e o **Ganhador** de cada rifa.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|------------------------|-----------------|
| Criar/editar rifas | **Rifas → Adicionar / Editar** |
| Definir total de números e preço | Campos **Total de números** e **Preço** |
| Escolher a carteira de pagamento | Campo **Carteira** |
| Entregar o prêmio automaticamente | Tipo **Recompensa** + card **Recompensas** (VIP, carteiras, moedas) |
| Entregar o prêmio manualmente | Tipo **Personalizado** |
| Comandos personalizados (avançado) | Campo **Customizado** (só no tipo **Recompensa**) |
| Acompanhar desempenho | Botão **Estatísticas** no topo da lista |
| Excluir uma rifa | Botão de excluir na lista de rifas |

---

## Dicas e boas práticas

- Ajuste **preço × total de números** pensando no valor do prêmio — a soma das vendas deve fazer sentido com o que será entregue.
- Rifas com **menos números** sorteiam mais rápido; com **mais números**, duram mais e geram mais expectativa.
- Use o tipo **Recompensa** para entrega instantânea e sem trabalho manual; use **Personalizado** quando o prêmio é algo físico ou fora do site.
- Mantenha boas **Descrições** explicando o prêmio — ajuda a vender os números.
- Evite o campo **Customizado** a menos que precise mesmo; teste em uma rifa pequena antes.

---

## Perguntas frequentes

**Quando o sorteio acontece?**
Automaticamente, assim que o **último número** da rifa é vendido.

**O mesmo número pode ser comprado por duas pessoas?**
Não. Cada número é único; se alguém comprar primeiro, ele fica indisponível para os demais.

**O jogador pode comprar vários números?**
Sim. Ele seleciona quantos quiser (entre os livres) e paga o preço por cada um.

**Como o prêmio é entregue?**
No tipo **Recompensa**, automaticamente (VIP, moedas e carteiras caem na conta do vencedor). No tipo **Personalizado**, você entrega manualmente.

**Preenchi as Recompensas numa rifa Personalizado. Elas serão entregues?**
Não. No tipo **Personalizado** nada é entregue automaticamente; troque para **Recompensa** se quiser entrega automática.

**O que acontece com o valor pago?**
É descontado da carteira do jogador no momento da compra.

**Posso ver quem ganhou?**
Sim. O ganhador, a data e o número sorteado aparecem na lista de rifas e nas estatísticas; no site, a rifa encerrada mostra o número sorteado.
