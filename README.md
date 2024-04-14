# Commands to config networks

## Router Cisco
### Basic commands
```bash
  # habilita o modo root
  $ enable

  # Entra no modo de configuração 
  $ configure terminal

  # especifica a interface que vai receber o endereço ip do proximo commando (EX: interface g0/0)
  $ interface <interface>

  # adciona um ip com uma determinada mascara (Ex: ip address 192.168.122.1 255.255.255.0)
  $ ip address <ip> <mascara>

  # reinicia a interface de rede
  $ no shutdown

  # mostra configurações de interface
  $ do show ip interface brief

  # mostra configuração de rotas
  $ do show ip route

  # configura rota padrao
  $ route 0.0.0.0 0.0.0.0 <ip_rede> <mask>

  # propaga pela rede o roteador padrão(verficar escrita)
  $ difinitin-information originate
```

### RIP config
```bash
  # abre arquivo de configuração com o editor nano
  # dever alterar a variavel ripd=no para ripd=yes
  $ nano /etc/frr/daemons

  # inicia servidor frr
  $ /etc/init.d/frr start

  # acessa o servidor frr
  $ vtyh

  # entra no modo de configuração
  $ conf t

  # inicia configuração do RIP
  $ router rip

  # alterar versão do RIP para 2
  $ version 2

  # informa uma rede conhecida (EX: network 192.168.122.0/24)
  $ network <ip_rede>/<mask>

  # finaliza configuração
  $ end
```

## Router linux
### Basic commands
```bash
  # configura um ip para a interface especificada (EX: ifconfig eth0 192.168.122.1 255.255.255.0)
  $ ifconfig <interface> <ip> <mascara>

  # mostra rotas configuradas
  $ ip route -n

  # configura rota padrao (EX: route add default gw 192.168.122.1 255.255.255.0)
  $ route add default gw <ip> <mascara>
```
