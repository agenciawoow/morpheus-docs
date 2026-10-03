# Slides (Banners e Modais) — Guia do Cliente

Este guia explica, de forma simples, o que são os Slides, onde aparecem para o jogador e como você os configura pelo painel administrativo. Não é necessário conhecimento técnico.

---

## O que são os Slides?

Os Slides são as **imagens de destaque** do seu site: o **carrossel de banners** e os **avisos em janela (modal)** que aparecem quando o jogador entra. Servem para divulgar promoções, eventos, novidades e links importantes.

É a sua **vitrine visual**: a primeira coisa que o jogador vê ao acessar o site.

---

## Conceitos principais

### O slide

Tem uma **imagem** (obrigatória), uma **URL** opcional (para onde o jogador vai ao clicar), um **título** em vários idiomas e pode ter **links** extras (botões com nome e endereço). Cada slide é **ativo** ou não e tem uma **ordem** de exibição.

### Tipos de slide

- **Slide:** entra no **carrossel de banners** do site, junto com os outros banners. Mostra só a imagem (com o link, se houver).
- **Modal:** aparece em uma **janela** sobreposta quando o jogador acessa o site. Mostra o título, a imagem e os **links** como botões no rodapé da janela. Se houver vários modais ativos, eles passam em sequência dentro da mesma janela.

### Ordem e ativação

Os slides são exibidos na **ordem** que você define (arrastando as linhas da lista). Slides **inativos** ficam guardados sem aparecer no site, sem precisar excluí-los.

### Tempos de transição

Você define em segundos quanto tempo cada banner fica na tela antes de passar para o próximo, de quanto em quanto tempo a janela de modal volta a aparecer para o mesmo jogador e o tempo de troca entre os modais.

### Bloco Slides no construtor de páginas

Com o plugin **Pages** ativo, o construtor de páginas ganha o bloco **Slides**, que exibe o carrossel de banners ativos em qualquer página que você montar. O bloco não tem opções: ele usa os mesmos slides do tipo **Slide** e o mesmo tempo de transição configurado.

---

## Como o jogador usa

1. No site, o jogador vê o **carrossel** com os banners ativos, em sequência, com setas e indicadores para navegar.
2. Ao clicar em um banner, é levado à **URL** configurada (se houver).
3. Avisos do tipo **Modal** aparecem em uma janela ao entrar no site, com o título, a imagem, os botões de **links** e o botão **Fechar**. A janela só volta a aparecer depois do intervalo que você definiu.

---

## Como configurar (passo a passo)

Tudo fica em **Configurações → Slides**.

### 1. Criar um slide

1. Vá em **Configurações → Slides** e clique em **Adicionar**.
2. Escolha o **Tipo** (Slide ou Modal) e ligue o interruptor **Ativo**.
3. Preencha o **Título** em cada idioma do site.
4. Envie a **Imagem**.
5. (Opcional) Informe a **URL** de destino do clique.
6. (Opcional) Em **Links**, adicione botões com **Nome** e **Link**. Use **Adicionar** para mais linhas e arraste para ordenar. Só valem as linhas com nome e link preenchidos.
7. Clique em **Salvar**.

Na edição, a imagem atual aparece como prévia; envie um novo arquivo só se quiser trocá-la.

### 2. Ordenar, buscar e desativar

Na lista de **Slides**, arraste as linhas para definir a **ordem** de exibição. A lista mostra miniatura, **Título**, **URL**, **Tipo** e **Status**, com busca por título e botões de editar e excluir em cada linha.

### 3. Ajustar os tempos

1. Na lista de Slides, clique no botão **Configurações** no topo.
2. No card **Configurações do Banner**, preencha **Transição do banner em (segundos)**: tempo que cada banner fica na tela.
3. No card **Configurações da Modal**, preencha **Apresentar modal em (segundos)**: intervalo mínimo até a janela voltar a aparecer para o mesmo jogador, e **Transição da modal em (segundos)**: tempo de troca entre os modais dentro da janela.
4. Clique em **Salvar**.

### 4. Ver as estatísticas

Clique em **Estatísticas** no topo da lista. Você vê o **Total de slides**, quantos estão **Ativo** e **Inativo**, e o quadro **Slides por tipo** com o total e os ativos de cada tipo.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|------------------------|-----------------|
| Criar ou editar slides | **Configurações → Slides**, botão **Adicionar** ou editar na linha |
| Escolher banner ou modal | Campo **Tipo** do slide |
| Definir imagem e link do clique | Campos **Imagem** e **URL** do slide |
| Título em cada idioma | Campo **Título** do slide |
| Botões extras na janela de modal | Seção **Links** do slide |
| Ativar ou desativar | Interruptor **Ativo** do slide |
| Reordenar | Arrastar as linhas na lista de Slides |
| Tempo de cada banner | Botão **Configurações** no topo da lista, campo **Transição do banner em (segundos)** |
| Frequência da janela de modal | Botão **Configurações** no topo da lista, campo **Apresentar modal em (segundos)** |
| Tempo de troca entre modais | Botão **Configurações** no topo da lista, campo **Transição da modal em (segundos)** |
| Acompanhar | Botão **Estatísticas** no topo da lista |
| Mostrar o carrossel em outra página | Bloco **Slides** no construtor de páginas do plugin **Pages** |

---

## Dicas e boas práticas

- Use **imagens no mesmo tamanho** para o carrossel ficar uniforme.
- Reserve o **Modal** para avisos realmente importantes. Usado demais, incomoda o jogador. Um intervalo grande em **Apresentar modal em (segundos)** evita que a janela apareça a cada visita.
- Mantenha banners antigos como **inativos** em vez de excluir; assim você reaproveita depois.
- Sempre aponte uma **URL** útil no banner (loja, evento, doação) para aproveitar o clique.
- No modal, os **Links** viram botões bem visíveis; use-os para "Ver evento", "Doar" ou "Saiba mais".

---

## Perguntas frequentes

**Qual a diferença entre Slide e Modal?**
O **Slide** entra no carrossel de banners; o **Modal** aparece em uma janela ao entrar no site, com título e botões de links.

**Como mudo a ordem dos banners?**
Arraste as linhas na lista de **Slides**. A ordem é salva automaticamente.

**Posso ter um banner sem link?**
Sim. A **URL** é opcional; sem ela, o banner é apenas visual.

**Como tiro um banner do ar sem perdê-lo?**
Desligue o interruptor **Ativo**. Ele some do site mas continua cadastrado.

**A janela de modal aparece toda vez que o jogador entra?**
Não. Ela respeita o intervalo em **Apresentar modal em (segundos)**: depois de aparecer, só volta quando esse tempo passar no mesmo navegador.

**Os links do slide aparecem no carrossel?**
Não. No carrossel só vale a **URL** de clique da imagem. Os **Links** aparecem como botões apenas na janela de modal.
