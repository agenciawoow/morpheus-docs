# Novidades do Morpheus

Aqui você acompanha, em linguagem simples, o que mudou no Morpheus a cada atualização: novos recursos, melhorias e correções, tanto no site do servidor quanto no painel administrativo. As mudanças mais recentes aparecem primeiro.

## 02/10/2026
- **Login — Correção:** depois de errar a senha três vezes, o site pedia a verificação anti-robô mas a tela de login não a mostrava, e o jogador ficava preso em "Captcha inválido" por dez minutos mesmo digitando a senha certa. Agora a verificação aparece no formulário quando é exigida e é renovada a cada tentativa. Vale para os plugins ReCaptcha e Turnstile.
- **Mercado de personagens — Novo:** plugin **Venda de personagens**. O jogador anuncia **um personagem** (sem vender a conta) em "Vender personagem", no painel do personagem; enquanto está anunciado, o personagem fica bloqueado no jogo e os serviços do painel sobre ele ficam trancados. Outro jogador compra logado, pelas formas de pagamento do site, e recebe o personagem na própria conta assim que o pagamento confirma, com inventário e equipamentos. Vitrine em **Mercado → Personagens** com busca e filtros por preço, level, resets, master resets e classe. No painel administrativo: comissão, preço mínimo, gateways, tempo de reserva, "remover itens" na entrega, lista de pedidos com vendedor e comprador, repasse, recibo e estatísticas. Regras de segurança: não vende mestre de guild, personagem bloqueado nem personagem de conta que está à venda no Mercado de Contas; anunciar a conta inteira retira os personagens dela do mercado.
- **Documentação — Melhoria:** todos os guias do cliente foram revisados contra o painel atual: caminhos de menu corrigidos (a maioria dos plugins fica em **Configurações → nome do plugin**), nomes de campos iguais aos da tela, telas de Estatísticas e recursos recentes incluídos. Guias novos: Instalação e primeiros passos, Tarefas agendadas e Fila, Atualização e licença, Configurações → Geral, Serviços de personagem e de conta, Contas e personagens, Páginas, Sender (WhatsApp), Assinaturas VIP e Proteção contra bots, além de um índice com ordem de leitura sugerida.

- **IGCN — Correção:** em servidores IGCN (Season 21) o site passou a funcionar com o banco oficial em quatro pontos que antes davam erro: montar e desmontar errtels no pentagrama, registrar o prazo de muuns por tempo, o ranking de Gens (famílias Duprian e Vanert, com total de membros e pontos) e o master level nos rankings de personagem. Nada muda para quem usa outros emuladores.
- **Mercado de contas — Melhoria:** no formulário de vender conta, o campo "Nome de exibição" passou a se chamar "Descrição de venda", deixando claro que é o texto que aparece no anúncio.
- **Painel do jogador — Novo:** plugin **Limpar PK**. O jogador pode limpar o status de PK de um personagem (offline) direto no painel, em "Limpar PK". O preço é definido pelo administrador em Configurações, Serviços, como qualquer outro serviço (grátis, em moeda ou em zen). O administrador escolhe se o Personal ID é exigido e se a contagem de kills também é zerada.

## 01/10/2026

- **Licença — Correção:** sites protegidos pelo Cloudflare ficavam, de tempos em tempos, redirecionados para a página de "licença ilegal" mesmo com a licença em dia. A verificação passou a usar o IP do próprio servidor (e não o do visitante) ao conferir a licença, como era antes. Não é preciso mexer em nada no Cloudflare nem na licença: basta atualizar o Morpheus.
- **Enquetes — Correção:** clicar várias vezes em "Resultado" na enquete do site empilhava o mesmo resultado repetidas vezes. Agora o botão fica desabilitado enquanto o resultado carrega e o bloco anterior é sempre substituído.

## 30/09/2026

- **Documentação — Novo:** o pacote do Morpheus passa a incluir um "skill" de inteligência artificial (pasta `.claude/skills/morpheus` e arquivo `AGENTS.md`) para você criar plugins, telas do painel e integrações com assistentes como Claude Code, Cursor ou Codex, sem precisar ler o código do sistema. Junto vem um plugin de exemplo completo (mural de avisos) usado como modelo. Guia em `docs/plugins-com-ia.md`.
- **Sistema — Novo:** comando `php morpheus make:plugin NomeDoPlugin` cria a estrutura de um plugin novo a partir do exemplo, já com nome, tabelas e traduções ajustados.
- **Conta do jogador — Novo:** o jogador pode editar o próprio nome em **Dados pessoais** no painel da conta. O campo é obrigatório e aceita até 50 caracteres.
- **Recompensa por voto — Melhoria:** o campo "URL do provedor" (ao adicionar e editar um provedor) agora explica as variáveis disponíveis, como `${username}` para a conta do jogador que clicou para votar, com um exemplo de URL.

## 28/09/2026

- **Pagamentos — Correção:** Stripe, PagSeguro, Pagarme e PayPal creditavam o valor cobrado em vez do valor do pedido. Com cupom de 20% o jogador pagava 80 e recebia 80 (o desconto não valia nada), e com taxa de 5% pagava 105 e recebia 105 (o site entregava a própria taxa). Agora todos os gateways creditam o valor do pedido, e se o valor informado pelo gateway não bater com o esperado, o pedido fica pendente para você confirmar manualmente em vez de ser entregue errado. Pedidos em moeda estrangeira passam a creditar o valor nominal do pedido.
- **Pagamentos — Correção:** estornos e chargebacks no Pagarme, PagSeguro e Stripe agora revertem o crédito da conta. Antes, em alguns casos, a carteira do jogador continuava creditada depois do estorno.
- **Cupons — Correção:** o limite de uso do cupom (por quantidade e por conta) passa a valer de verdade: vários checkouts simultâneos com um cupom de uso único não passam mais todos. O cashback só vai para quem de fato usou o cupom, e o estorno só reverte o cashback de quem usou. Na Loja (WebShop), se o cupom esgotar entre a escolha e o pagamento, a compra é desfeita com aviso.
- **Assinatura de VIP — Correção:** a renovação da assinatura não concede mais dois ciclos quando o gateway reenvia o mesmo aviso de fatura paga.
- **Assinatura de VIP, Pacotes, Sorteio, Troca de horas, Conquistas e Passe de Batalha — Melhoria:** ganhar ou comprar VIP nunca mais rebaixa nem zera os dias que o jogador já tem. Com um VIP maior ativo, ganhar um VIP menor soma os dias ao VIP maior. Antes, 7 dias de VIP Bronze por cima de 300 dias de VIP Ouro viravam 7 dias de Bronze. Rebaixar o plano continua possível só pelo painel administrativo.
- **Segurança — Melhoria:** trocar ou redefinir a senha agora encerra as outras sessões abertas da conta (inclusive os cookies de "lembrar de mim"). O link de redefinição de senha só funciona uma vez, mesmo que o programa de e-mail abra o link antes do jogador. Desativar a verificação em duas etapas passa a pedir a senha da conta (ou o código do aplicativo), e um código aceito não vale de novo na mesma janela. Tentativas de login, de "esqueci a senha" e de verificação em duas etapas são contadas corretamente mesmo em rajadas de requisições.
- **Conta do jogador — Correção:** o formulário "Esqueci a senha" não funcionava quando o site não tinha ReCaptcha ou Turnstile configurado. Agora funciona, com limite de tentativas por endereço IP (configurável em `login.forgot_max_tries`).
- **Notificações WhatsApp (Sender) — Melhoria:** novo campo **Segredo do disparo** em Sender → Configurações. Enquanto não configurado, o segredo antigo continua aceito (nada para de funcionar) e o painel mostra uma notificação pedindo para configurar o seu. Depois de configurado, só ele é aceito. Mensagens que o provedor recusou são reenviadas automaticamente em vez de serem perdidas.
- **Contas — Correção:** registrar duas contas com o mesmo e-mail ao mesmo tempo não é mais possível, e tentar criar um usuário que já existe mostra "Usuário já existe" em vez de um erro técnico.
- **Personagens — Correção:** reset, master reset, troca de classe, troca de nick, redistribuição de pontos, mover e reconstruir master skill revalidam os requisitos no momento exato da gravação. Dois cliques simultâneos não aplicam mais um reset "grátis". Limpar o inventário agora exige o personagem fora do jogo, como os demais serviços.
- **Conta do jogador — Correção:** transferir resets, ruud ou VIP entre contas, pagar serviços com zen e comprar horas na Troca de horas não podem mais ser duplicados com dois envios simultâneos. A transferência de VIP deixou de sobrescrever e-mail e bloqueio da conta de destino. Na Troca de horas, comprar VIP com um VIP já vencido passa a funcionar (antes o jogador pagava e não recebia).
- **Passe de Batalha, Conquistas e Leilão — Correção:** entregar um item no baú não apaga mais um item que entrou no baú depois do login. A entrega de recompensas em item do Passe de Batalha e das Conquistas passa a exigir o personagem fora do jogo. O resgate de conquista virou um envio de formulário, mais seguro.
- **Conta do jogador — Correção:** a tela "Reparar itens" dava erro com qualquer item no baú.
- **Recompensa por voto — Melhoria:** novo campo **Segredo do pingback** no provedor GTop100. Sem segredo, a premiação continua funcionando e o painel avisa para configurar; com segredo, só chamadas com a chave certa são aceitas. Nos três provedores, o mesmo voto não é mais premiado duas vezes.
- **Indicações, Saque (Rescue), Enquetes, Ranking e Pagamentos — Correção:** recompensas de indicação, confirmação e recusa de saque, bônus da enquete, premiação de ranking e confirmação bancária manual não podem mais ser pagos em dobro por duplo clique, dois admins ao mesmo tempo ou rodadas sobrepostas do agendador. Tentar processar de novo mostra "já processado".
- **Sorteio (Rifas) — Correção:** números inválidos (0, negativos ou acima do total) eram aceitos e podiam disparar o sorteio cedo ou travar a rifa. O sorteio agora é feito só entre números realmente vendidos.
- **Leilão — Correção:** excluir um item com lance em aberto no painel devolve o lance ao jogador; desativar um item com lance em aberto é recusado.
- **Contas — Correção:** com dois bloqueios ativos na mesma conta o painel dava erro ao abrir a conta. Aplicar um bloqueio encerra os anteriores, e a sincronização só desbloqueia quando não resta nenhum bloqueio vigente.
- **Mercado Direto e Mercado de Contas — Correção:** um pagamento atrasado de um pedido já cancelado ou reanunciado não é mais liquidado contra o dono errado. Fica registrado e o administrador é notificado.
- **Mercado de Itens — Correção:** uma venda concluída no meio da rotina de expiração não vira mais "expirada".
- **Caixas (LootBox) e Sorteio — Correção:** prêmios com peso fracionário eram sorteados errado (truncados) e peso total menor que 1 dava erro.
- **Pagamentos — Segurança:** as telas de checkout, confirmação e captura só abrem para o dono do pedido. Antes qualquer jogador logado conseguia reabrir o checkout pendente de outro.
- **Financeiro — Correção:** a sincronização de saldo de moedas não inventa mais um débito "alteração no jogo" quando um crédito do site acontece durante a leitura. A sincronização de VIP não reescreve mais todas as contas expiradas a cada minuto.
- **Instalação — Correção:** rodar os seeders de novo não volta mais nome do site, SMTP e taxas ao padrão.
- **Mercado Direto — Correção:** anunciar com preço zero ou inválido mostra "Preço inválido" em vez de erro técnico.
- **Loja (WebShop) — Novo:** pentagrama vendido já com errtel montado. Em servidores com tabela de pentagrama, a página do produto ganha, por slot, a escolha do errtel, seu nível e as opções de rank. O preço soma o valor configurado por errtel e por opção.
- **Loja (WebShop) — Novo:** campo **Período (minutos)** no produto. O item sai como temporário e expira no prazo informado após a compra, em qualquer emulador que tenha armazenamento de período. A página do produto avisa "Expira X após a compra".
- **Itens — Novo:** suporte às peculiaridades dos itens de seasons altas (S15+), em cada emulador que as tem:
  - **Socket** com seed sphere acima do nível 5: o site lê e grava todos os níveis que o servidor define (até 20 no IGCN e MuDevs, até 10 no GGCode), em vez de parar no 5.
  - **Excellent até 12 opções** (as de mastery de armas e sets), não mais só 6.
  - **Asas de 4ª e 5ª geração com grade:** as 4 opções graduadas, o elemento principal e o adicional.
  - **Brincos** com as 5 opções, **Guardian** com as 4 opções e o bônus elite, **ancient de 3º nível** e **Muun** (rank, opção, evolução e duração, com inventário de muun na edição do personagem).
  - Tudo aparece no tooltip do item e no montador de itens do painel, e pode ser vendido na Loja (WebShop): brinco com as opções, grade da asa e Guardian compráveis, com o preço por opção excellent. O seletor de "máximo de excellent" do produto passa a seguir a quantidade real de opções do item.
