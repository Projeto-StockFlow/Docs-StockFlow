# Guia de práticas de Git/GitHub para o projeto StockFlow

### Para uma produção eficiente e harmoniosa, usaremos o método de git flow:

## 1. O que é git flow?
É um método de desenvolvimento em equipe, para que tudo ocorra de forma harmoniosa, sem conflito entre códigos ou tarefas repetidas, além de ser uma forma segura de se desenvolver. É dividida em três tipos de branch: main, develop e feature.



## 2. O que é develop?
A branch develop é a branch que vai receber todas as alterações feitas nas branchs de feature. Ela existe para que, caso haja equívocos, estes nunca chegarem à main, a branch principal e que funcionará para o deploy da aplicação. Portanto, NUNCA COMMITE DIRETO NA MAIN

## 3 O que é feature?
São as branches que serão criadas para o desenvolvimento e resolução das tasks e issues cadastradas, aplicando funcionalidades novas. Nelas você faz as alterações, e dá o commit. Depois, dá o Pull Request. Portanto, NUNCA ALTERE A DEVELOP DIRETAMENTE

## 4. Boas práticas
### 4.1. Faça somente as issues que você tem assign
Isso evita que você repita ou usurpe o trabalho de alguém. Caso a issue não tenha ninguém como responsável, designe a si mesmo antes de começar a desenvolver.

### 4.2. Como trocar de branch
No terminal, execute o seguinte comando:
```
git status
```
Na saída, em algum lugar, estará escrito a branch que você está:
```
on branch <nome_branch>
```
Para trocar para uma branch já existente, execute:
```
git switch <nome_branch>
```


### 4.3. Como criar branches
Execute o seguinte comando para criar uma branch a partir da develop:
```
git switch -c <nome_branch>
```
Após criar a branch, você precisa atualizá-la no GitHub:
```
git push -u origin <nome__branch> 
```

## 8.5 Observação
Foi visto, durante este tópico, alguns nomes entre os seguintes sinais: < >	<br>
NÃO É PARA ADICIONAR ESTES SINAIS NO COMANDO, eles servem somente para exemplificar.
