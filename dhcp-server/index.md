# DHCP and Local DNS Server Configuration with dnsmasq

## Objective

Configure a DHCP server to assign dynamic IPs on the network and a DNS server to resolve local names.

---

## Step 1: View Main Configuration File (`dnsmasq.conf`)

```bash
cat /etc/dnsmasq.conf
```

![Captura 1: dnsmasq.conf](images/01.png)

---

## Step 2: View Local Hosts File (`dnsmasq.hosts`)

```bash
cat /etc/dnsmasq.hosts
```

![Captura 2: dnsmasq.hosts](images/02.png)

---

## Step 3: Restart Service and Check Status

```bash
sudo systemctl restart dnsmasq
systemctl status dnsmasq
```

![Captura 3: Estado del servicio dnsmasq](images/03.png)

---

## Step 4: Verify IP Assignment on Client

```bash
ifconfig # FreeBSD
```

![Captura 4: IP asignada en cliente](images/03b.png)

---

## Step 5: Test Local DNS Resolution

```bash
ping -c 4 servidor1.local
```

![Captura 5: Ping a servidor1.local](images/04.png)

---

## Conclusion

The DHCP server correctly assigns IP addresses within the configured range, and the DNS server resolves the defined local names. The configuration works correctly and is ready for use on the local network.