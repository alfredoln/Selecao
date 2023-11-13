Inicialmente é utilizado a biblioteca glob para verificação dos arquivos .xml, assim é utilizado a função for para extrair de cada arquivo somente as informações pertinentes.

Com essas informações é utilizado função pandas para gerar um dataframe e salvar o resultado em um arquivo .csv.

Dando sequência é carregado o arquivo .csv, verificado as informações se existe alguma entrada nula. Em seguida é verificado as imagens e realizado o processamento e normalização dos dados para construção de um modelo deep learning.

Depois de analisar as imagens, e com base nelas, construir um modelo para detecção, assim dando sequência ao processo é adicionado uma geolocalização, nesse caso foi utilizado a função for para atribuir de “maneira aleatória” um referido estado da região Nordeste para cada linha da base de dados.

Em seguida utilizado novamente a função for, primeiro, para contabilizar quantos carros temos de cada estado presentes nessa base de dados e armazenar essa informação em variáveis, e segundo, para anexar esses valores das variáveis em uma lista denominada nordeste.

É adquirido a informação de longitude e latitude do todo o Brasil e separado as informações que serão utilizadas, no caso informações referente aos estados brasileiros.

Com todas essas informações, utilizamos a biblioteca plotly para gerar um mapa da região Nordeste com a quantidade de carro em circulação de cada estado.

É possível utilizar o modelo gerado para detectar placas de carro e cruzar com as informações geradas com os seguintes objetivos:
•	Saber se o carro em questão se encontra no seu estado domicílio ou não;
•	Mapear o caminho percorrido por um veículo, adaptando um grafo de menor caminho;
•	Identificar a existência de carros clonados em outros estados;
