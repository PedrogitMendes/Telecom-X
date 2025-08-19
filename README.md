# 📊 Telecom X - Análise de Evasão de Clientes (Churn)

Este projeto faz parte do **Challenge do programa Oracle Next Education (ONE)** em parceria com a **Alura**.  
O objetivo é analisar os dados da empresa fictícia **Telecom X**, identificando os principais fatores que influenciam a **evasão de clientes (churn)** e propor recomendações estratégicas para reduzir a saída de clientes.

---

## 🚀 Objetivo do Projeto
- Importar e tratar dados de clientes da Telecom X.
- Explorar e analisar variáveis que impactam a evasão.
- Identificar padrões e gerar insights sobre o comportamento dos clientes.
- Fornecer recomendações que auxiliem na **retenção de clientes**.

---

## 🛠️ Estrutura do Projeto
- **`TelecomX_BR.ipynb`** → Notebook principal contendo todo o processo:
  - Extração e carregamento dos dados da API.
  - Limpeza e tratamento dos dados.
  - Criação de colunas derivadas (ex: `Contas_Diarias`).
  - Análise exploratória com tabelas e gráficos.
  - Relatório final com conclusões e recomendações.

- **Dados** → Os dados utilizados estão disponíveis via API (JSON) no repositório original fornecido pelo desafio.

---

## 📥 Como Executar o Projeto

### 1. Clonar o repositório
```bash
git clone https://github.com/PedrogitMendes/Telecom-X.git
2. Acessar a pasta do projeto
bash
Copiar
Editar
cd Telecom-X
3. Abrir o Notebook
Você pode abrir o notebook de duas formas:

No Google Colab (recomendado).

Ou localmente no Jupyter Notebook.

No Colab:

Acesse Google Colab.

Vá em Arquivo > Fazer upload do notebook.

Selecione o arquivo TelecomX_BR.ipynb.

📦 Dependências
O notebook utiliza principalmente as seguintes bibliotecas Python:

pandas

numpy

matplotlib

seaborn

requests

Se for rodar localmente, instale com:

bash
Copiar
Editar
pip install pandas numpy matplotlib seaborn requests
📊 Resultados e Insights
A análise identificou:

Perfil dos clientes mais propensos ao churn.

Impacto do tipo de contrato e método de pagamento.

Diferenças no faturamento entre clientes ativos e evadidos.

Recomendações estratégicas para redução da evasão.

⚠️ Possíveis Problemas
Caso execute fora do Colab, verifique se as bibliotecas listadas estão instaladas.

A conexão com a API depende de internet ativa. Se houver erro, baixe o JSON manualmente do repositório original do desafio.

✨ Autor
Desenvolvido por Pedro Mendes no âmbito do programa Oracle Next Education - Alura.
