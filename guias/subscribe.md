# Assinaturas VIP (Subscribe) — Guia do Cliente

No painel aparece como **Assinaturas**; para o jogador, o serviço se chama **Minha Assinatura**. Este guia explica, de forma simples, **o que é** o sistema de assinaturas, **como o jogador assina, renova e cancela** e **como você configura** tudo pelo painel administrativo. Não é necessário nenhum conhecimento técnico.

---

## O que é o sistema de Assinaturas?

É o **VIP com renovação automática**. Em vez de comprar VIP avulso toda vez que vence, o jogador escolhe um **plano**, paga com cartão e o meio de pagamento cobra sozinho a cada mês (ou a cada ano). A cada cobrança paga, o VIP do jogador é estendido automaticamente.

Por que vale a pena:

- **Receita previsível:** você sabe quanto entra todo mês, sem depender de o jogador lembrar de renovar.
- **Menos churn de VIP:** o benefício nunca "cai" por esquecimento — a renovação é automática.
- **Zero operação manual:** ativação, renovação, cancelamento e histórico de cobranças acontecem sozinhos; você só acompanha.

---

## Conceitos principais

### 1. Plano

O **plano** é o que o jogador assina. Cada plano define:

- **Tipo de VIP** que o assinante recebe (um dos níveis configurados no seu sistema de VIP).
- **Preço mensal** e/ou **preço anual** — pode oferecer só um dos dois ou os dois (aí o jogador escolhe o ciclo).
- **Moeda** da cobrança.
- **Gateway** (meio de pagamento) fixo, ou em branco para o jogador escolher entre os disponíveis.
- **Nome**, **Descrição** e lista de **Vantagens** (em todos os idiomas do site), que aparecem no cartão do plano.
- Marcação **Recomendado**, que destaca o plano na página.

### 2. Assinatura

A **assinatura** é o vínculo entre uma conta e um plano, com um **ciclo** (mensal ou anual), um **status** e a data **Renova em** (fim do período atual pago). Os status possíveis são **Ativo**, **Em atraso**, **Incompleta**, **Cancelada** e **Não paga**.

### 3. Meio de pagamento com cobrança recorrente

A cobrança automática depende de um meio de pagamento que suporte assinatura. Hoje o único disponível é o **Stripe** (cartão de crédito). As credenciais são as mesmas já configuradas em **Configurações → Gateways** — não há nada para repetir aqui.

### 4. Dias de carência

A cada cobrança paga, o VIP é estendido por **um ciclo + os dias de carência**. A carência serve para o VIP não cair enquanto o meio de pagamento ainda está tentando cobrar o cartão (quando uma cobrança falha, ele tenta de novo por alguns dias).

---

## Como o jogador usa

### Assinar

1. O jogador vê os planos em dois lugares: na página **VIP** do site (bloco **Planos de assinatura**, "Assine e mantenha seu VIP sempre ativo com renovação automática.") e no painel dele, no serviço **Minha Assinatura**.
2. Se algum plano tem preço mensal e anual, aparecem os botões **Mensal** / **Anual** para alternar o ciclo.
3. Cada cartão mostra o nome, a descrição, o preço por ciclo, as vantagens e o botão **Assinar**. Se o plano não fixa um meio de pagamento, o jogador escolhe em uma lista ao lado do botão.
4. Ao clicar em **Assinar**, ele é levado ao checkout do meio de pagamento ("Redirecionando para o checkout"), onde informa o cartão.
5. Concluído o pagamento, a assinatura fica **Ativo** e o VIP do plano é aplicado na conta assim que a primeira cobrança é confirmada. Se o plugin Sender estiver ativo, o jogador recebe um WhatsApp de "Assinatura ativada".

### Acompanhar

Na página **Minha Assinatura**, o bloco **Sua assinatura** mostra o plano, o status e a data **Renova em**. Abaixo, o **Histórico de cobranças** lista cada cobrança com **Data**, **Valor** e **Status**.

### Renovar

Não há nada a fazer: o meio de pagamento cobra o cartão no fim de cada ciclo. Cada cobrança paga estende o VIP, gera um pedido pago no financeiro do site e (com o Sender) envia o aviso "Assinatura renovada".

### Cancelar

1. Em **Minha Assinatura**, o jogador clica em **Cancelar assinatura**.
2. O cancelamento é agendado para o **fim do período já pago** ("Sua assinatura será cancelada no fim do período atual"). Não há reembolso proporcional: ele continua VIP até a data já concedida.
3. Quando o período termina, a assinatura passa a **Cancelada** e para de renovar.

---

## Como configurar (passo a passo)

