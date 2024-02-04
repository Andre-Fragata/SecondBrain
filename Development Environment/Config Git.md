---
tags:
  - DevelopmentEnvironment
---
git branch (nome)  - Criar uma nova Branch

git checkout (nome) - Trocar para a branch selecionada

git deflog - Ver o histórico de atualizações
![[image.png]]

git merge (nome da branch que deseja puxar as informações)

Serve para fazer a configuração do usuário no GIT

```
git config --global user.name "Your Name"
git config --global user.email "yourname@example.com"
```

O GitHub alterou recentemente a ramificação padrão em novos repositórios  ``` master``` para ```main``` . Altere a ramificação padrão do Git usando este comando:
```
git config --global init.defaultBranch main
```

Para ativar a saída colorida com git
```
git config --global color.ui auto
```

gerar chaves ssh para o github
```
ssh-keygen -t ed25519 -C "your@email.com"
```
