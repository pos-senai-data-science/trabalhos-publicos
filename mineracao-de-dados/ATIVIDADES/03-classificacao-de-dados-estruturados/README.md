# Desafio Titanic - Conclusão

Concluir o desafio do Titanic. 


As equipes devem gerar classificadores para a base fornecida usando os algoritmos KNN, árvore de decisão e random forest, variando os parâmetros de cada um deles (recomendo o uso de gridsearch).

Lembrem de testar diferentes conjuntos de atributos. 

Para identificar os melhores conjuntos, vocês podem usar as informações que vocês obtiveram na análise exploratória, técnicas de seleção de atributos (o sklearn tem algumas funções para isso) e o próprio random forest retorna a importância dos atributos.

Depois de gerar os diferentes classificadores, façam a avaliação para identificar o melhor conjunto de atributos, algoritmo de aprendizado e configuração de parâmetros, treine um novo classificador com todo o conjunto de treinamento e classifiquem o conjunto de teste fornecido na página do desafio do Kaggle.

Script para gerar csv no formato de submissão aceito pelo Kaggle:


submission = pd.DataFrame({
        "PassengerId": df["PassengerId"],
        "Survived": Y_prediction
    })
submission.to_csv('submission.csv', index=False)
files.download('submission.csv')