- **Itens — Correção:** o site não mostrava as cores do tooltip de item (excellent, ancient, socket, asa, brinco etc.) no tema público. Brincos em servidores GGCode mostravam "Earring option N" em vez do nome da opção. A Oficina (WorkShop) dava erro com itens de muitos slots excellent.
- **Caixas (LootBox) — Correção:** no painel, o campo de durabilidade do item da caixa estava fora do alinhamento das demais opções.

## 27/09/2026

- **Loja (WebShop) — Segurança:** era possível receber várias cópias de um produto pagando uma só, informando uma quantidade na requisição. A quantidade agora é validada no servidor. Produtos com faixa de quantidade passam a cobrar o preço **por unidade** e a consumir N do estoque.
- **Mercado de Itens — Correção:** comprar um item podia devolver ao vendedor um item que ele acabara de anunciar (duplicação) ou apagar do comprador um item que entrou no baú depois do login. O baú do vendedor só é regravado quando a forma de pagamento altera o baú.
- **Mercado Direto — Correção:** anunciar itens diferentes em duas abas ao mesmo tempo deixava um deles anunciado e ainda no baú; cancelar um anúncio podia ressuscitar um item já vendido.
- **Sistema — Correção:** as tarefas agendadas não rodam mais em paralelo consigo mesmas quando uma demora mais de um minuto. Isso causava e-mails e mensagens de WhatsApp em dobro, premiação de ranking duplicada e lançamentos financeiros repetidos. Trabalhos da fila presos em "processando" por mais de 15 minutos voltam à fila sozinhos e podem ser reprocessados em **Fila**.
- **Pagamentos — Correção:** o mesmo aviso de pagamento recebido duas vezes (ou ao mesmo tempo) não entrega mais o pedido duas vezes. Um aviso de "pago" atrasado sobre um pedido já estornado ou cancelado é ignorado e registrado, para você resolver pela confirmação manual.
- **Financeiro — Correção:** todo crédito e débito que pode se repetir (doação, cashback, bônus de registro, prêmios de Conquistas, Passe de Batalha, Leilão, Indicações, Mercados, Enquete, Sorteio, Saque, voto e Ranking) passa a ter uma chave única. Reenvios, duplo clique ou tarefas repetidas não creditam de novo.
- **Itens — Correção:** importar o `Item.txt` em **Itens → Importar** falhava para todos os itens, em todos os emuladores. Corrigido e testado com o arquivo completo do MorpheusEmulator.
- **Instalação — Correção:** as views dos plugins vinham codificadas no pacote, impedindo personalização. Pacotes refeitos a partir desta versão trazem as views em texto.

## 18/09/2026

- **Ranking — Novo:** os rankings do site estão disponíveis na API pública em `GET /api/v1/rankings` (lista de tipos) e `GET /api/v1/rankings/{tipo}` (classificação), com filtro por classe de personagem e por frequência (diário, semanal, mensal) onde houver. Documentado em `/api/docs`.

## 17/09/2026

- **Documentação — Correção:** a página `/api/docs` aparecia em branco ou com "Parser error" em produção. O pacote passa a trazer a documentação da API pronta e só mostra os endpoints dos plugins ativos. É preciso atualizar o pacote para receber a correção.

## 16/09/2026

- **Instalação — Novo:** as tabelas do site podem ficar em um banco de dados separado do jogo. Campo novo "Banco de dados do site (opcional)" na etapa Banco de dados do instalador: em branco, tudo continua como hoje; com um nome, o instalador cria o banco (se não existir) e todas as tabelas do Morpheus nascem nele, sem o prefixo `mw_`, deixando o banco do jogo só com as tabelas do MuOnline. Guia em `docs/banco-de-dados.md`.
- **Site — Novo:** os temas `empire`, `fatal`, `forest`, `unique` e `warriors` da versão 6 foram migrados para a versão 7 mantendo o visual original, com todas as páginas que faltavam (checkout, Passe de Batalha, Assinatura, Páginas, Mercado de Itens e outras).
- **Site — Correção:** abrir `/panel` diretamente dava erro. Agora leva ao primeiro serviço disponível da conta.
- **Financeiro — Melhoria:** erros de saldo de moedas mostram mensagens traduzidas ("Você não tem saldo suficiente", "A moeda X não está configurada") em vez de mensagens técnicas do banco.

## 15/09/2026

- **Mercado de Itens — Novo:** preço mínimo por forma de pagamento para anunciar um item. Card "Preços mínimos" em Configurações do Mercado de Itens, com um campo por moeda, carteira, Zen e item de pagamento. Anúncio abaixo do mínimo é recusado, e o formulário de venda mostra "Preço mínimo: X" assim que o jogador escolhe a forma de pagamento.

## 14/09/2026

- **Contas — Melhoria:** no painel, o histórico financeiro da conta saiu do formulário e virou um botão ao lado de "Logs" e "Baú", abrindo uma janela com os 100 lançamentos mais recentes e um atalho para o extrato completo.
- **Painel administrativo — Correção:** o Painel e as telas de Financeiro, Economia e Receita estouravam a largura no celular e no tablet. Filtros, cartões e tabelas foram ajustados para telas pequenas.
- **Perfil — Correção:** a página de bloqueio de perfil do personagem dava erro quando a coluna de horas ainda não estava configurada.
- **Troca de horas (Exchange) — Correção:** a página de troca de horas dava erro quando a coluna de horas não estava configurada e, mesmo configurada, o débito das horas não acontecia. Agora a página avisa que a troca ainda não foi configurada, e o débito usa a coluna certa. Valores vazios ou inválidos no câmbio de carteiras e moedas mostram erro de validação em vez de quebrar a página, e a mensagem "ddd" ao enviar 0 virou "O valor deve ser maior que 0".
- **Eventos — Melhoria:** o cadastro de horários do evento foi reorganizado. Um seletor de recorrência (todos os dias, por dia da semana ou texto livre) mostra só o campo daquele modo, e os horários são escolhidos com um relógio que vira etiquetas ordenadas, sem precisar digitar formato. Horas repetidas ou fora de ordem são corrigidas automaticamente, o que também conserta o contador do site que mostrava o próximo horário errado.

## 12/09/2026

- **Compatibilidade com emuladores — Novo:** suporte ao MorpheusEmulator (Season 6). Ele aparece no instalador e em **Configurações → Servidor**, com leitura correta dos itens do inventário e do baú, dos arquivos de dados do servidor e das 15 classes de personagem com evoluções até a 4ª.

## 09/09/2026

- **Loja (WebShop) — Correção:** o cupom de desconto era ignorado na compra de kits e, em itens comuns, o desconto era aplicado antes de somar o harmony, pentagram e errtel. Agora o desconto vale sobre o preço completo, cupons de valor fixo e com desconto máximo funcionam na loja igual ao checkout, e o uso do cupom passa a ser contabilizado (limite de quantidade e por conta agora valem).
- **Site — Melhoria:** as páginas de visualização de pacote, de item do mercado e de conta do mercado ganharam a mesma coluna lateral padronizada. No pacote, o preço fica em destaque, saldo e disponibilidade viram linhas, a barra de vendidos fica abaixo e o botão "Esgotado" ficou do mesmo tamanho do de compra.
- **Mercado de Itens — Melhoria:** os filtros de categoria e de classe da coluna lateral agora ocupam toda a largura em grade, com ícones maiores. Brincos, pendants e anéis ganharam ícones próprios.
- **Eventos — Melhoria:** a cor por categoria foi removida (o ponto colorido nas abas do site e na lista do painel não ficou bom). O formulário de categoria ficou só com o nome.
- **Streamers — Melhoria:** a lista de streamers no painel ganhou o botão "Configurações" ao lado de "Estatísticas".
- **Mercado Direto — Correção:** ativar o plugin no painel dava erro e não concluía.

## 08/09/2026

- **Site — Melhoria:** as páginas públicas carregam cerca de 35% mais rápido, com destaque para as ofertas do mercado de itens e o bloco de melhores jogadores do Hall da Fama.
- **Mercado de Itens — Novo:** página própria para cada anúncio. O botão "Comprar" das listagens (e a imagem/nome do card) agora abre a página do item, com imagem, raridade, expiração, preço comparado com a mediana ("X% abaixo/acima do preço mediano"), vendedor, data do anúncio, o tooltip do item no estilo do jogo, histórico de preços com gráfico (mediana, menor, maior, última venda) e as 20 vendas recentes de itens parecidos. Visitante vê "Entre para comprar", o dono vê "Este item é seu" e anúncio expirado mostra aviso.
- **Mercado de Itens — Novo:** página de consulta de preços, acessível pelo botão "Consultar preços" no topo da listagem e pelo link "Ver histórico completo" na página do item. Sem item escolhido, mostra busca por nome e os itens mais vendidos; com item escolhido, permite trocar o meio de pagamento (moeda, carteira, zen ou item), filtrar por faixa de nível e excellent, e ver gráfico, estatísticas e as últimas 20 vendas.
- **Mercado de Itens — Melhoria:** a página do item mostra o nome do vendedor em vez do login; o visual das páginas do item e de consulta ficou mais limpo (menos molduras, abas para trocar de moeda, filtros em linha); o botão "Comprar" da listagem aparece sempre que o anúncio não expirou. Corrigido o filtro de nível que não marcava a faixa escolhida.
- **Mercado de Itens — Melhoria:** no painel, a opção passou a se chamar "Exibir histórico de preços", com explicação de que ela liga e desliga de uma vez a sugestão de preço na venda, o histórico na página do item e a consulta de preços.
- **Site — Correção:** datas apareciam com uma vírgula sobrando no fim (ex.: "25/08/2026,") em "Comprado em" das compras do mercado, no vencimento do VIP do mercado de contas e no histórico da página do item.

## 07/09/2026

- **Compatibilidade com emuladores — Correção:** no MuEmu (Louis, Seasons 4/6/8) a opção azul de asas mostrava o atributo errado — Wings of Soul +9 aparecia com "Automatic HP Recovery" quando o jogo mostra "Additional Wizardry Damage". Agora o site escolhe a opção certa conforme o item, igual ao jogo.

## 03/09/2026

- **Notificações WhatsApp (Sender) — Novo:** os templates padrão de mensagem já vêm junto na instalação do site. Templates quebrados (com variáveis inexistentes ou emoji virado "??") são substituídos pelo padrão; personalizações válidas não são tocadas. Corrigido também o problema que transformava qualquer emoji salvo pelo painel em "??".
- **Instalação — Correção:** o pacote de instalação vinha sem as traduções de todos os plugins e sem as telas de Templates do Sender no painel.
- **Painel administrativo — Melhoria:** as telas de login, verificação em duas etapas e cadastro do QR code ganharam uma arte de fundo.

## 01/09/2026

