Clona o projeto para o repositório local:
```
git clone main
```

Abrir o projeto no VSCode.

No terminal do VSCode com o projeto aberto:
```
git checkout -b [nome branch]
```

Criar uma org scratch:
```
sfdx force:org:create -d [dias de validade da org] -a [nome org scratch] -v [nome org devhub] -f config/project-scratch-def.json 
```

Implantar os componentes na org scratch:
```
sfdx force:source:deploy -p force-app/main/default -u [nome autenticado org]
```

Atribuir o conjunto de permissão:
```
sfdx force:user:permset:assign -n [nome permission set]
```

Baixar para o projeto as alterações realizadas na org:
```
sfdx force:source:pull -f
```

Selecionar os arquivos para commit e adicionar no stage.  
Adicionar o comentário do commit + close #numero_issue.  
Enviar push.  
Solicitar pull request. apagar o que foi feito