### Passo 1 — Ativar o meio de pagamento

1. Abra **Configurações → Gateways** e ative o **Stripe**, preenchendo as credenciais da sua conta Stripe — inclusive o **Webhook secret**, que é o que permite ao Stripe avisar o site sobre cada cobrança paga, cancelamento ou atraso.
2. Sem o Stripe ativo, a página de planos mostra "Nenhum gateway de pagamento disponível" e o botão **Assinar** fica desligado.

### Passo 2 — Criar os planos

1. Abra **Assinaturas → Planos** no menu lateral (ou o card **Configurações → Assinaturas**).
2. Clique em **Adicionar** e preencha:
   - **Nome** (traduzível, obrigatório);
   - **Tipo de VIP** — o nível de VIP que o assinante recebe;
   - **Moeda**;
   - **Preço mensal** e/ou **Preço anual** — é obrigatório informar pelo menos um ("Defina ao menos um preço mensal ou anual");
   - **Gateway** — deixe em **Todos os gateways disponíveis** para o jogador escolher ("Deixe em branco para o usuário escolher") ou fixe o **Stripe**;
   - **Recomendado** — "Destaca este plano na página de assinatura";
   - **Ativo** — só planos ativos aparecem para o jogador;
   - **Descrição** (traduzível) — texto curto do cartão;
   - **Vantagens** (traduzível) — "Uma vantagem por linha — aparece na comparação".
3. Clique em **Salvar**.

Na lista de planos (colunas **Nome**, **Tipo de VIP**, **Mensal**, **Anual**, **Status**) o plano recomendado aparece com ★. Para mudar a ordem em que os planos aparecem no site, **arraste as linhas** — a ordem é salva na hora ("Ordem atualizada"). Cada linha tem os botões de editar e excluir.

### Passo 3 — Definir a carência

1. Abra **Assinaturas → Configurações**.
2. Em **Dias de carência** ("Dias extras somados ao VIP a cada renovação, pra sobreviver às retentativas de cobrança"), informe quantos dias extras somar a cada ciclo. O padrão é 3.
3. Clique em **Salvar**.

### Passo 4 — Conferir o serviço no painel do jogador

O serviço **Minha Assinatura** é criado pelo plugin e já vem liberado. Se ele não aparecer para os jogadores, confira em **Configurações → Serviços** se está ativo.

### Passo 5 — Acompanhar os assinantes

Em **Assinaturas → Assinantes** você vê todas as assinaturas com **Conta**, **Plano**, **Gateway**, **Status**, **Renova em** e **Created at**, e pode buscar por conta. Nas assinaturas ativas há o botão **Cancelar assinatura** ("Cancelar esta assinatura no fim do período atual?") — funciona igual ao cancelamento feito pelo jogador: para de renovar no fim do período pago.

---

## Como o VIP é aplicado

Vale entender as regras, porque o VIP da conta pode ter vindo de outras fontes (compra avulsa, pacote, bônus dado pelo administrador):

- **Cada cobrança paga concede um ciclo.** Uma cobrança mensal estende 1 mês + carência; uma anual, 1 ano + carência. A mesma cobrança nunca é contada duas vezes, mesmo que o meio de pagamento avise o site mais de uma vez — não existe "ciclo em dobro".
- **A assinatura soma, nunca rebaixa.** Se o jogador já é VIP:
  - o **nível** final é o maior entre o VIP atual e o do plano — um VIP mais alto vindo de outra fonte é mantido;
  - a **data de expiração** final é a maior entre a atual e "hoje + ciclo + carência" — uma expiração mais distante nunca é encurtada.
- **Sem VIP (ou VIP vencido):** a conta recebe o nível do plano por um ciclo + carência, contado a partir da cobrança.
- Cada aplicação fica registrada no histórico da conta como "Assinatura renovada".

---

## O que acontece ao vencer, atrasar ou cancelar

| Situação | Status no painel | O que acontece com o VIP |
|----------|------------------|--------------------------|
| Cobrança paga no vencimento | **Ativo** | Estendido por mais um ciclo + carência |
| Cartão recusado; o meio de pagamento está tentando de novo | **Em atraso** | Continua válido até a data já concedida (por isso existe a carência) |
| Tentativas esgotadas sem pagamento | **Não paga** | Para de renovar; o VIP vence na data já concedida |
| Jogador ou admin cancelou | **Ativo** até o fim do período, depois **Cancelada** | Continua válido até a data já concedida; depois vence normalmente |
| Checkout iniciado mas não concluído | **Incompleta** | Nada é concedido |

Enquanto a assinatura está **Ativo** ou **Em atraso**, ela conta como ativa: o jogador vê o botão **Cancelar assinatura** e o admin vê a ação de cancelar.

