# Readme

% ju -- https://bw1.eu -- 26-Okt-18  -- Readme.md

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

Commits, Referenzen, Verzweigungen und Zusammenführungen visualisieren.

**GitViz** <https://github.com/Readify/GitViz/releases>

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
  #git log --oneline  # less beenden mit <Shift+q>
  git log --graph --oneline --decorate
  git log --graph --pretty=format:";  %cn;  %h;  %ad;  %s" --date=relative > log.txt
~~~

## Zip

~~~
  $timestampArchiv = Get-Date -Format 'yyyy-MMM-dd' # 2018-Okt-11
  $thema = "ordnerpaket-Entwicklung"           # Thema
  $archiv = "archiv"
  if(test-path "./$archiv/$timestampArchiv-$thema.zip"){
    rm "./$archiv/$timestampArchiv-$thema.zip" -force -recurse
  }
  ls ./ | Compress-Archive -Update -dest "./$archiv/$timestampArchiv-$thema.zip" # Komprimieren
~~~