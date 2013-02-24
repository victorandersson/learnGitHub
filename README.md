Lär dig Github!
===========

Instruktioner för att snabbt och enkelt komma igång med github.

## Del 1. Installera Git
0: Skapa användare på github.com

1: Ladda ner Git från http://git-scm.com/

2: Följ instruktionerna och välj "Run Git from the Windows Command Promt" och "Checkout Windows-Style" alternativen när tillfrågad.

## Del 2. Sätt upp din användare
3: git config --global user.name "JohnDoe"

4: git config --global user.email your_email@example.com

## Del 3. Generera ssh-nyckel
5: cd ~/.ssh

6: mkdir key_backup

   cp id_rsa*
   
   rm id_rsa* 
   
(om det redan fanns en ssh-nyckel)

7: ssh-keygen -t rsa -C "your_email@example.com" 

8: Det kommer komma lite frågor om var man vill lagra nyckel och om passphrases, det går bra att bara trycka enter.

9: clip < ~/ssh/id_rsa.pub

10: Account Settings -> SSH Keys -> Add SSH key -> * klistra in nyckeln i textfältet * - > Add Key -> Fyll i Github lösenord

11: ssh -T git@github.com

12: Ovanstående försöker göra en anslutning till github, kommandotolken kommer att fråga om du vill autentisera github.com, skriv "yes" och gå vidare.

13: Om "Hi xxxx! .." kommer upp så har allting lyckats.

## Del 4. Hantera Git-Projekten
14: Gå till https://github.com/AntonAderum/learnGitHub i webbläsaren och tryck på "Fork" knappen. Detta kopierar hela mitt projekt till er Github användare.

15: Använd kommandotolken och gå till mappen där du vill ladda ner projektet.

16: git clone git@github.com:XXX/learnGitHub.git

17: Ändra i iWasHere.txt och fyll i ditt namn. Använd valfri editor.

18: git status

19: git add - A

20: git commit -m "Jag skrev in mitt namn"

21: git status

22: Gå till ert github-projekt och tryck på "Pull Request" och följ instruktionerna

23: Klart!



##Andra andvändbara commandon.

git pull : hämtar den mest uppdaterade versionen av githubprojektet som du står i. 

git config --local user.name "JohnAlive" : Ändra username i ett lokalt gitprojekt. 