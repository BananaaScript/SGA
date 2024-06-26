## :open_file_folder: Como rodar o projeto
### Facilite seu caminho
* [Baixando os arquivos](#BaixandoArquivos)
* [Rodando o *Front-end*](#RodandoFront)
* [Rodando o *Back-end*](#RodandoBack)
* [Vídeo](#video)
* [Links](#links)

<a name="BaixandoArquivos"/><br/>
## Baixando os arquivos
- Copie este *link* ```https://github.com/BananaaScript/SGA.git``` do [repositório](https://github.com/BananaaScript/SGA) do projeto
- Crie uma pasta na área de trabalho
- Com a pasta aberta, selecione a barra de endereços da pasta, digite *cmd* e pressione *enter*
- Digite o seguinte comando no *cmd*
```
git clone https://github.com/BananaaScript/SGA.git .
```
- Digite os seguintes comandos:
```
git submodule init
```
```
git submodule update
```
<a name="RodandoFront" /> <br/>
## Rodando o *Front-end*
AVISO: Nesta parte você **necessita** do [*Node.js*](https://nodejs.org/en/download/current) instalado e se desejar uma *IDE* para visualizar o código, no nosso caso utilizamos o [*Visual Studio Code*](https://code.visualstudio.com).
- Acesse a pasta do *Front-end*: ```<PastaClonada>\SGA-front\sga ```
- Acesse o *cmd* na pasta: ```<PastaClonada>\SGA-front\sga ```
- Já no *cmd* digite os seguintes comandos:
```
npm install
```
- Após finalizar a instalação digite:
```
npm start
```
Se tudo foi feito corretamente o *cmd* vai exibir uma mensagem em verde *No issues found* e a aplicação será aberta no seu navegador.

 <a name="RodandoBack"/><br/>
## Rodando o *Back-end*
### Banco de dados
Primeiro vamos configurar o banco de dados, neste projeto utilizamos o [*MySQL*](https://dev.mysql.com/downloads/installer/).<br/>
O instalador fornece instalações adicionais, portanto é importante se atentar na instalação do sistema gerenciador de banco de dados *MySQL Workbench* e se necessário alguma outra instalação para conexões.<br/> 
Após instalar o *MySQL* e o *MySQL Workbench*, prossiga os seguintes passos:
- Abra a barra de pesquisa do *Windows* e digite "Serviços", procure o serviço do *MySQL* e inicie ![image](https://github.com/BananaaScript/SGA/blob/main/Doc/Imgs/Sprint1/servicoMysql.png)
- Abra o *MySQL Workbench*, e crie uma conexão caso não tenha uma **(lembre da senha já que vamos precisar!)**![image](https://github.com/BananaaScript/SGA/blob/main/Doc/Imgs/Sprint1/mysqlConexoes.png)

- Abra o arquivo do banco de dados que está localizado na pasta: ```<PastaClonada>\SGA-back``` 
- Aplique o arquivo clicando no "*raiozinho*" na parte superior <br/> ![image](https://github.com/BananaaScript/SGA/blob/main/Doc/Imgs/Sprint1/MySQLrodar.png)
### Microsserviço
Agora que nosso banco de dados está criado, vamos rodar nossa aplicação de microsserviços<br/>
AVISO: É importante que você não feche a conexão ou o serviço do *MySQL*
- Abra a pasta: ```<PastaClonada>\SGA-back```
- A pasta chamada "*SGA*" é a nossa aplicação, para rodar precisamos ter a versão 17 ou superior do [*Java*](https://www.oracle.com/br/java/technologies/downloads/)
- Depois de instalar o *Java* vamos precisar de uma *IDE*, neste exemplo vamos utilizar o [*Eclipse*](https://eclipseide.org)
- Abra o *Eclipse* e monte o projeto localizado em: ```<PastaClonada>\SGA-back\SGA``` <br/> ![image](https://github.com/BananaaScript/SGA/blob/main/Doc/Imgs/Sprint1/abrirProjetoEclipse.png)
- Aguarde a *IDE* montar o projeto
- Abra os arquivos destacados: <br/>![image](https://github.com/BananaaScript/SGA/blob/main/Doc/Imgs/Sprint1/destaqueArquivos.png)
- Vamos editar arquivo "*application.properties*"
- Coloque seu *username* e *password* que configurou na conexão do banco de dados
```
spring.application.name=SGA
spring.datasource.url=jdbc:mysql://localhost:3306/SGAbd
spring.datasource.username=UsernameDaSuaConexão
spring.datasource.password=SenhaDaSuaConexão
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
```
- Após configurar o arquivo de conexão abra o arquivo "*SgaApplication.java*" e rode a aplicação <br/> ![image](https://github.com/BananaaScript/SGA/blob/main/Doc/Imgs/Sprint1/arquivosJava.png) <br/>
Se tudo foi feito corretamente o *spring* vai iniciar a aplicação, você pode verificar se a aplicação está funcionando colocando a seguinte rota no seu navegador: "http://localhost:8080" que vai ser mostrado uma mensagem

## Conclusão
Agora que tudo está rodando, nossa aplicação pode funcionar corretamente, a rota padrão para a página *web* é "*localhost:3000*", é importante que não pule as etapas e mantenha tudo que fez aberto, para a aplicação funcionar devidamente ela precisa tanto do "*front-end* quanto do *back-end*.
<a name="video"/><br/>
### Vídeo
Para facilitar foi feito um vídeo de como rodar o projeto, você pode conferir no youtube: ([assistir](https://youtu.be/JU2ztloM7h0))<br/>
<a name="links"/><br/>
### Links
Os *links* gerais das tecnologias e *IDE* que utilizamos podem ser conferidos aqui: <br/>
<br/>[![](https://img.shields.io/badge/Node%20js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)](https://nodejs.org/en)
<br/>[![](https://camo.githubusercontent.com/b0648ef7a9b6980ea27c1caaeb06d5c8503dbb4f9b4d9d7ca1df60a5edc14340/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f6a6176612d2532334544384230302e7376673f7374796c653d666f722d7468652d6261646765266c6f676f3d6f70656e6a646b266c6f676f436f6c6f723d7768697465)](https://www.oracle.com/br/java/technologies/downloads/)
<br/>[![](https://img.shields.io/badge/Spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white)](https://spring.io)
<br/>[![](https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white)](https://www.mysql.com/downloads/)
<br/>[![](https://img.shields.io/badge/VSCode-0078D4?style=for-the-badge&logo=visual%20studio%20code&logoColor=white)](https://code.visualstudio.com)
<br/>[![](https://img.shields.io/badge/Eclipse-2C2255?style=for-the-badge&logo=eclipse&logoColor=white)](https://eclipseide.org) 
