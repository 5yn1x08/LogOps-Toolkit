# winlogbeat configuration

#### For installation :

#### For configure winlogbeat follow this steps:
Run :
```powershell
PS C:\Program Files\Winlogbeat> .\install-service-winlogbeat.ps1
```

##### Search for output.elasticsearch and comment-out the lines as follows:
```yaml
[...]
output.elasticsearch:
  # Array of hosts to connect to.
  hosts: ["YOUR-IP:9200"]
[...]
```

#### or change any other config. according to your need!

##### From the installation directory, run:
```powershell
PS > .\winlogbeat.exe setup -e
```

then press R

##### Test your config file:
```powershell
PS C:\Program Files\Winlogbeat> .\winlogbeat.exe test config -c .\winlogbeat.yml -e
```

##### Start the winloagbeat:
```powershell
PS C:\Program Files\Winlogbeat> Start-Service winlogbeat
```

##### Check the status:
```powershell
PS C:\Program Files\Winlogbeat> services.msc
```

##### After check the data in kibana!!

##### Stop winlogbeat:
```powershell
PS C:\Program Files\Winlogbeat> Stop-Service winlogbeat
```
