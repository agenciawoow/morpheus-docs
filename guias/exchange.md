# Exchange (Conversões) — Guia do Cliente

No painel, o card aparece como **Exchange**. Este guia explica, de forma simples, o que o Exchange oferece, como o jogador usa e como você configura tudo pelo painel. Não é necessário conhecimento técnico.

---

## O que é o Exchange?

O Exchange reúne três conversões que o jogador faz sozinho, no painel dele no site:

- **Conversor de Moedas**: troca uma moeda do jogo por outra (ex.: WCoin por GoblinPoint), com uma taxa e uma cotação que você define.
- **Conversor de Carteira**: troca saldo entre as carteiras do site, também com taxa e cotação.
- **Troca de horas online**: converte o tempo que o jogador passou jogando em pacotes de recompensa (VIP, moedas ou um prêmio personalizado).

É uma ferramenta de **engajamento e economia**: dá utilidade a moedas paradas, recompensa quem fica mais tempo no servidor e ainda pode gerar receita com a taxa de cada conversão.

---

## Conceitos principais

### Taxa e cotação

Nas conversões de moedas e de carteiras, cada moeda ou carteira de origem tem:

- **Taxa**: a porcentagem descontada da quantidade que o jogador entrega (0 = sem desconto).
- **Cotação** para cada destino: quanto de cada unidade vira na moeda ou carteira de destino. Ex.: cotação 2 significa que cada unidade entregue (após a taxa) vira 2 unidades no destino.

A conta é sempre a mesma: a taxa é descontada da quantidade, o que sobra é multiplicado pela cotação, e o resultado é arredondado para baixo. O jogador vê a **Taxa** e o **Você recebe** antes de confirmar.

Só aparecem para o jogador as origens que você ligou na matriz e que têm pelo menos uma cotação preenchida. Uma moeda não pode ser convertida nela mesma.

### O pacote de horas

Cada pacote define quantas **Horas** custa e o que entrega. Tem **Nome** e **Descrição** (nos idiomas que você quiser), **Imagem** e o interruptor **Ativo**. Só os pacotes ativos aparecem para o jogador, na ordem que você definir arrastando as linhas da lista.

Um pacote pode entregar, em qualquer combinação:

- **VIP**: um **Tipo** por uma quantidade de **Dias**;
- **Moedas**: um campo por moeda do servidor, com a quantidade de cada;
- **Customizado**: um recurso avançado, para prêmios fora do padrão. Use com cuidado e com ajuda de quem conhece o banco do jogo.

### As horas jogadas

O saldo de horas vem do tempo que o jogador passa online, contabilizado pelo próprio servidor. Para o site saber onde ler esse número, você escolhe a **Column hours played** nas configurações. Enquanto esse campo não estiver preenchido, a página de troca de horas do jogador mostra o aviso *"A troca de horas ainda não foi configurada"* e nenhuma compra é feita.

### Os serviços

As três conversões são **serviços** do painel do jogador. Em **Serviços → Serviços** você pode ligar ou desligar cada um (**Ativo**), limitar a quem pode usar (**Allowed to**, por VIP) e definir um custo ou bônus próprio do serviço, que o jogador vê no alto da página antes de converter.

---

## Como o jogador usa

### Conversor de Moedas

1. No painel do jogador, em **Conversor de Moedas**, ele vê o saldo de cada moeda.
2. Informa a **Quantidade**, escolhe a **Moeda** de origem e, em **Para**, a moeda de destino (a lista mostra só os destinos que você configurou).
3. O site mostra na hora a **Taxa** descontada e o **Você recebe**.
4. Clica em **Converter**. A moeda de origem é debitada e a de destino, creditada, tudo de uma vez.

### Conversor de Carteira

Funciona do mesmo jeito, em **Conversor de Carteira**: ele vê o saldo das carteiras, informa a **Quantidade**, escolhe a **Wallet** de origem e o destino em **Para**, confere **Taxa** e **Você recebe** e clica em **Converter**.

### Troca de horas online

1. Em **Troca de horas online**, o jogador vê a mensagem *"Seu saldo é de X horas"* e os pacotes ativos, cada um com imagem, descrição, o que entrega (VIP e moedas) e o custo em horas.
2. Clica em **Comprar** e confirma. Se o pacote dá um VIP diferente do que ele tem hoje, o site avisa que o plano VIP vai ser trocado e pede uma segunda confirmação.
3. As horas são descontadas e a recompensa cai na conta imediatamente.

Regras que valem para todos:

- O jogador precisa estar **fora do jogo** nas conversões de moedas e carteiras; se estiver conectado, o site responde *"Você precisa sair do jogo antes"*.
- A quantidade precisa ser maior que zero e caber no saldo. Sem saldo, aparece *"Você não possuí X suficiente"* ou *"Você não possui horas suficientes para realizar essa compra!"*.
- Cada conversão fica registrada no histórico da conta do jogador.
- Se o Passe de Batalha estiver instalado, as conversões de moedas e de carteiras contam como ação dele.

---

## Como configurar (passo a passo)

Tudo fica em uma única tela: **Configurações → Exchange**. Ela tem o card **Packages** (os pacotes de horas) e, abaixo, os cards de configuração. No topo há o botão **Estatísticas**.

### 1. Escolher a coluna de horas jogadas

1. Abra **Configurações → Exchange**.
2. No card **Configurações**, escolha a **Column hours played** na lista (são as colunas disponíveis no banco do seu servidor; na dúvida, pergunte a quem cuida do servidor).
3. Clique em **Salvar**.

Esse é o pré-requisito da Troca de horas online. Sem ele, a página do jogador avisa que a troca ainda não foi configurada.

### 2. Configurar a conversão de moedas

