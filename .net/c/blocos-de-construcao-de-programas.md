# Blocos de construção de programas

> Os membros estáticos pertencem às classes e os membros de instância pertencem aos objetos \(instâncias de classes\). [\[1\]](https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/program-building-blocks)

## Membros

Existem vários tipos membros que uma classe pode conter[ \[1\]](https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/program-building-blocks), mas vale ressaltar dois deles:

1. **Constructor**: ações necessárias para inicializar instâncias da classe ou a própria classe;
2. **Finalizers**: ações executadas antes de instâncias da classe serem descartadas permanentemente.

### Acessibilidade do membros

Em relação a acessibilidade dos membros o C\# possuem três deles que são diferentes de outras linguagens:

1. `internal`;
2. `protected internal`;
3. `private protected`.

## Métodos

> O tipo de retorno de um método é `void` se ele não retornar um valor. [\[1\]](https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/program-building-blocks)

### Parâmetros

* Referência `ref`;
* Síada `out`;
* Matriz de parâmetros `params`.

### Sobrecarga

> A _sobrecarga_ de método permite que vários métodos na mesma classe tenham o mesmo nome, contanto que tenham assinaturas exclusivas. [\[1\]](https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/program-building-blocks)

## Construtores

Podem ser de dois tipos: instancia e estático.

> Construtores de instância podem ser sobrecarregados e ter parâmetros opcionais [\[1\]](https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/program-building-blocks)

Construtores de instância não podem ser herdados. Dessa forma quando uma classe filha não possuir construtor, será um construtor vazio sem parâmetros será fornecido automaticamente.

## Eventos

É um membro que permite a uma classe ou objeto forneça notificações.

## Finalizadores

> é um membro que implementa as ações necessárias para finalizar uma instância de uma classe [\[1\]](https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/program-building-blocks)

Normalmente utilizado para liberar recursos.

Eles não podem ter:

* Não podem ter parâmetros;
* Modificadores de acesso e
* Não podem ser invocados explicitamente.

Finalizadores são invocados automaticamente na coleta de lixo, com isso eles podem ser invocados a qualquer momentos. Dessa forma execução de finalizadores é não determinística. Por esse motivo a implementação de finalizadores deve ser efetuado quando não houver outras soluções viáveis.

> A instrução `using` fornece uma abordagem melhor para a destruição de objetos. [\[1\]](https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/program-building-blocks)



[\[1\]](https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/program-building-blocks)

### Referências bibliográficas

1. [https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/program-building-blocks](https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/program-building-blocks)

