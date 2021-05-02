# API Gateway

O API Gateway funciona como uma porta de entrada para o clients dos microsserviços do sistema. No lugar de chamar os microsserviços diretamente, os clients chamam a API Gateway, que redireciona a solicitação para o microsserviço apropriado. Quando o microsserviço retornar à solicitação, o API Gateway a retorna para o client.

Ou seja, ele funciona como uma camada intermediária entre os clients e os microsserviços. Como todas as solicitações irão passar por ele, o gateway pode modificar as solicitações recebidas e retornadas, o que nos fornece algumas vantagens:

Os microsserviços podem ser modificados sem se preocupar com os clients;
Os microsserviços podem se comunicar utilizando qualquer tipo de protocolo. O importante é o gateway implementar um protocolo que seja compreendido pelos clients;
O gateway pode implementar recursos que não impactam nos microsserviços, como autenticação, logging, SSL, balanceamento de carga, etc.

# Ocelot
Ocelot é uma biblioteca que permite criar um API Gateway com o ASP.NET. Possuindo uma grande gama de funcionalidades, como:

Agregação de solicitações;
Roteamento;
Autenticação;
Cache;
Balanceamento de carga;
Log;
WebSockets;
Service Fabric.
Mesmo que seja voltado para aplicações .NET que estejam implementando uma arquitetura de microsserviços, o Ocelot pode ser utilizado como API Gateway de qualquer tipo de sistema que implemente esta arquitetura.

Para conhecê-lo melhor, vamos ver um exemplo prático.
