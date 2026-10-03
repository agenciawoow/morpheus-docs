# Contas, personagens e itens — Guia do Cliente

No painel administrativo estas telas ficam no grupo **Jogo** do menu lateral: **Contas**, **Personagens** e **Itens**. Este guia explica, de forma simples, **o que você encontra** em cada uma, **como fazer a moderação do dia a dia** (buscar uma conta, banir, dar moedas, corrigir um personagem, encontrar um item) e **onde configurar** cada coisa. Não é necessário nenhum conhecimento técnico.

---

## O que são estas telas?

São as ferramentas de **operação diária** do servidor, direto no painel, sem precisar abrir o banco do jogo:

- **Contas** — ficha completa do jogador: dados, senha, VIP, carteiras e moedas (com depósito, saque e extrato), baú, logs, histórico financeiro, banimento.
- **Personagens** — lista e edição de qualquer personagem (level, resets, pontos, atributos, mapa, Zen, Ruud, status de PK) e a lista de **quem está online agora**, com opção de desconectar.
- **Itens** — o catálogo de itens do servidor usado pelo site inteiro (loja, mercado, caixas, baú): importar da season, trocar imagens, localizar um item pelo serial e classificar por **raridade**.

Tudo o que você altera por aqui fica registrado no log interno do painel (**Logs → Interno**), com o nome do administrador e o que mudou.

---

## Conceitos principais

### Conta e personagem

A **conta** é o login do jogador; cada conta tem vários **personagens**. Carteiras, moedas, VIP, baú e Personal ID são da **conta**; level, resets, inventário, Zen e Ruud são do **personagem**.

### Carteiras e moedas

- **Carteiras** guardam **dinheiro real** (em reais, dólares etc.) — é o saldo que o jogador usa em compras e que entra via doação.
- **Moedas** são as moedas do jogo (WCoin, Goblin Point e as que você criar) usadas em serviços, loja e caixas.

Nas duas, o painel permite **Depósito**, **Saque** e consulta de **Transações**.

### Banimento

Um banimento tem **Dias**, **Motivo** (o jogador vê) e **Observações** (internas). A conta banida fica bloqueada no site e no jogo e o histórico de bloqueios fica guardado na ficha da conta.

### Catálogo de itens e raridades

O **catálogo** é a lista de itens do servidor, importada do arquivo de itens da sua season. Cada item pode receber uma **raridade** (Comum, Incomum, Raro, Épico, Lendário, Mítico — ou as que você criar), que é só uma **etiqueta visual com cor**: a loja (WebShop), o mercado de itens e as caixas (LootBox) usam essa cor e esse nome para destacar o item para o jogador.

---

## Contas

### Buscar uma conta

Abra **Contas → Todas contas**. A lista mostra **Conta**, **Nome**, **E-mail**, **Último IP**, **Status** (Online/Offline) e **Última conexão**; contas banidas aparecem com a etiqueta **BLOQUEADO**.

- A busca rápida procura pelo **nome da conta**.
- Em **Filtros** você pode combinar **Conta**, **E-mail**, **Último IP**, **Personagem** (acha a conta pelo nome do personagem) e a chave **Contas banidas**. Clique em **Aplicar**; **Limpar** zera os filtros.
- Clique no nome da conta ou no botão de editar para abrir a ficha.

### A ficha da conta (Editar conta)

No topo da ficha ficam os botões **Lista**, **Baú**, **Logs**, **Histórico financeiro** e **Banir** (ou **Remover banimento**, se já estiver banida).

**Card Conta**

| Campo | O que faz |
|-------|-----------|
| **Nome** | Nome do jogador (obrigatório). |
| **Senha** | Digite para **trocar** a senha. Deixe em branco para manter a atual. |
| **E-mail** / **Telefone** | Contato do jogador. |
| **E-mail confirmado** | Marca o e-mail como verificado (útil para liberar uma conta cujo e-mail de confirmação não chegou). |
| **2FA ativado** | Desligue para **redefinir a autenticação em duas etapas** de um jogador que perdeu o aplicativo. |
| **Documento** | É o **Personal ID** do jogador. Use para recuperar o acesso de quem esqueceu. |
| **País** | País da conta. |
| **Pergunta secreta** / **Resposta secreta** | Só aparecem quando o cadastro do site usa perguntas secretas. |
| **Usuário**, **Criado em**, **Status**, **Online** | Somente leitura: login, data de criação, Normal/BLOQUEADO e se está no jogo agora. |

**Card VIP** (quando o sistema VIP está ativo): **VIP** (o tipo) e **Vencimento** (data de expiração). Para dar ou estender VIP manualmente, escolha o tipo e a data e salve.

**Card Histórico de bloqueios**: todos os banimentos da conta, com **Período**, **Motivo** e **Observações**.

