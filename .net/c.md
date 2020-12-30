# C\#

Hello world em C\#

```csharp
using System;

class Hello
{
    static void Main()
    {
        Console.WriteLine("Hello, World");
    }
}
```

> Todos os tipos do C\#, incluindo tipos primitivos, como `int` e `double`, herdam de um único tipo de `object` raiz. [\[1\]](https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/)

`using` faze referência a um _namespace_

**namespace**

* > fornecem um meio hierárquico de organizar bibliotecas e programas [\[1\]](https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp)
* É a forma de realizar o `import` de outras "bibliotecas";
* Sem a utilização do `using` o código ficaria `System.Console.WriteLine`.

**`static`**

* Modificador do método. Indica que o método é estático.
* > métodos estáticos operam sem referência a um objeto específico [\[1\]](https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp)

### Tipos de veriáveis

#### Valor

> contêm diretamente seus dados [\[1\]](https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/)

Elas são dívididas em "_simple types_, _enum types_, _struct types_, _nullable value types_ and _tuple value types_" [\[1\]](https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/)

#### Referencia

> armazenam referências a seus dados, \[...\] conhecido como objetos. [\[1\]](https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/)

> é possível que duas variáveis referenciem o mesmo objeto e possíveis operações em uma variável afetem o objeto referenciado pela outra variável. [\[1\]](https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/)

Elas são dívididas em "_class types_, _interface types_, _array types_, and _delegate types_."[ \[1\]](https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/)

`delegate` é um tipo que é utilizado para atribuir métodos em variáveis.

### Programa

> Quando programas C\# são compilados, eles são fisicamente empacotados em assemblies. Os assemblies normalmente têm a extensão de arquivo `.exe` ou `.dll`[\[1\]](https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/)

### Tipos

Lista dos tipos existente em C\#

* _Generics_;
* Classes;
* _Structs_;
* _Interfaces_;
* _Enums_;
* _Nullable_;
* _Tuples_.

### Blocos de construção de programas

> Os membros estáticos pertencem às classes e os membros de instância pertencem aos objetos \(instâncias de classes\). [\[3\]](https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/program-building-blocks)

#### Membros

Existem vários tipos membros que uma classe pode conter[ \[3\]](https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/program-building-blocks), mas vale ressaltar dois deles:

1. **Constructor**: ações necessárias para inicializar instâncias da classe ou a própria classe;
2. **Finalizers**: ações executadas antes de instâncias da classe serem descartadas permanentemente.

#### Acessibilidade dos

Em relação a acessibilidade dos membros o C\# possuem três deles que são diferentes de outras linguagens:

1. `internal`;
2. `protected internal`;
3. `private protected`.

#### Métodos

> O tipo de retorno de um método é `void` se ele não retornar um valor. [\[3\]](https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/program-building-blocks)

#### Parâmetros

* Referência `ref`;
* Síada `out`;
* Matriz de parâmetros `params`.

[\[3\]](https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/program-building-blocks)

### Referências bibiográficas

1. [https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/](https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/#code-try-0)
2. [https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/types](https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/types)
3. [https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/program-building-blocks](https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/program-building-blocks)