- **Notificações WhatsApp (Sender) — Novo:** plugin de envio de mensagens por WhatsApp reescrito para a versão atual, com templates por evento, instâncias, tela de configurações e widget de cadastro de telefone. As mensagens passam a ser disparadas automaticamente em várias jornadas do site: recuperação e troca de senha, vendas e entregas dos mercados de itens, direto e de contas, lance superado e vitória no leilão, prêmio do sorteio, saque solicitado/pago/recusado, resposta em ticket, compra de pacote, assinatura ativada/renovada/cancelada e recompensa de ranking. 15 templates novos no catálogo.
- **Notificações WhatsApp (Sender) — Melhoria:** a tela "Compor mensagem" foi removida e no lugar entrou "Auditoria de envios", com data, evento, conta, telefone, instância, status e detalhe de erro. A tela de Templates virou lista com página de edição própria (variáveis clicáveis para copiar, pré-visualização ao vivo e "Restaurar padrão"). A tela de Configurações ficou só com a origem dos dados de contas; o logo enviado nas mensagens é o do próprio site.
- **Notificações WhatsApp (Sender) — Correção:** o link do site saía malformado e o logo não era anexado nas mensagens enviadas pela fila.
- **Painel administrativo — Novo:** busca por ID nas telas de pedidos de Doações, Mercado Direto, Mercado de Contas, Mercado de Itens e Saques.
- **Site — Melhoria:** imagens de itens e avatares voltam a ser exibidas com a suavização padrão do navegador.

## 31/08/2026

- **Site — Correção (segurança):** com o modo de depuração ligado, visitantes comuns recebiam informações internas do site (inclusive dados enviados no login). Agora essas informações só aparecem para o administrador logado.

## 25/08/2026

- **Loja (WebShop) e Pacotes — Correção:** compras simultâneas podiam ultrapassar o estoque do item ou o limite de vendas do pacote.
- **Leilão — Correção:** lances feitos ao mesmo tempo podiam engolir as moedas de outro jogador, o aviso de "já vendido" praticamente nunca disparava e o item podia ser entregue duas vezes quando dois visitantes fechavam o leilão juntos.
- **Itens — Correção:** duas ações simultâneas na mesma conta (ex.: duas abas anunciando no mercado) podiam duplicar ou perder itens do baú e do inventário. Isso foi corrigido na Loja, no Mercado de Itens, na Oficina, nas Caixas e no Mercado Direto. Item entregue não cai mais em expansão de inventário que o jogador não comprou (ficava invisível no jogo).
- **Mercado de Itens — Correção (segurança):** comprar e remover anúncio passaram a exigir confirmação real (não dá mais para forçar uma compra por link) e o preço precisa ser maior que zero. A Oficina rejeita nível e opção inválidos.
- **Painel administrativo — Melhoria:** o editor de baú da conta agora exige que o jogador esteja desconectado (antes o jogo sobrescrevia a alteração do administrador ao sair) e valida cada item antes de salvar.
- **Itens — Correção:** vários problemas de leitura e gravação de itens: itens com índice alto perdiam empilhamento, luck, refine, ancient e descrição (ou pegavam os do item errado); trocar o emulador nas configurações podia continuar mostrando dados do anterior; ancient +10 era descartado na Loja e na Oficina; tooltip de item ancião com valor em porcentagem dava erro; itens temporários perdiam a marcação ao salvar; brincos eram apagados em qualquer alteração pela Oficina; baú novo nascia com metade dos espaços quando havia baú estendido; tooltip de item com opção dava erro no MuDevs e SSeMU; asas, pets e joias eram gravadas na categoria errada no SSeMU.
- **Compatibilidade com emuladores — Correção:** o GGCode (Season 21) tinha 6 leitores de arquivos de dados quebrados e a gravação de itens deslocava os demais itens do inventário; corrigidos e validados contra os arquivos reais. No MuDevs, GGCode e IGCN (Seasons 19–21) a Shining Lancer e a Lemuria Mage colidiam com outras classes e ficavam sem ícone.
- **Compatibilidade com emuladores — Novo:** integração completa do IGCN (Season 21): classes de personagem com a escada de evolução real, leitura e gravação de itens do inventário e baú, arquivos de dados oficiais e suporte ao hash de senha do IGCN (nova opção de ordem dos argumentos nas configurações).

## 21/08/2026

- **Itens — Correção:** no MuEmu (Louis), itens temporários com determinados seriais geravam erro recorrente e nunca mostravam a data de expiração.
- **Saque (Rescue) — Correção:** dois pedidos de saque ao mesmo tempo mostravam um erro genérico em vez de "Você não tem saldo suficiente", e o saldo ficava travado enquanto o gateway respondia. A mensagem agora é clara e a falha do gateway não desfaz o débito legítimo.

## 14/08/2026

- **Mercado de Contas — Correção:** a entrega de uma conta vendida falhava quando o vendedor tinha CPF cadastrado, e a limpeza dos dados do dono anterior não zerava de fato nome, telefone, pergunta e resposta secreta.

## 12/08/2026

- **Itens — Novo:** o tooltip do item mostra "Expira em" ou "Expirou em" para itens temporários (em vermelho quando já venceu). Asas de segundo nível não recebem mais o prefixo "Excellent" indevido.
- **Mercado de Itens — Novo:** ao anunciar um item, a tela de venda mostra o preço sugerido (mediana) e um mini gráfico das vendas concluídas do mesmo tipo de item, no mesmo meio de pagamento. Um interruptor permite ampliar a amostra ignorando a opção excellent. Pode ser ligado/desligado e ter a janela de dias ajustada nas configurações do Mercado de Itens no painel; some quando há menos de 3 vendas comparáveis.
- **Sorteio — Correção:** o prêmio de VIP não somava os dias quando o ganhador já tinha VIP do mesmo tipo.
- **Mercado de Contas — Novo:** colocar uma conta à venda remove o bloqueio de perfil dos personagens (a conta anunciada fica pública de qualquer forma).
- **Compatibilidade com emuladores — Correção:** a Lemuria Mage colidia com outra classe no GGCode, IGCN e MuDevs (Seasons 19–21).

## 11/07/2026

- **Painel administrativo — Correção:** editar uma conta cujo status de conexão estava vazio dava erro.
- **Painel administrativo — Correção:** os botões "Filtros", "Aplicar", "Todos", "Novo" e "Redefinir" das listagens apareciam em inglês.

## 10/07/2026

- **Mercado de Contas — Novo (segurança):** ao comprar uma conta, todos os dados do dono anterior são zerados (nome, telefone, pergunta secreta, CPF, pix, login com Google/Facebook, verificação em duas etapas), fechando a brecha em que o vendedor podia retomar a conta. No primeiro login, o comprador é levado a uma tela obrigatória para definir seus próprios dados antes de usar o painel.
- **Itens — Correção:** algumas asas apareciam como excellent no site, mas não no jogo (a opção extra de dano era confundida com um slot de excellent).

## 09/07/2026

- **Instalação — Correção:** o pacote de instalação tinha vários problemas: o site ficava sem estilos e scripts, nenhum plugin funcionava, o login social quebrava, o dashboard do painel e a página de downloads davam erro, e o instalador não abria. Tudo corrigido no pacote.
- **Instalação — Correção:** servidor sem arquivo de licença ficava travado como "ilegal" para sempre, sem conseguir baixar a licença.

## 08/07/2026

- **Site — Melhoria (segurança):** as pastas de sistema do site (configurações com credenciais, código, traduções) deixam de ser acessíveis pelo navegador; arquivos de desenvolvimento não vão mais no pacote.
- **Instalação — Novo:** versão 7.0.0. A atualização pode vir como pacote menor, só com os arquivos alterados, que é sobreposto na instalação; a licença assinada passa a ser obrigatória.
- **Painel administrativo — Correção:** acessar o painel sem a barra final (ex.: /admin) dava "página não encontrada"; agora redireciona.
- **Site — Correção:** uma licença corrompida derrubava o site inteiro; agora ele apenas mostra a tela de licença ilegal.
- **Cupons — Correção:** as opções de escopo do cupom apareciam sem nome no formulário.
- **Assinatura de VIP — Correção:** a renovação automática da assinatura rebaixava ou apagava VIP concedido por outra fonte (administrador, pacote, evento). Agora ela só estende o VIP, nunca encolhe nem rebaixa um VIP maior. Novo botão de cancelar assinatura por linha na lista de assinantes do painel.
- **Assinatura de VIP — Melhoria:** os planos de assinatura aparecem no início da página de VIP do site, com subtítulo, e o bloco "sobre VIP" virou uma faixa leve para deixar os planos em destaque. A página de assinatura mostra o histórico de cobranças (data, valor, status).

## 07/07/2026

- **Assinatura de VIP — Novo:** novo plugin para vender VIP como assinatura recorrente (além do Pacotes, que é compra única). Planos cadastrados no painel em **Economia → Assinaturas**, checkout pelo Stripe, VIP estendido a cada renovação, cancelamento ao fim do período, lista de assinantes no painel e página pública de planos com a assinatura atual do jogador.
- **Assinatura de VIP — Melhoria:** cada plano pode ter preço mensal e anual (o jogador escolhe no checkout), lista de vantagens e destaque de "Recomendado". O gateway do plano é opcional: em branco, o jogador escolhe entre os gateways ativos configurados em **Administração → Gateways**. A página de planos passou a ser pública e em largura total, sem a barra lateral do painel.
- **Painel administrativo — Melhoria:** as telas de pedidos dos mercados de Contas, Direto e de Itens ganharam o botão "Configurações" ao lado de "Estatísticas"; o submenu Mercado usa rótulos curtos (Contas, Direto, Itens).
- **Painel administrativo — Melhoria:** no editor de baú, o aviso de salvamento automático virou um toast discreto ("Salvo"), em vez de um texto colado ao botão de ZEN.
- **Painel administrativo — Correção:** o indicador de carregamento ficava fora da tela em páginas com rolagem.
- **Servidor — Correção:** a lista de servidores e a desconexão de conta (kick) davam erro fatal.
- **Painel administrativo — Correção:** o reset de personagem podia falhar por um erro interno.
- **Site — Correção:** a paginação do Mercado de Contas e do Sorteio aparecia sem estilo.
- **Instalação — Novo:** o instalador permite escolher a moeda base do site (ao lado do fuso horário).

## 06/07/2026

- **Painel administrativo — Melhoria:** novo editor de texto (Quill), mais leve e sem depender de serviços externos, com a mesma barra de ferramentas e upload de imagem.
- **Itens — Novo:** novas instalações já vêm com 6 raridades de item padrão (Comum, Incomum, Raro, Épico, Lendário, Mítico), com cor e nome traduzido.
- **Painel administrativo — Novo:** editor completo de baú na conta do jogador: grade com a cara do inventário do jogo (baú principal e estendidos em abas), painel lateral fixo para montar itens e adicionar várias cópias de uma vez (ideal para joias), arrastar com indicação de onde cabe, editar e remover itens, tooltip ao passar o mouse, salvamento automático e ZEN em janela própria.

## 05/07/2026

- **Mercado de Itens — Correção:** ao atualizar de uma versão antiga, itens já anunciados apareciam como "item normal" mesmo sendo excellent, com skill ou socket, e os filtros e etiquetas do mercado (site e painel) ficavam errados. Agora existe um passo pós-atualização que recalcula esses atributos a partir do próprio item.
- **Notícias — Correção:** a prévia do texto das notícias não mostra mais códigos estranhos (como "&nbsp;") nem gera avisos; acentos preservados.
- **Downloads — Correção:** ao atualizar de uma versão antiga, os downloads já cadastrados passam automaticamente para o novo cadastro (com tradução), sem se perder.
- **Finanças — Correção:** depois de uma atualização, as telas de finanças (receita, extrato e reconciliação) já vêm preenchidas com o histórico de pedidos, moedas e carteiras — antes apareciam zeradas. Também corrigido um cálculo que deixava o histórico de moedas e carteiras quase vazio.
- **Instalação — Melhoria:** a atualização de um servidor antigo (v6) ficou mais robusta e sem perda de dados, verificada ponta a ponta num banco real de produção.
- **Painel administrativo — Melhoria:** o menu lateral foi reorganizado em quatro seções (Jogo, Loja & Economia, Conteúdo e Sistema) em vez de uma lista alfabética enorme.
- **Painel administrativo — Novo:** Venda de contas, Mercado direto e Mercado de itens agora ficam juntos num único menu "Mercado". Nova tela de Pedidos do Mercado de Itens, listando vendas realizadas e itens à venda, com status (Disponível/Entregue/Expirado) e filtros por vendedor, comprador e nome do item. Os itens de Venda de contas e Mercado direto também passaram a aparecer para admins que não são super-admin.
- **Mercado de Contas — Correção:** a tela de pedidos e a de estatísticas não abrem mais com erro quando existe um anúncio estornado.
- **Segurança — Correção:** fechadas brechas em que as configurações de VIP definidas no painel podiam ser usadas para injetar comandos no banco de dados (rotina de VIP expirado, ranking de doadores e mercado de contas).

