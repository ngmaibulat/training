### Basics

```bash
grep [options] pattern [files]


cat /etc/passwd | grep root
grep root /etc/passwd
```

### Context Control

```bash
  -B, --before-context=NUM  print NUM lines of leading context
  -A, --after-context=NUM   print NUM lines of trailing context
  -C, --context=NUM         print NUM lines of output context

grep backup /etc/passwd -C 1 # print the matched line + one line and one line after the matched line
```

### Regex variations:

```
  -E, --extended-regexp     PATTERNS are extended regular expressions
  -F, --fixed-strings       PATTERNS are strings
  -G, --basic-regexp        PATTERNS are basic regular expressions
  -P, --perl-regexp         PATTERNS are Perl regular expressions
  -e, --regexp=PATTERNS     use PATTERNS for matching
```

### Load Patterns (regex) from file

```
  -f, --file=FILE           take PATTERNS from FILE

echo root > filter.txt
echo admin >> filter.txt
grep -f filter.txt /etc/passwd
```

### Specify multiple patterns in CLI

```
grep -e root -e admin /etc/passwd
```

### Search in multiple files

```
grep root *.txt
grep -f filter.txt *.txt

grep root *.txt
grep -R -f filter.txt
```

### Case insensitive search

```
wget https://gist.githubusercontent.com/kalinchernev/486393efcca01623b18d/raw/daa24c9fea66afb7d68f8d69f0c4b8eeb9406e83/countries -O country.txt

grep -i ge country.txt
```

### Match whole word

```
grep Niger country.txt
grep -w Niger country.txt
```

### Words

```
sudo apt install wamerican
sudo apt install wamerican-insane
sudo apt install wfrench
sudo apt install wgerman-medical

cat /usr/share/dict/american-english | wc -l
cat /usr/share/dict/american-english-insane | wc -l
cat /usr/share/dict/french  | wc -l
cat /usr/share/dict/german-medical | wc -l

grep linu /usr/share/dict/american-english-insane
```

### Using '.'

```
grep zealand  /usr/share/dict/american-english-insane
grep ze.land  /usr/share/dict/american-english-insane
```

### Special symbols

```
'.'  Match any symbol

'?'  The preceding item is optional and is matched at most once.

'*'  The preceding item is matched zero or more times.

'+'  The preceding item is matched one or more times.

'{n}' The preceding item is matched exactly n times.

'{n,}' The preceding item is matched n or more times.

'{,m}' The preceding item is matched at most m times. This is a GNU extension.

'{n,m}' The preceding item is matched at least n times, but not more than m times.
```

### Start/End of line

```
^str   line starts with 'str'
str$   line ends with 'str'
```

### []

```bash
[abcd] a or or c or

grep '^[ab]' /usr/share/dict/american-english #line that start by 'a' or 'b'
```

### Character Classes

```
‘[:alnum:]’
Alphanumeric characters: ‘[:alpha:]’ and ‘[:digit:]’; in the ‘C’ locale and ASCII character encoding, this is the same as ‘[0-9A-Za-z]’.

‘[:alpha:]’
Alphabetic characters: ‘[:lower:]’ and ‘[:upper:]’; in the ‘C’ locale and ASCII character encoding, this is the same as ‘[A-Za-z]’.

‘[:blank:]’
Blank characters: space and tab.

‘[:cntrl:]’
Control characters. In ASCII, these characters have octal codes 000 through 037, and 177 (DEL). In other character sets, these are the equivalent characters, if any.

‘[:digit:]’
Digits: 0 1 2 3 4 5 6 7 8 9.

‘[:graph:]’
Graphical characters: ‘[:alnum:]’ and ‘[:punct:]’.

‘[:lower:]’
Lower-case letters; in the ‘C’ locale and ASCII character encoding, this is a b c d e f g h i j k l m n o p q r s t u v w x y z.

‘[:print:]’
Printable characters: ‘[:alnum:]’, ‘[:punct:]’, and space.

‘[:punct:]’
Punctuation characters; in the ‘C’ locale and ASCII character encoding, this is ! " # $ % & ' ( ) * + , - . / : ; < = > ? @ [ \ ] ^ _ ` { | } ~.

‘[:space:]’
Space characters: in the ‘C’ locale, this is tab, newline, vertical tab, form feed, carriage return, and space. See Usage, for more discussion of matching newlines.

‘[:upper:]’
Upper-case letters: in the ‘C’ locale and ASCII character encoding, this is A B C D E F G H I J K L M N O P Q R S T U V W X Y Z.

‘[:xdigit:]’
Hexadecimal digits: 0 1 2 3 4 5 6 7 8 9 A B C D E F a b c d e f.
```

### Special Backslash Expressions

```
‘\b’
Match the empty string at the edge of a word.

‘\B’
Match the empty string provided it’s not at the edge of a word.

‘\<’
Match the empty string at the beginning of a word.

‘\>’
Match the empty string at the end of a word.

‘\w’
Match word constituent, it is a synonym for ‘[_[:alnum:]]’.

‘\W’
Match non-word constituent, it is a synonym for ‘[^_[:alnum:]]’.

‘\s’
Match whitespace, it is a synonym for ‘[[:space:]]’.

‘\S’
Match non-whitespace, it is a synonym for ‘[^[:space:]]’.

‘\]’
Match ‘]’.

‘\}’
Match ‘}’.
```

### Resources

- https://www.gnu.org/software/grep/manual/grep.html
