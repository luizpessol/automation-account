## Salvar as informações da conta de automação do Azure em uma variável

```
$azConn = Get-AutomationConnection -Name 'AzureRunAsConnection'

```

## Adicione o contexto da conta de automação à sessão

```
Add-AzureRMAccount -ServicePrincipal -Tenant $azConn.TenantID -ApplicationId $azConn.ApplicationId -CertificateThumbprint $azConn.CertificateThumbprint

```

## Salvar as VMs do Azure com tags com o valor '07pm' em uma variável

```
$azVMs = Get-AzureRMVM | Where-Object {$_.Tags.Start -eq '7am'}

```

## Start/ligar as VMs com valor "07am"

```
$azVMS | Start-AzureRMVM

```
