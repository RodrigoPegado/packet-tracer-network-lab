# Enterprise Network Lab — Cisco Packet Tracer

## 📌 Sobre o projeto

Laboratório de infraestrutura de redes empresariais desenvolvido no Cisco Packet Tracer, com foco em segmentação de redes, roteamento, serviços de rede e fundamentos de segurança.

O projeto simula uma pequena empresa com departamentos Administrativo e Suporte TI, além de uma rede dedicada a servidores.

## 🖥️ Tecnologias utilizadas

- Cisco Packet Tracer
- Cisco IOS
- VLANs e IEEE 802.1Q
- Inter-VLAN Routing (Router-on-a-Stick)
- DHCP e DHCP Relay
- DNS
- HTTP
- ACLs (em fase de validação)

## 🌐 Topologia

A infraestrutura possui:

- 1 roteador Cisco 2911
- 1 switch Cisco 2960
- 4 computadores
- 1 servidor

## 📡 Endereçamento IP

| VLAN | Departamento | Rede | Gateway |
|---|---|---|---|
| 10 | Administrativo | 192.168.10.0/24 | 192.168.10.1 |
| 20 | Suporte TI | 192.168.20.0/24 | 192.168.20.1 |
| 30 | Servidores | 192.168.30.0/24 | 192.168.30.1 |

**Servidor SRV1:** 192.168.30.10

## ⚙️ Serviços implementados

### DHCP
Distribuição automática de endereços IP para os computadores, utilizando DHCP Relay no roteador.

### DNS
Resolução de nomes internos, incluindo `servidor.empresa.test`.

### HTTP
Hospedagem de uma página web interna, acessível pelos departamentos Administrativo e Suporte TI.

### Segurança
Criação de uma ACL estendida para restringir tráfego ICMP entre o Administrativo e o servidor.

**Status:** política ainda não validada. Durante os testes, foi identificada uma inconsistência no endereçamento do ADM-PC1.

## 🧪 Testes realizados

- Comunicação entre VLANs
- Distribuição de endereços via DHCP
- Resolução de nomes com `nslookup`
- Testes de conectividade com `ping`
- Acesso ao servidor HTTP pelo navegador

## 🔍 Troubleshooting

Durante o laboratório, foram identificados problemas de conectividade e configuração.

Um dos problemas ocorreu na validação da ACL: o computador identificado como ADM-PC1 apresentou endereço `192.168.20.100`, pertencente à rede de Suporte TI.

A causa ainda precisa ser investigada antes da validação definitiva da política de segurança.

## 🎯 Objetivo

Desenvolver conhecimentos práticos de redes de computadores, infraestrutura empresarial, diagnóstico de problemas e segurança da informação.