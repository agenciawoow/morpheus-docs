# Tickets de Suporte (HelpDesk) — Guia do Cliente

No painel administrativo o módulo aparece como **Tickets de suporte**. Este guia explica, de forma simples, o que é o sistema de tickets, como o jogador abre um chamado e como você atende e configura tudo pelo painel. Não é necessário conhecimento técnico.

---

## O que são os Tickets de suporte?

É o **sistema de chamados** do seu servidor. Em vez de atendimento solto por Discord ou e-mail, o jogador abre um **ticket** pelo site, escolhe um **departamento**, descreve o problema e acompanha a resposta — tudo organizado e com histórico.

Para a equipe, centraliza o atendimento: cada chamado tem **status**, **prioridade**, **responsável** e a conversa completa registrada.

---

## Conceitos principais

### O ticket

É a solicitação do jogador. Tem um **assunto**, uma **mensagem** inicial, um **departamento**, uma **prioridade** e pode trazer **imagens** anexadas. Cada ticket recebe um número e guarda toda a troca de mensagens.

### Os departamentos

São as **categorias** de atendimento (ex.: *Dúvidas*, *Pagamentos*, *Bugs*, *Denúncias*). Você cria quantos quiser, ativa/desativa e **reordena** arrastando. O jogador escolhe um departamento ao abrir o chamado; departamentos inativos não aparecem para ele.

### Status

O ciclo de vida do ticket:

- **Pendente** — recém-aberto ou com nova resposta do jogador, aguardando a equipe.
- **Aguardando** — a equipe respondeu e espera o retorno do jogador.
- **Finalizado** — atendimento concluído.
- **Cancelado** — encerrado sem solução.

No menu lateral, os tickets com status *Aguardando* aparecem como **Tickets em progresso**.

### Prioridade

Cada ticket tem uma prioridade — **Baixo**, **Normal**, **Alto** ou **Crítico** — que ajuda a equipe a ordenar a fila. O jogador escolhe uma prioridade ao abrir o chamado (o padrão é *Normal*) e a equipe pode ajustá-la a qualquer momento.

### Responsável

Você pode atribuir um **atendente** a cada ticket, deixando claro quem está cuidando daquele caso.

### Avaliação

Depois de **finalizado**, o jogador pode dar uma **nota de 1 a 5** ao atendimento — uma única vez por ticket. É o seu termômetro de qualidade.

---

## Como o jogador usa

1. Na área da conta, o jogador acessa **Suporte** (a página **Meus tickets**) e clica em **Abrir novo ticket**.
2. Preenche **Assunto**, escolhe o **Departamento** e a **Prioridade**, escreve a **Mensagem** (com o limite de caracteres informado na tela) e pode anexar **Imagens**. As **Regras** que você configurou aparecem nessa mesma página.
3. Clica em **Abrir ticket** e passa a acompanhar as respostas na página do ticket, onde pode responder com **Enviar mensagem** (também com imagens). Toda resposta do jogador devolve o ticket para **Pendente**.
4. Quando o ticket é finalizado, ele pode avaliar em **Avalie este ticket**.

> Há um **intervalo mínimo** entre a abertura de um ticket e o próximo (configurável, em segundos). Se tentar antes do tempo, o jogador recebe um aviso para aguardar.

---

## Como atender (passo a passo)

### 1. Configurar (uma vez)

1. Vá em **Configurações → Tickets de suporte**.
2. Defina **Máximo de caracteres** (tamanho máximo de cada mensagem), **Tempo de abertura de um ticket para outro (segundos)** (intervalo mínimo entre tickets do mesmo jogador; deixe 0 para não limitar) e as **Regras** (texto exibido ao jogador na abertura do chamado).
3. Clique em **Salvar**.

### 2. Criar os departamentos

