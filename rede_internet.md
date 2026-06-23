Etapa 1: Configuração de Rede e Internet
1. Escopo e Configuração dos Adaptadores
A máquina virtual do servidor foi configurada com duas placas de rede distintas:

Placa 1 (Rede Interna): Comunicação com os hosts da rede local, configurada com o IP estático 192.168.10.10.

Placa 2 (Modo NAT/Bridge): Prover acesso temporário à internet para instalação de pacotes.

2. Arquivo de Configuração do Netplan (/etc/netplan/00-installer-config.yaml)
YAML
network:
  ethernets:
    enp0s3:
      dhcp4: no
      addresses:
        - 192.168.10.10/24
  version: 2
3. Comandos de Validação
Aplicar alterações: sudo netplan apply


