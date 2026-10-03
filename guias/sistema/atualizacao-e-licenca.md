# Atualização, licença e Morpheus Market — Guia do Cliente

No painel, a atualização aparece em **Configurações → Atualizar** (a tela se chama **Atualização do Morpheus MuWeb**) e a loja oficial aparece no menu lateral como **Mercado da Morpheus**.

Este guia explica, de forma simples, **como manter o Morpheus MuWeb atualizado**, **como funciona a licença** do seu site e **como comprar, instalar e ativar plugins e temas** — tudo pelo painel administrativo.

---

## O que é a atualização do sistema?

A equipe Morpheus lança versões novas com recursos, melhorias e correções. Você não precisa baixar nada manualmente: o painel **avisa quando há versão nova**, mostra **o que mudou** e aplica a atualização com **um clique**.

Benefícios de manter o site em dia:

- novos recursos e plugins passam a funcionar (plugins novos podem exigir a versão mais recente);
- correções de segurança e de pagamentos chegam na hora;
- o suporte sempre atende com base na versão atual.

---

## Conceitos principais

### 1. Versão

Cada instalação tem um número de versão (ex.: 7.0.0). A tela **Configurações → Atualizar** mostra a sua versão e, quando existe, a versão mais nova disponível.

### 2. Licença

A sua licença é o que autoriza o site a funcionar no **seu domínio** e no **seu servidor**, e define **quais plugins** você pode ativar. Ela é verificada automaticamente — não há chave para digitar.

### 3. Mercado da Morpheus

É a vitrine oficial de **plugins** e **temas**, dentro do próprio painel. Nela você vê preço, descrição e autor, e é levado à loja para comprar (ou ao download, no caso de temas gratuitos).

### 4. Super usuário

Só usuários marcados como **Super usuário** (em **Configurações → Usuários**) podem abrir a tela de atualização e aplicar versões novas.

---

## Como atualizar (passo a passo)

### Passo 1 — Ver a versão e as novidades

Abra **Configurações → Atualizar**. A tela pode mostrar três situações:

- **Você está atualizado** — com a mensagem "PARABÉNS! Você está usando a versão mais recente do Morpheus MuWeb X". O botão **Changelog** abre uma janela com o histórico de mudanças.
- **Nova versão disponível** — mostra **Sua versão**: a atual → a nova, com os botões **Atualizar** e **Changelog**. O painel também cria uma notificação **Atualização disponível** ("Versão X disponível") no sino de notificações.
- **Não foi possível conectar aos servidores do Morpheus MuWeb** — o site não conseguiu falar com o servidor da Morpheus. Verifique a conexão de internet do servidor web e tente de novo mais tarde.

> Antes de clicar em **Atualizar**, abra o **Changelog** e leia o que muda. Se você tem um tema personalizado, veja se há mudanças que o afetem.

### Passo 2 — Fazer backup

Faça um backup do **banco de dados** e dos **arquivos do site**. A atualização é segura, mas o backup é a sua garantia para voltar atrás em qualquer imprevisto.

### Passo 3 — Aplicar

1. Clique em **Atualizar**.
2. Confirme na pergunta "Tem certeza que deseja atualizar a versão do Morpheus MuWeb?".
3. Aguarde sem fechar a página.

O que acontece nesse momento:

- o site **baixa** o pacote de cada versão intermediária (se você está várias versões atrás, todas são aplicadas em sequência);
- os **arquivos do sistema** são substituídos pelos novos;
- o **banco de dados** é atualizado com as novidades da versão;
- a **licença** é renovada em seguida, automaticamente.

Ao terminar, aparece "Morpheus MuWeb atualizada com sucesso para versão X!" e a tela volta a mostrar **Você está atualizado**.

Só uma atualização roda por vez: se outra pessoa já clicou em **Atualizar**, a segunda tentativa recebe a mensagem **There is already an update in progress**.

### O que é preservado

- **Suas configurações** (tudo o que você define no painel) ficam no banco de dados e não são tocadas.
- **Dados** de jogadores, pedidos, carteiras, notícias, tickets etc. permanecem — a atualização só acrescenta o que é novo na estrutura.
- **Arquivos enviados por você** (logo, imagens de notícias, downloads) não fazem parte do pacote de atualização.
- **Plugins e temas de terceiros** também não fazem parte do pacote.

> Se você fez alterações **diretamente nos arquivos do tema padrão** ou de plugins oficiais, elas podem ser sobrescritas. Para personalizar o visual, use um tema próprio (veja o guia **Templates**/temas) em vez de editar o padrão.

### Se a atualização falhar

A mensagem "Não foi possível atualizar a Morpheus MuWeb no momento, tente mais tarde!" indica que algum passo não completou. As causas mais comuns:

- o servidor web **não tem permissão de escrita** na pasta do site ou na pasta temporária;
- **sem internet** no servidor web ou o servidor da Morpheus indisponível naquele momento;
- a extensão **ZIP** do PHP não está instalada.

