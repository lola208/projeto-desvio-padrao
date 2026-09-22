# Projeto: Análise de Dados com Média e Desvio Padrão
2
 
3
## Descrição
4
 
5
Este projeto foi desenvolvido para analisar a distribuição de um conjunto de dados utilizando conceitos de estatística com Python e NumPy. O objetivo é calcular a média, o desvio padrão amostral e visualizar os dados por meio de um histograma.
6
 
7
## Dados Utilizados
8
 
9
```python
10
dados = [5, 6, 6, 7, 7, 7, 8, 8, 9, 10]
11
```
12
 
13
## Cálculos
14
 
15
### Média
16
 
17
A média dos dados é:
18
 
19
```python
20
7.3
21
```
22
 
23
### Desvio Padrão Amostral
24
 
25
O desvio padrão amostral calculado com NumPy é:
26
 
27
```python
28
1.49
29
```
30
 
31
## Intervalo Média ± Desvio Padrão
32
 
33
- Limite inferior: 5.81
34
- Limite superior: 8.79
35
 
36
Esses valores são obtidos através das fórmulas:
37
 
38
```python
39
limite_inferior = média - desvio_padrão
40
limite_superior = média + desvio_padrão
41
```
42
 
43
## Código
44
 
45
```python
46
import numpy as np
47
import matplotlib.pyplot as plt
48
 
49
dados = [5, 6, 6, 7, 7, 7, 8, 8, 9, 10]
50
 
51
media = np.mean(dados)
52
desvio_padrao = np.std(dados, ddof=1)
53
 
54
limite_inferior = media - desvio_padrao
55
limite_superior = media + desvio_padrao
56
 
57
print("Média:", media)
58
print("Desvio Padrão:", desvio_padrao)
59
print("Limite Inferior:", limite_inferior)
60
print("Limite Superior:", limite_superior)
61
 
62
plt.hist(dados, bins=6, color='skyblue', edgecolor='black')
63
plt.axvspan(limite_inferior, limite_superior,
64
color='yellow', alpha=0.4,
65
label='Média ± Desvio Padrão')
66
plt.axvline(media, color='red', linestyle='--',
67
label='Média')
68
 
69
plt.legend()
70
plt.title('Histograma dos Dados')
71
plt.xlabel('Valores')
72
plt.ylabel('Frequência')
73
plt.show()
74
```
75
 
76
## O que a faixa representa?
77
 
78
A faixa destacada entre a média menos o desvio padrão e a média mais o desvio padrão mostra a região onde estão concentrados a maior parte dos valores do conjunto de dados. Ela ajuda a visualizar a dispersão dos dados em torno da média.
79
 
80
## Conclusão
81
 
82
A média fornece uma noção central dos dados, mas o desvio padrão permite compreender o quanto os valores variam em relação a essa média. Juntos, esses indicadores oferecem uma análise mais completa da distribuição dos dados.
83
 
84
# Reflexão Final
85
 
86
## Parte que está clara e fácil de entender
87
 
88
A apresentação dos dados e dos resultados está organizada de forma simples e objetiva. O leitor consegue identificar facilmente a média, o desvio padrão e os limites do intervalo analisado.
89
 
90
## Parte que pode confundir alguém
91
 
92
A interpretação do desvio padrão pode ser difícil para quem nunca estudou estatística ou programação.
93
 
94
## Como melhorar
95
 
96
Adicionar comentários no código e exemplos práticos explicando o significado do desvio padrão e da dispersão dos dados, tornando a análise mais acessível para novos leitores.
