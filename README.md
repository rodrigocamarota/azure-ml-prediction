# Projeto de Machine Learning no Azure ML - Previsão com Regressão

Este projeto demonstra o processo de criação e implantação de um modelo de Machine Learning usando o **Azure Machine Learning Studio**. O objetivo foi treinar um modelo de regressão baseado em um conjunto de dados públicos sobre Pokémon.

## 🚀 Passo a Passo

### 1. Configuração do Ambiente
1. Acesse o [Portal do Azure](https://portal.azure.com/) e crie um novo **Azure Machine Learning Workspace**.
2. No workspace criado, acesse o **Azure Machine Learning Studio**.

### 2. Criação do Trabalho Automatizado
3. No **Azure Machine Learning Studio**, crie um novo **Trabalho de ML Automatizado**.
4. Defina as **configurações básicas** do projeto.
5. No tipo de tarefa, escolha **Regressão**.

### 3. Configuração da Fonte de Dados
6. Adicione uma **fonte de dados** a partir de um endereço web contendo um conjunto de dados públicos sobre **Pokémons** em formato **CSV**.

### 4. Configuração das Tarefas
7. Configure os parâmetros do modelo:
   - Escolha os dados de entrada.
   - Defina a **coluna de destino**.
   - Configure as **métricas** e os **modelos permitidos**.
   - Ajuste os **limites** para o treinamento.

### 5. Treinamento do Modelo
8. Escolha as **configurações de computação** e inicie o **treinamento**.
9. O processo de treinamento levou aproximadamente **20 minutos**.

### 6. Avaliação do Modelo
10. Após a finalização do treinamento, acesse a aba **Modelos + Trabalhos Filho** e selecione o modelo treinado.
11. Analise os **resultados** na aba **Métricas** para avaliar o desempenho.

### 7. Implantação do Modelo
12. Vá até a aba **Implantar** e selecione a opção **Terminal em Tempo Real** para criar um **Ponto de Extremidade**.
13. Após a implantação, obtenha o **endpoint REST** para futuras inferências.

## 📂 Arquivos no Repositório
- `README.md` → Este guia com o passo a passo.
- `endpoint.json` → Configuração do ponto de extremidade gerado pelo Azure ML.

## 📡 Uso do Endpoint
Após a implantação, o modelo pode ser consumido via **requisições HTTP** para o endpoint gerado.

Exemplo de requisição usando **Python**:

```python
import requests

url = "https://ai-900-pokemon-uvksw.westus.inference.ml.azure.com/score"
headers = {
    "Content-Type": "application/json",
    "Authorization": "Bearer SUA_CHAVE"
}

data = {
    "features": [ /* Insira os dados de entrada aqui */ ]
}

response = requests.post(url, json=data, headers=headers)
print(response.json())
