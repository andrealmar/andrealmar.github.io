---
title: Operators and paradigm shift
description: Operators and paradigm shift
header: Operators and paradigm shift
---

https://coreos.com/blog/introducing-operators.html
https://itnext.io/wth-is-a-operator-lifecycle-manager-873cf1661b04

![](/img/foo_fighters_generator.png "Foo FIghters - Generator (single)")

- I believe we’re in the middle of a huge paradigm shift, in which Kubernetes and Operators will play a fundamental, new role.
- Kubernetes is not only a container Orchestrator, it is an Application Platform
- it’s not like infrastructure automation, service orchestration and automated recovery are anything new. The main point, though, is they were in different domains. This is exactly the reason why Operators matter: in Kubernetes world, everything belongs together
- Infrastructure == Kubernetes
- Service == Your Service
- Operational Intelligence == Operator
- What really matters, though, is that as long as our infrastructure is provided with the needed warranties, we can start building on top of it.
- Infrastructure Providers and Cloud Vendors are no longer competitors: they’re becoming customers/distributors.
- In a world where everybody is enabled to distribute the same piece of software, the difference stands in how you do it.
- The scenario today is: For software companies, building and maintaining cloud-native applications today is not a simple task - they must address significant complexities during the initial build and provide maintenance across siloed cloud footprints.
- Using Operators you can write software that runs across any cloud where Kubernetes runs.
- A Kubernetes application is an application that is both deployed on Kubernetes and managed using the Kubernetes APIs and kubectl tooling. Kubernetes Operators simplify application development for Kubernetes platforms by abstracting away complexities and coding human operational knowledge into applications, creating services that can function without human intervention.
- You write a software, package and make it available within the Kubernetes platform without knowing the details of the Kubernetes APIs.
- An Operator is a Kubernetes pattern that is extending the Kubernetes control plane with a custom Controller and Custom Resource Definitions that add additional operational knowledge of an application.
- The etcd Operator extends Kubernetes to handle operations such as backups and resizing etcd clusters. These are the type of tasks that normally have humans following written playbooks to fix deployments when they get paged at 4AM. The CoreOS philosophy was to automate solutions to eliminate operational toil for the future. If you’ve resized the cluster once, you’re going to need to resize it a million times. Why not teach the computer to do it for you?
- Eliminating Toil: https://landing.google.com/sre/book/chapters/eliminating-toil.html
-

Não…eu não vou escrever neste post sobre a ótima música do Foo Fighters, embora recomendo que você a escute =P. Estamos aqui para falar de uma função bastante legal na nossa linguagem de programação preferida: Os famosos Generators.

Em termo simples os `Generators` são funções que permitem a você declarar uma função que se comporta como um iterador, ou seja, que pode ser usado dentro de um loop for.

Simplificando mais ainda: Generators são uma forma simples de criarmos iteradores. Ele irá retornar um objeto (iterador) para que possamos iterar sobre este objeto (um valor de cada vez).

É muito simples criar uma função Generator, mas existem algumas peculiaridades. Por exemplo, nós usamos a declaração `yield` ao invés de `return`. Se a função contém ao menos uma declaração `yield` então ela se torna uma função Generator.

Um exemplo bem simples. Abra o seu interpretador Python e digite a função abaixo:

{% highlight go  %}
def generator():
    n = 1
    print("Essa  uma função Generator")
    yield n

    n += 1
    yield n

    n += 1
    yield n
{% endhighlight %}

Vamos agora, executar a função no interpretador Python:

{% highlight shell  %}
>>> # Retorna um objeto mas não executa a função imediatamente.
>>> a = generator()

>>> # Podemos iterar sobre os items usando next().
>>> next(a)

Essa  uma função Generator
1
>>> # Assim que a função executa o yield, ela é pausada e o controle da execução é transferido para quem a chamou.

>>> # Variáveis locais e os seus estados são "lembradas" durante as sucessivas chamadas à função.
>>> next(a)
2
>>> next(a)
3

>>> # Quando a função termina, a exceção StopIteration é levantada automaticamente.
>>> next(a)
Traceback (most recent call last):
...
StopIteration
>>> next(a)
Traceback (most recent call last):
...
StopIteration
{% endhighlight %}

Interessante notar que o valor da variável a no exemplo acima é lembrada durante cada chamada do método next(). Nós declaramos 3 yields, então o valor da variável a será lembrado por 3 vezes. Quando tentamos chamar next(a) pela 4a vez, veja o que acontece:

{% highlight python  %}
>>> # Quando a função termina, a exceção StopIteration é levantada automaticamente.
>>> next(a)
Traceback (most recent call last):
...
StopIteration
>>> next(a)
Traceback (most recent call last):
...
StopIteration
{% endhighlight %}

Uma exceção `StopIteration` é lançada, alertando que a iteração acabou. Ou seja, as variáveis locais NÃO são destruídas quando usamos o `yield`. O objeto Generator só pode ser iterado uma única vez. Se quisermos restartar o processo nós precisaremos criar um outro objeto Generator, por exemplo `b = generator()`.

Também podemos utilizar Generators dentro de um laço for diretamente. Isso porque o laço for também utiliza a função `next()` para iterar e automaticamente encerra a iteração quando a exceção `StopIteration` é lançada.

{% highlight bash  %}
>>> for item in generator():
...     print(item)
...
Essa é uma função Generator
1
2
3
>>
{% endhighlight %}

### Generators Expressions


As `Generators Expressions` facilitam à criação de Generators. Assim como uma função lambda cria uma função anônima, uma `Generator Expression` cria uma função Generator anônima. A sintaxe é bem parecida com as famosas `List Comprehensions` com o pequeno detalhe de que os colchetes `[ ]` são subsituídos pelos parênteses `()`.


{% highlight python  %}
list_comprehension = [1,2,3,4,5,6,7,8]
{% endhighlight %}

{% highlight python  %}
generator_expression = (1,2,3,4,5,6,7,8)
{% endhighlight %}

{% highlight python  %}
>>> x = [1, 2, 3, 4, 5, 6, 6, 8]
>>> x
[1, 2, 3, 4, 5, 6, 6, 8]
>>> generator_expression = (i for i in x)
>>> generator_expression
<generator object <genexpr> at 0x101812af0>
>>> list_comprehension = [i for i in x]
>>> list_comprehension
[1, 2, 3, 4, 5, 6, 6, 8]
>>>
{% endhighlight %}

Note no exemplo acima que a `List Comprehension` nos retorna a lista em si mas a `Generator Expression` nos retorna o objeto gerado: `<generator object <genexpr> at 0x101812af0>`.

A outra vantagem é que enquanto a `List Comprehension` gera a lista inteira, a `Generator Expression` gera um item de cada vez. Isso também é chamado de _lazy ou on demand generation of values_. E por consequência de ser lazy (preguiçosa), a `Generator Expression` consome bem menos memória sendo mais eficiente do que uma `List Comprehension`.

Espero que tenham gostado dessa explicação a respeito dos Generators.

See ya !!!
