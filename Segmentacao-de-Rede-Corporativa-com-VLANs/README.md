# Segmentação de Rede Corporativa com VLANs – Cisco Packet Tracer

Este projeto simula a criação de uma rede corporativa composta por três departamentos distintos, utilizando o software Cisco Packet Tracer.

## Objetivo
Implementar a segmentação lógica da rede por meio de VLANs (Virtual Local Area Networks), garantindo o isolamento do tráfego entre os setores, evitando broadcast desnecessário e aumentando a segurança e eficiência da rede.

## Configurações realizadas
- Definição da rede base: 192.168.10.0/24
- Criação de múltiplas VLANs com identificação e nomeação personalizada
- Configuração das interfaces do switch com atribuição das VLANs via comando `switchport access vlan`
- Verificação da configuração através do comando `show vlan brief`

## Problema solucionado
A segmentação da rede por VLANs resolve o problema de tráfego excessivo e a falta de segurança ao separar logicamente os departamentos, permitindo controle granular sobre o fluxo de dados dentro da infraestrutura.

