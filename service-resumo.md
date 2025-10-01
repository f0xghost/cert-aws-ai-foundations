# Guia de Serviços AWS para IA/ML – Resumo para Prova

Lista completa de serviços mencionados nos Domains 1-5, com explicações, cenários de uso, vantagens, desvantagens e uma frase para memorização.

---

### 1. Amazon SageMaker Studio
- **O que faz:** IDE integrada para desenvolvimento de ML (notebooks, experimentos, deploy).  
- **Quando usar:** Exploração de dados, testes de modelos, fine-tuning e experimentos.  
- **Vantagens:** Centraliza todo ciclo de ML, versionamento integrado, notebooks interativos.  
- **Desvantagens:** Requer configuração IAM/VPC; curva de aprendizado.  
- **Resumo:** "O hub completo de ML na AWS."

---

### 2. SageMaker Training Jobs
- **O que faz:** Treinamento de modelos customizados em instâncias gerenciadas.  
- **Quando usar:** Criar modelos próprios a partir de datasets internos.  
- **Vantagens:** Suporta frameworks populares (TensorFlow, PyTorch), uso de GPU.  
- **Desvantagens:** Custo alto dependendo do tempo/instâncias.  
- **Resumo:** "Treina seus modelos sem se preocupar com a infraestrutura."

---

### 3. SageMaker Pipelines
- **O que faz:** Orquestração de pipelines CI/CD para ML.  
- **Quando usar:** Automatizar treinamentos, deploy e monitoramento de modelos.  
- **Vantagens:** Integração total com SageMaker e serviços AWS.  
- **Desvantagens:** Inicialmente complexo de configurar.  
- **Resumo:** "Automatiza o fluxo completo do ML."

---

### 4. SageMaker Model Monitor
- **O que faz:** Monitora modelos em produção, detecta desvios de dados e performance.  
- **Quando usar:** Garantir confiabilidade de modelos após deploy.  
- **Vantagens:** Automático, integrado ao SageMaker.  
- **Desvantagens:** Funciona apenas com modelos implantados no SageMaker.  
- **Resumo:** "O vigia que protege a performance do modelo."

---

### 5. SageMaker JumpStart
- **O que faz:** Catálogo de modelos pré-treinados para ML e Generative AI.  
- **Quando usar:** Protótipos rápidos ou fine-tuning com modelos existentes.  
- **Vantagens:** Reduz tempo de desenvolvimento; fácil integração com Studio.  
- **Desvantagens:** Limitado aos modelos do catálogo.  
- **Resumo:** "Comece rápido com modelos prontos."

---

### 6. SageMaker Ground Truth
- **O que faz:** Rotulagem de dados para ML (imagens, texto, áudio).  
- **Quando usar:** Criar datasets anotados de forma semi-automatizada.  
- **Vantagens:** Otimiza tempo de rotulagem; suporte a múltiplos tipos de dados.  
- **Desvantagens:** Custo e tempo altos para datasets grandes.  
- **Resumo:** "O laboratório de rotulagem de dados."

---

### 7. SageMaker Clarify
- **O que faz:** Detecta e mitiga viés em dados e modelos ML.  
- **Quando usar:** Garantir fairness e conformidade ética.  
- **Vantagens:** Relatórios automáticos e integração com SageMaker.  
- **Desvantagens:** Limitado aos modelos suportados pelo SageMaker.  
- **Resumo:** "O detector de viés inteligente."

---

### 8. SageMaker Model Cards
- **O que faz:** Documentação de modelos (dados, métricas, limitações).  
- **Quando usar:** Auditoria, governança e transparência.  
- **Vantagens:** Facilita compliance; integrado ao SageMaker.  
- **Desvantagens:** Atualização manual necessária.  
- **Resumo:** "O cartão de identidade do modelo."

---

### 9. SageMaker Experiments
- **O que faz:** Rastreia experimentos, versões de modelos, hiperparâmetros e métricas.  
- **Quando usar:** Comparar treinamentos e selecionar melhores modelos.  
- **Vantagens:** Histórico completo, integração com Pipelines.  
- **Desvantagens:** Funciona apenas dentro do SageMaker.  
- **Resumo:** "O diário de bordo dos seus experimentos ML."

---

### 10. SageMaker Data Wrangler
- **O que faz:** Ferramenta visual para preparar, limpar e transformar dados.  
- **Quando usar:** Preparação de dados complexos para ML.  
- **Vantagens:** Interface intuitiva, integração direta com SageMaker e S3.  
- **Desvantagens:** Curva de aprendizado para transformações avançadas.  
- **Resumo:** "O assistente visual de preparação de dados."

---