## 04/07/2026

- **Pagamentos — Correção:** as notificações do Stripe e do Pagar.me agora exigem a chave secreta (Stripe) e usuário/senha (Pagar.me) configurados; sem eles a notificação é rejeitada e o painel não deixa ativar o gateway sem preencher esses campos.
- **Segurança — Correção:** a tela de configuração do VIP no painel não permite mais injetar comandos no banco de dados. O site também ganhou uma política de segurança de conteúdo configurável, que bloqueia carregamento de recursos de origens não autorizadas.
- **Itens — Correção:** a opção "azul" dos itens (+4, +8… de Dano, Defesa, HP etc.) passa a ser lida direto dos arquivos do servidor. Isso corrige asas que mostravam o atributo errado (Cloak of Fighter mostrava HP em vez de Dano; Wings of Despair mostrava Maldição em vez de Wizardry) e índices de asa errados conforme a season.

## 28/06/2026

- **Licença — Melhoria:** a licença do Morpheus passou a ser assinada digitalmente e a verificação ficou mais rígida, dificultando cópias não autorizadas. Se o servidor de licença ficar inacessível por mais de 72 horas, o site é bloqueado até restabelecer o contato.
- **Instalação — Melhoria:** depois de concluída a instalação, o instalador deixa de ficar acessível (antes ainda era possível reconfigurar o banco ou redefinir o admin por ele).
- **Troca de horas (Exchange) — Correção:** criar um pacote de horas pelo painel falhava.
- **Itens — Melhoria:** itens empilháveis mostram a quantidade no nome (ex.: "5x …"), e o pendant ganhou a opção "Max mana increase" (antes aparecia com o rótulo errado).
- **Instalação — Correção:** uma instalação nova podia falhar na etapa das Caixas (LootBox).
- **Loja (WebShop), Leilão e Sorteio — Correção:** criar uma loja, categoria de loja, leilão ou rifa pelo painel falhava por causa de colunas antigas que ficaram no banco.
- **Conta do jogador — Correção:** criar uma conta gerava um aviso quando o VIP fica em tabela separada.
- **Mercado Direto e Mercado de Contas — Novo:** estorno (chargeback) de uma venda de item agora reverte o crédito do vendedor. No mercado de contas, o anúncio é marcado como estornado e fica um alerta no histórico da conta para revisão manual pelo suporte.
- **Indique e ganhe — Correção:** as recompensas de indicação nunca eram criadas — o indicador não recebia nada. Agora funciona.
- **Mercado de Itens — Correção:** um item colocado à venda não aparecia no mercado nem podia ser comprado.

## 26/06/2026

- **Mercado de Contas — Correção:** o botão "desistir da venda" não funcionava e a conta ficava bloqueada para sempre até alguém comprá-la. Agora desistir remove o anúncio e desbloqueia a conta (não é permitido se a conta estiver online).
- **Conta do jogador — Correção:** o "esqueci a senha" mostrava erro e nunca enviava a senha nova; e no Mercado de Contas o comprador pagava mas não recebia a conta. Os dois casos foram corrigidos.
- **Mercado de Contas — Novo:** preço mínimo de venda configurável no painel (campo "Min price"); o formulário de venda mostra a dica do mínimo. O Mercado Direto ganhou a mesma dica de mínimo.
- **Pagamentos — Correção:** com o plugin de Mensagens ativo, toda doação, crédito de carteira ou estorno falhava. Além disso, uma falha ao enviar a notificação de pedido não cancela mais o crédito ou estorno já feito.
- **Painel administrativo — Correção:** ações sensíveis que estavam liberadas para qualquer admin passaram a respeitar as permissões: ativar/desativar produtos e kits da loja, gerar token de streamer, configurar Resgate e excluir serviço pago.
- **Painel administrativo — Correção:** criar uma Caixa (LootBox) e criar um serviço pago pelo painel davam erro. O card de Patentes na tela de Configurações aparecia numa categoria sem título.

## 25/06/2026

- **Painel administrativo — Melhoria:** as configurações de 20 plugins passaram para a tela Configurações, como cards organizados por categoria (Site, Acesso, Serviços, Rankings, Economia). Alguns plugins que antes só tinham configuração por link direto agora aparecem lá.
- **Painel administrativo — Novo:** tela de Estatísticas (botão no topo da listagem) para praticamente todos os plugins: Perfil, Recompensa por voto, Indique e ganhe, Troca de horas, Patentes, Contagem regressiva, Vídeos, Slides, Notícias (visualizações, comentários, mais vistas), Pacotes (vendas e receita), Mercado de Itens, Leilão, Páginas, Caixas, Guias, Eventos, Mercado Direto, Passe de Batalha, Oficina, Loja, Mercado de Contas, Tracker, Suporte (avaliação média, tickets por departamento), Streamers (ranking de afiliados), Sorteio e Resgate.
- **Painel administrativo — Correção:** criar um vídeo, um slide, um pacote de horas ou um status de categoria do Tracker dava erro.
- **Loja (WebShop) — Correção:** criar um produto e excluir uma categoria falhavam; a ação "Desativar" em massa não funcionava.
- **Mercado de Contas — Correção:** criar um anúncio falhava; e o tempo de expiração configurado era ignorado (caía sempre em 60 minutos).
- **Loja (WebShop) — Melhoria:** o cadastro de produto foi reorganizado em três blocos (Produto, Configurações e Preços) e o cadastro de kit padronizado na mesma ordem.
- **Painel administrativo — Melhoria:** as ações em massa das tabelas viraram um único menu "Ações", que só aparece quando há linhas selecionadas; os textos Ativar/Desativar agora aparecem traduzidos.
- **Streamers — Melhoria:** a edição do afiliado (link e cashback) virou uma janela na própria listagem, e o campo de cashback mostra o "%".

## 24/06/2026

- **Páginas — Correção:** criar e editar páginas passou a respeitar as permissões de admin (antes estava liberado), e criar/editar página dava erro.
- **Páginas — Melhoria:** o construtor de páginas passou a ter um único bloco HTML (os blocos hero, texto, imagem+texto e chamada foram removidos; o conteúdo rico vem dos blocos dos plugins: guias, notícias, enquete, contagem regressiva, slides e vídeos). Os campos CSS e Script personalizados ganharam realce de sintaxe e altura automática; o Enter não duplica mais o bloco HTML; e salvar uma página mantém você na tela de edição.
- **Site — Correção:** removido o espaço extra acima do rodapé.
- **Pacotes — Melhoria:** a listagem ficou sem a coluna de imagem, e os botões Categorias e Configurações foram para o cabeçalho.
- **Painel administrativo — Correção:** a coluna de arrastar (reordenar) das tabelas estava larga demais, e o campo de cor era um quadradinho pequeno — agora ocupa a largura da coluna (categorias de Notícias e Eventos).
- **Notícias — Melhoria:** as configurações ganharam textos de ajuda explicando cada opção, e os botões Categorias e Configurações foram para o cabeçalho.
- **Mercado Direto — Correção:** criar um anúncio quebrava.
- **Mercado Direto — Novo:** o vendedor recebe uma mensagem quando o item é vendido (valor bruto e líquido) e o comprador quando recebe o item. Se o armazém do comprador estiver cheio, o item não se perde mais (fica pago e tenta de novo). A janela de cancelamento deixou de ser fixa em 24h e agora é configurável em **Direct Market → Configs**.
- **Painel administrativo — Correção:** scripts de alguns plugins não carregavam no painel por um problema na junção dos arquivos.
- **Leilão — Correção:** a prévia do item nas telas de adicionar/editar não mostrava a imagem; os leilões de demonstração apareciam sem nome; e editar item de leilão (e item de kit na Loja) derrubava a página.
- **Painel administrativo — Melhoria:** o editor de texto rico voltou a funcionar de verdade em Guias, Notícias e Tracker (antes aparecia uma caixa de texto simples), com barra de ferramentas traduzida e envio de imagem.
- **Guias — Melhoria:** formulário reorganizado (título e ativo na mesma linha, depois URL, categoria e o editor de conteúdo); o botão Categorias foi para o cabeçalho.

## 23/06/2026

- **Eventos — Novo:** cada evento pode ter uma duração (em minutos). Enquanto um evento recorrente está acontecendo, a página mostra "Ao vivo" com destaque e a contagem passa a ser o tempo restante até terminar.
- **Eventos — Novo:** cada categoria de evento ganhou uma cor, escolhida no painel. A cor aparece na lista de categorias e como um ponto colorido nas abas da página de eventos e no destaque.
- **Eventos — Correção:** a opção "Notificável" passou a funcionar de verdade: o botão de aviso no navegador só aparece nos eventos marcados como notificáveis, e a opção agora está disponível no cadastro do evento.
- **Eventos — Melhoria:** no painel, os atalhos Categorias e Configurações ficaram no cabeçalho da lista de eventos, no mesmo padrão das outras telas.
- **Enquetes — Novo:** agora dá para escolher quando o resultado fica visível (sempre, só após votar ou só após encerrar), escrever uma descrição traduzível para a enquete e dar uma recompensa em moeda para quem vota (creditada uma única vez por conta). O site ganhou uma página de histórico com as enquetes encerradas e o painel uma tela de estatísticas de votos.
- **Enquetes — Correção:** enquetes de escolha única não aceitam mais mais de uma resposta por envio. No painel, agora é possível excluir uma enquete inteira (antes só dava para excluir as respostas).
- **Cupons — Novo:** o cupom pode ser de desconto fixo ou percentual, com teto de desconto, valor mínimo do pedido, limite de usos por conta e opção "só para a primeira compra". No checkout o total é recalculado ao vivo conforme essas regras. Nova tela de estatísticas com total de usos, cupons ativos, valor processado, cashback pago e cupons mais usados.
- **Cupons — Melhoria:** o item Cupons do menu do painel abre direto a lista, sem submenu.
- **Conquistas — Novo:** as recompensas agora são estruturadas por tipo (moedas, carteira, VIP, item ou personalizada), cada conquista pode ter um ícone, a data de desbloqueio fica registrada e o menu do site mostra quantas conquistas estão prontas para resgatar. A página exibe a raridade (percentual de contas que já desbloquearam) e o perfil do personagem ganhou uma vitrine com as conquistas desbloqueadas. No painel, há um botão para testar a regra da conquista antes de salvar (mostra o progresso alcançado) e uma tela de estatísticas com taxa de conclusão por conquista.
- **Conquistas — Melhoria:** os títulos de requisitos e recompensas podem ser traduzidos nos 6 idiomas, e as regras avançadas ganharam um editor com realce e numeração de linhas. A navegação do painel ficou mais direta: da edição da conquista dá para ir para Requisitos e Recompensas, e o botão de voltar vem sempre primeiro.
- **Documentação — Novo:** guias em português, sem linguagem técnica, para Eventos, Enquetes e Conquistas, explicando o conceito, a experiência do jogador, o passo a passo no painel, dicas e perguntas frequentes.

## 22/06/2026

