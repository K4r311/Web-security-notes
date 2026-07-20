SSH(Secure Shell) est un protocole réseau permettant a une machine d'avoir un terminal sur une autre machine distante.
```
ssh -p <PORT> <USER>@<TARGET_IP> 
```
SSH permet aussi le port forwarding.
```
ssh -L LOCAL_PORT:DESTINATION_HOST:DESTINATION_PORT
```