Clique em **Salvar** ao final. Só os campos que mudaram são gravados no log interno.

### Carteiras e moedas (depósito, saque e extrato)

Na mesma ficha, os cards **Carteiras** e **Moedas** listam cada carteira/moeda com o **Saldo** e três botões:

- **Transações** — abre o extrato daquela carteira ou moeda (**Data**, **Descrição**, **Valor**; débitos em vermelho, créditos em verde).
- **Depósito** (botão verde) — abre uma janela com **Valor** ("Valor a adicionar ao saldo") e **Descrição** ("Observação opcional para esta transação"). Confirme em **Depósito**.
- **Saque** (botão vermelho) — mesma janela, com "Valor a subtrair do saldo". Confirme em **Saque**.

A descrição que você escrever aparece no extrato do jogador, então vale escrever algo claro ("Compensação evento 12/05"). Cada depósito e saque também vai para o log interno com o nome do administrador.

### Histórico financeiro

O botão **Histórico financeiro** (ao lado de **Logs** e **Baú**) abre as movimentações financeiras da conta: **Data**, **Ativo** (carteira ou moeda), **Categoria**, **Descrição** e **Valor** (crédito ou débito). Mostra as **100 últimas** movimentações; quem tem acesso ao módulo Financeiro vê o botão **Extrato completo** para ir ao extrato geral.

### Logs da conta

O botão **Logs** abre tudo o que o jogador fez no site: resets, trocas de nick e classe, transferências de resets/Ruud/VIP (enviadas e recebidas), limpezas, trocas de senha e e-mail etc., com **Data**, **Log** e **Tipo**. Para procurar em todas as contas de uma vez, use **Logs → Contas**.

### Banir e desbanir

Há dois caminhos:

1. **Pela ficha da conta** — clique em **Banir**. Preencha **Motivo** ("Motivo do banimento", o jogador vê), **Observações** ("Notas internas, não visíveis ao jogador") e **Dias** ("Número de dias que o banimento vai durar"). Salve.
2. **Pelo menu** — **Contas → Banir conta**, quando você sabe o nome mas não quer abrir a ficha. O campo **Conta** sugere contas conforme você digita; os demais campos são os mesmos.

A conta banida é bloqueada imediatamente. O jogador, ao entrar no site, vê "Sua conta está banida", o **motivo** e a data **Bloqueado até**. Para liberar, abra a ficha e clique em **Remover banimento** (pede confirmação). Não é possível banir uma conta que já está banida — remova o banimento atual antes.

### Forçar logout (desconectar do jogo)

Abra **Personagens → Personagens online** e clique em **Desconectar** na linha do jogador (pede confirmação). A conta é derrubada do servidor do jogo. É o que você usa antes de editar o baú ou um personagem de quem está online.

### Editor de baú

O botão **Baú** na ficha abre o editor visual do baú da conta.

- Se o servidor tem baús estendidos, escolha no seletor entre **Baú** e **Baú estendido 1, 2…**.
- O botão **Zen** mostra o Zen guardado; clique para abrir **Editar Zen** e alterar.
- **Arraste** os itens pela grade para reorganizar; o **X** remove um item ("Remover este item?").
- Clique num item para abrir **Editar item** no painel ao lado, ajustar as opções e **Atualizar item**.
- Para incluir um item, use o painel **Adicionar item**: escolha o item, as opções (level, luck, excellent, ancient, sockets etc.), a **Quantidade** e clique em **Adicionar ao baú**. Clique antes numa célula vazia para escolher onde a peça entra; sem isso, ela vai para o primeiro espaço livre. Se não couber, o painel avisa.
- As alterações são **salvas automaticamente** (aparece "Salvo"). O jogador precisa estar **fora do jogo**; se estiver online, o painel recusa salvar.

---

## Personagens

### Listar e filtrar

**Personagens → Todos personagens** mostra **Nome**, **Classe**, **Conta** (clicável, abre a ficha da conta), **Guild**, **Status** (Online/Offline) e **Mapa** com as coordenadas. Personagens com status de banido recebem a etiqueta **BANIDO**.

Busca rápida pelo **Nome**. **Filtros**: **Nome**, **Conta**, **Guild**, **Classe**, **Mapa**, **Personagens online** e **Personagens banidos**.

### Editar personagem

Clique no nome para abrir **Editar personagem**. Lembre de **desconectar** o jogador antes, para que o jogo não sobrescreva o que você salvar.

