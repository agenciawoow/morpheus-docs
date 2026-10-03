# Temporizador (Contagem Regressiva) — Guia do Cliente

No painel aparece como **Temporizadores**.

Este guia explica, de forma simples, **o que é** o Temporizador, **onde aparece** para o jogador e **como você o configura** pelo painel administrativo. Não é necessário conhecimento técnico.

---

## O que é o Temporizador?

O Temporizador exibe um **relógio decrescente** no site, apontando para uma **data e hora** futuras — a abertura do servidor, o início de um evento, uma manutenção programada, etc. Quando o tempo zera, você pode mostrar uma **mensagem** no lugar do relógio.

É uma ferramenta de **expectativa e hype**: cria contagem para o grande momento e mantém os jogadores atentos.

---

## Conceitos principais

### O temporizador

Tem um **Título**, uma **Data** alvo (data e hora), uma **Mensagem** opcional (exibida quando o tempo acaba) e o estado **Ativo**.

### Ativo / inativo

Apenas os temporizadores **ativos** aparecem no site. Os inativos ficam guardados sem exibir, sem precisar excluí-los.

### A vencer / encerrado

Um temporizador está **a vencer** enquanto a data alvo está no futuro, e **encerrado** depois que a data passa. Você acompanha esses números nas estatísticas.

---

## A experiência do jogador

1. O jogador acessa o site e vê, no cabeçalho (acima da logo do servidor), o **relógio** de cada temporizador ativo, com **Dias**, **Horas**, **Minutos** e **Segundos**.
2. O contador diminui em tempo real até a data alvo.
3. Quando zera, a **Mensagem** configurada aparece no lugar do relógio (se houver).

Todos os temporizadores ativos são exibidos **ao mesmo tempo**, um abaixo do outro. Por isso, mantenha ativo apenas o que faz sentido mostrar agora.

---

## Como configurar (passo a passo)

Tudo é feito em **Configurações → Temporizadores**.

### 1. Criar um temporizador

1. Vá em **Configurações → Temporizadores** e clique em **Adicionar**.
2. Preencha o **Título** e escolha a **Data** (data e hora alvo).
3. Ligue o interruptor **Ativo**.
4. (Opcional) Escreva a **Mensagem** exibida ao terminar.
5. Clique em **Salvar**.

A lista mostra o **Título**, a **Data** e o **Status** de cada temporizador, com busca por título e botões de editar e excluir.

### 2. Ver as estatísticas

O botão **Estatísticas** no topo da lista mostra o **Total de contagens**, quantas estão **Ativo**, quantas ainda estão **A vencer** e quantas já estão **Encerradas**.

### 3. Usar um temporizador em uma página (construtor de Páginas)

Se você usa o plugin de **Páginas**, o construtor de páginas oferece o bloco **Countdown**. Ao inseri-lo, basta escolher qual temporizador exibir naquele ponto da página. Só os temporizadores **ativos** aparecem na escolha e são exibidos ao jogador — se você desativar o temporizador depois, o bloco simplesmente deixa de aparecer.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|------------------------|-----------------|
| Criar/editar temporizadores | **Configurações → Temporizadores → Adicionar / Editar** |
| Definir a data alvo | Campo **Data** |
| Mensagem ao terminar | Campo **Mensagem** |
| Ativar/desativar | Interruptor **Ativo** |
| Acompanhar | **Configurações → Temporizadores** → botão **Estatísticas** no topo |
| Mostrar dentro de uma página personalizada | Construtor de Páginas → bloco **Countdown** |

---

## Dicas e boas práticas

- Use o temporizador para o **grande lançamento** (abertura do servidor) — é o uso mais impactante.
- Escreva uma **Mensagem** clara para o momento em que o tempo zera (ex.: "O servidor está no ar!").
- Mantenha apenas **um temporizador ativo** por vez no cabeçalho para não confundir o jogador — todos os ativos aparecem juntos.
- Desative temporizadores antigos em vez de excluir, caso queira reaproveitar.

---

## Perguntas frequentes

**O que aparece quando o temporizador chega a zero?**
A **Mensagem** que você configurou, no lugar do relógio. Sem mensagem, o relógio some e nada é exibido no lugar.

**Posso ter vários temporizadores?**
Sim, mas só os **ativos** aparecem — e todos os ativos aparecem ao mesmo tempo. O ideal é manter um ativo por vez.

**Como tiro um temporizador do ar?**
Desligue o interruptor **Ativo** — ele some do site mas continua cadastrado.

**O temporizador usa o fuso de quem?**
O relógio é calculado no computador do jogador a partir da data e hora que você cadastrou. Defina a **Data** pensando no horário do evento e, se o seu público é de vários países, informe o fuso horário na mensagem ou no título.

**Posso mostrar o temporizador em outro lugar além do cabeçalho?**
Sim, em qualquer página criada no construtor de Páginas, usando o bloco **Countdown**.
