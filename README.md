# Projeto de Interface Humano-Computador

Projeto apresentado ao Centro Universitário [FEI](https://portal.fei.edu.br/), como parte dos requisitos necessários para aprovação na disciplina de Interface Humano-Computador (CC8122) do curso de Ciencia da Computação, orientado pelo Prof. Dr. [Plinio Thomaz Aquino Junior](http://lattes.cnpq.br/6186413528999908).

## Membros da Equipe:
- Mateus Rocha

## Título Original do TCC:
Sistema de Auxilio para Calibragem de Miras Ópticas

## Orientador:
- Plinio Thomaz Aquino Junior

### Previsto desenvolver interface?
(x) Sim   ( ) Não

### Objetivo do Trabalho?
Calcular a calibração da mira do usuário, e guiar ele para concluir sua calibragem.

### Qual o produto final?
Um sistema de interface simples para obter do usuário a informação da distância que ele deseja calibrar seu equipamento, e retornar o feedback o mais preciso e rápido possível.

### Quem é o usuário final deste produto?
Os CACs (Colecionadores, atiradores e caçadores), policiais, pessoas com porte de arma, jogadores de airsoft com uso de miras, qualquer usuário dentro da lei que deseja calibrar seu equipamento.

### O que o usuário recebe de benefício ao usar esse produto?
- Menos gasto de munição, consequentemente menos gasto financeiro;
- Não se faz necessário conhecimento técnico para calibração, o sistema resolve sozinho;
- Otimização do tempo do usuário, menos tempo para calibrar.

### Quais as funcionalidades da ferramenta (visão do usuário)?
- Sistema de cadastro e login do usuário;
- Tela de distância de calibração desejada;
- Tela de ponto de impacto (POI);
- Tela de feedback.

### Quais tecnologias e ferramentas computacionais que pretendem usar neste projeto (TCC)?
- Código desenvolvido em Python 3.10;
- Bibliotecas:
  - OpenCV;
  - PyWebView;
  - NumPy.
- Hardware de captura e transmissão: Redmi com protocolo RTSP/HTTP (App IP Webcam);
- Técnicas e Algoritmos:
  - Método de Zhang;
  - Matriz de homografia;
  - Subtração de Imagem e Operações Morfológicas.

### Qual é o contexto de uso dessa aplicação?
- Usuários: Atiradores esportivos, caçadores e colecionadores (CACs), com foco especial em iniciantes que carecem do conhecimento de cálculos balísticos, ou entusiastas que desejam otimizar seu tempo e munição.
- Ambiente: Local controlado e autorizado para a prática de tiro, como estandes de tiro ou clubes especializados, que possuam iluminação adequada para garantir a nitidez da captura de imagem.
- Equipamentos e Configuração: O usuário utiliza um Smartphone posicionada com um tripé a curta distância do alvo (aproximadamente 2 metros), que transmite o sinal de vídeo via wi-fi para um notebook atrás da linha de tiro, o alvo deve conter marcador fiduciais (ArUco) para permitir a coreção de perspectiva e escala.
- Tarefa: O atirador realiza disparos em direção ao centro do alvo (POA), o sistema processa a imagem do impacto e fornece, em menos de 1 segundo, o feedback visual e numérico da correção necessária em "cliques" nas torres do seu equipamento.
- Contexto Social/Econômico: Uma solução nacional de baixo custo voltada para tornar o esporte mais acessível no Brasil, reduzindo a dependência de tecnologias importadas de alto valor e simplificando um processo que tradicionalmente é feito por tentativa e erro.

# Desenvolvimento:
- [Análise de Concorrência](docs/analise_concorrencia.md)
- [Personas](docs/personas.md)
- [Cenário de Análise/Problema](docs/cenario_analise_problema.md)
- [Análide de Tarefas](docs/analise_tarefas.md)
- [Coleta de Dados](docs/coleta_dados.md)
- [Ciclo de vida da engenharia de usabilidade](docs/ciclo_vida_usabilidade.md)
- [Modelo Conceitual](docs/modelo_conceitual.md) 
- [MOLIC](docs/molic.md)
- [FIGMA](docs/figma.md)
- [Planejamento da Avaliação](docs/planejamento_avaliacao.md)
- [Avaliação de IHC através de Inspeção Heurística](docs/avaliacao_ihc_heuristica.md)
- [Avaliação de Usabilidade baseado em Observação do Usuário](docs/avaliacao_usabilidade_usuario.md)
