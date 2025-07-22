# 💸 Monitoramento de Custos com Azure Data Factory

Esse projeto foi criado como parte do desafio da DIO com foco em controle de custos na nuvem usando o **Azure Data Factory (ADF)**. A ideia aqui foi aprender a usar os recursos do portal do Azure pra visualizar e controlar os gastos de forma simples e clara.

---

## 🎯 Objetivo

- Criar uma instância do Azure Data Factory
- Monitorar custos de uso do ADF e outros recursos
- Configurar alertas automáticos quando o uso passar de certos limites
- Criar um painel visual no Azure com essas informações
- (Opcional) Automatizar o processo com template ARM

---

## 🧪 O que foi feito

1. Criação de um **Grupo de Recursos** no Azure
2. Criação da instância `adf-monitoramento-custos`
3. Ativação do **Gerenciamento de Custos + Faturamento**
4. Criação de um **Orçamento (Budget)** com alertas por e-mail
5. Configuração de um **Painel personalizado** com:
   - Orçamento
   - Métricas do ADF (execuções de pipeline, triggers)
6. (Extra) Exportação do template ARM do ADF para automatizar o ambiente

---

## 📸 Prints do Projeto

| Painel de Monitoramento | Alerta de Orçamento |
|-------------------------|---------------------|
| ![painel](./imagens/painel-dashboard.png) | ![alerta](./imagens/alerta-orcamento.png) |

---

## 💡 Insights que eu tive

- O próprio portal do Azure já oferece **muita coisa pronta** pra monitorar e controlar custos, só precisa ativar e usar.
- Criar alertas de orçamento é essencial, principalmente em contas gratuitas ou educacionais.
- Os templates ARM são uma boa prática pra repetir ambientes de forma rápida e padronizada.
- O painel personalizado facilita muito na hora de **visualizar tudo num lugar só**.

---

## 🛠 Ferramentas utilizadas

- Azure Portal (em português)
- Azure Data Factory
- Cost Management + Billing
- Log Analytics (opcional)
- Azure Cloud Shell (opcional)

---

## 🚀 Como rodar (pra quem quiser testar também)

Se quiser replicar o projeto, basta:

1. Criar um grupo de recursos:
```bash
az group create --name rg-monitoramento-custos --location brazilsouth
