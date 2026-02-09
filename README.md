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

# Segunda entrega

## PERSONAS

### PERSONAS PRIMÁRIAS:
- Márcio, policial civil
- Alessandra, policial aposentada

### PERSONA SECUNDÁRIA:
- Lourdes, secretária do clube de tiro

### PERSONA NEGATIVA:
- Henrique, aposentado, objetivo: busca por algo que o faça sentir-se forte na idade atual


