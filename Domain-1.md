# Domain 1: Fundamentos de IA e ML (AWS)

Este documento cobre os fundamentos de IA e ML aplicados no contexto da AWS, com foco em serviços, vantagens, desvantagens e casos de uso.  

---

## 1. Conceitos Fundamentais

- **IA (Inteligência Artificial):** capacidade de sistemas executarem tarefas normalmente atribuídas à inteligência humana.  
- **ML (Machine Learning):** subcampo da IA que cria modelos capazes de aprender padrões a partir de dados, sem programação explícita.  

### Tipos de Aprendizado
- **Supervisionado:** usa dados rotulados (classificação, regressão).  
- **Não-supervisionado:** descobre padrões sem rótulos (clustering, redução de dimensionalidade).  
- **Reforço:** agente aprende por tentativa/erro, recebendo recompensas ou penalidades.  

### Overfitting x Underfitting
- **Overfitting:** modelo aprende demais os dados de treino e não generaliza bem.  
- **Underfitting:** modelo simples demais, não captura os padrões.  

### Métricas
- **Classificação:** Accuracy, Precision, Recall, F1, ROC-AUC.  
- **Regressão:** MAE, MSE, RMSE, R².  
- **Clustering:** Silhouette Score, Davies–Bouldin.  

---

## 2. Ciclo de Vida de ML na AWS

### 2.1 Coleta e Armazenamento
- **Amazon S3:** armazenamento de dados brutos e artefatos de treino.  
  - **Vantagem:** escalabilidade, custo baixo, integração nativa com todos os serviços ML.  
  - **Desvantagem:** leitura massiva pode ter latência sem otimizações (partitioning, parquet, etc.).  

- **Amazon Kinesis / Firehose:** ingestão de dados em streaming.  

- **AWS Glue & Glue Data Catalog:** ETL e catálogo de metadados.  
  - **Vantagem:** serverless, integração com S3.  
  - **Desvantagem:** pode ser mais caro em cargas pesadas.  

---

### 2.2 Rotulagem
- **SageMaker Ground Truth:** cria datasets rotulados com workflows humanos ou semiautomáticos.  
  - **Vantagem:** reduz custo com rotulagem automática.  
  - **Desvantagem:** custo e tempo em datasets muito grandes.  

---

### 2.3 Preparação e Features
- **SageMaker Data Wrangler:** interface visual para limpar e transformar dados.  
- **SageMaker Processing:** processamento em lote de features.  
- **SageMaker Feature Store:** repositório centralizado para features usadas em treino e inferência.  
  - **Vantagem:** garante consistência entre treino e produção.  
  - **Desvantagem:** curva de aprendizado maior para equipes novas.  

---

### 2.4 Exploração e Notebooks
- **SageMaker Studio:** ambiente integrado com notebooks Jupyter, versionamento e experimentos.  
  - **Vantagem:** centraliza desenvolvimento, análise e treino.  

---

### 2.5 Treinamento
- **SageMaker Training Jobs:** execução de treinamentos em larga escala.  
  - Suporte para TensorFlow, PyTorch, Scikit-learn, XGBoost.  
- **SageMaker Built-in Algorithms:** algoritmos prontos otimizados pela AWS.  
- **SageMaker Automatic Model Tuning:** busca de hiperparâmetros automaticamente.  
- **SageMaker Debugger:** detecta problemas durante o treino em tempo real.  

  **Prós:** integração com GPUs, uso de spot instances para custo menor.  
  **Contras:** se não otimizar storage/instância, custos podem escalar rápido.  

---

### 2.6 Avaliação e Explainability
- **SageMaker Clarify:** detecta viés e gera explicabilidade (ex. SHAP).  
  - **Vantagem:** obrigatório em cenários regulatórios (justiça, compliance).  

---

### 2.7 Deploy e Inferência
- **SageMaker Endpoints:** deploy em tempo real.  
  - **Prós:** baixa latência.  
  - **Contras:** custo contínuo (mesmo sem uso).  

