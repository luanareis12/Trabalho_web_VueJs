# **Criando um conversor de moedas com Vue JS**

Trabalho feito para disciplina de Desenvolvimento Web sobre o framework Vue JS - Implementação de um conversor de moedas

**Integrantes do grupo:** Jairo Pedro, Luana Teixeira e Matheus Souza.

Para este projeto, primeiramente é necessário a instalação do VS Code e do Node js em sua máquina. Para baixar e instalar o VS Code basta acessar o 
[site](https://code.visualstudio.com/download) e selecionar a opção de acordo o Sistema Operacional de sua máquina

![](img/img1.png) 

E para baixar o Node.JS basta acessar o [site](https://nodejs.org/en/) e fazer o download. 

![](img/img2.png)

E seguir para os passos dados na janela de instalação. Por padrão, você não precisa alterar nada: apenas siga clicando em “Next”.

Também será necessário o NPM (ou Yearn). Acesse o [link](https://cli.vuejs.org/) -> get started - > Installation

![](img/img3.png) 

![](img/img4.png) 


Para instalar o novo pacote, use um dos comandos a seguir. Você precisa de privilégios de administrador para executá-los, a menos que o npm tenha sido instalado em seu sistema por meio de um gerenciador de versões do Node.js (por exemplo, n ou nvm).


``` npm install -g @vue/cli ou yarn global add @vue/cli ```

![](img/img6.png)

Você pode verificar a versão correta com este comando:

``` vue --version ```

![](img/img8.png)

Agora daremos início ao projeto, e para isso usaremos o comando (vue create) e nome do projeto. 

Criando o projeto Conversor: Abra o prompt de comando do seu computador e digite o seguinte comando: 

```vue create conversor ```

![](img/img9.png)

Aparecerá esta tela, na qual você irá escolher primeira opção default e pressionar a tecla **"ENTER"**:

![](img/img10.png)

Assim será feita a instalação, logo em seguida execute os seguintes comandos para que sua aplicação seja servida: 

Primeiro digite o comando: 

``` cd conversor ```

e pressione a tecla **"ENTER"**, logo após digite o segundo comando:

``` npm run serve ``` 

e pressione a tecla **"ENTER"** novamente.

![](img/img11.png)

Agora você pode acessar a tela do padrão do projeto em: http://localhost:8080/.

![](img/img12.png)

E aparecerá a seguinte tela padrão:

![](img/img13.png)

Depois você pode encerrar o projeto digitando **“S”** e abri-lo automaticamente no VS Code, para isso é necessário digitar o comando: 

``` code . ```

![](img/img14.png)

Agora iniciaremos a implementação do projeto.

Por padrão, dentre os arquivos e pastas criadas automaticamente na instalação do npm, tem-se o componente **“HelloWord.vue”** que neste caso não será utilizado, por isso você poderá deletá-lo, excluindo também os que estão dentro da pasta **“App.vue”**.


![](img/img15.png)

![](img/img16.png) 

Feito isso, iniciaremos criando um novo componente chamado **“Conversor.vue”** em **src/components**, criando também a seguinte estrutura:

![](img/img17.png) 

Para criar o conversor de moeda, é preciso escrever o seguinte código:

1º Inserindo códigos que farão parte do **template**

![](img/img18.png) 

2º- Inserindo códigos que farão parte do **script**

![](img/img19.png) 


3º- Inserindo códigos que farão parte do **style**

![](img/img20.png) 

Após inserir os códigos do componente **“ConversorM”** é preciso criar os conversores dentro do arquivo **“App.vue”**, ficando assim:

![](img/img21.png) 

E aqui será definido o estilo dos conversores.

![](img/img22.png) 

## Resultados:
Agora você pode acessar o link (http://localhost:8080/) para visualizar e testar o conversor de moedas.

![](img/img23.png) 
![](img/img24.png) 



**Teste: Convertendo de dólar para real e vice-versa.**

Basta digitar o valor que deseja e clicar em **Converter**.
![](img/img25.png) 

**Referência do código:** Programador BR.Criando um conversor de moedas com VUE JS-S02E10.Data de acesso: 2 de abril de 2022. Disponível em: <https://youtu.be/tIEa3MRBpI0>.
