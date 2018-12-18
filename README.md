# command-line-games

## Spel 1 - Guess the Number

Skapa en kommandopromptsbaserad version av ett spel där användaren ska gissa ett hemligt tal.

Spelet ska slumpmässigt välja ett hemligt tal från och med 1 till och med en svårighetsgrad som användaren väljer.

Användaren får sen, om och om igen, tills hen gissat rätt, gissa vad det hemliga talet är.

Om hen gissar fel ska programmet skriva ut att gissningen var för låg eller för hög.

När användaren gissat rätt avslutas spelet, och antalet gissningar skrivs ut.

### Att slumpa tal
I ruby finns en inbyggd funktion för att slumpa ett tal `rand()`.
Den går att använda på två sätt.
* `rand()` slumpar ett flyttal mellan 0 och 1.
* `rand(num)` slumpar ett tal mellan `0` och `num-1` .
   * ex. `rand(10)` slumpar ett tal mellan `0` och `9`.

### Exempel

```
> Welcome To "Guess the Secret Number"!
> Select Difficulty!
> 10
> Guess the secret number (1-10)
> Make a guess!
< 5
> 5 is lower than the secret number.
> Make a guess!
< 7
> 7 is higher than the secret number.
> Make a guess!
< 6
< Correct! The secret number was 6!
< It took you 3 guesses. Good job!
```

## Spel 2 - Jotto

Jotto är en ordlek som man vanligtvis spelar två och två mot varandra. Den här uppgiften går ut på att skapa envariant av Jotto där man spelar mot datorn. För att läsa mer om jotto, se http://en.wikipedia.org/wiki/Jotto

Programmet väljer slumpvis ett ord (med bara tre bokstäver) från en fil (här kan du skapa en egen ordlista: [http://app.aspell.net/create](http://app.aspell.net/create))

Programmet ber sen spelaren att gissa vilket ordet är.

Programmet skriver sen ut hur många bokstäver som det gissade ordet har gemensamt med dethemliga ordet.

Detta skall upprepas tills spelaren gissar rätt, då programmet skall tala om hur många gissningar det tog.

Programmet frågar sen om spelaren vill spela en gång till.

### Exempel: (Det hemliga ordet är ”eat”)

```
> Welcome to Jotto!
> Guess the secret word (3 letters long)
> Make a guess!
< owl
> "owl" has 0 characters in commom with the secret word
> Make a guess!
< are
> "are" has 2 characters in common with the secret word
> Make a guess!
< ate
> "ate" has 3 characters in common with the secret word
> Make a guess!
< eat
> Correct! The secret word was "eat".
> It took you 4 guesses!
> Would you like to play again? (Y/N)
```

Du får själv bestämma hur spelet bestämmer hur många gissningar användaren får.

## Spel 3 - Mastermind

[Mastermind](https://en.wikipedia.org/wiki/Mastermind_(board_game)) går ut på att hitta rättfärgkombination hos en rad med dolda pjäser. Spelaren gissar på en rad och spelledaren markerar hur många pjäster som är helt rätt (rätt färg och rättposition).

I vår version av Mastermind kommer vi byta utfärgerna mot siffror och markeringar kommer ske med ”x” och ”o” istället. (I vår version bryr vi oss inte om att markera om användaren har gissat på rätt siffra, men fel plats)

### Exempel

| Rätt rad (hemlig) | 1    | 4    | 5    | 4    |
| ----------------- | ---- | ---- | ---- | ---- |
| Gissning          | 6    | 4    | 5    | 6    |
| Markering         | O    | X    | X    | O    |

Programmet skall slumpa fram en rad med siffror från och med 1 till och med 6.
Användaren skall sen få gissa och få se resultatet av sin gissning. 

Ex: (den hemliga raden är 1337)

```text indikerar inmatning)
> Welcome to Mastermind!
> Guess the secret combination!
< 1234
> xoxo
> Guess again
< 1732
> xoxo
< 1337
> Correct! it took 3 guesses!
```

### Bonusbana

Hitta på ett sätt att visa om användaren har gissat på rätt siffra, men på fel position

## Spel 4 - Hangman

Skapa en kommandopromptsbaserad version av spelet hänga gubbe.

Spelet ska slumpmässigt välja ett ord från en fil med ord (här kan du skapa en egen ordlista: [http://app.aspell.net/create](http://app.aspell.net/create))

Du får själv bestämma hur spelet bestämmer hur många gissningar användaren får.

### Exempel

```
> Welcome to Hangman!
> Guess the Secret Word:
> _ _ _ _ _ _ _ _ _
< e
> E is in the word!
> _ _ _ e _ _ _ _ e
> Guessed letters: E
< I 
< I is in the word!
> _ i _ e _ _ _ _ e
> Guessed letters: E,I
< o 
> O is NOT in the word!
> Guessed letters: E,I,O
> You have 5 more guesses
```
### Bonusbana 1

Gör det möjligt för användaren gissa på hela ordet

### Exempel

```
...
< o 
> O is NOT in the word!
> _ i _ e _ _ _ _ e
> Guessed letters: E,I,O
> You have 5 more guesses
< pineapple
> Correct! The secret word was Pineapple!
```

### Bonusbana 2

Skapa ASCII-baserad grafik för att illustrera gubben

### Exempel

```
   ____
  |    |      
  |    o      Guessed : E,I,O
  |   /|\     
  |    |
  |   /
 _|_
|   |______
|          |
|__________|
 
Word: _ i _ e _ _ _ _ e
Guess :
```

## Spel 5 - Covert Action Crypto

I MicroProse spel [Covert Action](https://en.wikipedia.org/wiki/Sid_Meier's_Covert_Action) från 1990 finns ett [minispel där man ska avkryptera en text](https://youtu.be/oSGJ1JVj2dI?t=9m20s).

Försök skapa en version av minispelet i kommandoprompten.

Programmet ska läsa in text från en fil, och slumpa ut vilka bokstäver som ska "byta plats".

## Spel 6 - Fallout Terminal Hacking.

I spelet Fallout 3 finns ett hacking minigame. Försök skapa en kommandopromptsbaserad klon av spelet. 

Här finns en webbaserad klon som du kan använda som inspiration: [http://mitchellthompson.net/demos/terminal/](http://mitchellthompson.net/demos/terminal/). 

Eftersom man inte kan klicka i kommandoprompten för att göra sina val får du hitta på en annan lösning.

