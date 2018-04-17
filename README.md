```
sudo modprobe nf_nat_pptp && sudo sysctl -w net.ipv4.ip_forward=1
```

```
sudo docker run --restart always -d --privileged -e "PPTP_USERNAME=user" -e "PPTP_PASSWORD=password" -p 1723:1723/tcp mentor/pptpd:latest
```

```
sudo ufw allow 1723
```