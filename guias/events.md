# Eventos — Guia do Cliente

Este guia explica, de forma simples, o que é o sistema de Eventos, como o jogador usa e como você configura pelo painel. Não é necessário conhecimento técnico.

---

## O que é o sistema de Eventos?

Os Eventos mostram a **agenda do servidor**: quais eventos acontecem e a que horas, com uma **contagem regressiva** para o próximo e **avisos no navegador** quando um evento está prestes a começar.

É uma ferramenta de **engajamento e organização**:

- O jogador sempre sabe o que vem a seguir e quando entrar para participar.
- Mais gente online na hora certa, com eventos mais cheios.
- A comunidade fica informada sem você precisar avisar manualmente.

A agenda aparece na página de Eventos do site e, para os eventos em destaque, também no bloco da barra lateral. Tudo se atualiza sozinho.

---

## Conceitos principais

### O evento

É cada atividade da agenda (ex.: *Blood Castle*, *Invasão*, *Boss do servidor*). Tem um **Nome**, pertence a uma **Categoria** e define, no bloco **Agendamento**, quando acontece. O nome do evento é um texto único (não é traduzido por idioma).

### O agendamento

Cada evento tem **uma** forma de recorrência. No campo **Recorrência** você escolhe o modo, e o formulário mostra só o que aquele modo precisa:

- **Todos os dias**: acontece diariamente. No campo **Horários** você escolhe cada horário e aperta Enter ou **Adicionar**; ele vira uma etiqueta com um "x" para remover.
- **Por dia da semana**: ex.: só nas terças e quintas. Em **Horários por dia da semana** você usa **Adicionar dia** para criar uma linha por dia, escolhe o **Dia** e adiciona os horários daquela linha.
- **Texto livre**: para eventos sem hora fixa. Você preenche o campo **Texto exibido** (ex.: *Sábado 20h, após o Castle Siege*) e o site mostra esse texto no lugar do contador. Esse modo não aceita datas nem horários, e o evento não tem contagem regressiva nem aviso no navegador.

Nos dois primeiros modos o site calcula sozinho a próxima ocorrência e a contagem regressiva. As etiquetas ficam sempre em ordem e sem repetição. Se faltar horário, ou um dia da semana aparecer em duas linhas, o painel avisa na hora e não salva.

Os horários são sempre interpretados no **Fuso horário** definido em **Configurações → Eventos**. O fuso atual aparece como um botão no canto do bloco **Agendamento**, e clicar nele leva direto à configuração.

### A duração

O campo **Duração (minutos)** é opcional. Com ele preenchido, enquanto o evento está rolando o site mostra o destaque **Ao vivo** com o tempo restante até terminar, para o jogador saber que dá para entrar agora. Sem duração, o evento nunca aparece como ao vivo.

### As categorias

Servem para organizar os eventos em grupos (ex.: *PvP*, *PvE*, *Especiais*). No site, cada categoria vira uma **aba** da agenda. A categoria tem apenas um **Nome**, que pode ser escrito em vários idiomas.

### Destaque e notificação

Cada evento tem dois interruptores:

- **Destaque**: o evento aparece também no bloco de eventos da barra lateral do site, ganhando mais visibilidade.
- **Notificável**: mostra ao jogador um interruptor de aviso naquele evento. Com ele ligado, o navegador avisa o jogador 5 minutos antes do início. Se você desligar, o jogador não vê a opção.

### Fuso horário

Em **Configurações → Eventos** você define o **Fuso horário** do servidor. É o que faz a contagem regressiva e os horários aparecerem certos para todos os jogadores, onde quer que estejam.

---

## Como o jogador usa

1. Abre a página de Eventos do site e vê a agenda organizada em abas por categoria, com o próximo horário e a contagem regressiva de cada evento.
2. Quando um evento está perto de começar, a linha muda de cor; se o evento tem duração, aparece **Ao vivo** com o tempo restante.
3. Nos eventos **Notificáveis**, o jogador liga o interruptor de aviso. O navegador pede permissão para notificar e, 5 minutos antes do evento, exibe um aviso. A escolha fica guardada no navegador dele.
4. Os eventos marcados como **Destaque** aparecem também no bloco da barra lateral, em qualquer página do site.

---

## Como configurar (passo a passo)

No menu lateral do painel, em **Eventos**, você tem **Eventos** (a lista) e **Categorias**. No topo da lista de eventos ficam os botões **Estatísticas**, **Categorias** e **Configurações**.

### 1. Ajustar o fuso horário

1. Abra **Configurações → Eventos** (ou o botão **Configurações** no topo da lista de eventos).
2. Escolha o **Fuso horário** do servidor e clique em **Salvar**.

Faça isso primeiro: é o que garante horários e contagens corretos.

