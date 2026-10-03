# Streamers — Guia do Cliente

Este guia explica, de forma simples, o que é o sistema de Streamers, como o jogador participa e como você configura tudo pelo painel administrativo. Não é necessário conhecimento técnico.

---

## O que é o sistema de Streamers?

O sistema de Streamers transforma criadores de conteúdo da **Twitch** em **parceiros do seu servidor**. Ele tem duas frentes:

1. **Vitrine de lives:** os streamers parceiros que estiverem **ao vivo** aparecem automaticamente no site, levando audiência para o jogo.
2. **Programa de afiliados:** cada streamer aceito recebe um **link curto de convite**. Quem se cadastra por esse link fica vinculado ao streamer, e o streamer ganha **cashback** sobre as doações dessas pessoas.

É uma ferramenta de **marketing e divulgação**: incentiva criadores a promoverem o servidor em troca de visibilidade e recompensa.

---

## Conceitos principais

### A solicitação

O jogador pede para virar streamer informando o **Usuário no Twitch**. A solicitação entra como **pendente** e você decide **Aceitar** ou **Rejeitar** no painel. Cada conta só pode ter uma solicitação.

### O afiliado e o link curto de convite

Depois de aceitar um streamer, você define na tela **Afiliado** o **Link** (um código curto, único por streamer) e o **Cashback** (porcentagem). O site monta com esse código um **link curto de convite**, que o streamer copia na própria conta e divulga. Quem acessa esse link e **se cadastra** fica automaticamente **indicado** por aquele streamer.

### O cashback

Sempre que uma pessoa **indicada** faz uma doação que é **confirmada como paga**, o streamer recebe automaticamente a porcentagem de cashback, calculada sobre o **total do pedido**, na **carteira** que você escolheu. O cashback só é pago se houver uma carteira configurada e se a porcentagem do streamer for maior que zero.

### As lives ao vivo

O site consulta a Twitch e mostra os streamers parceiros que estão **ao vivo** naquele momento, num bloco **LIVE** visível em todas as páginas. Você pode informar uma **Tag** para mostrar só as lives marcadas com a tag do seu servidor.

---

## Como o jogador usa

- **Para virar streamer:** em **Minha conta**, no bloco **Streamer**, clica em **Solicitar**, informa o **Usuário no Twitch** (o nome de usuário, não o endereço do canal) e aguarda. O bloco passa a mostrar a situação da solicitação: **pendente**, **aceita** ou **rejeitada**.
- **Depois de aceito:** no mesmo bloco aparecem o **Link de convite** com botão **Copiar**, a quantidade de **Indicações** e o **Cashback** definido. Em **Convites** ele vê cada indicado, quanto já **Doado** e quanto rendeu de **Cashback**.
- **Para o público:** vê a vitrine de **LIVE** no site e pode entrar nas transmissões.

---

## Como configurar (passo a passo)

### 1. Configurar o cashback e a Twitch (uma vez)

Vá em **Configurações → Streamers** (ou use o botão **Configurações** no topo da lista de streamers). A tela tem dois cards, nesta ordem:

1. **Cashback:** escolha a **Carteira** que vai receber o cashback dos streamers. Sem carteira escolhida, nenhum cashback é pago.
2. **Twitch:** informe o **Client ID** e o **Client Secret** do seu aplicativo na Twitch, clique em **Gerar token** (o campo **Token** é preenchido automaticamente) e, se quiser, informe uma **Tag** para filtrar as lives.
3. Clique em **Salvar**.

Para gerar o token, o **Client ID** e o **Client Secret** precisam estar salvos. Caso contrário, o painel avisa.

### 2. Aprovar streamers

1. Vá em **Conteúdo → Streamers → Solicitações**. O menu mostra quantas solicitações estão **pendentes**.
2. A lista traz **Conta**, **Twitch**, **Cashback**, **Link**, **Criado em** e **Status**.
3. Em cada linha, use **Aceitar** ou **Rejeitar** (o painel pede confirmação).
4. Depois de aceitar, clique em **Afiliado** na mesma linha e preencha o **Link** (obrigatório e único) e o **Cashback** em porcentagem. Salve.

### 3. Acompanhar o desempenho

Clique em **Estatísticas**, no topo da lista. A tela mostra **Total de streamers**, **Aceitos**, **Pendentes** e **Total de indicações**, além da tabela **Desempenho dos afiliados** com conta, Twitch, cashback, número de **Indicações** e total **Doado** pelos indicados.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|------------------------|-----------------|
| Escolher a carteira do cashback | **Configurações → Streamers** → card **Cashback** → **Carteira** |
| Conectar à Twitch | **Configurações → Streamers** → card **Twitch** → **Client ID**, **Client Secret** e **Gerar token** |
| Filtrar as lives por tag | **Configurações → Streamers** → card **Twitch** → **Tag** |
| Aprovar ou rejeitar solicitações | **Conteúdo → Streamers → Solicitações** → botões **Aceitar** / **Rejeitar** |
| Definir o link curto e o cashback de um streamer | **Conteúdo → Streamers → Solicitações** → botão **Afiliado** na linha |
| Ver o desempenho dos afiliados | **Conteúdo → Streamers → Solicitações** → botão **Estatísticas** no topo |
| Abrir a ficha da conta do streamer | Clique no nome da conta na lista de solicitações |

---

## Dicas e boas práticas

- Combine uma **porcentagem de cashback** atrativa para o streamer e sustentável para o servidor.
- Use a **Tag** para garantir que só apareçam lives realmente sobre o seu servidor.
- Se as lives pararem de aparecer, abra **Configurações → Streamers** e clique em **Gerar token** novamente.
- Escolha a **Carteira** antes de aceitar o primeiro streamer. Doações pagas antes disso não geram cashback.
- Acompanhe as **Estatísticas** para identificar os afiliados que mais trazem doações e fortalecer a parceria.

---

## Perguntas frequentes

**O streamer precisa estar ao vivo para aparecer no site?**
Sim. A vitrine mostra apenas os parceiros aceitos que estão **ao vivo** na Twitch naquele momento.

**Como uma pessoa fica vinculada a um streamer?**
Ao **se cadastrar** depois de abrir o link curto de convite do streamer. O vínculo só acontece no cadastro: contas já existentes não ficam vinculadas.

**Quando o cashback é pago?**
Automaticamente, sempre que uma doação de um indicado é **confirmada como paga**. O valor é a porcentagem sobre o total do pedido e cai na carteira configurada.

**Posso mudar a porcentagem de cashback depois?**
Sim, na tela **Afiliado** do streamer. A nova porcentagem vale para as doações pagas a partir daí.

**O jogador pode enviar mais de uma solicitação?**
Não. Cada conta tem uma única solicitação, e o site avisa se já existir uma.

**Posso rejeitar um streamer que já foi aceito?**
Sim. O botão **Rejeitar** continua disponível enquanto a solicitação não estiver rejeitada.
