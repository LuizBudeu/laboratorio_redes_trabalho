# Comandos e notas úteis

Entrar em `contiki-ng/examples/rpl-border-router` e executar:

```bash
make TARGET=zoul connect-router-cooja
```

Mudar o tópico para `rafnak1/mote_writes` na função `construct_pub_topic(void)` e na `construct_sub_topic(void)`

```
mosquitto -c mosquitto.conf
```

```
mosquitto_sub -h fd00::1 -t "rafnak1/mote_writes"
```

```
mosquitto_sub -h test.mosquitto.org -t "rafnak1/mote_writes"
```

```
mosquitto_pub -h fd00::1 -t "rafnak1/mote_writes" -m "mensagem"
```

```
mosquitto_pub -h test.mosquitto.org -t "rafnak1/mote_writes" -m "mensagem"
```