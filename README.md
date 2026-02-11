# projeto_ihc

## Membros da Equipe:
- Mateus Rocha

## Título Original do TCC:
Auxilio de Calibragem de Mira Inteligente para Fins Esportivos

## Orientador:
- Flávio Tonidandel

### Previsto desenvolver interface?
(x) Sim   ( ) Não

### Objetivo do Trabalho?
Calcular a calibração da luneta do usuário, e guiar ele para concluir sua calibragem.

### Qual o produto final?
Um sistema de interface simples para obter do usuário a informação da distância que ele deseja calibrar sua luneta, e retornar o feedback o mais preciso e rápido possível.

### Quem é o usuário final deste produto?
Os CACs (Colecionadores, atiradores e caçadores), policiais, pessoas com porte de arma, jogadores de airsoft com uso de lunetas, qualquer usuário dentro da lei que deseja calibrar sua luneta.

### O que o usuário recebe de benefício ao usar esse produto?
- Menos gasto de munição, consequentemente menos gasto financeiro;
- Não se faz necessário conhecimento técnico para calibração, o sistema resolve sozinho;
- Otimização do tempo do usuário, menos tempo para calibrar.

### Quais as funcionalidades da ferramenta (visão do usuário)?
- Sistema de cadastro e login do usuário;
- Tela para receber do usuário a distância desejada para calibrar;
- Tela de feedback.

### Quais tecnologias e ferramentas computacionais que pretendem usar neste projeto (TCC)?
- Código desenvolvido em Python 3.10;
- Bibliotecas:
  - OpenCV;
  - NumPy;
  - Marplotlib.
- Hardware de captura e transmissão: Redmi com protocolo RTSP/HTTP (App IP Webcam);
- Técnicas e Algoritmos:
  - Método de Zhang;
  - Matriz de homografia;
  - Subtração de Imagem e Operações Morfológicas.
- Interface e Deploy:
  - Streamlit ou Flask.

### Qual é o contexto de uso dessa aplicação?
- Usuários: Atiradores esportivos, caçadores e colecionadores (CACs), com foco especial em iniciantes que carecem do conhecimento de cálculos balísticos, ou entusiastas que desejam otimizar seu tempo e munição.
- Ambiente: Local controlado e autorizado para a prática de tiro, como estandes de tiro ou clubes especializados, que possuam iluminação adequada para garantir a nitidez da captura de imagem.
- Equipamentos e Configuração: O usuário utiliza um Smartphone posicionada com um tripé a curta distância do alvo (aproximadamente 2 metros), que transmite o sinal de vídeo via wi-fi para um notebook atrás da linha de tiro, o alvo deve conter marcador fiduciais (ArUco) para permitir a coreção de perspectiva e escala.
- Tarefa: O atirador realiza disparos em direção ao centro do alvo (POA), o sistema processa a imagem do impacto e fornece, em menos de 5 segundos, o feedback visual e numérico da correção necessária em "cliques" nas torres da luneta.
- Contexto Social/Econômico: Uma solução nacional de baixo custo voltada para tornar o esporte mais acessível no Brasil, reduzindo a dependência de tecnologias importadas de alto valor e simplificando um processo que tradicionalmente é feito por tentativa e erro.

# SEGUNDA ENTREGA - ANÁLISE DE CONCORRÊNCIA
Chairgun Elite, Lapua Ballistics e Ballistic-X.

Padrões encontrados:
- Definição da arma utilizada;
- Tabelas e gráficos como guia;
- Campos para preencher dados de equipamentos e ambiente;
- Sistema de login e cadastro;
- Possibilidade de alterar unidades de medidas;
- Páginas com tons mais escuros.

Possibilidade competitiva além das calculadoras balísticas, com miras a laser, possível incrementação da tecnologia no TCC.

## Prints de sistemas da concorrência

