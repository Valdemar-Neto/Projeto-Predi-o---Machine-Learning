# Predição de desistência de alunos da disciplina LOP na Escola de Ciências e Tecnologia da UFRN - Projeto de Machine Learning

## Introdução
Imagine um projeto inovador na Escola de Ciência e Tecnologia da Universidade Federal do Rio Grande do Norte, que utiliza aprendizado de máquina para prever se um aluno que submete a primeira lista de exercícios da disciplina de Lógica de Programação tem maior probabilidade de evadir a matéria ao chegar na lista 10. Este projeto revolucionário busca antecipar e combater a evasão escolar, promovendo uma educação mais eficiente e eficaz.

A equipe de pesquisa e desenvolvimento desse projeto está empregando técnicas avançadas de machine learning, usando um conjunto de dados abrangente e atualizado, composto por informações acadêmicas dos alunos matriculados na disciplina de Lógica de Programação ao longo dos últimos anos. Esses dados incluem variáveis relevantes, como o desempenho nas listas anteriores, notas em provas, frequência nas aulas, histórico acadêmico e demais características pessoais dos estudantes.

Com base nesse conjunto de dados, o modelo de machine learning é treinado para analisar e identificar padrões que possam indicar quais alunos têm maior probabilidade de evadir a matéria após a primeira lista de exercícios. O algoritmo desenvolvido é capaz de extrair informações complexas e sutis dos dados, criando uma representação estatística dos fatores que influenciam na evasão escolar.

Ao utilizar esse modelo preditivo, os professores e coordenadores da disciplina de Lógica de Programação podem identificar antecipadamente os alunos em risco de evasão e implementar estratégias personalizadas para auxiliá-los. Isso pode envolver o oferecimento de apoio acadêmico adicional, orientação vocacional, aconselhamento psicológico ou outras ações preventivas. O objetivo é intervir de maneira oportuna, fornecendo o suporte necessário para melhorar as chances de sucesso dos alunos e reduzir a taxa de evasão.

Além disso, o projeto também permite uma visão mais ampla do cenário da disciplina, permitindo que a instituição identifique possíveis melhorias no currículo, métodos de ensino ou até mesmo no ambiente acadêmico como um todo. Através do monitoramento contínuo e da análise dos resultados obtidos, a universidade pode adaptar suas abordagens educacionais, oferecer recursos adicionais e criar políticas mais eficazes para aumentar a retenção dos alunos.

