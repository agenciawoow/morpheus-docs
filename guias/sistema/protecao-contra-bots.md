# Proteção contra bots (reCAPTCHA e Turnstile) — Guia do Cliente

No painel, os dois plugins aparecem como **reCAPTCHA** (Google) e **Turnstile** (Cloudflare), dentro de **Configurações → Acessos**. Este guia explica, de forma simples, **o que eles fazem**, **qual escolher**, **onde conseguir as chaves** e **como configurar** pelo painel administrativo. Não é necessário nenhum conhecimento técnico.

---

## O que é a proteção contra bots?

Robôs automatizados tentam criar centenas de contas falsas, disparar pedidos de recuperação de senha e adivinhar senhas. Um **desafio anti-bot** (CAPTCHA) confirma que quem está preenchendo o formulário é uma pessoa de verdade antes de o site aceitar o envio.

O Morpheus oferece dois plugins para isso, e você usa **um ou outro**:

- **Google reCAPTCHA** — versão invisível, baseada em pontuação: o jogador não vê nada; o Google avalia o comportamento e dá uma nota de 0,0 (robô) a 1,0 (humano). Você define a nota mínima para aceitar o envio.
- **Cloudflare Turnstile** — mostra um pequeno bloco no formulário que normalmente se resolve sozinho (um "visto" aparece em um segundo); em casos suspeitos, pede uma interação simples. Não usa quebra-cabeças de imagens.

Benefícios:

- Menos contas falsas e menos spam de "esqueci a senha".
- Menos trabalho de limpeza no painel e menos custo de e-mail.
- Experiência do jogador praticamente sem atrito (nenhum dos dois pede para "selecionar semáforos").

---

## Qual escolher?

| | **reCAPTCHA (Google)** | **Turnstile (Cloudflare)** |
|---|---|---|
| O que o jogador vê | Nada (invisível) | Um pequeno bloco que se resolve sozinho |
| Como decide | Pontuação de 0,0 a 1,0; você escolhe a nota mínima | Aprovado/reprovado, sem nota para ajustar |
| Onde pegar as chaves | Conta Google, no site do reCAPTCHA | Conta Cloudflare (gratuita) |
| Indicado quando | Você quer zero elemento visual e aceita ajustar a nota mínima | Você já usa Cloudflare no domínio ou prefere algo mais simples de configurar |

Os dois funcionam em qualquer servidor. Se não tiver preferência, o **Turnstile** é o mais simples: não exige ajuste de pontuação e não depende dos serviços do Google (bloqueados em algumas redes).

> ⚠️ **Ative apenas um dos dois.** Com os dois plugins ativos ao mesmo tempo, o formulário exibe só o reCAPTCHA, mas o site passa a exigir a confirmação dos dois — e o envio sempre falha com "Captcha inválido".

---

## Em quais telas o jogador passa pelo desafio

| Tela do site | Como aparece |
|--------------|--------------|
| **Cadastro** (criar conta) | Verificado antes de criar a conta. Com o Turnstile, o bloco aparece logo acima dos termos de uso; com o reCAPTCHA, nada é exibido. |
| **Esqueci a senha** (recuperação de senha) | Verificado antes de enviar o e-mail de recuperação. Com o Turnstile, o bloco aparece abaixo do campo de e-mail. |

Se a verificação falhar, o jogador vê a mensagem **Captcha inválido** e pode tentar de novo.

---

## O que acontece se nenhum plugin estiver configurado

Mesmo sem reCAPTCHA ou Turnstile, o site mantém proteções básicas por volume:

- **Login:** depois de um número de tentativas erradas (campo **Máximo de tentativas**), a conta e o endereço de origem ficam bloqueados pelo tempo definido em **Duração do bloqueio (segundos)**. O jogador vê a mensagem de conta temporariamente bloqueada. Esses dois campos ficam em **Configurações → Acessos → Login**, bloco **Proteção contra força bruta**.
- **Esqueci a senha:** há um teto de pedidos por endereço de origem dentro da mesma janela de bloqueio (5 pedidos); acima disso o site recusa o pedido ("Too many requests, please try again later.") e o jogador precisa esperar. O e-mail de recuperação só vai para o endereço já cadastrado na conta.
- **Cadastro:** sem um plugin ativo, o formulário de cadastro não tem desafio anti-bot — só as validações normais (e-mail único, termos de uso, confirmação de e-mail se você ligou essa opção). Por isso, se o seu servidor sofre com contas falsas, ative um dos dois plugins.

---

## Como configurar (passo a passo)

### Opção A — Google reCAPTCHA

**1. Obtenha as chaves no Google**

1. Acesse o site do Google reCAPTCHA com uma conta Google (o próprio painel tem o link **Register keys** no topo do bloco de chaves).
2. Registre um novo site: dê um nome, escolha o tipo **reCAPTCHA v3** (baseado em pontuação — é o único que o plugin usa) e informe o **domínio** do seu site (ex.: `meuservidor.com`). Se você usa mais de um domínio ou subdomínio, adicione todos.
3. Ao concluir, o Google mostra duas chaves: a **Chave do site** (pública) e a **Chave secreta**. Guarde as duas.

**2. Ative o plugin**

Em **Plugins**, ative o **Google reCAPTCHA**.

**3. Preencha no painel**

1. Abra **Configurações → Acessos → reCAPTCHA** (a tela chama-se **ReCaptcha plugin settings**).
2. No bloco **Keys**, preencha:
   - **Site key** — a chave do site (pública);
   - **Secret key** — a chave secreta;
   - **Minimum score** — a nota mínima de 0,0 a 1,0 para aceitar o envio ("Score from 0.0 (bot) to 1.0 (human). Recommended: 0.5"). Comece com **0.5**.
