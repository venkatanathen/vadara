All dates have to be in second epoch (date in seconds since 1970 - UNIX STYLE)

Start influx db
influxdb -config=/usr/local/etc/influxdb.conf

Access influx db
http://localhost:8083/

Start rabbitmq
rabbitmq-server



EXTENSION MODEL

monitor

scaler

Core
- has an argument -- queu anem
- must answer to instances
- must read queues to monitor


DICIONARIO MONITOR
:metric_name ==> [cpu_usage(%)|request_count]
:statistics ==> [[min|max|avg],[]]
:start_time ==> time in ???
:end_time ==> time in ???
:period ==> time
:detail ==> detailed|condensed






---- TODO ----

API PARA DAR ORDENS AO DECIDER PARA FAZER ACCOES
NIVEIS DE INSTANCIAS PARA VERTICAL SCALING DOWN_UP
TESTAR COM WEB-TRACES GOOGLE
CONCORRER AWS ACADEMIC GRANTS
PODER ENVIAR DICIONARIO ESPECIFICO DE CADA CLOUD PROVIDER PARA MONITOR E SCALER?
PEDIDOS DO DECIDER NO MONITOR E NO SCALER SAO POR CP? OU CP SÒ NO SCALER? LIVRE ESCOLHA?
ADICIONAR FULL_PERIOD A CONFIGURACAO
PASSAR O INIT PARA DENTRO DE CADA MONITOR/SCALER??
REVER LOAD BALANCER MONITOR EM TODOS ... FAZER IMAGEM COM SITE PARA TESTAR ETC
SCALER EM PRINCIPIO VAI TER DE GERIR OS IDS A TERMINAR
YOU NEED TO DEREGISTER FORM LB
CHOOSE INSTANCES TO DELETE THAT ARE FAILING HEALTH CHECKS

SCALER
-TEMPO DE BOOT DEVERA SER MEDIA? MODA? MEDIANA?
-CORE PASSA PARA CADA CP O BOOTUP TIME INICIAL

MONITOR
-DEFINIR REPLY QUEUE E PASSAR APENAS O FANOUT?
-APLICAR DICIONARIO AWS
-LIDAR COM ERROS DO LADO DO MONITOR
-PEDIR MAIS QUE UMA METRICA AO MESMO TEMPO?






