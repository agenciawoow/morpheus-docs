# Tracker (bugs e sugestões) — Guia do Cliente

Este guia explica, de forma simples, o que é o Tracker, como o jogador acompanha e vota, e como você gerencia tudo pelo painel administrativo. Não é necessário conhecimento técnico.

---

## O que é o Tracker?

O Tracker é o **mural público de bugs e sugestões** do seu servidor. Cada item (chamado de **tracker**) tem uma categoria, uma versão do jogo e uma situação. Os jogadores **votam** nos itens que acham importantes e acompanham o andamento, e a equipe organiza tudo por **categoria**, **versão** e **situação**, dando transparência sobre o que está sendo tratado.

É ótimo para **engajamento e transparência**: a comunidade vê que é ouvida, e os itens mais votados ajudam a priorizar o que corrigir ou implementar primeiro.

---

## Conceitos principais

### O tracker

É o item reportado. Tem **Título**, **Descrição**, **Como reproduzir**, **Frequência** (Sempre, As vezes ou Raro), **Sistema operacional** e pode ter **Imagens**. Pertence a uma **Categoria** e a uma **Versão** do jogo, e pode ser **Público** (aparece no mural do site) ou não.

### As categorias

Agrupam os trackers (por exemplo *Bug Report* e *Sugestão*, que já vêm criadas). Cada categoria tem **Nome** em vários idiomas, interruptor **Ativo** e interruptor **Público**. Cada categoria ativa vira um item no menu **Tracker** do painel, com um contador de itens abertos.

### As situações (por categoria)

São as etapas do fluxo de cada categoria (por exemplo *Aberto*, *Em análise*, *Resolvido*, *Não reproduzível*). Cada situação tem **Nome** em vários idiomas, uma **Cor** e o interruptor **Fechado**. Ao aplicar uma situação marcada como **Fechado**, o tracker é **encerrado**: sai da contagem de abertos e deixa de receber votos. As situações podem ser **reordenadas arrastando**.

### As versões

Representam as **versões do jogo** (por exemplo *1.0.0*, *1.1.0*). Cada tracker nasce ligado a uma versão, e você pode indicar em qual versão ele foi corrigido. A versão tem o interruptor **Disponível** e um **Changelog** em vários idiomas.

### Votos

Cada jogador logado pode dar **um voto** por tracker, positivo ou negativo. Trackers fechados não recebem mais votos.

### Comentários

A equipe comenta pelo painel, e os comentários aparecem na página do tracker no site, com o selo **Administração**.

---

## Como o jogador usa

1. Na página **Tracker** do site, o jogador vê os trackers públicos agrupados por **Versão** e pode filtrar por **categoria** na lateral.
2. Em cada item vê o número, o título, a data, a quantidade de votos positivos e negativos, a situação (com a cor definida por você) e, quando houver, **Fixado na versão**.
3. Logado, pode **votar** uma vez em cada tracker aberto.
4. Ao abrir um tracker, lê a descrição, as imagens, **Como reproduzir** e os **Comentários** da equipe.
5. Em **Meus trackers**, no painel da conta, acompanha os trackers abertos em nome dele, com categoria, data e situação.

---

## Como gerenciar (passo a passo)

Tudo é feito no menu **Conteúdo → Tracker** do painel.

### 1. Estruturar (uma vez)

1. Em **Conteúdo → Tracker → Categorias**, clique em **Adicionar**, preencha o **Nome** nos idiomas desejados e ligue **Ativo** e **Público**. Ao **editar** uma categoria aparece também o campo **URL**, que define o endereço da categoria no site.
2. Para cada categoria existe uma tela **Situações**, onde você cadastra as etapas com **Nome**, **Cor** e **Fechado**, e as ordena arrastando. As categorias que já vêm criadas trazem um conjunto inicial de situações.
3. Em **Conteúdo → Tracker → Versões**, clique em **Adicionar**, informe a **Versão**, ligue **Disponível** e, se quiser, escreva o **Changelog**.

### 2. Tratar os trackers

1. No menu **Tracker**, cada categoria ativa aparece com um **contador de itens abertos**. Clique nela para ver só os trackers daquela categoria.
2. A lista mostra número, **Conta**, **Título**, votos **Up** e **Down**, **Categoria**, **Versão**, **Criado em** e **Situação**. Não há filtros: use a busca pelo **Título**.
3. Clique em **Visualizar** na linha. A tela mostra a conta, a categoria, os votos e a descrição.
4. No card **Tracker**, escolha a **Situação** (obrigatória), a **Versão** em que foi corrigido (opcional) e se o item é **Público**. Se quiser responder ao jogador, escreva em **Comentário**. Clique em **Salvar**.
5. Os comentários já registrados aparecem abaixo do formulário, com autor e data.

### 3. Acompanhar as estatísticas

Clique em **Estatísticas**, no topo da lista de trackers. A tela mostra **Total de trackers**, **Abertos**, **Fechado** e **Votos** (positivos e negativos), além da tabela **Trackers por categoria** com os abertos e o total de cada categoria.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|------------------------|-----------------|
| Criar ou editar categorias | **Conteúdo → Tracker → Categorias** |
| Definir o endereço da categoria no site | **Conteúdo → Tracker → Categorias** → editar → campo **URL** |
| Cadastrar e ordenar as situações de uma categoria | Tela **Situações** da categoria (campos **Nome**, **Cor**, **Fechado**) |
| Cadastrar versões e changelog | **Conteúdo → Tracker → Versões** |
| Ver os trackers de uma categoria | **Conteúdo → Tracker → (nome da categoria)** |
| Mudar situação, versão corrigida ou visibilidade | **Conteúdo → Tracker → (categoria)** → **Visualizar** → card **Tracker** |
| Responder ao jogador | Mesma tela, campo **Comentário** |
| Ver desempenho | **Conteúdo → Tracker → (categoria)** → botão **Estatísticas** |
| Abrir a ficha da conta de quem reportou | Clique no nome da conta na lista ou na tela do tracker |

---

## Dicas e boas práticas

- Crie **poucas categorias e claras**. Facilita para o jogador entender e para você priorizar.
- Use **cores** intuitivas nas situações (verde para resolvido, vermelho para recusado) e marque corretamente as de **Fechado**.
- Acompanhe os **mais votados** para priorizar o que tem maior impacto na comunidade.
- Informe a **Versão** de correção ao resolver. Isso aparece no site como **Fixado na versão** e reduz reports repetidos.
- Mantenha as **Versões** atualizadas e com **Disponível** ligado para o jogador saber em qual versão está.
- Responda com um **Comentário** ao mudar a situação. O jogador vê a resposta com o selo **Administração**.

---

## Perguntas frequentes

**O jogador pode votar mais de uma vez no mesmo tracker?**
Não. Cada conta vota **uma única vez** por tracker, e trackers fechados não recebem votos.

**Quem define as situações?**
Você, por **categoria**. Cada categoria tem o próprio fluxo de situações.

**O que acontece quando aplico uma situação marcada como Fechado?**
O tracker é **encerrado**: sai da contagem de abertos do menu e das estatísticas e deixa de receber votos.

**Trackers não públicos aparecem para o jogador?**
Não. Apenas trackers com **Público** ligado aparecem no mural. Os demais ficam visíveis só pelo painel.

**Dá para indicar em qual versão o bug foi corrigido?**
Sim. Na tela do tracker, escolha a **Versão** no card **Tracker**. O site mostra **Fixado na versão**.

**Posso desativar uma categoria sem apagar os trackers?**
Sim. Desligue **Ativo** na categoria. Ela some do menu do painel e do filtro do site, e os trackers continuam guardados.
