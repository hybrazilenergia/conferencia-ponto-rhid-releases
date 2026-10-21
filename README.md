# Conferência de Ponto — Guia de instalação e uso

## Instalar
1. Abra https://github.com/hybrazilenergia/conferencia-ponto-rhid-releases/releases/latest
2. Clique em **Conferencia-de-Ponto-Setup-…exe** para baixar.
3. Abra o arquivo baixado. O Windows pode mostrar a tela azul **"O Windows protegeu o computador"**.
   Isso acontece porque o programa é interno da empresa. Clique em **Mais informações** e depois em **Executar assim mesmo**.
4. A instalação é automática. No fim, o programa abre sozinho e aparece o atalho **Conferência de Ponto** na Área de Trabalho.

## Atualizações
O programa se atualiza sozinho. Toda vez que é aberto, ele verifica se há uma versão nova; se houver, baixa em segundo plano e avisa com uma notificação do Windows. A versão nova é instalada quando você **fecha** o programa e já vale na próxima vez que abrir. Não é preciso baixar nada de novo.
Se o computador estiver sem internet, o programa abre normalmente e tenta de novo na próxima vez.

## Primeiro acesso
Digite o **mesmo e-mail e senha do site do RHiD** e clique em **Entrar e testar conexão**.
Eles ficam guardados de forma protegida neste computador. Para trocar: **Configurações → Trocar login do RHiD**.

## Como andar pelo programa
- **Menu à esquerda**: **Conferir** (escolher período e funcionários), **Resultado** (a última conferência) e **Configurações**. O item da tela atual fica destacado.
- **Recolher menu** (no pé do menu) deixa só os ícones, para sobrar mais espaço; passe o mouse num ícone para ver o nome. **Expandir menu** volta ao normal. O programa lembra a escolha da próxima vez que abrir.
- Durante uma conferência (ou reconsulta) o menu fica travado: espere terminar ou clique em **Cancelar**.
- No alto de cada tela aparece o **caminho** até ela, por exemplo **Resultado › Funcionários › ANA**. Clique numa parte do caminho para voltar até lá.
- Ao sair do Resultado e voltar pelo menu, ele abre na mesma aba e com os mesmos filtros de antes.