O card **Conversão de moedas** só aparece quando o servidor tem mais de uma moeda cadastrada.

1. Em cada linha há uma moeda de origem. Ligue o interruptor da linha para liberar aquela moeda como origem.
2. Preencha a **Taxa** (em %).
3. Em **Rate**, preencha a cotação para cada moeda de destino. Deixe em branco os destinos que não quer permitir.
4. Clique em **Salvar**. Linhas desligadas ou sem nenhuma cotação não aparecem para o jogador.

### 3. Configurar a conversão de carteiras

O card **Conversão de carteiras** só aparece quando há mais de uma carteira cadastrada. Funciona igual ao de moedas: ligue a linha da **Wallet** de origem, preencha a **Taxa** e a cotação em **Rate** para cada destino, e clique em **Salvar**.

### 4. Criar um pacote de horas

1. No card **Packages**, clique em **Adicionar**.
2. No card **Pacote**, preencha o **Nome** (nos idiomas que desejar), ligue **Ativo**, escreva a **Descrição**, envie uma **Imagem** e informe as **Horas** que o pacote custa.
3. No card **VIP**, escolha o **Tipo** e os **Dias** (deixe em branco se o pacote não dá VIP).
4. No card **Moedas**, informe a quantidade em cada moeda que o pacote entrega (deixe em branco as que não entram).
5. O card **Customizado** é um recurso avançado; deixe em branco a menos que alguém que conhece o banco do jogo esteja ajudando.
6. Clique em **Salvar**. Na lista, arraste as linhas para definir a ordem em que os pacotes aparecem.

A lista mostra **Pacote**, **Horas**, **VIP**, **Moedas** e **Status** (**Ativo** ou **Inativo**), com os botões de editar e excluir.

### 5. Ligar os serviços para o jogador

Em **Serviços → Serviços**, confira que **Conversor de Moedas**, **Conversor de Carteira** e **Troca de horas online** estão com **Ativo** ligado e liberados para os VIPs que você quiser.

### 6. Ver as estatísticas

O botão **Estatísticas**, no topo de **Configurações → Exchange**, mostra **Total de pacotes**, quantos estão **Ativo** e quantos **Inativo**.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|------------------------|-----------------|
| Indicar de onde vêm as horas jogadas | **Configurações → Exchange**, card **Configurações**, campo **Column hours played** |
| Liberar uma moeda para conversão | **Configurações → Exchange**, card **Conversão de moedas**, interruptor da linha |
| Definir a taxa de uma moeda | Card **Conversão de moedas**, campo **Taxa** |
| Definir quanto vira em cada destino | Card **Conversão de moedas**, campos **Rate** |
| Liberar e cotar carteiras | **Configurações → Exchange**, card **Conversão de carteiras** |
| Criar ou editar pacotes de horas | **Configurações → Exchange**, card **Packages**, botão **Adicionar** ou **Editar** |
| Definir o custo do pacote | Campo **Horas** do pacote |
| Dar VIP no pacote | Card **VIP** do pacote, campos **Tipo** e **Dias** |
| Dar moedas no pacote | Card **Moedas** do pacote |
| Ordenar os pacotes | Arrastar as linhas do card **Packages** |
| Ativar ou desativar um pacote | Interruptor **Ativo** do pacote |
| Ligar ou desligar cada conversão para o jogador | **Serviços → Serviços** |
| Acompanhar | Botão **Estatísticas** no topo de **Configurações → Exchange** |

---

## Dicas e boas práticas

- Configure a **Column hours played** antes de criar pacotes: sem ela, a troca de horas não funciona para ninguém.
- Use a **Taxa** como freio: uma porcentagem pequena já desestimula conversões em massa e vira uma fonte de receita indireta.
- Cotações muito generosas desvalorizam a moeda mais rara. Comece conservador e ajuste olhando o comportamento dos jogadores.
- Se quiser uma conversão só de ida (ex.: WCoin vira GoblinPoint, mas não o contrário), preencha a cotação apenas na linha de origem desejada.
- Monte uma **escada de pacotes**: poucas horas para um prêmio pequeno, muitas horas para um prêmio maior.
- Capriche na **Imagem** e na **Descrição** do pacote: é o que o jogador vê antes de decidir.
- Deixe o card **Customizado** para casos realmente especiais; **VIP** e **Moedas** resolvem a maioria.

---

## Perguntas frequentes

**De onde vêm as horas do jogador?**
Do tempo que ele passa online no jogo, contabilizado pelo próprio servidor. Você só indica, no campo **Column hours played**, onde o site deve ler esse número.

**O jogador vê a mensagem de que a troca de horas não foi configurada. O que fazer?**
Abra **Configurações → Exchange** e escolha a **Column hours played** no card **Configurações**.

**Por que o card Conversão de moedas não aparece?**
Ele só aparece quando há mais de uma moeda cadastrada no servidor. O mesmo vale para **Conversão de carteiras** e as carteiras.

**Por que uma moeda não aparece para o jogador na lista de origem?**
A linha dela precisa estar ligada e ter pelo menos uma cotação preenchida em **Rate**.

**Como a taxa é cobrada?**
Ela é uma porcentagem da quantidade entregue, descontada antes de aplicar a cotação. O jogador vê a **Taxa** e o **Você recebe** antes de confirmar.

**O jogador comprou um pacote com VIP diferente do que tinha. O que acontece?**
O site avisa que o plano VIP vai ser trocado e pede confirmação. Só depois de confirmar o VIP do pacote é aplicado.

**As horas são descontadas na hora?**
Sim. Ao comprar, as horas são debitadas e a recompensa é entregue imediatamente.

**Como tiro um pacote do ar?**
Desligue o interruptor **Ativo** do pacote: ele some da troca, mas continua cadastrado.
