# Resumo - Estudo para Certificação AWS AI Foundations

## Introdução

Este material vem de anotações e estudos da minhas preparação para a certificação AWS AI Foundations. Vamos abordar todos os domínios, explicando os conceitos principais, técnicas, serviços da AWS.

---

## Domain 1: Fundamentals of AI and ML

### 1.1 Conceitos básicos de IA

- **IA (Inteligência Artificial):** Campo que permite a máquinas realizarem tarefas que normalmente requerem inteligência humana.
- **ML (Machine Learning):** Subcampo da IA que usa dados para "treinar" modelos a reconhecer padrões.
- **Deep Learning:** Técnica de ML usando redes neurais profundas.
- **Redes neurais:** Modelos inspirados no cérebro humano, que processam dados em camadas.
- **Visão computacional:** Processamento e interpretação de imagens por máquinas.
- **Processamento de linguagem natural (NLP):** Compreensão e geração de linguagem humana por máquinas.
- **Modelo:** Representação matemática que faz previsões ou decisões baseadas em dados.
- **Algoritmo:** Conjunto de regras para criar ou treinar modelos.
- **Treinamento:** Processo de ensinar o modelo com dados.
- **Inferência:** Usar o modelo treinado para fazer previsões.
- **Viés e justiça:** Problemas relacionados a dados ou modelos que causam decisões injustas.
- **Fit:** Ajuste do modelo aos dados (underfitting, overfitting).
- **Large Language Model (LLM):** Modelos de linguagem grandes, como GPT, capazes de gerar texto.

### Diferenças entre IA, ML e Deep Learning

- IA é o guarda-chuva geral.
- ML são técnicas dentro da IA que aprendem com dados.
- Deep Learning é uma técnica de ML baseada em redes neurais profundas.

### Tipos de inferência

- **Batch:** Processa muitos dados de uma vez, geralmente offline.
- **Tempo real (real-time):** Responde imediatamente a cada requisição.

### Tipos de dados para IA

- **Rotulados:** Dados com respostas conhecidas (exemplo: imagens marcadas).
- **Não rotulados:** Dados sem resposta conhecida.
- **Tabular, série temporal, texto, imagem, estruturado, não estruturado.**

### Tipos de aprendizado

- **Supervisionado:** Treina com dados rotulados.
- **Não supervisionado:** Descobre padrões em dados não rotulados.
- **Reforço:** Aprende com feedback em forma de recompensa.

---

### 1.2 Casos práticos de IA

- IA é ótima para ajudar decisões, escalar soluções e automatizar tarefas.
- Não usar IA quando custo-benefício é ruim ou resultado exato é necessário.
- Técnicas comuns:
  - **Regressão:** prever valores contínuos.
  - **Classificação:** categorizar dados.
  - **Clustering:** agrupar dados similares sem rótulos.
- Exemplos: visão computacional, NLP, reconhecimento de fala, sistemas de recomendação, detecção de fraudes, previsão.
- AWS tem serviços gerenciados: SageMaker, Transcribe, Translate, Comprehend, Lex, Polly.

---

### 1.3 Ciclo de vida do ML

- Componentes:
  - Coleta de dados
  - Análise exploratória (EDA)
  - Pré-processamento e engenharia de atributos
  - Treinamento de modelo
  - Ajuste de hiperparâmetros
  - Avaliação
  - Deploy
  - Monitoramento
- Fontes de modelos:
  - Open source pré-treinados
  - Modelos customizados
- Métodos para produção:
  - API gerenciada (ex: SageMaker Endpoint)
  - API auto-hospedada
- Serviços AWS por etapa:
  - SageMaker Data Wrangler, Feature Store, Model Monitor
- Conceitos de MLOps:
  - Experimentação, processos repetíveis, escalabilidade, controle da dívida técnica, monitoramento e re-treinamento.
- Métricas importantes:
  - Performance: accuracy, AUC, F1 score
  - Negócios: custo por usuário, feedback, ROI

---

## Domain 2: Fundamentals of Generative AI

### 2.1 Conceitos básicos

- **Tokens:** Pedaços de texto que o modelo processa.
- **Chunking:** Divisão de texto para processamento.
- **Embeddings:** Representação numérica de palavras ou frases.
- **Vetores:** Dados numéricos para representar informações.
- **Prompt engineering:** Técnicas para criar comandos que geram melhores respostas.
- **Transformers:** Arquitetura base dos LLMs.
- **Foundation Models (FM):** Modelos grandes pré-treinados em múltiplos domínios.
- **Multi-modal:** Modelos que trabalham com texto, imagem, áudio juntos.
- **Diffusion models:** Modelos usados para gerar imagens (ex: DALL·E).

### Casos de uso

