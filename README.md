# Objetivo

Atualmente na rede existe um arquivo `.csv` que contém estruturas de dados que são mostradas para o usuário.
Basicamente, o arquivo possui, obviamente, linhas e colunas. O objetivo é ler o índice da coluna e retonar os valores das colunas.


# Configuração

Para os testes foram utilizados:
1. Node-Red - versão 1.0.1
2. CPU M580 - Schneider

## Configuração PLC

Em aplicação convencional o valor de referência(índice da coluna) seria escrito via interface com o usuário - SCADA. No nosso caso o criamos um contador simples com reset para poder simular o envio dos dados via Modbus TCP.

A CPU M580 utilizada já vem embarcada com o protoco modbus TCP o que facilita a integração.


#### Configuração do Rack
<img src="https://github.com/dedynobre/dados-modbus-csv/blob/master/imagens/config-rack.png"/></br>

#### Lógica
<img src="https://github.com/dedynobre/dados-modbus-csv/blob/master/imagens/logica.png"/></br>

> O pino CV do contador `CTU_1` é o pino onde o Node-Red lê o índice para ser procurado no arquivo `.csv`.
> Esta variável no programa tem o endereço de %MW102, parametro este que é configurado nos nodes Modbus.
> <img src="https://github.com/dedynobre/dados-modbus-csv/blob/master/imagens/var.png"/></br







