Vul onderstaande aan met de antwoorden op de vragen uit de readme.md file. Wil je de oplossingen file van opmaak voorzien? Gebruik dan [deze link](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) om informatie te krijgen over
opmaak met Markdown.


# Configuratie productieserver
Ik heb een nieuwe instance aangemaakt in aws voor de productieserver

![screenshot docker productieserver](images/Scherm­afbeelding%202024-11-13%20om%2017.57.15.png)



a) 
# Configuratie docker en jenkins
Ik heb docker geinstalleerd op de testserver via de gegeven installatie gids.

![screenshot docker testserver](images/Scherm­afbeelding%202024-11-13%20om%2017.27.08.png)

Om te zorgen dat er geen `sudo` kan worden gebruikt in de jenkinsfile heb ik het volgende commando gebruikt

`sudo usermod -aG docker ${USER}`

Om te zorgen dat jenkins dit ook kan heb ik jenkins toegang gegeven tot de opt map. Dan kan jenkins docker gebruiken

`sudo chown -R jenkins:jenkins /opt/`

`sudo chmod -R u=rwx /opt/`

`sudo usermod -aG docker jenkins`

b)

