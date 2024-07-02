## PASSO A PASSO - DOCKER

### 1 - Importar o Ubuntu e Criar Usuário
  - 1: Deixar a imagem dentro de uma pasta no C - Compartilhado da Amber/Ubuntu
  - 2: Importar o arquivo `wsl --import UbuntuCNTLM . <CAMINHO UbuntuCNTLM.tar>`
  - 3: Entrar na imagem - `wsl -d UbuntuCNTLM`
  - 4: Muda o usuário padrão para o seu - `usermod -l <USERNAME> user`
  - 5: Comando para alterar a senha do seu usuário - `passwd <USERNAME>`
### 2 - Configurar o CNTLM
  - 1: `sudo cntlm -d BR -u <usuario_rede_bosch> -H`
  - 2: Copiar a senha **PassNTLMv2** em um bloco de notas
  - 3: `sudo nano /etc/cntlm.conf`
  - 4: Em **username** colocar o usuário da rede Bosch e em **PassNTLMv2** colocar a senha copiada anteriormente
  - 5: Iniciar cntlm - `sudo service cntlm start`
  - 6: Verificar status - `sudo service <service_name> status`
### 3 - Iniciar o Docker
  - 1: Iniciar o docker - `sudo service docker start`
  - 2: Testar - `sudo docker run hello-world`
### 4 - Criar Container com Pontainer
 - 1: Pasta raiz do linux - `cd ~`
 - 2: Criar pasta - `mkdir portainer`
 - 3: Entrar na pasta - `cd portainer`
 - 4: Criar Network - `docker network create agent_network`
 - 5: Abre o editor de texto do linux (nano) e ja cria o arquivo do docker - `nano docker-compose.yml` 
 - 6: Cole os dados no editor
 - 7: `Ctrl + x` para salvar, `Y` para confirmar e `Enter` para sair do editor
 - 8: Cria e inicia os containers - `docker compose up -d`
### 2 - COMANDOS EXTRAS
 - 1: Criar network - `docker network create agent_network`
 - 2: Listar Containers - `docker ps`
 - 3: Excluir network - `docker rm <container_name>`
 - 4: Atualiza o Ubuntu - `sudo apt update`
 - 5: Abre um log sobre o funcionamento do Docker - `sudo dockerd`
