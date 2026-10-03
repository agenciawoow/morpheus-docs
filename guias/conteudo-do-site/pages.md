# Páginas (Pages) — Guia do Cliente

Este guia explica, de forma simples, o que é o construtor de páginas, como o jogador vê as páginas no site e como você as cria e configura pelo painel administrativo. Não é necessário conhecimento técnico.

---

## O que são as Páginas?

O plugin **Páginas** é o **construtor de páginas** do seu site. Com ele você cria páginas próprias — "Sobre o servidor", "Como jogar", "Regras", uma landing de lançamento, uma página de evento — sem mexer no tema. Cada página é montada com **blocos**: um bloco de conteúdo livre (**HTML**) e blocos prontos que outros plugins acrescentam (temporizador, notícias, slides, vídeos, enquete, guias).

É uma ferramenta de **comunicação e conversão**: dá a você liberdade para publicar conteúdo novo, em vários idiomas, com visual personalizado e otimizado para buscadores.

---

## Conceitos principais

### A página

Tem um **Título** (traduzível), um endereço no site (campo **Slug**), o estado **Ativo**, um **Layout**, os **Blocos** de conteúdo, um **CSS personalizado** e um **Script personalizado** opcionais, e os campos de **SEO** (**Meta título** e **Meta descrição**, traduzíveis).

### O endereço (Slug)

O campo **Slug** é a parte final do endereço da página. Se você informar `regras`, a página fica em **/page/regras** no site. Use só letras minúsculas, números e hífens; o endereço precisa ser único.

### Layout

Define como a página é encaixada no tema:

- **Default** — a página aparece dentro da área de conteúdo normal do site, como as demais páginas.
- **Page Builder** — a página ocupa a largura toda, sem a moldura central. Ideal para landing pages e páginas de evento com visual próprio.

### Blocos e idiomas

O conteúdo é montado por **blocos**, empilhados na ordem que você quiser, e é **separado por idioma**: cada idioma do site tem a sua própria lista de blocos. Nos idiomas secundários há o atalho **Copiar de PT** (ou do idioma padrão do seu site) para começar a partir da versão principal e só traduzir.

### Página ativa e inativa

Só páginas **ativas** abrem no site; uma página inativa responde como "não encontrada". Use isso para preparar uma página com calma e publicar na hora certa.

---

## Os blocos disponíveis

Os nomes dos blocos e dos campos dentro deles aparecem em inglês no editor.

### Bloco do próprio construtor

- **HTML** — conteúdo livre. Cole ou escreva o conteúdo da seção (textos, imagens, botões, tabelas). É o bloco principal para páginas de texto. Se precisar de um visual específico, combine com o **CSS personalizado** da página.

### Blocos que outros plugins acrescentam

Cada bloco abaixo só aparece no editor quando o plugin correspondente está ativo, e usa o conteúdo já cadastrado nele:

| Bloco | Plugin | O que mostra | Opções do bloco |
|-------|--------|--------------|-----------------|
| **Countdown** | Temporizador | Um contador regressivo (dias, horas, minutos, segundos) até a data de um temporizador cadastrado | **Countdown**: qual temporizador exibir |
| **Posts** | Notícias | As últimas notícias, com capa e resumo | **Title** (título opcional da seção), **Category** (uma categoria ou **All categories**), **Limit** (quantas notícias) |
| **Poll** | Enquete | Uma enquete com as opções de voto e o resultado | **Poll**: qual enquete exibir (só enquetes ativas aparecem no site) |
| **Slides** | Slides | O carrossel com os slides ativos cadastrados no plugin | Sem opções — usa os slides e o intervalo configurados no plugin |
| **Videos** | Vídeos | Os vídeos ativos, lado a lado | **Title** (título opcional), **Limit** (quantos vídeos) |
| **Guides** | Guias | Cartões com os guias de uma categoria, com link para cada guia | **Title** (título opcional), **Category** (categoria dos guias), **Limit** (quantos guias) |

Um bloco que aponte para um item que não existe mais, inativo ou sem conteúdo (ex.: enquete desativada, categoria sem notícias) simplesmente **não aparece** na página — nada quebra.

---

## Como o jogador usa

