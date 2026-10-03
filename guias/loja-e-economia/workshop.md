# Oficina — Guia do Cliente

No painel este recurso aparece como **WorkShop**; para o jogador, o serviço se chama **Oficina**. Este guia explica, de forma simples, o que é a Oficina, como o jogador melhora os itens e como você define as regras e os preços pelo painel administrativo. Não é necessário conhecimento técnico.

---

## O que é a Oficina?

A Oficina permite que o jogador **melhore os itens que já possui**, pagando com as **moedas** do site. Em vez de comprar um item novo, ele pega um item do próprio inventário ou do baú e **adiciona, troca ou remove atributos** (level, option, skill, luck, ancient, excellent, refine, harmony, socket, mastery, elemento, pentagrama e errtel), e o item é **atualizado no lugar**.

É uma ferramenta de **monetização e progressão**: o jogador evolui os itens favoritos pagando exatamente pelo que escolher.

---

## Conceitos principais

### A regra

É o que define **o que pode ser melhorado** e até onde. Cada regra tem um **Nome** obrigatório e um alcance:

- um **item específico** (escolhendo **Categoria** e **Item**),
- uma **categoria inteira** do jogo (escolhendo só a **Categoria**),
- ou **todos os itens** (sem categoria nem item, a regra geral).

Quando o jogador abre um item, vale a regra mais específica que estiver ativa: primeiro a do item, depois a da categoria e, por último, a geral. Na regra você define **o que é permitido** (ancient, refine, harmony, mastery, socket e combinações) e os **limites** (level, option, excellent, socket, pentagrama e errtel máximos).

### Os preços

Cada regra tem uma ou mais tabelas de **Preços**, **uma por moeda**. Assim a mesma melhoria pode custar X de uma moeda ou Y de outra, e o jogador escolhe com qual pagar. Os preços são **por valor alcançado** (cada level e cada option com um preço, cada opção excellent ou socket adicionada com um preço) ou um valor único por atributo. Também há preço para **remover** opções excellent, socket, pentagrama e errtel.

### O cálculo na hora

Quando o jogador monta a melhoria, o site **soma os preços** dos atributos alterados e mostra o total. Ele precisa estar **fora do jogo** e ter saldo na moeda escolhida; ao confirmar, a moeda é descontada e o item é atualizado no inventário ou no baú.

### Itens bloqueados

Em **Configurações → WorkShop** você marca itens que **nunca** podem ser melhorados, mesmo que exista uma regra geral que os alcance.

---

## Como o jogador usa

1. No painel dele, o jogador abre o serviço **Oficina** e escolhe entre **Inventório** (itens de um personagem) ou **Baú** (baú normal ou estendido).
2. Clica no item que quer melhorar. A tela mostra apenas os atributos liberados pela **regra** daquele item e o preço de cada alteração.
3. Ajusta o que quiser (level, option, skill, luck, ancient, opções excellent, refine, harmony, socket, mastery, elemento, pentagrama ou errtel), escolhe a **moeda** e clica em **Melhorar** (precisa estar fora do jogo).
4. O valor é descontado e o item é atualizado na hora.

---

## Como configurar (passo a passo)

As regras ficam no menu lateral **WorkShop → Regras**. Os itens bloqueados ficam em **Configurações → WorkShop**.

### 1. Criar uma regra

1. Vá em **WorkShop → Regras** e clique em **Adicionar**.
2. No card **Configurações**, informe o **Nome**, ligue **Ativo** e escolha o alcance: deixe **Categoria** e **Item** vazios para uma regra geral, escolha só a **Categoria** para uma categoria inteira ou escolha **Categoria** e **Item** para um item específico.
3. No card **Liberar opções**, ligue o que o jogador poderá mexer: **Liberar ancient**, **Liberar ancient + exc.**, **Liberar ancient + socket**, **Liberar refine**, **Liberar harmony**, **Liberar mastery** e **Allow mastery bonus** (as opções aparecem conforme o que o seu servidor suporta). Para socket, escolha em **Allow socket** entre **Todos** e **Apenas vazio** e, em **Sockets únicos**, entre **Por código** e **Por tipo**.
4. No card **Max options**, defina **Max level**, **Max option**, **Max excellent** e, se o servidor tiver, **Max socket**, **Max pentagram** e **Max errtel**.
5. Clique em **Salvar**.

