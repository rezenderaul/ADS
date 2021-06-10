# Exercício
Os servidores de aplicação geralmente são implantados utilizando o Sistema Operacional Linux, isso se da pelo fato de o Linux poder ser executado apenas via console textual, o que permite uma performance e controle maior sobre os processos que ali estão sendo executados.
 
Uma empresa de desenvolvimento de software utiliza a linguagem de programação Java como linguagem de base para o desenvolvimento das suas plataformas. Se faz necessário que você copie uma pasta e todo o seu conteúdo, que está disponível no seguinte caminho: ```/home/appsoftware/tomcat/webapps/app-client```, para o novo caminho: ```/home/appsoftware/backup-tomcat/```, a pasta em questão que deve ser copiada é a ```app-client```, mas antes deve-se criar a pasta ```backup-tomcat``` no seguinte caminho ```/home/appsoftware/```.
 
Além desta necessidade, a empresa solicitou que seja movido (copiado e apagado) o arquivo ```platform.war``` que está disponível no seguinte caminho: ```/home/appsoftware/tomcat/webapps/platform.war``` para o seguinte novo caminho: ```/home/appsoftware/backup-tomcat/```.
 
1. Apresente a sequência de comandos que você utilizou para executar essas tarefas como se estivesse utilizando o terminal do servidor Linux.
2. Para cada linha de comando apresentada deve-se apresentar um comentário utilizando **##** antes para informar o que está sendo feito, por exemplo:
 
```bash
cd /home/appsoftware/tomcat/webapps
```
\## entrando na pasta webapps a partir do caminho apresentado no comando.

* **COMO ENTREGAR A ATIVIDADE:**
1. Utilize um editor de textos e apresente o que foi solicitado.
2. Envie em **.DOC ou PDF**.

## Dados extraídos:
1. **Origem** ```/home/appsoftware/tomcat/webapps/app-client```
2. **Destino** ```/home/appsoftware/backup-tomcat/```
3. **Criar pasta** ```backup-tomcat``` no path ```/home/appsoftware/```
4. **Copiar pasta** a pasta **app-client** para o path ```/home/appsoftware/backup-tomcat/```
5. **Mover** (copiar e apagar) o arquivo ```platform.war``` do path ```/home/appsoftware/tomcat/webapps/platform.war``` para o path ```/home/appsoftware/backup-tomcat/```

# Comandos:
\## Voltar a pasta ```/home```:
```bash
cd ~ && cd ..
```
\## Ir até a pasta ```/home/appsoftware```:
```bash
cd appsoftware/
```
\## Criar a pasta ```backup-tomcat```:
```bash
sudo mkdir backup-tomcat
```
\## Copiar a pasta ```app-client``` para a pasta ```backup-tomcat```:
```bash
sudo cp -r /home/appsoftware/tomcat/webapps/app-client /home/appsoftware/backup-tomcat/
```
\## Mover o arquivo ```platform.war``` para o path ```/home/appsoftware/backup-tomcat/```:
```bash
sudo mv /home/appsoftware/tomcat/webapps/platform.war /home/appsoftware/backup-tomcat/
```
