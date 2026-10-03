# Tarefas agendadas e Fila — Guia do Cliente

No painel, as telas aparecem como **Tarefas** e **Fila de Jobs**, dentro de **Configurações**, na categoria **Sistema**.

Este guia explica, de forma simples, **o que são as tarefas automáticas** do Morpheus MuWeb, **por que elas são obrigatórias**, **como agendar a rotina no servidor** e **como acompanhar** tudo pelas telas **Configurações → Tarefas** e **Configurações → Fila de Jobs**.

---

## O que são as tarefas agendadas?

Muita coisa no site acontece "sozinha", sem ninguém clicar: um e-mail de confirmação de cadastro é enviado, um banimento vence e a conta é liberada, o ranking do dia é premiado, o financeiro é atualizado. Tudo isso é feito por **tarefas automáticas** que rodam em horários definidos.

Para que elas rodem, o seu servidor precisa de uma **rotina agendada que chama o Morpheus a cada minuto**. O Morpheus então verifica quais tarefas estão na hora de executar e as executa.

### Sem a rotina, o que para de funcionar

- **Fila de notificações**: e-mails de confirmação de cadastro, recuperação de senha, alerta de login, mensagens de WhatsApp e avisos enviados por plugins não saem.
- **Banimentos temporários** não são liberados na data de vencimento.
- **VIPs vencidos** continuam marcados como VIP (quando a tarefa de VIP está agendada).
- **Financeiro** (`Financeiro` no menu lateral) para de receber os lançamentos de moedas e pedidos e as **cotações** de câmbio não são atualizadas.
- **Premiação de rankings** (plugin Ranking Reward), **recompensas por indicação**, cancelamento de anúncios vencidos no mercado de contas e de itens, verificação de vencedores de leilão e cálculo de patentes não acontecem.

> Resumindo: a rotina é **obrigatória**. Agende-a logo depois da instalação.

---

## Conceitos principais

### 1. A rotina do servidor

É o agendamento feito **fora do painel**, no sistema operacional do servidor web, que executa o Morpheus **uma vez por minuto**. Ela é o "motor"; sem ela, nenhuma tarefa roda, mesmo que esteja ativa no painel.

### 2. Tarefa

Cada tarefa, em **Configurações → Tarefas**, é uma ação (um **Script**) com um horário de execução (**Minutos**, **Horas**, **Dias**, **Semanas**, **Meses**) e um interruptor **Ativo**. A cada minuto, o Morpheus executa as tarefas ativas cujo horário bateu.

Se uma execução ainda está rodando quando chega a próxima, a nova rodada daquela tarefa é pulada — assim uma mesma tarefa nunca roda duas vezes ao mesmo tempo (nenhum e-mail sai em dobro, nenhuma premiação é paga duas vezes).

### 3. Fila (Fila de Jobs)

A **fila** é a lista de trabalhos que o site deixa "para fazer depois": enviar um e-mail, mandar uma mensagem de WhatsApp, avisar o comprador de uma conta. A tarefa **process-queue** (Processar Fila) é quem esvazia essa lista. Cada trabalho tem um status (**Pendente**, **Processando**, **Concluído** ou **Falhou**) e um número de tentativas.

---

## Como agendar a rotina no servidor

A rotina deve executar o arquivo do agendador do Morpheus, a partir da pasta do site, **a cada minuto**. É o único comando que você precisa configurar.

### Linux (crontab)

Edite o crontab do usuário que roda o site e adicione uma linha (troque `/caminho/do/site` pela pasta onde o Morpheus está instalado):

```
* * * * * php /caminho/do/site/scheduler.php
```

### Windows (Agendador de Tarefas)

1. Abra o **Agendador de Tarefas** e crie uma tarefa básica.
2. Em **Disparador**, escolha **Diariamente** e, nas configurações avançadas, marque **Repetir a tarefa a cada: 1 minuto**, por tempo **Indefinidamente**.
3. Em **Ação**, escolha **Iniciar um programa**:
   - **Programa**: o caminho do PHP (ex.: `C:\php\php.exe`).
   - **Argumentos**: `C:\caminho\do\site\scheduler.php`.
   - **Iniciar em**: `C:\caminho\do\site`.