- **SageMaker Multi-Model Endpoints:** hospeda múltiplos modelos em um mesmo endpoint.  
- **SageMaker Asynchronous Inference:** para inferência em tarefas longas.  
- **SageMaker Batch Transform:** processamento em lote.  
- **SageMaker Neo:** compila e otimiza modelos para rodar em dispositivos IoT/edge.  

---

### 2.8 Monitoramento e MLOps
- **SageMaker Model Monitor:** detecta desvios de dados (data drift).  
- **SageMaker Pipelines:** orquestração CI/CD para ML.  
- **SageMaker Model Registry:** versionamento de modelos.  

- **Integrações AWS:**  
  - **CloudWatch:** monitoramento.  
  - **CloudTrail:** auditoria.  
  - **IAM:** controle de acesso.  
  - **KMS:** criptografia.  

---

## 3. Serviços de IA Pré-Treinados (Gerenciados)

- **Amazon Rekognition:** visão computacional (faces, objetos, cenas).  
  - **Quando usar:** projetos rápidos de visão.  
  - **Vantagem:** pronto, rápido, escalável.  
  - **Desvantagem:** pouca flexibilidade para casos muito específicos.  

- **Amazon Comprehend:** NLP (sentimento, extração de entidades, detecção de idioma).  
  - **Quando usar:** análise de texto rápida.  
  - **Desvantagem:** modelos limitados a tarefas pré-definidas.  

- **Amazon Polly:** conversão texto-fala (TTS).  
- **Amazon Lex:** construção de chatbots com NLP.  
- **Amazon Transcribe:** transcrição de áudio para texto.  
- **Amazon Translate:** tradução automática em tempo real.  

---

## 4. Serviços Adicionais Relevantes

- **SageMaker Autopilot:** AutoML para treinar modelos automaticamente.  
- **Amazon Athena:** consultas SQL diretamente no S3.  
- **Amazon Redshift:** Data Warehouse para análise massiva.  

---

## 5. Vantagens e Limitações Gerais

### Vantagens
- Integração completa entre serviços (S3, SageMaker, Glue, CloudWatch).  
- Ferramentas MLOps já disponíveis.  
- Serviços gerenciados aceleram prototipagem.  

### Limitações
- Custos podem crescer rápido em instâncias GPU e endpoints ativos.  
- Serviços pré-treinados têm pouca customização.  
- Arquitetura pode ser complexa (IAM, VPC, roles).  

---

## 6. Checklist para Prova

- Diferenças: **Endpoint vs Batch Transform vs Async Inference**.  
- Função de cada módulo: **Ground Truth, Data Wrangler, Feature Store, Clarify, Debugger, Model Monitor, Pipelines**.  
- Segurança: **IAM, KMS, VPC Endpoints**.  
- Custos: **spot instances, multi-model endpoints, auto-scaling**.  
- Métricas: **Precision, Recall, F1, RMSE**.  

---

## 7. Exemplo de Arquitetura (Fluxo Completo)

1. Dados brutos → **S3**  
2. ETL → **Glue**  
3. Rotulagem → **Ground Truth**  
4. Preparação → **Data Wrangler / Processing**  
5. Features → **Feature Store**  
6. Treino → **SageMaker Training** (com Debugger e Tuning)  
7. Avaliação → **Clarify**  
8. Deploy → **Endpoint** ou **Batch Transform**  
9. Monitoramento → **Model Monitor + CloudWatch**  
10. CI/CD → **SageMaker Pipelines + Model Registry**  

---

## 8. Dicas Práticas

- **Serviço pronto vs customizado:**  
  - Use **Rekognition/Comprehend/Polly** quando precisar de solução rápida.  
  - Use **SageMaker** quando precisar de controle total e customização.  

- **Custo:** prefira **Batch Transform** quando inferência não é em tempo real.  
- **Segurança:** sempre lembrar de roles IAM e KMS para criptografia.  

---
