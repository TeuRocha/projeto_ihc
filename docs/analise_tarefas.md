# Análise de Tarefas

# HTA

![hta](docs\images\hta.png)

## Objetivos/Operações

0.	Calibrar luneta 1 > 2 > 3 > 4

1.  Identificar usuário 1.1/1.2
- 1.1.	Cadastrar usuário 1.1.1 > 1.1.2
- 1.2.	Login no sistema inserindo credenciais
- 1.1.1.  Informar dados do usuário 1.1.1.1 + 1.1.1.2
- 1.1.2.	Enviar msg confirmando o cadastramento
- 1.1.1.1.	Informar e-mail	
- 1.1.1.2.	Criar senha

2.  Configurar ambiente 2.1 + 2.2
- 2.1.	Colocar alvo
- 2.2.	Definir distância

3.	Executar ciclo de calibração 3.1 > 3.2 > 3.3
- 3.1.	Definir ponto de impacto (POI) no sistema
- 3.2.	Efetuar disparo
- 3.3.	Receber feedback de correção

4.	Confirmar correção 4.1 > 4.2
- 4.1.	Efetuar disparo corrigido
- 4.2.	Visualizar acerto

## Problemas e Recomendações

0. Input: identificação do atirador e dados do ambiente de tiro

	Feedback: confirmação visual da calibração com base no acerto ao alvo definido

	Plano: identificar usuário e depois configurar ambiente e depois executar ciclo de calibração e depois o usuário confirmar correção

	Recomendação: definir o POI como o centro do alvo
1. Plano: cadastrar usuário ou confirmar login no sistema inserindo credenciais do usuário

	1.1. Plano: informar dados do usuário e depois enviar msg confirmando o cadastramento

	1.1.1. Plano: informar e-mail e criar senha

	1.1.2. Recomendação: alertar usuário sobre a confirmação
2. Plano: colocar alvo e definir distância

	2.2. Input: valor numérico da distância (em metros)
	
	Recomendação: oferecer distâncias pré-definidas (ex: 10m, 20m, 25m)
3. Plano: definir POI no sistema e depois efetuar disparo e depois o usuário receber feedback de correção

	3.1. Input: clique do POI na tela do sistema

	Recomendação: definir POI em partes limpas do alvo (com menor ocorrência de furos)
4. Ação: avaliar correção cedida pelo sistema na hora

	Plano: efetuar disparo corrigido e depois usuário visualizar acerto

	4.1. Ação: efetuar disparo visando POI

	4.2. Recomendação 1: confirmar a definição da configuração do ambiente

	Recomendação 2: caso tenha erro na correção retorne para o ciclo de calibração

# GOMS

## Modelo GOMS: Calibração de Mira Inteligente

GOAL 0: Calibrar luneta
- GOAL 1: Identificar usuário
  - METHOD 1.A: Cadastrar novo usuário (SEL. RULE: usuário não possui conta no sistema)
    - OP. 1.A.1: Digitar e-mail no campo de cadastro
    - OP. 1.A.2: Digitar nova senha
    - OP. 1.A.3: Clicar no botão "Cadastrar"
    - OP. 1.A.4: Verificar recebimento de mensagem de confirmação
  - METHOD 1.B: Fazer login (SEL. RULE: usuário já possui conta cadastrada) 
	- OP. 1.B.1: Inserir credenciais (e-mail e senha) 
	- OP. 1.B.2: Clicar no botão "Entrar" 
- GOAL 2: Configurar ambiente 
	- OP. 2.1: Posicionar alvo fisicamente no local de tiro 
	- METHOD 2.A: Selecionar distância pré-definida (SEL. RULE: distância é um valor padrão como 10m ou 20m)
	  - OP. 2.A.1: Clicar na opção de distância pré-definida deseja
	- METHOD 2.B: Digitar distância desejada (SEL. RULE: só será aceito um valor padrão de 5m a 25m)
	  - OP. 2.B.1: Digitar a distância desejada
- GOAL 3: Executar ciclo de calibração 
	- OP. 3.1: Clicar na tela para definir o Ponto de Impacto (POI) 
	- OP. 3.2: Efetuar o disparo físico com a arma 
	- OP. 3.3: Ler o feedback de correção exibido pelo sistema 
- GOAL 4: Confirmar correção 
	- OP. 4.1: Realizar disparo utilizando o ajuste sugerido pelo sistema 
	- OP. 4.2: Visualizar o acerto no alvo e validar a precisão 
	- GOAL 4.1: Verificar configuração de ambiente 
	  - OP. 4.1.1: Verificar configuração de ambiente definida
	- GOAL 4.2: Reiniciar ciclo de calibração 
	  - OP. 4.2.1: Executar ciclo de calibração novamente

# CTT

![ctt](docs\images\ctt.png)