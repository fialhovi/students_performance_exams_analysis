![Students Performance Exams](https://github.com/fialhovi/students_performance_exams_analysis/assets/104800356/eba2c8aa-f13d-47fe-8d1d-2150b95f33cf)

# EDA Students performance exams

## 🔎 **Sobre o projeto**

O objetivo deste projeto é informar as descobertas feitas durante as análises uni e multivariadas da performance de 1000 estudantes em um contexto escolar norte-americano em três exames, Matemática (_Math_), Leitura (_Reading_) e Escrita (_Writing_), buscando entender os seus perfis, analisando as suas pontuações e as variáveis que podem ter alguma relação com os seus desempenhos.

## 📄 **Data source**

O arquivo CSV utilizado está disponível neste repositório e pode ser baixado na plataforma Kaggle a partir do seguinte [_link_](https://www.kaggle.com/datasets/spscientist/students-performance-in-exams). Infelizmente, os dados são fictícios, não nos permitindo trazer _insights_ para a vida real.

Todo o projeto foi desenvolvido em Python com as bibliotecas Pandas, NumPy e Seaborn.

## 📝 **Dataset overview**

* O _dataset_ possui 1000 linhas e 8 colunas.
* Não há valores nulos ou linhas duplicadas.
* Possui apenas 2 _dtypes_: _object_ e _int64_.
* As palavras nos nomes das colunas vieram separadas por espaços e, seguindo boas práticas, foram substituídos por _underscore_.
* A mediana e a média das notas estão retornando valores muito próximos, o que pode indicar, a princípio, que há poucos ou nenhum _outlier_ a ser tratado.

# **Análise dos dados**

## 📊 **Análise univariada**

Aqui, vamos analisar cada variável de modo a entendermos quais são as características com maior e menor frequências.

**1.1. A nossa amostra contém um número ligeiramente maior (36 a mais) de estudantes mulheres do que de homens**


![gender](https://github.com/fialhovi/students_performance_exams_analysis/assets/104800356/1ae75b30-9808-4ddd-b1e2-48a9408251a4)


**1.2. Para raça/etnia, o grupo C (White - Any other White background) aparece como o mais numeroso, enquanto o grupo A (White - British) apresenta o menor número de estudantes**


![race](https://github.com/fialhovi/students_performance_exams_analysis/assets/104800356/f17da039-e395-4ccf-a22d-503619477e4e)


Com algumas buscas, descobri qual grupo racial é representado por cada letra:

* Group A - White - British
* Group B - White - Irish
* Group C - White - Any other White background
* Group D - Mixed - White and Black Caribbean
* Group E - Mixed - White and Black African
* Group F - Mixed - White and Asian
* Group G - Mixed - Any other mixed background

Também é importante notar que os grupos F e G não aparecem em nossa amostra.

**1.3. Poucos pais possuem um 'master's degree' (mestrado) ou mesmo um 'bachelor's degree' (bacharelado), enquanto a maioria possui 'some college' (alguma faculdade) ou um 'associate's degree' (diploma). Isso significa que a maior parte dos pais dos estudantes na nossa amostra não tiveram tanto tempo em espaços de educação formal**

![parents](https://github.com/fialhovi/students_performance_exams_analysis/assets/104800356/bbdee83b-4d87-45a9-a0c6-bea5c1727db3)

**1.4. Mais da metade dos estudantes recebe um almoço normal, mas preocupa analisar que aproximadamente 355 estudantes recebem um almoço reduzido ou sequer almoçam**

![lunch](https://github.com/fialhovi/students_performance_exams_analysis/assets/104800356/c031b07d-bc50-4f9f-872e-d4ca9f206c05)

**1.5. Mais de 60% dos estudantes não realizaram o curso preparatório para o teste**

![test](https://github.com/fialhovi/students_performance_exams_analysis/assets/104800356/a6b7c0be-f6e7-4794-ac54-43aeac6d7115)

**1.6. A maior parte das notas de Matemática (_Math_) estão concentradas entre 50 e 80, com uma média de 66**

![math](https://github.com/fialhovi/students_performance_exams_analysis/assets/104800356/890c1a03-7745-4c65-b2d0-c03ff69d6535)

**1.7. A maior parte das notas de Leitura (_Reading_) estão concentradas entre 50 e 80, com uma média de 69**

![reading](https://github.com/fialhovi/students_performance_exams_analysis/assets/104800356/7e01fc17-6d0b-402f-84d7-5072c502a0ab)

**1.8. A maior parte das notas de Escrita (_Writing_) estão concentradas entre 50 e 80, com uma média de 68**

![writing](https://github.com/fialhovi/students_performance_exams_analysis/assets/104800356/2ca52750-8220-4b39-840b-f96953c39156)

## 📈 **Análise multivariada**

**2.1. Correlação entre as notas das provas**

![s1](https://github.com/fialhovi/students_performance_exams_analysis/assets/104800356/6a4c8167-64ad-4957-adae-a722788c0358)

As notas de Leitura (_Reading_) e Escrita (_Writing_) apresentaram uma correlação positiva bastante forte (0.95), e Matemática (_Math_) também apresentou uma forte correlação positiva com Leitura (0.82) e Escrita (0.8).

### ✔️ Aprovação nas disciplinas

De modo geral, as escolas no Brasil adotam uma média de 5 para aprovação nas disciplinas. Aqui, também vou adotar esse sistema para checar a relação entre as demais variáveis e a quantidade de aprovações.

**2.2. Quantidade de aprovados nas 3 disciplinas**

O total de estudantes aprovados nas 3 disciplinas é: 812.

Isso representa um percentual bem alto de nossa amostra, com mais de 80% de aprovados.

**2.3. Aprovação por disciplina**

* Em **Matemática**, mais de 85% (865) dos estudantes foram aprovados.
* Em **Leitura**, mais de 90% (910) dos estudantes foram aprovados.
* Em **Escrita**, mais de 88% (886) dos estudantes foram aprovados.

Aqui, podemos observar que todas as disciplinas tiveram uma grande quantidade de estudantes aprovados, variando entre 85 e 90%, aproximadamente.

**2.4. Relação entre aprovação e demais variáveis**

**2.4.1. Gênero**

De modo geral, tivemos uma quantidade maior de estudantes mulheres aprovadas em relação a estudantes homens.

Matemática foi a única disciplina em que mais estudantes homens foram aprovados do que mulheres, em Escrita, por sua vez, o número de estudantes mulheres aprovadas foi consideravelmente maior.

**2.4.2. Raça/etnia**

Para todas as disciplinas, o Grupo E (Mixed - White and Black African) apresenta uma taxa de aprovação maior do que os outros, o Grupo A (White - British), por outro lado, apresenta a menor.

**2.4.3. Nível de escolaridade dos pais**

Nos casos em que o nível de escolaridade dos pais era mestrado ('master's degree'), houve uma maior taxa de estudantes aprovados para todas as disciplinas, para apenas um ensino médio ('some high school' e 'high school'), por sua vez, houve menor taxa de aprovação. A diferença de taxa de aprovação para esses dois grupos na disciplina Escrita foi a maior (81,1% de ensino médio ('high school') aprovados e 98,3% de mestrado aprovados).

Desse modo, em nossa amostra, podemos perceber que quanto maior o nível de escolaridade dos pais, maior a taxa de aprovação.

**2.4.4. Almoço**

Esta variável parece ser a com maior relação com a aprovação dos estudantes. De modo geral, 88% dos estudantes que tiveram um almoço padrão foram aprovados, enquanto apenas 68,7% dos que tiveram um almoço reduzido ou nenhum foram aprovados. A maior distância entre essas porcentagens, inclusive, foi em Matemática.

Assim, fica evidente a importância de uma boa nutrição dos estudantes para o seu melhor desempenho em sala de aula.

**2.4.5. Curso preparatório para o teste**

De modo geral, os estudantes que completaram o curso apresentaram uma taxa bem maior de aprovação (89,9%) em comparação com os que não realizaram (76,3%). Isso parece apontar para a importância da implementação de mais atividades para o desenvolvimento dos estudantes e consequente aumento de seus desempenhos.
