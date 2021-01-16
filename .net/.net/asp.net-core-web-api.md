# ASP.NET Core web API

## Criando o projeto

```bash
dotnet new webapi -o <diretorio-doprojeto>
```

## Estrutura do projeto

| Nome | Descrição |
| :--- | :--- |
| _Controllers/_ | Contêm as classes que expõem os métodos públicos com _endpoints_ HTTP. |
| _Program.cs_ | Contém o método _main_. O ponto de entrada para o gerenciamento do app. |
| _Startup.cs_ | Configura serviços e o pipeline de solicitação HTTP do aplicativo. |
| _file.csproj_ | Contêm os metadatos do projeto. |

## Classes Modelos \(Models\)

São utilizadas para passar dados entre uma web API e para persistir esses dados em um banco de dados.