| Card | Campos |
|------|--------|
| **Personagem** | **Nome** (trocar aqui renomeia o personagem), **Conta** (link para a ficha), **Level**, **Experiência**, **Pontos** (pontos livres), **Classe**, **Tipo** (Normal, Banned, Game Master, Game Master-ADM), **Nível PK** (Hero Player 2, Hero Player 1, Normal, Player Killer 1, Player Killer 2), **Mapa**, **Coordenada X** e **Coordenada Y**, **Força**, **Agilidade**, **Energia**, **Vitalidade** e **Comando** (só para classes que têm comando). |
| **Dinheiro** | **Zen** e **Ruud** (Ruud só em servidores que o possuem). |
| **Resets** | **Resets** e **Master Resets** (conforme o que o servidor usa). |
| **Inventário de muuns** | Somente leitura, em servidores com muuns: **Slot**, **Muun**, **Rank**, **Opção** e **Expira em**. |

O painel valida os limites: level entre 1 e o máximo do servidor, atributos entre 0 e o máximo de pontos do servidor. Alterar o **Tipo** para "Banned" bloqueia só aquele personagem (diferente do banimento da conta). Tudo o que mudou vai para o log interno.

### Jogadores online

**Personagens → Personagens online** (tela **Jogadores online**) lista quem está no jogo agora: **Servidor**, **Personagem**, **Conta**, **Tempo online** e **IP**. Em cada linha:

- **Personagem no mapa** — abre o mapa com um marcador na posição atual.
- **Desconectar** — derruba a conta do jogo (pede confirmação).

---

## Itens

### O catálogo

**Itens → Todos os itens** mostra o catálogo em grade, com imagem e nome. Busca rápida pelo **Nome**; **Filtros** por **Nome**, **Categoria** (armas, armaduras, asas, etc.) e **Raridade**.

Em cada item:

- As **bolinhas coloridas** são as raridades: clique numa para **aplicar** aquela raridade ao item; clique de novo na mesma para **remover**. A borda do item ganha a cor da raridade.
- **Alterar imagem** abre uma janela com o campo **Imagem**: envie um arquivo de imagem para substituir a figura usada no site inteiro (loja, baú, tooltips).

No topo da lista estão os botões **Procurar item**, **Raridades** e **Importar**.

### Importar itens

Use quando instalar o Morpheus, trocar de season ou adicionar itens customizados no servidor. Em **Importar itens**:

1. **Itens** — envie o arquivo de itens da sua season (texto ou XML, o mesmo usado pelos arquivos do servidor).
2. **Categorias** — por padrão todas marcadas; desmarque as que não quer importar.
3. **Apagar itens e importar novamente** — desligado, a importação só **adiciona** itens que ainda não existem (as raridades e imagens já definidas são preservadas). Ligado, apaga os itens das categorias marcadas e importa do zero.
4. Clique em **Importar**. O painel informa quantos itens foram adicionados.

### Procurar item

Para saber **onde está** um item (por exemplo, numa suspeita de duplicação), clique em **Procurar item** e cole o código do item ou só o seu serial no campo **Pesquisar por hexa ou serial**. O resultado diz se o item foi encontrado **no armazém**, **no inventário** de algum personagem ou **no armazém estendido**, com link para a conta/personagem e o botão **Visualizar**, que abre o editor de baú já com o item em destaque.

### Raridades

**Itens → Raridades** lista as raridades com **Nome** e **Cor**. Vêm instaladas: **Comum**, **Incomum**, **Raro**, **Épico**, **Lendário** e **Mítico**.

- **Reordenar**: arraste as linhas; a ordem define como as raridades aparecem nos filtros e nas bolinhas do catálogo.
- **Adicionar** (tela **Adicionar raridade**): **Nome** (em cada idioma do site) e **Cor** (seletor de cor). **Editar** e **Excluir** na própria linha.
- **Aplicar** a um item: é feito no catálogo, pelas bolinhas coloridas (veja acima).

