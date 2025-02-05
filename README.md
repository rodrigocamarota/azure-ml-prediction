# Projeto de Previsão com Regressão no Azure Machine Learning

Neste projeto, eu treinei um modelo de regressão no **Azure Machine Learning Studio**, utilizando um conjunto de dados público sobre Pokémon. O objetivo foi construir um modelo de previsão e implantar um ponto de extremidade para fazer previsões em tempo real.

## Passo a Passo

### 1. Criação do Workspace no Azure
A primeira etapa foi acessar o **Portal do Azure** e criar um novo **Azure Machine Learning Workspace**. Esse workspace é o ponto central onde todo o gerenciamento e os recursos de Machine Learning são organizados.

### 2. Acessando o Azure Machine Learning Studio
Após a criação do workspace, fui até o **Azure Machine Learning Studio**, que é a interface onde criei o trabalho de Machine Learning e configurei o modelo de previsão.

### 3. Criação do Trabalho de Machine Learning Automatizado
Dentro do **Azure Machine Learning Studio**, criei um novo trabalho de ML automatizado. Isso permite a criação de um fluxo automatizado para treinar e avaliar o modelo sem a necessidade de intervenção manual.

### 4. Configurações Iniciais do Trabalho
Realizei as configurações básicas do trabalho, como a definição do nome e a escolha de parâmetros iniciais. Na sequência, selecionei o tipo de tarefa como **Regressão**, que era adequado para prever valores numéricos com base em variáveis de entrada.

### 5. Fonte de Dados
Para o modelo, utilizei um conjunto de dados público sobre **Pokémons**, que estava disponível em formato **CSV** na web. Adicionei a fonte de dados diretamente do endereço web, o que me permitiu carregar os dados sem necessidade de uploads manuais.

### 6. Configuração das Tarefas do Modelo
Configurei as tarefas, que envolviam a definição de:
- **Dados de entrada**: Escolhi as colunas relevantes do conjunto de dados.
- **Coluna de destino**: Selecionei a variável que o modelo deveria prever.
- **Métricas de avaliação**: Configurei as métricas para avaliar o desempenho do modelo.
- **Modelos permitidos**: Estabeleci os modelos que poderiam ser utilizados para o treinamento, baseados nas características dos dados.

### 7. Escolha das Configurações de Computação
Selecionei as **configurações de computação** adequadas para o treinamento. Em seguida, enviei o trabalho para execução. O tempo de treinamento foi de aproximadamente **20 minutos**, durante o qual o Azure Machine Learning usou recursos computacionais para treinar o modelo com o conjunto de dados escolhido.

### 8. Avaliação do Modelo
Após a conclusão do treinamento, acessei o menu de **Modelos + Trabalhos Filho** para verificar os resultados. Na aba de **Métricas**, pude observar as estatísticas e avaliar o desempenho do modelo.

### 9. Implantação do Modelo
Após verificar que o modelo estava adequado, fui até a aba **Implantar** e selecionei a opção **Terminal em Tempo Real** para criar um ponto de extremidade (endpoint). O endpoint gerado permite que o modelo seja acessado via API, permitindo realizar previsões em tempo real.

### 10. Ponto de Extremidade Criado
O ponto de extremidade foi criado com sucesso, e agora ele pode ser utilizado para enviar dados de entrada e obter previsões do modelo treinado. O **endpoint REST** gerado está acessível através do seguinte link:
