## Aula BGP

Router 1

```bash
# configuring bgp
$ router bgp 10
$ neighbor 172.16.0.20 remote-as 20
$ network 10.10.0.0 mask 255.255.255.0

# debug bgp
$ show ip bgp
$ show ip bgp summary
```

Router 2

```bash
# configuring
$ router bgp 20
$ neighbor 172.16.0.20 remote-as 10
$ neighbor 172.16.1.30 remote-as 20
$ network 10.20.0.0 mask 255.255.255.0
$ end

# debug bgp
$ show ip bgp
$ show ip bgp summary
$ exit
```

Router 3

```bash
$ router bgp 30
$ neighbor 172.16.0.20 remote-as 20
$ network 10.30.0.0 mask 255.255.255.0
$ network 10.30.1.0 mask 255.255.255.0
$ end
```

Host 1

```bash
$ ping <ips>
```
