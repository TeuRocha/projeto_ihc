# Coleta de Dados

## Que dados coletar?
- Dados demográficos: idade, sexo, status socioeconômico;
- Educação e Conhecimento na Área: nível de escolaridade, proficiência na calibração;
- Idiomas e jargões: idiomas falados, familiaridade com vocabulário técnico do tiro esportivo.

## De quem coletar?
Todos que desejam se aprofundar nas minucias do tiro esportivo (calibração de lunetas). Focado principalmente nos CACs (Caçadores, atiradores e colecionadores), policial civil e militar, entusiastas do esporte.

## Aspectos Éticos
O projeto deve considerar aspectos éticos pois envolve a coleta de dados para identificação de necessidades (via questionários) e a realização de testes práticos com equipamentos que oferecem risco físico (armas de fogo e de pressão). A aplicação dos princípios da Resolução 196/96 justifica-se da seguinte forma:
- Autonomia: É indispensável devido ao uso de questionários para entender o perfil socioeconômico e a experiência tecnológica dos atiradores. Os participantes devem ter a liberdade de decidir participar ou retirar seus dados a qualquer momento, garantida pelo consentimento livre e esclarecido.
- Não Maleficência: Este princípio justifica-se pela natureza dos testes práticos com armas. O projeto deve garantir a mitigação total de danos aos envolvidos através do uso de ambientes totalmente controlados (estandes de tiro) e equipamentos de segurança, evitando riscos imediatos ou tardios.
- Beneficência: A justificativa reside no equilíbrio entre o risco da coleta de dados e o ganho tecnológico. O sistema visa reduzir o desperdício de munição (insumo caro) e o tempo de pista, oferecendo um feedback automático que beneficia diretamente o aprendizado do praticante nacional.
- Justiça e Equidade: O projeto justifica-se eticamente ao focar em soluções de baixo custo e acessíveis à realidade econômica brasileira. Ao democratizar o acesso à tecnologia que antes era restrita à elite ou a produtos importados caros, o trabalho cumpre sua função de relevância social e equidade tecnológica.
- Privacidade e Confidencialidade: Como o sistema utiliza um banco de dados (SQLite) para gerenciar perfis de usuários, credenciais e configurações de preferência, o projeto deve assegurar que essas informações sensíveis sejam protegidas e que o anonimato seja mantido em qualquer divulgação de resultados estatísticos.

## Ferramentas de Coleta de Dados
**Instrumento:** Questionário digital para identificar necessidades (via Google Forms).

**Objetivo:** Obter dados em escala sobre o perfil demográfico dos, atiradores, sua relação com tecnologias de auxílio balístico, conhecimento do domínio (calibragem de miras) e motivações para o uso de uma solução nacional de baixo custo.

**Protocolo de execução:** Todos os aplicadores devem utilizar o mesmo texto de introdução ao enviar o link, explicando brevemente que se trata de uma pesquisa acadêmica da FEI sobre tiro esportivo. O instrumento deve ser enviado exclusivamente para praticantes de tiro (esportivo, caça ou lazer) para evitar dados ruidosos. Deve ser informado que a participação é voluntária e anônima antes do usuário abrir o link. A distribuição do link será via grupos de atiradores e fóruns especializados para mantes o foco no domínio do produto.

## Sobre a Coleta de Dados com Questionário

Para garantir o alinhamento com a Engenharia de Usabilidade, a coleta de dados foi dividida em duas fases metodológicas distintas: Levantamento de Necessidades (aplicado ao público-alvo para guiar o design inicial) e Avaliação de Uso (aplicado aos testadores após a interação com o protótipo do sistema).

### Levantamento de Necessidades e Perfil de Usuário
Este questionário tem como objetivo mapear o perfil, a experiência e as dores dos atiradores no processo manual atual, subsidiando as decisões arquiteturais e visuais da interface.

Grupo A: Perfil Demográfico e Socioeconômico
- Perguntas do formulário: Idade, Gênero, Escolaridade, Renda salarial.
- Decisão de Design que este dado responde:
  - Acessibilidade e Layout: A faixa etária predominante (ex: acima de 50 anos) dita o tamanho das fontes, os níveis de contraste (Dark Mode) e o tamanho das áreas de clique para compensar limitações visuais e motoras.
  - Modelo de Negócios: A renda baliza como monetizar o sistema, seja via assinatura, taxa única, gratuito com propagandas.

Grupo B: Conhecimento do Domínio (Vocabulário)
- Perguntas do formulário: Idiomas falados; Familiaridade com jargões (MOA, MIL, Zeroing, FFP/SFP); Nível de conhecimento do processo; Proficiência nas etapas da calibração (Leitura de retículo, holdunder, etc).
- Decisão de Design que este dado responde:
  - Linguagem do Sistema (Microcopy): Define se a interface utilizará termos técnicos crus (ex: "Ajuste 0.5 MIL") ou se precisará traduzir a informação para uma linguagem leiga baseada em ação (ex: "Gire a torre 5 cliques para a Direita").