3. Clique em **Salvar**.

**4. Teste**

Abra a página de cadastro do site em uma janela anônima e crie uma conta de teste. Nada deve aparecer no formulário, e o cadastro deve concluir normalmente.

> 💡 Se jogadores legítimos começarem a receber "Captcha inválido" no cadastro, diminua o **Minimum score** (ex.: 0.3). Se contas falsas continuarem passando, aumente (ex.: 0.7).

### Opção B — Cloudflare Turnstile

**1. Obtenha as chaves na Cloudflare**

1. Entre no painel da Cloudflare (a conta gratuita basta; o domínio **não** precisa estar hospedado na Cloudflare). O próprio painel do Morpheus tem o link **Register keys** para a página do Turnstile.
2. No menu da Cloudflare, abra **Turnstile** e clique em adicionar um widget (site).
3. Dê um nome, informe o **domínio** do seu site e escolha o modo **Managed** (gerenciado — o padrão).
4. Ao concluir, a Cloudflare mostra a **Site Key** e a **Secret Key**. Guarde as duas.

**2. Ative o plugin**

Em **Plugins**, ative o **Cloudflare Turnstile**.

**3. Preencha no painel**

1. Abra **Configurações → Acessos → Turnstile** (a tela chama-se **Turnstile plugin settings**).
2. No bloco **Keys**, preencha **Site key** e **Secret key**.
3. Clique em **Salvar**.

**4. Teste**

Abra a página de cadastro em uma janela anônima: o bloco do Turnstile deve aparecer acima dos termos de uso e mostrar o "visto" sozinho em instantes. Conclua um cadastro de teste.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|-----------------------|-----------------|
| Ativar/desativar o plugin do Google | **Plugins** → **Google reCAPTCHA** |
| Informar as chaves do Google e a nota mínima | **Configurações → Acessos → reCAPTCHA** → **Site key**, **Secret key**, **Minimum score** |
| Ativar/desativar o plugin da Cloudflare | **Plugins** → **Cloudflare Turnstile** |
| Informar as chaves da Cloudflare | **Configurações → Acessos → Turnstile** → **Site key**, **Secret key** |
| Ir para a página de cadastro de chaves | Link **Register keys** no topo do bloco **Keys** de cada tela |
| Limitar tentativas de login e tempo de bloqueio | **Configurações → Acessos → Login** → **Proteção contra força bruta** → **Máximo de tentativas**, **Duração do bloqueio (segundos)** |
| Exigir confirmação de e-mail no cadastro (reforço contra contas falsas) | **Configurações → Acessos → Cadastro** → **Email confirmation** |

---

## Dicas e boas práticas

- **Um plugin só.** Nunca deixe reCAPTCHA e Turnstile ativos ao mesmo tempo (veja o aviso acima).
- **Chaves do domínio certo.** Se o site responde em `www.meuservidor.com` e `meuservidor.com`, cadastre os dois domínios no Google ou na Cloudflare; chave de domínio errado gera "Captcha inválido" para todo mundo.
- **Nunca compartilhe a chave secreta.** Só a **Site key** é pública. Se a secreta vazar, gere um novo par no Google/Cloudflare e atualize no painel.
- **Teste em janela anônima** após salvar — assim você vê exatamente o que um jogador novo vê.
- **Comece com a nota 0.5 no reCAPTCHA** e ajuste pelos resultados: menos falsos positivos (jogadores reais barrados) para baixo, mais rigor para cima.
- **Combine com a confirmação de e-mail** em **Configurações → Acessos → Cadastro** para cortar contas falsas que passem pelo desafio.
- **Tema personalizado?** O desafio aparece onde o formulário de cadastro e o de recuperação de senha do tema o incluem. Se o seu tema foi feito sob medida e o bloco não aparece, peça a quem o mantém para incluir o desafio nesses formulários.

---

## Perguntas frequentes

**Preciso dos dois plugins?**
Não — é um **ou** outro. Os dois ativos ao mesmo tempo quebram o cadastro e a recuperação de senha.

**O jogador vai ter que "clicar em semáforos"?**
Não. O reCAPTCHA usado é invisível (por pontuação) e o Turnstile normalmente se resolve sozinho sem interação.

**Jogadores reais estão recebendo "Captcha inválido". O que fazer?**
Primeiro confira se o domínio cadastrado nas chaves é o mesmo do site e se só um plugin está ativo. No reCAPTCHA, reduza o **Minimum score**. Se persistir, gere um novo par de chaves e salve de novo.

**O desafio aparece na tela de login?**
Não. O login é protegido pelo bloqueio por tentativas (**Máximo de tentativas** e **Duração do bloqueio (segundos)**), que funciona com ou sem os plugins.

**Posso usar o Turnstile sem hospedar o DNS na Cloudflare?**
Sim. Basta uma conta Cloudflare gratuita; o widget do Turnstile funciona em qualquer domínio.

**Desativei o plugin. O que muda?**
O desafio some do cadastro e da recuperação de senha na hora, e continuam valendo apenas as proteções por volume (bloqueio de login e teto de pedidos de recuperação). As chaves ficam salvas para quando você reativar.

**Isso afeta a velocidade do site?**
Não de forma perceptível. O desafio carrega junto com a página e a verificação leva uma fração de segundo no envio do formulário.

---

> Ficou em dúvida sobre qual escolher ou onde pegar as chaves? Entre em contato com o suporte.
