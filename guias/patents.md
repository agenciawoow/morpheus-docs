# Patentes (Patents) — Guia do Cliente

Este guia explica, de forma simples, o que são as Patentes, como o jogador as conquista e como você as configura pelo painel administrativo. Não é necessário conhecimento técnico.

---

## O que são as Patentes?

As Patentes são **insígnias** exibidas ao lado do personagem nos **rankings** do site, conquistadas conforme ele evolui — por **nível**, **resets**, **master level**, **master resets** ou por uma regra personalizada. Servem para destacar a progressão e dar status dentro da comunidade.

É uma ferramenta de **reconhecimento e progressão**: o jogador sobe de patente conforme avança, o que incentiva a evolução.

---

## Conceitos principais

### A patente

Tem um **Título**, uma **Imagem** (a insígnia) e um **Tipo** que define a condição para conquistá-la. A **ordem** das patentes na lista define a progressão: da mais baixa (primeira) para a mais alta (última). Sem imagem, o título aparece como um selo de texto no ranking.

### De onde vêm os dados

As patentes podem ser calculadas pelo próprio site ou lidas de uma tabela do seu servidor (quando o jogo já tem um sistema de patentes). Isso é definido na **origem dos dados**, no topo da tela de configurações, e muda quais **tipos** ficam disponíveis:

- **Sem origem configurada** (o site calcula): tipos **Corrigir** e **SQL**.
- **Com origem configurada** (o jogo já tem patentes): tipo **Código**.

### Tipos de patente

- **Corrigir** — o jogador conquista ao atingir os valores informados em **Level**, **Resets**, **Master Level** e/ou **Master Resets**. Preencha só os que importam.
- **SQL** — a condição segue uma regra personalizada. É um **recurso avançado**: use com cuidado e com ajuda de quem conhece o banco do jogo.
- **Código** — a patente corresponde a um **Código** do sistema de patentes do próprio servidor; o site apenas exibe o título e a imagem para quem tem aquele código.

---

## Como o jogador conquista

1. Conforme evolui (nível, resets, master), o personagem **alcança** as patentes correspondentes.
2. A **insígnia** da patente aparece ao lado do nome dele nos **rankings** do site.
3. Quanto mais ele avança, **mais alta** a patente exibida.

---

## Como configurar (passo a passo)

O único acesso é **Configurações → Patentes**. Nessa tela ficam a origem dos dados e, logo abaixo, a lista de patentes.

### 1. Definir a origem dos dados

No card **Configurações**:

- Se o seu servidor **não tem** sistema de patentes, deixe os campos em branco — o site calcula tudo.
- Se o jogo **já tem** patentes, informe o **Banco de dados**, a **Tabela**, a **Coluna do código da patente** e a **Coluna do nome da patente** (a coluna que identifica o personagem). Peça ajuda a quem conhece o banco do seu servidor se tiver dúvida.

Clique em **Salvar**.

### 2. Criar as patentes

1. Clique em **Adicionar** (botão no topo da tela).
2. Preencha o **Título** e envie a **Imagem** da insígnia.
3. Escolha o **Tipo**:
   - **Corrigir**: informe **Level**, **Resets**, **Master Level** e/ou **Master Resets**.
   - **SQL**: informe a regra personalizada (recurso avançado).
   - **Código**: informe o **Código** correspondente no sistema do jogo.
4. Clique em **Salvar**. Só o título é obrigatório.
5. Na lista, arraste as linhas para ordenar da patente **mais baixa para a mais alta**. A coluna **Requisito** resume a condição de cada uma.

### 3. Ativar a tarefa de cálculo (quando o site calcula)

Nos tipos **Corrigir** e **SQL**, quem atribui as patentes aos personagens é uma **tarefa agendada**. Vá em **Configurações → Tarefas**, clique em **Adicionar**, escolha no campo **Script** a tarefa **calculate-patents** do grupo **Patents**, defina a frequência (por exemplo, a cada 30 minutos), marque **Ativo** e salve. No tipo **Código** a tarefa não é necessária.

### 4. Ver as estatísticas

Em **Estatísticas** (botão no topo da tela) você vê o **Total de patentes** cadastradas e quantas estão **Ativo** e **Inativo**.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|------------------------|-----------------|
| Origem dos dados (banco, tabela, colunas) | **Configurações → Patentes**, card **Configurações** |
| Criar/editar/excluir patentes | **Configurações → Patentes**, lista abaixo das configurações (botão **Adicionar**) |
| Definir a condição | Campo **Tipo** (**Corrigir**, **SQL** ou **Código**) e seus campos |
| Imagem da insígnia | Campo **Imagem** da patente |
| Ordenar a progressão | Arrastar as linhas da lista |
| Calcular as patentes dos personagens | **Configurações → Tarefas** (tarefa **calculate-patents**) |
| Acompanhar | Botão **Estatísticas** no topo da tela |

---

## Dicas e boas práticas

- Crie uma **escada de patentes** coerente com a progressão do seu servidor (nível → resets → master).
- Use **imagens distintas** para cada patente — a diferença visual valoriza a conquista.
- Mantenha a **ordem** da mais baixa para a mais alta: o cálculo percorre a lista nessa ordem e para na primeira patente que o personagem ainda não alcançou.
- Reserve o tipo **SQL** para casos especiais; o tipo **Corrigir** cobre a maioria.
- Se o jogo já tem patentes, use a **origem dos dados** e o tipo **Código** em vez de recalcular no site.

---

## Perguntas frequentes

**Como o jogador ganha uma patente?**
Automaticamente, ao cumprir a **condição** da patente (nível, resets, master ou regra personalizada), quando a tarefa agendada roda — ou, no tipo **Código**, assim que o jogo atribuir o código a ele.

**Onde a patente aparece?**
Ao lado do nome do personagem nos **rankings** do site.

**Por que só vejo o tipo "Código" ao criar uma patente?**
Porque há uma **origem dos dados** configurada. Limpe os campos do card **Configurações** para voltar aos tipos **Corrigir** e **SQL**.

**As patentes não estão sendo atribuídas. O que verificar?**
Confirme que a tarefa **calculate-patents** está cadastrada e **ativa** em **Configurações → Tarefas** e que a ordem das patentes vai da mais baixa para a mais alta.

**Qual a diferença entre os tipos?**
**Corrigir** usa nível/resets/master; **SQL** usa uma regra personalizada (avançado); **Código** exibe uma patente que o próprio jogo já atribuiu.
