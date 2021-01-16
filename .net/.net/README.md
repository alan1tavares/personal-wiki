# .NET

## Ecossistema

> O .NET é um ecossistema para o desenvolvimento de aplicativos [ref](https://docs.microsoft.com/pt-br/learn/modules/dotnet-introduction/2-what-is-dotnet)

![Resumo dos modelos de aplicativos para .NET](../../.gitbook/assets/image%20%283%29.png)

## Funcionamento do compilador .NET

O compilador converte o código fonte para linguagem chamada IL. O compilador pega o código do IL e salva em um arquivo chamado _assbly .NET_. 

## NuGet

_"é um Gerenciador de pacotes de código-fonte aberto projetado para .net."_ [ref](https://docs.microsoft.com/pt-br/dotnet/core/introduction)

## Compilador JIT \(just-in-time\)

O compilador traduz o IL \(Linguagem Intermediária\) para o código de máquina que o processador entende.

_"Como a compilação JIT ocorre durante a execução do aplicativo, o tempo de compilação é parte do tempo de execução."_ [ref](https://docs.microsoft.com/pt-br/dotnet/core/introduction)

## Compilador AOT \(ahead-of-time\)

O resultado do compilador são binários com códigos nativos. A vantagem é que "_A latência e o tempo de inicialização do aplicativo .NET podem ser aprimorados"_ [ref](https://docs.microsoft.com/pt-br/dotnet/core/deploying/ready-to-run), a desvantagem é que a compilação é restrito para cada plataforma.

Existe dois cenários para a compilação AOT:

1. _"compilação da AOT de 100% \[...\] exemplo é Ios."_ [ref](https://docs.microsoft.com/pt-br/dotnet/core/introduction)
2. _"outros cenários, a maior parte do código de um aplicativo é compilada pela AOT, mas algumas são compiladas por JIT"_ [ref](https://docs.microsoft.com/pt-br/dotnet/core/introduction)_._ Um exemplo é a R2R \(ReadyToRun\)

### R2R

_"Os binários R2R melhoram o desempenho de inicialização reduzindo a quantidade de trabalho que o compilador just-in-time \(JIT\)"_ [ref](https://docs.microsoft.com/pt-br/dotnet/core/whats-new/dotnet-core-3-0#readytorun-images), mas _"os binários R2R são maiores porque contêm código de IL \(linguagem intermediária\), que ainda é necessário para alguns cenários, e a versão nativa do mesmo código."_ [ref](https://docs.microsoft.com/pt-br/dotnet/core/deploying/ready-to-run)

> Em geral, o tamanho de um assembly aumentará entre dois a três vezes maior. Esse aumento no tamanho físico do arquivo pode reduzir o desempenho do carregamento do assembly do disco e aumentar o conjunto de trabalho do processo. No entanto, em retorno, o número de métodos compilados no tempo de execução normalmente é reduzido substancialmente. **O resultado é que a maioria dos aplicativos que têm grandes quantidades de código recebem grandes benefícios de desempenho ao habilitar o ReadyToRun. Os aplicativos, que têm pequenas quantidades de código, provavelmente não terão uma melhoria significativ**a da habilitação de ReadyToRun, já que as bibliotecas de tempo de execução do .NET ainda foram pré-compiladas com o ReadyToRun. [ref](https://docs.microsoft.com/pt-br/dotnet/core/deploying/ready-to-run)

## Gerenciamento automático de memóriza

> O GC \(garbage collector\) gerencia a alocação e a liberação de memória para aplicativos. \[...\] Quando não houver espaço de endereço livre suficiente, o GC verificará se há objetos no heap gerenciado que não estão mais sendo usados pelo aplicativo. Em seguida, ele recupera essa memória. [ref](https://docs.microsoft.com/pt-br/dotnet/core/introduction)

## Recursos não gerenciados

_"são recursos que não são mantidos automaticamente pelo runtime do .NET"_ [ref](https://docs.microsoft.com/pt-br/dotnet/core/introduction)

> objetos que fazem referência a recursos não gerenciados implementam a interface `IDisposable`. Quando você termina de usar o objeto, você chama o método Dispose\(\) do objeto, responsável por liberar quaisquer recursos não gerenciados. [ref](https://docs.microsoft.com/pt-br/dotnet/core/introduction)



