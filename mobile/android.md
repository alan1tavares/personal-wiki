# Android

**MainActivty**

* Quando o app é executado, o sistema inicia o uma instância dessa `Activity`
* É a atividade principal do app

**app &gt; res &gt; layout &gt; activity\_main.xml**

* Esse arquivo define o layout da atividade principal

**app &gt; manifests &gt; AndroidManifest.xml**

* Descreve características fundamentais do app
* Possui _"informações essenciais sobre o aplicativo para as ferramentas de compilação do Android, para o sistema operacional Android e para o Google Play."_ [ref](https://developer.android.com/guide/topics/manifest/manifest-intro?hl=pt-br)
* Alguma informações que precisam ser declaradas:
  * Nome do pacote do aplicativo
  * Os componentes do aplicativo
  * "permissões que o aplicativo precisa ter para acessar partes protegidas do sistema ou de outros aplicativos."[ ref](https://developer.android.com/guide/topics/manifest/manifest-intro?hl=pt-br)
  * _"Os recursos de hardware e software exigidos pelo aplicativo"_[ ref](https://developer.android.com/guide/topics/manifest/manifest-intro?hl=pt-br)

**Gradle Scripts &gt; build.gradle**

* Existem dois arquivos com esse nome:
  * Um para o projeto
  * Outro para o módulo de app
  * Cada módulo tem o próprio arquivo `build.gradle`



