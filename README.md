# Desafio Invite App para Hackaton em parceria com a Laboratória

## Visão do Produto
Possuir a habilidade de se comunicar com eficácia e eficiência é fundamental para garantir que o conhecimento se dissemine numa organização. No entanto, o grande volume de informações geradas e compartilhadas nos meios “tradicionais” (e-mail, por exemplo) não tem atingido o objetivo esperado. Diversos são os “recados importantes” que passam batidos.
A expectativa com o desenvolvimento e aplicação do InviteApp é criar um canal de informação corporativa baseada numa rede peer-to-peer (P2P) e com aspectos de gamificação.
Exemplo: Evento interessante
1) Ao caminhar pela universidade, João, que é um colaborador da Avanade, viu um cartaz anunciando um evento sobre Blockchain que aconteceria em uma semana.
2) Ele achou superinteressante e gostaria de compartilhar aquela informação com alguns colegas de trabalho que ele julga que poderiam se interessar.
3) Ele abre o InviteApp e cria um Invite com foto e mais informações sobre o evento. Seleciona alguns colegas de trabalho e envia o Invite.
4) Logo em seguida, os colegas recebem a notificação em seus smartphones. Um deles, a Joana, ao ler a notificação, fica curiosa e imediatamente abre o App para ler as informações recebidas.
5) Joana acredita que outros colegas de trabalho também poderiam estar interessados no evento, e compartilha com eles a publicação.
6) Ao compartilhar, o João, que originalmente enviou a publicação, recebe alguns pontos, reconhecendo o seu valor. À medida que aquela publicação se espalha na rede, mais pontos o João receberá.

## Product Backlog

### 1. Controle de Acesso
- Logar

Como um colaborador, eu gostaria de me logar na aplicação usando minha conta corporativa. Desta forma,
espero ter acesso às demais funcionalidades do App.
- Deslogar

Como um colaborador, por questões de segurança, eu gostaria de me deslogar da aplicação, evitando que
outras pessoas tenham acesso às minhas informações ou para permitir que outro usuário possa se logar.

### 2. Gerenciar Invites
- Criar Invite

Como usuário, eu desejo criar um convite para que eu possa enviá-lo para colegas informando-os sobre “coisas” que
podem ser interessantes.
Critérios de Aceitação
• Todos os usuários poderão criar invites, não havendo restrição quanto ao número de invites criados.
• Invites deverão possuir:
o Título – linha única de texto até 80 caracteres;
o Descrição – múltiplas linhas de texto não-formatado até 500 caracteres;
o Imagem – upload de imagem (jpg ou png de até 4 MB) realizado pelo usuário;
o Quem criou – identificador do AD referente ao usuário;
o Quando foi criado – data preenchida automaticamente no ato da criação.
o Quando foi atualizado – ao criar, a data de última atualização deverá ser a data de criação.
• Com exceção da imagem, todos as demais informações são obrigatórias.
Listar Invites criados
Como usuário, eu desejo listar os invites que eu mesmo criei para poder tomar alguma ação sobre eles (enviar, editar
ou arquivar).
Critérios de Aceitação
• Invites deverão estar ordenados pela data de criação;
• Deverão ser exibidos nessa lista apenas os invites que o usuário logado criou;
Editar Invite
Como usuário, eu desejo editar um Invite que eu mesmo criei, podendo corrigir alguma informação anteriormente
passada.
Critérios de Aceitação
• Apenas poderão ser editados invites que o próprio usuário logado criou;
• Ao editar Invites que o usuário já tenha encaminhado, os usuários que os receberam também terão acesso às
novas informações (ver Detalhes do Invite);
• Ao editar um Invite, a data de última atualização deverão ficar registrada.
Listar Invites recebidos
Como usuário, eu desejo listar os invites que eu recebi de outros colegas a fim de obter maiores informações a respeito
dos mesmos (ver Enviar Invite e Encaminhar Invite para maiores informações).
Critérios de Aceitação
• Invites deverão estar ordenados pela data de recebimento;
• Os detalhes dos invites recebidos deverão estar acessíveis;
• Deverão ser exibidos apenas os invites que o usuário recebeu.
Detalhes do Invite
Como usuário, eu desejo visualizar os dados de um invite que eu recebi para obter mais detalhes a respeito do mesmo.
Critérios de Aceitação
• Os detalhes deverão ser exibidos “somente-leitura”, ou seja, desabilitados para edição.
• Deverão ser exibidos para o usuário:
o Título;
o Descrição;
o Imagem/ilustração;
o Quem criou;
o Quando foi criado;
o Quando foi atualizado (última atualização).
• Uma vez que o invite tenha sido aberto pelo pelo usuário, o mesmo deverá ser marcado como “lido” para
aquele usuário. Outros usuários que também receberam esse invite não deverão ser afetados, permanecendo
com o status de “não-lido”.
Arquivar Invite
Como usuário, eu desejo arquivar um invite recebido a fim de que ele não apareça mais na minha lista de Invites
Recebidos.
Critérios de Aceitação
• Apenas invites recebidos poderão ser arquivados nesse momento;
• Por ora, não existirá funcionalidade para “desarquivar” ou “reverter” a operação, portanto, a aplicação deverá
solicitar a confirmação do usuário antes de proceder com o arquivamento.

