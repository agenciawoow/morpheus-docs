# Loja Virtual — Guia do Cliente

No painel este recurso aparece como **WebShop**; para o jogador, o serviço se chama **Loja Virtual**. Este guia explica, de forma simples, o que é a Loja Virtual, como o jogador compra e como você monta a loja pelo painel administrativo. Não é necessário conhecimento técnico.

---

## O que é a Loja Virtual?

A Loja Virtual é onde o jogador **compra itens do jogo** usando as **moedas** do site (WCoin, Goblin Point e outras). Diferente de um pacote fixo, aqui o jogador pode **personalizar o item** na hora (nível, opção, excellent, socket, ancient, harmony, pentagrama e mais) e o item é **entregue direto no baú** da conta.

É a principal ferramenta de **monetização e conveniência**: o jogador monta exatamente o item que quer e paga pelo que escolher.

---

## Conceitos principais

### A loja

É um catálogo. Você pode ter **várias lojas** (por exemplo *Loja de Itens* e *Loja de Asas*), cada uma com **nome e descrição em vários idiomas**, uma **imagem**, uma **moeda** própria e regras próprias: nível e opção máximos, limites de excellent, socket, pentagrama e errtel, e **preços padrões** dos atributos. As lojas podem ser **reordenadas** arrastando na lista.

### As categorias

Organizam os produtos dentro de cada loja (por exemplo *Armas*, *Armaduras*, *Asas*). Têm nome em vários idiomas, ícone, podem ter uma **categoria pai** e são reordenadas arrastando.

### O produto

É o item à venda. Tem um **preço normal** e **preços por atributo** (por level, por option, por excellent, por socket e assim por diante). Quando o jogador adiciona atributos, o preço sobe conforme os seus valores. O produto pode ser marcado como **Oferta**, ter **Estoque** limitado, uma **Quantidade do item** fixa ou em faixa, atributos fixos (level, option, durabilidade) e pode ser **temporário**, expirando um certo número de minutos após a compra.

### O kit

É um **conjunto de itens** vendido como um pacote único, por um preço fechado. Você monta os itens do kit (cada um com seus atributos e quantidade) e, na compra, **todos** vão para o baú de uma vez. Kits não podem ser recuperados depois.

### A compra e a entrega

O jogador precisa estar **fora do jogo** para comprar. O valor é descontado da **moeda** da loja e o item é **gerado e entregue no baú**. Cada compra fica registrada em **Minhas Compras → Loja Virtual**, no painel do jogador, e itens elegíveis podem ser **recuperados** para o baú novamente.

### Cupons

Se o recurso de **Cupons** estiver ativo, o jogador pode informar um **Cupon de desconto** na tela do produto. Valem na loja os cupons de **percentual** e de **valor fixo**, respeitando o **desconto máximo** do cupom. Veja o guia de Cupons para criar e limitar cupons.

---

## Como o jogador usa

1. O jogador abre a página de lojas do site (quando há só uma loja ativa, entra direto nela), navega pelas **categorias** ou usa a **busca**.
2. Escolhe um produto e **personaliza**: level, option, skill, luck, ancient, opções excellent, harmony, socket e, conforme o item, grau da asa, guardião, elemento, errtel. O preço é recalculado na hora.
3. Se o produto tem faixa de quantidade, escolhe quantas unidades quer. Se tem cupom, informa em **Cupon de desconto**.
4. Clica em **Comprar** (precisa estar fora do jogo). A moeda é descontada e o item cai no **baú**.
5. Em **Minhas Compras → Loja Virtual**, no painel dele, vê o histórico e pode clicar em **Recuperar** para trazer um item elegível de volta ao baú.

### O que o jogador pode personalizar

- **Opções básicas:** level, option, skill, luck e ancient, conforme o que você liberar no produto. Level e option respeitam o máximo da loja.
- **Opções excellent:** o seletor mostra apenas as opções que o item realmente aceita, limitado ao **Máximo de opções excellent** do produto.
- **Harmony e socket:** quando liberados no produto; socket e harmony não podem ser combinados no mesmo item.
- **Asa:** itens com grau de asa permitem escolher o **Grau da asa**, cobrado pelo preço por excellent.
- **Guardião:** itens com bônus de guardião permitem escolher o **Bônus do guardião**, cobrado pelo preço por excellent.
- **Brinco:** vem com as **Opções incluídas** do próprio item (até cinco), sem escolha extra.
- **Pentagrama:** o jogador escolhe **Elemento principal**, **Elemento adicional**, os **Slots** e pode **Montar errtel** em cada slot (errtel, nível e opções de rank). Cada slot e cada errtel montado soma ao preço.
- **Errtel:** o jogador escolhe o **Elemento**, o **Level** e as opções de rank dos **Slots**.
- **Quantidade:** quando o produto tem faixa (por exemplo de 1 a 10), o jogador escolhe quantas unidades leva; o preço é **por unidade** e o estoque é consumido na mesma quantidade.
- **Item temporário:** a tela avisa que o item expira um certo tempo após a compra e ele vence no prazo definido.

