# Leilão — Guia do Cliente

Este guia explica, de forma simples, **o que é** o Leilão, **como o jogador participa** e **como você configura** tudo pelo painel administrativo. Não é necessário conhecimento técnico.

---

## O que é o Leilão?

O Leilão deixa o jogador **dar lances** (com o saldo de uma moeda do site) para **arrematar itens do jogo**. Quem estiver com o **maior lance** quando o item encerra leva o item para o baú.

É uma ferramenta de **economia e disputa**: gera competição entre os jogadores por itens raros, drena moedas da economia e cria expectativa em torno das peças mais cobiçadas.

---

## Conceitos principais

### O leilão

É o **evento** que agrupa um conjunto de itens. Tem um **Nome** (traduzível), uma **Descrição** opcional (traduzível), uma **Imagem** de capa, um período (**Data de início** e **Data de término**) e o interruptor **Ativo**. Enquanto estiver ativo, dentro do período e com pelo menos um item ainda sem ganhador, aparece para os jogadores.

### Os itens do leilão

Cada leilão contém **itens do jogo** colocados para arremate. Cada item tem:
- a **Moeda** usada nos lances (ex.: WCoin);
- a **Aposta inicial** (o valor mínimo do primeiro lance);
- o interruptor **Ativo** (só itens ativos aparecem para os jogadores);
- o item em si, montado no cadastro com nível, opções e uma **prévia visual**.

### Como o lance funciona

O jogador oferece um valor **maior que o melhor lance atual** (ou, se ninguém deu lance ainda, no mínimo a Aposta inicial). O valor é **descontado na hora** do saldo dele. Se outra pessoa cobrir o lance depois, o valor **volta** para quem foi superado. Ou seja, só fica reservado o saldo de quem está ganhando no momento.

### O encerramento e a entrega

Cada lance reinicia um contador. Quando passa o **Tempo para entrega do item** (configurado no painel, em segundos) sem nenhum lance novo, o item encerra e o **maior licitante vira o ganhador**. O item cai no **baú** do ganhador assim que ele estiver **fora do jogo**, e ele recebe uma mensagem no site avisando do arremate. Enquanto o ganhador estiver online, a entrega fica pendente.

---

## Como o jogador usa

1. O jogador, logado no site, acessa **Leilões** e vê os leilões abertos (com capa, descrição e período).
2. Clica em **Entrar** e vê os **itens disponíveis**, cada um com **Aposta inicial**, **Melhor lance**, quem está ganhando e o contador de tempo.
3. Clica em **Dar lance** e informa o valor. O valor é descontado na hora.
4. Se for superado, **recebe o valor de volta** e pode dar um lance maior.
5. Quando o contador zera sem lances novos, quem tiver o maior lance **ganha o item**, entregue no baú assim que ele sair do jogo.

---

## Como configurar (passo a passo)

Os leilões ficam no menu lateral, item **Leilão**. O comportamento geral fica em **Configurações → Leilão**.

### 1. Ajustar o tempo de encerramento

1. Vá em **Configurações → Leilão** (ou use o botão **Configurações** no topo da lista de leilões).
2. No card **Tempo**, preencha **Tempo para entrega do item**: quantos segundos sem lance novo até o item encerrar e ser entregue.
3. Clique em **Salvar**.

### 2. Criar o leilão

1. No menu lateral, abra **Leilão** e clique em **Adicionar**.
2. Preencha o **Nome** (nos idiomas que desejar) e ligue **Ativo**.
3. Preencha a **Descrição** (opcional, traduzível) e envie uma **Imagem** de capa, se quiser.
4. Defina **Data de início** e **Data de término** (apenas a data, sem horário). Em branco, não limita.
5. Clique em **Salvar**. Ao editar, aparece também o campo **URL**, gerado a partir do nome.

### 3. Adicionar itens ao leilão

1. Na lista de leilões, clique no ícone de itens do leilão (ou, na edição, no botão **Itens**).
2. Clique em **Adicionar**.
3. No card **Item**, escolha a **Moeda**, informe a **Aposta inicial** e deixe **Ativo** ligado.
4. Pesquise e monte o item do jogo (nível, opções etc.). A **prévia visual** mostra como ele ficará.
5. Clique em **Salvar**. Repita para cada item do evento. Ao editar, o item em si não muda, apenas moeda, aposta inicial, opções e o interruptor Ativo.