### 3. Compartilhar Invites
- Enviar Invite criado para colega

Como usuário que criou um convite, eu desejo enviá-lo para um colega para que ele tome conhecimento e possa tirar
proveito daquela informação.
Critério de Aceitação
• Um invite só poderá ser enviado para até 5 colegas;
• Apenas colegas ativos no AD da empresa deverão estar disponíveis;
• Usuários que receberem o Invite deverão ser notificados no App.
Encaminhar Invite recebido para colega
Como usuário que recebeu um invite, eu desejo encaminha-lo para outros colegas que também podem estar
interessados no conteúdo compartilhado, colaborando com a disseminação de um conhecimento relevante.
Critérios de Aceitação
• Todo invite recebido é passível de ser encaminhado;
• Apenas pessoas que não receberam o invite devem estar disponíveis para encaminhamento;
• O colaborador que recebeu o invite, só poderá ser encaminha-lo para até 5 outros colegas;
• Ao encaminhar o invite, todas as pessoas na sequencia anterior de compartilhamento deverão ser notificadas.
Mostrar total de compartilhamentos
Como usuário que criou o invite, eu desejo ver o número de usuários que o receberam. Desta forma, posso avaliar o
alcance do conteúdo compartilhado.
Critérios de Aceitação
• Na lista de invites criados, deverá ser exibido a quantidade de colaboradores que receberam o invite. Isto é,
não apenas para quem o usuário compartilhou diretamente, mas também para quem recebeu os sucessivos
encaminhamentos seguintes.
Agradecer Invite recebido
Como usuário que recebeu o invite, eu desejo agradecer a quem o enviou porque, por exemplo, aquele conteúdo era
de fato bastante relevante pra mim.
Critério de Aceitação
• Na lista de invites recebidos, deverá ser possível agradecer ao colega que enviou o invite;
• Ao agradecer, o usuário que enviou o invite deverá receber uma notificação.

### 4. Reconhecer Colaboradores
- Ganhar pontos pelo compartilhamento de Invite

Como usuário, eu desejo receber pontos toda vez que alguém encaminhar um invite que eu mandei. Mesmo que eu
não tenha criado o Invite originalmente, eu também gostaria de ser reconhecido por aquela cadeia de
compartilhamentos.
Critérios de Aceitação
• O usuário que criou o invite receberá 10 pontos para cada encaminhamento;
• O usuário que encaminhou receberá 10-2x pontos, onde X é o número de camadas na cadeia de
compartilhamento, para cada encaminhamento seguinte. Para X > 4, deverão ser concedidos apenas 1 ponto.
Figura 3 - Modelo de Pontuação: Exemplo
Exibir Leaderboard
Como usuário, eu desejo saber qual é a minha posição no ranking assim como ver quem são os primeiros colocados,
isto é, quem mais ganhou pontos de compartilhamento. Desta forma, conseguirei identificar os colaboradores mais
ativos na rede.
Critérios de Aceitação
• Serão exibidos todos os usuários que tiverem pontuação maior que 10;
• Como o volume de usuário tende a ser grande, a tela deverá ser paginada ou carregada sob demanda;
• Primeiro, os usuários com mais pontos, e assim sucessivamente;
• Independentemente da posição do usuário logado no ranking, a quantidade de pontos conquistados e sua
posição no ranking deverão exibidos na tela.
