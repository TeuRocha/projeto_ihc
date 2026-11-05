# Análise de concorrência

Para o desenvolvimento deste projeto, foram analisadas três soluções representativas disponíveis no mercado: *Chairgun Elite*, *Lapua Ballistics* e *Ballistic-X*. A escolha destes sistemas não foi aleatória; baseou-se em uma pesquisa de mercado considerando o volume de usuários ativos nas lojas de aplicativos e nos relatos diretos coletados durante entrevistas informais com frequentadores de clubes de tiro esportivo. Estes sistemas representam o padrão de interação ao qual o público-alvo já está habituado, estabelecendo as convenções de domínio que o nosso projeto deve considerar.

## Padrões Encontrados e Oportunidades de Melhoria

A análise detalhada das interfaces revelou padrões consistentes de affordances e tendências virtuais, mas também mostra gargalos de usabilidade que o nosso sistema se propõe a resolver.

1. Lapua Ballistics
   - *Análise:* O aplicativo foca na precisão extrema dos cálculos de munição. Como padrão visual, adota um design em blocos de configuração e páginas com tons escuros (dark mode) para reduzir o cansaço visual, um padrão que adotamos em nosso projeto (ver Figuras 1 e 2).
   - *Problema de Usabilidade Percebido:* A interface exige o preenchimento de uma carga cognitiva muito alta. O usuário é forçado a configurar múltiplas variáveis atmosféricas (temperatura, pressão, velocidade do vento) e dados balísticos complexos (Figura 3) antes de obter qualquer resultado prático na tela de retículo (Figura 4). Para o atirador iniciante ou focado em curtas distância, isso gera confusão e lentidão no estande.

2. Chairgun Elite
   - *Análise:* Muito popular entre atiradores de pressão (airguns). O sistema apresenta um longo menu de utilitários e um sistema de gerenciamento de equipamentos (presets de armas) que poupa o usuário de redigitar configurações recorrentes (Figuras 5 e 6).
   - *Problema de Usabilidade Percebido:* O fluxo de interação é excessivamente linear e baseado em formulários de texto (Figuras 7 e 8). O feedback numérico gerado nas tabelas é denso, exigindo que o atirador interprete os resultados e ainda tenha que fazer a aferição manual no alvo de papel.

3. Ballistic-X
   - *Análise:* Diferente dos anteriores, o Ballistic-X utiliza a câmera do dispositivo para ler os agrupamentos no alvo e calcular o tamanho do erro (Figuras 9 e 10), assemelhando-se parcialmente à proposta do nosso TCC.
   - *Problema de Usabilidade Percebido:* Embora use captura de imagem, o processo é altamente manual. O usuário precisa tirar a foto, arrastar réguas virtuais por cima da tela para definir a escala e marcar cada furo individualmente com o dedo. A usabilidade sofre em telas pequenas e exige tempo.

## Diferencial e Proposta Competitiva do Projeto
O sistema, Calibration Tool, se diferencia estrategicamente destes três concorrentes diretos. Enquanto o Lapua e o Chairgun exigem alta carga de entrada manual e o Ballistic-X exige manipulação prolongada da imagem na tela, o nosso sistema automatiza o processo via visão computacional em tempo real (OpenCV) conectada a uma câmera remota (smartphone).

Ao transferir a complexidade do cálculo para a máquina e focar a IHC apenas na confirmação de impacto e leitura de cliques, o projeto elimina a fadiga de cálculos manuais e o desperdício de tempo no estande, reduzindo drasticamente a curva de aprendizado exigida pelos sistemas tradicionais.

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
