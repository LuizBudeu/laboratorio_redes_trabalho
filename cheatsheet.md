# Comandos e notas úteis

Para que o exemplo faça subscribe, é preciso mudar o `quickstart` para qualquer outra string.

Quando o mote recebe um publish de um tópico no qual está inscrito, a função `pub_handler` é chamada.

Entrar em `contiki-ng/examples/rpl-border-router` e executar:

```bash
make TARGET=zoul connect-router-cooja
```

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
- Mote escreve um JSON em `SmartFarm/[ID do mote]/read` com temperatura, umidade e pH medidos.
- Mote lê em `SmartFarm/[ID do mote]/ideal` valores de referência separados por vírgula.

Para mandar atualizar valores de referência:

```
mosquitto_pub -h test.mosquitto.org -t "SmartFarm/25/ideal" -m "30,20,7"
```
