# Esquema Conceitual de Signos

## Cenário de Interação

Após o serviço, Márcio Rocha chega ao clube de tiro com sua luneta recém-comprada para realizar a calibração [6]. Ele precisa de agilidade, pois o horário é avançado e ele tem compromissos cedo no dia seguinte [4, 6]. Utilizando o computador disponível no estande e um smartphone como sensor [3, 7], Márcio abre o software que, por ser focado em uso profissional, permite o acesso imediato às funções de tiro sem etapas burocráticas de assinatura e cadastro densos [2]. Ao ver o status "Câmera Pronta" na tela, ele confirma que os pré-requisitos de conexão foram atendidos [1] e inicia a prática sabendo que o objetivo será alcançado rapidamente [8].

No estande, Alessandra Pinheiro posiciona seu armamento para a distância de 25 metros [3]. Ao interagir com o sistema, ela não se depara com tabelas complexas ou solicitações de dados ambientais e técnicos do projétil [1, 2]. O sistema utiliza os marcadores ArUco no alvo para realizar a compensação automática de escala e perspectiva [5], exigindo apenas que Alessandra confirme a distância no campo de texto com fontes ampliadas para facilitar sua leitura [4]. Ao finalizar a configuração simples, o sistema dispara o início do monitoramento de vídeo [6].

Lucas Mendes, preocupado com o custo das munições gastas [3], utiliza a Visão Top-Down do sistema em seu notebook para guiar seu ajuste [4]. Ele marca o ponto onde mirou (POA) com um clique e o software processa os dados de imagem para converter a diferença física em comandos semânticos de "cliques" [2]. Em vez de apresentar termos técnicos confusos como MIL ou MOA [1], o sistema exibe instruções diretas de direção para as torres da luneta, eliminando o erro de Lucas e garantindo que o próximo disparo atinja o centro [1].

## Design Centrado na Comunicação

| Tópico > Subtópico (diálogo) | Falas e Signos |
| ----- | ----- |
| Calibrar Luneta | U: Preciso cadastrar minha luneta. |
| > Efetuar login | D: Qual o seu login e senha? <br> U: Preencho os campos obrigatórios para logar no sistema. |
| > Definir distância da calibração | D: Deseja definir para qual distância a calibração?. <br> U: Quero definir a distância para 10 metros. |
| > Preparar alvo | D: Prepare o alvo na distância definida, e com os marcadores postos em suas extremidades. |
| > Posicionar câmera | D: Posicione a câmera até a detecção dos marcadores ArUcos. |
| > Definir POA | D: Agora defina o seu POA dentro dos marcadores ArUcos. <br> U: Defini o POA distante do centro. <br> D: POA definido com sucesso. |
| > Definir imagem de referência | D: Pressione o botão "Salvar Referência" para definir a referência dos cálculos. |
| Efetuar disparo | U: Efetuei o disparo, necessito do feedback. |
| > Confirmar POI | D: O POI sinalizado está correto? <br> U: Sim, está. <br> D: Estou processando os cálculos para correção da mira. |
| > Informar resultado | D: Faça X cliques para direção Y para calibrar sua mira. <br> U: Estou corrigindo a mira. |
| Efetuar disparo corrigido | U: A calibração foi certeira. |
| Confirmar calibração | D: A calibração foi realizada com sucesso? <br> U: Sim, calibração correta. |

## Mapa de Objetivos do Usuário

<img width="711" height="930" alt="mapacore" src="https://github.com/user-attachments/assets/5a786ed1-bfa3-4da1-a0f8-5c59789d9c55" />

## Tabela de Acesso
| Acesso (A) \- dados para acessar o sistema |  |  |  |  |  |  |  |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| **signo** | **origem** | **observações** | **Tipo de conteúdo** | **restrição sobre conteúdo** | **valor default** | **prevenção** | **recuperação** |
| Usuário | Domínio | Campo de login obrigatório (*) | Texto | Não pode ser nulo |  | PP: Campo marcado como obrigatório | RA: "Usuário ou senha incorretos. Tente novamente." |
| Senha | Domínio | Campo de login obrigatório (*) | texto (protegido) | Não pode ser nulo |  | PP: Campo marcado como obrigatório | RA: "Usuário ou senha incorretos. Tente novamente." |
| Nome | Domínio | Campo de login obrigatório (*) | Texto | Não pode ser nulo |  | PP: Campo marcado como obrigatório | RA: "Algum dos dados está incorreto." |
| E-mail |  Domínio | Campo de login obrigatório (*) | Texto (formato e-mail) | Não pode ser nulo; formato válido |  | PP: Campo marcado como obrigatório | RA: "Algum dos dados está incorreto." |
| Confirmar senha | Domínio | Campo de login obrigatório (*) | Texto (formato e-mail) | Não pode ser nulo; formato válido |  | PP: Campo marcado como obrigatório | RA: "Algum dos dados está incorreto." |

