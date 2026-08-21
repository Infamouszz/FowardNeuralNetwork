# Rede neural no formato *FeedForward* feita do zero, utilizando apenas torch para multiplicação de matrizes na GPU

## Sobre o projeto:
Uma rede neural treinada com milhões de posição de xadrez avaliadas pela engine do StockFish feita para analisar e classificar posições baseando-se na métrica de centi-peões.

## Objetivo do projeto:
Aprender o funcionamento computacional e matemático da rede neural feedforward do absoluto zero, desde a parte matemática e tratamento dos dados até a parte de otimização e arquitetura da rede.

## Módulos utilizados no algoritmo de aprendizado:
- **Arquitetura**: Feed Foward Neural Network (FNN).
- **Ativadores**: ReLU nas camadas ocultas e Softmax na camada final.
- **Inicializador**: Inicialização dos neurônios da rede utilizando He / Kaiming Initialization.
- **Função de perda**: Entropia Cruzada Categórica, visando uma perda alta para aprendizado de classificação por parte do modelo.
- **Otimizador**: Mini-Batch Gradient Descent com Momentum para processar todas as posições de forma rápida e sem estressar a memória RAM do computador e conseguir chegar no mínimo global da função de custo com mais leveza.

## Tratamento de dados utilizados:
- **Undersampling**: Igualamento das classes das posições, visando evitar o enviesamento do modelo por excesso de repitação de amostras de mesma classe.
- **One-hot encoding**: Para fazer com que o modelo entenda a classificação da posição e não sua grandeza númerica, utilizei o one hot encoding para dizer onde cada peça está em cada casa do tabuleiro.
- **Binning**: Agrupamento da classficação do StockFish para [0,1] = Ótima e boa para as brancas / [2] = Neutra / [3, 4] = Boa e ótima para as pretas.
- **Feature engineering**: Transformação do tabuleiro em colunas e números para o treinamento do modelo.

## Dataset e biblioteca utilizado
- Dataset público do lichess com jogos analisados pela engine StockFish.
- PyTorch para multiplicação das matrizes na GPU do computador, diminuindo o tempo de treinamento.