- Geração de imagem, vídeo e áudio.
- Resumos.
- Chatbots.
- Tradução.
- Geração de código.
- Atendimento ao cliente.
- Pesquisa e recomendação.

### Ciclo de vida de Foundation Models

- Seleção de dados
- Seleção do modelo
- Pré-treinamento
- Fine-tuning
- Avaliação
- Deploy
- Feedback contínuo

---

### 2.2 Capacidades e limitações

- **Vantagens:**
  - Adaptabilidade
  - Rapidez na geração de conteúdo
  - Simplicidade de uso
- **Desvantagens:**
  - Alucinações (informação incorreta gerada)
  - Dificuldade de interpretar decisões do modelo
  - Inconsistências e respostas não determinísticas
- Escolha do modelo considerando desempenho, restrições, compliance.
- Medir valor com métricas como conversão, receita média, engajamento.

---

### 2.3 Infraestrutura AWS para IA generativa

- Serviços: Amazon SageMaker JumpStart, Amazon Bedrock, PartyRock (playground Bedrock), Amazon Q
- Vantagens AWS: acessibilidade, rapidez para colocar no mercado, custo-benefício, segurança, compliance.
- Considerar trade-offs: latência, disponibilidade, custo por token, throughput, cobertura regional.

---

## Domain 3: Applications of Foundation Models

### 3.1 Considerações de design

- Critérios para escolher FM:
  - Custo, modalidade (texto/imagem), latência, suporte a idiomas, tamanho, complexidade, customização, tamanho de entrada/saída.
- Parâmetros de inferência que influenciam resposta:
  - Temperatura (criatividade)
  - Tamanho da entrada e saída
- RAG (Retrieval Augmented Generation): técnica que junta modelo generativo com busca em bases de conhecimento.
- Serviços para armazenar embeddings:
  - OpenSearch, Aurora, Neptune, DocumentDB, RDS PostgreSQL
- Trade-offs em personalização:
  - Pré-treinamento, fine-tuning, few-shot learning, RAG
- Agentes para tarefas multi-step (ex: Agents for Amazon Bedrock)

---

### 3.2 Engenharia de prompts

- Elementos:
  - Contexto, instrução, prompts negativos
  - Espaço latente do modelo
- Técnicas:
  - Chain-of-thought (explicação passo a passo)
  - Zero-shot (sem exemplos)
  - Single-shot (um exemplo)
  - Few-shot (poucos exemplos)
  - Templates de prompt
- Benefícios:
  - Melhor qualidade da resposta
  - Guardrails para evitar respostas erradas
  - Experimentação para achar o melhor prompt
- Riscos:
  - Exposição indevida de dados
  - Envenenamento, hijacking, jailbreaking do modelo

---

### 3.3 Treinamento e fine-tuning

- Etapas do treinamento:
  - Pré-treinamento (treino inicial com grandes dados)
  - Fine-tuning (ajuste com dados específicos)
  - Continuous pre-training (treino contínuo para manter atualizações)
- Métodos de fine-tuning:
  - Instruction tuning
  - Adaptação para domínio específico
  - Transfer learning
  - Reinforcement Learning from Human Feedback (RLHF)
- Preparação dos dados:
  - Curadoria e governança
  - Tamanho e rotulagem adequada
  - Representatividade dos dados

---

### 3.4 Avaliação do desempenho

- Métodos:
  - Avaliação humana
  - Benchmarks públicos
- Métricas:
  - ROUGE (para resumos)
  - BLEU (para tradução)
  - BERTScore (similaridade semântica)
- Avaliar impacto nos objetivos de negócio:
  - Produtividade, engajamento, qualidade da tarefa

---

## Domain 4: Guidelines for Responsible AI

### 4.1 Desenvolvimento responsável

- Características:
  - Viés e justiça
  - Inclusividade
  - Robustez e segurança
  - Veracidade e transparência
- Ferramentas para identificar:
  - Guardrails para Amazon Bedrock
- Práticas:
  - Seleção sustentável de modelos
- Riscos legais:
  - Direitos autorais, saída tendenciosa, perda de confiança, alucinações
- Características dos datasets:
  - Inclusivos, diversos, balanceados
- Impacto de viés e variância:
  - Afeta grupos demográficos, causa overfitting/underfitting
- Ferramentas para monitoramento:
  - SageMaker Clarify, Model Monitor, Amazon A2I

---

### 4.2 Transparência e explicabilidade

- Modelos transparentes são entendíveis por humanos.
- Explicabilidade ajuda a entender decisões complexas.
- Ferramentas:
  - SageMaker Model Cards
- Trade-offs entre segurança e transparência.
- Design centrado no usuário para IA explicável.

---

## Domain 5: Security, Compliance
