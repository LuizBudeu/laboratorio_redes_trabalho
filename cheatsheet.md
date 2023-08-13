# Comandos e notas úteis

Entrar em `contiki-ng/examples/rpl-border-router` e executar:

```bash
make TARGET=zoul connect-router-cooja
```

Mudar o tópico para `rafnak1/mote_writes` na função `construct_pub_topic(void)` e para `rafnak1/mote_reads` na `construct_sub_topic(void)`

```
mosquitto -v -c mosquitto.conf
```

```
mosquitto_sub -h fd00::1 -t "rafnak1/mote_writes"
```

```
mosquitto_sub -h test.mosquitto.org -t "rafnak1/mote_writes"
```

```
mosquitto_pub -h fd00::1 -t "rafnak1/mote_reads" -m "mensagem"
```

```
mosquitto_pub -h test.mosquitto.org -t "rafnak1/mote_reads" -m "mensagem"
```

No caso do projeto: 
- Mote escreve em `SmartFarm/[Id do sensor]/read`
- Mote lê em `SmartFarm/[Id do sensor]/ideal`
- Broker: `broker.emqx.io`
