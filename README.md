# plex-guide
Ein Guide für Leon

---

# Filme

Filme werden in den Ordner `/media/HDD1/Movies/filmtitel/` als `filmtitel_nummer.mp4` gespeichert. Optional mit einer anderen Dateiendung. Dafür gibt es mehrere Möglichkeiten, den Film auf den Plex Server zu kopieren:

### 1. einen oder mehrere Filme der gleichen Reihe mit Ordner:
  Dafür musst du einen Ordner auf deinem PC erstellen mit dem Name des Filmes / der Reihe. Keine Leerzeichen sondern Worte mit "_" trennen. In dem Ordner müssen alle Dateien diesem Muster entsprechen: `filmtitel_nummer.mp4`.
  Anschließend musst du diese Befehle ausführen:
  
  1. in den Ordner navigieren, in dem der Ordner liegt, der auf den Server soll:
  ```SHELL
  cd /mnt/laufwerkbuchstabe/pfad/zum/ordner/
  ```
  
  2. den gesamten Ordner kopieren:
  ```SHELL
  scp -r ordnername fibonatschi@plex:/media/HDD1/Movies/
  ```

### 2. einen Film einer Reihe ohne Ordner:
  Zuerst musst du den ordner auf dem Plex Server erstellen, sofern noch kein Film der Reihe auf dem Server liegt.
  
  1. mit dem Plex Server verbinden:
  ```SHELL
  ssh fibonatschi@plex
  ```
  
  2. in den Movies Ordner navigieren:
  ```SHELL
  cd /media/HDD1/Movies/
  ```
  
  3. den Ordner erstellen:
  ```SHELL
  mkdir name_der_reihe
  ```
  
  Danach musst du die Datei hochladen, dafür entweder die ssh Verbindung mit `exit` trennen oder einen anderen Tab im Terminal verwenden.

  1. in den Ordner navigieren, in dem die Datei liegt, der auf den Server soll:
  ```SHELL
  cd /mnt/<laufwerkbuchstabe>/pfad/zum/ordner/
  ```
  
  2. die Datei kopieren:
  ```SHELL
  scp dateiname.mp4 fibonatschi@plex:/media/HDD1/Movies/titel_der_reihe/filmtitel_nummer.mp4
  ```

### 3. mehrere Filme einer Reihe ohne Ordner:
  Zuerst musst du den ordner auf dem Plex Server erstellen, sofern noch kein Film der Reihe auf dem Server liegt.
  
  1. mit dem Plex Server verbinden:
  ```SHELL
  ssh fibonatschi@plex
  ```
  
  2. in den Movies Ordner navigieren:
  ```SHELL
  cd /media/HDD1/Movies/
  ```
  
  3. den Ordner erstellen:
  ```SHELL
  mkdir name_der_reihe
  ```
  
  Danach musst du die Dateien hochladen, dafür entweder die ssh Verbindung mit `exit` trennen oder einen anderen Tab im Terminal verwenden. Die Dateien müssen hierbei schon die Form `filmtitel_nummer.mp4` haben.

  1. in den Ordner navigieren, in dem die Dateien liegt, der auf den Server soll:
  ```SHELL
  cd /mnt/<laufwerkbuchstabe>/pfad/zum/ordner/
  ```
  
  2. die Dateien kopieren (es werden alle Dateien in diesem Ordner kopiert):
  ```SHELL
  scp * fibonatschi@plex:/media/HDD1/Movies/titel_der_reihe/
  ```

### 4. mehrere Reihen mit Ordner:
  TODO
  
---

# Serien

Filme werden in den Ordner `/media/HDD1/Series/serientitel/Stafel_staffelnummer/` als `serientitel_s<staffelnummer>e<episodennummer>.mp4` gespeichert. Optional mit einer anderen Dateiendung. Dafür gibt es mehrere Möglichkeiten, den Film auf den Plex Server zu kopieren:

### 1. eine ganze Serie kopieren


### 2. eine ganze Staffel kopieren


### 3. eine Episode kopieren


### 4. mehrere Serien kopieren
  TODO
