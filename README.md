# Rede neural no formato *FeddForward* feita do zero, utilizando apenas torch para multiplicação de matrizes na GPU
Para testar o modelo utilizei jogos de xadrez para ensina-lo a avaliar posições de xadrez baseado em jogos pre analisados pela engine StockFish

## Modulos utilizados no algoritmo de aprendizado:
- Ativadores: ReLU nas camadas ocultas e Softmax na camada final
- Inicializador: Inicialização He / Kaiming
- Função de perda: Entropia Cruzada Binária
- Otimizador: Batch Gradient Descent com Momentum

## Tratamento de dados utilizados:
- Pruning
- One-hot encoding
- Binnning
- Modelagem de dados
- Feature enginnering

## Dataset utilizado
- Dataset público do lichess com jogos analisados pela engine StockFish