1. O jogador abre a página pelo endereço **/page/** + o **Slug** que você definiu, ou por um link que você colocou no menu, numa notícia, num botão ou em outra página.
2. Ele vê o **Título** da página, o caminho de navegação e os blocos na ordem em que você os montou, no idioma em que está navegando.
3. Os blocos são interativos quando fazem sentido: o jogador vota na enquete, vê o contador correndo, navega pelo carrossel e assiste aos vídeos ali mesmo.

> A página **não entra no menu do site sozinha**. Depois de criá-la, use o endereço dela onde quiser divulgá-la.

---

## Como configurar (passo a passo)

Tudo é feito no menu lateral **Páginas**.

### 1. Criar a página

1. Vá em **Páginas** e clique em **Adicionar**.
2. No card **Page** (título em inglês):
   - preencha o **Título** nos idiomas que desejar (o idioma padrão é obrigatório);
   - marque **Ativo** quando quiser publicar;
   - informe o **Slug** (obrigatório) — o endereço final da página;
   - escolha o **Layout** (**Default** ou **Page Builder**).
3. No card **Blocos**, escolha a aba do idioma, clique no **+** do editor e adicione os blocos desejados (**HTML**, **Countdown**, **Posts**, **Poll**, **Slides**, **Videos**, **Guides**). Preencha as opções de cada bloco e arraste para reordenar. Repita nos outros idiomas ou use **Copiar de PT**.
4. No card **Personalizado** (opcional), informe o **CSS personalizado** (estilos só desta página) e o **Script personalizado** (comportamentos só desta página). São campos para quem conhece esses recursos; deixe em branco se não precisar.
5. No card **SEO** (opcional), preencha o **Meta título** e a **Meta descrição** nos idiomas desejados — são o título e o resumo que aparecem nos buscadores e ao compartilhar o link. Sem meta título, o **Título** da página é usado.
6. Clique em **Salvar**.

### 2. Editar, publicar e excluir

- Na lista, use **Editar** para alterar qualquer coisa e **Excluir** para remover a página. A lista mostra o **Título**, o endereço (**Slug**) e o **Status**.
- Para tirar uma página do ar sem perdê-la, desmarque **Ativo**.

### 3. Ver as estatísticas

Em **Estatísticas** (botão no topo da lista) você vê o **Total de páginas**, as **Páginas ativas**, as **Páginas inativas** e a tabela **Páginas por layout**.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|------------------------|-----------------|
| Criar/editar/excluir páginas | **Páginas → Adicionar / Editar / Excluir** |
| Definir o endereço da página | Campo **Slug** |
| Publicar ou tirar do ar | Campo **Ativo** |
| Página de largura total (landing) | Campo **Layout** = **Page Builder** |
| Montar o conteúdo | Card **Blocos** (bloco **HTML** + blocos dos plugins) |
| Conteúdo em outro idioma | Aba do idioma no card **Blocos** (atalho **Copiar de PT**) |
| Visual e comportamento só desta página | Card **Personalizado** (**CSS personalizado**, **Script personalizado**) |
| Título e descrição para buscadores | Card **SEO** (**Meta título**, **Meta descrição**) |
| Cadastrar o conteúdo que os blocos exibem | Nos plugins **Temporizador**, **Notícias**, **Enquetes**, **Slides**, **Vídeos** e **Guias** |
| Acompanhar | Botão **Estatísticas** no topo da lista |

---

## Dicas e boas práticas

- Use endereços **curtos e descritivos** (`regras`, `como-jogar`, `evento-de-natal`) — ficam melhores no menu e nos buscadores.
- Para landing pages e páginas de evento, escolha o **Page Builder** e abra com um bloco **Countdown** ou **Slides** para impacto visual.
- Preencha o **SEO**: o **Meta título** e a **Meta descrição** são o que o Google e as redes sociais mostram.
- Monte primeiro no idioma padrão e use **Copiar de PT** nos demais — só traduza o que for texto.
- Deixe a página **inativa** enquanto monta; ative quando estiver pronta.
- Prefira os blocos prontos (Notícias, Guias, Vídeos) ao invés de copiar conteúdo no bloco **HTML**: eles se atualizam sozinhos quando você publica algo novo.

---

## Perguntas frequentes

**Como coloco a página no menu do site?**
A página não entra no menu automaticamente. Copie o endereço dela (**/page/** + o **Slug**) e use-o onde quiser: no menu do tema, numa notícia, num botão de outra página.

**Posso ter conteúdo diferente em cada idioma?**
Sim. Os blocos são separados por idioma; cada aba do card **Blocos** é independente. Use **Copiar de PT** para começar a partir do idioma padrão.

**Por que um bloco não aparece no editor?**
Os blocos de plugin só existem quando o plugin correspondente está **ativo**. Ative o plugin (Temporizador, Notícias, Enquetes, Slides, Vídeos ou Guias) e abra a página de novo.

**Por que um bloco não aparece no site?**
Quando o item escolhido não existe mais, está inativo ou não tem conteúdo (ex.: enquete desativada, categoria sem guias), o bloco é omitido. Confira o cadastro no plugin de origem.

**Qual a diferença entre Default e Page Builder?**
**Default** mostra a página dentro da área de conteúdo normal do site; **Page Builder** usa a largura toda, sem a moldura central — ideal para landing pages.

**Preciso saber programar para usar o construtor?**
Não para o básico: título, endereço, blocos prontos e SEO são preenchimentos simples. O bloco **HTML** e os campos **CSS personalizado** e **Script personalizado** exigem alguém que conheça esses recursos.

**O que acontece se eu desativar a página?**
Ela deixa de abrir no site (responde como não encontrada), mas todo o conteúdo fica guardado para reativar depois.
