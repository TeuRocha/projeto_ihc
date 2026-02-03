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
Os CACs (Colecionadores, atiradores e caçadores), policiais, pessoas com porte de arma.

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
