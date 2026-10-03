# Mercado de Contas — Guia do Cliente

No painel, o card de configuração aparece como **Venda de contas** e a lista de anúncios fica em **Mercado → Contas**. Este guia explica, de forma simples, o que é o Mercado de Contas, como o jogador vende e compra uma conta e como você configura e acompanha tudo pelo painel administrativo.

---

## O que é o Mercado de Contas?

O Mercado de Contas é a **loja oficial de compra e venda de contas** do seu servidor. Em vez de negociações por fora, arriscadas e sem controle, o jogador **anuncia a própria conta** pelo site e outro jogador **compra com segurança**, pagando pelas formas de pagamento que você já usa no site.

- Centraliza as negociações e **evita golpes** entre jogadores.
- A conta é **transferida automaticamente** ao comprador assim que o pagamento é confirmado.
- Você pode cobrar uma **comissão** sobre cada venda, gerando receita para o servidor.

---

## Conceitos principais

### O anúncio

É a conta colocada à venda. Tem uma **Descrição de venda** (o título do anúncio, com pelo menos 10 caracteres), um **Preço**, o **Tipo de chave PIX** e a chave **PIX** do vendedor (para receber o repasse) e um **Contato e-mail/telefone**. Enquanto está anunciada, a conta fica **bloqueada**: o vendedor não consegue entrar no jogo com ela.

Ao anunciar, os personagens da conta ficam visíveis para quem está comprando. Por isso, se algum personagem tinha o perfil bloqueado (recurso do plugin de Perfil), esse bloqueio é **removido** no momento do anúncio.

### A comissão (Taxa)

Você define uma **taxa percentual** sobre o valor da venda. O comprador paga o preço cheio; o vendedor recebe o valor **menos a comissão**, que fica com o servidor. O jogador vê um aviso com a taxa antes de anunciar.

### O preço mínimo

Valor mínimo que o vendedor é obrigado a pedir, para evitar anúncios de valor simbólico. Deixe em 0 para não limitar.

### As situações do anúncio

- **Pendente** — anúncio ativo, disponível para compra.
- **Aguardando** — alguém iniciou o pagamento; a conta fica reservada para esse comprador.
- **Pago** — o pagamento foi confirmado (na tela aparece como **Payed**).
- **Entregue** — a conta foi transferida ao comprador.
- **Estornado** — o pagamento foi estornado depois da entrega (na tela aparece como **Refunded**).

Reservas de pagamento que não se concluem **expiram** depois do tempo configurado em **Minutos para expirar**, e o anúncio volta a ficar disponível.

### A entrega

Assim que o pagamento é confirmado, o sistema transfere a conta ao comprador automaticamente:

1. **Desbloqueia** a conta e desliga a autenticação em dois fatores.
2. **Apaga os dados do dono anterior**: nome, telefone, documento, chave PIX, pergunta e resposta secreta, ID pessoal e logins sociais. Isso impede o vendedor de recuperar a conta depois.
3. Gera uma **nova senha**, desconecta quem estiver logado e envia os dados de acesso por **e-mail** ao comprador.
4. Se **Alterar e-mail** estiver ligado, o e-mail da conta passa a ser o e-mail usado no pagamento.
5. Se **Remover itens** estiver ligado, esvazia o baú, os baús extras e o inventário de todos os personagens.

### O repasse ao vendedor

O valor do vendedor (preço menos a comissão) é repassado **por você**, fora do site, usando a chave PIX informada no anúncio. Depois de pagar, você marca o anúncio como pago na lista de pedidos para manter o controle.

### O estorno

Se o pagamento de uma conta já entregue for estornado pela forma de pagamento, o anúncio passa para **Estornado** e o ocorrido fica registrado no histórico da conta. A conta **não** é devolvida automaticamente ao vendedor: a decisão fica com o seu suporte, caso a caso.

---

## Como o jogador usa

### Vendendo

1. No painel do jogador, ele acessa **Vender minha conta**.
2. Preenche **Descrição de venda**, **Preço**, **Tipo de chave PIX**, **PIX** e **Contato e-mail/telefone**. Todos são obrigatórios.
3. Confirma com o **ID pessoal** (a senha de segurança da conta). É preciso estar **fora do jogo**.
4. A conta é bloqueada e o anúncio entra no mercado. Na página de informações da conta aparece o aviso "Sua conta está sendo vendida, caso queira desistir clique aqui": enquanto ninguém iniciou o pagamento, o vendedor pode **desistir** e a conta é desbloqueada na hora.

Cada conta só pode ter **um anúncio pendente** por vez.

### Comprando

1. O comprador abre a página de **Contas** do Mercado no site. Pode **pesquisar**, filtrar por **Preço**, **Level**, **Resets**, **Master Resets** e **Vip** (quando o servidor tem esses recursos) e usar **Ordenar por** (menor/maior preço, level, resets, master resets).
2. Clica em **Ver** para abrir o anúncio: vê o tipo de conta, a maturidade, o **baú** e cada **personagem** com atributos, level, resets, pontos, zen, mapa e guild.
3. Clica em **Comprar**, escolhe a forma de pagamento em **Pagar com ...** e conclui o pagamento. Não é preciso estar logado para comprar.
4. Com o pagamento confirmado, recebe por e-mail o usuário e a nova senha.

### Primeiro acesso do comprador

