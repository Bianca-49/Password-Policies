# Password-Policies

În noua aplicație web pe care ați dezvoltat-o este necesară introducerea unor elemente suplimentare de securitate. Pentru asta veți dezvolta o bibliotecă de Password Policies. Aceste politici de parolă sunt configurate de fiecare client care folosește biblioteca voastră și apoi fiecare parola setată de utilizatori este verificată contra acestor reguli. Ele sunt:

Length - restricția poate specifica lungimea minimă sau lungimea minimă și maximă a unei parole.
Class - restricția spune câte clase diferite de caractere trebuie să aibă minim parola; clasele sunt: literă mică, literă mare, cifră și alte caractere
Must Include - parola trebuie obligatoriu să includă cel puțin un caracter din clasa specificată.
Must Not Include - parola trebuie obligatoriu să NU includă niciun caracter din clasa respectivă.
Repetition - restricția impune de câte ori se poate repeta consecutiv același caracter în parolă
Consecutive - restricția impune un număr maxim de caractere consecutive (ex: abc sau 123)

Cerință
Dându-se un set de politici de parolă sigură și apoi o listă de parole, să se afișeze pentru fiecare din ele OK sau NOK, în funcție de respectarea sau nu a tuturor acestor politici.

Date de intrare
Pe prima linie se află un număr întreg pozitiv n, necunoscut de mare, reprezentând numărul de reguli care trebuie respectate. Pe următoarele n linii se află definiția unei reguli, în următoarele formate posibile:

length <min_length> - parola trebuie să aibă min_length caractere (inclusiv); 0 < min_length
length <min_length> <max_length> - parola trebuie să aibă între min_length și max_length caractere (inclusiv); 0 < min_length <= max_length
class <min_class_count> - parola trebuie să aibă minim min_class_count tipuri de caractere diferite (literă mică, literă mare, cifră și alte caractere); 0 < min_class_count < 5
include <class> - parola trebuie obligatoriu să includă cel puțin un caracter din clasa specificată; class poate fi a, A, 0 sau $, caractere ce denotă clasa dorită
ninclude <class> - parola trebuie obligatoriu să nu includă niciun caracter din clasa specificată; class urmează aceleași reguli de mai sus
repetition <max_count> - același caracter se poate repeta pe poziții consecutive de maxim max_count ori; 0 < max_count
consecutive <max_count> - parola poate avea max_count caractere consecutive în secvență; 0 < max_count
Pe următoarele linii, până la EOF, se află câte o parolă pe linie, ce vor fi verificate cu regulile specificate.

Date de ieșire
Pentru fiecare parolă verificată, se va afișa OK dacă parola respectă TOATE regulile specificate, sau NOK dacă există măcar o regulă care nu este respectată.
