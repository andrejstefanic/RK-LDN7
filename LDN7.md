Ugotovili smo, da je komuniciranje preko foruma spletni učilnici zamudno in nepraktično. Študenti bi radi med seboj komunicirali zanesljivo in v realnem času. Na spletu obstaja veliko rešitev, ki bi bile primerne, a nobena ne ustreza vsem našim zahtevam. Tako nam ne ostane drugega, kot da kot pravi računalničarji sprogramiramo svojo rešitev

Na voljo imate dve delni implementaciji (Java in Python), ki sta zelo preprosti, saj pošiljata le enovrstična, tekstovna sporočila. Izberite si enega od programskih jezikov in dopolnite oba programa (pogovorni strežnik in klient) tako, da bosta sposobna pošiljati in sprejemati strukturirane podatke.

ChatServer.java
ChatClient.java
chatServer.py
chatClient.py


Sporočila
V nalogi morate implementirati vsaj 4 tipe sporočil:

pošiljanje imena uporabnika - ko odjemalec pridobi ime uporabnika, ga s tem sporočilom pošlje na strežnik,
javno sporočilo - javna sporočila so namenjena vsem prijavljenim uporabnikom, zato jih strežnik razpošlje na vse odjemalce (že narejeno),
privatno sporočilo - privatna sporočila pošlje strežnik le naslovniku sporočila in
sporočilo o napaki - ta tip sporočila naj se uporablja za sporočanje napak, npr. ko ni mogoče najti naslovnika privatnega sporočila.
V trenutni implementaciji se med strežnikom in odjemalci pošiljajo preprosta sporočila v obliki niza znakov. To morate nadgraditi tako, da bodo sporočila strukturirana in sestavljena iz več polj, na primer:

tip sporočila,
ime pošiljatelja,
čas pošiljanja in
besedilo sporočila.
Za implementacijo strukturiranih sporočil imate več možnosti:

uporabite lahko namenske formate, recimo XML ali JSON. V tem primeru priporočamo uporabo knjižnic po lastni izbiri, na primer:
za delo z JSON v jeziku Java - json-simple ali
za delo z JSON v jeziku Python - json.
lahko si izmislite svoj format - zgledujte se po protokolih, ki smo jih obravnavali na vajah.

Delovanje pogovornega strežnika in odjemalca
Strežnik in odjemalec morata na posamezne tipe sporočil primerno odreagirati . Delo si boste olajšali, če boste vsako sporočilo tudi izpisali v komandno vrstico.

Vsa sporočila, ki se pošiljajo med strežnikom in odjemalci, morajo biti strukturirana.
Uporabnik se mora v odjemalca prijaviti z imenom, odjemalec nato na strežnik sporoči ime uporabnika.
Odjemalec naj omogoča uporabniku pošiljanje javnih in privatnih sporočil. Sami se odločite, kako bo uporabnik preko komandne vrstice določil tip sporočila, naslovnika in besedilo sporočila.
Strežnik mora javna in privatna sporočila ustrezno pošiljati na odjemalce.
V kolikor strežnik ne more najti naslovnika privatnega sporočila, naj pošiljatelju pošlje pošiljatelju sporočilo o napaki.
Vsako sporočilo, ki ga strežnik pošlje odjemalcu, mora biti opremljeno z imenom pošiljatelja.