No primeiro login com a conta comprada, o comprador é levado para a tela **Configure sua conta comprada** e não consegue usar o painel antes de concluí-la. Ali ele define os próprios dados: **Nome**, **Telefone**, **Documento**, **Tipo de chave PIX**, **PIX**, **Pergunta secreta** e **Resposta secreta**, e clica em **Salvar e usar a conta**.

---

## Como configurar (passo a passo)

### 1. Configurar o mercado (uma vez)

1. Vá em **Configurações → Venda de contas**.
2. No card **Configurações**, defina:
   - **Remover itens** — esvazia baús e inventários na entrega.
   - **Alterar e-mail** — troca o e-mail da conta pelo e-mail do pagamento.
   - **Minutos para expirar** — tempo que uma reserva de pagamento pode ficar aberta (padrão 60).
   - **Taxa** — comissão em porcentagem.
   - **Preço mínimo** — valor mínimo de um anúncio (0 = sem mínimo).
3. No card **Gateways**, marque as formas de pagamento aceitas.
4. Clique em **Salvar**.

### 2. Acompanhar os pedidos

1. Vá em **Mercado → Contas**. A tela **Pedidos** lista cada anúncio com #ID, **Conta**, **PIX**, **Contato**, **Preço**, **Comissão**, **A pagar**, **Criado em**, a situação, o número do **Pagamento** e a coluna **Pago**.
2. Use o campo de busca por conta ou abra os filtros: **ID**, **Conta**, situação, **Data inicial** e **Data final**.
3. Depois que a conta foi **Entregue**, faça o repasse ao vendedor e clique em **Pagar** na coluna **Pago**. A linha passa a mostrar a marca de pago.
4. Em anúncios entregues e pagos, o botão **Recibo** abre o comprovante do pagamento do comprador.

No topo da lista há os botões **Estatísticas** e **Configurações**.

### 3. Ver as estatísticas

Em **Estatísticas** (botão no topo da lista) você vê **Total de anúncios**, quantos estão **À venda**, o valor e a quantidade de contas **Vendidas** e a **Comissão arrecadada**, além da tabela **Anúncios por situação** com quantidade e total por situação.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|------------------------|-----------------|
| Definir a comissão | **Configurações → Venda de contas**, campo **Taxa** |
| Definir o preço mínimo de um anúncio | **Configurações → Venda de contas**, campo **Preço mínimo** |
| Escolher as formas de pagamento | **Configurações → Venda de contas**, card **Gateways** |
| Tempo para uma reserva de pagamento expirar | **Configurações → Venda de contas**, campo **Minutos para expirar** |
| Esvaziar itens na entrega | **Configurações → Venda de contas**, interruptor **Remover itens** |
| Trocar o e-mail da conta na entrega | **Configurações → Venda de contas**, interruptor **Alterar e-mail** |
| Ver e filtrar os anúncios | **Mercado → Contas** |
| Registrar o repasse ao vendedor | **Mercado → Contas**, botão **Pagar** na coluna **Pago** |
| Ver o comprovante do pagamento | **Mercado → Contas**, botão **Recibo** |
| Ver o desempenho do mercado | **Mercado → Contas**, botão **Estatísticas** no topo |

---

## Dicas e boas práticas

- Defina uma **Taxa** justa: cobre os custos da forma de pagamento e gera receita sem desestimular as vendas.
- Ajuste **Minutos para expirar** para liberar rápido anúncios de reservas abandonadas, sem cortar quem ainda está pagando.
- Ligue **Remover itens** e **Alterar e-mail** conforme a sua política de segurança na transferência.
- Faça o repasse ao vendedor só depois que o anúncio estiver **Entregue** e marque **Pagar** em seguida, para nunca pagar duas vezes.
- Acompanhe as **Estatísticas** para entender o volume e a receita do mercado.

---

## Perguntas frequentes

**O vendedor pode jogar com a conta enquanto ela está à venda?**
Não. A conta fica **bloqueada** durante o anúncio. Se ele desistir antes de alguém iniciar o pagamento, a conta é desbloqueada na hora.

**Quanto o vendedor recebe e como?**
O preço do anúncio **menos a comissão**. O repasse é feito por você, pela chave PIX do anúncio; depois marque o pedido como pago na lista.

**O que acontece se o comprador não concluir o pagamento?**
A reserva **expira** após os **Minutos para expirar** e o anúncio volta a ficar disponível para outros compradores.

**Por que pedir o ID pessoal e exigir estar fora do jogo para vender?**
Por segurança: confirma que é o dono da conta e evita conflitos com a conta em uso no jogo.

**A conta entregue vem com os itens?**
Depende de **Remover itens**: ligado, baús e inventários são esvaziados na entrega; desligado, tudo vai junto com a conta.

**O vendedor consegue recuperar a conta depois de vendida?**
Não. Na entrega, senha, pergunta secreta, PIX, documento, telefone, ID pessoal e logins sociais do dono anterior são apagados, e o comprador define os próprios dados no primeiro acesso.

**O que acontece em um estorno?**
O anúncio passa para **Estornado** e o caso fica registrado no histórico da conta para o seu suporte avaliar. A conta não é devolvida automaticamente.

**Posso ter mais de um anúncio da mesma conta?**
Não. Cada conta só pode ter **um anúncio pendente** por vez.