### Chairgun Elite:
![chair (2)](https://github.com/user-attachments/assets/c7c6ce22-de30-4812-83c5-e3de42062dc9)
![chair (3)](https://github.com/user-attachments/assets/5a76cdfe-39d4-473d-8e2f-3dfd4e4acac5)
![chair (4)](https://github.com/user-attachments/assets/14ba6cdc-e187-4f8e-9ea0-18cdc6cf8de7)
![chair (5)](https://github.com/user-attachments/assets/8c8579a2-3f53-4388-b7bb-39ee919a4a0e)

### Lapua Ballistics:
![lapua (4)](https://github.com/user-attachments/assets/a9b4c9ce-6978-4bf1-b07d-57f7ce22a643)
![lapua (1)](https://github.com/user-attachments/assets/49270e40-0d7b-4e91-8e05-772bc9b63814)
![lapua (2)](https://github.com/user-attachments/assets/2cffe576-ed78-42d8-a96e-c619923f6c52)
![lapua (3)](https://github.com/user-attachments/assets/80d0bf17-b43b-4679-a6f4-abc0d83f1cbc)

### Ballistic-X:
![balilistic (1)](https://github.com/user-attachments/assets/6eeafbb4-9ae9-475f-b575-d019285e5c6d)
![balilistic (2)](https://github.com/user-attachments/assets/5388ea3a-5f4c-4d57-9924-cafb20ddd10c)
![balilistic (3)](https://github.com/user-attachments/assets/be9c9942-9b00-4c40-a90b-76121ab6609c)

# Terceira entrega

## PERSONAS

### Márcio Rocha, policial civil
- Idade: 45 anos.
- Status: Primária.
- Objetivos: Aposentar quando os filhos forem auto suficiente, continuar com o Hobbie de atirar.
- Habilidades: Mestre de capoeira, atirador de elite.
- Tarefas: Escolta de presos, operações especiais, ronda em todo estado de São Paulo, frequência dia sim, dia não.
- Relacionamentos: Divorciado, com dois filhos.
- Requisitos: Sistema que entregue um feedback exato com o menor número de uso.
- Expectativas: Um sistema com gráficos informativos para buscar uma melhora no desempenho.

#### Mapa de Empatia: Márcio Rocha
- O que PENSA e SENTE?
Quais as suas preocupações?
Márcio se preocupa em manter sua precisão técnica como atirador de elite mesmo com o passar dos anos, visando uma transição tranquila para a aposentadoria sem perder sua identidade como atirador.

- O que OUVE?
Quais pessoas e ideias o influenciam?
Ouve conselhos de colegas de operações especiais sobre novas tecnologias de balística e o feedback de seus alunos de capoeira sobre disciplina e foco.

- O que VÊ?
O que é mais comum no seu cotidiano?
A rotina de plantões "dia sim, dia não", o manuseio constante de equipamentos de precisão e a busca por eficiência máxima em cada ação.

- O que FALA e FAZ?
Quais seus hobbies?
Praticar e ensinar capoeira e frequentar clubes de tiro para manter sua habilidade como atirador de elite.

- Quais são as DORES?
Quais obstáculos precisa ultrapassar?
A dificuldade de conciliar o tempo com os filhos após o divórcio com a carga horária exaustiva das rondas estaduais.

- Quais são as NECESSIDADES?
O que é sucesso para sua persona?
Conseguir um feedback de calibração perfeito e preciso logo no primeiro disparo, garantindo que seu equipamento esteja sempre pronto para uso.

#### Contexto de Uso: Márcio Rocha
- Ambiente Físico e Social: Márcio utiliza o sistema em clubes de tiro profissionais ou estandes militares em São Paulo. O ambiente é barulhento, com outros atiradores ao lado, exigindo que ele mantenha o foco total na linha de tiro. A iluminação é controlada, permitindo que a câmera do smartphone capture nitidamente o alvo com os marcadores ArUco.

- Interação e Equipamento: Como ele prefere eficiência máxima e "comandos" diretos, ele monta o tripé a 2 metros do alvo e posiciona o notebook. Para ele, o sistema não é um brinquedo, mas uma ferramenta de precisão que deve economizar sua munição de alto custo e seu tempo escasso entre plantões.

- Narrativa de Uso: Imagine Márcio chegando ao estande após uma ronda cansativa. Ele não quer fazer cálculos manuais. Ele realiza um único disparo de aferição. Em menos de 5 segundos, ele olha para o notebook posicionado atrás dele e vê o feedback numérico exato: "Subir 4 cliques". Ele ajusta a luneta e segue para seu treinamento de precisão com a confiança de que o equipamento está zerado.

#### Jornada do Usuário: Márcio Rocha
Um dia de ronda em São Paulo e o cuidado com o equipamento próprio.
Durante uma pausa em sua ronda pela Rodovia dos Imigrantes, Márcio olha para o case de seu fuzil de precisão no banco traseiro da viatura. Ele nota que a luneta pode ter sofrido vibrações excessivas com o movimento do carro e decide: "Assim que encerrar o plantão, vou ao estande zerar esse equipamento".
Ao final do serviço, ele se dirige ao clube de tiro. Ainda fardado, mas sem o peso da responsabilidade operacional, ele sente o alívio de estar em um ambiente controlado.
Márcio monta o sistema rapidamente. Ele não quer perder tempo. Realiza o disparo, olha o feedback no notebook, faz os 4 cliques indicados e confirma a precisão. O sistema entregou o que ele precisava: confiança no primeiro disparo.
De volta em casa, Márcio limpa seu armamento. Ele guarda o fuzil no cofre, sentindo-se pronto para o próximo chamado, sabendo que o equipamento está cirúrgico.

### Alessandra Pinheiro, policial aposentada
- Idade: 60 anos.
- Status: Primária
- Objetivos: Curtir a aposentadoria, manter a segurança pessoal dentro e fora de casa.
- Habilidades: Investigadora policial, com certa experiência em negócios.
- Tarefas: Cuidado com a casa, acompanhamento médico contínuo.
- Relacionamentos: Viúva, com duas filhas do primeiro casamento.
- Requisitos: Sistema de manuseio simples, sem muito esforço físico por parte do usuário.
- Expectativas: Um sistema de uso simples e direto ao ponto, com tutoriais mais visuais.

#### Mapa de Empatia: Alessandra Pinheiro
- O que PENSA e SENTE?
Como a persona se sente e, relação ao mundo?
Sente que, apesar da experiência como investigadora, a idade e a necessidade de acompanhamento médico contínuo a tornam um pouco mais vulnerável, o que reforça seu desejo por proteção.

- O que OUVE?
Quais produtos de comunicação consome?
Consome notícias sobre segurança pública e saúde, preferindo conteúdos que utilizem tutoriais visuais e linguagem clara.

- O que VÊ?
Como é o mundo em que a persona vive?
Um ambiente doméstico tranquilo, mas onde ela está sempre atenta a detalhes de segurança, aplicando seu olhar treinado de ex-investigadora.

- O que FALA e FAZ?
Sobre o que sua persona costuma falar?
Conversa frequentemente sobre estratégias de segurança pessoal e compartilha experiências de sua carreira na polícia e no mundo dos negócios.

- Quais são as DORES?
Do que sua persona tem medo?
Tem receio de sofrer algum incidente de segurança por falta de monitoramento eficiente ou por não conseguir manusear sistemas tecnológicos complicados em momentos de urgência.

- Quais são as NECESSIDADES?
O que acabaria com seus problemas?
Um sistema de segurança intuitivo, com comandos simples e guias visuais, que garanta sua proteção sem demandar esforço físico ou aprendizado técnico exaustivo.

#### Contexto de Uso: Alessandra Pinheiro
Ambiente Físico e Social: Alessandra frequenta o estande em horários mais calmos, buscando um ambiente seguro e bem iluminado. Por ter 60 anos e precisar de acompanhamento médico, ela evita carregar pesos excessivos ou fazer deslocamentos desnecessários entre a linha de tiro e o alvo.

Interação e Equipamento: O foco dela é a simplicidade de manuseio. Ela utiliza o smartphone e o notebook para evitar o esforço físico de caminhar até o alvo para verificar o impacto. A transmissão via Wi-Fi é essencial para que ela possa ver tudo sentada ou em uma postura confortável, sem forçar as articulações.

Narrativa de Uso: Imagine Alessandra no estande. Ela segue o tutorial visual do sistema para posicionar o smartphone. Após o disparo, em vez de tentar decifrar fórmulas balísticas complexas, ela vê na tela do notebook uma imagem clara do seu impacto e uma instrução visual simples (setas e números de cliques). O sistema funciona como um assistente que remove a barreira do "esforço físico" e da "tentativa e erro", tornando a prática do tiro um hobby relaxante e seguro para sua aposentadoria.

#### Jornada do Usuário: Alessandra Pinheiro
A rotina de aposentadoria e o zelo pela proteção do lar.
Pela manhã, enquanto organiza sua casa, Alessandra nota no noticiário local um aumento nas ocorrências de segurança no seu bairro. Como ex-investigadora, seu instinto de proteção dispara e ela pensa: "Preciso garantir que minha arma de porte esteja perfeitamente calibrada caso eu precise dela. Vou ao estande hoje após minha consulta médica".
Após sair do médico, ela vai ao clube de tiro. Ela escolhe um horário mais calmo, pois prefere um ambiente onde possa se concentrar sem pressa e sem o barulho excessivo de muitos atiradores ao redor.
Alessandra retira seu equipamento da bolsa. Em vez de caminhar várias vezes até o alvo — o que cansaria seus joelhos — ela posiciona o smartphone no tripé a curta distância. Sentada na bancada, ela dispara e observa o notebook. O sistema mostra instruções visuais claras e grandes. "As setas indicam exatamente o ajuste", pensa ela, sentindo-se aliviada por não precisar de esforço físico para interpretar cálculos complexos.
Satisfeita com o agrupamento perfeito no centro do alvo, ela limpa e guarda seu armamento. Ao chegar em casa, coloca o equipamento em seu local seguro, sentindo uma profunda sensação de autonomia e paz. Ela sabe que, mesmo aposentada e com as limitações da idade, a tecnologia permitiu que ela mantivesse sua capacidade de defesa intacta

### Lucas Mendes, formando em jogos digitais
- Idade: 23 anos
- Status: Persona Primária.
- Objetivos: Aprender a zerar sua luneta sozinho, economizar munição (alto custo para iniciantes) e ganhar confiança no esporte.
- Habilidades: Nativo digital, familiarizado com interfaces de jogos e aplicativos de alta performance; pouca experiência com mecânica de armas e cálculos balísticos manuais.
- Tarefas: Prática de tiro de precisão nos finais de semana, estudo de manuais digitais e participação em comunidades online de CACs.
- Relacionamentos: Solteiro.
- Requisitos: Interface no estilo das calculadoras ballísticas mobile, feedback instantâneo e linguagem visual que dispense o uso de tabelas de papel complexas.
- Expectativas: Que o sistema seja tão intuitivo quanto um aplicativo de banco ou jogo, resolvendo o problema técnico com poucos toques.

- O que PENSA e SENTE?
Quais são os seus sonhos? 
Lucas sonha em dominar a técnica de tiro de precisão com a mesma naturalidade com que domina mecânicas de jogos complexos, sentindo-se empoderado pela tecnologia para superar sua falta de experiência prática.

- O que OUVE?
Quais produtos de comunicação consome? 
Consome vídeos de tutoriais rápidos no YouTube, fóruns de discussão sobre balística digital e comunidades de Discord voltadas para entusiastas de tecnologia e tiro.

- O que VÊ?
Como é o mundo em que a persona vive? 
Vive em um mundo saturado de interfaces digitais de alta performance e gratificação instantânea, onde processos analógicos baseados em papel parecem obsoletos e ineficientes.

- O que FALA e FAZ?
Quais seus hobbies? 
Além de frequentar o clube de tiro, dedica seu tempo ao desenvolvimento de projetos de jogos e ao estudo de UX (experiência do usuário), o que o torna muito crítico quanto à usabilidade dos sistemas que utiliza.

- Quais são as DORES?
Que obstáculos precisa ultrapassar para conseguir o que deseja? 
Precisa vencer a barreira da terminologia técnica densa (como entender cálculos de MOA e MIL) e o medo de "passar vergonha" no estande ao não conseguir ajustar seu equipamento sozinho.

- Quais são as NECESSIDADES?
O que acabaria com seus problemas? 
Um sistema que traduza a física balística em uma interface visual "gamificada", que indique exatamente quantos "cliques" ele deve girar na torre da luneta sem exigir cálculos manuais.

#### Contexto de Uso: Lucas Mendes
Ambiente Físico e Social: Lucas utiliza o sistema em clubes de tiro modernos. Socialmente, ele se sente compelido a demonstrar competência técnica para seus pares e busca na tecnologia uma forma de validar seu desempenho rapidamente.

Interação e Equipamento: Como um nativo digital, ele opera o notebook e o smartphone com extrema agilidade. Ele valoriza a conexão Wi-Fi estável e a precisão dos marcadores ArUco, tratando o setup do sistema como parte da "configuração de hardware" necessária para sua prática.

Narrativa de Uso: Imagine Lucas no estande de tiro. Ele posiciona o smartphone no tripé próximo ao alvo e volta para trás da linha de tiro. Após o primeiro disparo, ele não precisa de um telescópio de observação; ele olha para a tela do notebook e, em menos de 5 segundos, o sistema exibe um gráfico visual intuitivo. Lucas sorri ao ver a instrução "Girar 6 cliques para a direita", sentindo a mesma satisfação de quem resolve um puzzle em um jogo, economizando munição e tempo.

#### Jornada do Usuário: Lucas Mendes
Expectativa acadêmica e a experiência com equipamento alugado.
No laboratório da faculdade, enquanto compila um código para seu projeto de jogos, Lucas recebe uma notificação de um grupo de CACs sobre uma nova técnica de agrupamento. Curioso e querendo testar o que aprendeu, ele pensa: "Vou passar no clube hoje à noite, alugar uma carabina e ver se consigo calibrar a luneta usando o sistema que estou estudando".
Lucas chega ao clube e faz o aluguel de uma arma disponível. Como não é um equipamento que ele conhece a fundo, ele se sente um pouco inseguro sobre como a luneta foi deixada pelo usuário anterior.
Ele posiciona o smartphone e o notebook. O sistema atua como seu instrutor. A cada clique que o software sugere, Lucas sente que está "subindo de nível". Ele agrupa os tiros no centro do alvo e tira uma foto da tela do notebook para mostrar aos amigos do curso.
Lucas devolve o armamento no balcão do clube, sentindo que aproveitou cada centavo da munição cara que comprou. Ele chega em casa, abre seu computador e anota as observações da experiência, satisfeito por ter dominado a máquina sem depender de ninguém.