1. No menu lateral, vá em **Tickets de suporte → Departamentos** e clique em **Adicionar**.
2. Informe o **Nome** (traduzível nos idiomas do site) e marque **Ativo**.
3. Salve. Na lista, arraste as linhas para definir a ordem em que aparecem para o jogador.

### 3. Responder os tickets

1. No menu lateral, **Tickets de suporte** mostra **Tickets pendentes**, **Tickets em progresso** e **Tickets finalizados**, cada um com um contador. O painel inicial também exibe um indicador com os **Tickets pendentes** e os **Tickets em progresso**.
2. Na lista, use **Pesquisar** para filtrar por **Usuário**, **Assunto**, **Departamento**, **Responsável** e período (**Criado de** / **Criado até**).
3. Abra o ticket (botão **Visualizar**) para ver a conta, o departamento, o status, a prioridade, a mensagem original e todo o histórico de **Mensagens**.
4. Em **Adicionar nova mensagem**, escreva a resposta (opcionalmente com **Imagens**), ajuste **Status**, **Responsável** e **Prioridade** e clique em **Salvar**. Mesmo sem escrever mensagem, salvar atualiza o status, o responsável e a prioridade.
5. O jogador recebe um aviso na conta de que o ticket teve novas interações.

### 4. Acompanhar as estatísticas

Em **Estatísticas** (botão no topo da lista de tickets) você vê o **Total de tickets**, quantos estão **Pendente**, **Aguardando** e **Finalizado**, a **Avaliação média** (com a quantidade de tickets avaliados) e a tabela **Tickets por departamento**.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|------------------------|-----------------|
| Limite de caracteres, intervalo entre tickets e regras | **Configurações → Tickets de suporte** |
| Criar, ativar/desativar e reordenar departamentos | **Tickets de suporte → Departamentos** |
| Ver os chamados por status | **Tickets de suporte → Tickets pendentes / Tickets em progresso / Tickets finalizados** |
| Filtrar a lista | Botão **Pesquisar** no topo da lista (Usuário, Assunto, Departamento, Responsável, período) |
| Responder e alterar status, prioridade e responsável | Dentro do ticket, em **Adicionar nova mensagem** |
| Ver indicadores rápidos | Painel inicial (card **Tickets pendentes**) |
| Ver desempenho e avaliação média | Botão **Estatísticas** no topo da lista de tickets |

---

## Dicas e boas práticas

- Crie **departamentos claros** — direciona o chamado para a pessoa certa e agiliza a resposta.
- Use as **Regras** para orientar o jogador (ex.: "informe o nome do personagem e o horário do problema").
- Ajuste a **prioridade** ao triar os tickets para não deixar casos críticos no fim da fila.
- Atribua um **Responsável** para evitar que dois atendentes respondam o mesmo ticket.
- Calibre o **intervalo entre tickets** para reduzir abertura em excesso sem atrapalhar quem realmente precisa.
- Acompanhe a **Avaliação média** nas estatísticas para medir a qualidade do atendimento.

---

## Perguntas frequentes

**O jogador pode abrir vários tickets de uma vez?**
Há um intervalo mínimo configurável (em segundos) entre a abertura de um ticket e o próximo. Com o valor 0, não há limite.

**Dá para anexar imagens?**
Sim, tanto na abertura quanto nas respostas, do lado do jogador e do lado da equipe.

**Quem pode ver um ticket?**
Só o jogador que o abriu e a equipe administrativa.

**Como o jogador sabe que respondi?**
Ele recebe um aviso na conta a cada atualização do ticket.

**A avaliação pode ser refeita?**
Não. Cada ticket finalizado é avaliado **uma única vez**, e só tickets finalizados podem ser avaliados.

**Posso ter departamentos desativados?**
Sim. Departamentos inativos não aparecem para o jogador ao abrir um chamado, mas o histórico dos tickets antigos é preservado.

**O que acontece quando o jogador responde um ticket já respondido pela equipe?**
O ticket volta para **Pendente** e reaparece na fila da equipe.
