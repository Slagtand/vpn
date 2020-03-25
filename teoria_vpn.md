# Teoria VPN

## Què és VPN?

VPN són les sigles de **Virtual Private Network**, és a dir, és una xarxa privada virtual.

El que fa una VPN és crear un túnel en el qual el tràfic va **xifrat** de punta a punta de les interfícies túnel, però segueix viatjant per internet.

## Instal·lació

Instal·larem **openvpn**

```bash
dnf -y install openvpn
```

## Ordre

```bash
openvpn −−remote june.kg −−dev tun1 −−ifconfig 10.4.0.1 10.4.0.2 −−verb 9
```

* `--remote`: especifiquem el host remot

* `--dev`: especifiquem la interfície de túnel per on anirà

* `--ifconfig`: especifiquem les ips local/destí

* `--verb`: és un verbose, ens vomita informació. Si el treiem s'executarà el programa però sense dir res
