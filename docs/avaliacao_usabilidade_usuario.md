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

### Links dos vídeos

- Sessão 1 (Atirador Experiente): `[link do vídeo]`

---

### Respostas do Formulário de Perfil dos Usuários



---

## 4. Conclusão da Avaliação por Observação do Usuário

Os testes de usabilidade com observação direta produziram resultados positivos para ambos os perfis de usuário avaliados. O fluxo completo de calibração foi concluído com sucesso por ambos os participantes, sem necessidade de intervenção do avaliador.

**Principais achados:**

O atirador experiente executou o fluxo com fluência e mínimo de erros, demonstrando que a interface atende bem ao público já familiarizado com o domínio de calibração de lunetas. O único ponto de confusão foi a espera pela detecção dos marcadores ArUco.

O iniciante completou todas as tarefas, porém com maior tempo na definição do POA (o participante não tinha certeza se deveria clicar em algum ponto específico inicialmente).

O ponto mais positivo destacado por ambos os participantes foi a etapa de feedback de correção: a apresentação do resultado em "cliques + direção" (ex.: "4 cliques para Direita \| 7 cliques para Cima") foi considerada clara, direta e muito mais fácil de alcançar do que os métodos tradicionais com calculadora balística ou termos em MOA/MIL. Esse resultado valida a principal proposta de valor do sistema.

**Problema recorrente confirmado pelos dois participantes:**

A ausência de botão "Voltar" foi citada espontaneamente por ambos ao final da sessão. O atirador experiente mencionou: "Eu queria ter voltado para mudar o POA depois que vi como ficou, mas não tinha como." Esse achado confirma a gravidade 3 atribuída a essa violação na avaliação heurística e reforça a prioridade de implementação do botão "Voltar" em todas as etapas do fluxo.

**Impacto no reprojeto:**

Com base nos resultados consolidados de ambos os métodos de avaliação (inspeção heurística e observação de usuário), as melhorias prioritárias para o próximo ciclo de design são, em ordem de prioridade:

1. Implementar botão "Voltar" em todas as etapas do fluxo de calibração (gravidade 3, confirmado pelos dois participantes)
2. Incluir tooltips com definição de POA e POI nas telas onde os termos aparecem (gravidade 2, causa de hesitação no iniciante)
