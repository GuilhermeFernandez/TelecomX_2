# TelecomX_2

<div align="center">
  <h1>📊 Previsão de Churn em Telecom: KNN e Árvore de Decisão</h1>
  <p>
    <em>Uma análise comparativa de modelos de Machine Learning para identificar e entender a evasão de clientes (Churn).</em>
  </p>
</div>

<hr>

<h2>🎯 Objetivo do Projeto</h2>
<p>
  Este projeto teve como objetivo construir, otimizar e comparar dois modelos de classificação — <strong>K-Nearest Neighbors (KNN)</strong> e <strong>Árvore de Decisão (Decision Tree)</strong> — para prever quais clientes têm maior probabilidade de cancelar seus serviços de telecomunicações. Além da performance preditiva, o foco do projeto é extrair <em>insights</em> de negócio analisando a importância das variáveis na tomada de decisão de cada algoritmo.
</p>

<h2>🛠️ Bibliotecas Utilizadas</h2>

<p align="left">
  <img height="50" alt="Pandas" src="https://github.com/user-attachments/assets/58cb0f92-c3a9-4ca6-8296-8a4c82436612" style="margin-right: 10px;" />
  <img height="50" alt="Scikit-Learn" src="https://github.com/user-attachments/assets/506868fb-db8a-48fc-9670-c9acc8780d44" style="margin-right: 10px;" />
  <img height="50" alt="Matplotlib" src="https://github.com/user-attachments/assets/3378dc38-774b-4634-b98b-ae07d15fef71" style="margin-right: 10px;" />
  <img height="50" alt="Yellowbrick" src="https://github.com/user-attachments/assets/20c635f6-268b-41ba-b9a6-a62a373a742f" style="margin-right: 10px;" />
</p>

<ul>
  <li><strong>Pandas</strong>: Manipulação, limpeza e análise exploratória dos dados.</li>
  <li><strong>Scikit-Learn (sklearn)</strong>: Construção do <em>pipeline</em> de Machine Learning, incluindo:
    <ul>
      <li><code>ColumnTransformer</code> para o <em>One-Hot Encoding</em>.</li>
      <li><code>StandardScaler</code> para a normalização de dados numéricos.</li>
      <li><code>GridSearchCV</code> para a validação cruzada e otimização de hiperparâmetros.</li>
      <li><code>permutation_importance</code> para extração da importância de variáveis do KNN.</li>
    </ul>
  </li>
  <li><strong>Matplotlib</strong>: Construção e customização de gráficos de barras para visualização das importâncias das variáveis.</li>
  <li><strong>Yellowbrick</strong>: Visualização gráfica de informações estatísticas como importâncias das variáveis, matriz de confusão de relatório de classificação.</li>
  <li><strong>Graphviz</strong>: Renderização estrutural da Árvore de Decisão para análise visual dos nós de corte.</li>
</ul>

<h2>⚙️ Metodologia e Modelagem</h2>
<p>
  O projeto lidou com desafios comuns através de dados reais, como o desbalanceamento de classes, que inicialmente causava viés e <em>Overfitting</em> nos modelos. A abordagem consistiu em:
</p>
<ol>
  <li><strong>Pré-processamento:</strong> Separação adequada de dados numéricos e categóricos para garantir que algoritmos sensíveis à escala (como o KNN) não fossem distorcidos por grandezas financeiras.</li>
  <li><strong>Otimização:</strong> Foco na métrica <em>F1-Score</em> durante o uso do <code>GridSearchCV</code> para encontrar o melhor ponto de equilíbrio na detecção de churn.</li>
</ol>

<h2>📈 Principais Resultados</h2>
<p>
  A Árvore de Decisão Otimizada apresentou um desempenho robusto, saltando de um <em>Recall</em> inicial quase nulo para <strong>0.578</strong> e mantendo uma Precisão na casa dos <strong>85%</strong>, o que a torna uma ferramenta viável para campanhas direcionadas de retenção.
</p>
<p>Na análise de interpretabilidade, os modelos concordaram na relevância das variáveis, mas agiram de formas diferentes:</p>
<ul>
  <li>🌳 <strong>Árvore de Decisão:</strong> Focou esmagadoramente em três fatores (Contrato Mensal, Tempo de Permanência e Internet Fibra Ótica).</li>
  <li>📏 <strong>KNN:</strong> Apresentou uma distribuição de importância mais equilibrada, considerando o pacote de serviços como um todo (Segurança Online, Múltiplas Linhas) e as Cobranças Totais para agrupar clientes com comportamentos similares.</li>
</ul>

<hr>

<div align="center">
<p>Autor</p>
<a href="https://github.com/GuilhermeFernandez">
        <img src="https://github.com/user-attachments/assets/e854d14c-2bf0-45f4-9fd4-8a4b1afeb364" width="115" alt="Foto de Guilherme">
        <br>
        <sub><b>Guilherme Honório Fernández</b></sub>
