# Receita para configuração do gsutil dentro do Jenkins com GCP

[gsutil commands](https://cloud.google.com/storage/docs/gsutil/commands/config)  
[gsutil ls](https://cloud.google.com/storage/docs/gsutil/commands/ls)  
[issue git](https://github.com/GoogleCloudPlatform/gsutil/issues/419)  
[cloud storage authentication](https://cloud.google.com/storage/docs/authentication#gsutilauth)  

```
gsutil config -e
```

O arquivo .json com os dados da Service Account pode ser salvo em JENKINS_HOME/gauth.
Garanta que o diretório tenha acesso restrito.

Responder as questões feitas e passar o caminho completo para o arquivo 
.json que contém a autorização de uso da Service Account.
Passar o email da SA, algo como: 9XYZXYZXYX-compute@developer.gserviceaccount.com.
Não deve ter senha.

Preencher com o nome do projeto: <seu_projeto>

Esse comando deve gerar um arquivo chamado .boto que contém a autorização 
para que o gsutil possa acessar o bucket do google.