- **Caixas (LootBox) — Novo:** o atributo ancient agora tem uma chance por variação (por exemplo, "Hyon +5" e "Hyon +10"), igual ao excellent. Antes havia um único campo de chance e o ancient nunca era aplicado no sorteio; agora ele é sorteado e entregue corretamente.
- **Caixas (LootBox) — Melhoria:** a raridade mostrada ao jogador é a do próprio item cadastrado no catálogo (o campo de raridade separado no item da caixa foi removido). A seleção de item ganhou busca, os campos de percentual ficam em uma só linha e a edição da caixa tem um botão Itens no cabeçalho. O menu Caixas abre direto a lista.
- **Caixas (LootBox) — Correção:** ao editar um item da caixa, o item selecionado voltou a aparecer preenchido.
- **Passe de Batalha — Correção:** a recompensa de item entregava o mesmo número de série para todos os jogadores (risco de item duplicado). Se dois resgates chegam ao mesmo tempo, o segundo mostra "Recompensa já resgatada" em vez de um erro. O limite diário de XP passou a contar o dia corretamente na virada da meia-noite.
- **Passe de Batalha — Melhoria:** o título de exibição da recompensa personalizada pode ser traduzido nos 6 idiomas. No painel, reordenar níveis por arrasto ganhou animação, e a edição da temporada tem atalhos para Níveis e Fontes de XP.
- **Painel administrativo — Novo:** ao cadastrar um item (Passe de Batalha, Leilão, Loja), a lista de itens ganhou busca e um painel ao lado mostra a imagem e a descrição do item conforme você escolhe as opções, exatamente como o jogador veria no jogo.
- **Painel administrativo — Correção:** skill, ancient, refine e socket escolhidos no cadastro de item eram descartados em silêncio; agora são aplicados. Corrigidos espaçamentos entre campos do montador de item, a borda do seletor com busca e o foco automático no primeiro campo do formulário.
- **Documentação — Novo:** guias em português para Caixas da Sorte e Passe de Batalha, e o guia do Financeiro foi reescrito em linguagem simples (dinheiro real, créditos, moedas do jogo, meios de pagamento, cupons, câmbio, relatórios e antifraude).

## 21/06/2026

- **Passe de Batalha — Correção:** a página mostrava só a primeira recompensa de cada nível quando havia várias. Agora, com mais de uma recompensa, o card mostra um resumo com a lista completa ao passar o mouse e o botão "Resgatar tudo".
- **Passe de Batalha — Melhoria:** as fontes de XP ganharam um nome traduzível, exibido na página do passe e no painel. No cadastro, o campo de consulta só aparece no tipo personalizado.
- **Pagamentos — Correção:** três problemas no estorno: o cupom usado no pedido não era liberado, o registro financeiro não anulava a receita do pedido estornado e um estorno parcial debitava o valor cheio.
- **Sistema — Novo:** erros inesperados do site passam a ser reportados automaticamente à equipe do Morpheus para correção mais rápida (o mesmo erro não é reenviado repetidamente). Pode ser desligado nas configurações.
- **Painel administrativo — Melhoria:** a barra lateral usa o logotipo do Morpheus (e o ícone do lobo quando recolhida). As telas de login e de verificação em duas etapas foram redesenhadas com um único card central sobre o fundo da marca, sem ícones dentro dos campos.
- **Site — Melhoria:** imagens de itens e logotipos de guild carregam bem mais rápido: ficam guardadas prontas em vez de serem geradas a cada visita.
- **Site — Melhoria:** com o registro de consultas ao banco ligado, as páginas ficavam lentas; o registro passou a ser gravado de uma vez ao final de cada acesso.
- **Instalação — Correção:** os dados de demonstração (banners da home e guias) usavam imagens de um serviço externo fora do ar, o que deixava a home lenta e com imagens quebradas. Instalações novas usam uma imagem local; bases já instaladas precisam trocar as imagens manualmente.

## 20/06/2026

- **Instalação — Correção:** os modelos de e-mail não eram criados durante a instalação; agora são, em 7 idiomas, com assunto e corpo traduzidos. A instalação também não aborta mais por um erro na etapa de raridades de itens, e as caixas e downloads de exemplo passaram a ter tradução completa.
- **Instalação — Melhoria:** as mensagens de validação do instalador aparecem no idioma escolhido.
- **Site — Correção:** em instalações de produção, o site podia falhar depois de limpar os arquivos temporários pelo painel; corrigido. Os avisos de sucesso e erro voltaram a aparecer e a poder ser fechados corretamente.
- **Painel administrativo — Melhoria:** na edição de conta, as seções Carteiras e Moedas só aparecem quando há alguma configurada no servidor.
- **Pagamentos — Correção:** o PicPay não creditava o pagamento; o MorpheusPay tratava aviso duplicado como erro e a notificação dele estava quebrada; o PayPal ignorava silenciosamente falhas de verificação. Todos corrigidos.
- **Pagamentos — Novo:** verificação de autenticidade dos avisos de pagamento no Stripe (campo Webhook secret) e no Pagarme (usuário e senha do webhook). Opcionais, mas quando preenchidos um aviso falsificado não credita nada.
- **Pagamentos — Correção:** o estorno passou a funcionar mesmo quando o jogador já gastou os créditos (o saldo fica negativo, refletindo a perda real) e fica registrado no financeiro.
- **Pagamentos — Novo:** estornos e chargebacks vindos do PicPay, MercadoPago, PagHiper e PayPal agora revertem o crédito da carteira e o cashback do cupom, e um pedido cancelado no provedor fica cancelado no site. Se faltar a taxa de câmbio da moeda, o pagamento fica em espera até o administrador cadastrar a taxa, em vez de creditar um valor errado.
- **Pagamentos — Melhoria:** o checkout mostra a taxa de cada meio de pagamento ("+X% de taxa" ou "Sem taxa") e a linha "Total a pagar" com a taxa incluída. O cupom é aplicado ao vivo ao digitar o código, mostrando a linha "Desconto do cupom". Os valores sugeridos passaram a ser configuráveis em **Configurações → Doação**. Os meios de pagamento e os valores viraram cards padronizados, o botão Continuar ficou alinhado e o selo "Pagamento seguro" foi removido.

## 19/06/2026

- **Pagamentos — Novo:** a página de pagamento foi redesenhada em uma tela única, com o valor primeiro: escolha um valor sugerido ou digite outro (mostrando ao vivo o que você recebe e o nome da carteira), escolha o meio de pagamento em cards, informe um cupom opcional e continue. Pagamentos pendentes aparecem no topo com link para finalizar, e o histórico virou cards em uma coluna lateral com as 5 últimas doações.
- **Pagamentos — Melhoria:** o plugin Doações foi incorporado ao sistema: checkout, pedidos, contas bancárias, confirmação de pagamento por comprovante e configuração de meios de pagamento agora fazem parte do núcleo e funcionam sem o plugin. A carteira creditada por doações fica em **Configurações → Doação**, e a confirmação de pagamento passou a estar sempre disponível. Atenção: a URL de notificação dos meios de pagamento mudou e precisa ser atualizada no painel de cada provedor.
- **Pagamentos — Novo:** transferência bancária vale para qualquer compra (mercados, Passe de Batalha, doação): o jogador envia o comprovante ligado ao pedido e, quando o administrador aprova, o item ou crédito é entregue automaticamente. A tela de pedidos foi para **Financeiro → Pedidos**, e a confirmação manual agora entrega o produto corretamente (antes só marcava como pago).
- **Pagamentos — Correção:** os checkouts do Mercado Direto, Mercado de Contas e Passe de Batalha davam erro fatal; a lista de pedidos do checkout também quebrava. Desativar o plugin Doações não derruba mais os meios de pagamento.
- **Pagamentos — Melhoria:** a tela de meios de pagamento virou um grid de cards com logotipo, interruptor de ativo (salva na hora, com mensagens "Gateway ativado/desativado") e botão Configurar que abre as credenciais em uma janela. Campos secretos são mascarados com botão de olho, e os campos obrigatórios só são exigidos quando o meio está ativo. A conversão manual de moedas saiu dessa tela: o câmbio vem das taxas cadastradas no financeiro.
- **Pagamentos — Novo:** tela **Financeiro → Eventos de pagamento** registra cada aviso recebido dos provedores (recebido, pago, entregue, ignorado, erro) com filtros, para acompanhar pagamentos em produção. Plugins podem adicionar seus próprios meios de pagamento.
- **Painel administrativo — Novo:** sistema de notificações com sino na barra superior (contador de não lidas, marcar como lida) e página com o histórico. Reúne mensagens do servidor de licença e avisos do sistema: alerta de fraude, tarefa em fila que falhou e atualização disponível.
- **Painel administrativo — Novo:** o painel inicial virou um centro de comando: faixa com jogadores online, recorde e equipe online; lista "Precisa de atenção" (fraudes, confirmações pendentes, tarefas com falha, divergências financeiras) com links; resumo do jogo e snapshot de vendas com comparação ao período anterior, ticket médio e melhor meio de pagamento. O gráfico detalhado de receita continua no Financeiro.
- **Painel administrativo — Melhoria:** a página de configurações foi reorganizada: a categoria Personagem virou Serviços (com Resets e Transferência de VIP), Sistema VIP foi para Economia, Downloads para Site e E-mails para Sistema. Ao clicar em "Configurações" no caminho de navegação, a categoria correta já abre. Títulos do menu ficaram mais curtos e as dicas de **Configurações → Geral** foram traduzidas.
- **Painel administrativo — Melhoria:** em **Configurações → Geral**, a lista de servidores pode ser reordenada por arrasto. As telas de Plugins e Meios de pagamento passaram a usar o mesmo card com interruptor de ativo e botão Configurar. A lista de itens ganhou filtro por raridade, e imprimir recibo abre em nova guia já no modo de impressão.
- **Painel administrativo — Correção:** **Configurações → Geral** e o cadastro do plugin Patentes não abriam por causa de um erro ao carregar o formulário. Barra lateral recolhida voltou a mostrar os ícones e não gera mais barra de rolagem horizontal; títulos longos do menu ficam com reticências; o painel de notificações abre para o lado certo e fecha ao clicar em um link; corrigidos a seta duplicada no menu do usuário e os dois ícones no botão de tema.
- **Site — Melhoria:** a opção "URL Rewrite" foi removida de **Configurações → Geral**: as URLs do site são sempre limpas, sem "index.php". A hospedagem precisa suportar reescrita de URL.

## 18/06/2026

- **Financeiro — Novo:** o painel ganhou o menu **Financeiro**, com visão única de tudo que entra e sai: resumo (receita do período, pedidos pagos, créditos emitidos, gastos internos, saldo em circulação por moeda e contas que mais gastaram), **Extrato** com busca, filtros e exportação para planilha (CSV) e relatório de **Receita** por dia, forma de pagamento e moeda.
- **Financeiro — Novo:** toda movimentação de moedas (coins) e carteiras passa a ficar registrada num extrato único, com o histórico antigo importado. Isso também protege contra crédito em dobro quando o jogador clica duas vezes ou o gateway reenvia a confirmação de pagamento.
- **Financeiro — Novo:** **Reconciliação** (Financeiro → Reconciliação) aponta carteiras cujo saldo não bate com o histórico de transações, e **Ajuste manual** (Financeiro → Ajuste manual) permite creditar ou debitar o saldo de uma conta com motivo obrigatório, tudo registrado no histórico de ações do administrador.
- **Financeiro — Novo:** alterações de moeda feitas diretamente pelo jogo (fora do site) agora também aparecem no extrato, como "Alteração no jogo". A captura roda automaticamente a cada 10 minutos (pode ser desligada em **Jobs**); a primeira execução só registra o ponto de partida.
- **Financeiro — Novo:** alerta de ganho anômalo de moeda. Defina um limite por moeda no cadastro de Coins e, quando um jogador ganhar dentro do jogo um valor acima do limite, aparece um alerta em **Financeiro → Alertas** para revisar ou dispensar, além de um aviso vermelho no painel financeiro.
- **Financeiro — Novo:** aba "Histórico financeiro" na página da conta (Contas → Editar), reunindo moedas, carteiras, ajustes e alterações no jogo num só lugar, com filtros por direção e período e link para o extrato completo.
- **Financeiro — Novo:** **Economia** (Financeiro → Economia) mostra a saúde da economia do jogo: quanto de cada moeda entrou e saiu no período, o fluxo líquido (inflação) por categoria e o gráfico da quantidade total em circulação ao longo do tempo.
- **Financeiro — Novo:** suporte a várias moedas. Em **Configurações → Geral** é possível escolher a moeda padrão do site (23 opções, independente do idioma — por exemplo, site em português com preços em dólar). Em **Financeiro → Taxas de câmbio** você cadastra as cotações, e a receita passa a ser consolidada na moeda padrão, com quebra por forma de pagamento e moeda e aviso de pedidos ainda sem cotação.
- **Financeiro — Novo:** botão "Atualizar via API" em Financeiro → Taxas de câmbio busca as cotações do dia automaticamente. Há também uma tarefa agendada para isso, desligada por padrão — ative em **Jobs** (sugestão: diariamente às 4h).
- **Pagamentos — Melhoria:** o sistema de pagamento passou a fazer parte do núcleo do site. Mercado Direto, Mercado de Contas, Passe de Batalha e Streamers não dependem mais do plugin de Doações, e os pedidos pagos entram no Financeiro na hora. As confirmações já configuradas nos gateways continuam funcionando.
- **E-mails — Novo:** os modelos de e-mail agora são editados direto no painel (Configurações → E-mails), com lista de nome amigável e descrição, campo de **assunto**, e assunto e corpo traduzíveis por idioma. O editor ganhou destaque de sintaxe, pré-visualização ao vivo (versão computador e celular) com dados de exemplo e variáveis para inserir com um clique. Também foi fechada uma brecha de segurança na edição desses modelos.
- **E-mails — Melhoria:** novo visual dos e-mails enviados (logo em faixa escura, cartão central, botão de ação, adaptado ao celular), com estilos que agora aparecem corretamente no Gmail e no Outlook. Corrigido o link que saía com "http://" duplicado.
- **Personagens — Novo:** a lista de personagens ganhou filtros por Conta, Guild, Classe, Mapa e Online, e o filtro de banidos virou uma chave liga/desliga. Corrigido o filtro de Mapa, que aparecia vazio.
- **Personagens — Melhoria:** a lista de jogadores online agora é paginada, com busca por nome e coluna de servidor, em vez de um bloco por servidor.
- **Painel administrativo — Correção:** os cartões de resumo dos painéis (principal, financeiro e doações) não ficam mais colados nos gráficos. A permissão do reCAPTCHA passou a aparecer traduzida na tela de grupos.

