# Perfil e Bloqueio de Perfil (Profile) — Guia do Cliente

No painel aparece como **Profile**. Este guia explica, de forma simples, o que é o perfil público e o recurso de bloqueio de perfil, como o jogador o usa e como você o configura pelo painel administrativo. Não é necessário conhecimento técnico.

---

## O que é o Perfil?

Cada personagem e cada guilda tem um **perfil público** no site (**Perfil do personagem** e **Perfil da guilda**), com informações, atributos, combate e, se você permitir, os **equipamentos**.

O **Bloqueio de perfil** deixa o jogador **esconder o perfil de um personagem** por um período, pagando com **horas jogadas** ou, se não tiver horas suficientes, com o **saldo de uma carteira**. É um recurso de **privacidade e monetização leve**: dá ao jogador controle sobre a visibilidade e cria mais um uso para as horas e o saldo dele.

---

## Conceitos principais

### O pacote de bloqueio

Cada **pacote** define por quanto tempo o perfil fica oculto (**Horas de bloqueio**) e quanto custa. Tem um **Nome**, uma **Descrição**, uma **Imagem** e o estado **Ativo**.

### Como o custo funciona

- **Custo em horas** (obrigatório): quantas horas jogadas são consumidas.
- **Custo em carteira** + **Carteira** (opcionais): o valor cobrado **somente quando o saldo de horas não cobre** o custo em horas. Se o pacote não tiver custo em carteira e o jogador não tiver horas suficientes, a compra é recusada.

Ou seja: horas primeiro; carteira só como alternativa.

### Formato dos tempos

Tanto **Horas de bloqueio** quanto **Custo em horas** aceitam horas inteiras (ex.: `24`) ou o formato **hora:minuto** (ex.: `1:30`).

### O bloqueio é por personagem

O bloqueio vale para o **personagem** escolhido, não para a conta inteira. Comprar um novo pacote enquanto o bloqueio está ativo **soma** o tempo ao bloqueio vigente.

---

## Como o jogador usa

1. No painel da conta, o jogador abre o **personagem** desejado e acessa **Bloquear perfil**.
2. A tela mostra **Seu saldo atual é de X horas** e os pacotes disponíveis, com a **Duração** e o custo em **horas**.
3. Ele clica em **Comprar** e confirma. O custo é debitado (horas ou, na falta delas, carteira) e o perfil fica **oculto** pelo período.
4. Quem tentar abrir o perfil vê a mensagem **Perfil bloqueado até** a data/hora do fim do bloqueio. Depois disso, o perfil volta a ficar visível sozinho.

---

## Como configurar (passo a passo)

Tudo é feito em **Configurações → Profile** (o card aparece com o nome em inglês). Nessa tela ficam as configurações gerais e, logo abaixo, a lista de pacotes de bloqueio.

### 1. Configurações gerais e origem das horas (pré-requisito)

No card **Configurações**:

- **Mostrar equipamentos** — exibe os equipamentos do personagem no perfil público.
- Origem das horas jogadas: **Banco de dados**, **Tabela de horas jogadas**, **Coluna de horas jogadas** e **Coluna identificadora** (a coluna que identifica o personagem ou a conta na tabela escolhida). Peça ajuda a quem conhece o banco do seu servidor se tiver dúvida.

Clique em **Salvar**. **Sem a coluna de horas configurada, o bloqueio não funciona**: o perfil nunca é ocultado e o jogador não tem saldo de horas.

### 2. Criar um pacote de bloqueio

1. Clique em **Adicionar** (botão no topo da tela).
2. Preencha o **Nome** (traduzível), as **Horas de bloqueio**, marque **Ativo**, escreva a **Descrição** e envie a **Imagem**.
3. No card **Preços**, informe o **Custo em horas** (obrigatório) e, se quiser oferecer a alternativa, o **Custo em carteira** e a **Carteira**.
4. Clique em **Salvar**.
5. Na lista, arraste as linhas para definir a ordem em que os pacotes aparecem para o jogador.

### 3. Ver as estatísticas

Em **Estatísticas** (botão no topo da tela) você vê o **Total de pacotes** cadastrados e quantos estão **Ativo** e **Inativo**.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|------------------------|-----------------|
| Mostrar/ocultar equipamentos no perfil | **Configurações → Profile**, opção **Mostrar equipamentos** |
| Origem das horas jogadas | **Configurações → Profile**, campos **Banco de dados / Tabela de horas jogadas / Coluna de horas jogadas / Coluna identificadora** |
| Criar/editar/excluir pacotes de bloqueio | **Configurações → Profile**, lista abaixo das configurações (botão **Adicionar**) |
| Definir o tempo de bloqueio | Campo **Horas de bloqueio** |
| Definir o custo | Card **Preços** (**Custo em horas**, **Custo em carteira**, **Carteira**) |
| Ordenar os pacotes | Arrastar as linhas da lista |
| Ativar/desativar um pacote | Campo **Ativo** |
| Acompanhar | Botão **Estatísticas** no topo da tela |

---

## Dicas e boas práticas

- Ofereça **opções variadas** de duração (1 dia, 7 dias, 30 dias) com custos proporcionais.
- Use o **Custo em horas** para premiar quem joga bastante e o **Custo em carteira** como alternativa para quem prefere pagar com saldo.
- Capriche na **Descrição** explicando o que o bloqueio faz (privacidade do perfil do personagem).
- Mantenha pacotes antigos como **inativos** em vez de excluir.
- Confira a **origem das horas** antes de divulgar o recurso: sem ela, nada funciona.

---

## Perguntas frequentes

**O que o bloqueio esconde?**
O **perfil público do personagem** escolhido, pelo tempo do pacote. Os outros personagens da conta continuam visíveis.

**Como o jogador paga pelo bloqueio?**
Com **horas jogadas**. Se não tiver horas suficientes e o pacote tiver **Custo em carteira**, o valor é cobrado da carteira indicada.

**O perfil volta sozinho depois?**
Sim. Ao fim do período, o perfil volta a ficar **visível** automaticamente.

**O jogador pode renovar antes de acabar?**
Sim. Uma nova compra **soma** o tempo ao bloqueio ainda em vigor.

**Posso oferecer vários pacotes?**
Sim. Cada pacote tem sua própria duração e custo.

**O bloqueio não funciona. O que verificar?**
Se a **Coluna de horas jogadas** está configurada em **Configurações → Profile**. Sem ela, o recurso fica desativado.
