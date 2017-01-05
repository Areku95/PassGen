#[EN] : PassGen
Wordlist Generator using key-words, options and recursivity

PassGen is a Wordlist generator: it take words as input and mix them to make all the possible combinaison at the output. PassGen also take a minimum size and a maximum size for the generated words. 

For example, if the script take "a" "b" and "c" with min size 0 and max size 3 in input, output will be: a, b, c, aa, bb, cc, aaa, bbb, ccc, ab, ac, ba, bc, ca, cb, aab, aac, aba, abb, abc, aca, acb, acc, baa, bab, bac, bba, bbc, bca, bcb, bcc, caa, cab, cac, cba, cbb, cbc... ccb
The script propose also additionals "extra" chars to add at the end of each words for completing the combo. User can define max number of extra-char to add at the end. Words without extra chars will still be generated. 
It may be usefull when someone add a number or #/@ at the end of his password ;) !.

The scripts may be also usefull for guessing email address : user can define with what does the generated words should start and with what should they finish (prefix / suffix).

The script also propose option to add such as lower-case words, L33T 5P34K words ... (see Words Options)

The script regularly removes duplicated words.

# ARGMOD
Default script work in command-line ("argument" mode):

        -m : Min Size for the generated words
        -M : Max Size for the generated words
        -o : Ouput file
        -ws : Word Start (each words will start with)
        -we : Word End (each words will end with)
        -i : Input file, each line will be add to the start list as a Word
        -w : Input words, MUST BE THE LAST ARG

      Words Options :

        -ab : add lowercase words
        -AB : add UPPERCASE words
        -Ab : add lowercase words with uppercase first letter 
        -ba : add reverse word in lowercase
        -Ba : add reverse word in lowercase with uppercase first letter
        -BA : add reverse word in UPPERCASE
        -L337 : add word in L33T 5P34K


Examples :


>python passgen.py -m 5 -M 12 -w foo bar abc zeecka words nice

>python passgen.py -m 4 -we @live.com -i inputfile.txt

>python passgen.py -M 15 -ws Alex -we .fr -i inputfile.txt

>python passgen.py -M 10 -i inputfile.txt -o ouputfile.txt

>python passgen.py -m 5 -M 7 -i inputfile.txt -ab -AB -L337

You can also edit the script by setting ARGMOD to False value: ARGMOD = False

And then set manually the wordstart, maxSize...

#[FR] : PassGen
Générateur de Dictionaires (wordlist) utilisant des mots clés, options et de la recursivité

PassGen est un générateur de Dictionaires (wordlist): Il prends des mots en entrée et les mélange pour renvoyer en sortie toutes les possibilités de combinaisons et "combo" possibles. PassGen prend également en paramètre une taille minimum et maximum pour les mots générés.

Par exemple, si le script prend "a" "b" et "c" avec comme min size 0 et max size 3 en entrée , alors la sortie sera: a, b, c, aa, bb, cc, aaa, bbb, ccc, ab, ac, ba, bc, ca, cb, aab, aac, aba, abb, abc, aca, acb, acc, baa, bab, bac, bba, bbc, bca, bcb, bcc, caa, cab, cac, cba, cbb, cbc... ccb

Le script propose également d'ajouter des caractères supplémentaires en fin de mots. L'utilisateur peut définir le nombre maximum de caractère à ajouter.Les mots sans caractères supplémentaires seront bien entendu présent dans la sortie. 
Cela peut être utile quand quelqun ajoute un #/@ à la fi de son mot de passe ;) !.

Le script peut être également utile pour deviner de addresses mails: l'utilisateur peut définir par quoi doivent commencer et finir les mots générés (préfix / suffix).

Le script propose également des options comme ajouter les mots en minuscules, les mots en L33T 5P34K ... (voir Options)

Le script supprimé régulièrement les doublons.


# ARGMOD
Par default, le script fonctionne en commande-line (mode "argument"):

        -m : Taille minimum des mots générés
        -M : Taille maximum des mots générés
        -o : Fichier de sortie
        -ws : Préfixe (chaque mots commenceront par ...)
        -we : Suffixe (chaque mots finiront par ...)
        -i : Fichier d'entrée, chaque ligne sera défini comme un mot ajouté à la liste de départ
        -w : Les mots suivant la balise seront ajoutés aux mots d'entrée, CELA DOIT ETRE LE DERNIER ARGUMENT

      Options :

        -ab : ajoute les mots entrés en minuscule
        -AB : ajoute les mots entrés en MAJUSCULE
        -Ab : ajoute les mots entrés en minuscule avec la première lettre en majuscule
        -ba : ajoute les mots entrés en renversés et en minuscule
        -Ba : ajoute les most entrés en renversés et en minuscule avec la première lettre en majuscule
        -BA : ajoute les mots entrés en renversés et en MAJUSCULE
        -L337 : ajoute les mots entrés en L33T 5P34K


Exemples :


>python passgen.py -m 5 -M 12 -w foo bar abc zeecka words nice

>python passgen.py -m 4 -we @live.com -i inputfile.txt

>python passgen.py -M 15 -ws Alex -we .fr -i inputfile.txt

>python passgen.py -M 10 -i inputfile.txt -o ouputfile.txt

>python passgen.py -m 5 -M 7 -i inputfile.txt -ab -AB -L337

Vous pouvez égallement éditer le script en passant ARGMOD sur sa valeur False: ARGMOD = False

Pour ensuite définir manuellement le préfix, la taille maximum...
