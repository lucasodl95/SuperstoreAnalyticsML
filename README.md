# Projeto de Análise e Integração com IA Generativa – Superstore Dataset

Este repositório apresenta uma solução de desafio que combina análise exploratória, modelagem de machine learning e integração com IA generativa para extrair insights a partir do Superstore Dataset. O projeto foi desenvolvido para demonstrar técnicas de análise de dados, segmentação de clientes e geração automatizada de relatórios em PDF.

## Estrutura do Projeto

```
├── data/          # Contém o Superstore Dataset (ex.: Sample - Superstore.csv)
├── notebooks/     # Notebooks Python com as análises dos Níveis 1, 2 e 3
├── src/           # Scripts complementares, se necessário
├── reports/       # Relatórios em PDF gerados automaticamente
├── requirements.txt  # Lista de dependências do projeto
└── README.md      # Este arquivo
```

## Níveis do Projeto

### Nível 1: Análise Exploratória (EDA)
- **Objetivo:**  
  Realizar limpeza, preparação e visualização dos dados do Superstore Dataset para extrair insights sobre vendas, lucros, descontos, categorias e regiões.
- **Ferramentas:**  
  Python, Pandas, NumPy, Matplotlib e Seaborn.
- **Descrição:**  
  Um notebook realiza o carregamento dos dados, conversão de datas, verificação de valores faltantes/duplicados e a criação de gráficos (histogramas, boxplots, pairplots) para facilitar a interpretação dos dados.

### Nível 2: Machine Learning Aplicado
- **Objetivo:**  
  Desenvolver um modelo de segmentação de clientes utilizando as métricas RFM (Recência, Frequência e Monetário) e o algoritmo K-Means.
- **Etapas:**  
  - Cálculo das métricas RFM com nomes em português.
  - Escalonamento dos dados e experimentação com vários valores de K (utilizando o silhouette score para escolher o melhor número de clusters).
  - Visualização dos clusters com pairplot para identificar perfis de clientes (ex.: clientes de alto valor, intermediários e de baixo engajamento).
- **Ferramentas:**  
  Scikit-learn, Pandas, NumPy e Seaborn.

### Nível 3: Integração com IA Generativa (Plus)
- **Objetivo:**  
  Integrar os insights extraídos das análises com um modelo de IA generativa para criar um relatório em linguagem natural, que é então salvo automaticamente em PDF.
- **Etapas:**  
  - Geração do relatório utilizando um modelo de linguagem (neste exemplo, usamos o "google/flan-t5-base" em um pipeline de text2text-generation).
  - Criação de uma pasta "reports" na raiz do projeto para salvar o PDF.
  - Criação do PDF utilizando a biblioteca ReportLab.
- **Ferramentas:**  
  Transformers, ReportLab, Python e Pathlib.

## Requisitos e Instalação

1. **Clone o Repositório:**
   ```bash
   git clone https://github.com/lucasodl95/SuperstoreAnalyticsML
   ```

2. **Crie e Ative um Ambiente Virtual:**
   ```bash
   python -m venv .venv
   # No Windows:
   .\.venv\Scripts\activate
   # No Linux/Mac:
   source .venv/bin/activate
   ```

3. **Instale as Dependências:**
   ```bash
   pip install -r requirements.txt
   ```

## Execução dos Notebooks e Scripts

### Notebooks:
Abra os notebooks na pasta `notebooks` (usando VSCode, Jupyter Notebook ou Google Colab) e execute as células sequencialmente para reproduzir cada nível da análise.

### Ambiente Local vs. Google Colab:
Modelos de IA generativa podem ser muito exigentes em termos de recursos computacionais. Se o seu PC tiver limitações (sem GPU ou memória insuficiente), recomenda-se:
- Executar os notebooks no Google Colab, que oferece GPUs gratuitas.
- Ajustar os parâmetros dos modelos para reduzir o consumo de recursos.

### Geração do Relatório em PDF (Nível 3)
O script do Nível 3 utiliza o pipeline "text2text-generation" com o modelo "google/flan-t5-base" para gerar um relatório com base em um prompt detalhado. Em seguida, o relatório é salvo em PDF na pasta `reports`.

Caso seu computador local não suporte os modelos de IA generativa, a execução no Google Colab é altamente recomendada.

## Considerações Finais

### Desempenho dos Modelos:
Modelos de linguagem modernos podem exigir uma boa quantidade de recursos (GPU e memória). Se o seu PC não suportar essas cargas, use o Google Colab para garantir uma execução mais rápida e eficiente.

### Personalização:
Sinta-se à vontade para ajustar os parâmetros dos modelos (como `max_length`, `temperature`, `top_p`, etc.) e explorar outros modelos disponíveis na Hugging Face para melhor atender ao seu contexto.

### Contribuição:
Se você encontrar melhorias ou quiser adicionar novas funcionalidades, abra uma issue ou envie um pull request.

## Contato
Para dúvidas ou sugestões, entre em contato através das issues deste repositório.

Este projeto foi desenvolvido como parte de um desafio para demonstrar habilidades em análise de dados, machine learning e integração com IA generativa. Aproveite e explore!

