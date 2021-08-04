# test-tools
## netcat
Run the command on one of the servers:
$ nc -l 8080

On a remote machine use the following command to connect:
$ nc 127.0.0.1 8080

## shinatra
sudo sh shinatra.sh 80 MY_BASH_WEB_SERVER
```
#!/usr/bin/env bash
RESPONSE="HTTP/1.1 200 OK\r\nConnection: keep-alive\r\n\r\n${2:-"OK"}\r\n"
while { echo -en "$RESPONSE"; } | nc -l "${1:-8080}"; do
  echo "================================================"
done
```
curl --http0.9 shinatra_server_ip

## curl to nothing to prevent downloads to disk
curl http://ip_or_name -o /dev/null

iperf and iperf3
server (which downloads from client?)
```
iperf -s
```
client
```
iperf -c SERVER_IP -f M
```

