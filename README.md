
Here i will show you how to check or fetch for your publicIP adresss.

to create a powershell code that retrieves our ip address we need to use a web api to make it easy, we put this command in ours windows powershell.




function Get-PublicIP {
    try {
        $ip = Invoke-RestMethod -Uri "https://api.ipify.org?format=text"
        Write-Output "Your public IP address is: $ip"
    }
    catch {
        Write-Output "Error: Unable to retrieve public IP address. Please check your internet connection."
    }
}



and after we done this we can use a much for simple command "Get-PublicIP"
and it will show us our ip adress.


and i solved this with help from Chatgbt.
