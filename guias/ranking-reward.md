# Prêmio por Ranking (RankingReward) — Guia do Cliente

No painel aparece como **Ranking Reward**. Este guia explica, de forma simples, o que é o Prêmio por Ranking, como o jogador ganha e como você o configura pelo painel administrativo. Não é necessário conhecimento técnico.

---

## O que é o Prêmio por Ranking?

O Prêmio por Ranking **recompensa automaticamente os três primeiros** de cada ranking do servidor (level, resets, PvP, guildas, etc.) com **moedas do site**. Quem fica no topo ganha um prêmio, periodicamente.

É uma ferramenta de **competição e retenção**: dá um motivo concreto para o jogador disputar o topo dos rankings.

---

## Conceitos principais

### A recompensa por posição

Para cada **ranking**, você define o prêmio do **1º**, do **2º** e do **3º** colocado — exatamente três posições. Cada posição tem a **moeda** e a **quantidade** próprias (o 1º pode ganhar em uma moeda e o 2º em outra, por exemplo).

### Configuração por período

Um ranking pode ter, além da classificação geral, as versões **Diário**, **Semanal** e **Mensal** (quando o ranking está configurado assim no site). Cada versão tem a **sua própria** tabela de prêmios e a sua própria opção de **Redefinir**.

### Redefinir

Com **Redefinir** ligado, logo depois de pagar os prêmios o sistema **zera aquele ranking**, e a disputa recomeça do zero. Útil para premiações recorrentes (ex.: premiar os melhores da semana e reiniciar).

### De onde vêm os rankings

O plugin reaproveita os **rankings** já configurados no site; só os rankings **ativos** aparecem na tela. Você define apenas a premiação de cada um.

### Quem paga os prêmios

A premiação é feita por **tarefas agendadas** — uma para a classificação geral e uma para cada período (diário, semanal, mensal). A frequência da tarefa é o que define **de quanto em quanto tempo** os prêmios são pagos.

---

## Como o jogador ganha

1. O jogador disputa as posições nos **rankings** do servidor.
2. Quando a tarefa de premiação roda, os **três primeiros** recebem as **moedas** configuradas.
3. O prêmio cai automaticamente na conta, com uma mensagem de **Parabéns** informando a posição e o ranking.

---

## Como configurar (passo a passo)

### 1. Definir os prêmios

1. Vá em **Configurações → Ranking Reward**.
2. No card **Recompensas 1°/2°/3°**, cada ranking ativo aparece com a sua classificação geral e, quando houver, as versões **Diário**, **Semanal** e **Mensal**.
3. Para cada uma, informe a **moeda** e a **Quantidade** do 1º, do 2º e do 3º lugar. Deixe em branco as posições que não premiam.
4. Ligue **Redefinir** nas versões em que o ranking deve ser zerado após o pagamento.
5. Clique em **Salvar**.

### 2. Ativar as tarefas agendadas (pré-requisito)

Sem as tarefas, **nenhum prêmio é pago**. Vá em **Configurações → Tarefas**, clique em **Adicionar** e cadastre, com **Ativo** marcado, as tarefas do grupo **Ranking Reward** que você usa:

| Tarefa (campo **Script**) | O que paga | Frequência sugerida |
|---------------------------|-----------|---------------------|
| **reward** | A classificação geral de cada ranking | A cada rodada de premiação que você quiser (ex.: 1 vez por mês) |
| **reward-daily** | A versão **Diário** | 1 vez por dia |
| **reward-weekly** | A versão **Semanal** | 1 vez por semana |
| **reward-monthly** | A versão **Mensal** | 1 vez por mês |

Cada rodada de uma tarefa paga uma única vez: executar a mesma tarefa duas vezes no mesmo horário não duplica o prêmio.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|------------------------|-----------------|
| Premiar um ranking | **Configurações → Ranking Reward**, card **Recompensas 1°/2°/3°** |
| Definir moeda e valor de cada posição | Campos do 1º, 2º e 3º lugar de cada ranking/período |
| Premiar a versão diária, semanal ou mensal | Linhas **Diário / Semanal / Mensal** do ranking (quando existem) |
| Zerar o ranking após pagar | Opção **Redefinir** de cada ranking/período |
| Pagar os prêmios de fato | **Configurações → Tarefas** (tarefas **reward**, **reward-daily**, **reward-weekly**, **reward-monthly**) |
| Ativar/desativar um ranking | Configuração de rankings do site (só rankings ativos aparecem aqui) |

---

## Dicas e boas práticas

- Premie os **rankings mais disputados** para gerar competição real.
- Calibre os valores para **incentivar sem inflacionar** a economia.
- Use **Redefinir** nas premiações recorrentes (diária/semanal/mensal) para manter a disputa viva; na classificação geral, pense bem antes de ligar — ela zera o ranking.
- Recompensas em **degraus** (1º ganha mais que o 2º, etc.) aumentam a disputa pelo topo.
- Alinhe a **frequência da tarefa** ao período: a tarefa diária uma vez por dia, a semanal uma vez por semana, e assim por diante.

---

## Perguntas frequentes

**Quais rankings posso premiar?**
Os **rankings ativos** já configurados no site — você só define a recompensa de cada um.

**Quantas posições são premiadas?**
Exatamente **três**: 1º, 2º e 3º lugar, cada uma com moeda e quantidade próprias.

**Como o jogador recebe o prêmio?**
Automaticamente, em **moedas**, quando a tarefa agendada roda; ele recebe uma mensagem de **Parabéns** na conta.

**Configurei os prêmios e ninguém recebeu. O que verificar?**
Se as tarefas **reward** / **reward-daily** / **reward-weekly** / **reward-monthly** estão cadastradas e **ativas** em **Configurações → Tarefas**.

**O que o "Redefinir" faz?**
Zera o ranking logo após o pagamento dos prêmios, para a disputa recomeçar. Cada ranking e cada período tem o seu próprio.

**O prêmio pode ser pago duas vezes na mesma rodada?**
Não. Cada rodada de premiação é registrada e paga uma única vez.
