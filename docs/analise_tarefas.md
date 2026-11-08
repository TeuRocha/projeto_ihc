# Análise de Tarefas

# HTA

<img width="1941" height="582" alt="htafinal drawio" src="https://github.com/user-attachments/assets/b49bbbe2-2063-4d54-8193-2d70f1a2abdc" />

## Objetivos/Operações

0.	Calibrar mira 1 > 2 > 3 > 4

1.  Identificar usuário 1.1/1.2
- 1.1.	Cadastrar usuário 1.1.1 > 1.1.2
- 1.2.	Login no sistema inserindo credenciais
- 1.1.1.  Informar dados do usuário 1.1.1.1 + 1.1.1.2 + 1.1.1.3
- 1.1.2.	Login no sistema inserindo credenciais
- 1.1.1.1.	Informar nome	
- 1.1.1.2.	Informar e-mail
- 1.1.1.3.  Criar senha e confirmar senha

2.  Configurar ambiente 2.1 + 2.2
- 2.1.	Colocar alvo com marcadores ArUco
- 2.2.	Configurar setup de calibração 2.2.1 + 2.2.2
- 2.2.1. Definir distância
- 2.2.2. Definir valor do clique

3.	Executar ciclo de calibração 3.1 > 3.2 > 3.3 >3.4 > 3.5
- 3.1.	Definir ponto de mira (POA) no sistema
- 3.2. Salvar imagem de referência
- 3.3.	Efetuar disparo 3.3.1 > 3.3.2 > 3.3.3
- 3.4. Confirmar ponto de impacto (POI) no sistema
- 3.5.	Retornar feedback
- 3.3.1. Distanciar o alvo da câmera
- 3.3.2. Realizar disparo com equipamento não calibrado
- 3.3.3. Reaproximar o alvo da câmera

4.	Confirmar correção 4.1 > 4.2 > 4.3
- 4.1.  Calibrar mira
- 4.2.	Efetuar disparo corrigido
- 4.3.	Validar acerto

## Problemas e Recomendações

0. Input: identificação do atirador e dados do ambiente de tiro

	Feedback: confirmação visual da calibração com base no acerto ao alvo definido

	Plano: identificar usuário e depois configurar ambiente e depois executar ciclo de calibração e depois o usuário confirmar correção

	Recomendação: definir o POI como o centro do alvo

1. Plano: cadastrar usuário ou confirmar login no sistema inserindo credenciais do usuário

	1.1. Plano: preencher *nome, *e-mail, *senha, *confirmar senha e confirmar cadastro
   
   	Problema: dados inválidos ou senhas não coincidem
   
	Recomendação: validar campos em tempo real (inline) antes do envio

	1.2. Plano: preencher *usuário e *senha e confirmar login

	Problema: credenciais incorretas ou cadastro inexistente

	Recomendação: diferenciar as mensagens de erro — indicar se o problema é na senha ou se o usuário não existe

	1.1.1. Plano: informar e-mail e criar senha e confirmar senha

	1.1.2. Recomendação: alertar usuário sobre a confirmação
   
2. Plano: preparar alvo e definir setup de calibração

	2.2. Plano: definir valor numérico da distância em metros e definir valor do clique
	
	Problema: valor inválido inserido para calibração

	Recomendação: especificar no campo a faixa de valores aceitos além do placeholder

	2.2.1. Ação: Definir distância em metros

   	2.2.2. Ação: Definir valor do clique
	
3. Plano: definir POA no sistema e depois salvar referência e depois efetuar disparo e depois confirmar POI e depois retornar feedback de correção

	3.1. Plano: Clique do usuário dentro do bloco verde para definir o POA

   	Problema: clique fora da área delimitada pelo bloco verde

    Recomendação 1: ampliar o destaque visual do bloco verde e indicar cursor ativo somente sobre a área válida

	Recomendação 2: definir POI em partes limpas do alvo (com menor ocorrência de furos)

	3.2. Ação: clicar no botão "Salvar referência"
   
	Problema: falha ao salvar a imagem (câmera instável ou alvo fora de posição)
	
	Recomendação: exibir pré-visualização da imagem capturada antes de confirmar o salvamento

	3.3. Ação: efetuar disparo teste, distanciar e reaproximar o alvo da câmera
   
	Recomendação: exibir instruções claras e sequenciadas na tela para guiar o usuário nessa etapa externa

	3.4. Interação: confirmar POI sinalizado na imagem via botões "sim" / "não"
   
	Problema: Falhas — ruído de iluminação, detecção muito pequena, nenhum impacto detectado

	Recomendação: para cada tipo de falha, exibir orientação específica de correção

	3.5. Plano: sistema exibe cálculo de cliques por direção
   
	Problema: valor discrepante do habitual detectado pelo sistema

	Recomendação: destacar visualmente o alerta de valor discrepante e sugerir que o usuário repita o disparo

