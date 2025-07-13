# Cisco Packet Tracer – ACL Lab: LANS 1

Este projeto simula um ambiente de rede com múltiplas sub-redes utilizando o Cisco Packet Tracer, com foco na aplicação de políticas de controle de acesso (ACL) para gerenciamento e segurança do tráfego entre redes.

## 🎯 Objetivos

- Negar acesso ao serviço HTTP da rede `192.168.10.0/24`.
- Permitir acesso HTTP somente à rede `172.20.20.0/24`.
- Permitir tráfego ICMP entre todas as redes envolvidas.

## 🧱 Topologia de Rede

| Nome da Rede | Faixa de IP         |
|--------------|---------------------|
| Rede A       | 192.168.10.0/24     |
| Rede B       | 172.20.20.0/24      |
| Rede C       | 10.10.10.0/24       |

## 🔐 Regras de ACL (Access Control List)

```bash
access-list 110 deny tcp 192.168.10.0 0.0.0.255 host 10.10.10.2 eq 80
access-list 110 permit tcp 172.20.20.0 0.0.0.255 host 10.10.10.2 eq 80
access-list 110 permit icmp 192.168.10.0 0.0.0.255 host 10.10.10.2
access-list 110 permit icmp 172.20.20.0 0.0.0.255 host 10.10.10.2

interface fastethernet0/2
ip access-group 110 out
```

## ✅ Habilidades Aplicadas
Configuração de ACLs padrão e estendidas em roteadores Cisco.

Aplicação de filtros de tráfego com base em protocolos (TCP, ICMP) e portas (HTTP).

Simulação de cenários realistas de segmentação de serviços.

Compreensão de endereçamento IP privado conforme RFC 1918.

## 🧪 Ferramentas
Cisco Packet Tracer

CLI de roteadores e switches Cisco (modo simulado)

## 🔒 Observações
Todos os endereços IP utilizados neste projeto são reservados para uso privado (RFC 1918) e utilizados exclusivamente em ambiente de simulação, sem qualquer relação com redes reais.