Corrija a causa e clique em **Atualizar** de novo — o processo pode ser repetido com segurança. Se o site ficar com erro depois de uma falha, restaure o backup e fale com o suporte.

---

## Licença

### Como funciona

- A licença é **vinculada ao domínio** informado na compra e ao(s) **IP(s) do servidor** onde o site roda.
- O site **se comunica com o servidor da Morpheus automaticamente** (cerca de uma vez por hora) e guarda uma cópia local da licença. Você não precisa digitar chave nenhuma.
- Se o servidor ficar **sem conseguir contato por mais de 3 dias**, a cópia local vence e o site passa a ser tratado como sem licença até conseguir se comunicar de novo. Por isso o servidor web precisa de acesso à internet.
- A licença também define **a versão** que você pode usar e **os plugins** que pode ativar. Plugins que não estão na sua licença são desativados automaticamente, e ao tentar ativar um deles o painel mostra "Você precisa adquirir esse plugin antes de usar!".
- Avisos da equipe Morpheus para a sua instalação aparecem no **Painel** (tela inicial).

### Mensagens de licença

Quando a verificação não passa, o site redireciona para uma página explicativa no site da Morpheus. As situações possíveis são: licença **ilegal** (domínio/IP/versão não conferem ou sem contato há mais de 3 dias), **expirada**, **inválida**, **cancelada** ou **corrompida**.

Se você vir a página de **licença ilegal**:

1. Confira se o site está no **domínio exato** da licença (o domínio principal, sem contar `www`).
2. Confira se o **IP do servidor** é o que está cadastrado na licença. Mudou de hospedagem? Peça a atualização do IP ao suporte.
3. Confira se o servidor web **acessa a internet**.
4. Se trocou de domínio, é preciso solicitar a mudança — conforme os **Termos de uso** aceitos na instalação, a troca de domínio tem uma taxa de manutenção.

### Cloudflare e proxies

Sites atrás do **Cloudflare** (ou proxy semelhante) funcionam normalmente: a verificação reconhece que o domínio aponta para o Cloudflare e valida pelo IP real do servidor. Só garanta que o IP do servidor cadastrado na licença é o IP real da máquina, não o do proxy.

---

## Mercado da Morpheus

No menu lateral, abra **Mercado da Morpheus** e escolha **Plugins** ou **Templates**. As mesmas vitrines também estão no botão **Mercado**, no topo das telas **Plugins** e **Configurações → Templates**.

### Plugins

Cada cartão mostra a imagem, o nome, o **preço**, a descrição e o autor do plugin, com o botão **Comprar**, que abre a loja em outra aba. No topo há um banner com o pacote de todos os plugins.

Depois da compra, o plugin passa a fazer parte da sua licença. Se ele já estiver na sua instalação, basta ativá-lo em **Plugins**; caso contrário, você recebe o arquivo ZIP e o instala conforme a seção abaixo.

### Templates (temas)

Cada cartão mostra o tema com preço ou **Grátis**. Temas pagos têm o botão **Comprar**; temas gratuitos têm o botão **Baixar**. Quando há demonstração, aparece também **Visualizar**.

Se a vitrine não carregar, a tela mostra "Nenhum plugin encontrado" ou "Nenhum template encontrado" — normalmente é falta de conexão do servidor web com a internet.

---

## Instalar plugin ou tema por arquivo ZIP

### Plugin

1. No menu lateral, abra **Plugins**.
2. Clique em **Instalar** (no topo da lista). Abre uma janela com o campo **Plugin (ZIP)**.
3. Selecione o arquivo ZIP recebido e clique em **Instalar**.
4. Com a mensagem "Plugin instalado com sucesso!", o plugin aparece na lista como **Inativo**. Clique em **Ativar**.

Mensagens que podem aparecer:

- "ZIP corrompido ou não reconhecido." — o arquivo não é um ZIP válido; baixe de novo.
- "Plugin X já existe!" — esse plugin já está na instalação; use **Ativar** na lista.
- "Arquivo de informações do plugin não foi encontrado!" — o ZIP não é um plugin do Morpheus (ou foi compactado com a pasta errada). Peça o arquivo original ao fornecedor.

### Tema

1. Abra **Configurações → Templates** (a tela se chama **Templates disponíveis**).
2. Clique em **Instalar** no topo. Abre uma janela com o campo **Template (ZIP)**.
3. Selecione o arquivo e clique em **Instalar**. A mensagem de sucesso é "Template instalado com sucesso!".
4. O tema aparece como um cartão com imagem, nome e autor. Clique em **Ativar** no tema que quer usar; o tema em uso aparece com o selo de ativo.

Se o tema já existir na instalação, aparece "Template X já existe!".

---

## Ativar e desativar plugins