## Tabela de Configuração de Calibração
| Configuração (C) \- dados para configurar distância no sistema |  |  |  |  |  |  |  |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| **signo** | **origem** | **observações** | **Tipo de conteúdo** | **restrição sobre conteúdo** | **valor default** | **prevenção** | **recuperação** |
| Distância de calibração | Domínio/UI | Valor em metros obrigatório (*) | Numéro decimal | Valor válido para calibração (ex: 10.0); não nulo |  | PP: Placeholder "ex: 10.0" exibido no campo | RA: "Valor inválido para calibração." |


## Tabela de Interação e Captura
| Interação e Captura (IC) \- interação do usuário para captura de dados |  |  |  |  |  |  |  |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| **signo** | **origem** | **observações** | **Tipo de conteúdo** | **restrição sobre conteúdo** | **valor default** | **prevenção** | **recuperação** |
| Imagem em tempo real da câmera | Sistema | Feed ao vivo exibido na cena "Definir POA" | Imagem (stream) | Câmera deve estar ativa e com alvo enquadrado |  | PP: Instrução para preparar alvo antes de acessar a cena | RA: Verificar conexão/posição da câmera |
| Status de detecção dos ArUcos | Sistema | Indicador exibido sobre a imagem | Texto/ícone | Marcadores devem estar visíveis no campo da câmera | Não detectado | PP: Instrução de posicionamento exibida ao usuário | RA: Sistema exibe status negativo; usuário reposiciona alvo |
| Marcação do POA | Domínio/UI | Clique do usuário dentro do bloco verde na imagem | Coordenada (x,y) | Deve estar dentro da área delimitada pelo bloco verde |  | PP: Bloco verde destaca a área válida para clique | RA: "Erro, clique fora da área do alvo! Clique dentro do bloco verde." |
| Imagem de referência | Sistema | Capturada ao clicar no botão "Salvar referência" | Imagem estática | Câmera estável; alvo visível com ArUcos detectados |  | PP: Mensagem de sucesso do POA exibida antes de liberar o botão | RA: "Não foi possível salvar a imagem. Tente novamente." |
| POI sinalizado | Sistema | Calculado por subtração entre imagem de referência e imagem pós-disparo | Coordenada (x,y) sonreposta na imagem | Furo de impacto deve ser detectável; sem ruído excessivo |  | PP: Instrução para manter câmera estável e alvo em boailuminação | RA: Sistema exibe mensagem específica e retorna para nova tentativa |

## Tabela de Calibração
| Calibração (CB) \- dados para calibrar |  |  |  |  |  |  |  |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| **signo** | **origem** | **observações** | **Tipo de conteúdo** | **restrição sobre conteúdo** | **valor default** | **prevenção** | **recuperação** |
| Desvio linear calculado | Sistema | Resultado do processamento após confirmação do POI | Valor numérico (distância em pixels/cm) | Deve ser calculável com POI e POA definidos |  | PP: POA e POI confirmados antes do cálculo | RA: Valor discrepante do habitual - sistema emite alerta |
| Feedback de correção | Sistema | Exibido na cena "Consultar Feedback" | Texto (cliques x direção) | Deve ser gerado após cálculo do desvio linear |  | PP: Instrução de leitura exibida antes do valor | RA: Alerta de "Valor discrepante do habitual" - usuário deve verificar |

## Tabela de Validação
| Validação (V) \- dados para validar |  |  |  |  |  |  |  |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| **signo** | **origem** | **observações** | **Tipo de conteúdo** | **restrição sobre conteúdo** | **valor default** | **prevenção** | **recuperação** |
| Confirmação de acerto | UI | Botões "sim" e "não" na cena "Confirmar acerto" | Binário (sim/não) | Torres devem ter sido corrigidas previamente |  | PP: Precondição exibida antes de acessar a cena; usuário confirma correção das torres | RA: "não" sistema retorna para "Definir POA" para reiniciar o ciclo de calibração |