## 17/06/2026

- **Painel administrativo — Melhoria:** botões que só têm ícone (editar, excluir, ações) mostram uma dica ao passar o mouse.
- **Tokens de API — Melhoria:** tokens não são mais vinculados a uma conta de jogador; o campo saiu do cadastro e da lista.
- **Painel administrativo — Melhoria:** o cursor já entra no primeiro campo ao abrir um formulário ou janela, e os campos de valor (depósito e saque de carteira) formatam o número conforme o idioma (ex.: 1.234,56).
- **Painel administrativo — Correção:** links não ficam mais sublinhados ao passar o mouse (busca do topo, cartões de configurações, sugestões).
- **Contas — Novo:** no formulário de banimento, a conta é sugerida enquanto você digita.
- **Mercado de Itens — Correção:** a ordenação por preço ordenava como texto (800 antes de 7500); agora ordena pelo valor.
- **Painel administrativo — Melhoria:** datas nas tabelas não quebram mais em duas linhas, e tabelas largas rolam na horizontal no celular em vez de serem cortadas.
- **Contas — Melhoria:** o baú aberto pela página da conta ficou mais largo, com a grade centralizada e rodapé igual ao das outras janelas; a janela de logs também ficou mais larga. Itens do jogo passaram a mostrar as cores de raridade, socket e pentagrama corretamente nas telas do painel (catálogo, baú).
- **Contas — Novo:** a lista de contas ganhou as colunas Status (online/offline) e Última conexão, a coluna de personagens deu lugar ao Nome da conta, e o filtro ganhou E-mail, Último IP e Personagem (Banidas virou chave). Corrigido o selo "Bloqueado" grudado no nome.
- **Contas — Melhoria:** a página de edição da conta foi reorganizada em grupos (identidade, acesso e contato, verificações, dados pessoais, perguntas secretas, informações do sistema), o campo País aparece sempre e entrou o campo Telefone. A conta pode ter nome completo (até 50 caracteres), sem o limite curto do jogo. Textos traduzidos e dicas nos campos.
- **Painel administrativo — Novo:** busca global no topo do painel, que encontra contas e personagens conforme você digita (substitui a busca da barra lateral). Corrigido o menu do usuário/sair no topo.
- **Páginas — Correção:** o editor de páginas não carregava ao navegar dentro do painel (só após recarregar a página) e o envio de imagens pelo editor usava um endereço errado; ambos corrigidos.
- **Painel administrativo — Melhoria:** o painel antigo foi aposentado: todas as telas (núcleo e todos os plugins) passaram para o novo visual, mais leve, com ícones no mesmo estilo do site. Listas com busca, filtros laterais e paginação; formulários com erros mostrados junto ao campo; janelas de confirmação próprias. Corrigido o item ativo do menu lateral após navegar.
- **Loja (WebShop) — Melhoria:** produtos e kits ganharam seleção em massa (ativar, desativar ou excluir vários de uma vez); categorias em árvore com reordenação por arrastar; montagem de item (produto e item de kit) no novo formulário, com campos que aparecem conforme o item escolhido. Correção: o ícone da categoria não era salvo ao criar.
- **Leilão, Caixas (LootBox) e Passe de Batalha — Melhoria:** os formulários de item (item do leilão, drop da caixa, recompensa de nível) foram refeitos no novo padrão, mostrando só os campos que fazem sentido para o item selecionado.
- **Itens — Novo:** catálogo de itens com busca, filtro por seção, paginação, definição de raridade com um clique nos pontos coloridos e troca da imagem do item por uma janela. O nome das raridades agora é traduzível por idioma e aparece traduzido na Loja, Leilão, Mercado de Itens, Mercado Direto e Caixas.
- **Suporte (tickets) — Correção:** a lista de tickets no painel dava erro ao abrir.
- **Notícias e Guias — Novo:** editor de texto com formatação (negrito, imagens etc.) nos conteúdos; a descrição dos guias voltou a aceitar formatação.
- **Hall da Fama — Melhoria:** a configuração passou para o novo painel; a reordenação por arrastar dos rankings ficou de fora por enquanto (seguem a ordem da configuração).
- **Enquetes, Eventos, Câmbio (Exchange), Patentes e Streamers — Melhoria:** cadastros que abriam em janela (pacotes do câmbio, patentes, afiliado do streamer) agora abrem em página cheia; respostas da enquete e horários do evento são adicionados em linhas dinâmicas.

## 15/06/2026

- **Painel administrativo — Novo:** novo visual do painel (opcional, ativado por configuração), com design moderno, menu lateral repaginado e ícones novos. As telas de plugins continuam funcionando dentro do visual novo mesmo sem terem sido adaptadas.
- **Painel administrativo — Novo:** modo escuro, com botão de alternar (lua/sol) no topo. A escolha fica salva no navegador e é aplicada sem "piscar" ao abrir as páginas.
- **Painel administrativo — Melhoria:** menu lateral organizado em duas seções, "Application" (telas principais) e "Plugins" (em ordem alfabética), cada plugin com seus próprios subitens. O menu abre automaticamente o grupo da tela em que você está.
- **Painel administrativo — Novo:** o item "Configurações" agora abre uma página única com categorias (Site, Acesso, VIP, Resets, Personagem, Rankings, Economia, Usuários e Sistema) e cartões para cada tela. Telas que antes não apareciam no menu (reset, master resets, troca de classe e de nick, mover personagem, transferências, reconstruir master skill) ficaram fáceis de encontrar, e plugins também podem colocar suas configurações lá.
- **Painel administrativo — Melhoria:** todas as telas de Configurações ganharam o visual novo: Geral (servidor, lista de servidores, site, e-mail, castle siege, connect/join server, baú externo, idioma e fuso horário), VIP, Transferência de VIP, Reset (com condições por tipo de VIP), Master Resets, Transferir resets, Reconstruir master skill, Trocar classe, Trocar nick, Mover, E-mails, Login, Cadastro (campos personalizados editados em janela) e Rankings.
- **Ranking — Melhoria:** em Configurações → Rankings, a lista virou editável na própria página: dá para ativar/desativar, renomear e reordenar arrastando, e salvar tudo de uma vez.
- **Painel administrativo — Correção:** nas configurações gerais, as opções do baú externo não estavam sendo salvas; corrigido. As dicas explicativas dos campos voltaram, agora visíveis logo abaixo de cada campo.
- **Painel administrativo — Melhoria:** telas de gestão migradas para o visual novo: página inicial (cartões de contas, personagens e guilds, filtro por período, e avisos do servidor de licença exibidos na própria página em vez de popup), Market (plugins e templates em cartões), Plugins (cartões com busca instantânea e instalação pelo cabeçalho), Templates, Ferramentas, Serviços (árvore com reordenação de categorias e serviços arrastando), Fila (resumo por status, detalhe em janela, reprocessar, excluir e limpar), Logs (interno, contas, banco de dados e acessos, com filtros em painel lateral e detalhe em janela), Tarefas agendadas, Tokens de API, Usuários, Grupos, Moedas, Carteiras, Verificação em duas etapas e Atualização do sistema.
- **Painel administrativo — Melhoria:** a grade de permissões dos Grupos foi redesenhada, agrupada por área e com "Marcar todos" em cada seção.
- **Painel administrativo — Melhoria:** listagens com ordenação por coluna, busca, paginação e escolha de itens por página. Reordenar arrastando ganhou indicador visual e confirmação por notificação, e excluir um registro atualiza a lista sem recarregar a página.
- **Carteiras — Novo:** os tipos de carteira podem ser reordenados arrastando no painel; a ordem vale também na lista de carteiras da área do jogador.
- **Painel administrativo — Correção:** os registros de consultas ao banco de dados não eram gravados mesmo com a opção ligada; corrigido. Os registros de acessos ao site passaram a ser gravados de fato (com senhas, tokens e outros dados sensíveis ocultos). Novas tarefas de limpeza de registros antigos (padrão: mais de 7 dias), agendáveis em Tarefas.
- **Painel administrativo — Correção:** a tela de Usuários do painel dava erro quando algum usuário estava sem e-mail; corrigido, junto com outros cadastros com o mesmo tipo de problema (tokens de API, caixas e rastreadores).
- **Painel administrativo — Correção:** enviar um plugin ou template (ZIP) dava erro fatal; corrigido.
- **Painel administrativo — Correção:** a tela da Fila não abria; corrigido.
- **Painel administrativo — Correção:** a listagem de Itens dava erro; corrigido.
- **Painel administrativo — Correção:** telas de plugin que dependem de recursos de outros plugins (ex.: cupons com escopos do Donate e da Loja) davam erro no painel; corrigido.
- **Painel administrativo — Melhoria:** textos que apareciam só em inglês (verificação em duas etapas, atualização do sistema, carteiras e "Painel de controle" no login) agora estão traduzidos nos 6 idiomas.

## 13/06/2026

- **Cupons — Correção:** a tela de cupons dava erro quando nenhum plugin oferecia escopos de cupom; corrigido.
- **Painel administrativo — Correção:** a atualização do sistema pelo painel falhava em alguns casos; corrigido.
- **Segurança — Melhoria:** proteção extra contra tentativas de ataque ao banco de dados pelo site.

## 12/06/2026

- **Site — Correção:** a contagem de jogadores online dava erro em servidores configurados com consulta única de online por servidor; corrigido.
- **Compatibilidade com emuladores — Correção:** reset e limpeza de master skill em servidores IGCN não funcionavam; corrigido.
- **Conta do jogador — Correção:** ao salvar o personagem, Vida e Mana perdiam as casas decimais; corrigido. O serviço de troca de classe também falhava; corrigido.
- **Carteiras — Correção:** o saldo podia aparecer zerado quando havia carteiras duplicadas na mesma conta; corrigido, e não são mais criadas duplicatas.

## 11/06/2026

