# Sharing SMB with Kubernetes

## Notice

- My SMB server is an OLD Apple Timecapsule. That's why it doesn't work. Configuration is good for more modern SMB versions.

## Establishing `smbcreds` Secret

```bash
kubectl create secret generic smbcreds --from-literal username=hittjw --from-literal password="xxx" --from-literal mountOptions="dir_mode=0777,file_mode=0777,uid=1001,gid=1001,vers=1.0,noserverino"
```

> Copyright &copy; 2023-2025 [JWH Consolidated LLC](https://www.jwhco.com/), All rights reserved.
