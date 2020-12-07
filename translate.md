# Istruzioni per traduttori


Risorse | Link
--------|:----:
Obbligatorie | [[Linee guida]](https://drive.google.com/file/d/1IACZxWdk84rs81ElQ9OWws-aroQZDtxZ/view?usp=sharing)
Consigliate | [[Telegram Web]](https://web.telegram.org), [[Telegram Desktop]](https://desktop.telegram.org/)


## Setup/Overview

Per poter contribuire alla traduzione, dopo aver letto le [linee
guida](https://drive.google.com/file/d/1IACZxWdk84rs81ElQ9OWws-aroQZDtxZ/view?usp=sharing)
occorre:

1. creare (gratuitamente) un account su
   [GitHub](https://www.github.com) ("Sign Up" e seguire la procedura
   sino a verificare la mail);
   
2. comunicarmi lo username GitHub con cui intendete collaborare, per
   [abilitazione](data/users.csv). 

	Verrà risposto un nome file di prova: tradurlo e sottomettere la
	revisione, *come illustrato nel seguito* (occorre leggere fino a
	fine pagina per saper cosa/come fare).
	
	Una volta fatto, se ci si sente ragionevolmente a proprio agio con
    la procedura di modifica/sottomissione si può passare allo step
    successivo, alternativamente si può chiedere
	
	```
	@lucailgarb #sandbox
	```
	per la predisposizione di un altro file di prova;

3. per richiedere l'assegnazione di uno spezzone di sottotitoli postare:
   
	```
	@lucailgarb #translate
	```


## Il file su cui lavoriamo per la traduzione

Il file su cui dobbiamo operare è stato generato (verosimilmente) dal
software speech-to-text di Google/YT, a partire dal video originale.

Per quanto riguarda il riconoscimento delle parole (soprattutto in
inglese e quando l'audio è chiaro) oramai questi software fanno
abbastanza "paura"; quello che ancora fanno fatica a capire sono i
toni (es quindi fanno fatica a capire le domande, la punteggiatura
ecc). 

Ma qui entrate in gioco voi e l'imprescindibilità, quando si andrà a
tradurre e preparare i subs, di *ascoltare/guardare* il video.


### Formato sottotitoli 

Informaticamente i sottotitoli si trovano in un file `.srt` ossia un
file di testo (tipo `.txt`) con una struttura precisa, da
rispettare/non modificare.

Ad esempio, di seguito uno stralcio per i primi secondi del video che
usiamo ai cubi:

```
1
00:00:00,000 --> 00:00:01,200
Prodotti caseari

2
00:00:02,000 --> 00:00:24,000
Inseminazione forzata

3
00:00:33,000 --> 00:00:49,000
Separazione dei neonati

4
00:00:51,000 --> 00:01:04,000
Questa è una pratica standard
```

Per ogni sottotitolo vi è dunque:
* un numero progressivo;
* i secondi di inizio e fine della sua visualizzazione;
* il testo (che può essere organizzato su più righe);
* una linea bianca di separazione.

Questo file (tradotto in italiano) è quello a cui dobbiamo, *alla fine
di tutto*, arrivare.


### Come/cosa modificare

Per permettere la **revisione** delle traduzioni, i traduttori
lavorano su un file *lievemente diverso*, che includa sia l'originale
che la traduzione. Uno stralcio/esempio del file che otterrete:

```
3
00:00:33,000 --> 00:00:49,000
## Newborn separation



4
00:00:51,000 --> 00:01:04,000
## This is standard practice



```

Quello che dovrete fare è la cosa seguente:
* lasciare **tutto immutato**;
* **aggiungere la/e linea/e tradotta/e** in italiano sotto a quella inglese;
* **lasciare almeno una linea di spazio** alla fine.

Come segue:
```
3
00:00:33,000 --> 00:00:49,000
## Newborn separation
Separazione dei neonati



4
00:00:51,000 --> 00:01:04,000
## This is standard practice
Questa è pratica standard



```


## Il processo step-by-step

Per lavorare alle traduzioni:

0. da **computer**, effettuare il login su [GitHub](https://www.github.com);

1. aprire [questa](https://github.com/lbraglia/av_it_subs) pagina, dove sono
   conservate le traduzioni;

2. nel gruppo Telegram "AV: Traduzioni e Sub YouTube" postare:

	```
	@lucailgarb #translate
	```
	Per richiedere l'assegnazione di un file da tradurre.
	Verrà risposto (quanto prima) un messaggio con la posizione del 
	file, del tipo:
	
	```
	subs/hnva2/subs_012000_lbraglia.srt
	```
	che sta a significare: ti è stato assegnato
	
	* il file `subs_012000_lbraglia.srt` (uno
	spezzone di sottotitoli che inizia approssimativamente a
	`01:20:00` nel video) 
	* che si trova nella cartella `hnva2` (che contiene i sottotitoli
	per "Holding Non-Vegans Accountable 2.0") 
	* posta nella cartella `subs` (che racchiude tutti i
	sottotitoli di tutti i video).

3. cliccare quindi sulla cartella `subs`
   
   ![subs dir](img/subs_dir.png)

4. cliccare sulla cartella del video (`hnva2` nell'esempio)

	![hnva2 dir](img/hnva2_dir.png)

5. arrivati a questo punto conviene **salvare questa pagina nei
   preferiti** (per accedervi facilmente alle prossime sessioni)
   perché tutte i file di un dato video si trovano qui e si
   velocizzerà l'accesso al file assegnato.

   Cliccare dunque sul nome del file che ci è stato assegnato
   (`subs_012000_lbraglia.srt` nell'esempio);

   ![subs file_select](img/subs_file_select.png)

6. ora **visionare il lavoro da fare nel suo complesso**, seguendo [le
   istruzioni riportate qui sotto](translate.md#il-workflow-da-adottare);

7. **una volta chiara la traduzione da effettuare nel suo complesso**,
   puoi cliccare sul pulsante matita per procedere alla modifica del
   file (quello a destra dei bottoni `Raw` e `Blame`);

   ![pencil](img/pencil.png)

8. fare le modifiche/tradurre (non preoccuparsi del messaggio "You are
   making changes ...")
   
   ![editing](img/editing.png)

   Se si vuole avere un sommario delle modifiche effettuate spostarsi
   nel tab `Preview changes`;

9. a termine sessione, quando si vuole "salvare", scorrere in basso
   nella pagina, verso la sezione `Propose changes`: cliccare sul
   tasto verde `Propose changes`

	![propose_changes](img/propose_changes.png)

10. cliccare sul pulsante verde `Create Pull Request`
   
   ![pull_request1](img/pull_request1.png)

11. cliccare su `Create Pull Request`;

	![pull_request2](img/pull_request2.png)

12. fine!! 


In seguito a revisione informatica di minima le modifiche saranno
accettate ed integrate: modifiche che impattino su qualsiasi cosa
diversa dalla traduzione (es progressivo sottotitolo, secondi)
saranno verosimilmente rifiutate.
	
Ora, se si è **terminato** il proprio file:
* attendere accettazione/merge (comunicata automaticamente via mail);
* *dare comunicazione* in chat che la modifica del file assegnato è
  completa (per motivi logistici, aka "sbloccare" la revisione). 
  
  Il modo migliore per farlo è rispondere all'assegnazione (per
  trovarla *cercare il proprio username GitHub* nella chat) con un
  messaggio del tipo "completato"/"terminato". Es

	![trn_completa](img/translate_completa.jpg)
 
  
* si può procedere a richiesta di un nuovo file da modificare, re-iniziando
  dal punto 2.

Se viceversa **occorre finire** il file assegnato, ri-cominciare dal
punto 7 (tener conto che le modifiche in precedenza apportate non
saranno visualizzate, se non sono state nel frattempo
approvate. Tuttavia sono state sottomesse/non perse).


## Il workflow da adottare

Nell'attività di traduzione **il modo peggiore di procedere**, **da
non adottare**, consiste nel partire a testa bassa con la modifica
dei subs su GitHub, procedendo un sub alla volta, e non ascoltando il
video.

**Quello che viceversa si consiglia caldamente di fare è:**

* puntare il proprio browser all'url riportato a inizio file; questo è
  il link all'inizio dello spezzone di propria competenza:

  ![url inizio file](img/url_inizio_file.png)

* può essere davvero molto utile **stampare** (su carta riciclata) i
  sottotitoli, per poter avere un supporto utile per
  appunti/annotazioni ecc;
  
* **riascoltare più volte** l'audio, **scorrendo visivamente i sottotitoli**
  in contemporanea. Si consiglia di ascoltare anche un pezzo di video
  precedente e uno susseguente, per contesto;

* iniziare ad **abbozzare** punteggiatura, traduzione, e ad evidenziare
  *dubbi*;

* non esitare a **domandare/condividere eventuali dubbi** nella chat "AV:
  Traduttori e Revisori".  Alcuni suggerimenti su come farlo sono forniti
  nel seguito;

* una volta che abbiamo una idea compiuta della traduzione da
  effettuare *nella sua interezza* e abbiamo risolto eventuali dubbi,
  possiamo **procedere alla modifica** dei file;

* durante la modifica è possibile **lasciare una nota per i revisori**
  ponendola dopo *1 cancelletto*, come *ultima linea* e assicurandosi che dopo
  vi sia sempre una *linea vuota* di separazione. Ad esempio:

	```
	3
	00:00:33,000 --> 00:00:49,000
	## Linea 1 in inglese
	## Linea 2 in inglese
	Testo tradotto
	testo tradotto
	# REVISORI: qui nel dubbio si è optato per XYZ perché ...

	4
	...
	```