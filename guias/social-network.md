# Login social (Social Network) — Guia do Cliente

No painel, este recurso aparece como **Social Network**. Este guia explica, de forma simples, o que é o login social, como o jogador usa e como você configura pelo painel administrativo. Não é necessário conhecimento técnico.

---

## O que é o login social?

O login social deixa o jogador **entrar no site com a conta do Facebook ou do Google**, sem precisar digitar usuário e senha. Agiliza o acesso e reduz a barreira para novos jogadores.

É uma ferramenta de **conveniência e conversão**: quanto mais fácil entrar, mais jogadores criam conta e voltam.

---

## Conceitos principais

### Os provedores

O plugin suporta **Facebook** e **Google**. Para cada um, você liga ou desliga o login pelo interruptor **Ativo** e informa as credenciais do seu aplicativo: **Client ID** e **Client Secret**.

### Client ID e Client Secret

São as credenciais que autorizam o seu site a usar o login do Facebook ou do Google. Você as gera **uma vez** no painel de desenvolvedor de cada serviço e cola no painel do Morpheus.

### O vínculo

Cada conta do jogo pode ficar **vinculada** a uma conta do Facebook e a uma do Google. É esse vínculo que permite entrar sem senha nas próximas vezes. O jogador vê e controla os vínculos na própria conta, no site.

---

## Como o jogador usa

### Entrar pelo site

1. Na tela de login, abaixo da opção de cadastro, o jogador vê os botões **Facebook** e/ou **Google** (apenas os provedores que você ativou).
2. Ao clicar, autoriza o acesso na janela do provedor.
3. O que acontece em seguida depende da situação da conta:
   - **Já existe vínculo** com aquele Facebook/Google: o jogador entra direto.
   - **Não existe vínculo, mas o e-mail** da conta social é o mesmo de uma conta do jogo: o site cria o vínculo automaticamente e o jogador entra.
   - **Nenhum dos dois:** o jogador cai na tela de **cadastro já pré-preenchida** com nome e e-mail vindos do provedor. Ao concluir o cadastro, a nova conta nasce vinculada àquela rede social.

### Conectar e desconectar na conta

Na área **Minha conta**, o jogador encontra o bloco **Social login**, que lista cada provedor ativo com a situação **Conectado** ou **Não conectado**:

- **Conectar:** abre a autorização do provedor e cria o vínculo com a conta atual.
- **Desconectar:** pede confirmação e remove o vínculo. Depois disso, aquele Facebook/Google não entra mais nessa conta até ser conectado de novo.

---

## Como configurar (passo a passo)

Tudo é feito em **Configurações → Social Network**.

1. No painel de desenvolvedor do **Google** e/ou do **Facebook**, crie um aplicativo e obtenha o **Client ID** e o **Client Secret**. Ao criar o aplicativo, informe o endereço do seu site como endereço autorizado de retorno do login, conforme pedido pelo próprio provedor.
2. Em **Configurações → Social Network**, no card **Facebook**, ligue **Ativo** e preencha **Client ID** e **Client Secret**.
3. No card **Google**, faça o mesmo.
4. Clique em **Salvar**.

Os botões aparecem na tela de login assim que pelo menos um provedor estiver com **Ativo** ligado.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|------------------------|-----------------|
| Ativar ou desativar o login com Facebook | **Configurações → Social Network** → card **Facebook** → interruptor **Ativo** |
| Ativar ou desativar o login com Google | **Configurações → Social Network** → card **Google** → interruptor **Ativo** |
| Informar as credenciais do Facebook | Card **Facebook** → campos **Client ID** e **Client Secret** |
| Informar as credenciais do Google | Card **Google** → campos **Client ID** e **Client Secret** |
| Ver se uma conta está vinculada | Na área **Minha conta** do jogador, bloco **Social login** (Conectado / Não conectado) |

---

## Dicas e boas práticas

- Guarde o **Client Secret** com cuidado. Ele autoriza o login em nome do seu site.
- Ative só os provedores que você realmente vai oferecer, para não exibir botões que não funcionam.
- Oriente o jogador a usar no Facebook/Google o **mesmo e-mail** da conta do jogo. Assim o vínculo é criado sozinho na primeira entrada.
- Se o provedor mudar as credenciais do aplicativo, atualize os campos no painel. Com credenciais antigas o login falha.

---

## Perguntas frequentes

**Quais redes são suportadas?**
**Google** e **Facebook**.

**Preciso de uma conta de desenvolvedor?**
Sim. O **Client ID** e o **Client Secret** são gerados no painel de desenvolvedor de cada serviço.

**O jogador ainda pode entrar com usuário e senha?**
Sim. O login social é **opcional**, uma forma adicional de entrar.

**O jogador já tem conta no jogo, mas nunca usou o login social. O que acontece?**
Se o e-mail do Facebook/Google for o mesmo da conta do jogo, o site vincula automaticamente e ele entra. Se o e-mail for diferente, ele cai na tela de cadastro. Nesse caso, basta entrar com usuário e senha e usar **Conectar** em **Minha conta** para vincular.

**Como o jogador troca a rede social vinculada?**
Em **Minha conta**, bloco **Social login**, clica em **Desconectar** e depois em **Conectar** com a outra conta.

**Como desativo um provedor?**
Desligue **Ativo** no card do provedor em **Configurações → Social Network** e salve. O botão some da tela de login e do bloco **Social login**.