### 2. Criar as categorias

1. Em **Eventos → Categorias**, clique em **Adicionar**.
2. Preencha o **Nome** nos idiomas que desejar e clique em **Salvar**.
3. Na lista, arraste as linhas para definir a ordem das abas no site.

### 3. Criar o evento

1. Em **Eventos → Eventos**, clique em **Adicionar**.
2. Informe o **Nome** e escolha a **Categoria**.
3. Ligue **Destaque** e/ou **Notificável** conforme quiser.
4. Se quiser o destaque **Ao vivo**, preencha a **Duração (minutos)**.
5. No bloco **Agendamento**, escolha a **Recorrência**:
   - **Todos os dias**: adicione os horários no campo **Horários**.
   - **Por dia da semana**: use **Adicionar dia**, escolha o **Dia** e adicione os horários de cada linha.
   - **Texto livre**: escreva o **Texto exibido**.
6. Clique em **Salvar**. Na lista, arraste as linhas para definir a ordem em que os eventos aparecem.

### 4. Acompanhar

O botão **Estatísticas**, no topo da lista, mostra **Total de eventos**, **Eventos em destaque**, **Eventos notificáveis**, **Categorias** e a tabela **Eventos por categoria**.

---

## Onde configurar cada coisa

| O que você quer fazer | Onde, no painel |
|------------------------|-----------------|
| Criar ou editar eventos | **Eventos → Eventos**, botão **Adicionar** ou **Editar** |
| Escolher o tipo de agenda | Campo **Recorrência** do bloco **Agendamento** |
| Definir os horários diários | Campo **Horários** (modo **Todos os dias**) |
| Definir horários por dia | Campo **Horários por dia da semana** (modo **Por dia da semana**) |
| Mostrar um texto no lugar do contador | Campo **Texto exibido** (modo **Texto livre**) |
| Mostrar **Ao vivo** durante o evento | Campo **Duração (minutos)** do evento |
| Colocar na barra lateral | Interruptor **Destaque** do evento |
| Permitir aviso no navegador | Interruptor **Notificável** do evento |
| Organizar em grupos | **Eventos → Categorias** |
| Ordenar eventos ou categorias | Arrastar as linhas nas listas |
| Ajustar o fuso horário | **Configurações → Eventos**, campo **Fuso horário** |
| Ver os números | Botão **Estatísticas** no topo da lista de eventos |

---

## Dicas e boas práticas

- Confirme o **Fuso horário** logo no começo. Horários errados são quase sempre fuso errado.
- Use **categorias** para separar tipos de evento: fica muito mais fácil para o jogador encontrar.
- Dê uma **categoria** a todo evento, para ele aparecer na aba certa da agenda.
- Marque como **Destaque** só os eventos mais importantes, para a barra lateral não ficar poluída.
- Reserve **Notificável** para eventos que valem o aviso, assim o jogador não desliga por excesso.
- Para eventos diários, use **Todos os dias**; para eventos sem hora fixa, use **Texto livre**.
- Preencha a **Duração (minutos)** nos eventos de invasão e boss: o **Ao vivo** convida o jogador a entrar na hora.

---

## Perguntas frequentes

**Onde a agenda aparece para o jogador?**
Na página de Eventos do site e, para os eventos marcados como **Destaque**, também no bloco da barra lateral.

**Como o jogador recebe os avisos?**
Nos eventos **Notificáveis**, ele liga um interruptor de aviso e o navegador o notifica 5 minutos antes do início. É opcional, por evento, e depende de o jogador permitir notificações no navegador.

**Posso ter um evento em dias e horários diferentes?**
Sim. Escolha a recorrência **Por dia da semana** e crie uma linha para cada dia, cada uma com seus horários. Cada evento tem uma única recorrência.

**Como cadastro um evento que não tem hora fixa?**
Use a recorrência **Texto livre** e escreva no campo **Texto exibido** o que o jogador deve ler (ex.: *Sábado 20h*). Nesse modo não há contagem regressiva nem aviso.

**Os horários aparecem errados para alguns jogadores. O que fazer?**
Verifique o **Fuso horário** em **Configurações → Eventos**: ele deve corresponder ao horário do seu servidor.

**Como o site mostra que um evento está acontecendo agora?**
Preencha a **Duração (minutos)** do evento. Do início até o fim dessa janela, o site exibe **Ao vivo** com o tempo restante. Sem duração, esse destaque não aparece.

**Qual a diferença entre Destaque e Notificável?**
**Destaque** coloca o evento no bloco da barra lateral. **Notificável** permite que o jogador peça o aviso no navegador. São independentes.

**Posso traduzir o nome do evento?**
Não. O nome do evento é um texto único. Só o nome da categoria aceita vários idiomas.