4. Marque a opção para executar mesmo sem usuário conectado.

### Como saber se está funcionando

Abra **Configurações → Tarefas**: a coluna **Última execução** passa a mostrar a data e a hora da última rodada de cada tarefa ativa, e **Último resultado** mostra **sucesso** ou **erro**. Se **Última execução** continua vazia depois de alguns minutos, a rotina do servidor não está rodando.

> O horário das tarefas segue o **Fuso horário** definido em **Configurações → Geral**.

---

## A tela Configurações → Tarefas

A lista mostra todas as tarefas cadastradas com as colunas **Nome**, **Minutos**, **Horas**, **Dias**, **Semanas**, **Meses**, **Última execução** e **Último resultado**. Tarefas ativas e inativas são diferenciadas pela faixa colorida na linha. Há um campo **Pesquisar** por nome.

Ações de cada linha:

- **Editar** (ícone de lápis) — abre o formulário da tarefa.
- **Desativar** / **Ativar** — liga ou desliga a tarefa sem apagá-la.

No **Último resultado**, passe o mouse sobre **erro** para ver a mensagem do problema.

### Adicionar ou editar uma tarefa

Clique em **Adicionar** (ou em editar) e preencha:

| Campo | O que é |
|------|------|
| **Nome** | Um nome amigável para você reconhecer a tarefa (ex.: "Processar Fila"). |
| **Ativo** | Liga a tarefa. Tarefas desligadas ficam na lista, mas não rodam. |
| **Script** | A ação que será executada. A lista é agrupada: o grupo **Default** traz as ações do próprio Morpheus e os demais grupos levam o nome de cada plugin ativo (só aparecem ações de plugins ativos). |
| **Minutos**, **Horas**, **Dias**, **Semanas**, **Meses** | Quando rodar. Todos vêm preenchidos com `*`, que significa "sempre". |

Clique em **Salvar**.

### Como preencher o horário

Os cinco campos seguem o padrão de agendamento mais comum em servidores. Alguns exemplos:

| Quero rodar... | Minutos | Horas | Dias | Semanas | Meses |
|------|------|------|------|------|------|
| A cada minuto | `*` | `*` | `*` | `*` | `*` |
| A cada 5 minutos | `*/5` | `*` | `*` | `*` | `*` |
| A cada 15 minutos | `*/15` | `*` | `*` | `*` | `*` |
| Todo dia às 04:00 | `0` | `4` | `*` | `*` | `*` |
| Todo dia às 23:59 | `59` | `23` | `*` | `*` | `*` |
| Todo domingo à meia-noite | `0` | `0` | `*` | `0` | `*` |
| Todo dia 1 do mês à meia-noite | `0` | `0` | `1` | `*` | `*` |

- **Semanas** é o dia da semana: `0` = domingo, `1` = segunda... `6` = sábado.
- **Dias** é o dia do mês (1 a 31).

---

## Tarefas disponíveis e para que servem

Algumas tarefas já aparecem cadastradas depois da instalação (as do financeiro); as demais você cria em **Adicionar**, escolhendo o **Script** correspondente. Confira a sua lista e crie as que faltam — principalmente **process-queue**, que é a mais importante.

### Grupo Default (Morpheus)

| Script | O que faz | Agendamento sugerido |
|------|------|------|
| **process-queue** | Processa a **Fila de Jobs**: envia e-mails, mensagens de WhatsApp e demais notificações. Indispensável. | A cada minuto (`* * * * *`) |
| **syncronize-bans** | Libera as contas cujo banimento temporário já venceu. Uma conta só é liberada quando não tem outro banimento em vigor. | Todo dia às 23:59 (`59 23 * * *`) |
| **syncronize-vips** | Rebaixa para o tipo gratuito as contas cujo VIP já expirou. Só tem efeito quando o **Sistema VIP** está configurado em **Configurações → Sistema VIP**. | A cada minuto ou a cada 5 minutos |
| **finance-sync-coins** | Captura as movimentações de moedas dos jogadores para o módulo **Financeiro** (relatórios de economia e alertas). Já vem cadastrada e ativa. | A cada 10 minutos (`*/10`) |
| **finance-sync-orders** | Leva os pedidos pagos para o extrato do **Financeiro** (rede de segurança, caso algum pedido não tenha sido registrado na hora). Já vem cadastrada e ativa. | A cada 15 minutos (`*/15`) |
| **finance-fetch-rates** | Busca as cotações das moedas estrangeiras usadas nos pedidos (**Financeiro → Taxas de câmbio**). Já vem cadastrada, porém **inativa** — ative se você recebe pagamentos em mais de uma moeda. | Todo dia às 04:00 (`0 4 * * *`) |
| **clear-http-logs** | Apaga os registros antigos de acesso (**Logs → HTTP**), mantendo só os dias recentes. Evita que o banco cresça demais. | Todo dia, de madrugada |
| **clear-sql-logs** | Apaga os registros antigos de consultas (**Logs → SQL**). | Todo dia, de madrugada |