## Conferir
Em **Origem dos dados**, escolha de onde vêm os cartões: **RHiD** (já vem marcado) ou **Arquivo PDF (sistema 2)** (veja [Conferir pelo PDF](#conferir-pelo-pdf-sistema-2)).

1. **Período**: já vem com o último fechamento (21 a 20). Use os botões **Último fechamento** ou **Fechamento atual** (até ontem), ou mude as datas. Só dá para conferir até ontem.
2. **Funcionários**: escolha a empresa, busque por nome ou matrícula e marque quem conferir (clicar em qualquer parte da linha também marca), ou clique em **Selecionar todos os … da lista**. A lista mostra 50 funcionários por vez: use **‹ Anterior** e **Próxima ›** (acima ou abaixo da lista) para ver os outros. **Selecionar todos os … da lista** marca todos os da lista, de todas as páginas, não só os que aparecem na tela.
3. O quadro **Resumo da seleção** mostra quantos estão marcados e quantos de cada empresa. **Limpar seleção** desmarca todos.
4. Clique em **Conferir … funcionários**, na barra do rodapé. Aparece o andamento ("Conferidos 12 de 50"). Para parar no meio, clique em **Cancelar**: aparece "Conferência cancelada." e você pode mudar a seleção e conferir de novo.
5. Se já existe um resultado que ainda não foi exportado, o programa pergunta antes de substituí-lo. Clique em **Iniciar nova conferência** para continuar ou em **Voltar** para guardar o resultado antes.

### Conferir pelo PDF (sistema 2)
O segundo sistema de ponto não tem ligação com o programa: ele exporta a **FOLHA DE PONTO** em PDF, com um cartão por página, e o programa confere esse arquivo.
1. Exporte a folha de ponto no sistema 2 e salve o PDF no computador (por exemplo, em Downloads).
2. Em **Conferir**, marque **Arquivo PDF (sistema 2)** em **Origem dos dados**.
3. No quadro **Arquivo**, clique em **Escolher arquivo PDF** e escolha o arquivo. O programa lê todos os cartões (leva alguns segundos) e mostra o nome do arquivo e um resumo, por exemplo **"12 cartões · 21/09 a 20/10/2026 · EMPRESA"**.
4. O período é o do arquivo e não muda aqui. Só dá para conferir até ontem.
5. Cada cartão só é usado se a leitura bater com os totais impressos no próprio cartão (horas trabalhadas, abonadas, extras, faltas e total) e se as batidas de cada dia baterem com as horas do dia. Cartão que não bate, ou página que não parece um cartão de ponto, aparece num aviso amarelo, com a página e o motivo; ele não é conferido e entra no Resultado como **não conferido**.
6. Marque os funcionários na lista (busca, empresa e **Selecionar todos** funcionam como no RHiD) e clique em **Conferir … funcionários**.
7. As marcações de abono e afastamento vistas no arquivo (por exemplo, **AFASTADO: ATESTADO**) passam a aparecer em **Configurações → Justificativas → PDF – sistema 2**, para você classificar.
8. Para conferir outro arquivo, clique em **Escolher outro arquivo**. Ao ir para outra tela e voltar, a origem e o arquivo continuam escolhidos.

O que muda no resultado de um PDF:
- No alto aparece **"Origem: PDF — nome-do-arquivo.pdf"** e **"Regras: PDF – sistema 2"**: as regras usadas são as da aba **PDF – sistema 2** em Configurações.
- Não existe **Reconsultar os que falharam**: o arquivo é o mesmo, então ler de novo não muda nada. Corrija no sistema 2, exporte de novo e confira o novo arquivo.
- No cartão do funcionário, as colunas dizem **Previsto (PDF)**, **Total (PDF)**, etc. Os totais (normais, extras) são os do PDF. As horas abonadas (**[ABN: …]**) não contam como trabalhadas.
- Conta só o que está no arquivo. A contagem de **6 dias seguidos** começa no primeiro dia do arquivo. A semana que começa antes ou termina depois do período é conferida com os dias que o arquivo traz ("Semana incompleta no arquivo"). No mês incompleto, um domingo de folga nos dias do arquivo basta; sem nenhum, fica **Pendente** ("Mês incompleto no arquivo … e sem domingo de folga nesses dias"), porque os outros domingos não estão no arquivo.
- Dia marcado como **FOLGA** no cartão, mas com batidas, é dia trabalhado: aparece como **Folga trabalhada**, não conta como domingo de folga e não zera a contagem de dias seguidos.
- Domingo com abono ou afastamento (por exemplo, **AFASTADO: FERIAS**) que ainda está em **Ainda não decidi** em **Configurações → Justificativas → PDF – sistema 2** não conta como domingo de folga. Se o mês depender dele, o domingo de folga fica **Pendente** ("Domingo 09/08 com "AFASTADO: FERIAS" ainda não classificada em Configurações"). Depois de classificar, valem as regras de sempre: em **Conta como ausência**, o domingo não é folga (e conta nos dias de ausência do mês); em **Não conta**, ele volta a contar como folga.

#### Sem o RHiD
Se o RHiD não carregar na abertura do programa (sem internet, RHiD fora do ar ou login que precisa ser atualizado), a tela de erro tem o botão **Conferir um PDF**. Ele abre **Conferir** só com a origem **Arquivo PDF (sistema 2)**: a opção **RHiD** fica desabilitada, com o aviso **"O RHiD não está disponível agora."**. O resto funciona como sempre: abrir o arquivo, conferir, ver o resultado, exportar e classificar as marcações do PDF em **Configurações** (as justificativas do RHiD não aparecem e ficam como estavam salvas). Para voltar a usar o RHiD, feche e abra o programa de novo.

Problemas ao abrir o PDF:
- **"O arquivo escolhido não é um PDF."**: escolha o arquivo .pdf exportado pelo sistema 2.
- **"Este PDF não parece ser uma folha de ponto do sistema 2."**: o arquivo é outro relatório. Exporte a **FOLHA DE PONTO**.
- **"O arquivo está aberto em outro programa."**: feche o PDF no leitor e tente de novo.
- **"Não foi possível ler este PDF…"**: o arquivo pode estar danificado ou protegido por senha. Exporte de novo.

## Resultado
O Resultado tem duas abas: **Visão geral** (abre primeiro) e **Funcionários (N)**. No alto ficam o período, a data em que foi gerado, quantos funcionários foram selecionados, o menu **Exportar ▾** e o botão **Nova conferência**.

### Visão geral
- **Números do período**: Conferidos, Com violação (e a % dos conferidos), Violações, Com pendência, Sem dias para conferir e Não conferidos. Clique num número para ver a lista desses funcionários (por exemplo, **Com violação** abre a aba Funcionários mostrando só quem tem violação).
- **Violações por regra**: uma barra por regra. Clique numa barra (por exemplo, **Almoço**) para ver só quem tem violação naquela regra.
- **Violações por semana**: quantas violações em cada semana do período (domingo de folga não entra, porque é contado por mês).
- **Empresas × regras**: quanto mais escura a cor, maior a parte dos funcionários da empresa com violação naquela regra. Passe o mouse para ver os números. Clique no nome da empresa para ver todos dela, numa célula para ver quem tem violação naquela empresa e regra, ou no total para ver todos com violação daquela empresa.
- **Mais violações**: os funcionários com mais violações. Clique no nome para abrir o cartão dele.
- Cada quadro tem o botão **Como calculamos**, que explica de onde vêm os números.
- Se nenhum funcionário teve dias para conferir, os gráficos não aparecem: veja a situação de cada um na aba Funcionários.

### Funcionários
Cada coluna é uma regra: o número vermelho é a quantidade de violações, o amarelo a de pendências, e ✓ quer dizer OK. Para achar quem interessa, use os filtros acima da lista:
- **Mostrar**: começa em **Com violação, pendência ou aviso**. As outras opções são:
  - **Todos**: todo mundo.
  - **Com violação**, **Com pendência** ou **Com aviso**.
  - **Sem violação**: quem foi conferido e não teve nenhuma violação (pode ter pendência ou aviso).
  - **Tudo OK**: quem foi conferido e não teve violação, pendência nem aviso.
  - **Sem dias para conferir**.
  - **Sem violação** e **Tudo OK** nunca mostram quem não teve dias para conferir.
- **Empresa**: aparece quando o resultado tem funcionários de mais de uma empresa.
- **Regra**: deixa a lista olhar só para uma regra (por exemplo, **Almoço**). Junto com **Com violação** ou **Com pendência**, conta só os problemas daquela regra. Junto com **Sem violação**, mostra quem não tem violação naquela regra. Junto com **Tudo OK**, mostra quem teve aquela regra conferida e sem violação nem pendência (quem só tem "Não se aplica" nela fica de fora; os avisos não contam). **Ordenar → Mais problemas primeiro** também conta só os problemas daquela regra.
- **Buscar funcionário** (nome ou matrícula) e **Ordenar**.
- A lista mostra 50 funcionários por vez; use **‹ Anterior** e **Próxima ›** para passar de página. Ao mudar um filtro, a lista volta para a primeira página. Os filtros só mudam o que aparece na tela: as exportações continuam com o resultado completo.
- Se nenhum funcionário combinar com os filtros, aparece **"Nenhum funcionário encontrado com esses filtros."**

### Cartão do funcionário
1. Clique no nome do funcionário para ver o cartão dia a dia. No topo, um número por regra mostra quantas violações ou pendências ele teve (ou OK). Clique no número de uma regra do dia (Intervalo de 11h, Almoço, Extra diária, 6 dias seguidos) para a tabela mostrar só os dias com problema naquela regra; **44h semanais** e **Domingo de folga** levam às listas de semanas e meses (e, com o banco de horas ligado, **Banco de horas (fechamento)** leva à lista **Fechamento**).
2. **‹ Funcionário anterior** e **Próximo funcionário ›** passam para o funcionário vizinho da lista (mesmo que ele esteja em outra página). Para voltar à lista, clique em **Funcionários** no caminho do alto: ela volta na página desse funcionário e com os mesmos filtros.
3. Na tabela dos dias, **Mostrar dias → Só dias com problema** deixa só os dias com violação, pendência ou sem dados (do RHiD ou do PDF), e **Regra** deixa só os dias com problema naquela regra. A tabela mostra até 31 dias por vez (com os dias de referência marcados, pode passar disso: use **Próxima ›**). Ao trocar de funcionário, os filtros do cartão voltam ao normal. Quando o RHiD não informou as horas do dia, **Total**, **Normais** e **Extras** aparecem como **—** (no Excel, a célula fica vazia), e não como 0:00.
4. Clique em qualquer situação (✓ OK, Violação, Pendente) para ver **Como calculamos** e de onde veio cada dado.

### Situações especiais
- Se o período ainda não terminou, aparece **"Conferido até … (ontem)"** abaixo do título: os dias seguintes não entram no resultado, e a semana ou o mês que ainda não terminou aparece como **Pendente**.
- Funcionário sem nenhum dia de ponto para conferir no período (por exemplo, admitido depois) aparece com a explicação no lugar das regras, nunca como OK.
- Se algum funcionário não pôde ser conferido (por exemplo, a internet caiu, ou o cartão do PDF não bateu com os totais), ele aparece no quadro amarelo acima das abas, com o motivo. Na origem RHiD, clique em **Reconsultar os que falharam** — só esses são consultados de novo (enquanto isso, o menu fica travado). Se o RHiD recusar o login na reconsulta, clique em **Trocar login** na mensagem. Quem falhou por falta de acesso no RHiD não entra na reconsulta: peça a liberação ao administrador do RHiD.

## Exportar
- No Resultado, clique em **Exportar ▾** e escolha:
  - **PDF completo**: começa com a visão geral (números, gráficos, empresas e quem mais teve violações) e depois traz o cartão de cada funcionário.
  - **Excel completo**: a primeira aba, **Visão geral**, tem os mesmos números da tela e, no fim, as **Regras usadas** (o conjunto e os valores de cada regra); depois vêm **Resumo**, **Violações e pendências** e **Dias**.
  - **Excel só com problema**: só quem tem violação, pendência ou aviso (e quem não pôde ser conferido).
- No cartão de um funcionário, **Exportar este funcionário (PDF)** salva só o cartão dele.
- Depois de salvar, o arquivo abre sozinho e aparece **"Relatório salvo: nome-do-arquivo"** com o botão **Abrir pasta**, que mostra onde o arquivo ficou.
- Ao fechar o programa com um resultado que ainda não foi exportado, ele avisa que o resultado será perdido: **Fechar mesmo assim** fecha; **Voltar** deixa o programa aberto para você exportar.

## Configurações
- **Login do RHiD**: **Trocar login do RHiD** pede o e-mail e a senha de novo.
- **Aparência**: **Claro** ou **Escuro**. Muda na hora e fica guardado neste computador.
- **Regras**: um conjunto de regras por origem dos cartões, nas abas **RHiD** e **PDF – sistema 2**. Para cada regra, a caixa **Conferir …** liga ou desliga a regra, e os campos abaixo dela mudam os valores (horas no formato HH:MM, por exemplo 44:00). **Conferir banco de horas (fechamento)** vem desligada: no RHiD, ligue só depois que o banco de horas estiver configurado lá; no PDF, só se a folha trouxer o banco de horas (colunas CRE. e DEB.). Até o RH definir as regras do sistema 2, o conjunto **PDF – sistema 2** começa com os mesmos valores do RHiD. **Voltar ao padrão** volta todas as regras do conjunto aos valores combinados com o RH (pede confirmação e só vale depois de salvar). As mudanças valem a partir da próxima conferência.
- **Justificativas**: uma seção por origem. Diga quais são férias, atestado ou afastamento. As do PDF aparecem depois que um PDF for aberto.
- Clique em **Salvar configurações** para guardar as regras e as justificativas.

## As regras conferidas
Os valores abaixo são os padrão. Quando algum valor foi mudado em **Configurações → Regras**, o alto do Resultado mostra **"Regras: RHiD (ajustadas)"**, e o Excel e o PDF trazem o bloco **Regras usadas** com os valores de cada regra.
- **Intervalo de 11h** entre o fim de um dia de trabalho e o início do próximo.
- **Almoço**: obrigatório quando o dia passa de 6h trabalhadas; duração exigida pela escala do dia (sábado sem intervalo previsto usa o intervalo normal do funcionário).
- **Domingo de folga**: pelo menos 1 por mês do calendário (domingo que é feriado e não foi trabalhado também conta; dispensado com 22 dias ou mais de afastamento no mês).
- **Extra diária**: no máximo 2h (domingo e feriado trabalhados podem ficar fora — ver Configurações).
- **44h por semana** (segunda a domingo), somando horas normais e o total trabalhado em domingos e feriados.
- **6 dias seguidos** no máximo sem folga.
- **Banco de horas (fechamento)** — opcional: só com **Conferir banco de horas (fechamento)** ligada em Configurações. O saldo do banco de horas do RHiD precisa estar zerado no último dia do período conferido (horas que sobraram ou faltaram são violação; sem o saldo do RHiD, fica pendente). Desligada, a regra não aparece em lugar nenhum. **Ligue a chave só depois que o banco de horas estiver configurado no RHiD**: antes disso o RHiD informa saldo 0 para todos, e o programa mostraria todo mundo como "zerado" (OK) sem que o banco esteja funcionando.
- Plantão que passa da meia-noite é conferido como um único dia, o do início; a batida da madrugada aparece com a data do dia seguinte.

## Situações
- **Violação**: a regra não foi cumprida. **Pendente**: falta informação (batida faltando ou mês/semana não terminou). **Não se aplica**: a regra não vale para aquele dia.
- Aviso **"Classifique a justificativa…"**: vá em **Configurações → Justificativas** e diga se ela é férias/atestado/afastamento.

## Problemas comuns
- **"E-mail ou senha do RHiD incorretos"** ou **"Seu login do RHiD precisa ser atualizado"**: a senha do RHiD pode ter mudado. Confira no site do RHiD e clique em **Trocar login**. Login inválido ou login não salvo interrompem a conferência inteira; qualquer outro problema afeta apenas o funcionário em questão.
- **"Não foi possível se comunicar com o RHiD"**: verifique a internet e se o site do RHiD abre no navegador, e tente de novo (na abertura do programa, clique em **Tentar de novo**). Enquanto isso, dá para conferir a folha do sistema 2 em **Conferir um PDF** (veja [Sem o RHiD](#sem-o-rhid)).
- **"O RHiD está fora do ar"**: tente mais tarde e use **Reconsultar os que falharam**.
- Problemas com o arquivo PDF do sistema 2: veja [Conferir pelo PDF](#conferir-pelo-pdf-sistema-2).
- **"Seu usuário do RHiD não tem acesso…"**: peça ao administrador do RHiD para liberar o acesso, ou entre com outro usuário (**Trocar login**).
- **Erro ao exportar**: se o arquivo estiver aberto no Excel ou no leitor de PDF, feche-o e exporte de novo; se a pasta não estiver disponível (por exemplo, uma unidade de rede desconectada), escolha outra pasta, como a Área de Trabalho.
- Se continuar, avise o suporte técnico.
