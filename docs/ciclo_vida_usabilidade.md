# Ciclo de Vida de Engenharia de Usabilidade

## Capacidades e Restrições

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

## Tabela dos Princípios Gerais de Projeto

| Descrição do contexto de uso | Nome da referência | Descrição da referência | Link de Referência |
| :--- | :--- | :--- | :--- |
| Atirador esportivo realizando a calibração de mira em um estande de tiro (ambiente ruidoso) utilizando notebook e smartphone | 10 Heurísticas de Usabilidade (Jakob Nielsen) | Garante a visibilidade do status do sistema (ex: confirmar se os ArUcos foram detectados) e a prevenção de erros (ex: não permitir o cálculo se o campo de distância estiver vazio) | [Link](https://www.nngroup.com/articles/ten-usability-heuristics/)
| Calibração técnica de precisão onde o usuário precisa de eficácia (acertar o ajuste) e eficiência (fazer rápido no estande) | ISO 9241-11 (Ergonomia da interação humano-sistema) | Esta norma define usabilidade em termos de eficácia e eficiência em um contexto de uso específico. É vital para validar se o sistema realmente ajuda a reduzir o tempo de calibração no clube de tiro | [Link](https://www.iso.org/obp/ui/#iso:std:iso:9241:-11:ed-2:v1:en)
| Uso do software em clubes de tiro e entidades de prática desportiva regulamentadas no Brasil | Estatuto do Desarmamento e Decretos (Lei nº 10.826/2003) | Representa o Aspecto de Negócio. O projeto deve estar alinhado às normas de segurança e regulação de tiro esportivo para ser um produto legalmente aceito em clubes oficiais | [Link](https://www.planalto.gov.br/ccivil_03/leis/2003/l10.826.htm)

# Metas de Usabilidade

## Exigências Qualitativas

- *Feedback de alinhamento em tempo real:* A interface deve fornecer indicadores visuais claros que confirmem a detecção dos 4 ArUcos, garantindo que o atirador saiba que a homografia está ativa.
- *Visão top-down padronizada:* O sistema deve apresentar o alvo corrigido (sem distorção de perspectiva) para que o usuário tenha uma "visão bem definida", facilitando a marcação do POA.
- *Prevenção de erros de configuração:* O software deve impedir o disparo da função de calibração caso informações críticas (como a distância do alvo) não tenham sido inseridas, evitando diagnósticos balísticos incorretos.
- *Navegação orientada:* A interface desktop deve guiar o usuário sequencialmente pelas etapas: Conexão -> Marcação POA -> Captura de Referência -> Captura de Impacto.

## Exigência Quantitativas

- *Facilidade de aprendizado:* 20%
- *Facilidade de memorização:* 20%
- *Eficiência:* 20%
- *Baixa taxa de erro:* 20%
- *Satisfação positiva do usuário:* 20%