Grupo C: Experiência Tecnológica
- Perguntas do formulário: Uso prévio de ferramentas balísticas digitais; Relato de pontos positivos/negativos de outras tecnologias; Dispositivos que possui no estande (Computador, Celular, Tablet); Avaliação geral no uso de PCs/Smartphones.
- Decisão de Design que este dado responde:
  - Plataforma e Responsividade: A escolha dos dispositivos dita se a interface deve ser Mobile First (focada em toques e arrastes em telas pequenas) ou se pode usar atalhos de teclado de notebooks.

Grupo D: Contexto da Tarefa, Dores e Motivações
- Perguntas do formulário: Frequência de prática; Média de munições gastas; Objetivo principal com a assistência; Gravidade típica dos erros; Tempo levado no processo manual; Tarefas mais desafiadoras (cálculos, fatores ambientais); Importância da economia vs precisão; Desejo por tutoriais.
- Decisão de Design que este dado responde:
  - Priorização de Funcionalidades (Core Features): Se "Cálculos de correção" e "Tempo" forem as maiores dores, o sistema deve exigir o mínimo de cliques (inputs) para gerar o resultado.
  - Sistema de Ajuda (H10 de Nielsen): O grau de interesse em tutoriais define se a aplicação terá um sistema de Onboarding (telas de explicação no primeiro acesso) obrigatório ou opcional, e se haverá ícones de ajuda contextual ("?") ao lado de cada campo de entrada.
 
### Avaliação de Uso e Satisfação
(Nota metodológica: Os dados a seguir são coletados exclusivamente após o usuário testar o sistema proposto, visando mensurar a eficácia da interface construída frente às necessidades mapeadas no Levantamento de Necessidades e Perfil de Usuário)
- Taxa de Sucesso e Tempo: Medição de quanto tempo o usuário levou para configurar a distância no sistema comparado ao tempo relatado no questionário de perfil.
- System Usability Scale (SUS): Aplicação de afirmações em escala Likert (Discordo Totalmente a Concordo Totalmente) para avaliar a carga cognitiva. Exemplos:
  1. Achei o sistema desnecessariamente complexo.
  2. Achei o sistema fácil de usar.
  3. Achei que as instruções visuais (cliques/setas) substituíram a necessidade de cálculos mentais.
- Decisão de Design que este dado responde: Identificar gargalos remanescentes no fluxo (ex: necessidade de incluir um botão "Voltar") e validar se a meta quantitativa de usabilidade (redução do tempo de calibração) foi atingida.

