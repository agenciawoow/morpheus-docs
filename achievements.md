# Conquistas (Achievements) — Guia do Cliente

Este guia explica, de forma simples, **o que são** as Conquistas do seu servidor, **como o jogador usa** e **como você configura** tudo pelo painel administrativo. Não é necessário conhecimento técnico para a maior parte da configuração.

---

## O que são as Conquistas?

As Conquistas são **metas** que o jogador cumpre no jogo e no site para **ganhar recompensas**. Por exemplo: *"Alcance o nível 200"*, *"Faça 10 resets"*, *"Entre em uma guild"*.

É uma ferramenta de **engajamento e fidelização**:

- Dá objetivos claros para o jogador perseguir.
- Premia quem evolui e se dedica, com moedas, VIP, itens e mais.
- Cria progressão de longo prazo, com conquistas que **dependem de outras** (cadeias).
- Mostra prestígio: conquistas raras destacam os jogadores mais dedicados.

---

## Conceitos principais

Cada conquista tem três peças:

### 1. A conquista

É a meta em si. Tem um **nome** e uma **descrição** (em vários idiomas), um **ícone** opcional e pode **depender de outra conquista** — ou seja, só fica disponível depois que o jogador resgatar a conquista anterior. Isso permite criar **trilhas** (Iniciante → Veterano → Mestre).

### 2. Os requisitos

São as **condições** que o jogador precisa cumprir. Cada requisito tem um **progresso** (quanto o jogador já alcançou em relação ao objetivo) — por exemplo, *"180 / 200"* de nível, mostrado como uma barra para o jogador.

Uma conquista pode ter **vários requisitos**, e o jogador só pode resgatar quando **todos** chegam a 100%.

> A definição do requisito é uma **consulta técnica** ao banco do servidor (mede o progresso do jogador). É o ponto mais avançado da configuração — se você não tiver familiaridade, peça ajuda à equipe técnica do servidor. Para facilitar, o painel tem um botão **Testar** que mostra na hora o progresso retornado para uma conta de exemplo, evitando erros.

### 3. As recompensas

É o que o jogador recebe ao resgatar. Você escolhe o **tipo** de recompensa, sem precisar de nada técnico:

- **Moedas** — credita uma moeda do jogo (ex.: WCoin) na conta.
- **Carteira** — credita saldo em uma carteira do site.
- **VIP** — concede dias de um tipo de VIP.
- **Item** — entrega um item no armazém do personagem (com todos os atributos que você montar).
- **SQL personalizado** — um recurso **avançado** para casos especiais, executado ao resgatar (também com botão **Testar**).

Cada recompensa tem um **título** (o texto que aparece para o jogador, ex.: *"+500 WCoin"*).

---

## A experiência do jogador

Na página **Conquistas** do site, o jogador vê todos os cards com:

- O **ícone**, nome e descrição da conquista.
- O **progresso** de cada requisito em barras.
- As **recompensas** que vai receber.
- Quão **rara** é a conquista (quantos % dos jogadores já a desbloquearam).
- O **status**: *Incompleta*, *Disponível* (pronta para resgatar) ou *Resgatada*.

Quando uma conquista fica pronta, aparece o botão **Resgatar**. O jogador também vê um **aviso no menu** (um número vermelho) indicando quantas conquistas estão prontas para resgatar — incentivando o retorno ao site.

As conquistas resgatadas ainda aparecem **no perfil** do personagem, como uma vitrine de troféus com a data em que foram desbloqueadas.

---

## Como configurar (passo a passo)

Tudo é feito no menu **Conquistas** do painel administrativo.

### 1. Criar a conquista

1. Vá em **Conquistas** e clique em **Adicionar**.
2. Preencha **nome** e **descrição** (nos idiomas que desejar).
3. (Opcional) Escolha uma conquista em **Requerido** para criar uma trilha (essa conquista só ficará disponível depois daquela).
4. (Opcional) Envie um **ícone**.
5. Marque como **Ativa** e salve.

### 2. Definir os requisitos

1. Na conquista, abra **Requisitos** (atalho no topo da tela de edição).
2. Clique em **Adicionar**, dê um **título** (ex.: *"Nível 200"*) e defina a condição.
3. Use o botão **Testar**, informando uma conta de exemplo, para conferir o progresso retornado.
4. Salve. Repita para quantos requisitos quiser.

### 3. Definir as recompensas

1. Na conquista, abra **Recompensas**.
2. Clique em **Adicionar**, dê um **título** e escolha o **tipo** (Moedas, Carteira, VIP, Item ou SQL personalizado).
3. Preencha os campos do tipo escolhido (valor, dias de VIP, item, etc.).
4. Salve. Repita para quantas recompensas quiser.

### 4. Acompanhar resultados

No topo da lista de conquistas, em **Estatísticas**, você vê quantas contas existem, o total de resgates e a **taxa de conclusão/raridade** de cada conquista — útil para calibrar a dificuldade.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|------------------------|-----------------|
| Criar/editar conquistas | **Conquistas → Adicionar / Editar** |
| Criar uma trilha (dependência) | Campo **Requerido** na conquista |
| Definir o ícone | Campo **Ícone** na conquista |
| Definir condições | **Conquistas → (conquista) → Requisitos** |
| Testar uma condição | Botão **Testar** no requisito |
| Definir prêmios | **Conquistas → (conquista) → Recompensas** |
| Ver desempenho | **Conquistas → Estatísticas** |
| Ordenar a lista | Arrastar e soltar na listagem de conquistas |

---

## Dicas e boas práticas

- **Comece simples:** poucas conquistas bem pensadas valem mais que uma lista enorme.
- **Use trilhas** (dependências) para guiar o jogador do início ao fim do servidor.
- **Equilibre as recompensas** com a dificuldade — use as **Estatísticas** para ajustar.
- **Capriche nos ícones e títulos**: a página fica muito mais atraente.
- **Sempre teste** os requisitos antes de ativar, com o botão **Testar**.
- Conquistas **raras** (poucos % de jogadores) viram símbolo de status — reserve-as para feitos realmente difíceis.

---

## Perguntas frequentes

**O jogador resgata automaticamente?**
Não. Quando a conquista fica pronta, o jogador precisa clicar em **Resgatar**. Ele é avisado por um número no menu.

**Posso dar mais de uma recompensa na mesma conquista?**
Sim. Adicione quantas recompensas quiser; todas são entregues no resgate.

**O jogador pode resgatar a mesma conquista duas vezes?**
Não. Cada conquista é resgatada **uma única vez** por conta.

**Uma conquista pode exigir outra?**
Sim. Use o campo **Requerido**. Ela só ficará disponível depois que o jogador resgatar a anterior.

**E se a condição de um requisito estiver errada?**
Use o botão **Testar** antes de ativar. Ele mostra o progresso retornado para uma conta de exemplo, sem afetar nada (qualquer alteração de teste é desfeita automaticamente).

**Onde o jogador vê as conquistas que já conquistou?**
Na página de Conquistas (marcadas como *Resgatada*) e também na **vitrine do perfil** do personagem, com a data de cada uma.

**Preciso saber programar para usar?**
Para **recompensas**, não — basta escolher o tipo (Moedas, Carteira, VIP, Item). Para **requisitos** e para o tipo de recompensa **SQL personalizado**, é preciso conhecimento técnico; peça ajuda à equipe do servidor se necessário.
