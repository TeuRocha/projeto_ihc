# Avaliação de Usabilidade por Observação do Usuário

**Método:** Teste de Usabilidade com Observação Direta <br>
**Número de participantes:** 2 (1 por perfil de usuário identificado no projeto) <br>
**Avaliador:** Mateus Rocha

---

## 1. Fluxograma de Avaliação por Observação do Usuário

```
┌──────────────────────────────────────────────────────────────┐
│  PREPARAÇÃO                                                  │
│  • Definir objetivos e tarefas do teste                      │
│  • Preparar materiais: termo, tabela de observação           │
│  • Configurar ambiente: notebook, câmera IP, alvo ArUco      │
│  • Recrutar participantes (atirador experiente + iniciante)  │
│  • Realizar teste-piloto para verificar dependências         │
└──────────────────────────────────┬───────────────────────────┘
                                   │
                                   ▼
┌──────────────────────────────────────────────────────────────┐
│  RECEPÇÃO DO PARTICIPANTE                                    │
│  • Apresentar o avaliador e o ambiente                       │
│  • Explicar os objetivos do teste (avaliar o sistema,        │
│    não o usuário)                                            │
│  • Informar sobre os cuidados éticos                         │
│  • Entregar e coletar Termo de Consentimento                 │
│  • Aplicar Questionário de Perfil (pré-teste)                │
└──────────────────────────────────┬───────────────────────────┘
                                   │
                                   ▼
┌──────────────────────────────────────────────────────────────┐
│  SESSÃO DE OBSERVAÇÃO                                        │
│  • Apresentar o sistema brevemente (sem ensinar o uso)       │
│  • Participante executa as tarefas                           │
│  • Avaliador observa e registra: erros, acertos,             │
│     tempo por tarefa (sem interferir)                        │
└──────────────────────────────────┬───────────────────────────┘
                                   │
                                   ▼
┌──────────────────────────────────────────────────────────────┐
│  PÓS-TESTE                                                   │
│  • Esclarecer dúvidas observadas durante a sessão            │
│  • Coletar impressões livres do participante                 │
└──────────────────────────────────┬───────────────────────────┘
                                   │
                                   ▼
┌──────────────────────────────────────────────────────────────┐
│  ANÁLISE E CONSOLIDAÇÃO                                      │
│  • Transcrever anotações da tabela de observação             │
│  • Consolidar resultados dos dois participantes              │
│  • Identificar padrões e tendências comuns                   │
│  • Produzir relatório com conclusões e melhorias             │
└──────────────────────────────────────────────────────────────┘
```

---

## 2. Descrição do Procedimento de Preparação do Teste

**Passo 1 — Definição das tarefas**

As tarefas foram definidas com base no fluxo principal modelado no MOLIC e no CTT do projeto. Cada tarefa corresponde a uma etapa do ciclo de calibração:

- Tarefa 1: Criar uma conta e realizar login no sistema
- Tarefa 2: Configurar o ambiente — definir distância e cliques de calibração
- Tarefa 3: Posicionar o alvo e ajustar até a detecção dos marcadores ArUco
- Tarefa 4: Definir o Ponto de Mira (POA) clicando no alvo
- Tarefa 5: Salvar a imagem de referência
- Tarefa 6: Realizar o disparo e verificar o Ponto de Impacto (POI) detectado pelo sistema
- Tarefa 7: Consultar o feedback de correção e interpretar as instruções de ajuste
- Tarefa 8: Confirmar o acerto e encerrar a sessão de calibração

**Passo 2 — Perfil dos participantes recrutados**

| Critério | Participante 1 | Participante 2 |
| :--- | :--- | :--- |
| Perfil | Atirador experiente | Iniciante em tiro esportivo |
| Referência no projeto | Alessandra Pinheiro | Lucas Mendes |
| Familiaridade com lunetas | Alta | Baixa |
| Familiaridade com tecnologia | Moderada | Alta |
| Experiência com calibração | Sim (método tradicional) | Não |

**Passo 3 — Formulário de perfil do usuário (pré-teste)**

Aplicado antes da sessão, o formulário coletou:

- Nome e faixa etária
- Frequência de prática de tiro esportivo
- Experiência prévia com tecnologia para calibração
- Ferramentas que possui ou utiliza para calibração
- Nível de familiaridade com termos técnicos
- Média de munições gasta para calibrar um equipamento
- O objetivo principal ao utilizar um sistema de assistência à calibração
- Quais as tarefas mais desafiadoras durante o processo de calibração
- Tempo médio para realizar uma calibração completa
- Nível de erro cometido durante o processo

