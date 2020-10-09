# S7-1x00 DataLog Download
Skrypty wspierające proces pobierania logów danych na serwerze WWW w sterownikach SIMATIC S7-1200/1500. Dla każdej wersji sterownika dostępne są dwie wersje skryptu:
<ul>
 <li>Pobieranie wszystkich logów w postaci archiwum ZIP</li>
 <li>Listowanie logów na stronie WWW zdefiniowanej przez użytkownika i selektywne pobieranie logów</li>
</ul>

### Przetestowane sterowniki
<ul>
 <li>S7-1200 FW V4.4 (niepełna funkcjonalność)</li>
 <li>S7-1500 FW V2.8</li>
</ul>
Pobieranie logów danych w postaci archiwum ZIP na sterownikach S7-1200 nie działa dla dużej ilości logów z uwagi na niską wydajność serwera. Być może zmieni się to w kolejnych wersjach firmware. Alternatywna opcja (automatyczne pobieranie logów jeden po drugim) jest <strong>aktualnie w przygotowaniu</strong>.

### Konfiguracja w TIA Portal
<ul>
 <li>Umieść wszystkie pliki z repozytorium (dot. właściwego sterownika) w folderze zdefiniowanym jako główny katalog serwera WWW w TIA Portal</li>
 <li>Nie dodawaj rozszerzenia .js w sekcji "files with dynamic content" w ustawieniach serwera WWW</li>
 <li>Zmień stronę główną z "index.htm" na "index.html" w ustawieniach serwera WWW</li>
 <li>Skrypty nie uwzględniają autoryzacji użytkowników dlatego konieczne jest ustawienie praw dostępu do plików na "Everyone"</li>
</ul>
<strong>Nie ma potrzeby modyfikacji kodu źródłowego skryptów - adres IP sterownika czytany jest automatycznie z adresu URL w przeglądarce</strong>

### Referencje
Skrypt wykorzystuje następujące biblioteki dostepne na licencji MIT:
<ul>
 <li>https://github.com/Stuk/jszip</li>
 <li>https://github.com/eligrey/FileSaver.js</li>
</ul>