### 11. SageMaker Processing
- **O que faz:** Processamento de dados em batch antes ou depois do treinamento.  
- **Quando usar:** Limpeza, transformação e feature engineering de datasets grandes.  
- **Vantagens:** Serverless, integrado a SageMaker.  
- **Desvantagens:** Requer configuração de recursos e jobs.  
- **Resumo:** "O motor de pré-processamento de dados."

---

### 12. SageMaker Feature Store
- **O que faz:** Armazena e gerencia features para ML.  
- **Quando usar:** Reaproveitar features entre múltiplos modelos e equipes.  
- **Vantagens:** Centraliza features, reduz inconsistências, integração com Pipelines.  
- **Desvantagens:** Curva de aprendizado e custo adicional.  
- **Resumo:** "O arquivo organizado de características do modelo."

---

### 13. SageMaker Debugger
- **O que faz:** Detecta erros, divergências e overfitting durante o treinamento.  
- **Quando usar:** Acompanhar saúde do treinamento em tempo real.  
- **Vantagens:** Diagnóstico automático, alertas em tempo real.  
- **Desvantagens:** Apenas para treinamentos no SageMaker.  
- **Resumo:** "O fiscal do treino do modelo."

---

### 14. SageMaker Batch Transform
- **O que faz:** Inferência em lote (batch) para datasets grandes.  
- **Quando usar:** Predições não em tempo real, com grandes volumes de dados.  
- **Vantagens:** Escalável, simples de usar.  
- **Desvantagens:** Não é para inferência em tempo real.  
- **Resumo:** "Inferência em massa sem pressa."

---

### 15. SageMaker Asynchronous Inference
- **O que faz:** Inferência assíncrona para modelos que demoram para responder.  
- **Quando usar:** Modelos pesados ou consultas longas.  
- **Vantagens:** Evita timeouts, escalável.  
- **Desvantagens:** Maior complexidade que endpoints síncronos.  
- **Resumo:** "Respostas longas sem travar sua aplicação."

---

### 16. Amazon Bedrock
- **O que faz:** Acesso gerenciado a Foundation Models de múltiplos provedores (LLMs e generative AI).  
- **Quando usar:** Aplicações com LLMs e IA generativa sem treinar do zero.  
- **Vantagens:** Rápido, escalável, sem infraestrutura própria.  
- **Desvantagens:** Pouco controle total sobre o treinamento.  
- **Resumo:** "Use grandes modelos sem levantar servidor."

---

### 17. Amazon Rekognition
- **O que faz:** Visão computacional (detecção de faces, objetos, cenas).  
- **Quando usar:** Análise de imagens e vídeos, segurança, detecção de objetos.  
- **Vantagens:** Escalável e pronto para uso.  
- **Desvantagens:** Pouca customização; limites em casos muito específicos.  
- **Resumo:** "Olhos artificiais da AWS."

---

### 18. Amazon Comprehend
- **O que faz:** NLP para análise de texto (sentimento, entidades, idioma).  
- **Quando usar:** Processamento de texto sem criar modelos próprios.  
- **Vantagens:** Fácil de usar, rápido para implementar.  
- **Desvantagens:** Flexibilidade limitada.  
- **Resumo:** "O tradutor e analista de textos automático."

---

### 19. Amazon Polly
- **O que faz:** Conversão de texto em fala (TTS).  
- **Quando usar:** Aplicações de voz, assistentes virtuais.  
- **Vantagens:** Pronto para produção, escalável.  
- **Desvantagens:** Customização de voz limitada.  
- **Resumo:** "Fala o que você escreve."

---

### 20. Amazon Lex
- **O que faz:** Chatbots com NLP integrado.  
- **Quando usar:** Assistentes conversacionais ou chatbots empresariais.  
- **Vantagens:** Integração com AWS, pronto para produção.  
- **Desvantagens:** Flexibilidade limitada em lógica complexa.  
- **Resumo:** "O cérebro do seu chatbot AWS."

---

### 21. Amazon Transcribe
- **O que faz:** Transcrição de áudio → texto.  
- **Quando usar:** Reuniões, áudios ou vídeos para análise ML ou registro.  
- **Vantagens:** Escalável, fácil de usar.  
- **Desvantagens:** Custo por minuto; precisão depende do áudio.  
- **Resumo:** "Transforma fala em texto automaticamente."

---

### 22. Amazon Translate
- **O que faz:** Tradução automática de textos.  
- **Quando usar:** Tradução multilíngue em aplicativos ou análise de dados.  
- **Vantagens:** Fácil de usar; suporta múltiplos idiomas.  
- **Desvantagens:** Qualidade limitada em contextos complexos.  
- **Resumo:** "O tradutor automático da AWS."

---

