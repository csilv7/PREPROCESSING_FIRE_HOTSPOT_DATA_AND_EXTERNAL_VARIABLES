# PRÉ PROCESSAMENTO DE DADOS DE FOCOS DE INCÊNDIOS E VARIÁVEIS EXTERNAS

## 📝 Resumo Executivo

Este repositório contém um ***pipeline especializado de engenharia de dados desenvolvido para a limpeza, normalização e estruturação de dados de focos de incêndio e variáveis externas em Python***. O objetivo primordial é transformar registros operacionais brutos em um dataset de alta integridade, pronto para ***Análise Temporal, Climática e Geográfica***.

---

## 🛠️ Metodologia e Funcionalidades Técnicas

### 1. Saneamento e Normalização de Dados

A etapa de pré-processamento garante a integridade dos metadados através de:

* Padronização de formatode base de dados.
* Criação e manipulação de atributos (colunas) de *Data Frames*
* Construção de variáveis temporias e climáticas além de integração de Data Frames
* Uso de funções como: `pd.concat`, `pd.merge` e `pd.melt`

### 2. Engenharia de Atributos Temporais, Climáticos e Geográficos (Feature Engineering)

Para capturar padrões cíclicos nas ocorrências, o pipeline extrai:

* **Ano** e **Mês** para avaliar os padrões de tendência e sazonalidade mensal.
* **Variável Periódica** que indica o periódo climático em cada registro (linha) do Data Frame
* **Integração de Informações** de localização a nível municipal

---

## 📂 Estrutura do Projeto

```text
├── dados brutos/
│   └── 001 - Arquivos Excel Focos 1995-2024/  # Dados de Focos de Incêndios
│   └── DADOS DE HOPITALIZAÇÕES - 1998 A 2024/ # Dados de Hospitalizações
│   └── DADOS DE QUEIMADAS/                    # Dados de Cicatrizes de Queimadas
│   └── DADOS DE EMISSÃO/                      # Dados de Emissão de PM 2.5
├── dados processados/
│   └── data_focus_fire_2005_2024.csv          # Dados de Focos de Incêndios Pré-processados
│   └── data_hospitalizations_1998_2024.csv    # Dados de Hospitalizações Pré-processados
│   └── data_pm25_2005_2024.csv                # Dados de Emissão de PM 2.5 Pré-processados
│   └── data_complete.csv                      # Dados Consolidados
├── code_data_fire.ipynb    # Notebook do Projeto
├── code_data_fire.pyn      # Arquivo Python do Projeto
├── requirements.txt        # Dependências do projeto
└── README.md
```

---

## 🚀 Como Utilizar

1. **Clonar o repositório:**
```bash
git clone https://github.com/csilv7/PREPROCESSING_FIRE_HOTSPOT_DATA_AND_EXTERNAL_VARIABLES.git

```


2. **Instalar dependências:**
```bash
pip install -r requirements.txt

```


3. **Executar o pipeline:**
Utilize o Jupyter Notebook em `notebooks/`.

---

## 📈 Trabalhos Futuros

* Integração de variáveis meteorológicas externas (Umidade, Velocidade do Vento, Precipitação).
* Implementação de modelos de **Regressão de Poisson** para estimativa de taxas de ocorrência.
* Ingestão automatizada de dados via *web scraping*.

---

### Observações Técnicas Adicionais:

* **Sobre os Dados:** Os dados são públicos e fazem parte da dissertação de mestrado do **CEL QOBM WAGNER** do Corpo de Bombeiros Militar do Pará (CBMPA) intitulada de: ***INCÊNDIOS FLORESTAIS NO ESTADO DO PARÁ (2005–2024): UMA ANÁLISE DOS IMPACTOS SOCIOAMBIENTAIS E DECRETAÇÕES DE SITUAÇÕES DE EMERGÊNCIA***. Sendo esta demanda foi exceutada no período de *Voluntáriado Civil* exercido na coorporação. Caso se interesse entre em contato em [brenosilvasantos@gmail.com](mailto:brenosilvasantos@gmail.com)
