# Readme

% ju -- https://bw1.eu -- 10-Okt-18  -- Readme.md

## Hinweis

Projekt getestet unter Win10


Git: <https://git-scm.com/downloads>

~~~
  # Shell: Git version
  git --version
~~~


## Repository ordnerpaket-Entwicklung von Github downloaden

~~~
  # Shell: Kopie downloaden
  $ git clone https://github.com/ju-bw/ordnerpaket-Entwicklung.git .
~~~

## neues Repository auf github anlegen

~~~
  # https://github.com/new
  # github: Create a new repository
  # Repository name = ordnerpaket-Entwicklung
  # Shell: Git Befehle
  # ".gitconfig", ".gitignore" konfigurieren und erstellen
  git init
  git add .
  git commit -am "Projekt start"
  git remote add origin https://github.com/ju-bw/ordnerpaket-Entwicklung.git
  git push -u origin master 
  git status
  git pull
  git push
  git status
~~~

## Zip

~~~
  $timestampArchiv = Get-Date -Format 'yyyy-MMM-dd' # 2018-Okt-11
  $thema = "ordnerpaket-Entwicklung"           # Thema
  $archiv = "archiv"
  ls ./ | Compress-Archive -Update -dest "./$archiv/$timestampArchiv-$thema.zip" # Komprimieren
~~~