- **Conta do jogador — Correção:** salvar o baú (inclusive baús estendidos), limpar inventário, limpar skills/quests e resetar master skill voltaram a funcionar (davam erro). Os campos personalizados do cadastro voltaram a ser lidos na conta, e a troca de senha ganhou proteção extra contra ataques.
- **Conta do jogador — Correção:** o login social só entra ou vincula uma conta existente se o provedor confirmar que o e-mail é verificado, evitando que alguém acesse a conta de outra pessoa. Erros do site não mostram mais detalhes internos em produção.
- **Serviços — Correção:** taxas de serviço configuradas "para todos" (sem condição) não estavam sendo cobradas.
- **Ranking — Correção:** o reset de rankings dava erro e, nos rankings de personagem e duelo, zerava só a primeira coluna. Os rankings também ganharam proteção contra configurações inválidas.
- **Site — Correção:** os nomes dos serviços passaram a aparecer também quando o idioma escolhido é inglês (antes ficavam vazios).
- **Mercado de Contas — Correção:** erro ao abrir quando a mesma conta tinha mais de um anúncio pendente.
- **Instalação — Correção:** a instalação em banco limpo falhava por ordem errada de criação das tabelas; uma tentativa que falhava no meio não trava mais o instalador em "já instalado"; instalar ou atualizar em servidor v6 já existente não estoura mais com "tabela já existe".
- **Painel administrativo — Novo:** API de integração com tokens de acesso gerenciados em **Configurações** (criar, revogar, excluir), com página de documentação, limite de requisições e acesso a downloads, notícias (com categorias) e eventos.
- **Painel administrativo — Correção:** a lista de IPs permitidos, o limite de tentativas de login e os bans não podem mais ser burlados com cabeçalhos falsos; nova opção de configuração para quem usa Cloudflare ou proxy. Textos cadastrados por jogadores e admins (confirmações de pagamento, pix/contato do mercado de contas, canal de streamers, nomes e títulos em geral) passaram a ser exibidos com segurança no painel.
- **Recompensa por voto — Correção:** o XtremeTop100 creditava o voto quando a confirmação NÃO vinha do provedor, o que permitia forjar votos.
- **Notícias — Melhoria:** a imagem de capa aceita um link externo.
- **Downloads — Melhoria:** a lista no painel mostra o status pela borda da linha e os nomes no idioma do painel.

## 09/06/2026

- **Mercado de Itens — Correção:** um preço inválido permitia comprar de graça; a compra é bloqueada enquanto o vendedor está dentro do jogo (evita perder o item); o limite de anúncios por vendedor é respeitado mesmo com cliques simultâneos; a listagem carrega mais rápido.
- **Mercado Direto — Melhoria:** a venda direta passa a ser feita pelo nome do personagem em vez do login da conta. Correção: cancelamento em duplicidade bloqueado e filtro de busca do painel corrigido.
- **Mercado de Contas — Correção:** duas compras ou duas entregas simultâneas da mesma conta não acontecem mais; anúncio duplicado bloqueado; filtro de busca do painel corrigido.

## 08/06/2026

- **Pagamentos (Doações) — Melhoria:** a lista de pedidos mostra o status em selo colorido e um botão "Pagar" nos pedidos aguardando pagamento (MorpheusPay e PagHiper); página de pagamento simplificada. Correção: erro ao iniciar pagamento pelo MorpheusPay quando a resposta vinha fora do esperado.
- **Oficina (WorkShop) — Correção:** a opção "permitir harmony" da regra salvava o valor de "permitir ancient".
- **Caixas (LootBox) — Melhoria:** as raridades passam a usar o cadastro global de raridades de itens; o menu "Raridades" próprio foi removido.
- **Troca de horas (Exchange) — Melhoria:** página redesenhada em cards com selos de VIP/moedas e custo em horas; nome e descrição dos pacotes traduzíveis.
- **Sorteio — Correção:** erro ao concluir um sorteio. Melhoria: nome e descrição traduzíveis.
- **Leilão — Correção:** erro que quebrava a página ao abrir o leilão pela segunda vez sem recarregar. Melhoria: nome e descrição traduzíveis; integração com Pusher removida.

## 07/06/2026

- **Loja (WebShop) — Melhoria:** nomes e descrições de lojas e categorias traduzíveis.
- **Pacotes — Melhoria:** nome e descrição de pacotes e categorias traduzíveis; a imagem aceita link externo.
- **Recompensa por voto — Novo:** XtremeTop100, GTop100 e TopG já vêm cadastrados (desativados) na instalação.
- **Conquistas — Melhoria:** nome e descrição traduzíveis.
- **Indicações — Correção:** metas não atingidas mostravam valor 0 (agora exibem o valor potencial); a lista de indicados mostra o melhor personagem de cada conta; o processamento automático de recompensas estava quebrado.
- **Patentes — Novo:** 10 patentes padrão (de Recruta a Marechal) por resets na instalação.
- **Resgate — Melhoria:** status em selo colorido; filtro de busca do painel corrigido.
- **Perfil — Melhoria:** página de bloqueio redesenhada; 5 pacotes de bloqueio padrão na instalação; traduções em vietnamita e chinês completadas.
- **Painel administrativo — Correção:** campos traduzíveis dentro de janelas modais não funcionavam; os nomes das permissões "banir conta" e "editar conta" estavam trocados.

## 06/06/2026

- **Serviços — Novo:** taxas de serviço podem ser cobradas em carteira ou em Ruud (quando o servidor tiver esses recursos).
- **Painel administrativo — Melhoria:** tela de grupos de usuários reformulada: permissões agrupadas por área em cards com "selecionar todos", áreas do sistema primeiro e nomes traduzidos também para os plugins.
- **Painel administrativo — Melhoria:** login mais rápido e seguro; o limite de tentativas de login não falha mais.
- **Fila de tarefas — Correção:** o processamento em segundo plano falhava por uma incompatibilidade com o banco de dados; corrigido.
- **Carteiras — Correção:** erro ao depositar ou sacar na primeira operação de uma carteira recém-criada; saldo lido corretamente.
- **Cupons — Melhoria:** página de cupons do jogador redesenhada.

## 05/06/2026

- **Guias — Melhoria:** nome, título e descrição traduzíveis. Correção: o bloco de guias nas páginas dava erro.
- **Enquetes — Novo:** bloco de enquete no construtor de páginas. Melhoria: pergunta e respostas traduzíveis.
- **Slides — Melhoria:** título traduzível.
- **Vídeos — Melhoria:** aceita o link completo do YouTube (watch e youtu.be), convertido automaticamente.
- **Páginas — Melhoria:** o layout "page-builder" exibe os blocos em largura total, sem título; ordenação por arrastar removida. Correção: conteúdos com aspas eram corrompidos ao salvar.

## 04/06/2026

- **Páginas — Novo:** construtor de páginas por blocos (Hero, Texto, Imagem+Texto, Chamada para ação) com SEO por idioma, CSS e script próprios em editor de código, escolha de layout por página, editor por idioma com "Copiar do PT", bloco de guias e suporte a blocos de outros plugins.
- **Site — Correção:** ao editar um registro, o endereço da página ganhava um "-1" indevido.
- **Mensagens — Correção:** mensagens enviadas a todos não abriam; mensagem inexistente mostra "não encontrada".
- **Login social — Correção:** desconectar a conta Google não funcionava.
- **Cloudflare Turnstile — Correção:** o plugin não funcionava por uma configuração interna incorreta; corrigido.
- **Conta do jogador — Correção:** a opção "Lembrar de mim" não causa mais o desligamento imediato logo após entrar automaticamente. O acesso automático também ficou mais seguro: a chave guardada no navegador é renovada a cada entrada, impedindo que uma chave copiada seja reutilizada.
- **Site — Melhoria:** os scripts dos plugins passaram a ser entregues em um único arquivo, guardado no navegador do visitante. As páginas ficam mais leves e carregam mais rápido nas visitas seguintes.

## 03/06/2026

- **Avatar — Novo:** o jogador pode remover o avatar do personagem e vê uma prévia da imagem escolhida antes de enviar. O painel ganhou limites de largura e altura máximas para o avatar (0 = sem limite), e trocas e remoções ficam registradas no histórico da conta.
- **Suporte (tickets) — Novo:** os departamentos agora são cadastrados no painel, com nome em cada idioma e ordenação por arrastar e soltar; instalações novas já vêm com "Suporte" e "Financeiro".
- **Suporte (tickets) — Novo:** tickets ganharam prioridade (Baixa, Normal, Alta, Crítica), escolhida pelo jogador ao abrir e ajustável pelo administrador ao responder; a lista do painel mostra os mais urgentes primeiro. Ao final do atendimento o jogador avalia com 1 a 5 estrelas, e o administrador vê a nota.
- **Suporte (tickets) — Melhoria:** listagem de tickets no painel com paginação e pesquisa por conta, assunto, departamento e responsável. O termo "Concluído" foi padronizado como "Finalizado" em todos os idiomas.
- **Site — Melhoria:** o bloco "Top Class" da página inicial ganhou destaque visual ao passar o mouse e ao selecionar uma classe, igual aos demais componentes.

## 02/06/2026

- **Passe de Batalha — Novo:** sistema completo de Passe de Batalha por temporada. O administrador cria temporadas, níveis e recompensas (gratuitas e premium) e define quais ações dão XP; o jogador acumula XP, sobe de nível e resgata recompensas de moedas, VIP, itens ou recompensas personalizadas configuradas pelo administrador.
- **Passe de Batalha — Novo:** ações que rendem XP: login diário, compra de pacote, recarga e troca de moedas, compras na loja, rifas, lances em leilão e abertura de caixas. O administrador também pode criar fontes de XP personalizadas.
- **Passe de Batalha — Novo:** o Passe Premium é comprado pelo fluxo de doação, com valor em dinheiro e escolha do meio de pagamento, e é ativado automaticamente quando o pagamento é confirmado. Continua liberado também para quem é VIP.
- **Passe de Batalha — Melhoria:** página pública em faixa horizontal (recompensas gratuitas em cima, níveis com barra de progresso no meio, premium embaixo), visível também para visitantes sem login, que veem um cadeado no lugar do botão de resgate. Recompensas de item mostram a imagem real do item com detalhes ao passar o mouse, e nome e descrição da temporada podem ser traduzidos. No painel, arrastar um nível leva suas recompensas junto e o formulário de item já vem preenchido ao editar.
- **Eventos — Melhoria:** página de eventos redesenhada em formato de agenda: nome e próximo horário à esquerda, contagem regressiva à direita, ícone por categoria e borda verde (falta menos de 15 minutos) ou amarela (menos de 1 hora). O destaque na página inicial ficou mais compacto. Textos que faltavam em japonês, russo, vietnamita e chinês foram adicionados.
- **Site — Melhoria:** lista da equipe na barra lateral redesenhada, com ponto verde para quem está online.

## 01/06/2026

- **Conta do jogador — Novo:** nova página "Dados pessoais" no painel do jogador, com documento, telefone, tipo e chave PIX. O campo CPF virou "Documento" e aceita outros documentos, como passaporte. Nas doações, documento e telefone já vêm preenchidos e são guardados após o pagamento.
- **Conta do jogador — Correção:** cadastro pelo Facebook ou Google passa a salvar a vinculação no lugar certo, para que o login social reconheça a conta. Falhas inesperadas durante o cadastro, a ativação ou o login agora são exibidas em vez de travar em silêncio, e acessar "sair" sem estar logado não gera mais erro.
- **Conta do jogador — Correção:** autenticação em duas etapas: a página de ativação exige estar logado, não é mais possível substituir a chave existente sem confirmar o código atual e o redirecionamento após a verificação só aceita páginas do próprio site.
- **Oficina (WorkShop) — Correção:** um item que já está acima do nível ou opção máximos permitidos pela regra não gera mais cobrança indevida. A troca de baú passou a ser feita por abas com links diretos, no lugar da lista suspensa.
- **Downloads — Melhoria:** a seção de requisitos foi redesenhada com blocos "Mínimo" e "Recomendado", ícones e cores. No painel, o formulário de download tem campos traduzíveis por idioma e a listagem é ordenada por arrastar e soltar.
- **Ranking — Correção:** um filtro de classe inválido na URL não causa mais erro na página de rankings.

## 30/05/2026

