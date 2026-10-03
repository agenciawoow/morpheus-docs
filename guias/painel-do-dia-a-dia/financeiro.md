# Financeiro — Guia do Cliente

Este guia explica, de forma simples, o que é o Financeiro do Morpheus, como o jogador paga pelo site e como você acompanha e controla tudo pelo painel. Não é necessário nenhum conhecimento técnico.

---

## O que é o Financeiro?

O Financeiro cuida de **tudo o que envolve dinheiro** no seu servidor: o jogador escolhe um valor, paga por um meio de pagamento, o sistema confirma o pagamento e entrega os créditos — e cada passo fica registrado para você.

- **Receita clara:** você vê quanto entrou, por dia, por meio de pagamento e por moeda.
- **Economia sob controle:** acompanha quanto de moeda do jogo está entrando e saindo de circulação.
- **Proteção:** confirmações repetidas não creditam duas vezes, estornos desfazem o crédito e ganhos suspeitos de moeda geram alerta para você revisar.

No painel, tudo fica no menu lateral **Financeiro** (seção Loja & economia). As configurações ficam nos cards da landing **Configurações**, no grupo **Economia**.

---

## Conceitos principais

Pense em **três tipos de "dinheiro"** que o Financeiro acompanha. No painel eles aparecem como **Ativos**:

| Ativo | O que é | Para que serve |
|-------|---------|----------------|
| **Dinheiro** | O pagamento real (reais, dólar etc.) que entra pelos meios de pagamento. | É a sua **receita**. |
| **Carteira** | Um saldo interno do site que o jogador acumula ao pagar. | O jogador **gasta** na loja, em pacotes, VIP etc. |
| **Moeda** | A moeda dentro do jogo (WCoin, Goblin Point e outras que você cadastrar). | É usada **dentro do servidor**. |

Outras peças que aparecem nas telas:

- **Pedido:** cada tentativa de pagamento gera um pedido, com valor, meio de pagamento, cupom (se houver), o que será entregue e a situação (Pendente, Pago, estornado, cancelado etc.).
- **Lançamento:** todo movimento de saldo (crédito ou débito) em qualquer ativo. O conjunto dos lançamentos é o **Extrato**.
- **Categoria do lançamento:** indica a origem do movimento — Depositar, Retirar, Compra, Pagamento por gateway, Transferência, Recompensa, Reembolso, Ajuste manual e Alteração no jogo.
- **Meio de pagamento (Gateway):** o serviço que recebe o dinheiro do jogador. O Morpheus traz nove: **Stripe**, **PayPal**, **PagSeguro**, **Mercado Pago**, **PicPay**, **Pagar.Me**, **PagHiper**, **MorpheusPay** e **Transferência bancária** (esta última com confirmação manual, pelo comprovante).
- **Cupom:** código de desconto que o jogador aplica na hora de pagar. Tem guia próprio (veja o guia de Cupons).

---

## Como o jogador usa

1. O jogador abre a página de doação/compra do site e, em **Escolha o valor**, clica em um dos valores sugeridos ou informa **Outro valor**.
2. Em **Como você quer pagar?**, escolhe um dos meios de pagamento ativos. Cada um mostra a taxa (ex.: "+5% fee") ou **Sem taxa**.
3. Se tiver um cupom, digita o **Código do cupom**. O **Total a pagar** e o **Você recebe** são recalculados na hora, já com desconto e taxa.
4. Clica em **Finalizar pagamento** e conclui no meio de pagamento escolhido. Assim que o pagamento é confirmado, os créditos entram na carteira dele (ou o item/VIP comprado é entregue).
5. Se a **Transferência bancária** estiver ativa, aparece a opção **Ou pague por transferência bancária**: o jogador vê as contas bancárias cadastradas, faz a transferência e envia uma **Nova confirmação de pagamento** informando **Conta bancária**, **Valor**, o **Comprovante** e uma **Mensagem** opcional. Ele acompanha o andamento em **Minhas doações**, pode trocar mensagens com você e recebe os créditos quando você aprovar.

> O jogador pode acessar o recibo dos próprios pedidos e, nos pagamentos por transferência, conversar com você pela própria confirmação.

---

## Como configurar (passo a passo)

### 1. Carteiras e moedas

