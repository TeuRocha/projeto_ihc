# Capacidades e Restrições

## Tabela de Capacidades e Restrições

| Capacidades | Restrições |
| ----------- | ---------- |
| Uso de câmeras smartphone | Uso de ArUcos nos alvos |
| Independência de escala | Condição de iluminação constante |
| Processamento local e offline | Visibilidade total dos marcadores |
| Compensação de perspectiva | Estabilidade da câmera |
| Cálculo de ajuste angular | Contraste de impacto |

## Descrição das Capacidades

- Uso de câmeras smartphone: É possível utilizar câmeras mais acessíveis, até mesmo do seu celular para a coleta de dados do alvo.
- Independência de escala: O sistema é capaz de se autoajustar a qualquer tamanho de alvo (do A4 ao alvo oficial de 47x25 cm) sem necessidade de alteração no código fonte, utilizando os marcadores ArUco como referência métrica universal.
- Processamento local e offline: Por rodar nativamente em Python (VS Code), o sistema não depende de conexão com servidores na nuvem para processar as imagens, garantindo privacidade dos dados e funcionamento em estandes de tiro remotos (via Hotspot ou USB)
- Compensação de perspectiva: Graças à matriz de homografia, o software é capaz de "desentortar" a imagem capturada. Isso permite que o smartphone não precise estar perfeitamente centralizado ou paralelo ao alvo durante a coleta de dados.
- Cálculo de ajuste angular: O sistema converte o erro linear em unidades angulares de tiro, informando o número exato de "cliques" para a correção das torres da luneta para a distância definida.

## Descrição das Restrições

- Uso de ArUcos nos alvos: Os ArUcos são necessários nos alvos para a captura das informações na imagem, nenhum alvo é desenvolvido já com tais imagens, tendo a necessidade de serem colocadas antes da calibração no alvo limpo.
- Condição de iluminação constante: Como o sistema utiliza a técnica de subtração de fundo, mudanças bruscas de luz entre a foto de referência e a foto pós-disparo podem gerar falsos positivos na detecção do furo.
- Visibilidade total dos marcadores: Para o cálculo da matriz H de 3x3, é obrigatório que os 4 marcadores ArUco estejam visíveis e sem obstruções. Se um tiro atingir o marcador ou se ele for encoberto, o sistema perde a capacidade de alinhar a imagem.
- Estabilidade da câmera: Embora a homografia ajude, vibrações extremas ou falta de um suporte fixo (tripé) no momento da captura da imagem de referência e da detecção podem prejudicar a precisão milimétrica desejada.
- Contraste de impacto: A detecção do ponto de impacto (POI) depende de um contraste visual entre o furo e o alvo. Em alvos com cores muito escuras onde o furo não gera uma sombra nítida, a eficácia do algoritmo de detecção de contornos pode ser reduzida.

## Justificativa das Capacidades

- Uso de câmeras smartphone: Baratiar o acesso a tecnologia, possibilitando a implementação para o máximo de estandes possíveis.
- Independência de escala: Não se limitar aos padrões de alvos oficiais, buscando agradar o público geral lhes proporcionando qualquer alvo que desejem (desde que tenha os ArUcos incluso).
- Processamento local e offline: Garantir a privacidade, e facilitando o uso tanto para os usuários quanto os funcionários do estande caso a necessidade do manuseio.
- Compensação de perspectiva: Para garantir a confiabilidade dos cálculos, e permitir o uso da câmera em outros ângulos que não necessariamente a visualização frontal do alvo.
- Cálculo de ajuste angular: Conceder um feedback dos cálculos já interpretados em cliques para o usuário, para auxiliar a calibração de suas ferramentas.

## Justificativa das Restrições

- Uso de ArUcos nos alvos: Para garantir a confiabilidade nos cálculos o sistema desenvolvido não tem como realizar a homografia sem as imagens.
- Condição de iluminação constante: Sem uma boa iluminação a detecção dos ArUcos com a câmera tornam-se imprecisos, e dificulta na detecção do furo nos alvos, gerando dificuldades para o funcionamento devido do sistema.
- Visibilidade total dos marcadores: A detecção dos marcadores é a base do nosso sistema, e estamos trabalhando com disparos que tendem a errar o alvo, caso um disparo acerte um dos marcadores sera necessário efetuar a troca do marcador, gerando assim mais trabalho para o usuário.
- Estabilidade da câmera: Quanto mais nitida a imagem melhor para o sistema garantir a correção milimétrica da ferramenta do usuário, além de garantir uma boa definição do POI.
- Contraste de impacto: Dependendo da cor do alvo, iluminação e ângulo da câmera, é capaz de prejudicar no contraste do furo do projétil no alvo.