**Para que servem:** a raridade é lida automaticamente pelos plugins que exibem itens ao jogador. Na **Loja** (WebShop) e no **Mercado de itens**, o produto ganha a borda na cor da raridade e uma etiqueta com o nome; nas **caixas** (LootBox) a raridade de cada item possível aparece na lista de recompensas. Você não precisa configurar nada nesses plugins: basta classificar o item no catálogo.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|-----------------------|-----------------|
| Procurar uma conta por login, e-mail, IP ou nome de personagem | **Contas → Todas contas** → **Filtros** |
| Trocar senha, e-mail, Personal ID (campo **Documento**), país ou redefinir o 2FA | **Contas → Todas contas** → abrir a conta → card **Conta** |
| Dar, estender ou remover VIP manualmente | **Contas → Todas contas** → abrir a conta → card **VIP** |
| Dar ou retirar moedas ou saldo em dinheiro, ver o extrato | **Contas → Todas contas** → abrir a conta → cards **Carteiras** e **Moedas** (**Depósito**, **Saque**, **Transações**) |
| Ver as movimentações financeiras de uma conta | Ficha da conta → botão **Histórico financeiro** |
| Ver o que o jogador fez no site | Ficha da conta → botão **Logs**; ou **Logs → Contas** para todas |
| Banir com motivo e prazo | Ficha da conta → **Banir**, ou **Contas → Banir conta** |
| Desbanir | Ficha da conta → **Remover banimento** |
| Derrubar um jogador do jogo | **Personagens → Personagens online** → **Desconectar** |
| Ver ou editar o baú, colocar ou remover itens, alterar Zen do baú | Ficha da conta → botão **Baú** |
| Corrigir level, resets, pontos, atributos, Zen, Ruud, mapa ou classe | **Personagens → Todos personagens** → abrir o personagem |
| Tirar o status de PK ou marcar um personagem como banido/GM | Editar personagem → **Nível PK** e **Tipo** |
| Ver onde um personagem online está no mapa | **Personagens → Personagens online** → **Personagem no mapa** |
| Importar os itens da season | **Itens → Todos os itens** → **Importar** |
| Trocar a imagem de um item | **Itens → Todos os itens** → **Alterar imagem** no item |
| Descobrir em qual conta/personagem está um item | **Itens → Todos os itens** → **Procurar item** |
| Criar, renomear, colorir ou reordenar raridades | **Itens → Raridades** |
| Aplicar uma raridade a um item | **Itens → Todos os itens** → bolinhas de cor no item |
| Criar novas moedas ou carteiras | **Configurações → Economia → Moedas** / **Carteiras** |
| Alterar os tipos de VIP disponíveis | **Configurações → Economia → Sistema VIP** |
| Limitar o que cada administrador pode fazer nestas telas | **Configurações → Usuários → Grupos** |

---

## Dicas e boas práticas

- **Desconecte antes de editar.** Personagem ou baú de quem está online: use **Desconectar** em **Personagens online** primeiro, senão o jogo pode sobrescrever a sua alteração.
- **Escreva a descrição nos depósitos e saques.** Ela aparece no extrato do jogador e evita tickets do tipo "de onde veio isso?".
- **Use Observações no banimento para a equipe** (provas, link do ticket) e **Motivo para o jogador** — ele vê o motivo na própria conta.
- **Prefira banir a conta** em vez de marcar cada personagem como "Banned": o banimento da conta tem prazo, motivo e histórico.
- **Dê permissões por grupo.** Nem todo moderador precisa de **Depósito**/**Saque** ou do editor de baú; restrinja em **Configurações → Usuários → Grupos**.
- **Importe os itens logo após trocar de season** e mantenha as raridades: a importação sem "Apagar itens e importar novamente" preserva o que você já classificou.
- **Padronize as raridades** antes de montar loja e caixas, assim a mesma cor significa a mesma coisa em todo o site.

---

## Perguntas frequentes

**Dei moedas pelo painel e o jogador diz que não apareceu.**
Abra **Transações** na moeda da conta e confira o lançamento. Se estiver lá, peça para o jogador atualizar a página do painel da conta; o saldo da moeda é lido direto da conta.

**O jogador perdeu o Personal ID. Onde vejo?**
Na ficha da conta, campo **Documento** (card **Conta**). Você pode informar o atual ou definir um novo e salvar.

**O jogador perdeu o celular do 2FA e não consegue entrar.**
Na ficha da conta, desligue **2FA ativado** e salve. Ele entra só com a senha e pode ativar o 2FA de novo pelo painel da conta.

**Para que serve o campo Dias do banimento?**
Ele define a data **Bloqueado até**, que o jogador vê na própria conta e que fica no **Histórico de bloqueios**. Para liberar a conta — no prazo ou antes dele — use **Remover banimento** na ficha.

**Qual a diferença entre banir a conta e o Tipo "Banned" do personagem?**
Banir a conta bloqueia o login, tem motivo, prazo e histórico. O **Tipo** do personagem é o status do próprio jogo, por personagem, sem prazo nem motivo; use-o para casos pontuais.

**Por que o editor de baú não deixa salvar?**
Porque o jogador está online. Desconecte-o em **Personagens → Personagens online** e tente de novo.

**Troquei de season e os itens novos não aparecem na loja nem no baú.**
Importe o arquivo de itens da season em **Itens → Todos os itens → Importar**. Só itens que estão no catálogo podem ser usados pelo site.

**Posso apagar uma raridade que está em uso?**
Pode, pela lixeira em **Itens → Raridades**; os itens que a usavam ficam sem raridade (sem cor nem etiqueta) até você classificar de novo.

---

> Precisa de ajuda com um caso de moderação ou com a importação dos itens da sua season? Entre em contato com o suporte.