O sistema **não depende de tarefa agendada**: tudo é acionado pelos avisos que o meio de pagamento envia ao site (cobrança paga, mudança de status, cancelamento). Por isso o **Webhook secret** do Stripe precisa estar configurado — sem ele, os avisos são ignorados e a assinatura não ativa nem renova.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|-----------------------|-----------------|
| Ativar o meio de pagamento com cobrança recorrente (Stripe) e o Webhook secret | **Configurações → Gateways** |
| Criar um plano | **Assinaturas → Planos** → **Adicionar** |
| Editar ou excluir um plano | **Assinaturas → Planos** → botões da linha |
| Mudar a ordem dos planos no site | **Assinaturas → Planos** → arrastar as linhas |
| Destacar um plano | Formulário do plano → **Recomendado** |
| Esconder um plano sem excluir | Formulário do plano → desligar **Ativo** |
| Fixar ou liberar o meio de pagamento de um plano | Formulário do plano → **Gateway** |
| Definir os dias extras de VIP por renovação | **Assinaturas → Configurações** → **Dias de carência** |
| Ver quem assina, status e próxima renovação | **Assinaturas → Assinantes** |
| Cancelar a assinatura de um jogador | **Assinaturas → Assinantes** → **Cancelar assinatura** |
| Ver as cobranças de uma assinatura no financeiro | **Financeiro → Pedidos** (cada cobrança paga vira um pedido) |
| Liberar/ocultar o serviço **Minha Assinatura** para os jogadores | **Configurações → Serviços** |
| Avisar o jogador por WhatsApp (ativada, renovada, cancelada) | Plugin **Sender** → **Templates** |

---

## Dicas e boas práticas

- **Ofereça mensal e anual no mesmo plano.** O anual com desconto aumenta o valor pago à vista e reduz cancelamentos; o toggle **Mensal/Anual** aparece sozinho.
- **Deixe a carência em 3 a 5 dias.** Pouca carência derruba o VIP de quem só teve o cartão recusado por um dia; carência demais vira VIP de graça para quem cancelou.
- **Use as Vantagens como comparação.** Liste os benefícios reais de cada nível de VIP, uma por linha, para o jogador entender por que o plano recomendado vale mais.
- **Não exclua um plano com assinantes — desative.** Desligar **Ativo** tira o plano da página sem mexer em quem já assina.
- **Combine com o Sender.** Os avisos de ativação, renovação e cancelamento por WhatsApp reduzem dúvidas e chamados ("meu VIP renovou?").
- **Teste com um cartão de teste do Stripe** antes de divulgar, e confira que a assinatura aparece em **Assinantes** como **Ativo** com a data **Renova em** preenchida.

---

## Perguntas frequentes

**O jogador já é VIP e assinou. Ele perde o VIP que tinha?**
Não. A assinatura só soma: mantém o nível mais alto e a expiração mais distante entre o VIP atual e o do plano.

**Se o meio de pagamento avisar a mesma cobrança duas vezes, o jogador ganha dois ciclos?**
Não. Cada cobrança é identificada e só concede um ciclo, mesmo que o aviso chegue repetido.

**O que acontece quando o cartão é recusado?**
A assinatura fica **Em atraso** e o Stripe tenta cobrar de novo por alguns dias. O VIP continua valendo até a data já concedida (ciclo + carência). Se o pagamento sair, volta para **Ativo** e estende; se não, para de renovar e o VIP vence na data.

**O jogador cancelou. O VIP cai na hora?**
Não. O cancelamento vale para o fim do período já pago; ele continua VIP até a data concedida e não é cobrado de novo.

**Posso cancelar a assinatura de um jogador pelo painel?**
Sim, em **Assinaturas → Assinantes**, botão **Cancelar assinatura** — com o mesmo efeito: para de renovar no fim do período atual.

**Quais meios de pagamento fazem cobrança recorrente?**
Hoje, apenas o **Stripe**. Os demais meios de pagamento do site continuam servindo para doações e compras avulsas, mas não para assinaturas.

**Preciso agendar alguma tarefa para as renovações?**
Não. As renovações são acionadas pelos avisos do próprio Stripe. O que precisa estar certo é o **Webhook secret** em **Configurações → Gateways**.

**Onde vejo o dinheiro das assinaturas?**
Cada cobrança paga gera um pedido pago em **Financeiro → Pedidos**, e o jogador vê o mesmo histórico em **Minha Assinatura → Histórico de cobranças**.

---

> Precisa de ajuda para configurar o Stripe ou montar os planos? Entre em contato com o suporte.