- **Mercado de Contas — Novo:** filtros por faixa de preço, level, resets, master resets e tipo de VIP, além de ordenação por resets e master resets. Quando não há contas à venda, a página mostra apenas o aviso, sem filtros.
- **Painel administrativo — Novo:** sistema de raridades de itens (Itens → Raridades): cadastro com nome e cor, ordenação por arrastar e soltar e, na listagem de itens, basta clicar no ícone da raridade para atribuir ou remover, sem recarregar a página.
- **Site — Novo:** no Mercado de Itens, Leilão, Mercado Direto e Loja, os itens exibem a raridade como etiqueta colorida sobre a imagem, e o fundo da imagem usa a cor da raridade.
- **Mercado de Itens — Melhoria:** filtro de categorias apenas com ícones (nome ao passar o mouse) e contagem de itens disponíveis por categoria; classes como botões com imagem e Ancient em lista suspensa.
- **Oficina (WorkShop) — Melhoria:** escolha da moeda em cartões clicáveis com o total em destaque; seleção de personagem no mesmo estilo de cartão do restante do site, com avatar, classe, level e resets.
- **Pagamentos — Melhoria:** seleção do meio de pagamento padronizada (cartão clicável com a logo) no Mercado de Contas, Mercado Direto e compra de VIP. A chave PIX passa a ser validada conforme o tipo (CPF, CNPJ, e-mail, telefone ou chave aleatória) no Resgate e no Mercado de Contas.
- **Site — Melhoria:** saldos de moedas e carteiras nas páginas de Troca e de Resgate exibidos em cartões.
- **Compatibilidade com emuladores — Melhoria:** suporte ao sistema Muun ativado para MuDevs Season 19, 20 e 21 e IGCN Season 21.

## 29/05/2026

- **Mercado de Itens — Melhoria:** filtro por categoria reorganizado em 20 categorias nomeadas (espadas, machados, asas, pets, anéis, joias, consumíveis e outras); joias passam a ser classificadas corretamente, e as categorias Muun e Pentagram aparecem apenas em servidores que as suportam.
- **Mercado de Itens — Novo:** filtros avançados por skill, ancient (+5/+10), socket (elemento), refine e excellent com seleção múltipla; Luck, Harmony e Refine viraram botões. Os filtros só são aplicados ao clicar em "Filtrar". Os cartões seguem o mesmo padrão da loja e mostram os atributos do item (excellent, ancient, socket, harmony, luck, skill, refine) no lugar do nome do vendedor; a página "Vender" também exibe os itens em cartões.
- **Painel administrativo — Novo:** botão "Comprovante" nos pedidos pagos de Doações, Mercado Direto e Mercado de Contas, gerando um comprovante com dados do usuário, pedido e pagamento, seção de observações com aviso legal e texto em todos os idiomas.
- **Painel administrativo — Melhoria:** pedidos do Mercado de Contas ganharam coluna de comissão, link para o comprovante do pagamento e o valor "A pagar" passou a usar a taxa gravada no pedido.
- **Painel administrativo — Novo:** tela de monitoramento da fila de tarefas em Configurações → Fila: resumo por status, lista com filtros, detalhe de cada tarefa, reprocessar as que falharam, excluir e limpar em massa.
- **Site — Melhoria:** e-mails de alerta de login, confirmação de e-mail, nova senha, recuperação de senha e compra de conta passam a ser enviados em segundo plano, com novas tentativas automáticas em caso de falha; a resposta ao usuário fica mais rápida.
- **Conta do jogador — Correção:** ajustadas a verificação de dias na transferência de VIP e a verificação de VIP na compra de pacote.
- **Conta do jogador — Melhoria:** página inicial do painel redesenhada: cartão de identidade com nome, VIP e duas etapas (com botão para ativar/desativar), saldos com atalhos "Recarregar" e "Comprar", personagens em cartões com avatar e selo "Online", e última conexão em uma faixa de rodapé (personagem, servidor, IP e data). A barra lateral do painel mostra um mini cartão da conta e a lista de personagens usa o mesmo estilo de cartão.
- **Conta do jogador — Melhoria:** página de redes sociais em lista com logo, status "conectado/não conectado" e botão de ação.
- **Perfil — Melhoria:** página do personagem redesenhada em duas colunas: atributos em blocos, barras de HP/MP, Zen e Ruud, selos Hero/PK/Online, cartão da guilda com logo e equipamentos ao lado. Página da guilda com membros ordenados por cargo (Mestre, Sub-Mestre, Membro), indicador de quem está online, selo de Sub-Mestre e faixa vermelha no topo.
- **Indicações — Melhoria:** área de indicações redesenhada: link de convite com botão copiar, contadores de indicações, moedas já ganhas e pendentes com botão "Resgatar" sempre visíveis, e lista de metas com status. A lista de indicados passou a usar cartões de personagem, e erros de digitação nos textos foram corrigidos.
- **Streamers — Melhoria:** página do streamer redesenhada: pedido de parceria, link de divulgação com botão copiar e cartões de status, indicações, cashback e Twitch.
- **Sorteio (Rifas) — Melhoria:** página da rifa redesenhada em duas colunas, com grade de números por estado (disponível, selecionado, meus, vendido), legenda, barra de progresso, preço e total, e os números vendidos são atualizados em tempo real. Lista de rifas em cartões com o número sorteado nas encerradas e aviso quando não há rifas abertas.
- **Leilão — Melhoria:** cartões e página inicial redesenhados; melhor lance e tempo restante atualizados em tempo real; alerta visual quando faltam 30 segundos (amarelo) e 10 segundos (vermelho); itens encerrados somem suavemente. Nova janela de lance mostrando lance inicial e melhor lance, com validação do valor.
- **Caixas (LootBox) — Melhoria:** visual totalmente renovado: roleta com aro, ponteiro e nome dos itens em cada fatia, palco escuro com destaque de luz, painel de preço, saldo e ação, lista de itens possíveis com tamanho uniforme e página de presente redesenhada. O saldo aparece formatado.
- **Conquistas — Melhoria:** lista redesenhada com barras de progresso por requisito, status (Resgatado, Disponível, Incompleto) e recompensas em etiquetas.
- **Mercado Direto — Melhoria:** lista em cartões com etiqueta de status colorida, comprador e vendedor, e botões de ação (Cancelar, Pagar, Continuar pagamento, Retirar item). O destino da venda passa a ser o nome do personagem em vez da conta.
- **Mercado de Contas — Novo:** ao vender, o vendedor informa um título de exibição (mínimo 10 caracteres) e o tipo de chave PIX; o título substitui o nome do vendedor em toda a listagem. Cartões com avatares dos personagens, selo VIP, saldos e preço; página da conta com barra lateral fixa e abas por personagem com atributos e inventário; ao passar o mouse no personagem aparece um resumo com atributos, level, mapa e guilda.
- **Loja (WebShop) — Melhoria:** cartões de produto redesenhados (imagem com fundo colorido, selos de nível e quantidade, barra de estoque, preço e botão), lista de lojas em cartões, ofertas em destaque na barra lateral com imagem, preço e vendidos, e novos ícones para as 17 categorias de itens. A seção "Disponível para" mostra as classes como ícones com o nome ao passar o mouse e agora aparece em todos os tipos de produto.
- **Pacotes — Melhoria:** listagem com abas de categoria, cartões com selos de benefícios (VIP, moedas, kit de itens), barra de disponibilidade e botão "Esgotado"; página do pacote em duas colunas com preço e saldo em cartões, "O que está incluído" e itens do kit em tamanho uniforme.
- **Notícias — Novo:** categorias de notícias cadastradas no painel (Notícias → Categorias), com nome em cada idioma e ordenação por arrastar e soltar; título, texto e descrição das notícias traduzíveis no mesmo formulário; comentários nas notícias; visual renovado (cartão com miniatura e resumo, artigo com capa e comentários).
- **Ranking — Melhoria:** listagens em formato de lista com avatar, classe, guilda e pontuação; pódio dos 3 primeiros em todos os rankings (inclusive guildas, contas e gens); barra lateral redesenhada.
- **Hall da Fama — Melhoria:** visual renovado: primeiro lugar em destaque com avatar maior, demais posições com medalhas ouro, prata e bronze e abas de período (tempo real, diário, semanal, mensal); cores alinhadas à cor principal do site.
- **Pagamentos (Doações) — Melhoria:** telas de doação redesenhadas: lista de meios de pagamento, formulário centralizado, tela PIX com QR code, passo a passo e botão copiar, e histórico de pedidos. A integração com o Mercado Pago foi atualizada, corrigindo um erro fatal em algumas páginas.
- **Site — Melhoria:** página inicial com Top Class (avatar, level, pontuação e guilda) e Castle Siege (logo da guilda, mestre e próximo cerco) redesenhados; página de informações do servidor com barra de rates, estatísticas, eventos, comandos e planos VIP em cartões; páginas de VIP (resumo, vantagens, pagamento) e de moedas redesenhadas com o saldo do usuário logado; menu do usuário no topo com nome, VIP, saldos por moeda, serviços com notificações e botão sair.
- **Site — Melhoria:** notificações (sininho), mensagens, guias, tracker, vídeos, contagem regressiva, página inicial do mercado, avisos com ícone por tipo, tabelas e menus laterais redesenhados no mesmo padrão visual, com cantos arredondados em todos os elementos.
- **Site — Correção:** o mapa do site (sitemap) voltou a funcionar após a mudança nas notícias.
- **Painel administrativo — Correção:** campos traduzíveis passam a mostrar os erros de validação, e vários campos traduzíveis na mesma tela funcionam de forma independente. Componentes de seleção e editor de texto do painel que eram bloqueados pelo navegador voltaram a carregar.
- **Painel administrativo — Novo:** montagem de itens no Leilão, nos kits da Loja e nas Caixas com suporte a Mastery e bônus de Mastery.
- **Compatibilidade com emuladores — Correção:** Mastery não aparecia em servidores GGCode e o bônus de Mastery era perdido ao salvar; edições de errtel, pentagram, elemento, opção e quantidade não eram gravadas; itens da seção de espadas não eram identificados; itens sem suporte a Mastery causavam erro.
- **Site — Correção:** corrigido erro fatal que afetava diversas telas com operações de gravação.
- **Painel administrativo — Novo:** opção "Campo de país" em Configurações → Cadastro para mostrar ou ocultar a seleção de país no formulário de cadastro.
- **Instalação — Novo:** instalador com design reformulado e traduzido em todos os idiomas; suporte a atualização a partir da versão 6, sem pedir credenciais de administrador; proteção contra reinstalação acidental e várias correções de segurança no processo.
- **Instalação — Correção:** a atualização da versão 6 para a 7 não aplicava as novidades do banco de dados; corrigido.
- **Site — Correção:** revisão geral das traduções: dezenas de textos faltantes adicionados em todos os idiomas e correções em chinês, japonês, vietnamita, russo e português (mensagens que mostravam números no lugar dos valores, termos traduzidos errado). Todos os plugins passam a ter tradução em espanhol, japonês, russo, vietnamita e chinês.
- **Painel administrativo — Novo:** tempo de atualização da contagem de jogadores online nas Configurações gerais; limite, tempo de atualização e busca por classes dos rankings editáveis nas Configurações de ranking.
- **Painel administrativo — Correção:** campos de taxa dos meios de pagamento aceitam vírgula como separador decimal; o campo "limite" das notícias ficou obrigatório e numérico; as perguntas secretas (Configurações → Cadastro) respeitam o limite de caracteres do servidor; a troca de nick exige 4 caracteres também no formulário.
- **Segurança — Correção:** corrigidos redirecionamento indevido no login e falhas nas buscas e registros do painel; a senha não aparece mais em texto no e-mail de recuperação; trocar o e-mail exige a senha atual.
- **Painel administrativo — Novo:** módulo Configurações → Login: redirecionamento após o login, alerta por e-mail de acesso suspeito, bloqueio por tentativas e exibição de captcha após um número de falhas.
- **Segurança — Novo:** proteção contra robôs nos formulários, limite de requisições nas páginas públicas, reCAPTCHA versão 3 (invisível, com pontuação mínima configurável) e Cloudflare Turnstile corrigido; o captcha antigo foi removido.
- **Segurança — Novo:** bloqueio de login por conta além de por IP; links de ativação (24 horas) e de redefinição de senha (2 horas) expiram; e-mail de alerta em login suspeito (novo IP ou tentativas falhas anteriores).
- **Compatibilidade com emuladores — Novo:** suporte ao emulador GGCode.
- **Pagamentos (MorpheusPay) — Correção:** campo de e-mail no checkout e no saque corrigido; chave PIX do tipo telefone recebe o +55 automaticamente.
