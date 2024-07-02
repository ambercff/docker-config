**OBS: UTILZAR COMO APOIO O TXT "configs_iniciais" CONTIDO NESSE REPOSITÓRIO**

# PASSO A PASSO - DOCKER
- 1: Deixar a imagem dentro de uma pasta no C
- 2: `wsl --import UbuntuCNTLM . .\UbuntuDockerCNTLM.tar`
- 3: `wsl -d UbuntuCNTLM`
- 4: Cria o usuário e loga
- 5: `sudo cntlm -d BR -u <usuario_rede> -H`
- 6: Copiar a senha **PassNTLMv2** em um bloco de notas
- 7: `sudo nano /etc/cntlm.conf`
- 8: em **username** colocar o usuário de rede e em **PassNTLMv2** colocar a senha copiada anteriormente
- 9: startar cntlm
- 10: `sudo apt update`
- 11: iniciar o docker
- 12: para testar - `sudo docker run hello-world`

# PASSO A PASSO - PORTAINER
 - 1: `cd ~`
 - 2: `mkdir portainer`
 - 3: `docker network create agent_network`
 - 4: `nano docker-compose.yml`
 - 5: colocar dentro o arquivo de mesmo nome contido nesse repositório
 - 6: `docker compose up -d`
