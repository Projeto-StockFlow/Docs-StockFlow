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
![Assing_example](./assets/assign%20example.jpg)

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

## 5 O que é Pull Request?
O Pull Request serve como uma etapa de verifiação, onde evidencia a quantidade de conflitos e a possibilidade de dar merge em duas branches. Segue o tutorial de como abrir um Pull Request (PR):
![Pull_Request_example(1)](./assets/PullRequest%20Example(1).png)
Perceba que, ao commitar em uma branch, a mensagem escrito "Compare & Pull Request" aparece aceso em sua tela. Clique nele
<br>
<br>

![Pull_Request_example(2)](./assets/PullRequest_example(2).png)
### A base é a branch que recebe, a compare é a branch que foi alterada.
Dê o nome da issue corrigida ao título e clique em "Create Pull Request"

### Após isso, seu Pull Request foi criado!

## 6 Observação
Foi visto, durante este tópico, alguns nomes entre os seguintes sinais: < >	<br>
NÃO É PARA ADICIONAR ESTES SINAIS NO COMANDO, eles servem somente para exemplificar.
