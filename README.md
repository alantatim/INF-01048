# INF-01048 - Trabalho 1: Redes Neurais

<p align="justify">
  Arquivo README.md feito em Markdown sobre o Trabalho de Redes Neurais, o primeiro trabalho de quatro trabalhos, da cadeira Inteligência Aritifical de código INF-01048 da Universidade Federal do Rio Grande do Sul.
</p>

## Integrantes

<ol>
  <li>
    Alan Elias Prestes Tatim
    <ul>
      <li>
        00324874
      </li>
      <li>
        Turma B
      </li>
    </ul>
  </li>
  <li>
    Bruno Grohs Vergara
    <ul>
      <li>
        00324256
      </li>
      <li>
        Turma B
      </li>
    </ul>
  </li>
  <li>
    Erick Larratéa Knoblich
    <ul>
      <li>
        00324422
      </li>
      <li>
        Turma A
      </li>
    </ul>
  </li>
  <li>
    Pedro Arejano Scheunemann
    <ul>
      <li>
        00335768
      </li>
      <li>
        Turma A
      </li>
    </ul>
  </li>
</ol>

## Exercício 1:

<p align="justify">
Valores iniciais de b, w, valores de alpha e num_iterations que resultam na melhor execução da regressão linear:
b = -3, w = 1, alpha = 0.01 e num_iterations = 8500. O melhor erro quadrático médio obtido: 8.527708190982557.
</p>

## Exercício 2:

### Características dos Datasets:

<table>
  <tr>
    <td> &nbsp; </td>
    <th> Mnist </th>
    <th> Fashion-Mnist </th>
    <th> Cifar-10 </th>
    <th> Cifar-100 </th>
  </tr>
  <tr>
    <td> Classes </td>
    <td> 10 </td>
    <td> 10 </td>
    <td> 10 </td>
    <td> 100 </td>
  </tr>
  <tr>
    <td> Amostras </td>
    <td> 70000 </td>
    <td> 70000 </td>
    <td> 60000 </td>
    <td> 60000 </td>
  </tr>
  <tr>
    <td> Alturas </td>
    <td> 28 </td>
    <td> 28 </td>
    <td> 32 </td>
    <td> 32 </td>
  </tr>
  <tr>
    <td> Larguras </td>
    <td> 28 </td>
    <td> 28 </td>
    <td> 32 </td>
    <td> 32 </td>
  </tr>
  <tr>
    <td> Canais de Cor </td>
    <td> 1 </td>
    <td> 1 </td>
    <td> 3 </td>
    <td> 3 </td>
  </tr>
</table>

Referências:

<ul>
  <li>
    <a href="https://www.tensorflow.org/datasets/catalog/mnist?hl=pt-br" target="_blank"> Mnist </a>
  </li>
  <li>
    <a href="https://www.tensorflow.org/datasets/catalog/fashion_mnist?hl=pt-br" target="_blank"> Fashion-Mnist </a>
  </li>
  <li>
    <a href="https://www.tensorflow.org/datasets/catalog/cifar10?hl=pt-br" target="_blank"> Cifar-10 </a>
  </li>
  <li>
    <a href="https://www.tensorflow.org/datasets/catalog/cifar100?hl=pt-br" target="_blank"> Cifar-100 </a>
  </li>
</ul>

### Questão 1:

<p align="justify">
  Em quais datasets um perceptron simples (sem convolução e sem camadas ocultas) obtem uma
  acurácia acima de 80%?
</p>

<p align="justify">
  Sempre no dataset Mnist e nem sempre no dataset Fashion-Mnist, cuja acurácia oscila entre 0.78 e 0.82.
</p>

### Questão 2:

<p align="justify">
  Qual a acurácia máxima obtida no CIFAR-10? Qual modificação teve maior impacto positivo?
  Qual o maior desafio/dificuldade?
</p>

<p align="justify">
  A acurácia máxima obtida no dataset Cifar-10 oscila entre 0.67 e 0.69. A modificação que teve maior impacto positivo em relação à acurácia foi o acréscimo de redes convulcionais enquanto a modificação que     
  teve maior impacto positivo em relação à velocidade foi a execução de max poolings. O maior desafio/dificuldade foi o tempo entre as execuções.
</p>

### Questão 3:

<p align="justify">
  Foi possivel obter mais de 60% de acurácia no CIFAR-100? Qual modificação teve maior
  impacto positivo? Qual o maior desafio/dificuldade?
</p>

<p align="justify">
  Não foi posspível obter uma acurácia de valor maior de 60%. A modificação que teve maior impacto positivo em relação à acurácia foi o acréscimo de redes convulcionais enquanto a modificação que     
  teve maior impacto positivo em relação à velocidade foi a execução de max poolings. O maior desafio/dificuldade foi o tempo entre as execuções.
</p>

### Questão 4:

<p align="justify">
  Quais fatores (tanto das próprias redes quanto dos dados) levam as redes neurais a melhorarem o
  desempenho? E quais fatores tornam o desempenho pior?
</p>

<p align="justify">
  O uso do otimizador adam, camadas convolutivas, filtragem e max pooling levam as redes neurais a melhorarem o desempenho.
  A dimensão dos filtros e do max pooling foram 3x3 e 2x2, respectivamente, para todos os datasets.
  Contudo, o número de camadas convolutivas e de filtros é diferente entre os datasets do tipo Mnist e do tipo Cifar.
  16 filtros foram utilizados para os datasets Mnist e Fashion-Mnist enquanto múltiplos filtros foram usados para os datasets Cifar-10 e Cifar-100, visto que são os únicos com múltiplos canais de cores.
  O número de camadas convolutivas também é diferente entre os datasets: uma para o dataset Mnist, duas para o dataset Fashion-Mnist e quatro paras os datasets Cifar-10 e Cifar-100.
</p>

<p align="justify">
  A adição de camadas convolutivas, filtros e neurônios desnecessários tornam a execução muito mais lenta e não apresenta melhoras significativas, inclusive piorando em alguns casos.
</p>
