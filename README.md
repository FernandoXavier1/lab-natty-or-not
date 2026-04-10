# Conformidade Documental Inteligente com IA 🤖📄

## 📒 Descrição
Este projeto explora o uso de IAs Generativas e modelos de Machine Learning para automatizar a análise de conformidade documental em instituições financeiras. Combinando OCR, classificação inteligente e intervenção humana nos casos críticos, o sistema é capaz de validar documentos de clientes (KYC) de forma rápida, precisa e escalável — reduzindo erros, custos operacionais e o tempo de onboarding.

> 💡 Este projeto é uma evolução prática dos conceitos explorados em [LabDIO AI-900](https://github.com/FernandoXavier1/labdioai900), aplicando na prática os serviços de IA do Azure em um cenário real do setor financeiro.

## 🤖 Tecnologias Utilizadas
- **Claude (Anthropic)** — Apoio na estruturação da arquitetura e geração de conteúdo técnico
- **Azure AI Document Intelligence** — OCR e extração de campos estruturados em PDFs
- **Azure Machine Learning** — Treinamento e deploy do modelo de classificação de conformidade
- **API REST** — Endpoint de inferência e registro de resultados
- **Python** — Engenharia de atributos e integração dos componentes

## 🧐 Processo de Criação
O projeto foi estruturado em etapas encadeadas:

1. **Coleta de documentos** via API REST, integrando sistemas de onboarding e filas de processamento
2. **Extração de dados** com Azure Document Intelligence, gerando campos estruturados a partir dos PDFs
3. **Engenharia de atributos** — criação de variáveis como presença de assinatura, validação de CPF, similaridade de nome, legibilidade e indícios de rasura
4. **Treinamento e deploy** de um modelo de classificação no Azure ML, publicado como endpoint de inferência em tempo real
5. **Fluxo híbrido**: documentos com alta confiança são aprovados automaticamente; casos duvidosos seguem para validação humana
6. **Registro de conformidade** via API, consolidando resultados automáticos e manuais

Durante o desenvolvimento, IAs Generativas foram utilizadas para apoiar a documentação técnica, refinamento da arquitetura e geração de exemplos de payload.

## 🚀 Resultados
O sistema entrega:
- ✅ Automação da validação documental com score de confiança por documento
- ✅ Redução significativa no tempo de análise em processos de onboarding
- ✅ Fallback humano estruturado para casos de baixa confiança ou inconsistências
- ✅ Endpoint funcional com resposta em tempo real (exemplo abaixo)

**Exemplo de resposta da API:**
```json
{
  "documento_valido": true,
  "score_confianca": 0.92,
  "necessita_validacao_humana": false,
  "observacoes": "Documento válido sem inconsistências"
}
```

**Aplicações diretas:**
- Onboarding de clientes (abertura de conta)
- KYC (Know Your Customer)
- Prevenção à fraude documental
- Análise de crédito e compliance regulatório

## 🔗 Projetos Relacionados
- [**LabDIO AI-900**](https://github.com/FernandoXavier1/labdioai900) — Projeto originário, com os fundamentos de IA do Azure que serviram de base teórica para este trabalho.

## 💭 Reflexão
O maior desafio foi criar um sistema que fosse *natty* — ou seja, que parecesse robusto e confiável sem depender de intervenção humana em cada etapa. A IA consegue cobrir a grande maioria dos casos com alta precisão, mas o fluxo híbrido foi essencial para garantir conformidade regulatória nos casos-limite. Equilibrar automação e supervisão humana é, em si, uma forma de inteligência aplicada.

### Exemplos e Insigths

- [E-BOOK](/exemplos/E-BOOK.md)
- [Podcast](/exemplos/PODCAST.md)
- [Vídeo (Avatar Virtual)](/exemplos/VIDEO.md)

## Links Interessantes

[Base10: If You’re Not First, You’re Last: How AI Becomes Mission Critical](https://base10.vc/post/generative-ai-mission-critical/)

![Base10's Trend Map Generative AI](https://github.com/digitalinnovationone/lab-natty-or-not/assets/730492/f4df26e8-f8f7-4419-8252-c69d73ea930c)
