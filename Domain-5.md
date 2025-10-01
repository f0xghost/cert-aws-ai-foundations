# Domain 5: Security, Compliance, and Governance

## 5.1 Segurança na AWS para IA

### Controle de Acesso
- **IAM (Identity and Access Management):** gerenciamento granular de permissões e roles para usuários e serviços.  
- **Roles e Políticas Restritivas:** limitar quem pode acessar datasets, modelos e endpoints.  

### Proteção de Dados
- **Amazon S3:** armazenamento criptografado para datasets e artefatos.  
- **Criptografia em trânsito:** TLS para proteger dados entre serviços e clientes.  
- **Amazon Macie:** identifica e classifica dados sensíveis automaticamente.  

### Segurança de Aplicações
- **SageMaker Endpoints:** proteja via VPC, Security Groups e PrivateLink para conexões privadas.  
- **Amazon Inspector:** análise automatizada de vulnerabilidades e práticas de segurança em instâncias EC2 e workloads, detectando riscos de configuração e segurança.  
- **Monitoramento de ataques adversariais:** como **prompt injection**, usando CloudWatch e práticas de validação.  

---

## 5.2 Compliance e Governança

- **Auditoria e Monitoramento:** CloudTrail e CloudWatch para rastrear alterações e uso dos serviços.  
- **Políticas de Governança:** controle de dados sensíveis, segregação de funções, processos de aprovação.  
- **Conformidade Legal:** GDPR, LGPD e regulamentações específicas de setores (saúde, financeiro, etc.).  

---

## 5.3 Boas Práticas para Prova

- Diferencie **serviços gerenciados** (Comprehend, Rekognition) de **customizados** (SageMaker).  
- Entenda o **ciclo de vida ML** e onde cada serviço se encaixa.  
- Pratique **engenharia de prompts** e conheça limitações das LLMs.  
- Estude **MLOps** na AWS: Pipelines, Monitoramento, Experimentos.  
- Conheça as ferramentas para **controle de viés e segurança** (Clarify, Model Cards, Guardrails).  
- Avalie **trade-offs**: custo, latência, flexibilidade (Bedrock vs SageMaker).  
- Armazenamento para embeddings e dados: S3, OpenSearch, Aurora, Neptune.  
- Diferencie **inferência batch** vs tempo real e quando usar cada uma.  
- Faça perguntas baseadas em cenários reais para fixar conceitos.  

---

## 5.4 Resumo dos Serviços Citados

| Serviço | Função | Quando Usar | Vantagens | Desvantagens |
|---------|--------|-------------|-----------|-------------|
| IAM | Controle de acesso | Todos os recursos AWS | Granularidade alta | Curva de aprendizado |
| Amazon S3 | Armazenamento | Dados e artefatos | Escalável, seguro | Latência se não otimizado |
| Amazon Macie | Identificação de dados sensíveis | Compliance | Automático, integrado | Custo adicional |
| Amazon Inspector | Análise de vulnerabilidades | Avaliar segurança de EC2 e workloads | Automatizado, detalhado | Custo adicional |
| VPC + Security Groups + PrivateLink | Proteção de endpoints | Segurança de endpoints SageMaker | Conexão privada, isolada | Configuração complexa |
| CloudWatch | Monitoramento | Logs e métricas | Integração AWS | Necessita configuração |
| CloudTrail | Auditoria | Histórico de ações AWS | Compliance | Volume de logs |

---