**Passo 4 — Preparação do ambiente físico**

- Notebook com o sistema em execução local
- Smartphone posicionado em tripé a aproximadamente 2-3 metros do alvo, configurado como câmera IP
- Alvo de papel com marcadores ArUco impressos nos quatro cantos, fixado de 10-20 metros
- Arma de fogo ou pressão disponível para o participante efetuar o disparo controlado
- EPIs disponíveis para todos os presentes (protetor auricular e óculos balísticos)

**Passo 5 — Teste-piloto**

Antes das sessões com os participantes reais, foi realizado um teste-piloto pelo próprio desenvolvedor para verificar: funcionamento do sistema no ambiente do estande, tempo médio de cada tarefa, clareza das instruções e adequação dos instrumentos de coleta.

---

## 3. Resultados do Teste

### Avaliação por Tarefa — Participante 1 (Atirador Experiente)

| Tarefa | Grau de Sucesso | Total de Erros | Tipos de Erros | Tempo Necessário | Grau de Satisfação |
| :--: | :--- | :--: | :--- | :--- | :--- |
| 1 — Login/Cadastro | Sucesso Total | 0 | — | ~1 min | Satisfeito |
| 2 — Definir Distância | Sucesso Total | 0 | — | ~30 s | Satisfeito |
| 3 — Preparar Alvo | Sucesso Total | 0 | — | ~1 min | Satisfeito |
| 4 — Definir POA | Sucesso Parcial | 1 | Demora para entender que precisa esperar a detecção ArUco | ~1 min | Confusão Moderada |
| 5 — Salvar Referência | Sucesso Total | 0 | — | ~20 s | Satisfeito |
| 6 — Verificar POI | Sucesso Total | 0 | — | ~3 min (inclui disparo) | Satisfeito |
| 7 — Consultar Feedback | Sucesso Total | 0 | — | ~30 s (inclui calibrar) | Muito Satisfeito |
| 8 — Confirmar Acerto | Sucesso Total | 0 | — | ~1 min (inclui disparo) | Muito Satisfeito |

### Avaliação por Tarefa — Participante 2 (Iniciante)

| Tarefa | Grau de Sucesso | Total de Erros | Tipos de Erros | Tempo Necessário | Grau de Satisfação |
| :--: | :--- | :--: | :--- | :--- | :--- |
| 1 — Login/Cadastro | Sucesso Total | 0 | — | ~30 s | Satisfeito |
| 2 — Definir Distância | Sucesso Total | 0 | — | ~1 min | Neutro |
| 3 — Preparar Alvo | Sucesso Total | 0 | - | ~30 s | Satisfeito |
| 4 — Definir POA | Sucesso Parcial | 2 | Hesitação sobre onde clicar | ~2 min | Neutro |
| 5 — Salvar Referência | Sucesso Total | 0 | — | ~30 s | Satisfeito |
| 6 — Verificar POI | Sucesso Total | 0 | — | ~4 min (inclui disparo) | Satisfeito |
| 7 — Consultar Feedback | Sucesso Total | 0 | — | ~1 min (inclui calibrar) | Muito Satisfeito |
| 8 — Confirmar Acerto | Sucesso Total | 0 | — | ~1 min (inclui disparo) | Muito Satisfeito |

---

### Respostas do Formulário de Perfil dos Usuários

**Participante:** Marcio Rocha
**Data:** 16/05/2026<br>

---

### 1. Quais destes jargões ou termos técnicos do tiro esportivo você está familiarizado?
(X) MOA (Minute of Angle)<br>
(X) MIL (Milirradianos)<br>
(X) Zeroing (Zeragem)<br>
(X) Trajetória Balística<br>
(X) Ajuste de Torre/Clicks<br>
(X) Paralaxe<br>
(X) Primeiro Plano Focal (FFP)<br>
(X) Segundo Plano Focal (SFP)<br>
( ) Nenhum

---

### 2. Você já utilizou algum software, aplicativo ou ferramenta digital especificamente para auxiliar em cálculos balísticos ou na calibração de miras?
( ) Sim, utilizo frequentemente<br>
(X) Sim, utilizei poucas vezes<br>
( ) Não, mas desejo acesso<br>
( ) Não, nunca utilizei<br>
( ) Não sabia que existia

---

