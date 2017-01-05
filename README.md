#[EN] : PassGen
Wordlist Generator using key-words, options and recursivity

PassGen is a Wordlist generator: it take words as input and mix them to make all the possible combinaison at the output. PassGen also take a minimum size and a maximum size for the generated words. 

The script propose also additionals "extra" chars to add at the end of each words for completing the combo. User can define max number of extra-char to add at the end. Words without extra chars will still be generated. 
Ti may be usefull when someone add a number or #/@ at the end.

The scripts may be usefull for guessing 

For example, if the script take "a" "b" and "c" with min size 0 and max size 3, output will be: a, b, c, aa, bb, cc, aaa, bbb, ccc, ab, ac, ba, bc, ca, cb, aab, aac, aba, abb, abc, aca, acb, acc, baa, bab, bac, bba, bbc, bca, bcb, bcc, caa, cab, cac, cba, cbb, cbc... ccb

# ARGMOD
Default script work under "argument" mode:

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

