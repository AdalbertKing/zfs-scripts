# SnapSend & DelSnaps

## Opis

SnapSend i DelSnaps to skrypty do automatyzacji tworzenia i usuwania migawek ZFS.

### Funkcje SnapSend

- Automatyczne tworzenie migawek
- Wysyłanie migawek na zdalne serwery lub lokalne dataset'y
- Obsługa transferów inkrementalnych i pełnych
- Opcjonalna obsługa kompresji i mbuffer

### Funkcje DelSnaps

- Usuwanie starych migawek na podstawie określonych kryteriów czasu
- Obsługa operacji rekurencyjnych

### Opcje SnapSend

- `-m <snapshot_prefix>`: Niestandardowy prefix dla migawek.
- `-u <remote_user>`: Niestandardowy użytkownik SSH.
- `-R`: Włączenie rekurencji.
- `-b`: Użycie mbuffer do transferu danych.
- `-z`: Włączenie kompresji podczas transferu.

### Przykłady użycia SnapSend

#### Zdalny backup
```bash
./snapsend.sh -m "automated_hourly_" -R "hdd/tests,rpool/data/tests" "192.168.28.8:hdd/kopie"