### 4. Acompanhar e entregar

A lista de itens do leilão mostra **Nome**, **Ganhador**, **Data que venceu** e **Entregue** (Sim/Não). Quando um item já tem ganhador, ele está fora do jogo e a entrega ainda não aconteceu, aparece o botão de **entrega manual** para concluir na hora.

Dois cuidados automáticos do sistema:
- um item com **lance em aberto não pode ser desativado**; a tela recusa e orienta a excluir o item ou aguardar o encerramento;
- **excluir** um item com lance em aberto **devolve o lance** ao jogador.

### 5. Ver as estatísticas

No botão **Estatísticas** no topo da lista você acompanha **Leilões ativos**, **Itens vendidos** (do total), **Entrega pendente** e **Total em lances**, além do card **Desempenho dos leilões** com **Itens** e **Itens vendidos** de cada leilão.

### 6. Liberar o serviço para os jogadores

O Leilão é um serviço do site. Confira em **Configurações → Serviços** que o serviço **Leilão** está liberado; caso contrário, a página não abre para os jogadores.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|------------------------|-----------------|
| Criar ou editar leilões | **Menu lateral → Leilão → Adicionar / Editar** |
| Definir período e capa | Campos **Data de início**, **Data de término** e **Imagem** |
| Ligar ou desligar um leilão | Interruptor **Ativo** do leilão |
| Adicionar itens ao leilão | Ícone de itens na lista (ou botão **Itens** na edição) → **Adicionar** |
| Definir moeda e lance mínimo | Campos **Moeda** e **Aposta inicial** do item |
| Esconder um item sem lance | Interruptor **Ativo** do item |
| Ajustar o tempo até o encerramento | **Configurações → Leilão** → **Tempo para entrega do item** |
| Entregar manualmente um item ganho | Botão de entrega na lista de itens (ganhador fora do jogo) |
| Acompanhar desempenho | Botão **Estatísticas** no topo da lista |
| Liberar o serviço aos jogadores | **Configurações → Serviços → Leilão** |

---

## Dicas e boas práticas

- Use **Apostas iniciais** coerentes com o valor do item: muito alto afasta participantes, muito baixo "queima" itens raros.
- Um **Tempo para entrega do item** curto deixa a disputa frenética; um tempo maior dá chance de resposta a quem foi superado. Teste e ajuste.
- Itens **realmente cobiçados** geram leilões mais movimentados; misture peças de alto e médio valor para manter o interesse.
- Capriche na **Imagem** e na **Descrição** do leilão para divulgar o evento.
- Acompanhe o card **Entrega pendente** nas estatísticas para garantir que os ganhadores recebam seus itens.
- Use **Data de início** e **Data de término** para criar eventos sazonais (fim de semana, datas comemorativas).

---

## Perguntas frequentes

**O que acontece com o valor quando alguém cobre meu lance?**
Ele é **devolvido** na hora. Só fica reservado o saldo de quem está ganhando o item naquele momento.

**Quando o item encerra?**
Quando passa o **Tempo para entrega do item** (definido em **Configurações → Leilão**) sem nenhum lance novo. O maior lance naquele momento vence.

**Por que meu item ganho ainda não chegou no baú?**
A entrega acontece quando o ganhador está **fora do jogo**. Basta sair do jogo que o item é entregue; você também pode concluir pelo botão de entrega na lista de itens.

**Posso desativar um item que já tem lance?**
Não. Enquanto houver lance em aberto, a tela recusa a desativação. Exclua o item (o lance é devolvido ao jogador) ou aguarde o encerramento.

**Posso ter vários leilões ao mesmo tempo?**
Sim. Cada leilão é independente, com seus próprios itens e período.

**O lance precisa ser sempre maior que o atual?**
Sim. O primeiro lance precisa ser pelo menos a **Aposta inicial**; os seguintes, maiores que o **Melhor lance** vigente.
