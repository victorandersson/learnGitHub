Lär dig Github!
===========

Instruktioner för att snabbt och enkelt komma igång med github.

## Del 1. Installera Git
* Skapa användare på github.com

* Ladda ner Git från http://git-scm.com/

* Följ instruktionerna och välj "Run Git from the Windows Command Promt" och "Checkout Windows-Style" alternativen när tillfrågad.

## Del 2. Sätt upp din användare
* git config --global user.name "JohnDoe"

* git config --global user.email your_email@example.com

## Del 3. Generera ssh-nyckel
Kontrollera om du har en nyckel genom att köra:
* cd ~/.ssh

Om en nyckel hittas fast du ändå vill skapa en ny så kan du köra nedanstående så sparas nyckeln i en backup-mapp:
* mkdir key_backup

*  cp id_rsa*
   
*  rm id_rsa* 


För att skapa en ny nyckel körs kommandot:
* ssh-keygen -t rsa -C "your_email@example.com" 

Det kommer komma lite frågor om var man vill lagra nyckel och om passphrases, det går bra att bara trycka enter.

Nu ska vi kopiera in nyckel till github, vi använder oss utav kommandotalken att spara nyckeln då det är väldigt noga att inte få med ofrivilliga "new line"-tecken
* clip < ~/.ssh/id_rsa.pub

* Account Settings -> SSH Keys -> Add SSH key -> * klistra in nyckeln i textfältet * - > Add Key -> Fyll i Github lösenord

Nedanstående tester att en koppling finns till Github och att dina nycklar stämmer överens. Första gången detta körs så kommer kommandotolken fråga om du vill autentisiera hosten (github), accpetera detta för att slutföra.
* ssh -T git@github.com

Om "Hi xxxx! .." kommer upp så har allting lyckats.

## Del 4. Hantera Git-Projekten
Gå till https://github.com/AntonAderum/learnGitHub i webbläsaren och tryck på "Fork" knappen. Detta kopierar hela mitt projekt till er Github användare.
Använd kommandotolken och gå till mappen där du vill ladda ner projektet i din dator. Skriv sedan nedanstående för att klona ner projektet från er github-sida till er dator.

* git clone git@github.com:XXX/learnGitHub.git

Ändra i iWasHere.txt och fyll i ditt namn. Använd valfri editor.
Skriv sedan följande rader i kommandotolken för att lägga till filer och göra en "commit" med ett meddelande, och sedan pusha upp det till er github-sida.
* git status

* git add - A

* git commit -m "Jag skrev in mitt namn"

* git status

* git push

Gå till ert github-projekt och tryck på "Pull Request" och följ instruktionerna för att be orginal-projektet att pulla ert projektet in till orginalet.

Klart!



##Andra andvändbara kommandon.

* git pull : hämtar den mest uppdaterade versionen av githubprojektet som du står i. 

* git config --local user.name "JohnAlive" : Ändra username i ett lokalt gitprojekt. 

* git reset --hard \<commit ID\>


