# Comandos e notas úteis

Entrar em `contiki-ng/examples/rpl-border-router` e executar:

```bash
make TARGET=zoul connect-router-cooja
```

Mudar o tópico para `rafnak1/json` na função `construct_pub_topic(void)`

```
mosquitto -c mosquitto.conf
```

```
mosquitto_sub -h fd00::1 -t "rafnak1/json"
```

```
mosquitto_sub -h test.mosquitto.org -t "rafnak1/json"
```

```
mosquitto_pub -h fd00::1 -t "rafnak1/json" -m "mensagem"
```

```
mosquitto_pub -h test.mosquitto.org -t "rafnak1/json" -m "mensagem"
```