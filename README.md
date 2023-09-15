# Projekat iz mašinskog učenja
## Klasifikacija karcinoma dojke na osnovu slika uzoraka od pacijenata
Ovaj projekat kreira model konvolutivnih neuronskih mreža koji na osnovu velikog broja slika uzoraka karcinoma dojke, deli podatke u dve klase (0 - no IDC, 1 - yes IDC). IDC je invazivni duktalni karcinom koji je najčešći oblik raka dojke. Projekat se sastoji od dva pristupa kreiranja modela. Prvi prati ideju ansambla, zasnovanu na postupno implementiranoj prostoj agregaciji (Bagging), a drugi model koristi težinu instanci. Ova dva pristupa su korišćena zarad rešavanja problema nebalansiranosti podataka koji je u ovim podacima prisutan.

## Skup podataka
Za izradu projekta korišćen je skup podataka [Breast Histopathology Images](https://www.kaggle.com/paultimothymooney/breast-histopathology-images). Podaci su inicijalno organizovani u foldere po id-u pacijenta i dalje podeljeni u foldere prema klasama. Za potrebe projekta uzet je podskup pacijenata čiji podaci su korišćeni. Ukupno je korišćeno 24607 slika, dimenzije 50x50 u tri kanala.

## Inicijalna obrada podataka

Prva Jupyter sveska obuhvata obradu ulaznih podataka tako što podatke od svih izabranih pacijenata razvrstava u dve kolekcije slika koje se čuvaju u .npy fajlovima kao višedimenzioni nizovi. 

Pomenuti, već obrađeni podaci iz .npy fajlova, mogu se preuzeti preko sledećih linkova i koristiti kao gotovi, bez pokretanja prve Jupyter sveske.
[data0](https://drive.google.com/file/d/1mc1_XFbaJyuUjT-mPsOyd54YlEBIK79q/view?usp=sharing)
[data1](https://drive.google.com/file/d/1mv6BlBmcrJQ_713DvHKa_bQWVvHjzVen/view?usp=sharing)


## Modeli

Oba modela koriste arhitekturu konvolutivnih neuronskih mreža, sa istim brojem, redosledom i parametrima slojeva. Cilj je bio pronaći bolji model u zavisnosti od pristupa rešavanju problema, a ne u zavisnosti od arhitekture konvolutivne neuronske mreže.

## Instalacija
Sve korišćene biblioteke u kodu se mogu instalirati kroz komandnu liniju:
  ```
pip install [ime-biblioteke]
  ```
ili direktno iz Jupyter sveske

```
!pip install [ime-biblioteke]
```

##  Autor projekta
- Svetlana Bićanin
