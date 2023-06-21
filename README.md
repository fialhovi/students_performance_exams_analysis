![Students Performance Exams](https://github.com/fialhovi/students_performance_exams_analysis/assets/104800356/eba2c8aa-f13d-47fe-8d1d-2150b95f33cf)

# EDA Students performance exams

## 🔎 **Sobre o projeto**

O objetivo deste projeto é informar as descobertas feitas durante as análises uni e multivariadas da performance de 1000 estudantes norte-americanos em três exames, Matemática (_Math_), Leitura (_Reading_) e Escrita (_Writing_), buscando entender os seus perfis, analisando as suas pontuações, e as variáveis que podem ter alguma relação com os seus desempenhos.

## 📄 **Data source**

O arquivo CSV utilizado está disponível neste repositório e pode ser baixado na plataforma Kaggle a partir do seguinte [_link_](https://www.kaggle.com/datasets/spscientist/students-performance-in-exams). Infelizmente, os dados são fictícios, por isso, foram utilizados apenas com o propósito de praticar.

Todo o projeto foi desenvolvido com Python e com as bibliotecas Pandas, NumPy e Seaborn.

## 📝 **Dataset overview**

* O _dataset_ possui 1000 linhas e 8 colunas.
* Não há valores nulos ou linhas duplicadas.
* Possui apenas 2 _dtypes_: _object_ e _int64_.
* As palavras nos nomes das colunas vieram separadas por espaços e foram substituídas por _underscore_.
* A mediana e a média das notas estão retornando valores muito próximos, não havendo _outliers_ a serem tratados.

# **Análise dos dados**

## 🔬 **Análise univariada**

Aqui, vamos analisar cada variável de modo a entendermos quais são as características mais frequentes.

**1. A nossa amostra contém um número ligeiramente maior (36 a mais) de estudantes mulheres do que de homens**


![gender](https://github.com/fialhovi/students_performance_exams_analysis/assets/104800356/1ae75b30-9808-4ddd-b1e2-48a9408251a4)


**2. Para raça/etnia, o grupo C aparece como o mais numeroso, enquanto o grupo A apresenta o menor número de estudantes**


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

**3. Poucos pais possuem um 'master's degree' (mestrado) ou mesmo um 'bachelor's degree' (bacharelado), enquanto a maioria possui 'some college' (alguma faculdade) ou um 'associate's degree' (diploma). Isso significa que a maior parte dos pais da nossa amostra não investiram tanto tempo em suas educações formais**

![parents](https://github.com/fialhovi/students_performance_exams_analysis/assets/104800356/bbdee83b-4d87-45a9-a0c6-bea5c1727db3)

**4. **
