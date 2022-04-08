# Aurora

Rede neural convolucional que prediz o resultado de benignidade ou malignidade  a partir de uma imagem digitalizada de um aspirado por agulha fina (FNA) de uma massa mamária.  

Dados de treino:

conjunto de dados do câncer de mama em Wisconsin (diagnóstico)

Fonte:

Criadores do conjunto de dados:

1. Dr. William H. Wolberg, Departamento de Cirurgia Geral da
Universidade de Wisconsin, Centro de Ciências Clínicas
Madison, WI 53792
wolberg '@' eagle.surgery.wisc.edu

2. W. Nick Street, Departamento de Ciências da Computação da
Universidade de Wisconsin, 1210 West Dayton St., Madison, WI 53706
street '@' cs.wisc.edu 608-262-6619

3. Olvi L. Mangasarian, Departamento de Ciências da Computação da
Universidade de Wisconsin, 1210 West Dayton St., Madison, WI 53706
olvi '@' cs.wisc.edu


Informações do conjunto de dados:

Os recursos são calculados a partir de uma imagem digitalizada de um aspirado por agulha fina (FNA) de uma massa mamária. Eles descrevem as características dos núcleos celulares presentes na imagem. Algumas das imagens podem ser encontradas em [Web Link]

O plano de separação descrito acima foi obtido usando Multisurface Method-Tree (MSM-T) [KP Bennett, "Decision Tree Construction Via Linear Programming". Proceedings of the 4 Midwest Artificial Intelligence and Cognitive Science Society, pp. 97-101, 1992], um método de classificação que usa programação linear para construir uma árvore de decisão. Os recursos relevantes foram selecionados usando uma pesquisa exaustiva no espaço de 1-4 recursos e 1-3 planos de separação.

O programa linear real usado para obter o plano de separação no espaço tridimensional é descrito em: [KP Bennett e OL Mangasarian: "Robust Linear Programming Discrimination of Two Linearly Inseparable Sets", Optimization Methods and Software 1, 1992, 23- 34].


Informação de Atributo:

1) ID número
2) Diagnóstico (M = maligno, B = benigno)
3-32)

Dez características de valor real são calculadas para cada núcleo celular:

a) raio (média das distâncias do centro aos pontos no perímetro)

b) textura (desvio padrão dos valores da escala de cinza)

c) perímetro

d) área

e) suavidade (variação local nos comprimentos dos raios)

f) compacidade (perímetro ^ 2 / área - 1,0)

g) concavidade (severidade das porções côncavas do contorno)

h ) pontos côncavos (número de porções côncavas do contorno)

i) simetria

j) dimensão fractal ("aproximação da linha costeira" - 1)



Requisitos de desenvolvimento para dados sensíveis:

Privacidade


Projeto de sistema

Arquitetura de software : Para obter o máximo de provacidade todos os testes das camadas neurais utilizarão o poder de processamento da sua máquina e nenhum dado de pacientes serão enviados aos nossos servidores.(On-device intelligence).

Design da interface do usuário: Para UX, construíremos nas 10 heurísticas de usabilidade de Jakob Nielsen .

Implementação de sistema
Tecnologias utilizadas:

TensorFlow

Bootstrap

Jquery



