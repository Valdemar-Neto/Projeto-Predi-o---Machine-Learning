# Predição de desistência de alunos da disciplina LOP na Escola de Ciências e Tecnologia da UFRN - Projeto de Machine Learning

# Título do Trabalho 

## Introdução

### Identificação 
| [<img src="https://user-images.githubusercontent.com/108936921/231314406-7d757d0e-c097-416c-bb28-6d830ea41d2f.png" width=115><br><sub>Valdemar Gonçalves Pereira Neto<br>20210036908</br></sub>](https://github.com/Valdemar-Neto)<br> ⚽👨‍💻🐧🖥️| 
| :---: | 

* Apresentar os membros da equipe (nome e mátricula). 
* Colocar o link para o vídeo da apresentação do trabalho. 

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


* Informar o link para acessar o código. 

## Experimentos 
* Descrever em detalhes os tipos de testes executados. 
* Descrever os parâmentros avaliados. 
* Explicar os resultados. 

## Conclusão 
* O trabalho atendeu aos objetivos? 
