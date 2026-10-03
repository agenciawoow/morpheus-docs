# Indicação de Amigos (Indication) — Guia do Cliente

Este guia explica, de forma simples, o que é o programa de Indicação, como o jogador participa e como você o configura pelo painel administrativo. Não é necessário conhecimento técnico.

---

## O que é a Indicação de Amigos?

A Indicação deixa o jogador **convidar amigos** para o servidor por um link exclusivo e ganhar **moedas** quando esses amigos cumprem as **metas** que você definiu (criar conta, atingir um nível, fazer uma doação, etc.). É o clássico "indique e ganhe".

É uma ferramenta de **crescimento orgânico**: transforma sua base atual em divulgadores, premiando quem traz jogadores novos.

---

## Conceitos principais

### O código e o link de indicação

Ao clicar em **Participar**, o jogador recebe um **código** próprio e um **link de indicação**. Quem criar conta por esse link fica vinculado a ele como "indicado".

### A meta

Cada **meta** define o que o amigo indicado precisa cumprir e **quanto** o jogador que indicou recebe. Tem um texto de **Meta** (a descrição que o jogador vê), a **Moeda** da recompensa e a **Quantidade** (a regra que calcula o valor creditado).

### A recompensa por indicação

Quando um amigo indicado cumpre uma meta, é registrada uma **recompensa** para quem indicou. Ela fica **pendente** até o jogador resgatar e, então, passa a **recompensada**.

### Pendente x Recompensada

- **Pendente:** o amigo atingiu a meta e a recompensa está **disponível para resgate**, mas o jogador ainda não a resgatou.
- **Recompensada:** o jogador clicou em **Resgatar** e as moedas já estão na conta dele.

---

## Como o jogador usa

1. Na área **Minha conta**, o jogador encontra o bloco **Programa de indicação** e clica em **Participar**.
2. A partir daí o bloco mostra o **Link para indicação** (com botão **Copiar**), o total de **Indicações**, quanto já foi **Ganho** e quanto está **Disponível para resgate** em cada moeda, além da lista de metas com o status de cada uma (as já cumpridas ficam marcadas; as **Pendente** aguardam resgate).
3. Ele divulga o link; os amigos abrem o link, são levados ao cadastro e ficam vinculados a ele. Em **Visualizar** (página **Indicações**) ele vê os personagens dos amigos indicados.
4. Quando um amigo cumpre uma meta, a recompensa aparece como **Disponível para resgate**. O jogador clica em **Resgatar** e as moedas são creditadas na conta.

> O amigo precisa **criar a conta pelo link** do jogador para a indicação valer. Cada amigo conta **uma vez** por meta.

---

## Como configurar (passo a passo)

### 1. Abrir a tela de metas

O plugin **não tem item no menu lateral**. Para chegar à tela, vá em **Plugins**, localize o plugin **Indication** e clique no botão de configurar dele. Abre a tela **Metas de indicação**.

### 2. Criar uma meta

1. Em **Metas de indicação**, clique em **Adicionar**.
2. Preencha:
   - **Meta** — o texto descritivo que o jogador vê (ex.: "Amigo atingir o level 100").
   - **Moeda** — a moeda em que a recompensa é paga.
   - **Quantidade** — a regra que calcula quanto o jogador recebe quando o amigo cumpre a meta. Este campo é um **recurso avançado**: a condição e o valor saem de uma consulta ao banco do jogo. Peça ajuda a quem conhece o banco do seu servidor para montá-la.
3. Clique em **Salvar**. Os três campos são obrigatórios.

### 3. Ativar a tarefa agendada (pré-requisito)

As recompensas **não são geradas na hora**: uma **tarefa agendada** verifica periodicamente os amigos indicados, confere as metas e cria as recompensas pendentes. Sem ela, nada aparece para o jogador resgatar.

1. Vá em **Configurações → Tarefas** e clique em **Adicionar**.
2. Dê um **Nome**, marque **Ativo**, escolha no campo **Script** a tarefa **process-rewards** do grupo **Indication** e defina a frequência (por exemplo, a cada 10 minutos).
3. Salve.

### 4. Acompanhar

Em **Estatísticas** (botão no topo da lista de metas) você vê a quantidade de **Metas**, o **Total de indicações** registradas, quantas já foram **Recompensados** (resgatadas) e quantas estão **Pendente**.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|------------------------|-----------------|
| Abrir a tela do plugin | **Plugins → Indication** (botão de configurar) |
| Criar/editar/excluir metas | **Metas de indicação → Adicionar / Editar / Excluir** |
| Definir a moeda da recompensa | Campo **Moeda** da meta |
| Definir a regra do valor (avançado) | Campo **Quantidade** da meta |
| Gerar as recompensas automaticamente | **Configurações → Tarefas** (tarefa **process-rewards** do grupo **Indication**) |
| Acompanhar | Botão **Estatísticas** no topo da lista de metas |

---

## Dicas e boas práticas

- Crie metas com **dificuldade crescente** (criar conta → atingir nível → doar) e recompensas proporcionais.
- Recompensas **atrativas** incentivam a divulgação; calibre o valor para não desequilibrar a economia.
- Escreva o texto da **Meta** pensando no jogador — é o que aparece na lista dele.
- Não esqueça a **tarefa agendada**: sem ela as recompensas nunca ficam disponíveis.
- Divulgue o programa no site e nas redes — quanto mais visível, mais convites.

---

## Perguntas frequentes

**Quando o jogador ganha a recompensa?**
Quando um amigo que ele indicou **cumpre uma meta** e a tarefa agendada registra a recompensa. Depois disso ele precisa clicar em **Resgatar** para receber as moedas.

**O que significa "pendente"?**
A recompensa já foi liberada e está **disponível para resgate**; vira "recompensada" quando o jogador resgata.

**Por que o jogador não vê o link de indicação?**
Ele precisa clicar em **Participar** no bloco **Programa de indicação** da página **Minha conta**. Só então o código e o link são gerados.

**Posso ter várias metas?**
Sim. Cada meta tem sua própria condição e recompensa, e cada amigo indicado conta **uma vez** por meta.

**As recompensas aparecem na hora?**
Não. Elas dependem da **tarefa agendada**; o intervalo que você definir na tarefa é o tempo máximo de espera.