### Tarefas de plugins

Só aparecem na lista de **Script** quando o plugin está **ativo**.

| Plugin (grupo) | Script | O que faz | Agendamento sugerido |
|------|------|------|------|
| **Ranking Reward** | **reward-daily** | Premia os 3 primeiros do ranking diário e reinicia o ranking (se configurado). | Todo dia às 23:59 |
| **Ranking Reward** | **reward-weekly** | Premia o ranking semanal. | Domingo à meia-noite (`0 0 * 0 *`) |
| **Ranking Reward** | **reward-monthly** | Premia o ranking mensal. | Dia 1 à meia-noite (`0 0 1 * *`) |
| **Ranking Reward** | **reward** | Premia o ranking geral. | Dia 1 à meia-noite (`0 0 1 * *`) |
| **Indication** | **process-rewards** | Verifica as metas de indicação alcançadas e credita as recompensas de quem indicou. | A cada 5 minutos (`*/5`) |
| **Account Market** | **cancel-expired-purchases** | Cancela compras de contas que ficaram sem pagamento pelo tempo limite configurado. | A cada minuto ou a cada 5 minutos |
| **Item market** | **remove-expired-items** | Cancela anúncios de itens vencidos (quando há tempo de expiração configurado). | A cada 5 minutos |
| **Auction** | **verify-items** | Encerra leilões finalizados e entrega item e valor aos vencedores. | A cada minuto |
| **Patents** | **calculate-patents** | Recalcula as patentes dos personagens conforme as regras cadastradas. | Uma vez por dia |

> O guia de cada plugin traz detalhes sobre o que a tarefa dele faz e como configurar as regras.

---

## A tela Configurações → Fila de Jobs

Mostra tudo o que o site colocou na fila para processar. No topo há quatro cartões com o total de trabalhos em cada status: **Pendente**, **Processando**, **Concluído** e **Falhou**.

A tabela traz **#** (número), **Handler** (o tipo do trabalho — ex.: envio de e-mail de confirmação), **Status**, **Tentativas** (feitas / máximo), **Criado em** e **Processado em**. Um ícone de alerta ao lado do nome indica que houve erro; passe o mouse para ver a mensagem. Use **Filtros** → **Status** para ver só um status e **Aplicar** / **Limpar**.

Ações de cada linha:

- **Detalhes do job** (ícone de olho) — abre uma janela com **ID**, **Status**, **Tentativas**, **Criado em**, **Disponível em**, **Processado em**, **Handler**, **Payload** (os dados do trabalho, como o destinatário) e **Erro** (quando houve falha).
- **Tentar novamente** — só para trabalhos com status **Falhou**: volta o trabalho para a fila para ser processado de novo.
- **Excluir** — só para trabalhos **Concluído** ou **Falhou**.

No topo da tela, o botão **Purgar concluídos e falhos** apaga de uma vez todos os trabalhos já concluídos ou que falharam, após confirmação. Use para manter a lista enxuta.

### Como a fila se comporta

