# Fala Senado

Projeto que busca analisar os pronunciamentos de senadores e senadoras em Python com técnicas de Processamento de Linguagem Natural, Linguística de Corpus, Análise de Sentimento e por aí afora.

## Começando

Essas instruções vão te ajudar a pegar uma cópia do projeto e fazer ela funcionar na sua máquina para testar.

### Pré-requisitos

Além do Python 3.6+, é necessário um ambiente com as seguintes bibliotecas e suas respectivas dependências:
 - pandas
 - nltk
 - sklearn
 - matplotlib
 - requests
 - lxml
 - beautifulsoup
 - unidecode
 
### Instalando

É preciso configurar um ambiente com os pré-requisitos acima.

## Executando

Para que os exemplos de análise nesse repositório funcionem, é preciso salvar todos os scripts numa mesma pasta e executá-los numa determinada ordem. 
Os primeiros scripts vão buscar os objetos de análise na internet, são eles:
 - lista_senadores: salva um xml temporário e um csv com dados básicos de cada senador(a). 152kb+ e 13kb+
 - lista_urls: salva um csv com os links de cada pronunciamento que será acessado. 2,6MB+
 - todos_textos: acessa os links e salva um csv com todos os pronunciamentos de maneira organizada. 400MB+
 - bow_partidos: a partir do csv maior, organiza um csv menor com os textos por partido para análise com bag of words (bow). 250MB+

Depois de salvar a base de dados, as análises podem ser feitas em qualquer ordem:
 - comp_freq: a partir dos bows dos partidos, compara a frequência relativa de termos nos pronunciamentos. 
 Exemplo: educação, saúde, segurança/todos partidos
![exemplo comp_freq](https://github.com/liquera/fala-senado/blob/master/comp_freq.png)

 
 - graf_termo: a partir do csv geral, faz um gráfico comparativo que mostra a evolução da frequência de determinado termo pelo tempo por partidos.
 Exemplo: educação/PT, MDB, PSDB
![exemplo graf_termo](https://github.com/liquera/fala-senado/blob/master/graf_termos.png)

 - tfidf: a partir do csv geral, vetoriza os termos de um partido por data e pontua com TF-IDF, revelando os termos mais importantes por data do partido escolhido.
 Exemplo: PT
![exemplo tfdif](https://github.com/liquera/fala-senado/blob/master/tfidf.png)
 
### Notas

Os scripts têm indicações de funcionamento dentro deles para maiores detalhes.
Não sou especialista em Python, muito menos em programação, qualquer ajuda é bem-vinda.

## Contribuições

O projeto ainda tá engatinhando, entre em contato para discutirmos possíveis contribuições.

## Licença

Esse projeto está licenciado sob os termos do AGPL 3.0 - veja o arquivo LICENSE para mais detalhes.
