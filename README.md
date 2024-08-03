# Teste-Senai
Este repositório é referente a resolução de dois problemas usando python3+ e algoritmos de aprendizado de máquina,  um sistema de detecção de emoções(felicidade, tristeza e raiva) em frases aleatórias e um sistema de identificação de idioma(português, inglês e mandarim).

# Funcionamento
Ambos projetos foram feitos a partir de notebook virtual, disponibilizado pela Google Colab!
 O Google Colab fornece um ambiente de notebook baseado em nuvem que facilita a execução de código Python e a utilização de bibliotecas, sem a necessidade de configuração local.
- O sistema de detecção de emoções é eficaz para identificar frases relacionada a felicidade, tristeza e raiva, sendo assim ele deve não só corresponder a frase que esta no banco de dados mas também, deve fazer uma generalização de novas frases.
- Já o sistema de detecção de idiomas, deve informar com base nos dados, de qual idioma se trata aquela frase ou saudação.
- O modelo que mas se mostrou eficaz foi o Naive bayer - algoritmo de classificação supervisionada, ou seja ele precisa de uma exemplificação para aprender, foram criados frases relacionadas as respectivas propostas de problematização, bem simples mas cumpre com o esperado.
- As bibliotecas usadas foram:
 scikit-learn: Biblioteca para aprendizado de máquina em Python que fornece ferramentas para classificação, regressão, clustering e redução de dimensionalidade;
 pandas: Biblioteca para manipulação e análise de dados, oferecendo estruturas de dados como DataFrames para trabalhar com dados tabulares;

# As Importações dos Módulos:
import pandas as pd
from sklearn.feature_extraction.text import TfidfVectorizer
from sklearn.model_selection import train_test_split
from sklearn.naive_bayes import MultinomialNB
from sklearn.metrics import classification_report, accuracy_score

import pandas as pd: Importa a biblioteca pandas e a renomeia como pd para facilitar seu uso. Pandas é usada para manipulação de dados e análise de dados, especialmente com estruturas de dados como DataFrames;

from sklearn.feature_extraction.text import TfidfVectorizer: Importa a classe TfidfVectorizer do módulo feature_extraction.text da biblioteca scikit-learn. TfidfVectorizer é usada para converter uma coleção de documentos de texto em uma matriz de características TF-IDF;

from sklearn.model_selection import train_test_split: Importa a função train_test_split do módulo model_selection da biblioteca scikit-learn. train_test_split é usada para dividir um conjunto de dados em conjuntos de treinamento e teste;

from sklearn.naive_bayes import MultinomialNB: Importa a classe MultinomialNB do módulo naive_bayes da biblioteca scikit-learn. MultinomialNB é um classificador Naive Bayes para distribuição multinomial, frequentemente usado para classificação de texto;

from sklearn.pipeline import make_pipeline: Importa a função make_pipeline do módulo pipeline da biblioteca scikit-learn. make_pipeline é usada para criar um pipeline que sequencialmente aplica uma lista de transformações e um estimador final;

from sklearn.metrics import accuracy_score: Importa a função accuracy_score do módulo metrics da biblioteca scikit-learn. accuracy_score é usada para calcular a precisão de um classificador, ou seja, a proporção de previsões corretas;

import joblib: Importa a biblioteca joblib, que é usada para salvar e carregar modelos treinados em disco. Isso permite que você salve o estado de um modelo de aprendizado de máquina e o recarregue posteriormente sem precisar treinar novamente;
# Como usar:
 Inicialmente, você pode usar o google colab ou Jupyter notebook, seguir as linhas de código, incluindo as ativações de bibliotecas, seguidamente a isto, deve ser feita a preparação dos dados e a qual modelo de aprendizado de máquina usar, seguindo nesta linha, Crie um pipeline que inclua transformações e o classificado, e treine o modelo com dados de treinamento e teste com dados de teste - para ver qual será o modelo mais eficaz e o que fará melhor previsão e por fim, avalie a performance do modelo usando métricas como a precisão.
