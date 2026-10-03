# Banco de dados do site

O Morpheus guarda as informações do site (pedidos, carteiras, notícias, tickets, configurações etc.) em tabelas próprias. Na instalação você escolhe **onde** essas tabelas ficam.

## As duas opções

**1. No mesmo banco do jogo (padrão).**
As tabelas do site são criadas dentro do banco do jogo, identificadas por um prefixo próprio no nome para não se misturarem com as do MuOnline. É a opção mais simples: um banco só, um backup só.

**2. Em um banco separado.**
As tabelas do site são criadas em outro banco (por exemplo `MorpheusWeb`). O banco do jogo fica intocado, contendo só as tabelas do MuOnline.

Escolha a opção 2 se você quer:

- backups e restaurações do site e do jogo independentes;
- restaurar um backup antigo do jogo sem perder pedidos, carteiras e notícias do site;
- manter o banco do jogo limpo, sem tabelas de terceiros, como alguns administradores de servidor exigem.

## Como escolher

No instalador, na etapa **Database**, há o campo **Banco de dados do site (opcional)**:

- deixe em branco para usar o mesmo banco do jogo (padrão);
- informe um nome (ex.: `MorpheusWeb`) para usar um banco separado. Se o banco não existir, o instalador cria.

Os dois bancos precisam estar no **mesmo SQL Server** e o usuário informado no instalador precisa ter permissão nos dois. Depois de instalado, tudo funciona igual: painel, plugins, compras, atualizações.

## Perguntas frequentes

**Já instalei tudo no banco do jogo. Posso mudar para um banco separado?**
A escolha é feita só em instalação nova. Para mudar depois, é preciso mover as tabelas do site para o novo banco e apontar o Morpheus para ele, um procedimento manual. Faça backup antes e fale com o suporte para fazer a migração com segurança.

**Preciso mudar alguma coisa nos plugins ou no tema?**
Não. Plugins, temas e atualizações usam o mesmo nome de sempre para as tabelas e o Morpheus traduz sozinho.

**Posso usar um servidor SQL diferente para o site?**
Não. O site precisa cruzar dados com o jogo (personagens, contas, baú) na mesma transação, então os dois bancos precisam estar na mesma instância do SQL Server.

**A opção de banco separado aparece na atualização (upgrade)?**
Não. Na atualização de uma instalação existente o campo fica desabilitado, porque as tabelas já existem no banco do jogo.

**Como faço o backup?**
Faça backup dos dois bancos: o do jogo e o do site. Se restaurar só um deles, o outro continua como estava.
