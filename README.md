# 📊 Telecom X — Análise de Evasão de Clientes (Churn)

Projeto desenvolvido no **Challenge de Especialização (Oracle Next Education / Alura)** para analisar a **evasão de clientes (Churn)** na empresa fictícia **Telecom X**.

O trabalho cobre **Extração** dos dados via API, **Transformação** (limpeza/padronização/criação de feature) e **Análise Exploratória** com visualizações e **Relatório Final** com insights e recomendações. Este README contém: propósito, estrutura, **instalação e dependências**, **como executar** e **possíveis problemas/soluções**.

---

## 🎯 Objetivos do Projeto

* Carregar os dados diretamente de uma **API (JSON)** e convertê-los em **Pandas DataFrame**.
* Tratar e padronizar os dados (tipos, valores ausentes, categorias inconsistentes).
* Criar a coluna derivada **`Contas_Diarias`** a partir do faturamento mensal.
* Explorar a distribuição de **Churn** e sua relação com variáveis **categóricas** e **numéricas**.
* Elaborar um **relatório** (no próprio notebook) com conclusões e recomendações acionáveis.

---

## 🗂️ Estrutura do Repositório

* **`TelecomX_BR.ipynb`** — Notebook principal contendo:

  * **E — Extract**: consumo da API com `requests` e conversão para DataFrame.
  * **T — Transform**: limpeza/padronização (`Total` → `TotalCharges`, conversão numérica com `pd.to_numeric(..., errors="coerce")`, `fillna(0)`, padronização de categorias como `'No internet service'`/`'No phone service'` → `'No'`, ajuste de `'Churn'` vazio → `'No'`), criação de **`Contas_Diarias`**.
  * **L — Load & Analysis**: estatísticas descritivas, distribuição de **Churn**, análises por variáveis **categóricas** e **numéricas** com gráficos (barras, pizza, boxplots e histogramas).
  * **Relatório Final**: introdução, descrição das etapas, análises com visualizações, **conclusões** e **recomendações**.
* **`README.md`** — Este documento.

> ℹ️ Os dados são carregados **dinamicamente** via API durante a execução; o JSON não precisa estar versionado no repositório.


---

## ⚙️ Ambiente e Dependências

* **Python 3** — desenvolvido e testado no **Google Colab** (Python **3.10** no momento da execução); compatível com **Python 3.8 ou superior**.
* Bibliotecas utilizadas:

  * `pandas` — manipulação de dados
  * `matplotlib` — gráficos
  * `seaborn` — visualizações estatísticas
  * `requests` — consumo da API

Instalação rápida (ambiente local):

```bash
pip install pandas matplotlib seaborn requests
```

---

## ▶️ Como Executar

### Opção A — Google Colab (recomendado)

1. Acesse o **Google Colab**.
2. **Arquivo → Fazer upload do notebook** e selecione `TelecomX_BR.ipynb`.
3. Clique em **Executar tudo**.
4. Ao final, para garantir a visualização dos gráficos no GitHub, use **Arquivo → Fazer download → Download .ipynb** (salva o notebook **com as saídas**).

### Opção B — Ambiente Local (Jupyter Notebook)

1. Clone o repositório:

   ```bash
   git clone https://github.com/PedrogitMendes/Telecom-X.git
   cd Telecom-X
   ```
2. Crie (opcional) um ambiente virtual e instale as dependências:

   ```bash
   pip install pandas matplotlib seaborn requests
   ```
3. Abra o Jupyter Notebook e execute `TelecomX_BR.ipynb` **em ordem**.

---

## 🔎 O que o Notebook Faz (Mapeado ao Trello)

**E — Extract**

* ✅ Carrega os dados diretamente da **API** usando `requests`.
* ✅ Converte o JSON para **DataFrame do Pandas**.

**T — Transform**

* ✅ Explora as colunas e verifica tipos (`df.info()`/`dtypes`).
* ✅ Consulta o dicionário de dados (linkado e carregado no notebook para referência).
* ✅ Identifica e trata problemas: nulos, duplicados, formatações e categorias inconsistentes.
* ✅ Aplica correções (conversões, padronização de categorias e alvo `Churn`).
* ✅ Cria a coluna **`Contas_Diarias`** a partir de `Monthly/30`.
* 🟨 Padronização opcional (binarização 0/1) — **não obrigatória**; o notebook prioriza padronização textual clara.

**L — Load & Analysis**

* ✅ Estatísticas descritivas (média, mediana, desvio padrão etc.).
* ✅ Distribuição de **Churn** (gráfico de barras e pizza).
* ✅ Evasão por variáveis **categóricas** (gênero, contrato, pagamento, serviços etc.).
* ✅ Evasão por variáveis **numéricas** (`tenure`, `Monthly`, `TotalCharges`, `Contas_Diarias`) — boxplots e histogramas.
* ✅ **Relatório Final** no próprio notebook: Introdução, Limpeza/Tratamento, EDA, Conclusões/Insights e Recomendações.

---

## 📊 Principais Insights (resumo)

* **Contrato mês a mês** apresenta maior propensão ao churn em comparação a contratos anuais.
* Ausência de **serviços adicionais** (ex.: segurança online, suporte técnico) está associada a maior churn.
* **Electronic check** tende a ter maior churn que outros métodos de pagamento.
* **Tenure** menor (primeiros meses) concentra a maior parte das evasões.
* Custos **mensais** e **totais** mais altos correlacionam-se com maior churn em alguns segmentos.

> Todos os pontos acima são sustentados por visualizações no relatório final do notebook.

---

## 🧩 Reprodutibilidade

* Desenvolvido no **Google Colab** (Python 3.10). Compatível com **Python 3.8+**.
* Execute o notebook **em ordem** e salve **com as saídas** para visualização completa no GitHub.

---

## 🛠️ Problemas Comuns & Soluções

* **Gráficos não aparecem no GitHub**
  Execute todas as células e baixe o `.ipynb` **com as saídas** (Colab: *Arquivo → Download .ipynb*). Os blocos finais do relatório já usam `plt.show()` para embutir as figuras.
* **Erro ao acessar a API**
  Verifique a conexão com a internet e a disponibilidade do repositório-base. Em caso de indisponibilidade temporária, tente novamente mais tarde.
* **Biblioteca ausente**
  Instale com: `pip install pandas matplotlib seaborn requests`.
* **Resultados levemente diferentes**
  Diferenças de versões de bibliotecas e ambiente podem alterar estilos de gráficos. Recomenda-se **Python 3.8+** e reexecução completa.


---

## ✍️ Autor

**Pedro de Carvalho Mendes** — participante do **Oracle Next Education (ONE)** em parceria com a **Alura**.
