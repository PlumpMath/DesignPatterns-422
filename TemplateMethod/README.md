# Template Method

## Descrição

O template method deve ser utilizado quando temos um algoritmo em que alguns do seus passos podem ser personalizados. Esses passos passiveis de customização devem ser abstratos permitindo sua implementação nas subclases.

"Define the skeleton of an algorithm in an operation, deferring some steps to subclasses. Template Method lets subclasses redefine certain steps of an algorithm without changing the algorithm's structure" by GOF

"The general idea of the Template Method pattern is to build an abstract base class with a skeletal method. This skeletal method (also called a template method) drives the bit of the processing that needs to vary, but it does so by
making calls to abstract methods, which are then supplied by the concrete subclasses." by Design Patterns in Ruby

<div align="center">
    <img src="http://s21.postimg.org/e5kzh8c5j/template_method_class_diagram.png"/>
    <p style="font-weight: bold;">Diagrama de classe - TemplateMethod</p>
</div>

## Participantes

+ **AbstractClass**
 + Define operações abstratas que devem ser definidas por subclasses concretas
 + Implementa templateMethod definindo o esqueleto do algoritmo. Esse algoritmo chama as operações primitivas (abstratas).
+ **ConcretClass**
 + Implementa as operações primitivas para realizar as etapas especificas do algoritmo.