- **Configurações → Carteiras:** cadastre pelo menos uma carteira (**Nome**, **Ativo**). É nela que os créditos das doações caem.
- **Configurações → Moedas:** cadastre as moedas do jogo (**Nome**, **Ativo**). Os campos **Banco de dados**, **Tabela**, **Coluna de saldo**, **Coluna de condição** e **Valor da condição** são um recurso avançado que diz onde a moeda vive no banco do jogo — altere só com ajuda de quem conhece o banco do seu servidor. O campo **Limite de alerta de anomalia** define a partir de que ganho dentro do jogo o sistema gera um alerta (deixe em branco para não alertar).
- **Configurações → Sistema VIP:** cadastre os **Tipos** de VIP (**Código** e **Nome**). Os campos de coluna são avançados, como nas moedas.

### 2. Doação

Em **Configurações → Doação**:

- **Carteira de doação:** a carteira que recebe os créditos das doações e das transferências bancárias aprovadas.
- **Valores sugeridos:** os valores (separados por vírgula) que viram botões rápidos na tela de pagamento.

### 3. Meios de pagamento

Em **Configurações → Gateways** cada meio de pagamento aparece como um card com um interruptor para ativar/desativar e o botão **Configurar**, que abre os campos daquele serviço (credenciais como Client ID, Client Secret, Token, Webhook secret, além de **Moeda**, **Sandbox** e **Taxa**, conforme o serviço).

- **Taxa** é um percentual somado ao total que o jogador paga. Não existe valor mínimo por meio de pagamento no painel.
- Os campos obrigatórios só são exigidos quando o meio de pagamento está ativo — você pode deixar as credenciais salvas e ativar depois.
- Alguns meios de pagamento dependem de licença; só os disponíveis para a sua instalação aparecem.

### 4. Contas bancárias

Em **Configurações → Contas bancárias** cadastre as contas que o jogador verá ao pagar por transferência: **Nome do banco**, **Agência**, **Conta**, **Operação**, **Favorecido**, **Documento**, **Logo** e **Observações**. Arraste as linhas da lista para definir a ordem de exibição.

### 5. Taxas de câmbio (se você vende em mais de uma moeda)

Em **Financeiro → Taxas de câmbio**:

- Clique em **Atualizar via API** para buscar as cotações mais recentes das moedas estrangeiras usadas pelos seus meios de pagamento.
- Ou cadastre manualmente em **Adicionar taxa**: **Moeda**, **Taxa** (valor de 1 unidade na sua moeda base) e **Data de vigência** (deixe em branco para valer a partir de agora).
- A lista mostra cada taxa com **Adicionado por** e o botão **Remover**.

As taxas convertem a receita em moeda estrangeira para a sua moeda base nos relatórios, usando a taxa vigente na data do pedido. **Sem cotação, o pagamento passa normalmente** — o pedido apenas fica fora do total consolidado da tela de Receita até você cadastrar a taxa.

### 6. Acompanhar os pedidos

Em **Financeiro → Pedidos** você vê todos os pedidos com conta, meio de pagamento, **Valor**, **Total**, **Entrega**, **Cupom**, **Criado em** e **Status**. Use **Pesquisar** para filtrar por **Conta** e por período (**Criado de** / **Criado até**).

Em cada pedido:

- **Confirmar:** marca como pago e entrega os créditos (para meios que aceitam confirmação manual).
- **Recusar:** cancela o pedido.
- **Recibo:** abre o recibo do pedido, com opção de **Imprimir**.

Quando o recebimento de comprovantes está habilitado, aparece no topo o botão **Confirmações de pagamento**, que lista os comprovantes enviados pelos jogadores (**Usuário**, **Conta bancária**, **Valor**, **Comprovante**, **Status**, **Criado em**). Abra um deles em **Visualizar** para ver o comprovante, ler e responder as **Mensagens** (**Responder**) e decidir: **Liberar créditos** (ajustando o **Valor** se precisar) ou **Recusar**.

---

## As telas do Financeiro