### 2. Definir os preços da regra

Os preços só são acessados pela tela de edição da regra.

1. Em **WorkShop → Regras**, abra a regra para editar e clique em **Preços** no topo.
2. Clique em **Adicionar** e escolha a **Moeda**.
3. Preencha os valores:
   - **Level:** um preço para cada level (+0, +1, +2 e assim por diante).
   - **Option:** um preço para cada option (+0, +4, +8...).
   - **Excellent:** um preço para cada opção adicionada (#1 a #6) e um preço em **Remover**.
   - **Skill**, **Luck**, **Ancient**, **Harmony**, **Refine** e **Mastery Bonus**: um valor único cada.
   - **Socket:** um preço por socket adicionado (#1 a #5) e um preço em **Remover**.
   - **Elemento**, **Pentagrama** (#1 a #5 e **Remover**), **Errtel Option** (#1 a #5 e **Remover**) e **Errtel Level** (#1 a #10), quando o servidor tem pentagrama.
4. Clique em **Salvar**. Repita para cada moeda que você quiser aceitar nessa regra.

### 3. Bloquear itens

Em **Configurações → WorkShop**, o card **Ítens bloqueados** lista todos os itens do jogo. Marque os que nunca poderão passar pela Oficina e clique em **Salvar**.

### 4. Acompanhar

Em **WorkShop → Regras**, clique em **Estatísticas** no topo da lista para ver **Regras ativas**, **Total de regras**, **Tabelas de preço** e **Aprimoramentos** realizados, além da tabela de regras com quantas tabelas de preço cada uma tem.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|------------------------|-----------------|
| Definir o que pode ser melhorado | **WorkShop → Regras → Adicionar** |
| Regra para um item, uma categoria ou todos | Campos **Categoria** e **Item** da regra |
| Liberar ancient, refine, harmony, mastery e socket | Card **Liberar opções** da regra |
| Limites de level, option, excellent, socket, pentagrama e errtel | Card **Max options** da regra |
| Definir preços por moeda | Editar a regra → botão **Preços** → **Adicionar** |
| Cobrar pela remoção de excellent, socket, pentagrama ou errtel | Campos **Remover** na tabela de preços |
| Impedir que certos itens sejam melhorados | **Configurações → WorkShop → Ítens bloqueados** |
| Ativar ou desativar uma regra | Interruptor **Ativo** da regra |
| Ver desempenho | **WorkShop → Regras → Estatísticas** |

---

## Dicas e boas práticas

- Comece com uma **regra geral** e crie regras específicas só para categorias ou itens que precisam de tratamento diferente. A regra mais específica sempre vence.
- Uma regra sem tabela de **Preços** não permite melhorar nada: cadastre ao menos uma moeda.
- Defina **limites** coerentes com o equilíbrio do servidor (level, option e excellent máximos).
- Ofereça **mais de uma moeda** por regra para dar opções de pagamento ao jogador.
- Deixe os levels e options mais altos mais caros na tabela de preços para encarecer a progressão de forma gradual.
- Use os campos **Remover** para cobrar quando o jogador tira opções do item, ou deixe em branco para permitir de graça.
- Acompanhe os **Aprimoramentos** nas estatísticas para entender o uso da Oficina.

---

## Perguntas frequentes

**O item muda ou é criado um novo?**
O **mesmo item** é atualizado no lugar, sem criar um item novo.

**Com que moeda se paga?**
Com qualquer uma das moedas que tenham tabela de **Preços** na regra; o jogador escolhe na hora.

**Por que o jogador precisa estar fora do jogo?**
Por segurança: o item está na conta e não pode estar em uso no jogo durante a alteração.

**Posso impedir que certos itens sejam melhorados?**
Sim, marcando-os em **Configurações → WorkShop → Ítens bloqueados**. Itens sem nenhuma regra ativa que os alcance também não podem ser melhorados.

**O jogador pode remover opções do item?**
Sim, quando a regra libera o atributo. A remoção de opções excellent, socket, pentagrama e errtel é cobrada pelo valor do campo **Remover** da tabela de preços.

**O que acontece se o jogador não tiver saldo?**
A melhoria é recusada e o item não muda. Ele precisa ter saldo suficiente na moeda escolhida.
