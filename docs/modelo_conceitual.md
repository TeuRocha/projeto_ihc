# Esquema Conceitual de Signos

## Cenário de Interação

Após o serviço, Márcio Rocha chega ao clube de tiro com sua luneta recém-comprada para realizar a calibração. Ele precisa de agilidade, pois o horário é avançado e ele tem compromissos cedo no dia seguinte. Utilizando o computador disponível no estande e um smartphone como sensor, Márcio acessa o sistema que, por ser focado em uso profissional, permite a entrada na sessão de tiro sem etapas burocráticas densas. Ao receber o status visual de que a câmera está conectada, ele confirma que os pré-requisitos foram atendidos e inicia a prática sabendo que o objetivo será alcançado rapidamente.

No estande, Alessandra Pinheiro posiciona seu armamento para a distância de 25 metros. Ao interagir com o sistema, ela não se depara com tabelas complexas ou solicitações de dados ambientais e técnicos do projétil. O sistema realiza a compensação automática de escala e perspectiva via marcadores, exigindo apenas que Alessandra forneça a distância desejada de forma simples e legível. Ao finalizar essa configuração inicial, o sistema inicia o monitoramento ativo.

Lucas Mendes, preocupado com o custo das munições gastas, utiliza a Visão Top-Down do sistema em seu notebook para guiar seu ajuste. Ele aponta para o sistema a exata coordenada onde mirou (POA) e o software processa os dados da imagem para converter a diferença física em comandos semânticos de "cliques". Em vez de apresentar termos técnicos confusos como MIL ou MOA, o sistema instrui diretamente qual direção ele deve adotar nas torres da luneta, eliminando o erro de conversão matemática de Lucas e garantindo que o próximo disparo atinja o centro.

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
| Acesso (A) \- dados para acessar o sistema |  |  |  |  |  |  |  |  |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| **Signo** | **Origem** | **Observações** | **Tipo de conteúdo** | **Restrição sobre conteúdo** | **Cena MOLIC** | **Valor default** | **Prevenção** | **Recuperação** |
| Usuário | Domínio | Campo de login obrigatório (*) | Texto | Não pode ser nulo | Efetuar login |  | PP: Campo marcado como obrigatório | RA: "Usuário ou senha incorretos. Tente novamente." |
| Senha | Domínio | Campo de login obrigatório (*) | texto (protegido) | Não pode ser nulo | Efetuar login |  | PP: Campo marcado como obrigatório | RA: "Usuário ou senha incorretos. Tente novamente." |
| E-mail |  Domínio | Campo de login obrigatório (*) | Texto (formato e-mail) | Não pode ser nulo; formato válido | Cadastrar usuário |  | PP: Campo marcado como obrigatório | RA: "Algum dos dados está incorreto." |
| Confirmar senha | Domínio | Campo de login obrigatório (*) | Texto (formato e-mail) | Não pode ser nulo; formato válido | Cadastrar usuário |  | PP: Campo marcado como obrigatório | RA: "Algum dos dados está incorreto." |

## Tabela de Configuração de Calibração
| Configuração (C) \- dados para configurar distância no sistema |  |  |  |  |  |  |  |  |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| **Signo** | **Origem** | **Observações** | **Tipo de conteúdo** | **Restrição sobre conteúdo** | **Cena MOLIC** | **Valor default** | **Prevenção** | **Recuperação** |
| Distância de calibração | Domínio/UI | Valor em metros obrigatório (*) | Numéro decimal | Valor válido para calibração (ex: 10.0); não nulo | Definir distância |  | PP: Placeholder "ex: 10.0" exibido no campo | RA: "Valor inválido para calibração." |


## Tabela de Interação e Captura
| Interação e Captura (IC) \- interação do usuário para captura de dados |  |  |  |  |  |  |  |  |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| **Signo** | **Origem** | **Observações** | **Tipo de conteúdo** | **Restrição sobre conteúdo** | **Cena MOLIC** | **Valor default** | **Prevenção** | **Recuperação** |
| Imagem em tempo real da câmera | Sistema | Feed ao vivo exibido na cena "Definir POA" | Imagem (stream) | Câmera deve estar ativa e com alvo enquadrado | Definir POA |  | PP: Instrução para preparar alvo antes de acessar a cena | RA: Verificar conexão/posição da câmera |
| Status de detecção dos ArUcos | Sistema | Indicador exibido sobre a imagem | Texto/ícone | Marcadores devem estar visíveis no campo da câmera | Definir POA | Não detectado | PP: Instrução de posicionamento exibida ao usuário | RA: Sistema exibe status negativo; usuário reposiciona alvo |
| Marcação do POA | Domínio/UI | Clique do usuário dentro do bloco verde na imagem | Coordenada (x,y) | Deve estar dentro da área delimitada pelo bloco verde | Definir POA |  | PP: Bloco verde destaca a área válida para clique | RA: "Erro, clique fora da área do alvo! Clique dentro do bloco verde." |
| Imagem de referência | Sistema | Capturada ao clicar no botão "Salvar referência" | Imagem estática | Câmera estável; alvo visível com ArUcos detectados | Salvar referência |  | PP: Mensagem de sucesso do POA exibida antes de liberar o botão | RA: "Não foi possível salvar a imagem. Tente novamente." |
| POI sinalizado | Sistema | Calculado por subtração entre imagem de referência e imagem pós-disparo | Coordenada (x,y) sonreposta na imagem | Furo de impacto deve ser detectável; sem ruído excessivo | Confirmar POI |  | PP: Instrução para manter câmera estável e alvo em boailuminação | RA: Sistema exibe mensagem específica e retorna para nova tentativa |

## Tabela de Calibração
| Calibração (CB) \- dados para calibrar |  |  |  |  |  |  |  |  |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| **Signo** | **Origem** | **Observações** | **Tipo de conteúdo** | **Restrição sobre conteúdo** | **Cena MOLIC** | **Valor default** | **Prevenção** | **Recuperação** |
| Desvio linear calculado | Sistema | Resultado do processamento após confirmação do POI | Valor numérico (distância em pixels/cm) | Deve ser calculável com POI e POA definidos | Consultar feedback |  | PP: POA e POI confirmados antes do cálculo | RA: Valor discrepante do habitual - sistema emite alerta |
| Feedback de correção | Sistema | Exibido na cena "Consultar Feedback" | Texto (cliques x direção) | Deve ser gerado após cálculo do desvio linear | Consultar feedback |  | PP: Instrução de leitura exibida antes do valor | RA: Alerta de "Valor discrepante do habitual" - usuário deve verificar |

## Tabela de Validação
| Validação (V) \- dados para validar |  |  |  |  |  |  |  |  |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| **Signo** | **Origem** | **Observações** | **Tipo de conteúdo** | **Restrição sobre conteúdo** | **Cena MOLIC** | **Valor default** | **Prevenção** | **Recuperação** |
| Confirmação de acerto | UI | Botões "concluir e salvar" e "novo disparo (manter POA)" na cena "Consultar feedback" | Binário (sim/não) | Torres devem ter sido corrigidas previamente | Consultar feedback |  | PP: Precondição exibida antes de acessar a cena; usuário confirma correção das torres | RA: "novo disparo (manter POA)" sistema retorna para "Salvar referência" para reiniciar o ciclo de calibração |