---

## Como montar a loja (passo a passo)

As telas ficam no menu lateral **WebShop**, com os itens **Lojas**, **Produtos** e **Kits**. As opções gerais ficam em **Configurações → WebShop**.

### 1. Criar a loja

1. Vá em **WebShop → Lojas** e clique em **Adicionar**.
2. No card **Loja**, informe o **Nome** (em cada idioma), ligue **Ativo**, escreva a **Descrição** (em cada idioma), escolha a **Moeda** e envie uma **Imagem**.
3. No card **Configurações**, defina **Máximo de level**, **Máximo de option** e **Máximo de opções excellent**. Se o servidor tiver socket, defina **Liberar sockets**, **Máximo de opções de socket** e **Sockets únicos**. Se tiver pentagrama, defina **Max pentagram options** e **Max errtel options**.
4. No card **Preços padrões**, informe os preços de **level**, **option**, **skill**, **luck**, **excellent**, **ancient**, **harmony**, **refine**, **socket** e, se houver pentagrama, de **element**, **pentagram** e **errtel**. Esses valores são copiados para cada produto importado.
5. Clique em **Salvar**. Para mudar a ordem das lojas no site, arraste as linhas na lista.

### 2. Criar as categorias

1. Em **WebShop → Lojas**, clique no botão de categorias da linha da loja.
2. Clique em **Adicionar**: informe o **Nome** (em cada idioma), ligue **Ativo**, escolha a **Item category** (categoria do jogo que esta categoria representa), a **Categoria pai** (para criar subcategorias) e envie um **Ícone**.
3. Arraste as categorias na árvore para reordenar.

### 3. Cadastrar os produtos

Você pode cadastrar um a um ou importar em lote.

**Importar em lote**

1. Em **WebShop → Produtos**, clique em **Importar** no topo da lista.
2. Escolha a **Loja** e marque as **Categorias** do jogo que deseja importar, depois clique em **Importar**.
3. Todos os itens dessas categorias entram **desativados**, com os preços padrões da loja, dentro da categoria da loja cuja **Item category** corresponde. Itens que já existem na loja são ignorados. Depois é só revisar, ajustar preços e ativar.

**Cadastrar um a um**

1. Em **WebShop → Produtos**, clique em **Adicionar**.
2. Ligue **Ativo** e, se quiser destacar, **Oferta**. Informe o **Nome**, escolha a **Loja** e a **Categoria**, envie uma **Imagem**, defina o **Estoque** (vazio = ilimitado) e a **Quantidade do item** (um número fixo, ou uma faixa como 1-10 para o jogador escolher).
3. Em **Preços**, informe o **Preço normal** e o **Preço por level**.
4. Em **Item**, pesquise e selecione o item do jogo. Em **Configurações**, defina **Level fixo em**, **Option fixo em**, **Fix durability** e **Período (minutos)** (preencha para vender como item temporário). Ligue o que o jogador poderá escolher: **Ancient**, **Luck**, **Skill**, **Refine**, **Harmony**, **Sockets**, e os limites **Máximo de opções excellent**, **Máximo de opções de socket**, **Max pentagram options** e **Max errtel options**.
5. Em **Preços do item**, informe o preço de cada atributo que o jogador pode adicionar (option, skill, luck, excellent, ancient, harmony, refine, socket, element, pentagram e errtel).
6. Clique em **Salvar**.

Na lista de produtos, use os filtros **Produto** e **Loja** para localizar, marque várias linhas e use **Ações** para **Ativar**, **Desativar** ou **Excluir** em massa.

### 4. Montar kits (opcional)

1. Em **WebShop → Kits**, clique em **Adicionar**.
2. Informe o **Nome**, ligue **Ativo** e, se quiser, **Oferta**; escolha a **Loja** e a **Categoria**, envie uma **Imagem**, defina o **Preço** e o **Estoque**. Clique em **Salvar**.
3. Abra o kit para editar e clique em **Itens** no topo. Clique em **Adicionar**, escolha o item do jogo, monte os atributos dele, informe a **Quantidade** e salve. Repita para cada item do kit.

