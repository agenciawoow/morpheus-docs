# Criando plugins com inteligência artificial — Guia do Cliente

Este guia explica, de forma simples, como usar um assistente de IA (como o **Claude Code**) para criar **plugins** e personalizações no seu site Morpheus, sem precisar conhecer o código interno do sistema.

---

## O que vem junto com o seu Morpheus?

Toda instalação do Morpheus traz uma pasta chamada `.claude/skills/morpheus/`. Dentro dela está o **manual completo do sistema para a IA**: como um plugin é montado, quais eventos o site dispara (cadastro, doação paga, login, item vendido…), quais funções existem, como criar telas no painel administrativo, como criar tabelas no banco e muito mais.

Também existe um **plugin de exemplo completo** em `.claude/skills/morpheus/templates/Example/`. Ele é um mural de avisos que funciona de verdade: tem página pública, tela no painel, tradução nos 6 idiomas, tabela no banco, API e reação a eventos. A IA usa esse exemplo como ponto de partida para o que você pedir.

Na raiz do site há ainda um arquivo `AGENTS.md`, que serve como porta de entrada para outros assistentes (Cursor, Codex, Copilot).

> Você não precisa ler esses arquivos. Eles existem para a IA.

---

## O que eu preciso instalar?

1. **Claude Code** no seu computador: siga as instruções em https://claude.com/claude-code.
2. Acesso aos arquivos do site (a pasta onde o Morpheus está instalado), seja localmente ou por uma cópia sincronizada com o servidor.
3. PHP instalado no computador, para a IA poder rodar os comandos `php morpheus ...` (migrations, cache, criação do plugin).

Abra o terminal **na pasta do site** (a mesma onde ficam `index.php` e `plugins/`) e inicie o Claude Code. Ele encontra o manual sozinho.

---

## Como pedir um plugin

Descreva **o que você quer que aconteça**, do jeito que explicaria para uma pessoa. Alguns exemplos que funcionam bem:

- "Crie um plugin que dê 100 WCoin para toda conta nova no momento do cadastro."
- "Quero uma página pública `/eventos-da-semana` listando eventos que eu cadastro no painel, com título, data e descrição, nos 6 idiomas."
- "Quando uma doação for paga, mande uma mensagem interna para o jogador agradecendo e informando o valor."
- "Crie uma tela no painel para eu cadastrar cupons de desconto do meu Discord, com código e validade, e uma página pública onde o jogador resgata."
- "Adicione um endpoint na API que liste os 10 jogadores com mais resets."

A IA vai criar a pasta `plugins/<NomeDoPlugin>/` com tudo o que for necessário e dizer os próximos passos.

---

## Depois que a IA terminar

1. **Ative o plugin** no painel: **Plugins → ativar**.
2. Se o plugin criou tabelas, rode no terminal (na pasta do site):
   ```
   php morpheus migrations:migrate
   php morpheus cache:clear
   ```
   A própria IA costuma rodar esses comandos; confirme que não houve erro.
3. Abra a página pública e a tela do painel para conferir.
4. Se algo não ficou como esperava, descreva o problema para a IA na mesma conversa ("o botão não aparece para quem não está logado", "quero a lista ordenada por data").

---

## Dicas para pedidos melhores

- **Uma coisa por vez.** Peça o plugin básico, confira, depois peça melhorias.
- **Diga onde deve aparecer:** página pública, painel do jogador, painel administrativo ou API.
- **Diga quem pode usar:** todos, só jogadores logados, só VIP, só administradores.
- **Fale em termos do jogo:** WCoin, GoblinPoints, VIP Prata, resets, personagem, guild. A IA conhece esses conceitos do Morpheus.
- **Peça tradução** quando a página for visível aos jogadores: "nos 6 idiomas do site".

---

## O que o Morpheus garante e o que fica por sua conta

**Garantido pelo Morpheus**

- O manual (`.claude/skills/morpheus/`) é atualizado a cada versão e descreve exatamente o que o seu Morpheus oferece.
- O plugin de exemplo funciona na versão instalada.
- Atualizações do Morpheus **não apagam** a pasta `plugins/` nem os seus plugins.

**Por sua conta**

- O conteúdo e o funcionamento dos plugins que você (ou a IA) criar. O suporte do Morpheus cobre o sistema; plugins próprios são tratados como personalização.
- Fazer **backup** antes de ativar um plugin novo em produção, principalmente se ele mexe em coins, VIP ou itens.
- Testar primeiro em um ambiente de testes, se tiver um.

---

## Perguntas frequentes

**Preciso saber programar?**
Não para pedir e usar. Saber o básico ajuda a conferir o resultado, mas o manual foi feito justamente para a IA fazer o trabalho técnico seguindo as regras do Morpheus.

**Posso usar outra IA que não o Claude Code?**
Sim. Qualquer assistente que leia arquivos do projeto pode usar o `AGENTS.md` da raiz, que aponta para o manual. O Claude Code é o que encontra o manual automaticamente.

**A IA pode quebrar o meu site?**
Ela só cria arquivos dentro de `plugins/`. Um plugin com erro pode gerar uma página em branco enquanto estiver ativo; basta **desativá-lo no painel** (ou renomear a pasta) e o site volta ao normal. Por isso o backup antes de ativar em produção.

**O plugin que a IA criou vai continuar funcionando depois de atualizar o Morpheus?**
Plugins que seguem o manual usam só a parte pública e estável do sistema. Mudanças que afetam plugins são avisadas nas notas de versão.

**Posso vender ou compartilhar o plugin que criei?**
Pode. O plugin é seu. Para instalá-lo em outro Morpheus, basta copiar a pasta (ou enviar um ZIP pelo painel em **Plugins → Instalar**).

**O comando `php morpheus make:plugin` serve para quê?**
Cria a estrutura de um plugin novo a partir do exemplo, já com o nome que você escolher. A IA usa esse comando como primeiro passo; você também pode usá-lo manualmente.