### 23. Amazon S3
- **O que faz:** Armazenamento escalável de dados e artefatos.  
- **Quando usar:** Datasets, modelos e resultados de ML.  
- **Vantagens:** Escalável, barato, durável.  
- **Desvantagens:** Latência se não otimizado.  
- **Resumo:** "O cofre de dados da AWS."

---

### 24. AWS Glue
- **O que faz:** ETL serverless para preparação de dados.  
- **Quando usar:** Transformação e limpeza de dados para ML.  
- **Vantagens:** Serverless, integração com S3 e SageMaker.  
- **Desvantagens:** Custo em grandes volumes; configuração necessária.  
- **Resumo:** "O liquidificador de dados."

---

### 25. Amazon OpenSearch Service
- **O que faz:** Indexação e busca de documentos e vetores (RAG).  
- **Quando usar:** Armazenar embeddings, busca semântica.  
- **Vantagens:** Rápido, escalável.  
- **Desvantagens:** Setup complexo; manutenção de cluster se auto-gerenciado.  
- **Resumo:** "A lupa que encontra dados rapidamente."

---

### 26. Amazon Neptune
- **O que faz:** Banco de grafos para consultas complexas.  
- **Quando usar:** Modelagem de relacionamentos e grafos em ML.  
- **Vantagens:** Performance para grafos, gerenciado.  
- **Desvantagens:** Curva de aprendizado em consultas complexas.  
- **Resumo:** "O cérebro conectado em grafos."

---

### 27. Amazon Aurora
- **O que faz:** Banco de dados relacional gerenciado.  
- **Quando usar:** Armazenamento de dados estruturados para ML ou aplicações.  
- **Vantagens:** Escalável, compatível com MySQL/PostgreSQL.  
- **Desvantagens:** Mais caro que S3; gerenciamento de schema necessário.  
- **Resumo:** "O guardião dos dados estruturados."

---

### 28. AWS Lambda
- **O que faz:** Computação serverless.  
- **Quando usar:** Orquestração de pipelines, chamadas a modelos e APIs.  
- **Vantagens:** Sem servidor, escalável automaticamente.  
- **Desvantagens:** Limite de timeout; restrição de memória.  
- **Resumo:** "Código que roda sem servidor."

---

### 29. Amazon API Gateway
- **O que faz:** Exposição de APIs RESTful.  
- **Quando usar:** Permitir que clientes acessem modelos ou pipelines.  
- **Vantagens:** Gerenciado, escalável, seguro.  
- **Desvantagens:** Limite de payload; configuração extra para throttling.  
- **Resumo:** "O portão de entrada das suas APIs."

---

### 30. AWS CloudWatch
- **O que faz:** Monitoramento e logs.  
- **Quando usar:** Observar métricas, logs e performance de aplicações ML.  
- **Vantagens:** Integrado AWS, alertas automáticos.  
- **Desvantagens:** Necessita configuração de dashboards e métricas.  
- **Resumo:** "Olhos e ouvidos da sua aplicação AWS."

---

### 31. AWS CloudTrail
- **O que faz:** Auditoria e rastreamento de ações AWS.  
- **Quando usar:** Compliance e investigação de alterações.  
- **Vantagens:** Histórico completo de eventos.  
- **Desvantagens:** Geração grande de logs; custo extra.  
- **Resumo:** "O diário de bordo da sua conta AWS."

---

### 32. Amazon Macie
- **O que faz:** Identificação de dados sensíveis.  
- **Quando usar:** Compliance, GDPR/LGPD, proteção de informações pessoais.  
- **Vantagens:** Automático, integrado ao S3.  
- **Desvantagens:** Custo adicional por volume de dados.  
- **Resumo:** "O detetive de dados confidenciais."

---

### 33. AWS PrivateLink
- **O que faz:** Conexão privada entre VPCs e serviços AWS.  
- **Quando usar:** Proteger endpoints de SageMaker ou outros serviços.  
- **Vantagens:** Rede privada, segura, isolada.  
- **Desvantagens:** Configuração inicial complexa.  
- **Resumo:** "O túnel seguro da AWS."

---

### 34. Amazon Inspector
- **O que faz:** Avaliação automatizada de vulnerabilidades e conformidade de segurança.  
- **Quando usar:** Verificar segurança de EC2, containers e workloads.  
- **Vantagens:** Automático, detalhado, fornece recomendações.  
- **Desvantagens:** Custo adicional; gera alertas que precisam de análise.  
- **Resumo:** "O fiscal de vulnerabilidades da AWS."

---

### 35. Amazon Kinesis
- **O que faz:** Streaming de dados em tempo real.  
- **Quando usar:** Ingestão contínua de logs, eventos ou dados de sensores.  
- **Vantagens:** Baixa latência, escalável.  
- **Desvantagens:** Curva de aprendizado; custos por throughput.  
- **Resumo:** "O fluxo constante de dados em tempo real."