A lista de kits também tem **Ações** em massa para **Ativar**, **Desativar** e **Excluir**.

### 5. Bloquear itens para recuperação

Em **Configurações → WebShop**, o card **Ítens bloqueado para recuperação** lista todos os itens do jogo. Marque os que o jogador **não** poderá trazer de volta ao baú pela tela de compras e clique em **Salvar**.

### 6. Acompanhar

Em **WebShop → Lojas**, clique em **Estatísticas** no topo da lista para ver **Lojas ativas**, **Produtos ativos**, **Kits / Ofertas**, **Itens vendidos** e a tabela **Produtos por loja** com os itens vendidos de cada uma.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|------------------------|-----------------|
| Criar ou editar lojas | **WebShop → Lojas → Adicionar** / botão de editar |
| Nome, descrição e imagem da loja | Card **Loja** do formulário da loja |
| Limites de level, option, excellent, socket, pentagrama e errtel da loja | Card **Configurações** do formulário da loja |
| Preços padrões dos atributos | Card **Preços padrões** do formulário da loja |
| Ordem das lojas no site | Arrastar as linhas em **WebShop → Lojas** |
| Criar categorias e subcategorias | Botão de categorias na linha da loja → **Adicionar** |
| Ordem das categorias | Arrastar na árvore de categorias da loja |
| Cadastrar produtos um a um | **WebShop → Produtos → Adicionar** |
| Importar produtos em lote | **WebShop → Produtos → Importar** |
| Preço do produto e dos atributos | Cards **Preços** e **Preços do item** do produto |
| Produto temporário | Campo **Período (minutos)** do produto |
| Faixa de quantidade | Campo **Quantidade do item** (por exemplo 1-10) |
| Ativar, desativar ou excluir vários produtos | Selecionar linhas em **WebShop → Produtos** → **Ações** |
| Montar kits | **WebShop → Kits → Adicionar**, depois **Itens** na edição do kit |
| Ativar, desativar ou excluir vários kits | Selecionar linhas em **WebShop → Kits** → **Ações** |
| Impedir a recuperação de certos itens | **Configurações → WebShop → Ítens bloqueado para recuperação** |
| Ver desempenho | **WebShop → Lojas → Estatísticas** |

---

## Dicas e boas práticas

- Preencha os **Preços padrões** da loja antes de **Importar**: os produtos importados já nascem com esses valores, e você só ajusta as exceções.
- Produtos importados entram **desativados**. Revise, ajuste e ative aos poucos para não abrir uma loja incompleta.
- Use **Oferta** para destacar os itens que você quer vender mais e **Estoque** para criar escassez em itens especiais.
- Limite **Máximo de level**, **Máximo de option** e os máximos de excellent e socket por loja para manter o equilíbrio do servidor.
- Use **Período (minutos)** para vender itens de teste ou de evento, que somem sozinhos depois do prazo.
- Use **kits** para vender conjuntos prontos (sets, kits iniciais) com um preço atraente.
- Bloqueie a recuperação de itens que não devem voltar ao baú (por exemplo itens consumíveis ou de evento).
- Acompanhe as **Estatísticas** para entender o que mais sai em cada loja.

---

## Perguntas frequentes

**O jogador pode personalizar o item?**
Sim. Ele escolhe level, option, excellent, socket, ancient, harmony e, conforme o item, grau da asa, guardião, elemento e errtel, dentro do que você liberar no produto. O preço é calculado automaticamente.

**Com que moeda se paga?**
Com a **Moeda** configurada na loja. Cada loja pode usar uma moeda diferente.

**O item vai para onde?**
Direto para o **baú** da conta. Por isso o jogador precisa estar **fora do jogo** ao comprar.

**O que acontece se o estoque acabar?**
O produto aparece como venda encerrada e a compra é recusada. Com faixa de quantidade, cada unidade comprada consome uma do estoque.

**Dá para usar cupom de desconto?**
Sim, se o recurso de **Cupons** estiver ativo. Se o cupom se esgotar entre a escolha e o pagamento, a compra é desfeita e nada é cobrado.

**O jogador pode recuperar um item comprado?**
Sim, em **Minhas Compras → Loja Virtual**, desde que o item não esteja bloqueado em **Configurações → WebShop** e não esteja no baú, no inventário ou no mercado. Kits não podem ser recuperados.

**Como vendo um pentagrama já montado?**
Cadastre o pentagrama como produto. Na compra, o jogador escolhe elemento, slots e monta os errtels (com nível e opções de rank) em cada slot, e cada parte soma ao preço conforme os valores de **pentagram** e **errtel** do produto.
