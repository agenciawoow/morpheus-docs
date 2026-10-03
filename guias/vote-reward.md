# Recompensa por Voto — Guia do Cliente

No painel este recurso aparece como **Vote Reward**. Este guia explica, de forma simples, o que é a Recompensa por Voto, como o jogador participa e como você configura pelo painel administrativo. Não é necessário conhecimento técnico.

---

## O que é a Recompensa por Voto?

A Recompensa por Voto deixa o jogador **votar no seu servidor** em sites de ranking (GTop100, TopG, XtremeTop100 e outros) e ganhar **moedas** do site em troca. Quanto mais votos, melhor a posição do servidor nesses rankings e mais visibilidade para atrair novos jogadores.

É uma ferramenta de **divulgação e engajamento**: você troca uma pequena recompensa por votos que promovem o servidor nos grandes sites de listagem.

---

## Conceitos principais

### O provedor (site de voto)

Cada **provedor** é um site de ranking onde o jogador vota. Ele tem um **Nome**, a **URL** da página de voto, uma **Imagem**, a **Moeda** e a **Quantidade** de recompensa por voto, um **Delay em horas** (tempo até o jogador poder votar de novo naquele site) e, opcionalmente, uma **API** de confirmação automática com um **Segredo do pingback**.

### O voto

Quando o jogador clica para votar, é registrado um voto **Pendente**. Quando o site de ranking avisa que o voto foi válido, o voto vira **Concluído** e a recompensa é creditada na conta do jogador. Cada voto só é premiado **uma única vez**, mesmo que o site envie a confirmação mais de uma vez.

### Confirmação automática

Três sites têm confirmação automática: **GTop100**, **TopG** e **XTremeTop100**. Para eles, o painel mostra na lista de provedores a coluna **Pingback/Postback** com o endereço que você precisa cadastrar no site de ranking. Para qualquer outro site, o jogador até é levado à página de voto, mas não há como confirmar o voto e creditar a recompensa automaticamente.

### Intervalo entre votos

O **Delay em horas** define de quanto em quanto tempo o jogador pode votar novamente no mesmo provedor (o mais comum é 12 ou 24 horas). Se o jogador tentar antes, o site avisa que ele só pode votar a cada X horas.

---

## Como o jogador usa

1. Logado no site, o jogador abre a página de votação (endereço `/vote`) e vê os provedores ativos, cada um com sua imagem e a recompensa em moedas.
2. Clica em **Votar** no provedor escolhido e é levado à página de voto do site de ranking.
3. Quando o site de ranking confirma o voto, a moeda é creditada na conta e o jogador recebe uma mensagem no painel dele avisando da recompensa.
4. Para votar de novo naquele provedor, precisa aguardar o **Delay em horas**.

---

## Como configurar (passo a passo)

Tudo fica em **Configurações → Vote Reward**, que abre a lista de **Provedores**.

### 1. Cadastrar um provedor

1. Em **Configurações → Vote Reward**, clique em **Adicionar**.
2. Informe o **Nome**, o **Delay em horas** e ligue o interruptor **Ativo**.
3. Em **URL**, cole o endereço da página de voto do site de ranking. Você pode usar a variável `${username}` para que o site de ranking receba a conta do jogador que clicou para votar (exemplo mostrado na própria dica do campo: `https://provedor.com/vote?id=123&pingUsername=${username}`). Isso é necessário para a confirmação automática identificar quem votou.
4. Em **Segredo do pingback**, defina uma senha qualquer. Cadastre no site de ranking o endereço de confirmação acrescentando `?key=<segredo>` ao final. Com o segredo configurado, só confirmações que trazem essa chave são aceitas.
5. Em **API**, escolha o site de ranking correspondente (**XtremeTop100.com**, **GTop100.com** ou **TopG.org**) para ligar a confirmação automática. Deixe em branco para sites sem confirmação.
6. Envie uma **Imagem** (logo do site), escolha a **Moeda** e a **Quantidade** de recompensa por voto e clique em **Salvar**.

### 2. Cadastrar o endereço de confirmação no site de ranking

1. De volta à lista de provedores, copie o endereço da coluna **Pingback/Postback** do provedor.
2. No painel do site de ranking, cadastre esse endereço como pingback/postback do seu servidor, acrescentando `?key=<segredo>` quando você definiu um **Segredo do pingback**.

### 3. Acompanhar

Clique em **Estatísticas**, no topo da lista, para ver **Provedores ativos**, **Total de votos**, **Concluídos**, **Pendente** e a tabela **Votos por provedor**.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|------------------------|-----------------|
| Ver e cadastrar provedores | **Configurações → Vote Reward** |
| Adicionar um site de voto | **Configurações → Vote Reward → Adicionar** |
| Alterar um site de voto | Botão de editar na linha do provedor |
| Endereço de voto do site de ranking | Campo **URL** (com `${username}` para identificar o jogador) |
| Senha da confirmação automática | Campo **Segredo do pingback** |
| Ligar a confirmação automática | Campo **API** |
| Definir a recompensa | Campos **Moeda** e **Quantidade** |
| Intervalo entre votos | Campo **Delay em horas** |
| Ativar ou desativar um provedor | Interruptor **Ativo** |
| Copiar o endereço de confirmação | Coluna **Pingback/Postback** na lista |
| Acompanhar os votos | Botão **Estatísticas** no topo da lista |

---

## Dicas e boas práticas

- Cadastre **vários sites de ranking**: quanto mais sites, mais votos e mais visibilidade.
- Sempre defina o **Segredo do pingback** nos provedores com confirmação automática. Sem segredo, a confirmação do GTop100 é aceita de qualquer origem, e o painel emite um aviso pedindo para configurar.
- Use `${username}` na **URL** para que o site de ranking devolva a conta do jogador. Sem isso, a confirmação automática não consegue saber quem votou.
- Calibre a **Quantidade** de recompensa para incentivar o voto sem desequilibrar a economia.
- Acompanhe **Votos por provedor** nas estatísticas para saber quais rankings trazem mais retorno.

---

## Perguntas frequentes

**Como o jogador recebe a recompensa?**
Quando o site de ranking confirma o voto, a moeda é creditada na conta e o jogador recebe uma mensagem no painel dele.

**Por que um voto fica "Pendente"?**
O jogador clicou para votar, mas o site de ranking ainda não confirmou. Isso acontece se o voto não foi concluído lá, se o provedor não tem **API** configurada ou se o endereço de confirmação não foi cadastrado no site de ranking.

**Quais sites confirmam o voto automaticamente?**
GTop100, TopG e XTremeTop100. Para os demais, não há confirmação automática.

**O jogador pode ser premiado duas vezes pelo mesmo voto?**
Não. Cada voto é creditado uma única vez, mesmo que o site de ranking envie a confirmação repetida.

**De quanto em quanto tempo o jogador pode votar?**
Conforme o **Delay em horas** de cada provedor. Deixando zero, não há espera.

**Posso ter quantos provedores quiser?**
Sim. Cada provedor é independente, com sua própria recompensa, intervalo e segredo.
