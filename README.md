# Installare LineageOS su Samsung Galaxy Tab A6 (gtaxllte) con MicroG.
Guida completa per installare **LineageOS 19.1** sul Samsung Galaxy Tab A6 `(SM-T585)`.
>[!WARNING]
>Questa guida è stata fatta a scopo informativo, non mi assumo nessuna responsabilità nel caso il dispositivo si rompa o si danneggi permanentemente.

Ormai il Galaxy Tab A6 è un tablet datato, soffre di pesanti rallentamenti, Samsung ha completamente abbandonato il supporto alla sua versione Android, potresti non essere in grado di utilizzare le applicazioni più moderne. Installare un CustomOS come LineageOS sul tuo dispositivo ti permette di ottenere maggiori prestazioni, controllo, privacy e inoltre gli concedi una nuova vita. <br>
<br>
Il tablet è supportato da LineageOS solo in modo non ufficiale. Usando BitGApps, NikGApps o MindTheGApps per avere i servizi google, incapperete in degli errori. <br>
Seguendo questa guida risolverete tutti i problemi.

📥 Prima di procedere ecco tutto il necessario da scaricare:
| Nome | Link | Note |
| :--- | :--- | :--- |
| **Odin Tool** | [Download](https://odindownload.com/) | Versione 3.13.1 |
| **TWRP Recovery** | [Download](https://dl.twrp.me/gtaxllte/) | Ultima versione per SM-T585 |
| **LineageOS 19.1** | [Download](https://xdaforums.com/t/lineageos-19-1-for-sm-t580-gtaxlwifi-sm-t585-gtaxllte-sm-p580-gtanotexlwifi-and-sm-p585-gtanotexllte.4432957/page-95#post-89998855) | Per gtaxllte |
| **minMicroG** | [Download](https://github.com/friendlyneighborhoodshane/minmicrog_releases/releases) | Scaricate NoGoolag | <br>

**1. Inserire il TWRP dentro il dispositivo**
  - Andiamo su Impostazioni, Sistema e facciamo TAP su Numero Build fino a che compare con scritto "ora sei uno sviluppatore".
  - Vai in Opzioni Sviluppatore e attiva la voce Sblocco OEM e spegni il tablet.
  - Riaccendilo premendo contemporaneamente `Volume Giù + Home + Power`.
  - Ora premi `Volume Su` e sarai in **Download Mode**.
  - Apri **Odin** sul PC. Collega il tablet. Dovresti vedere un rettangolo azzurro `[ID:COM]`, se lo vedi significa che procede bene.
  - Clicca su **AP** e seleziona il file della TWRP (`.tar`).
  - Vai nella scheda **Options** di Odin e **togli la spunta** a "Auto Reboot". **(IMPORTANTE)**
  - Premi **Start** e appena compare la scritta verde **PASS** scollega il cavo.
  - Ora premi contemporanemanete `Volume Giù + Home + Power` ma appena lo schermo diventa nero sposta il dito su `Volume Su + Home + Power` e lascia appena si accende nel menu TWRP. <br>
  
    >Nel caso questo ultimo passo sia fallito e sei tornato alla normale schermata del Samsung, bisogna rifare il procedimento partendo dal punto 4, entra in Download Mode, Apri Odin e rimetti dentro il file .tar
    
**2. Pulizia (Wipe)**
  - Ora siamo dentro la TWRP, fai uno *swipe* a destra per entrare nel menu principale.
  - Vai su **Wipe** poi **Format Data** e digita `yes` per dare conferma.
  - Ora torniamo indietro con il pulsante indietro (◄) **(NON PREMERE SU REBOOT)**
  - Clicca su **Advanced Wipe**
  - Seleziona **solo** queste: `Dalvik / Art Cache`, `System`, `Data`, `Cache`.
  - Trascina verso destra per confermare. (Swipe to Wipe) e Torniamo indietro al menu principale della TWRP. <br>
  
**3. Installare LineageOS e MicroG**
  - Collega il tablet al PC tramite cavo (la TWRP lo riconoscerà come memoria esterna).
    > Non tutti i cavi sono adatti alla trasmissione dati, alcuni sono costruiti solo per caricare il dispositivo, è necessario fare attenzione a scegliere il cavo giusto che possa fare entrambe le cose.
  - Copia i file `.zip` della **LineageOS** e di **microG** nella memoria interna.
    > È possibile inserire i file anche tramite MicroSD, in questo caso, copiarli sulla microSD e poi inserirla dentro il tablet.
  - Sul tablet, vai su **Install**
  - Seleziona la zip del **LineageOS** e installa.
    > Se non vedi i file .zip appena messi, prova a riavviare dalle impostazioni della TRWP cliccando su Recovery, il dispositivo si riavvierà ma tornerà sul menu TWRP.
  - Torna indietro (◄) e installa lo zip di **microG**.
  - Ora puoi finalmente fare **Reboot System**. <br>
  
**4. Come abilitare i servizi Google con MicroG**<br>
*Ora finalmente abbiamo il nostro tablet con il nuovo customOS, per prima cosa dobbiamo abilitare i servizi Google.*
  - Apri l'app **Impostazioni microG**
  - Clicca su **Controllo dei problemi** e controlla che ci siano tutte le spunte, nel caso, premi e dai i permessi a microG.
  - Abilita **Registrazione del dispositivo**
  - Abilita **Messaggistica cloud**
  - Abilita **SafetyNet** <br>
  
**5. F-Droid e Aurora Store** <br>
*Per scaricare le applicazioni, inanzitutto scarichiamo F-Droid (abilitando il download di applicazioni esterne tramite browser).*
  - Aprire il broswer (Icona viola con una stellina bianca in mezzo), cercate **F-Droid**. deve essere [questo sito](https://f-droid.org/it/).
    > **F-Droid** ti permette di scaricare tantissime app open source, dacci un'occhiata!
  - Una volta scaricato, concedete i permessi di installare app esterne.
  - Aprite **F-droid** e cercate **Aurora Store**
  - Facendo tap su **Aurora Store** e scegliendo  modalità anonimo entrerete nell'app store. <br>


> [!NOTE]
> Per applicazioni Google non avrete problemi ma per Youtube ci sarà bisogno di ulteriori passaggi tramite Revanced. Lascio il link per chi fosse interessato [qui](https://revanced.app/). <br>

Ora avrete terminato l'installazione, godetevi il vostro dispositivo, più veloce, fluido e con mille possibilità open source! <br>

**Se vuoi tornare alla versione Android precedente o hai avuto errori.**<br>
Puoi invertire il procedimento facendo tornare il tablet nel suo stato originale di fabbrica.<br>
- Per farlo scarica da [qui](https://samfw.com/firmware/SM-T585) l'ultima versione del firmware ITV.
- Apri odin e collega il tablet in modalità **Download**.
- Inserisci i file **BL, AP, CP, CSC** nel corretto spazio.
- Premi Start.
- Fai terminare il tablet di scaricare e si riavvierà da solo. <br>

>[!TIP]
>Questo invertirà tutto, fallo anche nel caso la TWRP si blocchi o il tablet sembra non rispondere più ai comandi.

<br>
<details>
  <summary>📂 Visualizza Allegati Fotografici</summary>
  <br>
  
[Fronte](https://github.com/user-attachments/assets/64db537f-bc46-418e-882e-c17f2840ab39)<br>
[Retro](https://github.com/user-attachments/assets/379197c8-02f3-45d4-aad0-f6604dc6da11) <br>
[Info SO](https://github.com/user-attachments/assets/e0746a80-0084-4130-9b95-f879e4b26636)


</details>