4. Ação: confirmar correção cedida pelo sistema

	Plano: efetuar disparo corrigido e depois usuário confirmar acerto

	4.1. Ação: corrigir as torres da mira conforme o feedback recebido

	4.2. Ação: efetuar disparo visando o POA

	4.3. Ação: confirmar acerto com "sim" retornando ao menu principal

   	Problema: Calibração falhou em acertar alvo retorna para "Definir POA"

   	Recomendação 1: ao retornar para "Definir POA", manter a distância já configurada para evitar reinício completo

   	Recomendação 2: possibilitar alteraração da distância definida para deixar na decisão do usuário após erro

# GOMS

## Modelo GOMS: Calibração de Mira Inteligente

GOAL 0: Calibrar mira
- GOAL 1: Identificar usuário
  - METHOD 1.A: Cadastrar novo usuário
  - (SEL. RULE: usuário não possui conta no sistema)
    - OP. 1.A.1: Digitar e-mail no campo de cadastro
    - OP. 1.A.2: Digitar nova senha
    - OP. 1.A.3: Confirmar senha
    - OP. 1.A.4: Clicar no botão "Cadastrar"
  - METHOD 1.B: Fazer login
  - (SEL. RULE: usuário já possui conta cadastrada) 
	- OP. 1.B.1: Inserir credenciais (e-mail e senha) 
	- OP. 1.B.2: Clicar no botão "Entrar"
- GOAL 2: Configurar ambiente 
	- OP. 2.1: Posicionar fisicamente o alvo com marcadores na distância planejada
	- METHOD 2.A: Selecionar distância via scroll do mouse
 	- (SEL. RULE: Se o usuário prefere utilizar apenas o mouse)
	  - OP. 2.A.1: Arrastar scroll do mouse
	- METHOD 2.B: Digitar distância manualmente
 	- (SEL. RULE: só será aceito um valor positivo)
      - OP. 2.B.1: Clicar no campo distância
	  - OP. 2.B.2: Digitar o valor numérico
   - OP. 2.2: Definir valor do clique (MOA)
- GOAL 3: Executar ciclo de calibração
  	- OP. 3.1: Visualizar imagem em tempo real da câmera e aguardar status positivo de detecção dos ArUcos
	- OP. 3.2: Clicar dentro do bloco verde na imagem para definir o Ponto de Mira (POA)
   	- OP. 3.3: Verificar confirmação "Sucesso, POA definido: '[ponto]' cm."
   	- OP. 3.4: Clicar no botão "Salvar frame"
   	- OP. 3.5: Distanciar o alvo para distância definida
	- OP. 3.6: Efetuar o disparo físico com a arma
   	- OP. 3.7: Reaproximar o alvo da câmera após disparo
   	- OP. 3.8: Confirmar se o POI sinalizado está correto clicando em "Confirmar, POI" ou "Não, ignorar"
	- OP. 3.9: Ler o feedback de correção exibido pelo sistema 
- GOAL 4: Confirmar correção
  	- OP. 4.1: Calibrar equipamento 
	- OP. 4.2: Realizar disparo utilizando o ajuste sugerido pelo sistema 
	- OP. 4.3: Visualizar o acerto no alvo e validar a precisão
  	- METHOD 4.A: Confirmar calibração bem-sucedida
  	- (SEL. RULE: acerto visual confirmado pelo usuário)
  	  - OP 4.A.1: Clicar em "Concluir e salvar" retornando sistema ao menu principal
  	  - GOAL 4.A.2.: Calibrar outro equipamento se houver
  	    - OP. 4.A.2.1: Selecionar opção "nova calibração" no menu principal
	- METHOD 4.B: Novo disparo (manter POA)(Reiniciar ciclo de calibração)
 	- (SEL. RULE: acerto não confirmado após correção das torres)
      - OP. 4.B.1: Clicar em "Novo disparo (manter POA)"
      - OP. 4.B.2: Retornar ao OP.3.4

# CTT

<img width="1505" height="502" alt="cttfinal drawio" src="https://github.com/user-attachments/assets/5d9ae413-d7f4-49f4-a18f-5a65b861e5dc" />
