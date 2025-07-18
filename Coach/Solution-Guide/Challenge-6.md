# Desafio 6: Gerar Scripts usando GitHub Copilot - Guia da Solução

## Task 1: Gerar Scripts de Sysadmin

Nesta tarefa, você utilizará o GitHub Copilot para gerar scripts de monitorização de recursos de sysadmin para uso de CPU e memória para uma VM Linux e uso de disco para uma VM Windows

1. No VS Code, peça ao GitHub Copilot Chat para gerar um script de sysadmin que monitore o uso de CPU e memória com um limite para uma VM Linux e copie o script para um novo arquivo.

   ![](../../media/generate-bash-script.png)

1. O GitHub Copilot irá gerar um script bash que monitoriza o uso de CPU e memória para um certo limite e também explica seu uso.

1. Agora, peça ao GitHub Copilot Chat para gerar um script de administração de sistema que monitore o uso de disco com um limite para uma VM Windows e copie o script para um novo arquivo.

   ![](../../media/generate-ps-script.png)

1. O GitHub Copilot gera um script PowerShell que monitoriza o uso de disco para um certo limite e também explica seu uso.

## Task 2: Refatorar e debug dos scripts gerados

Nesta tarefa, você irá refatorar e fazer debug dos scripts de administração de sistema gerados pelo GitHub Copilot na tarefa anterior.

1. Selecione o script inteiro e clique em **Ctrl+Enter** para ver as sugestões fornecidas pelo GitHub Copilot para refatorar e/ou fazer debug do script.

1. Aceite as sugestões mais adequadas para corrigir os scripts selecionado a tecla **Accept**..

1. Você também pode utilizar o Chat Inline do GitHub Copilot. Oriente o GitHub Copilot para melhorar e corrigir os scripts.

1. Salve os arquivos depois de ter utilizado com sucesso o GitHub Copilot para refatorar e corrigir os scripts.

   - Bash script to monitor CPU and memory usage in a Linux VM.
     ```
     #!/bin/bash

     # Sysadmin Resource Monitoring Script

     # Set the thresholds for CPU and memory usage (in percentage)
     cpu_threshold=90
     memory_threshold=90

     # Get the current CPU usage
     cpu_usage=$(top -bn1 | grep "Cpu(s)" | awk '{print $2}' | cut -d'%' -f1)

     # Get the current memory usage
     memory_usage=$(free | grep Mem | awk '{print $3/$2 * 100.0}' | cut -d'.' -f1)

     # Check CPU usage
     if [ "$cpu_usage" -gt "$cpu_threshold" ]; then
         # CPU usage exceeds the threshold, send an alert
         echo "CPU usage is above the threshold: ${cpu_usage}%"
         # Add your alerting mechanism here (e.g., send an email, log to a file, etc.)
     else
         # CPU usage is within the acceptable range
         echo "CPU usage is within the acceptable range: ${cpu_usage}%"
     fi

     # Check memory usage
     if [ "$memory_usage" -gt "$memory_threshold" ]; then
         # Memory usage exceeds the threshold, send an alert
         echo "Memory usage is above the threshold: ${memory_usage}%"
         # Add your alerting mechanism here (e.g., send an email, log to a file, etc.)
     else
         # Memory usage is within the acceptable range
         echo "Memory usage is within the acceptable range: ${memory_usage}%"
     fi
     ```
     
   - PowerShell script to monitor disk usage in a Windows VM
     ```
     # Sysadmin Disk Space Monitoring Script

     # Set the threshold for disk space usage (in percentage)
     $threshold = 90

     # Get the current disk space usage for the C: drive
     $diskUsage = Get-WmiObject Win32_LogicalDisk -Filter "DeviceID='C:'" | Select-Object @{Name='FreeSpace';Expression={$_.FreeSpace}}, @{Name='Size';Expression={$_.Size}}

     # Calculate the percentage of free space
     $freeSpacePercentage = ($diskUsage.FreeSpace / $diskUsage.Size) * 100

     # Check if disk space usage exceeds the threshold
     if ($freeSpacePercentage -gt $threshold) {
         # Disk space usage exceeds the threshold, send an alert
         Write-Host "Disk space usage is above the threshold: $($freeSpacePercentage)%"
         # Add your alerting mechanism here (e.g., send an email, log to a file, etc.)
     } else {
         # Disk space usage is within the acceptable range
         Write-Host "Disk space usage is within the acceptable range: $($freeSpacePercentage)%"
     }
     ```

## Task 3: Executar os scripts

Nesta tarefa, você executará os scripts de administração de sistema gerados pelo GitHub Copilot em VMs Linux e Windows

1. Abra o command prompt e faça login na sua VM Linux.

   > **Observação:** Insira o nome de usuário admin, a senha e o endereço IP público da sua VM Linux. 

1. Execute cada comando do seu script bash, que monitora o uso de CPU e memória, e verifique os resultados.

   ![](../../media/execute-bash-script.png)

1. Abra o PowerShell ISE como administrador, copie e cole o script PowerShell que monitora o uso de disco em um novo arquivo, execute o script e verifique os resultados.

   ![](../../media/execute-ps-script.png)

### Você concluiu o Hackathon com sucesso.   
