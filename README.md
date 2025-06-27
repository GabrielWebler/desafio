# desafio
Montar um cluster kubernetes com aum aplicação API respondendo pelo nome do dominio. 

## Infra
**server-01** - computador com o control plane<br>
**server-02** - computador com o node<br>
**node-vm02** - Node no VM do virtualbox no computador<br>
**node-vm03** - Node no VM do virtualbox no computador<br>
**node-vm04** - Node no VM do virtualbox no computador<br>
**docker-server** - VM do virtualbox no computador para o zabbix server<br>
**desafio.png** - Diagrama da estrutura fisica<br>

## APP
Aplicação entregue pelo time

## Servers-prep
Arquivos de preparação dos servidores<br>

* **control-plane-ubuntu-2404.txt** e **nodes-ubuntu-2404.txt**- Comandos para configurar o Control Plane do Kube
* **docker-server-zbx.txt** - **docker-compose-zabbix.yml** - Comandos para configurar o *docker-server* e docker compose para executar o container
* **curls-linux.txt**  e **curls-powershell.txt** - Diversos curls para executar na aplicação pelo Linux e PowerShell

### kube-manifests
* **allow-metrics-access.yml** -  Habilita a requisição para API do Kube
* **cadvisor-access.yml** - Acesso para o cadvisor nos nodes para monitor uso e performance dos pods
* **deployment.yml** e **service.yml** - Executa o deploy da aplicação
