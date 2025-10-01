# Domain 4: Guidelines for Responsible AI

## 4.1 Desenvolvimento Responsável na AWS

A responsabilidade no uso de **IA** vai além do desempenho técnico. A AWS fornece ferramentas e práticas para garantir que os modelos sejam justos, seguros e governáveis.

### Ferramentas e Práticas
- **SageMaker Clarify:**  
  - Detecta **viés** nos dados de treinamento e nas previsões dos modelos.  
  - Gera relatórios sobre equidade e ajuda a ajustar datasets ou algoritmos.  

- **Guardrails com Amazon Bedrock:**  
  - Definição de **limites de comportamento** em modelos de linguagem.  
  - Bloqueio de respostas ofensivas, tóxicas ou fora de contexto.  

- **Governança de IA na AWS:**  
  - **IAM (Identity and Access Management):** Controle granular de acesso a dados, pipelines e modelos.  
  - **CloudWatch / CloudTrail:** Monitoramento e auditoria de uso.  
  - **GDPR / LGPD:** Conformidade com leis de privacidade de dados.  

### Considerações Éticas e Legais
- Evite vieses que possam afetar minorias ou grupos vulneráveis.  
- Avalie impacto social, legal e cultural antes de colocar modelos em produção.  
- Garanta **privacidade e segurança** no tratamento de dados sensíveis.  

---

## 4.2 Transparência e Explicabilidade

### Documentação e Rastreabilidade
- **SageMaker Model Cards:**  
  - Documentam informações essenciais sobre modelos:  
    - Dataset usado no treinamento.  
    - Desempenho em métricas.  
    - Limitações conhecidas.  
    - Recomendações de uso seguro.  
  - Suportam auditorias e boas práticas de governança.  

### Explicabilidade de Modelos
- Técnicas integráveis ao SageMaker:  
  - **SHAP (SHapley Additive Explanations):** Explica a contribuição de cada feature para a predição.  
  - **LIME (Local Interpretable Model-agnostic Explanations):** Fornece explicações locais de previsões específicas.  

### Equilíbrio Transparência x Segurança
- Transparência é vital para confiança.  
- Contudo, evite expor detalhes excessivos que possam ser explorados para **ataques adversariais**.  
- Use documentação e relatórios direcionados ao público adequado (ex.: equipe técnica, stakeholders, reguladores).  

---

## Resumo dos Serviços Citados

- **SageMaker Clarify:** Detecção e mitigação de vieses.  
- **Amazon Bedrock Guardrails:** Controle de comportamento de LLMs e IA generativa.  
- **SageMaker Model Cards:** Documentação estruturada de modelos.  
- **IAM + CloudWatch + CloudTrail:** Governança, auditoria e monitoramento.  

---
