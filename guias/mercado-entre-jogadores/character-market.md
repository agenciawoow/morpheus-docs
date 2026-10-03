# Mercado de Personagens — Guia do Cliente

No painel, o card de configuração aparece como **Venda de personagens** e a lista de anúncios fica em **Mercado → Personagens**. Este guia explica, de forma simples, o que é o Mercado de Personagens, como o jogador vende e compra um personagem e como você configura e acompanha tudo pelo painel administrativo.

---

## O que é o Mercado de Personagens?

O Mercado de Personagens é a **loja oficial de compra e venda de personagens avulsos** do seu servidor. Diferente do Mercado de Contas, aqui o jogador vende **um personagem só**, e continua com a conta e os outros personagens. Quem compra recebe o personagem **na própria conta**, com inventário e equipamentos, assim que o pagamento é confirmado.

- Centraliza as negociações e **evita golpes** entre jogadores.
- O personagem é **transferido automaticamente** para a conta do comprador.
- Você pode cobrar uma **comissão** sobre cada venda, gerando receita para o servidor.

---

## Conceitos principais

### O anúncio

É o personagem colocado à venda. Tem uma **Descrição de venda** (o título do anúncio, com pelo menos 10 caracteres), um **Preço**, o **Tipo de chave PIX** e a chave **PIX** do vendedor (para receber o repasse) e um **Contato e-mail/telefone**.

Enquanto está anunciado, o personagem fica **bloqueado no jogo** (não consegue entrar) e **os serviços do painel sobre ele ficam trancados** (trocar nick, limpar inventário, transferir resets, mudar classe etc.). Assim o comprador paga exatamente pelo que viu no anúncio. A conta do vendedor e os outros personagens continuam livres.

Se o personagem tinha o perfil bloqueado (recurso do plugin de Perfil), esse bloqueio é **removido** no momento do anúncio, para o comprador conseguir ver o personagem.

### O que não pode ser anunciado

- Personagem **mestre de guild** (transfira a guild antes).
- Personagem já **bloqueado** no jogo.
- Personagem de uma conta que está **à venda** no Mercado de Contas.
- Personagem que **já está anunciado**.
- Com a conta **online** no jogo.

Se a conta inteira for colocada à venda no Mercado de Contas, os anúncios de personagens dela são **retirados automaticamente**.

### A comissão (Taxa)

Você define uma **taxa percentual** sobre o valor da venda. O comprador paga o preço cheio; o vendedor recebe o valor **menos a comissão**, que fica com o servidor. O jogador vê um aviso com a taxa antes de anunciar.

### O preço mínimo

Valor mínimo que o vendedor é obrigado a pedir, para evitar anúncios de valor simbólico. Deixe em 0 para não limitar.

### As situações do anúncio

- **Pendente** — anúncio ativo, disponível para compra.
- **Aguardando** — alguém iniciou o pagamento; o personagem fica reservado para esse comprador.
- **Pago** — o pagamento foi confirmado (na tela aparece como **Payed**).
- **Entregue** — o personagem foi transferido ao comprador.
- **Estornado** — o pagamento foi estornado depois da entrega (na tela aparece como **Refunded**).

Reservas de pagamento que não se concluem **expiram** depois do tempo configurado em **Minutos para expirar**, e o anúncio volta a ficar disponível.

### A entrega

Assim que o pagamento é confirmado, o sistema transfere o personagem para a conta do comprador automaticamente:

1. Move o personagem para a **conta do comprador**, ocupando uma vaga livre de personagem.
2. **Desbloqueia** o personagem no jogo.
3. Se **Remover itens** estiver ligado, esvazia o inventário do personagem antes de entregar.
4. Registra a venda no histórico das duas contas e envia uma mensagem ao comprador (quando o plugin de Mensagens está ativo).

O comprador precisa ter uma **vaga livre** de personagem na conta. Sem vaga, a compra não é aceita.

### O repasse ao vendedor

O valor do vendedor (preço menos a comissão) é repassado **por você**, fora do site, usando a chave PIX informada no anúncio. Depois de pagar, você marca o anúncio como pago na lista de pedidos para manter o controle.

### O estorno

Se o pagamento de um personagem já entregue for estornado pela forma de pagamento, o anúncio passa para **Estornado** e o ocorrido fica registrado no histórico da conta do vendedor. O personagem **não** volta automaticamente: a decisão fica com o seu suporte, caso a caso.

---

## Como o jogador usa

### Vendendo

1. No painel do jogador, ele escolhe o personagem e acessa **Vender personagem**.
2. Preenche **Descrição de venda**, **Preço**, **Tipo de chave PIX**, **PIX** e **Contato e-mail/telefone**. Todos são obrigatórios.
3. Confirma com o **ID pessoal** (a senha de segurança da conta). É preciso estar **fora do jogo**.
4. O personagem é bloqueado e o anúncio entra no mercado. Na página do personagem aparece o aviso "Este personagem está à venda": enquanto ninguém iniciou o pagamento, o vendedor pode **desistir** e o personagem é desbloqueado na hora.

