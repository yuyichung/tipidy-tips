# VMWare

- ESXi: If you can't connect to the server via web service or vSphere client, SSH onto the server and check hostd & vpxa
- ESXi: /etc/init.d/hostd may look for keyword "localhost" in /etc/hosts. If hostd fails to start, check /etc/hosts