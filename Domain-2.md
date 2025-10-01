# Domain 2: Fundamentos de Generative AI (AWS)

Este documento cobre os conceitos, serviços e boas práticas relacionados a **IA Generativa** na AWS.  

---

## 1. Conceitos Fundamentais de Generative AI

- **IA Generativa:** cria novos conteúdos (texto, imagens, áudio, código) a partir de dados de treino.  
- Baseada em **Foundation Models (FMs):** modelos de larga escala treinados em datasets massivos (ex: GPT, Claude, Stable Diffusion, BERT).  

### Características principais:
- **Generalização:** aplicável a diversas tarefas com pouco ou nenhum fine-tuning.  
- **Zero-shot / Few-shot:** responde corretamente mesmo com pouco contexto ou exemplos.  
- **Multimodalidade:** pode combinar texto, imagem e áudio.  

---

## 2. Serviços AWS para Generative AI

### 2.1 Amazon Bedrock
- **O que é:** plataforma que permite acesso via API a Foundation Models de provedores como Anthropic, AI21, Stability AI e Amazon Titan.  
- **Quando usar:** quando você quer usar LLMs e modelos generativos **sem precisar treinar do zero** ou gerenciar clusters de GPU.  
- **Vantagem:** não precisa gerenciar infraestrutura, suporte multi-modelo, escalabilidade automática.  
- **Desvantagem:** menos controle sobre o treinamento (não indicado para cenários que exigem customização completa).  

---

### 2.2 Amazon SageMaker JumpStart
- **O que é:** catálogo dentro do SageMaker com modelos pré-treinados para NLP, visão, tradução e geração de texto.  
- **Quando usar:** quando precisar testar ou fazer fine-tuning rápido de um modelo já pronto.  
- **Vantagem:** integração com SageMaker Studio, rápido para prototipagem.  
- **Desvantagem:** nem sempre oferece os modelos mais novos comparado ao Bedrock.  

---

### 2.3 Amazon SageMaker Studio
- **O que é:** ambiente de notebooks para desenvolvimento, experimentação e ajuste de modelos.  
- **Quando usar:** quando você precisa experimentar prompts, fazer EDA, treinar ou ajustar modelos.  
- **Vantagem:** centraliza todo o ciclo de ML (treino, deploy, monitoramento).  
- **Desvantagem:** exige configuração e permissões corretas (IAM, VPC).  

---

## 3. Capacidades e Limitações da Generative AI

### 3.1 Capacidades
- Geração de texto coerente (resumo, tradução, Q&A, assistentes virtuais).  
- Geração de imagens com **Diffusion Models** (ex: via Stability AI no Bedrock).  
- Multi-modalidade (texto + imagem + áudio).  
- Suporte para casos empresariais: chatbots, geração de documentos, prototipagem de código.  

### 3.2 Limitações
- **Alucinações:** modelos podem inventar informações falsas.  
- **Latência:** tempo de resposta pode ser maior em modelos grandes.  
- **Custo:** varia conforme número de tokens processados (entrada + saída).  
- **Privacidade:** dados enviados ao modelo podem ser usados para treino (depende do provedor).  

---

## 4. Infraestrutura AWS para Generative AI

Um stack típico para aplicações de IA generativa na AWS pode incluir:

- **Amazon Bedrock:** consumo direto de FMs sem gerenciar infraestrutura.  
- **Amazon SageMaker:** fine-tuning, customização e deploy de modelos próprios.  
- **Amazon S3:** armazenamento de dados e resultados gerados.  
- **AWS Glue:** ETL e preparação de dados para treino.  
- **AWS Lambda:** orquestração de chamadas, manipulação de prompts e resultados.  
- **Amazon API Gateway:** exposição da aplicação como API REST.  
- **Amazon CloudWatch:** monitoramento, métricas e logs.  
- **Amazon KMS + IAM:** segurança e criptografia de dados.  

---

## 5. Comparativo rápido: Bedrock vs SageMaker

| Aspecto | Amazon Bedrock | Amazon SageMaker |
|---------|----------------|------------------|
| **Abordagem** | Consumo de modelos prontos via API | Treinamento e customização de modelos |
| **Infraestrutura** | Gerenciada pela AWS (sem clusters GPU) | Você gerencia instâncias, tuning, datasets |
| **Customização** | Baixa (prompt engineering, RAG) | Alta (fine-tuning, modelos próprios) |
| **Uso típico** | Aplicações rápidas com LLMs e geração de conteúdo | Pesquisas, custom models, MLOps |
| **Custo** | Por tokens consumidos (entrada + saída) | Por hora/instância usada no treino e deploy |

---

## 6. Checklist para Prova

- Diferença entre **Amazon Bedrock** e **SageMaker** (pronto vs custom).  
- Quando usar **JumpStart** (modelos prontos dentro do SageMaker).  
- Limitações da Generative AI (alucinação, latência, custo por token).  
- Stack de serviços para expor um modelo generativo (S3 + Lambda + API Gateway + CloudWatch).  
- Entender **multimodalidade** e casos de uso (texto, imagem, áudio).  

---

## 7. Exemplo de Arquitetura (App Generative AI)

1. Usuário → front-end web/chatbot.  
2. API Gateway → recebe request.  
3. Lambda → prepara prompt + envia para **Bedrock**.  
4. Bedrock → processa e retorna resposta do modelo (texto, imagem, etc.).  
5. Lambda → pós-processa resposta e grava em **S3**.  
6. CloudWatch → monitora logs e métricas.  

---

## 8. Dicas de Estudo

- **Memorize:** Amazon Bedrock = consumo de LLMs e FMs via API sem infraestrutura.  
- **SageMaker JumpStart:** use para testar e refinar modelos já prontos.  
- **SageMaker Studio:** ambiente para experimento e ajuste de modelos.  
- **Cenários comuns em prova:**  
  - “Qual serviço usar para acessar modelos generativos de terceiros sem treinar?” → **Bedrock**.  
  - “Qual usar para ajustar um modelo próprio de NLP?” → **SageMaker**.  

---
