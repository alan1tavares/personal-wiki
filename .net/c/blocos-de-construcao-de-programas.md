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
* Saída `out`;
* Matriz de parâmetros `params`.

### Sobrecarga

> A _sobrecarga_ de método permite que vários métodos na mesma classe tenham o mesmo nome, contanto que tenham assinaturas exclusivas. [\[1\]](https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/program-building-blocks)

### Virtual

A palavra-chave `virtual` informa para a classe derivada que o método pode ser substituído. Por padrão os métodos não são virtuais, portanto a tentativa de substituir um método não virtual irá ocasionar erro de compilação.

> Não é possível usar o modificador `virtual` com os modificadores `static`, `abstract`, `private` ou `override`. [\[4\]](https://docs.microsoft.com/pt-br/dotnet/csharp/language-reference/keywords/virtual)

Para substituir um método virtual é necessário utilizar a palavra-chave `override` .

```csharp
class Pai {
    public virtual string MeuMetodo {
        //...Código aqui
    }
}

class Filha {
    public override string MeuMetodo {
        //...Código de substituição
    }
}
```

## Construtores

Podem ser de dois tipos: instancia e estático.

### Construtores de instância

> Construtores de instância podem ser sobrecarregados e ter parâmetros opcionais [\[1\]](https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/program-building-blocks)

> são usados para criar e inicializar quaisquer variáveis de membro de instância quando você usa a expressão `new` para criar um objeto de uma classe [\[2\]](https://docs.microsoft.com/pt-br/dotnet/csharp/programming-guide/classes-and-structs/instance-constructors)

> O compilador não gera um construtor padrão quando você define um construtor por conta própria. Isso significa que cada classe derivada deve chamar explicitamente esse construtor. [\[3\]](https://docs.microsoft.com/pt-br/dotnet/csharp/tutorials/intro-to-csharp/object-oriented-programming)

Construtores não são herdados. Dessa forma quando temos a classe Pai com o construtor declarado explicitante, ele deve ser passado para o construtor da classe Filha. Isso é feito utilizando a palavra-chave `base` , como segue no exemplo abaixo.

```csharp
class Pai {
    public Pai(int arg) {
        // ...Codigo aqui
    }
}

class Filha {
    public Filha(int args) : base(args) {
        // ...Codigo aqui
    }
}
```

## Eventos

É um membro que permite a uma classe ou objeto forneça notificações.

## Finalizadores

> é um membro que implementa as ações necessárias para finalizar uma instância de uma classe [\[1\]](https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/program-building-blocks)

Normalmente utilizado para liberar recursos. Um classe só pode ter um finalizador.

Eles não podem:

* Ter parâmetros;
* Ser definidos por _struct_;
* Não podem ser herdados ou sobrecarregados;
* Ter modificadores de acesso e
* Não podem ser invocados explicitamente.

Finalizadores são invocados automaticamente pela coleta de lixo, com isso eles podem ser invocados a qualquer momentos. Dessa forma execução de finalizadores é não determinística. Por esse motivo a implementação de finalizadores deve ser efetuado quando não houver outras soluções viáveis.

> A instrução `using` fornece uma abordagem melhor para a destruição de objetos. [\[1\]](https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/program-building-blocks)

Exemplo de implementação do finalizador.

```csharp
class Pai {
    ~Pai() {
        //...C[odgio aqui
    }
}
```

Finalizadores normalmente são utilizados para liberar recursos não gerenciados como leitura/escrita de arquivos e conexões de redes. Para recursos externo custoso é recomendável liberar explicitamente o recurso antes que o coletor libere o objeto. Isso pode ser feito implementando o método `Dispose` da interface `IDisposable` .

[\[1\]](https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/program-building-blocks)

### Referências bibliográficas

1. [https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/program-building-blocks](https://docs.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/program-building-blocks)
2. [https://docs.microsoft.com/pt-br/dotnet/csharp/programming-guide/classes-and-structs/instance-constructors](https://docs.microsoft.com/pt-br/dotnet/csharp/programming-guide/classes-and-structs/instance-constructors)
3. [https://docs.microsoft.com/pt-br/dotnet/csharp/tutorials/intro-to-csharp/object-oriented-programming](https://docs.microsoft.com/pt-br/dotnet/csharp/tutorials/intro-to-csharp/object-oriented-programming)
4. [https://docs.microsoft.com/pt-br/dotnet/csharp/language-reference/keywords/virtual](https://docs.microsoft.com/pt-br/dotnet/csharp/language-reference/keywords/virtual)

