
# Laboratório de Rede para Pequena Empresa

Este projeto simula uma pequena rede de escritório criada utilizando o Cisco Packet Tracer.

O principal objetivo foi praticar conceitos básicos de redes, incluindo endereçamento IPv4, máscaras de sub-rede, gateways padrão, conectividade entre switches, configuração de roteador e segmentação de rede.

# Topologia da Rede

A rede é composta por:

* 1 Roteador
* 2 Switches
* 3 Computadores
* 1 Servidor

<img width="1920" height="1032" alt="Image" src="https://github.com/user-attachments/assets/a0af6a07-e666-44b9-8f99-845e8b21778e" /> 

# Endereços de Rede

**Switch 1:** `192.168.10.0/24` — interface do roteador: `192.168.10.1`

**Switch 2:** `192.168.20.0/24` — interface do roteador: `192.168.20.1`

## Endereçamento IP

| Dispositivo | Endereço IPv4 | Máscara de Sub-rede | Gateway Padrão |
| ----------- | ------------- | ------------------- | -------------- |
| Roteador    | 192.168.10.1  | 255.255.255.0       | —              |
| Roteador    | 192.168.20.1  | 255.255.255.0       | —              |
| PC1         | 192.168.10.10 | 255.255.255.0       | 192.168.10.1   |
| PC2         | 192.168.10.11 | 255.255.255.0       | 192.168.10.1   |
| PC3         | 192.168.20.5  | 255.255.255.0       | 192.168.20.1   |
| Servidor    | 192.168.20.2  | 255.255.255.0       | 192.168.20.1   |

# Configuração

A interface do roteador conectada ao Switch 1 foi configurada com:

```text
interface gigabitEthernet 0/0

ip address 192.168.10.1 255.255.255.0

no shutdown
```

A interface do roteador conectada ao Switch 2 foi configurada com:

```text
interface gigabitEthernet 0/1

ip address 192.168.20.1 255.255.255.0

no shutdown
```

Os computadores e o servidor foram configurados utilizando endereços IPv4 estáticos.

# Testes de Conectividade

A conectividade foi testada utilizando o comando `ping`.

### PC1 → PC2

```text
ping 192.168.10.11
```

### PC1 → Servidor

```text
ping 192.168.20.2
```

### PC1 → Roteador

```text
ping 192.168.10.1
```

### PC3 → PC1

```text
ping 192.168.10.10
```

### Servidor → Roteador

```text
ping 192.168.20.1
```

Os testes demonstraram com sucesso a conectividade entre os dispositivos das redes locais.

# O que aprendi

Por meio deste projeto, pratiquei:

* Endereçamento IPv4
* Máscaras de sub-rede
* Gateways padrão
* Configuração de LAN
* Conectividade entre switches
* Comandos básicos do Cisco IOS
* Testes de conectividade
* Comunicação entre diferentes redes

# Melhorias Futuras

As próximas versões deste laboratório poderão incluir:

* DHCP
* DNS
* VLANs
* Controle de acesso
* Configuração de firewall
* Troubleshooting de segurança

# Ferramentas

* Cisco Packet Tracer
* Cisco IOS CLI
* Windows Command Prompt

# Screenshots

## Configuração de IP do PC1

<img width="1000" height="520" alt="Image" src="https://github.com/user-attachments/assets/1109a3cd-159b-4a60-8980-6b763dc7a865" />

## Configuração das Interfaces do Roteador

<img width="1920" height="1032" alt="Image" src="https://github.com/user-attachments/assets/b272a922-5d2c-43dc-bde6-cfb1ce298a59" />

## Teste de Ping entre o Servidor e o Roteador

<img width="1920" height="1032" alt="Image" src="https://github.com/user-attachments/assets/5fc7caa4-3a7a-4622-8bfc-13713714ab03" />