- Um trabalho é processado por **process-queue**; se der erro, ele tenta de novo até o número máximo de tentativas e então fica como **Falhou**.
- Se um trabalho ficar preso em **Processando** por mais de 15 minutos (por exemplo, o servidor reiniciou no meio), ele volta sozinho para **Pendente** — ou vai para **Falhou** se já esgotou as tentativas.
- A coluna **Disponível em** mostra a partir de quando o trabalho pode rodar (alguns são agendados para mais tarde).

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|------|------|
| Ligar o "motor" das tarefas | Fora do painel: rotina a cada minuto no servidor (crontab ou Agendador de Tarefas) |
| Ver, criar, editar, ativar ou desativar uma tarefa | **Configurações → Tarefas** |
| Conferir se as tarefas estão rodando | **Configurações → Tarefas** → colunas **Última execução** e **Último resultado** |
| Ver e-mails e notificações pendentes ou com falha | **Configurações → Fila de Jobs** |
| Reenviar uma notificação que falhou | **Configurações → Fila de Jobs** → **Tentar novamente** |
| Limpar a fila antiga | **Configurações → Fila de Jobs** → **Purgar concluídos e falhos** |
| Ajustar o fuso horário usado pelos agendamentos | **Configurações → Geral** → **Fuso horário** |
| Configurar o e-mail de envio usado pela fila | **Configurações → Geral** → card **SMTP** |
| Regras de premiação de ranking, indicação, leilão etc. | Tela de configuração de cada plugin |

---

## Dicas e boas práticas

- **Crie a tarefa process-queue a cada minuto antes de qualquer outra coisa.** Sem ela nenhum jogador recebe e-mail de cadastro ou de recuperação de senha.
- **Mantenha o nome das tarefas claro** ("Premiar ranking diário", "Liberar banimentos") para a equipe entender a lista.
- **Olhe a tela de Tarefas de vez em quando.** Um **erro** em **Último resultado** aponta um problema de configuração (SMTP errado, plugin desativado, regra incompleta).
- **Não agende tarefas pesadas a cada minuto** (como cálculo de patentes ou limpeza de logs); uma vez por dia basta.
- **Use Purgar concluídos e falhos** periodicamente para manter a fila leve.
- **Desative em vez de excluir**: para pausar uma tarefa temporariamente (ex.: um evento), use **Desativar**.

---

## Perguntas frequentes

**Criei a tarefa no painel e ela não roda. Por quê?**
O painel só define *o que* e *quando* rodar. Quem executa é a rotina do servidor, que precisa estar agendada a cada minuto. Confira se **Última execução** se atualiza; se não, a rotina não está configurada ou o caminho do site está errado.

**Os e-mails não estão saindo.**
Primeiro confira se a tarefa **process-queue** existe, está **Ativa** e a cada minuto. Depois veja **Configurações → Fila de Jobs**: se os trabalhos estão em **Falhou**, abra **Detalhes do job** e leia o campo **Erro** — normalmente é o SMTP em **Configurações → Geral** incorreto. Depois de corrigir, use **Tentar novamente**.

**Posso rodar a rotina a cada 5 minutos em vez de a cada minuto?**
Não é recomendado. A rotina a cada minuto é leve e permite que tarefas como a fila e os leilões respondam rápido. Com intervalos maiores, as tarefas marcadas para um minuto específico podem nunca bater.

**Uma tarefa demorada pode rodar duas vezes ao mesmo tempo?**
Não. Se a execução anterior ainda está rodando, a próxima rodada daquela tarefa é pulada automaticamente.

**O que significa "erro" em Último resultado?**
A última execução falhou. Passe o mouse sobre o selo para ler a mensagem. As causas mais comuns são plugin desativado, configuração incompleta ou falha de conexão com um serviço externo.

**Por que as tarefas de um plugin não aparecem na lista de Script?**
A lista só mostra tarefas de plugins **ativos**. Ative o plugin em **Plugins** e volte à tela.

**O que acontece com um trabalho da fila se o servidor reiniciar durante o processamento?**
Ele volta para **Pendente** sozinho depois de 15 minutos e é processado de novo. Por isso, em casos raros, uma notificação pode chegar duas vezes.

**Posso apagar um trabalho Pendente?**
Não. Só trabalhos **Concluído** ou **Falhou** podem ser excluídos. Se não quiser que ele seja processado, desative a tarefa **process-queue** antes (não recomendado) ou aguarde.

---

> Dúvida sobre o agendamento no seu servidor? Envie ao suporte o sistema operacional do servidor web e a pasta onde o site está instalado.
