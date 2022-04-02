## Domeny białkowe

### Zad. 1 - Serwis Pfam (modele HMM)
> **Pfam** jest bazą domen białkowych. Każda domena w bazie jest przedstawiona za pomocą ukrytego modelu Markowa (HMM) utworzonego z przyrównania (*seed alignment*) konserwatywnych oraz reprezentatywnych sekwencji danej rodziny białkowej. Serwis Pfam umożliwia identyfikację potencjalnych domen białkowych w sekwencji białkowej użytkownika. Polega to na przyrównaniu modeli HMM do sekwencji zapytania i identyfikacji istotnych statystycznie przyrównań (najbardziej prawdopodobnych domen). W związku z tym, że sposób oceniania prawdopodobieństw w przypadku HMM jest bardziej złożony niż w przypdaku metod opartych na profilach, ich wykorzystanie zwiększa czułość dopasowywania sekwencji do bazy danych.


Otwórz serwis [Pfam](https://pfam.xfam.org) i zidentyfikuj domeny białkowe obecne w poniższej sekwencji: 
```
>sequence
NNRNQDNYVSWSDSEDDDEDEEIEEKEKPETNFPSPFTNILCGIIFVERRYTAVVLNRLI
KEAGKQDPELAYISSNFITGHGIGKNQPRNKQMEAEFRKQEEVLRKFRAHETNLLIATSI
VEEGVDIPKCNLVVRFDLPTEYRSYVQSKGRARAPISNYIMLADTDKIKSFEEDLKTYKA
IEKILRNKCSKSVDTGETDIDPVMDDDDVFPPYVLRPDDGGPRVTINTAIGHINRYCARL
PSDPFTHLAPKCRTRELPDGTFYSTLYLPINSPLRASIVGPPMSCVRLAERVVALICCEK
LHKIGELDDHLMPVGKETVKYEEELDLHDEEETSVPGRPGSTKRRQCYPKAIPECLRDSY
PRPDQPCYLYVIGMVLTTPLPDELNFRRRKLYPPEDTTRCFGILTAKPIPQIPHFPVYTR
SGEVTISIELKKSGFMLSLQMLELITRLHQYIFSHILRLEKPALEFKPTDADSAYCVLPL
NVVNDSSTLDIDFKFMEDIEKSEARIGIPSTKYTKETPFVFKLEDYQDAVIIPRYRNFDQ
PHRFYVADVYTDLTPLSKFPSPEYETFAEYYKTKYNLDLTNLNQPLLDVDHTSSRLNLLT
PRHLNQKGKALPLSSAEKRKAKWESLQNKQILVPELCAIHPIPASLWRKAVCLPSILYRL
HCLLTAEELRAQTASDAGVGVRSLPADFRYPNLDFGWKKSIDSKSFISISNSSSAENDNY
CKHSTIVPENAAHQGANRTSSLENHDQMSVNCRTLLSESPGKLHVEVSADLTAINGLSYN
QNLANGSYDLANRDFCQGNQLNYYKQEIPVQPTTSYSIQNLYSYENQPQPSDECTLLSNK
YLDGNANKSTSDGSPVMAVMPGTTDTIQVLKGRMDSEQSPSIGYSSRTLGPNPGLILQAL
TLSNASDGFNLERLEMLGDSFLKHAITTYLFCTYPDAHEGRLSYMRSKKVSNCNLYRLGK
KKGLPSRMVVSIFDPPVNWLPPGYVVNQDKSNTDKWEKDEMTKDCMLANGKLDEDYEEED
EEEESLMWRAPKEEADYEDDFLEYDQEHIRFIDNMLMGSGAFVKKISLSPFSTTDSAYEW
KMPKKSSLGSMPFSSDFEDFDYSSWDAMCYLDPSKAVEEDDFVVGFWNPSEENCGVDTGK
QSISYDLHTEQCIADKSIADCVEALLGCYLTSCGERAAQLFLCSLGLKVLPVIKRTDREK
ALCPTRENFNSQQKNLSVSCAAASVASSRSSVLKDSEYGCLKIPPRCMFDHPDADKTLNH
LISGFENFEKKINYRFKNKAYLLQAFTHASYHYNTITDCYQRLEFLGDAILDYLITKHLY
EDPRQHSPGVLTDLRSALVNNTIFASLAVKYDYHKYFKAVSPELFHVIDDFVQFQLEKNE
MQGMDSELRRSEEDEEKEEDIEVPKAMGDIFESLAGAIYMDSGMSLETVWQVYYPMMRPL
IEKFSANVPRSPVRELLEMEPETAKFSPAERTYDGKVRVTVEVVGKGKFKGVGRSYRIAK
SAAARRALRSLKANQPQVPNS
```

1. Ile domen zostało zidentyfikowanych w analizowanej sekwencji?
2. W jakiej pozycji w sekwencji znajduje się domena `PAZ`?
   > Serwis Pfam przedstawia dwa typy koordynatów `start` i `end`. Pozycje start i end w kolumnie **Alignment** oznaczają region przyrównania sekwencji zapytania z modelem HMM (*Hidden Markov Model*) reprezentującym domenę. Z kolei, koordynaty **Envelope** wyznaczają region w sekwencji, który został dodatkowo probabilistycznie wyznaczony jako miejsce występowania domeny. Region **Envelope** jest zwykle kilka aminokwasów dłuższy niż region **Alignment** i wyznacza on prawdopodobne miejsce występowania domeny.
3. Podaj wartość `E-value` przyrównania domeny `PAZ` z modelem HMM.

#### Rekord domeny PAZ

Otwórz stronę rekordu domeny `PAZ`.

4. Podaj numer dostępu tej domeny w bazie Pfam.
   > Numer dostępu zaczyna się od liter `PF`.
5. Jaką funkcję pełni ta domena (krótko)?
6. Ile gatunków (*species*) posiada tę domenę białkową?

Otwórz zakładkę `Species`.

7. Czy domena występuje u organizmów prokariotycznych?
8. W ilu gatunkach zwierząt (*Metazoa*) występuje ta domena?

Będąc w zakladce `Species`, kliknij na kartę `Tree`.

9. Ile sekwencji białek człowieka posiada tę domenę?
10. Ile gatunków człowiekowatych (*Hominidae*) posiada tę domenę?

Otwórz zakładkę `HMM logo`.

11. Ile wynosi długość sekwencji domeny `PAZ`?
12. Wymień aminokwas najbardziej zachowane w 68 pozycji sekwencji domeny?

Przejdź do zakładki `Domain organization`.

13. Podaj najczęściej występujący układ domen w białkach (*architecture*), w którym występuje domena `PAZ`.

<br>

### Zad. 2 - Serwis PROSITE (wzorce i profile sekwencyjne)
> **PROSITE** charakteryzuje funkcję białka oraz jego rodziny stosując jeden wzorzec konsensusowy. Wzorce sekwencji konsensusowe pochodzą z konserwatywnych regionów przyrównań sekwencji białkowych i przedstawiane są w bazie PROSITE za pomocą wyrażeń regularnych. Informacje na temat funkcji tych wzorców pochodzą przede wszystkim z danych literaturowych. W celu przeszukania bazy badaną sekwencją, PROSITE stosuje dokładne skojarzenie z wzorcem. Poza wyrażeniami regularnymi, w celu ich dopełnienia, serwis PROSITE tworzy także profile.

Użyj sekwencji z zad. 1 i serwisu [PROSITE](https://prosite.expasy.org/prosite.html) w celu identyfikacji domen białkowych. Umieść sekwencję w polu `Quick Scan mode of ScanProsite`. Naciśnij przycisk `Scan`.

1. Podaj numer dostępu domeny `PAZ` w bazie PROSITE.
   > Numer dostępu zaczyna się od liter `PS`.
2. Czy lokalizacja domeny *PAZ* w sekwencji jest taka sama, jak w przewidywaniach Pfam?

#### Rekord domeny PAZ

Wejdź w rekord domeny PAZ w bazie PROSITE.

3. Podaj długość profilu domeny PAZ w bazie PROSITE (`Retrieve the sequence logo from the alignment`).
4. Wymień aminokwasy najbardziej zachowane na pozycjach 62 i 74?

<br><br>

### Zad. 3 - Metaserwis InterPro (integracja wyników)
> **InterPro** jest zintegrowaną bazą domen zaprojektowaną w celu ujednolicenia wielu baz domen i miejsc funkcjonalnych białek. InterPro łączy informacje z ponad 10 baz danych takich jak: PROSITE, Pfam. Program przetwarza wzorce sekwencji z tych baz danych. Uwzględnia jedynie te motywy oraz domeny sekwencji białkowych, które pokrywają się w kilku bazach. InterPro dopasowuje rekordy, wykorzystując kombinację wyrażeń regularnych, profili oraz ukrytych modeli Markowa. InterPro prezentuje wyniki w postaci graficznej, która podsumowuje dopasowania motywów oraz zawiera linki przekierowujące użytkownika do bardziej szczegółowych informacji na temat zidentyfikowanych domen.

Użyj sekwencji z zad. 1 i serwisu [InterPro](http://www.ebi.ac.uk/interpro/) w celu identyfikacji domen białkowych.

1. Podaj numer dostępu domeny `PAZ`.
   > Numer dostępu zaczyna się od liter `IPR`.
2. Podaj lokalizacaję domeny PAZ w sekwencji.
3. Podaj nazwę i numer dostepu InterPro nadrodziny, w skład której wchodzi domena PAZ (sekcja w wynikach przeszukiwania: *Homologous superfamily*).

#### Rekord domemy PAZ
Otwórz rekord domeny `PAZ` w bazie InterPro (`IPR003100`).

4. Wymień bazy domen, na podstawie których tworzony jest rekord domeny PAZ w bazie InterPro (*Contributing member database entries*).
5. W ilu sekwencjach białkowych domena PAZ jest dostępna (zakładka `Proteins`)?
6. Ile jest różnych układów domen (`Domain architectures`), w których występuje domena PAZ?
7. Czy domena PAZ występuje częściej u Eukaryota czy Prokaryota (zakładka `Species`)?
8. Ile jest znanych struktur przestrzennych białek zawierających domenę PAZ (zakładka `Structures`)?
9. Ile jest przewidzianych struktur przestrzennych białek z domeną PAZ (zakładka `AlphaFold`)?
10. Wymień trzy szlaki biochemiczne (`Pathways`), w które zaangażowana jest domena PAZ
<br><br>


## Python

### Zad. 4
Napisz skrypt, który zliczy występowanie każdej reszty (aminokwasu) w każdej kolumnie dopasowania sekwencji z pliku [profile.aln](http://www.combio.pl/files/profile.aln).

Output:

```python
{
  0: {'V': 14, 'L': 2, 'A': 1},          # np. V na pozycji 0 występuje 14 razy.
  1: {'D': 17},                          # D na pozycji 1 występuje 17 razy.
  2: {'F': 17},
  3: {'W': 5, 'S': 8, 'Y': 3, 'T': 1},
  4: {'A': 17},
  5: {'E': 4, 'P': 2, 'T': 8, 'V': 1, 'S': 1, 'D': 1}
}

```

### Zad. 5
Zmodyfikuj skrypt, aby zamiast zliczeń przedstawiał częstości aminokwasu w danej kolumnie (tj. zliczenie danego aminokwasu w kolumnie podzielone przez wielkość kolumny; suma częstości aminokwasów w danej kolumnie powinna być równa 1).

Output:

```python
{
    0: {'V': 0.8235294117647058,      # częstość = 14/17 = 0.8234
        'L': 0.11764705882352941,     # częstość = 2/17 =  0.1176
        'A': 0.058823529411764705},   # częstość = 1/17 = 0.0588
    1: {'D': 1.0},                    # częstość = 17.17 = 1
    2: {'F': 1.0},
    3: {'W': 0.29411764705882354,
        'S': 0.47058823529411764, 
        'Y': 0.17647058823529413,
        'T': 0.058823529411764705},
    4: {'A': 1.0},
    5: {'E': 0.23529411764705882,
        'P': 0.11764705882352941,
        'T': 0.47058823529411764,
        'V': 0.058823529411764705,
        'S': 0.058823529411764705,
        'D': 0.058823529411764705}
}
```

### Zad. 6
Zmodyfikuj poprzedni skrypt, aby zamiast częstości danego aminokwasu w danej kolumnie obliczał logarytm ilorazu szans. **Logarytm ilorazu szans** to logarytm u podstawie 2 ze stosunku częstości występowania danego aminokasu w danej kolumnie przez ogólną częstość występowania danego aminokwasu. Poniżej umieszczono ogólne częstości występowania aminokwasów w sekwencjach białkowych.

```python
# General amino-acid frequencies
AA = {
  'A': 0.082, 'Q': 0.039, 'L': 0.096, 'S': 0.066, 
  'R': 0.055, 'E': 0.067, 'K': 0.058, 'T': 0.053,
  'N': 0.040, 'G': 0.070, 'M': 0.024, 'W': 0.010,
  'D': 0.054, 'H': 0.022, 'F': 0.038, 'Y': 0.029,
  'C': 0.013, 'I': 0.059, 'P': 0.047, 'V': 0.068,
}
```

Output:

```python
{
    0: {'V': 3.598213524219012,     # log2(0.823529/0.068) = 3.5982
        'L': 0.2933589426905913,    # log2(0.117647/0.096) = 0.2934
        'A': -0.4792305612063362},  # log2(0.058823/0.082) = -0.4792
    1: {'D': 4.210896782498619},
    2: {'F': 4.717856771218502},
    3: {'W': 4.878321443411748,
        'S': 2.833927324053294,
        'Y': 2.605302949005332,
        'T': 0.15040098884854838},
    4: {'A': 3.6082322800440036},
    5: {'E': 1.8122322529539752,
        'P': 1.3237325917341103,
        'T': 3.1504009888485482,
        'V': -0.2091413978385919,
        'S': -0.16607267594670586,
        'D': 0.12343394124827907}
}
```

Dodatnia wartość logarytmu ilorazu szans oznacza, że dany aminokwas występuje częściej w danej kolumnie przyrównania (pozycji) niż wynikałoby to z przypadku (tj. z ogólnej częstości jego występowania). Natomiast ujemne wartości oznaczają, że dany aminokwas występuje rzadziej w danej pozycji niż wynikałoby to z przypadku. W ten sposób uzyskaliśmy profil PSSM (*Position-specific scoring matrix*), który określa wartość punktacji danego aminokwasu na danej pozycji przyrównania. Jeżeli jakiś aminokwas nie występuje w uzyskanym profilu to możemy nadać mu bardzo niską wartość punktacji, np. `-10`. Dzięki temu możemy obliczyć wartość punktacji dowolnej sekwencji 6 aminokwasów. Na przykład, sekwencja `LCFSAT` uzyska wartość punktacji `0.29 + (-10) + 4.72 + 2.83 + 3.61 + 3.15 = 4.6`.


### Zad. 7 (dla chętnych)
W pliku [seqs_pssm.fasta](http://www.combio.pl/files/seqs_pssm.fasta) znajduje się 30 sekwencji białkowych. Utwórzy skrypt, który wykorzysta profil utworzony w poprzednim zadaniu i znajdzie w każdej z 30 sekwencji najwyżej punktowany fragment 6-aminokwasowy podając jego wartość punktacji oraz lokalizację w sekwencji.

Output:

```
#seqid                  motif   score    start  end
sp|O13735|FAT1_SCHPO    LDFYAT  18.586   930    935
sp|O13821|VPS27_SCHPO   VVFSDT  -5.700   543    548
sp|O13926|YF66_SCHPO    VVFTIT  -8.383    25     30
sp|O13941|YEPB_SCHPO    LVFSDE  -10.343  240    245
...
```

```