| Tela | O que mostra |
|------|--------------|
| **Financeiro → Painel** | Resumo do período (filtro de datas): **Receita real** com **Pedidos pagos**, **Créditos emitidos**, **Gasto interno**, **Total de lançamentos** por ativo, gráfico **Receita real por dia**, **Saldo em circulação** e **Contas que mais gastaram**. Se houver alertas abertos, um aviso no topo leva direto para eles. Botão **Ver extrato**. |
| **Financeiro → Extrato** | Todos os lançamentos. **Filtros**: **Conta**, **Tipo de ativo**, **Direção** (Crédito/Débito), **Categoria**, **De** / **Até**. Botão **Exportar CSV** para levar para a planilha. |
| **Financeiro → Receita** | Dinheiro real por período: **Receita real**, **Pedidos pagos**, **Ticket médio**, gráfico por dia e a tabela **Receita por gateway** (Gateway, **Moeda**, Pedidos pagos, **Total**, Ticket médio). Avisa quando há pedidos em moeda estrangeira sem taxa de câmbio fora do total. |
| **Financeiro → Economia** | Para cada moeda do jogo: **Entrada** (moeda entrando em circulação), **Saída** (moeda saindo) e **Fluxo líquido** no período, com filtro por **Categoria**, além do gráfico de **Oferta** (quanto existe ao longo do tempo). Entrada maior que saída por muito tempo significa inflação. |
| **Financeiro → Taxas de câmbio** | Cotações das moedas estrangeiras (ver passo 5). |
| **Financeiro → Alertas** | **Alertas de anomalia**: **Data**, **Conta**, **Ativo**, **Quantidade**, **Motivo** (ex.: **Ganho suspeito de moeda**) e **Status** (**Aberto**, **Revisado**, **Dispensado**). Filtros por **Conta** e **Status**. Botões **Marcar como revisado** e **Dispensar**. |
| **Financeiro → Eventos de pagamento** | Registro de cada aviso recebido dos meios de pagamento: **Data**, **Gateway**, **Pedido**, **Evento**, **Status** e **Mensagem**. Filtros por **Pedido**, **Gateway**, **Evento** e **Status**. |
| **Financeiro → Reconciliação** | Compara, sob demanda, o saldo gravado de cada carteira com a soma dos lançamentos dela. Lista as **Divergências** (**Conta**, **Carteira**, **Saldo real**, **Líquido do ledger**, **Diferença**) ou avisa que **Todas as carteiras estão reconciliadas**. |
| **Financeiro → Ajuste manual** | Credita ou debita o saldo de uma conta registrando um lançamento auditado: **Conta**, **Ativo**, **Direção** (Crédito/Débito), **Quantidade** (sempre positiva) e **Motivo** (obrigatório). Botão **Aplicar ajuste**. |

### Histórico financeiro na ficha da conta

Em **Contas**, ao abrir a ficha de um jogador, o botão **Histórico financeiro** (ao lado de **Logs** e **Baú**) mostra as últimas movimentações dele em todos os ativos, com atalho **Extrato completo** para o Extrato já filtrado por aquela conta. Na mesma ficha, os cards **Carteiras** e **Moedas** permitem **Depositar** e **Retirar** saldo diretamente.

---

## Como o sistema protege a sua economia

- **Valor conferido:** quando o meio de pagamento avisa que pagou, o sistema compara o valor informado com o valor do pedido. Na mesma moeda, tolera até R$ 0,01 de diferença; entre moedas diferentes, até 2% após a conversão. Se o valor divergir, o pedido **fica pendente** para você confirmar ou recusar manualmente em **Financeiro → Pedidos**, e o motivo aparece em **Eventos de pagamento**.
- **Crédito do valor do pedido:** o meio de pagamento credita o valor do pedido na carteira. Pagamentos em moeda estrangeira creditam o valor nominal do pedido.
- **Sem crédito duplicado:** confirmações repetidas do mesmo pagamento são ignoradas — cada pedido é creditado uma única vez. Todo crédito que poderia se repetir (pedidos, recompensas, cashback) tem proteção contra duplicidade.
- **Estornos revertidos:** se um pagamento é estornado ou contestado, o sistema desfaz o crédito daquele pedido (e as entregas ligadas a ele, como VIP ou cashback de cupom) e registra o reembolso no Extrato.
- **Avisos fora de ordem:** um aviso de "pago" que chega sobre um pedido já estornado ou cancelado é ignorado e fica registrado em **Eventos de pagamento**.
- **Alertas de anomalia:** o sistema acompanha o saldo das moedas do jogo e, quando uma conta ganha dentro do jogo um valor igual ou acima do **Limite de alerta de anomalia** da moeda, cria um alerta em **Financeiro → Alertas** e uma notificação no painel. Você decide se **Marcar como revisado** ou **Dispensar**.
- **Reconciliação sob demanda:** sempre que quiser, abra **Financeiro → Reconciliação** para conferir se os saldos das carteiras batem com os lançamentos.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|-----------------------|-----------------|
| Ativar um meio de pagamento, credenciais e **Taxa** | **Configurações → Gateways** |
| Carteira que recebe as doações e valores sugeridos | **Configurações → Doação** |
| Criar/ativar carteiras de crédito | **Configurações → Carteiras** |
| Cadastrar moedas do jogo e o **Limite de alerta de anomalia** | **Configurações → Moedas** |
| Tipos de VIP | **Configurações → Sistema VIP** |
| Contas para transferência bancária | **Configurações → Contas bancárias** |
| Cupons de desconto | Guia de Cupons |
| Ver, confirmar, recusar pedidos e abrir recibos | **Financeiro → Pedidos** |
| Aprovar comprovantes de transferência | **Financeiro → Pedidos**, botão **Confirmações de pagamento** |
| Cotações de moeda estrangeira | **Financeiro → Taxas de câmbio** |
| Resumo do período | **Financeiro → Painel** |
| Todos os lançamentos e exportação CSV | **Financeiro → Extrato** |
| Receita por meio de pagamento e moeda | **Financeiro → Receita** |
| Entrada/saída de moeda do jogo | **Financeiro → Economia** |
| Revisar ganhos suspeitos | **Financeiro → Alertas** |
| Conferir avisos dos meios de pagamento | **Financeiro → Eventos de pagamento** |
| Conferir se saldos e lançamentos batem | **Financeiro → Reconciliação** |
| Dar ou retirar saldo com motivo registrado | **Financeiro → Ajuste manual** |
| Ver o histórico de um jogador | **Contas → ficha da conta → Histórico financeiro** |

