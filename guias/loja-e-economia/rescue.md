# Resgates — Guia do Cliente

Este guia explica, de forma simples, o que é o sistema de Resgates, como o jogador usa e como você configura pelo painel administrativo. Não é necessário conhecimento técnico.

---

## O que são os Resgates?

Os Resgates permitem que o jogador **transforme o saldo de uma carteira do site em dinheiro de verdade**, recebido via **PIX**. É o caminho inverso da doação: em vez de colocar dinheiro para ganhar créditos, o jogador **saca** o saldo que acumulou (por exemplo, vendendo itens no mercado, ganhando prêmios ou recebendo comissões).

Na prática, é um **sistema de saque com aprovação manual**:

- O jogador pede o resgate informando o valor e a chave PIX.
- O valor é descontado da carteira na hora.
- Você faz o pagamento por fora e **marca o pedido como pago**, ou **recusa** e o valor volta para o jogador.

---

## Conceitos principais

### A carteira

Os créditos do jogador ficam em **carteiras** (por exemplo, "Créditos", "Bônus"). Você escolhe **quais carteiras podem ser resgatadas**. Só o saldo das carteiras liberadas pode virar PIX.

### A taxa

Você pode cobrar uma **taxa percentual** por carteira. Ela é descontada do valor solicitado: se o jogador pede R$ 100 com taxa de 10%, ele recebe R$ 90 (o **Total**). A diferença fica com o servidor.

### O valor mínimo

Cada carteira pode ter um **valor mínimo de resgate**. Pedidos abaixo desse valor são bloqueados na hora, com a mensagem "O valor mínimo de resgate é X".

### A chave PIX

O jogador informa o **tipo** de chave (E-mail, CPF, CNPJ, Telefone ou Chave aleatória) e a **chave** em si. O sistema valida o formato antes de aceitar. O tipo e a chave cadastrados na conta do jogador já vêm preenchidos.

### As situações do pedido

- **Pendente** — pedido aberto, esperando a sua ação.
- **Pago** — você confirmou o pagamento; o jogador recebeu.
- **Rejected** — pedido recusado; o valor foi **devolvido** para a carteira do jogador.

Na tela também existe a situação **Aguardando**, que só aparece em casos especiais e é tratada exatamente como **Pendente** (continua esperando confirmação ou recusa).

### Avisos por WhatsApp

Se o plugin **Sender** estiver configurado, o jogador recebe uma mensagem no WhatsApp quando solicita o resgate, quando o pedido é marcado como pago e quando é recusado.

---

## Como o jogador usa

1. No painel da conta, o jogador acessa **Resgates** e vê a lista **Solicitações de resgates** com os pedidos anteriores (valor, taxa, total, carteira, chave PIX, data e situação).
2. Clica em **Novo resgate**. A tela **Nova solicitação de resgate** mostra o saldo de cada carteira.
3. Escolhe a **Carteira** (a taxa aparece ao lado do nome quando existe), informa o **Valor**, o tipo de chave em **PIX Type** e a chave em **PIX**, e clica em **Request**.
4. Confirma com o **PID** (a senha pessoal de segurança da conta). Sem o PID correto, o pedido não é enviado.
5. O valor é descontado na hora e o pedido entra na lista como **Pendente**.
6. Quando você marca como pago, a situação vira **Pago**. Se você recusar, o valor volta para a carteira.

O sistema também bloqueia pedidos com **saldo insuficiente** ou de **carteira não liberada**.

---

## Como configurar (passo a passo)

### 1. Ajustar as configurações

1. Vá em **Configurações → Resgates**.
2. Em **Carteiras liberadas**, marque quais carteiras podem ser resgatadas.
3. (Opcional) No card **Minimum rescue**, informe o valor mínimo de resgate de cada carteira.
4. (Opcional) No card **Taxes**, informe a taxa percentual de cada carteira.
5. Clique em **Salvar**.

### 2. Acompanhar os pedidos

1. Vá em **Conteúdo → Resgates**. A lista mostra ID, **Conta**, **Valor**, **Taxa**, **Total**, **PIX**, **Criado em** e **Status**.
2. Use a busca por conta ou os filtros **ID**, **Conta**, **Status**, **Criado de** e **Criado até** para encontrar um pedido.
3. Faça o PIX para a chave informada, por fora do site.
4. Em cada pedido pendente, clique em **Confirmar** (marca como pago) ou **Reject** (recusa e devolve o valor). Os dois pedem uma confirmação antes de executar.

Se dois administradores tentarem processar o mesmo pedido, ou o botão for clicado duas vezes, só a primeira ação vale; a segunda mostra o aviso "Resgate já processado". Se um pedido tiver algum motivo de falha registrado, ele aparece como dica ao passar o mouse sobre o selo de situação.

### 3. Ver as estatísticas

Clique no botão **Estatísticas** no topo da lista. Você vê o **Total de solicitações**, quantas estão **Pendentes**, o total **Pago** aos jogadores e a **Taxa arrecadada**, além do quadro **Solicitações por status** com quantidade, valor solicitado e total de cada situação.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|------------------------|-----------------|
| Liberar carteiras para saque | **Configurações → Resgates**, card **Carteiras liberadas** |
| Definir valor mínimo por carteira | **Configurações → Resgates**, card **Minimum rescue** |
| Cobrar taxa de saque por carteira | **Configurações → Resgates**, card **Taxes** |
| Ver e filtrar os pedidos | **Conteúdo → Resgates** |
| Marcar como pago ou recusar | **Conteúdo → Resgates**, botões **Confirmar** e **Reject** em cada linha pendente |
| Abrir a conta do jogador | **Conteúdo → Resgates**, clique no nome da conta |
| Acompanhar desempenho | Botão **Estatísticas** no topo da lista de resgates |
| Avisar o jogador por WhatsApp | Configuração do plugin **Sender** |

---

## Dicas e boas práticas

- Defina uma **taxa** e um **valor mínimo** coerentes para evitar muitos saques pequenos e cobrir custos.
- Confira a **chave PIX** antes de pagar; o sistema valida o formato, mas não o dono da chave.
- Só clique em **Confirmar** depois de fazer o PIX. O botão apenas registra que o pagamento foi feito; ele não envia dinheiro.
- Recusar um pedido **devolve o valor** ao jogador automaticamente; não é preciso estornar à mão.
- Use o filtro **Status** = Pendente para ver só o que ainda precisa de ação.

---

## Perguntas frequentes

**O que o jogador recebe: o valor pedido ou o total?**
O **Total**, ou seja, o valor solicitado menos a taxa. Se não houver taxa, recebe o valor cheio.

**O valor sai da carteira na hora do pedido?**
Sim. O desconto é imediato. Se o pedido for recusado, o valor é devolvido.

**O site envia o PIX sozinho?**
Não. Você faz o pagamento por fora e depois clica em **Confirmar** para registrar que o pedido foi pago.

**Cliquei em Confirmar duas vezes. O jogador recebeu em dobro?**
Não. O segundo clique mostra "Resgate já processado" e nada muda.

**O que é o PID pedido na hora do resgate?**
É a senha pessoal de segurança da conta. Serve para confirmar que é mesmo o dono pedindo o saque.

**Posso resgatar qualquer carteira?**
Só as que você marcar em **Carteiras liberadas** nas configurações.

**O jogador é avisado quando o pedido muda?**
Sim, por WhatsApp, desde que o plugin **Sender** esteja configurado. Ele recebe aviso ao solicitar, ao ser pago e ao ser recusado.
