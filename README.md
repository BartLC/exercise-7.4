Maak een powershell script waarmee je een nieuwe gebruiker aanmaakt in de OU Sint-Niklaas

1° Maak gebruik van variabelen en vraag de naam en het wachtwoord van de gebruiker op met Reads-host

2° Zorg dat de overige parameters correct ingevuld worden.

$voornaamNaam = "Jo Lranan"
$Naam = "Lranan"
$wachtwoord = Read-Host "wachtwoord"
New-ADUser -Name $voornaamNaam -AccountPassword `
( ConvertTo-SecureString -AsPlainText $wachtwoord -Force) `
-DisplayName $voornaamNaam `
-SamAccountName $Naam `
-Enabled $true
