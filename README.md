# M3
M3 da disciplina de Introdução a Ciências da Computação
import cv2
import numpy as np
import matplotlib.pyplot as plt
# caso for usar o Google Colab com a OpenCV, usar a lib abaixo
from google.colab.patches import cv2_imshow 

# Importando as bibliotecas necessárias: OpenCV, NumPy e Matplotlib

# Carregar a imagem usando a OpenCV
# A imagem será armazenada na variável 'cv2' para ser usada posteriormente
imagem = cv2.imread('caminho/para/sua/imagem.jpg')

# Exibir a imagem usando a função 'cv2_imshow' (usada no Google Colab)
# Se estiver usando o Jupyter Notebook ou outro ambiente, você pode usar 'plt.imshow' para exibir a imagem
cv2_imshow(imagem)

# Converter a imagem para escala de cinza
imagem_cinza = cv2.cvtColor(imagem, cv2.COLOR_BGR2GRAY)

# Exibir a imagem em escala de cinza
cv2_imshow(imagem_cinza)

# Realizar operações ou processamentos na imagem em escala de cinza

# Exibir a imagem processada

# Aguardar pressionamento de tecla para fechar as janelas
cv2.waitKey(0)
cv2.destroyAllWindows()

# Caso esteja usando o Google Colab com a OpenCV, usamos a função cv2_imshow() para exibir a imagem
cv2_imshow(img)

# Exibir a imagem em uma janela com o título 'in' usando a função cv2.imshow()
cv2.imshow('in', img)

# Aguardar até que uma tecla seja pressionada usando a função cv2.waitKey()
# O valor 0 passado como argumento indica que o programa vai esperar indefinidamente até que uma tecla seja pressionada
cv2.waitKey(0)

# Fechar todas as janelas abertas usando a função cv2.destroyAllWindows()
cv2.destroyAllWindows()

# Separar os canais de cor B, G e R da imagem usando a função cv2.split()
B, G, R = cv2.split(img)

# Calcular uma versão em escala de cinza ponderada da imagem usando a fórmula: 0.299*B + 0.587*G + 0.114*R
img_grayscale_pondered = 0.299*B + 0.587*G + 0.114*R

# Converter a imagem para o tipo de dados 'uint8' usando a função np.array() e especificando o tipo de dados como np.uint8
img_grayscale_pondered = np.array(img_grayscale_pondered, dtype=np.uint8)

# Exibir a imagem em escala de cinza ponderada usando a função cv2_imshow()
cv2_imshow(img_grayscale_pondered)

# Definir a flag 'colorida' como 1 para carregar a imagem em cores ou como 0 para carregar em escala de cinza
colorida = 1

# Carregar a imagem usando a função cv2.imread()
# 't1.jpg' é o caminho para a imagem que você deseja abrir
# A flag 'colorida' indica se a imagem será carregada em cores ou em escala de cinza
img_in = cv2.imread('t1.jpg', colorida)

# Inverter os valores dos pixels da imagem, resultando em uma imagem negativa
img_out = 255 - img_in

# Exibir a imagem original usando a função cv2_imshow()
cv2_imshow(img_in)

# Exibir a imagem negativa usando a função cv2_imshow()
cv2_imshow(img_out)

# Carregar a imagem em escala de cinza usando a função cv2.imread()
# 't1.jpg' é o caminho para a imagem que você deseja abrir
# A flag '0' indica que queremos carregar a imagem em escala de cinza
img_in = cv2.imread('t1.jpg', 0)

# Definir os valores dos parâmetros 'a' e 'b'
a = -1
b = 1

# Aplicar uma transformação linear na imagem usando a fórmula: a * img_in + b
img_out = a * img_in + b

# Converter a imagem resultante para o tipo de dados 'uint8' usando a função np.array() e especificando o tipo de dados como np.uint8
img_out = np.array(img_out, dtype=np.uint8)

# Exibir a imagem original em escala de cinza usando a função cv2_imshow()
cv2_imshow(img_in)

# Exibir a imagem resultante após a transformação linear usando a função cv2_imshow()
cv2_imshow(img_out)

# Carregar a imagem em escala de cinza usando a função cv2.imread()
# 't1.jpg' é o caminho para a imagem que você deseja abrir
# A flag '0' indica que queremos carregar a imagem em escala de cinza
img_in = cv2.imread('t1.jpg', 0)

# Definir um kernel de filtro médio 5x5
kernel = np.ones((5, 5), np.float32) / 25

# Aplicar o filtro 2D na imagem usando a função cv2.filter2D()
# O argumento -1 indica que a imagem resultante terá a mesma profundidade de bits da imagem de entrada
img_out_1 = cv2.filter2D(img_in, -1, kernel)

# Exibir a imagem original em escala de cinza usando a função cv2_imshow()
cv2_imshow(img_in)

# Exibir a imagem resultante após a aplicação do filtro usando a função cv2_imshow()

RESUMO:
O código fornecido é um exemplo de usar a biblioteca OpenCV em Python para executar operações de ponto e filtros em imagens. Ele visa demonstrar diferentes etapas e técnicas no processamento de imagens, usando uma imagem como exemplo.
Primeiro, são importadas as bibliotecas necessárias para o processamento de imagens: OpenCV, NumPy e Matplotlib. Estas bibliotecas oferecem uma ampla gama de funcionalidades para manipulação de imagens e visualização.
O próximo passo é carregar a imagem que será processada. A função cv2.imread() é usada para ler a imagem a partir de seu caminho de arquivo específico. A imagem é então armazenada em uma variável chamada "imagem".
Depois de carregar a imagem, a função cv2_imshow() (ou plt.imshow () em outros ambientes) é usada para exibir a imagem original na tela. Isso nos permite visualizar a imagem antes de qualquer processamento ser aplicado.
Em seguida, a imagem é convertida para grayscale usando a função cv2.cvtColor(), que realiza a conversão do espaço de cores BGR para a escala de cores. Este passo é útil quando se trabalha com a imagem em preto e branco, sem o componente de cor.
A imagem de escala cinzenta é então exibida novamente usando a função cv2_imshow(), permitindo-nos visualizar a imagem em sua nova representação de escala Cinzenta.
A partir deste ponto, é possível realizar diferentes operações de ponto ou aplicar filtros à imagem de escala cinzenta. Por exemplo, cálculos ponderados podem ser realizados para obter uma nova versão da imagem usando pesos diferentes para os canais de cor. As transformações lineares também podem ser aplicadas para alterar o contraste ou brilho da imagem. Além disso, os filtros podem ser aplicados para suavizar ou melhorar certas características da imagem.
Depois de processar a imagem, o resultado é exibido novamente usando a função cv2_imshow(), permitindo uma comparação entre a imagem original e a imagem processada.
Para visualizar os resultados e interagir com as janelas, o comando cv2.waitKey(0) é usado, que aguarda até que uma chave seja pressionada. Isso permite que o usuário observe os resultados antes de proceder.
Finalmente, a função cv2.destroyAllWindows() é chamada para fechar todas as janelas abertas pelo programa.
Este código é apenas um exemplo básico e pode ser expandido e adaptado de acordo com necessidades específicas de processamento de imagens. As técnicas apresentadas são fundamentais no campo do processamento de imagens e têm diversas aplicações em áreas como visão por computador, reconhecimento de padrões e processamento médico de imagens.