### Comprando

1. O comprador abre a página de **Personagens** do Mercado no site. Pode **pesquisar**, filtrar por **Preço**, **Level**, **Resets**, **Master Resets** e **Classe** (quando o servidor tem esses recursos) e usar **Ordenar por**.
2. Clica em **Ver** para abrir o anúncio: vê classe, level, resets, atributos, pontos, zen, mapa, guild e o **inventário** do personagem.
3. Clica em **Comprar**, escolhe a forma de pagamento em **Pagar com ...** e conclui o pagamento. É preciso estar **logado**: o personagem vai para a conta que fez a compra.
4. Com o pagamento confirmado, o personagem aparece na conta do comprador. Basta entrar no jogo.

---

## Como configurar (passo a passo)

### 1. Configurar o mercado (uma vez)

1. Vá em **Configurações → Venda de personagens**.
2. No card **Configurações**, defina:
   - **Remover itens** — esvazia o inventário do personagem na entrega.
   - **Minutos para expirar** — tempo que uma reserva de pagamento pode ficar aberta (padrão 60).
   - **Taxa** — comissão em porcentagem.
   - **Preço mínimo** — valor mínimo de um anúncio (0 = sem mínimo).
3. No card **Gateways**, marque as formas de pagamento aceitas.
4. Clique em **Salvar**.

### 2. Acompanhar os pedidos

1. Vá em **Mercado → Personagens**. A tela **Pedidos** lista cada anúncio com #ID, **Personagem**, **Vendedor**, **Comprador**, **PIX**, **Preço**, **Comissão**, **A pagar**, **Criado em**, a situação, o número do **Pagamento** e a coluna **Pago**.
2. Use o campo de busca por personagem ou abra os filtros: **ID**, **Personagem**, **Vendedor**, **Comprador**, situação, **Data inicial** e **Data final**.
3. Depois que o personagem foi **Entregue**, faça o repasse ao vendedor e clique em **Pagar** na coluna **Pago**. A linha passa a mostrar a marca de pago.
4. Em anúncios entregues e pagos, o botão **Recibo** abre o comprovante do pagamento do comprador.

No topo da lista há os botões **Estatísticas** e **Configurações**.

### 3. Ver as estatísticas

Em **Estatísticas** você vê **Total de anúncios**, quantos estão **À venda**, o valor e a quantidade de personagens **Vendidos** e a **Comissão arrecadada**, além da tabela **Anúncios por situação**.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|------------------------|-----------------|
| Definir a comissão | **Configurações → Venda de personagens**, campo **Taxa** |
| Definir o preço mínimo de um anúncio | **Configurações → Venda de personagens**, campo **Preço mínimo** |
| Escolher as formas de pagamento | **Configurações → Venda de personagens**, card **Gateways** |
| Tempo para uma reserva de pagamento expirar | **Configurações → Venda de personagens**, campo **Minutos para expirar** |
| Esvaziar o inventário na entrega | **Configurações → Venda de personagens**, interruptor **Remover itens** |
| Ver e filtrar os anúncios | **Mercado → Personagens** |
| Registrar o repasse ao vendedor | **Mercado → Personagens**, botão **Pagar** na coluna **Pago** |
| Ver o comprovante do pagamento | **Mercado → Personagens**, botão **Recibo** |
| Ver o desempenho do mercado | **Mercado → Personagens**, botão **Estatísticas** |
| Liberar o serviço "Vender personagem" para os jogadores | **Configurações → Serviços**, serviço **Vender personagem** |

---

## Dicas e boas práticas

- Defina uma **Taxa** justa: cobre os custos da forma de pagamento e gera receita sem desestimular as vendas.
- Ajuste **Minutos para expirar** para liberar rápido anúncios de reservas abandonadas, sem cortar quem ainda está pagando.
- Ligue **Remover itens** se a política do servidor for vender só o personagem, sem os itens.
- Faça o repasse ao vendedor só depois que o anúncio estiver **Entregue** e marque **Pagar** em seguida, para nunca pagar duas vezes.
- O personagem anunciado fica bloqueado no jogo: avise os jogadores que, para jogar com ele de novo, basta **desistir** da venda.

---

## Perguntas frequentes

**O personagem anunciado some do ranking?**
Não. Ele continua no banco do jogo, só bloqueado para entrar. Os rankings seguem normais.

**O comprador pode escolher em qual conta receber?**
O personagem vai para a conta que está logada no momento da compra. Quem quiser receber em outra conta deve entrar com ela antes de comprar.

**O que acontece com a guild do personagem?**
Um mestre de guild não pode ser vendido. Um membro comum continua na guild depois da transferência, porque a guild é ligada ao nome do personagem.

**E se o comprador não tiver vaga de personagem?**
A compra não é aceita. O comprador precisa liberar uma vaga (ou o servidor aumentar o limite) e tentar de novo.

**O vendedor pode mexer no personagem enquanto está anunciado?**
Não. Ele não entra no jogo com esse personagem e os serviços do painel sobre ele ficam trancados até desistir da venda ou a venda concluir.
