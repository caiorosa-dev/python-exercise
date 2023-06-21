# Exercícios de Python
### Estes exercicios representam um estudo realizado na aula de Introdução a Ciência da Computação, a qual foi instigado aos alunos a criação deste repositório com alguns códigos em Python.

O código presente no arquivo `Exemplo_Morfologia.ipynb` representa exemplos de funções e algoritmos utilizados na grande área de visão computacional. 

Primeiramente no topo do código, são importados os módulos `cv2` (Biblioteca para tratamento de imagens) e `numpy` (Biblioteca com funções matemáticas). Além de importar o `cv2_imshow` que é responsável por exibir as imagens no terminal de execução do Google Colab. Em seguida é utilizada a biblioteca `OpenCV` para realizar o carregamento dos arquivos (imagens) para a memória, tornando possível a manipulação destas. 
A altura e a largura da imagem `j.png` são armazenadas em variáveis.

Em seguida é criado um kernel, que é um elemento estruturante, esta variável se trata de um array 5x5 preenchido com 1 em todos os seus valores (Nesta parte é feito uso da biblioteca `numpy`).

O algoritmo então executa operações morfológicas utilizando o kernel definido anteriormente. Estas são Erosão, Dilatação, Gradiente, Abertura e Fechamento. Cada operação destas é aplicada á imagem `j.png` e os resultados são armazenados em variáveis.

No fim do código, as imagens são exibidas através do método `cv2_imshop()` (adaptado para utilização no Google Colab).

Vale resaltar o porque destas funções morfológicas existirem. Elas são utilizadas, como dito anteriormente, na área de visão computacional, e realizam a parte do tratamento da imagem, melhorando a imagem para ser posteriormente processada nos algoritmos de inteligência artificial. Uma breve explicação de como cada operação morfológica funciona:
- Todas as operações são baseadas no elemento estruturante (kernel), o qual serve como um filtro.

| Operação   | Descrição                                                                                                                             |
|------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Erosão     | Reduz o tamanho do objeto (Remove pixels de sua borda)                                                                                |
| Dilatação  | Aumenta o tamanho do objeto (Adiciona pixels a sua borda)                                                                             |
| Abertura   | Executa uma erosão e posteriormente uma dilatação, é utilizada para remover ruídos e objetos pequenos.                                |
| Fechamento | É o inverso da abertura, realizando uma dilatação e depois uma erosão. É utilizado para preencher lacunas e remover pequenos buracos. |
| Gradiente  | Realiza a diferença entre a erosão e a dilatação. Geralmente utilizado para destacar as bordas de objetos na imagem.                  |
