# Esquema Conceitual de Signos

| Configuração de Calibração (C) \- dados para calcular a calibração no sistema|  |  |  |  |  |  |  |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| **signo** | **origem** | **observações** | **Tipo de conteúdo** | **restrição sobre conteúdo** | **valor default** | **prevenção** | **recuperação** |
| +Distância | Domínio | Distância real entre o atirador e o alvo para cálculo de MOA | Número decimal |  Não pode ser nulo ou negativo | 10,0 | PP: dica visual "(metros)", PA: Bloqueio de caracteres não númericos | RA: Mensagem de erro se o campo estiver vazio ao calcular |
| Tamanho do ArUco | Domínio | Medida real do lado do marcador impresso para escala de pixels | Número decimal | Deve ser um valor real em centímetros | 3,0 | PP: Instrução "Meça o marcador com um régua" | RA: Alerta se o valor inserido for discrepante da escala detectada |
| Status da Câmera | Aplicação | Indica se o sinal de vídeo do smartphone está ativo no PC | Estado (Texto/Ícone) | {Conectado, Desconectado} | Desconectado | PA: Desabilita botões de captura se o status for "Desconectado" | CE: Instrução "Verifique a conexão Wi-Fi ou IP do smartphone" |
| Ponto de Mira (POA) | Aplicação | Coordenada do centro do alvo definida pelo clique do usuário | Coordenada (x,y) | Deve estar dentro da área delimitada pelos ArUcos |  | PA: Impedir a fixação do ponto fora da área do alvo | RA: Opção "Redefinir POA" para novo clique se houver erro de marcação |
| Valor do Clique | Domínio Z Sensibilidade da luneta (ex: 1/4 MOA) para cálculo de correção | Seleção simples | {1/2, 1/4, 1/8} | 1/4 | PA: Seleção obrigatória através de menu dropdown |  |

