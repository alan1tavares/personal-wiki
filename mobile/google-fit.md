---
description: Anotações sobre a integração do Google Fit com aplicações mobile
---

# Google Fit

Exites duas formas de realizar integração pelo o Google Fit, são elas:

* API do Android;
* REST API.

## API do Android

No [Get Started](https://developers.google.com/fit/android/get-started) da documentação do Google Fit tem um cunjunto de passos de como relizar a configuração para a integração. A partir disso separei alguns passos a serem explorados.

### Obter o client ID do OAuth 2.0

> Todos os aplicativos Android são assinados com um certificado digital - [ref](https://developers.google.com/fit/android/get-api-key)

Existem dois tipos de certificados o _release_ e o _debug_.

> Obter um ID para seu aplicativo requer várias etapas. Essas etapas são descritas abaixo.
>
> 1. Encontre as informações do certificado do seu aplicativo.
> 2. Crie ou modifique um projeto no Console de API do Google.
> 3. Solicite um ID de cliente OAuth 2.0. 
>
> - [ref](https://developers.google.com/fit/android/get-api-key)

#### Obter informações do certificad

Para listar o certificado _debug_ no _React Native_, na raiz do projeto vá na pasta `android/app` que é onde etá localizado o arquivo `debug.keystore`. Dentro da pasta execute o seguinte comando:

```text
keytool -list -v -keystore ./debug.keystore -alias androiddebugkey -storepass android -keypass android
```

Irá mostrar algo como:

```text
Alias name: androiddebugkey
Creation date: Jan 01, 2013
Entry type: PrivateKeyEntry
Certificate chain length: 1
Certificate[1]:
Owner: CN=Android Debug, O=Android, C=US
Issuer: CN=Android Debug, O=Android, C=US
Serial number: 4aa9b300
Valid from: Mon Jan 01 08:04:04 UTC 2013 until: Mon Jan 01 18:04:04 PST 2033
Certificate fingerprints:
     MD5:  AE:9F:95:D0:A6:86:89:BC:A8:70:BA:34:FF:6A:AC:F9
     SHA1: BB:0D:AC:74:D3:21:E1:43:07:71:9B:62:90:AF:A1:66:6E:44:5D:75
     Signature algorithm name: SHA1withRSA
     Version: 3
```

#### Criar criar um projeto no Console API do Google

Em Get an OAuth 2.0 Client ID possui um conjunto de passo em como fazer isso, mas vale fazer alguma observações

1. Para saber o nome do pacote que foi criado, ir na pasta `android\app\src` e localizar o arquivo `_BUCK`. Nesse arquivo tem um _json_ com a propriedade _package_. O que estiver atribuído nessa propriedade é o nome do pacote.
2. Durante o processo da obtenção do client ID irá pedir para confiurar a tela consentimento. É necessário realizar a configuração para poder finalizar o processo de obtenção  do client ID.

## Referencia bibliográfica

Getting Started on Android, Acessado em: [https://developers.google.com/fit/android/get-started](https://developers.google.com/fit/android/get-started) - 05/12/2020

Get an OAuth 2.0 Client ID, Aessado em: [https://developers.google.com/fit/android/get-api-key](https://developers.google.com/fit/android/get-api-key) - 05/12/2020