Na tela **Plugins**, cada plugin aparece como um cartão com nome, descrição, **Versão**, autor e o selo **Ativo** ou **Inativo**. Há um campo de busca para encontrar o plugin pelo nome.

- **Ativar** — liga o plugin. Os menus e as telas dele aparecem no painel na hora, e os serviços que ele oferece são registrados. Se o plugin depender de outro, o painel avisa: "O plugin X depende do plugin Y estar ativo" — ative o outro primeiro.
- **Desativar** — desliga o plugin. As telas somem do painel e os jogadores deixam de ver o recurso no site; os dados ficam guardados e voltam quando você ativar de novo.
- **Configurar** — aparece nos plugins ativos que têm tela própria de configuração.

Só plugins **incluídos na sua licença** podem ser ativados (exceto os gratuitos). Ao tentar ativar um plugin não adquirido, o painel mostra "Você precisa adquirir esse plugin antes de usar!".

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|------|------|
| Ver a versão atual e se há atualização | **Configurações → Atualizar** |
| Ler o que mudou em cada versão | **Configurações → Atualizar** → **Changelog** |
| Aplicar uma atualização | **Configurações → Atualizar** → **Atualizar** (só Super usuário) |
| Dar a alguém permissão para atualizar | **Configurações → Usuários** → **Super usuário** |
| Ver avisos da equipe Morpheus | **Painel** (tela inicial) |
| Comprar plugins | **Mercado da Morpheus → Plugins** → **Comprar** |
| Comprar ou baixar temas | **Mercado da Morpheus → Templates** → **Comprar** / **Baixar** |
| Instalar plugin por ZIP | **Plugins** → **Instalar** → **Plugin (ZIP)** |
| Instalar tema por ZIP | **Configurações → Templates** → **Instalar** → **Template (ZIP)** |
| Ativar / desativar um plugin | **Plugins** → **Ativar** / **Desativar** |
| Trocar o tema do site | **Configurações → Templates** → **Ativar** |
| Limpar o cache depois de uma mudança | **Configurações → Ferramentas** → **Limpar cache** |
| Alterar domínio ou IP da licença | Suporte da Morpheus |

---

## Dicas e boas práticas

- **Atualize em horário de pouco movimento** e avise a equipe. A atualização leva poucos minutos, mas é melhor sem jogadores comprando naquele instante.
- **Backup antes, sempre.** Banco de dados e arquivos.
- **Leia o Changelog.** Ele diz se uma versão traz mudanças no tema ou em plugins que você usa.
- **Não edite arquivos do tema padrão.** Crie um tema próprio para personalizar; assim as atualizações nunca apagam o seu trabalho.
- **Mantenha o IP da licença atualizado** ao trocar de hospedagem — faça isso antes de apontar o domínio para o servidor novo.
- **Limite o Super usuário** a uma ou duas pessoas de confiança.
- **Depois de atualizar ou instalar um tema**, use **Configurações → Ferramentas → Limpar cache** se alguma tela parecer desatualizada.

---

## Perguntas frequentes

**A tela Configurações → Atualizar não aparece para mim.**
Ela só existe para usuários marcados como **Super usuário**. Peça para quem administra o painel ativar essa opção no seu usuário em **Configurações → Usuários**.

**A atualização apaga minhas configurações ou meus pedidos?**
Não. Configurações e dados ficam no banco de dados e são preservados; a atualização só acrescenta o que é novo.

**Estou várias versões atrás. Preciso atualizar uma por uma?**
Não. Ao clicar em **Atualizar**, o site aplica todas as versões intermediárias em sequência, na ordem certa.

**O site foi para uma página de "licença ilegal" do nada.**
Verifique se o servidor web continua com acesso à internet (sem contato por mais de 3 dias a licença local vence) e se o IP ou o domínio do servidor mudaram. Se nada mudou, fale com o suporte informando o domínio.

**Posso usar a mesma licença em dois domínios (ex.: site de teste)?**
Não. A licença vale para um domínio. Para ambientes de teste, fale com o suporte.

**Comprei um plugin e ele não ativa.**
Depois da compra a licença é renovada automaticamente em até uma hora. Se continuar com "Você precisa adquirir esse plugin antes de usar!", aguarde alguns minutos e tente de novo; persistindo, confirme com o suporte se a compra foi vinculada ao seu domínio.

**Desativar um plugin apaga os dados dele?**
Não. Os dados ficam guardados; ao ativar de novo, tudo volta como estava.

**Instalei um tema e ele ficou "quebrado".**
Confira se o tema é compatível com a sua versão (o cartão da loja e o Changelog ajudam) e limpe o cache em **Configurações → Ferramentas**. Se persistir, volte para o tema padrão em **Configurações → Templates** e contate o autor do tema.

---

> Precisa trocar o domínio ou o IP da licença, ou teve problema em uma atualização? Entre em contato com o suporte informando o domínio do site e a versão mostrada em **Configurações → Atualizar**.
