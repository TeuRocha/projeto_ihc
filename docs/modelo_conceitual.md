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

## Tabela de Configuração de Calibração
| Configuração de Calibração (C) \- dados para calcular a calibração no sistema|  |  |  |  |  |  |  |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| **signo** | **origem** | **observações** | **Tipo de conteúdo** | **restrição sobre conteúdo** | **valor default** | **prevenção** | **recuperação** |
| +Distância | Domínio | Distância real entre o atirador e o alvo para cálculo de MOA | Número decimal |  Não pode ser nulo ou negativo | 10,0 | PP: dica visual "(metros)", PA: Bloqueio de caracteres não númericos | RA: Mensagem de erro se o campo estiver vazio ao calcular |
| Tamanho do ArUco | Domínio | Medida real do lado do marcador impresso para escala de pixels | Número decimal | Deve ser um valor real em centímetros | 3,0 | PP: Instrução "Meça o marcador com um régua" | RA: Alerta se o valor inserido for discrepante da escala detectada |
| Status da Câmera | Aplicação | Indica se o sinal de vídeo do smartphone está ativo no PC | Estado (Texto/Ícone) | {Conectado, Desconectado} | Desconectado | PA: Desabilita botões de captura se o status for "Desconectado" | CE: Instrução "Verifique a conexão Wi-Fi ou IP do smartphone" |
| Ponto de Mira (POA) | Aplicação | Coordenada do centro do alvo definida pelo clique do usuário | Coordenada (x,y) | Deve estar dentro da área delimitada pelos ArUcos |  | PA: Impedir a fixação do ponto fora da área do alvo | RA: Opção "Redefinir POA" para novo clique se houver erro de marcação |
| Valor do Clique | Domínio Z Sensibilidade da luneta (ex: 1/4 MOA) para cálculo de correção | Seleção simples | {1/2, 1/4, 1/8} | 1/4 | PA: Seleção obrigatória através de menu dropdown |  |

## Tabela de Resultado do Disparo
| Resultado do Disparo (R) \- dados para verificar disparo |  |  |  |  |  |  |  |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| **signo** | **origem** | **observações** | **Tipo de conteúdo** | **restrição sobre conteúdo** | **valor default** | **prevenção** | **recuperação** |
| Ponto de Impacto (POI) | Aplicação | Coordenada do furo detectada automaticamente via subtração de imagens | Coordenada (x, y) | Deve estar dentro da área útil do alvo delimitada pelos ArUcos | - | PA: Bloqueia a detecção se a imagem de referência ('r') não existir | RA: Permite ao usuário clicar manualmente no furo caso a detecção automática falhe |
| Desvio Linear | Aplicação | Distância real calculada entre o POA e o POI em centímetros | Número decimal | Valor deve ser maior ou igual a zero | 0,0 | PP: Exibição clara da unidade de medida (cm) ao lado do valor | = |
| Ajuste de Cliques | Domínio | Resultado final da calibração informando a direção e quantidade de giros na luneta | Texto | - | "0 cliques" | PA: Só realizar o cálculo se a 'Distância' e o 'Valor do Clique' estiverem preenchidos | - |
| Imagem de Subtração | Aplicação | Frame processado que destaca o novo furo (impacto) para validação visual do atirador | Imagem | - | - | PP: Legenda informativa "Destaque do impacto detectado" | CE: Mensagem "Ruído visual excessivo: verifique a estabilidade da câmera" |
| Status de Detecção | Aplicação | Feedback textual sobre o sucesso ou falha do algoritmo de visão computacional | Seleção simples | {Sucesso, Falha, Aguardando} | Aguardando | PP: Barra de status com cores (Verde/Vermelho) para feedback imediato | RA: Sugestão de "Tente aproximar o alvo da câmera para melhor contraste" |
Valor de MOA Calculado | Aplicação | Conversão do desvio linear para medida angular baseada na distância informada | Número decimal | - | 0,0 | PP: Exibição do valor com precisão de duas casas decimais | - |

## Tabela de Equipamento
| Equipamento (E) \- dados para definir clique |  |  |  |  |  |  |  |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| **signo** | **origem** | **observações** | **Tipo de conteúdo** | **restrição sobre conteúdo** | **valor default** | **prevenção** | **recuperação** |
| Valor do Clique | Domínio | Sensibilidade de ajuste das torres da luneta (essencial para o cálculo final) | Seleção simples | {1/2 MOA, 1/4 MOA, 1/8 MOA, 0,1 MIL} | 1/4 MOA | PA: Seleção obrigatória; o sistema não calcula sem este dado | RA: Alerta caso o valor não seka compatível com a distância informada |
| Unidade de Medida | Domónio | Define se a correção será exibida em MOA (Minuto de Ângulo) ou MIL (Miliradiano) | Seleção simples | {MOA, MIL} | MOA | PP: Explicação sobre a diferença entre as unidades | - |
| Sentido de Rotação | Domínio | Define se o ajuste físico é no sentido horário (CW) ou anti-horário (CCW) | Seleção simples | {CW, CCW} | CW | AL: Confirmação "Sua luneta gira no sentido horário para subir o impacto?" | - |
