# Domain 3: Applications of Foundation Models

## 3.1 Design e Escolha de Modelos

A escolha do modelo depende de **custo**, **latência**, **necessidade de customização** e **formato dos dados**:

- **Custo:**  
  - **Amazon Bedrock** cobra por uso de tokens (pay-as-you-go).  
  - **Amazon SageMaker** cobra por instância (tempo de treinamento e inferência).  
- **Latência:**  
  - Modelos maiores ⇒ respostas mais poderosas, porém mais lentas.  
- **Customização:**  
  - **Bedrock**: acesso a modelos fixos de provedores (Anthropic, Stability, AI21).  
  - **SageMaker**: permite fine-tuning, transfer learning e treinamento profundo.  
- **Entrada/Saída:**  
  - Avalie se precisa de texto, imagem, áudio ou multimodalidade.  

### Integração com Bases de Conhecimento (RAG - Retrieval Augmented Generation)
- Combine modelos LLM com dados proprietários para respostas mais relevantes.  
- Serviços AWS para vetores e documentos:  
  - **Amazon OpenSearch Service** → indexação e busca vetorial.  
  - **Amazon Neptune** → consultas em grafos complexos.  
  - **Amazon Aurora** → dados relacionais estruturados.  

---

## 3.2 Engenharia de Prompts

**Prompt engineering** é essencial para controlar a saída dos modelos generativos:

- Boas práticas:  
  - Forneça **exemplos claros** no prompt.  
  - Use **instruções explícitas** sobre estilo, formato e contexto.  
  - Aplique **Chain-of-Thought** para guiar o raciocínio.  
- Segurança:  
  - Evite expor informações sensíveis em prompts.  
  - Use filtros e políticas de acesso a dados.  
- Ferramentas AWS:  
  - **SageMaker Studio** → experimentação com prompts.  
  - **Bedrock Playground (PartyRock)** → testes rápidos de prompts com modelos de parceiros.  

---

## 3.3 Treinamento e Fine-Tuning

Se **prompt engineering** não for suficiente, é possível treinar e adaptar modelos:  

- **SageMaker** suporta:  
  - **Pré-treinamento** (casos avançados, requer muitos dados).  
  - **Fine-tuning** com datasets específicos.  
  - **Transfer Learning** para aproveitar modelos existentes.  

- Serviços envolvidos:  
  - **SageMaker Training Jobs** → execução do treinamento.  
  - **SageMaker Experiments** → rastreio de versões, parâmetros e métricas.  

⚠️ **Atenção:** Fine-tuning pode ser caro e complexo. Avalie se realmente é necessário antes de optar por essa abordagem.  

---

## 3.4 Avaliação de Modelos

- **Métricas automáticas:**  
  - **BLEU** (qualidade de tradução).  
  - **ROUGE** (qualidade de sumarização).  
- **Métricas humanas:**  
  - Clareza, relevância e utilidade da resposta.  
- **Monitoramento:**  
  - **SageMaker Model Monitor** → detecta desvios nos dados de entrada e saída.  
- **Impacto de Negócio:**  
  - Ex.: Taxa de conversão, tempo de resposta, engajamento de usuários.  

---

## Resumo dos Serviços Citados

- **Amazon Bedrock:** acesso gerenciado a Foundation Models.  
- **Amazon SageMaker:** desenvolvimento, treinamento e fine-tuning de modelos customizados.  
- **Amazon OpenSearch Service:** busca vetorial e indexação de embeddings.  
- **Amazon Neptune:** banco de grafos para consultas complexas.  
- **Amazon Aurora:** banco de dados relacional escalável.  
- **SageMaker Experiments:** controle de versões e experimentação.  
- **SageMaker Model Monitor:** monitoramento de modelos em produção.  
- **Bedrock Playground (PartyRock):** experimentação com prompts.  

---