### 3. Quais dispositivos ou ferramentas você possui e utiliza rotineiramente para auxiliar na calibração do seu equipamento?
( ) Computador/Notebook<br>
(X) Celular<br>
( ) Tablet<br>
( ) Calculadora balística<br>
(X) Binóculos<br>
( ) Nenhum desses

---

### 4. Com que frequência você pratica tiro esportivo (utilizando lunetas)?
( ) Diariamente<br>
(X) Semanalmente<br>
( ) Mensalmente<br>
( ) Raramente (Menos de uma vez por mês)<br>
( ) Não pratico, desejo começar

---

### 5. Qual o seu nível de conhecimento sobre o processo de calibração de lunetas?
( ) Básico (Sei apenas o essencial)<br>
( ) Intermediário (Consigo calibrar, mas com dificuldade ou incerteza)<br>
( ) Avançado (Calibro com precisão e compreendo os princípios)<br>
(X) Especialista (Consigo ensinar o processo a outros)

---

### 6. Em média, quantas munições você gasta para 'zerar' ou recalibrar uma luneta em um novo equipamento/distância?
Resposta: 10

---

### 7. Qual é o seu principal objetivo ao utilizar um sistema de assistência à calibração?
(X) Reduzir o tempo gasto com calibração<br>
( ) Reduzir a quantidade de munição desperdiçada<br>
( ) Aumentar a precisão e consistência dos disparos<br>
( ) Aprender a calibrar de forma mais eficaz<br>
( ) Outro

---

### 8. Em sua atividade de tiro esportivo, qual é a gravidade típica dos erros cometidos durante a calibração?
( ) 1 Erro Mínimo (Apenas ajusto)<br>
(X) 2<br>
( ) 3<br>
( ) 4<br>
( ) 5 Erro Crítico (Perda de tempo e dinheiro significativo)

---

### 9. Quanto tempo você leva, em média, para realizar o processo completo de calibração em campo (do início ao fim)?
00:30:00

---

### 10. Quais são as tarefas que você considera mais desafiadoras durante o processo de calibração?
(X) Cálculos de correção balística<br>
( ) Determinar o 'zero' ideal para diferentes distâncias<br>
( ) Ajustar as torres com precisão<br>
( ) Gerenciar fatores ambientais (vento, temperatura)<br>
( ) Verificação da precisão após o ajuste<br>
( ) Nenhuma dificuldade significativa

---

## 4. Conclusão da Avaliação por Observação do Usuário

Os testes de usabilidade com observação direta produziram resultados positivos para ambos os perfis de usuário avaliados. O fluxo completo de calibração foi concluído com sucesso por ambos os participantes, sem necessidade de intervenção do avaliador.

**Principais achados:**

O atirador experiente executou o fluxo com fluência e mínimo de erros, demonstrando que a interface atende bem ao público já familiarizado com o domínio de calibração de lunetas. O único ponto de confusão foi a espera pela detecção dos marcadores ArUco.

O iniciante completou todas as tarefas, porém com maior tempo na definição do POA (o participante não tinha certeza se deveria clicar em algum ponto específico inicialmente).

O ponto mais positivo destacado por ambos os participantes foi a etapa de feedback de correção: a apresentação do resultado em "cliques + direção" (ex.: "4 cliques para Direita | 7 cliques para Cima") foi considerada clara, direta e muito mais fácil de alcançar do que os métodos tradicionais com calculadora balística ou termos em MOA/MIL. Esse resultado valida a principal proposta de valor do sistema.

**Problema recorrente confirmado pelos dois participantes:**

A ausência de botão "Voltar" foi citada espontaneamente por ambos ao final da sessão. O atirador experiente mencionou: "Eu queria ter voltado para mudar o POA depois que vi como ficou, mas não tinha como." Esse achado confirma a gravidade 3 atribuída a essa violação na avaliação heurística e reforça a prioridade de implementação do botão "Voltar" em todas as etapas do fluxo.

**Impacto no reprojeto:**

Com base nos resultados consolidados de ambos os métodos de avaliação (inspeção heurística e observação de usuário), as melhorias prioritárias para o próximo ciclo de design são, em ordem de prioridade:

1. Implementar botão "Voltar" em todas as etapas do fluxo de calibração (gravidade 3, confirmado pelos dois participantes).
2. Implementar um botão de ajuda (ícone "?") fixo no header, alternativamente, adicionar tooltips de instrução contextual em cada etapa descrevendo brevemente o que o usuário deve fazer e por quê (gravidade 2, causa de hesitação no iniciante).