_________
**Link de acesso:** [Questionário](https://docs.google.com/forms/d/e/1FAIpQLSdTzKR5pnkemryP6aMUYcu8cplQR8We-0h1Hy6UY7gMNr6BaQ/viewform?usp=dialog)

# Questionário:

## Título: Projeto para Auxiliar a Calibração de Lunetas para Fins Esportivos

Coleta de dados para auxiliar no desenvolvimento do projeto, que promete auxiliar na calibração de lunetas, apenas para fins esportivos, visando economia de munição e tempo.

'*' indica uma pergunta obrigatória.

E-mail (Campo de texto aberto)*  
*Seu e-mail*

Informe o nome do usuário (Campo de texto aberto)*  
*Sua resposta*

Qual a sua idade? (Múltipla escolha - Selecione apenas uma)*  
( ) Abaixo de 18  
( ) 18 - 30  
( ) 31 - 40  
( ) 41 - 50  
( ) Acima de 51

Qual o seu gênero? (Múltipla escolha - Selecione apenas uma)\
( ) Masculino\
( ) Feminino\
( ) Prefiro não dizer

Qual o seu nível mais alto de escolaridade completo? (Lista suspensa - Selecione apenas uma)\
( ) Ensino Fundamental Incompleto\
( ) Ensino Fundamental Completo\
( ) Ensino Médio Incompleto\
( ) Ensino Médio Completo\
( ) Ensino Superior Incompleto\
( ) Ensino Superior Completo\
( ) Pós-Graduação (Especialização, Mestrado ou Doutorado)

Quais idiomas você fala além do Português (se houver)? (Caixas de seleção - Selecione múltiplas)\
[ ] Inglês\
[ ] Espanhol\
[ ] Nenhum\
[ ] Outro: __________

Quais destes jargões ou termos técnicos do tiro esportivo você está familiarizado? (Caixas de seleção - Selecione múltiplas)*\
[ ] MOA (Minute of Angle)\
[ ] MIL (Milirradianos)\
[ ] Zeroing (Zeragem)\
[ ] Trajetória Balística\
[ ] Ajuste de Torre/Clicks\
[ ] Paralaxe\
[ ] Primeiro Plano Focal (FFP)\
[ ] Segundo Plano Focal (SFP)\
[ ] Nenhum

Selecione a opção que se enquadra melhor com sua renda salarial atual: (Múltipla escolha - Selecione apenas uma)\
( ) Abaixo de um salário mínimo\
( ) Um salário mínimo\
( ) Entre 1.519 e 3.000\
( ) Entre 3.001 e 5.000\
( ) Entre 5.001 e 8.000\
( ) Entre 8.001 e 12.000\
( ) Acima de 12.000\
( ) Prefiro não informar

Você já utilizou algum software, aplicativo ou ferramenta digital especificamente para auxiliar em cálculos balísticos ou na calibração de miras? (Múltipla escolha - Selecione apenas uma)\
( ) Sim, utilizo frequentemente\
( ) Sim, utilizei poucas vezes\
( ) Não, mas desejo acesso\
( ) Não, nunca utilizei\
( ) Não sabia que existia

Quais dispositivos ou ferramentas você possui e utiliza rotineiramente para auxiliar na calibração do seu equipamento? (Caixas de seleção - Selecione múltiplas)\
[ ] Computador/Notebook\
[ ] Celular\
[ ] Tablet\
[ ] Calculadora balística\
[ ] Binóculos\
[ ] Nenhum desses

Avalie sua experiência geral no uso de computadores e smartphones para tarefas complexas: (Escala linear - Selecione apenas uma)\
Muito Limitada\
( ) 1\
( ) 2\
( ) 3\
( ) 4\
( ) 5\
Muito Avançada

Caso tenha utilizado algum software, aplicativo ou ferramenta digital para auxiliar em cálculos balísticos ou na calibração de lunetas, descreva um pouco sobre a tecnologia utilizada (pontos positivos e negativos). (Campo de texto aberto)\
*Sua resposta*

Com que frequência você pratica tiro esportivo (utilizando lunetas)? (Múltipla escolha - Selecione apenas uma)\
( ) Diariamente\
( ) Semanalmente\
( ) Mensalmente\
( ) Raramente (Menos de uma vez por mês)\
( ) Não pratico, desejo começar

Qual o seu nível de conhecimento sobre o processo de calibração de lunetas? (Lista suspensa - Selecione apenas uma)\
( ) Básico (Sei apenas o essencial)\
( ) Intermediário (Consigo calibrar, mas com dificuldade ou incerteza)\
( ) Avançado (Calibro com precisão e compreendo os princípios)\
( ) Especialista (Consigo ensinar o processo a outros)

Em média, quantas munições você gasta para 'zerar' ou recalibrar uma luneta em um novo equipamento/distância? (Campo de texto aberto)\
*Sua resposta*

Avalie sua proficiência nos seguintes aspectos da calibração: (Grade de múltipla escolha com escala linear - Selecione apenas uma por linha)\
Entre 1 (Baixa Proficiência) à 5 (Alta Proficiência)\
( ) Determinação da Distância Alvo Correta\
( ) Leitura do Retículo (Crosshair)\
( ) Ajuste de Vertical e Horizontal (Elevation/Windage)\
( ) Compensação de Queda (Goldover/Holdunder)

Qual é o seu principal objetivo ao utilizar um sistema de assistência à calibração? (Múltipla escolha - Selecione apenas uma)\
( ) Reduzir o tempo gasto com calibração\
( ) Reduzir a quantidade de munição desperdiçada\
( ) Aumentar a precisão e consistência dos disparos\
( ) Aprender a calibrar de forma mais eficaz\
( ) Outro

Em sua atividade de tiro esportivo, qual é a gravidade típica dos erros cometidos durante a calibração? (Escala linear - Selecione apenas uma)\
Erro Mínimo (Apenas ajusto)\
( ) 1\
( ) 2\
( ) 3\
( ) 4\
( ) 5\
Erro Crítico (Perda de tempo e dinheiro significativo)

Quanto tempo você leva, em média, para realizar o processo completo de calibração em campo (do início ao fim)? (Campo numérico aberto - Horário)\
*Duração em horas*

Quais são as tarefas que você considera mais desafiadoras durante o processo de calibração? (Caixas de seleção - Selecione múltiplas)\
[ ] Cálculos de correção balística\
[ ] Determinar o 'zero' ideal para diferentes distâncias\
[ ] Ajustar as torres com precisão\
[ ] Gerenciar fatores ambientais (vento, temperatura)\
[ ] Verificação da precisão após o ajuste\
[ ] Nenhuma dificuldade significativa

Classifique a importância dos seguintes fatores para você na prática do tiro esportivo: (Grade de múltipla escolha com escala linear - Selecione apenas uma por linha)\
Entre 1 (Não Importante) - 3 (Neutro) - 5 (Extremamente Importante)\
( ) Precisão Máxima\
( ) Otimização de Tempo\
( ) Economia de Recursos (Munição)\
( ) Aprendizagem e Conhecimento Técnico\
( ) Participação em Competições

Faria uso de uma tecnologia nova para auxiliar na calibração de lunetas, mesmo já tendo conhecimento e aprendizado sobre outra ferramenta? (Múltipla escolha - Selecione apenas uma)\
( ) Sim\
( ) Não

Qual o seu grau de interesse em utilizar um sistema que forneça treinamento/tutoriais interativos sobre calibração de lunetas? (Classificação - Selecione apenas uma)\
( ) 1\
( ) 2\
( ) 3\
( ) 4\
( ) 5

Em um texto curto, descreva o que o sucesso na calibração de lunetas representa para você. (Campo de texto aberto)\
*Sua resposta*
