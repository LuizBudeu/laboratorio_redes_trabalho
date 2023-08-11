# Comandos e notas úteis

```
mosquitto -c mosquitto.conf
```

```
mosquitto_sub -h fd00::1 -t "iot-2/evt/status/fmt/json"
```

```
mosquitto_pub -h fd00::1 -t "iot-2/evt/status/fmt/json" -m "mensagem"
```
