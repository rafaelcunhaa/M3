# M3
M3 da disciplina de Introdução a Ciências da Computação

model.compile(optimizer='adam',
              loss=tf.keras.losses.SparseCategoricalCrossentropy(from_logits=True),
              metrics=['accuracy'])
A função compile configura o modelo de rede neural para o treinamento. Aqui, definimos o otimizador como 'adam', que é um método de otimização popular para redes neurais. A função de perda é definida como SparseCategoricalCrossentropy, que é adequada para problemas de classificação com rótulos de classe discreta. Também especificamos que queremos acompanhar a métrica de acurácia durante o treinamento.

python
Copy code
history = model.fit(train_images, train_labels, epochs=10,
                    validation_data=(test_images, test_labels))
A função fit é responsável por treinar o modelo. Passamos os dados de treinamento train_images e os rótulos correspondentes train_labels. Definimos o número de épocas como 10, o que significa que o conjunto de treinamento será percorrido 10 vezes durante o treinamento. Também fornecemos o conjunto de validação composto por dados de teste test_images e rótulos de teste correspondentes test_labels.

Durante o treinamento, o modelo ajusta seus pesos com base nos dados de treinamento para minimizar a função de perda. A cada época, os resultados do treinamento são registrados na variável history para análise posterior.

No exemplo fornecido, o treinamento é executado por 10 épocas. Durante cada época, são exibidos os valores de perda (loss) e acurácia (accuracy) para os dados de treinamento e validação. Isso nos permite monitorar o desempenho do modelo ao longo do tempo e avaliar se ele está aprendendo adequadamente a partir dos dados fornecidos.

Ao final do treinamento, podemos usar o modelo treinado para fazer previsões em novos dados e avaliar sua precisão com base nos rótulos verdadeiros.

Os resultados específicos podem variar dependendo do conjunto de dados e da complexidade do problema em questão. O objetivo é obter um modelo com baixa perda e alta acurácia, capaz de generalizar bem para dados não vistos.
RESUMO:
A função "model.compile" configura o modelo de rede neural para treinamento, especificando o otimizador, a função de perda e as métricas a serem rastreadas. Neste caso, o otimizador é definido como "adam", que é uma escolha popular para otimização baseada em gradiente. A função de perda utilizada é SparseCategoricalCrossentropy, adequado para tarefas de classificação com rótulos de classe discretos. A métrica desejada para monitorar durante o treinamento é precisão.


A função "model.fit" é responsável pelo treinamento do modelo. Ele leva os dados de treinamento, `train_images`, e rótulos correspondentes, `trein_labels`, como entradas. O parâmetro 'epochs' determina o número de vezes que o modelo irá repetir em todo o conjunto de dados de treinamento. Os dados de validação, 'test_images' e 'test-labels', são fornecidos para avaliar o desempenho do modelo em dados invisíveis.


Durante o treinamento, o modelo ajusta seus pesos com base nos dados de treinamento para minimizar a função de perda. O objeto "história" registra os resultados do treinamento para análise adicional.


No exemplo dado, o treinamento é realizado por 10 épocas. Os valores de perda e precisão são exibidos para dados de treinamento e validação em cada época. Isso permite monitorar o desempenho do modelo ao longo do tempo e avaliar sua aprendizagem a partir dos dados fornecidos.


Após o treinamento, o modelo treinado pode ser usado para fazer previsões sobre novos dados e avaliar sua precisão contra os rótulos verdadeiros.

https://github.com/rafaelcunhaa/M3/blob/main/README.md
É importante notar que os resultados específicos podem variar dependendo do conjunto de dados e da complexidade do problema. O objetivo é alcançar um modelo com baixa perda e alta precisão, capaz de generalizar bem para dados invisíveis.