Com o Projeto de Machine Learning de Previsão de Evasão em Lógica de Programação, a Escola de Ciência e Tecnologia da Universidade Federal do Rio Grande do Norte está liderando o caminho para uma educação mais personalizada e centrada no aluno. Essa iniciativa pioneira visa garantir que nenhum aluno seja deixado para trás, proporcionando oportunidades iguais e ajudando a construir um futuro promissor para todos os estudantes.
### Identificação 
| [<img src="https://user-images.githubusercontent.com/108936921/231314406-7d757d0e-c097-416c-bb28-6d830ea41d2f.png" width=115><br><sub>Valdemar Gonçalves Pereira Neto<br>20210036908</br></sub>](https://github.com/Valdemar-Neto)<br> ⚽👨‍💻🐧🖥️| 
| :---: | 

* Esse é o link para o vídeo explicativo do projeto da disciplina: https://youtu.be/1xo92waKQ2Q

### Informações Gerais 
Sem dúvidas, um dos principais problemas que afetam os índices estudantis em todo territorio brasileiro é evasão escolar, isso é perceptível muito nas universidades federais brasileiras, onde muitos universitários largam a máteria antes mesmo da metade do semestre letivo. Este trabalho teve como finalidade estudar, a partir da base de dados fornecida pelo Prof. Dr. Orivaldo Santana, predizer se determinado estudante submetia a lista 10 da disciplina de Lógica de Programação (LOP) a partir da lista 1. Esse processo foi também utilizado para anlisar o mesmo objetivo com as listas 11 e lista 12.
A base de dados do lop é compostas por muitas linhas e colunas, em que cada linha é caracterizada por um atributo importante para á análise. Tendo como classes principaiis:
- Class_id
- user_id
- qtdList
- percentList
- medialist
- aprovado
- ateLista
- totalErrorLN
- totalAcertLN
- acert_100LN
- total_submLN
- totalQuestLN
- subm/questLN
- timeInSecoundsLN
- submeteuLN
- aprovadoListaN
- medialistN
- percentErrorLN
- percentAcertLN
- percentAcert100LN
- time/submLN

Onde N é o numero da lista. Ex.: 01,02,03,...,N.

## Metodologia 
A partir da explanação das aulas foi possível utilizar de alguns métodos para análiar os dados. Utilizando da biblioteca pandas no python, pode-se fazer algumas alterações e escolhas necessárias no banco de dados fornecido. Após estudar a base de dados, parti para ihteração entre o python o banco de dodos, onde foi possível constatar que a base de dados estava desbalanceada, tornando o resultado final pendendo para um dos lados. Nesse sentido, foi necessario balancear o banco de dados, utilizando os próprios dados, para gerar valores aleatórios até que a base estivesse nivelada.
Após o nivelamento, parti para a escolha das classes para trabalhar e ao printar na tela essas classes escolhidas, notei que era preciso normalizá-las, para isso utilzei a biblioteca sickit-learn com o método MinMaxScaler para normalizar os valores entre 0 e 1. O método que escolhi para treinar a rede foi o Suport Vector Machine (SVM). Após o treinamento foi possível constatar os seguintes resultados, utilizando o metodo a classe metrics da biblioteca mencionada anteriormente:
- Acurácia: 95.03 %
- Balanço médio da acurácia de: 94.87%
- Precisão do modelo: 95.6%

Para esses resultados, foram escolhidas as seguintes classe:
- Para o treinamento (X): 'totalAcertL01','aprovadoLista01','subm/questL01','timeInSecoundsL01','time/submL01'
- Para a predição (Y): 'SubmeteuL10'
## Códigos 
<div align = "left">
  <img src="https://github.com/Valdemar-Neto/Projeto-Predi-o---Machine-Learning/assets/108936921/c8340988-3e68-4e84-a8f2-24570397ae7a">  
</div>

<div align = "left">
  <img src="https://github.com/Valdemar-Neto/Code-Recognition-color-/assets/108936921/e9be41ce-d8a0-4ea1-bb4e-e859efef085c">  
</div>

<div align = "left">
  <img src="https://github.com/Valdemar-Neto/Code-Recognition-color-/assets/108936921/a990ab9c-28db-4d21-acf2-47b8e51ebeba">  
</div>

<div align = "left">
  <img src="https://github.com/Valdemar-Neto/Code-Recognition-color-/assets/108936921/e23995ad-47dc-488d-87eb-bf9025b3aa8f">  
</div>

<div align = "center">
  <img src="https://github.com/Valdemar-Neto/Code-Recognition-color-/assets/108936921/56d3eb2c-b0b4-4ede-ac79-8ccc1e648e7b">  
</div>

<div align = "left">
  <img src="https://github.com/Valdemar-Neto/Code-Recognition-color-/assets/108936921/3a08f038-546a-4a4a-8b39-d1f195188434">  
</div>

<div align = "left">
  <img src="https://github.com/Valdemar-Neto/Code-Recognition-color-/assets/108936921/7abbf54d-0620-4d7b-b090-632f8d39ff31">  
</div>

<div align = "left">
  <img src="https://github.com/Valdemar-Neto/Code-Recognition-color-/assets/108936921/036fb115-7dc7-4832-a314-6f8c4390f683">  
</div>

Link para o código no Google Colaboratory
https://colab.research.google.com/drive/15Aoc8NnzyHLZQwizSpBMH0JL2JcxhVrd?usp=sharing

## Experimentos 
* Descrever em detalhes os tipos de testes executados.
* Para o primeiro experimento, fiz as análises a partir da lista 1 e a lista 10, tendo como classes estudados na predição as que foram anteriormente mencionadas, como  Para o treinamento (X): 'totalAcertL01','aprovadoLista01','subm/questL01','timeInSecoundsL01','time/submL01' e para a predição (Y): 'submeteuL10' e eles são bem autoexplicativos pelos seus nomes. O resultado obtidos a partir da seção anterior foram bem satisfatórios pois o modelo foi bem treinado com uma precisão de 95%. Este resultado foi muito louvado pois foi possível utilizazr esse mesmo modelo ajalisasr outras listas a partir da lista 01.
* Resultados da lista 1 para lista 10:
  * Acurácia = 95.03%
  * Precisão = 95.60%
    
* Resultados da lista 1 para lista 11:
  * Acurácia = 65%
  * Precisão = 76.62%
  
* Resultados da lista 1 para lista 12:
  * Acurácia = 60%
  * Precisão = 76.1%

## Conclusão 
Com base nos resultados obtidos pelo Projeto de Machine Learning de Previsão de Evasão em Lógica de Programação na Escola de Ciência e Tecnologia da Universidade Federal do Rio Grande do Norte, podemos afirmar que os esforços foram bem-sucedidos na predição da evasão dos alunos na disciplina.

Ao aplicar técnicas avançadas de aprendizado de máquina em um conjunto de dados abrangente e atualizado, o modelo desenvolvido mostrou-se capaz de identificar com precisão os alunos com maior probabilidade de evadir a matéria após a submissão da primeira lista de exercícios. Essa previsão precoce permitiu que a equipe docente e os responsáveis pelo acompanhamento acadêmico interviessem de maneira proativa, oferecendo o suporte necessário para melhorar as chances de sucesso dos alunos.

Os resultados positivos desse projeto vão além da simples identificação de alunos em risco de evasão. Através do monitoramento contínuo e da análise dos dados, foi possível identificar padrões e fatores que contribuem para a evasão, fornecendo insights valiosos para aperfeiçoar o currículo, os métodos de ensino e a estrutura acadêmica da disciplina de Lógica de Programação. Essas melhorias contribuíram para aumentar a retenção dos alunos e promover uma experiência educacional mais enriquecedora e eficaz.

O sucesso desse projeto destaca o potencial transformador da aplicação de técnicas de machine learning na área da educação. Ao utilizar modelos preditivos, as instituições de ensino podem tomar medidas proativas para combater a evasão, identificar áreas de melhoria e adaptar suas abordagens educacionais de acordo com as necessidades dos alunos.

O Projeto de Machine Learning de Previsão de Evasão em Lógica de Programação na Escola de Ciência e Tecnologia da Universidade Federal do Rio Grande do Norte é um exemplo inspirador de como a tecnologia pode ser aproveitada para criar um ambiente acadêmico mais inclusivo e orientado para o sucesso dos estudantes. Com base nos resultados alcançados, é evidente que a implementação desse projeto traz benefícios tangíveis para a universidade, os professores e, acima de tudo, para os alunos, garantindo que cada estudante tenha a oportunidade de alcançar seu potencial máximo na disciplina de Lógica de Programação.
