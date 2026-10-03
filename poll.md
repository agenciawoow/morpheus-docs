# Enquetes (Poll) — Guia do Cliente

Este guia explica, de forma simples, o que são as Enquetes do seu servidor, como o jogador vota e como você configura tudo pelo painel administrativo. Não é necessário conhecimento técnico.

---

## O que são as Enquetes?

As Enquetes deixam você **fazer perguntas aos jogadores** e coletar a opinião deles — por exemplo: *"Qual será o próximo evento?"*, *"Qual mapa você prefere?"*, *"Gostou da última atualização?"*.

É uma ferramenta simples de **engajamento e relacionamento**:

- Dá voz à comunidade e mostra que você ouve os jogadores.
- Ajuda a tomar decisões (eventos, balanceamento, novidades) com base no que a maioria quer.
- Pode até **recompensar quem participa**, incentivando o jogador a voltar ao site.

A enquete ativa mais recente aparece automaticamente na **barra lateral** do site, pronta para receber votos. Você também pode inserir uma enquete específica em qualquer página criada no construtor de páginas.

---

## Conceitos principais

### A enquete

É a pergunta em si. Tem um **Título**, uma **Descrição** opcional (para dar contexto), uma data em que **Começa em** (obrigatória) e, se quiser, uma em que **Termina em**. Quando você marca a enquete como **Ativo** e ela está dentro do período, ela aparece no site.

### As respostas

São as **opções de voto** (ex.: *"Sim"*, *"Não"*, *"Tanto faz"*). Você as cadastra no próprio formulário da enquete e, depois, pode gerenciá-las numa tela separada, com **reordenação** arrastando.

### Opções de votação

- **Liberar multiplos votos** — o jogador pode marcar **mais de uma** resposta (caixas de seleção) em vez de só uma.
- **Apenas logados** — só quem está logado pode votar.
- **IPs liberados** — permite votar **repetidamente** do mesmo computador (útil em enquetes informais). Desligado, cada pessoa vota uma vez.

### Visibilidade do resultado

Você controla **quando** o jogador pode ver o gráfico de resultados:

- **Sempre visível** — qualquer um vê o resultado a qualquer momento.
- **Após votar** — o resultado só aparece depois que a pessoa vota (o clássico "vote para ver").
- **Após o término da enquete** — o resultado fica em segredo até a enquete encerrar (cria suspense).

### Recompensa por votar (opcional)

Você pode **dar uma moeda** ao jogador quando ele vota. A recompensa é entregue **uma única vez por conta** (na primeira vez que aquela conta vota naquela enquete) e só vale para jogadores logados. Ótimo para aumentar a participação.

---

## Como o jogador usa

- A enquete ativa aparece na barra lateral do site com o título, a descrição e as opções.
- O jogador escolhe a(s) resposta(s) e clica em **Votar**. O botão **Resultado** mostra o gráfico, respeitando a visibilidade configurada.
- Se houver **recompensa**, a moeda é creditada automaticamente na primeira votação.
- Enquetes antigas ficam na página **Histórico de enquetes**, com os resultados de cada uma.

---

## Como configurar (passo a passo)

Tudo é feito no menu lateral **Enquetes**.

### 1. Criar a enquete

1. Vá em **Enquetes** e clique em **Adicionar**.
2. Preencha o **Título** e (opcional) a **Descrição** — nos idiomas que desejar — e marque **Ativo**.
3. Defina **Começa em** (obrigatório) e, se quiser, **Termina em**.
4. Ajuste as opções: **Liberar multiplos votos**, **IPs liberados**, **Apenas logados**.
5. Escolha a **Visibilidade do resultado** (**Sempre visível**, **Após votar** ou **Após o término da enquete**).
6. (Opcional) Escolha a **Moeda da recompensa** e a **Quantidade da recompensa**.
7. Em **Respostas**, preencha cada opção de voto; clique em **Adicionar** para incluir mais linhas.
8. Clique em **Salvar**.

### 2. Gerenciar as respostas

Na lista de enquetes, o botão **Respostas** abre a tela com as opções daquela enquete e os **Votos** de cada uma. Ali você pode **Adicionar**, editar, excluir e **reordenar** arrastando.

### 3. Inserir a enquete em uma página

No construtor de páginas (plugin **Pages**), adicione o bloco **Poll** e escolha a enquete. Ela passa a aparecer naquela página, além da barra lateral.

### 4. Acompanhar os resultados

Em **Estatísticas** (botão no topo da lista de enquetes) você vê o **Total de votos**, as **Enquetes ativas** (sobre o total) e a tabela **Votos por enquete**, com o número de respostas e de votos de cada uma.

### 5. Encerrar

Para encerrar uma enquete, defina **Termina em** com uma data no passado ou desmarque **Ativo**. Enquetes encerradas continuam visíveis no **Histórico de enquetes** do site.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|------------------------|-----------------|
| Criar/editar enquetes | **Enquetes → Adicionar / Editar** |
| Definir o período | Campos **Começa em** e **Termina em** |
| Definir as regras de voto | Campos **Liberar multiplos votos / IPs liberados / Apenas logados** |
| Controlar quando o resultado aparece | Campo **Visibilidade do resultado** |
| Premiar quem vota | Campos **Moeda da recompensa** e **Quantidade da recompensa** |
| Cadastrar as opções de voto | Seção **Respostas** do formulário da enquete |
| Reordenar ou editar as opções | Botão **Respostas** na lista de enquetes |
| Exibir em uma página do construtor | Bloco **Poll** no plugin **Pages** |
| Ver desempenho | Botão **Estatísticas** no topo da lista de enquetes |
| Excluir uma enquete | Botão de excluir na lista de enquetes |

---

## Dicas e boas práticas

- **Perguntas curtas e claras** geram mais participação.
- Use **escolha única** para decisões objetivas e **múltiplos votos** para "marque tudo que se aplica".
- A visibilidade **Após o término da enquete** cria expectativa em votações importantes.
- Uma **recompensa pequena** por votar aumenta bastante a participação — sem exagerar.
- Mantenha **uma enquete ativa por vez** para não dividir a atenção; a barra lateral mostra só a mais recente, e as antigas ficam no histórico.
- Revise o período: uma enquete só aparece enquanto está **ativa e dentro das datas**.

---

## Perguntas frequentes

**Onde a enquete aparece para o jogador?**
Na barra lateral do site, automaticamente, enquanto estiver ativa e dentro do período — e em qualquer página do construtor onde você inserir o bloco **Poll**.

**O jogador pode votar mais de uma vez?**
Por padrão, não — cada pessoa vota uma vez. Se você ligar **IPs liberados**, o mesmo computador pode votar repetidamente.

**Dá para escolher mais de uma resposta?**
Sim, se você ligar **Liberar multiplos votos**. Caso contrário, é escolha única.

**Posso esconder os resultados até a enquete acabar?**
Sim. Use a visibilidade **Após o término da enquete**. Também há a opção **Após votar** (mostra só depois que a pessoa vota).

**A recompensa é dada toda vez que o jogador vota?**
Não. É entregue **uma única vez por conta**, na primeira votação naquela enquete, e apenas para jogadores logados.

**O que acontece com as enquetes antigas?**
Ficam disponíveis na página **Histórico de enquetes** do site, com os resultados de cada uma.

**Como encerro uma enquete?**
Defina **Termina em** com uma data no passado ou desmarque **Ativo**.

**Excluir uma enquete apaga os votos?**
Sim. Ao excluir, as respostas e os votos daquela enquete são removidos junto.
