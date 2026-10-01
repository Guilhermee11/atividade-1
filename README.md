Guilherme de Souza Dutra 45604061

O id(lista) deve permanecer o mesmo durante essas operações, porque estamos modificando o mesmo objeto lista, em vez de criar outra lista.

Já os id() dos valores podem mudar ou permanecer iguais dependendo da operação. Isso ocorre porque inteiros são objetos e a atribuição/remoção pode fazer com que a lista passe a referenciar objetos diferentes.

Respostas para colocar no trabalho

a) O id() da lista mudou durante as operações? O que isso indica?

Não. O id() da lista permaneceu o mesmo durante as operações. Isso indica que append(), insert(), remove(), pop(), alteração de elementos e clear() modificaram a mesma lista existente, sem criar um novo objeto lista.

b) O que aconteceu com os elementos quando novos valores foram adicionados?

Quando usamos append() ou insert(), novos valores foram adicionados à lista. Os elementos que já estavam nela continuaram existindo, apenas mudando de posição no caso do insert().

c) O que acontece com a referência de um elemento quando ele é removido da lista?

Quando um elemento é removido, a lista deixa de manter uma referência para aquele objeto naquela posição. O objeto pode continuar existindo se houver outra referência apontando para ele; caso contrário, poderá ser posteriormente descartado pelo gerenciamento de memória do Python.

d) Ao alterar um elemento da lista, o id() desse elemento permaneceu igual? Explique o resultado observado.

o elemento que estava na posição 0 é substituído por outro objeto, o valor 100. Portanto, o id() observado nessa posição pode mudar. A lista continua sendo o mesmo objeto, mas sua referência naquela posição foi alterada.

e) Por que dizemos que uma lista em Python é um objeto mutável?

Uma lista é considerada mutável porque seu conteúdo pode ser alterado depois que ela foi criada. Podemos adicionar, remover ou substituir elementos sem precisar criar uma nova lista.

f) Qual é a diferença entre alterar o conteúdo de uma lista e criar uma nova lista?

Alterar o conteúdo modifica o próprio objeto existente, mantendo seu id(). Por exemplo:

lista.append(40)
nova_lista = lista + [40]