---

## Dicas e boas práticas

- **Ative só os meios de pagamento que você realmente usa.** Cada card ativo aparece para o jogador; menos opções confundem menos.
- **Use a Taxa com moderação.** Ela é somada ao total que o jogador paga e aparece na tela de pagamento ("+X% fee"); taxas altas derrubam a conversão.
- **Prefira o Ajuste manual a mexer direto nas carteiras** quando precisar corrigir algo: ele exige um motivo e fica no Extrato, o que facilita entender o histórico depois.
- **Olhe os Eventos de pagamento quando um jogador disser que pagou e não recebeu.** Ali você vê se o aviso chegou, se foi ignorado e por quê (valor divergente, pedido já processado etc.).
- **Mantenha as cotações atualizadas** se vende em mais de uma moeda; um clique em **Atualizar via API** resolve. Sem cotação, o pedido só fica fora do total consolidado da Receita.
- **Defina o Limite de alerta de anomalia em cada moeda.** É a sua rede de proteção contra exploits: um ganho fora do normal gera alerta e notificação no painel.
- **Exporte o Extrato em CSV** no fim do mês para a sua contabilidade.

---

## Perguntas frequentes

**O crédito chega na hora?**
Sim. Assim que o meio de pagamento confirma, os créditos entram na carteira. Boleto e transferência dependem da compensação ou da sua aprovação manual.

**O jogador pagou e não recebeu. O que fazer?**
Abra **Financeiro → Eventos de pagamento** e filtre pelo pedido. Se o aviso foi ignorado por valor divergente, o pedido está pendente em **Financeiro → Pedidos**: confira e use **Confirmar** ou **Recusar**. Se o aviso nem chegou, confira as credenciais do meio de pagamento em **Configurações → Gateways**.

**Preciso cadastrar cotação para receber em outra moeda?**
Não. O pagamento passa normalmente. A cotação só serve para somar aquele pedido ao total consolidado em **Financeiro → Receita**.

**Como funcionam os estornos?**
Se o meio de pagamento informa estorno ou contestação, o sistema reverte o crédito daquele pedido e desfaz o que foi entregue com ele. O reembolso aparece no Extrato e o evento fica registrado em **Eventos de pagamento**.

**Posso dar créditos ou moeda manualmente?**
Sim. Em **Financeiro → Ajuste manual** (com motivo obrigatório e registro no Extrato) ou direto na ficha da conta, pelos cards de Carteiras e Moedas.

**O que é o alerta de "Ganho suspeito de moeda"?**
Uma conta ganhou dentro do jogo um valor igual ou acima do limite que você definiu para aquela moeda. Investigue a conta e depois use **Marcar como revisado** ou **Dispensar**.

**A Reconciliação roda sozinha?**
Não. É uma tela de consulta: abra quando quiser conferir se o saldo gravado de cada carteira bate com os lançamentos. Se não houver divergência, ela avisa que todas as carteiras estão reconciliadas.

**Onde configuro cupons de desconto?**
Os cupons (percentual ou valor fixo, desconto máximo, pedido mínimo, usos por conta, quantidade, só primeira compra e escopo) têm guia próprio: veja o guia de Cupons.
