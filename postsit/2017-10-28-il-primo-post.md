---
permalink: /it/blog/:year/:month/:day/:title
title: Come installare Mac OS X su un normale PC
layout: default
date: 2017/11/01
---
Arieccomi! Questo sarà il mio decimo sito, e, come ormai è per me tradizione, il primo post sarà proprio ”Come installare Mac OS X 10.6.2 Hazard su PC”! <!-- more -->
Ho scritto questa guida completamente a memoria, quindi chiedo perdono per eventuali mancanze.

### Occorrente:

*   Un computer con processore Intel
*   La DMG di Mac OS X by Hazard [Quick Search: [Mac OS X Hazard 10.6.2 ISO](https://www.google.it/search?q=mac+os+x+10.6.2+by+hazard+iso)]
*   A seconda del procedimento, CDBurnerXP e un DVD vuoto
*   A seconda del procedimento, VirtualBox
*   Tanta, tantissima pazienza ;)

<div>

#### Procedimento 1:

</div>

Questo procedimento si basa sulla masterizzazione dell’ISO su un DVD vuoto per l’installazione del sistema sull’hard disk. È il più rischioso, in quanto potrebbe portare alla perdita dei dati. Per prima cosa bisogna scaricare la DMG di Hazard. Ci sta mettendo tanto? Hehehe! Per un file di circa 5GB mi sembra più che normale no? Comunque, una volta ottenuta la DMG dell’OS bisogna convertirla con un fantastico programma chiamato "DMGtoISO" o una cosa del genere. Una volta convertita, la ISO va masterizzata con CDBurnerXP.
Per cui, apriamo il programma, doppio click su <span style="font-weight: bold;">Masterizza immagine ISO</span><span style="font-variant-ligatures: no-common-ligatures;">, cliccare su</span> <span style="font-variant-ligatures: no-common-ligatures; font-weight: bold;">Sfoglia...</span><span style="font-variant-ligatures: no-common-ligatures;">,</span> <span style="font-variant-ligatures: no-common-ligatures; font-weight: bold;">selezionare la ISO di Hazard appena creata</span><span style="font-variant-ligatures: no-common-ligatures;">, poco più in basso selezionare l'</span><span style="font-variant-ligatures: no-common-ligatures; font-weight: bold;">unità del DVD e la velocità <u>x2</u></span><span style="font-variant-ligatures: no-common-ligatures;">, masterizzare, aspettare una mezz'ora che masterizza, dare l'ok e spegnere il pc.</span>
<span style="font-family: inherit;"><span style="font-variant-ligatures: no-common-ligatures;">Ora, il prossimo passo è un po’ più complicato: bisogna fare in modo che il PC parta dal disco. Da qualche parte forse c’è scritto il tasto che porta alla selezione del disco di avvio del BIOS (basic input-output system). Comunque sia, dovreste arrivare alla selezione del disco di avvio. Ovviamente, noi vogliamo installare winzozz, quindi lo scegliamo... no dai scherzo! Scegliamo il disco appena masterizzato e aspettiamo che la 1ª schermata di configurazione (quella della lingua) venga a noi. Selezioniamo Lingua Italiana, o </span></span>⌘+I (comando(che dovrebbe essere il tasto “menu contestuale”) + I)e successivamente dalla barra dei menu scegliamo Utility > Utility Disco. Scegliete e formattate in Mac OS Esteso (journaled) il disco che poi sarà quello d’installazione. Fatto? Perfetto! Ora accettiamo tutto e andiamo avanti fino a che non compare la schermata selezione disco di installazione e <u style="font-style: italic; font-weight: bold;">NON CLICCARE SU INSTALLA!!</u> Piuttosto clicca quel rotondo pulsante chiamato “Personalizza...” e seleziona i kext (driver) compatibili con il tuo pc. Purtroppo questa è una fase delicata e io non ti posso aiutare... Fai una rapida ricerca Google oppure fai un po’ di trial and error. Quello su cui ti posso aiutare è, però, quando hai finito, che devi selezionare il disco formattato in precedenza.
La barra va, giusto? OK. Ha finito? Benissimo!
Quando riavvii il pc potrai usare quasi appieno il nuovo(?) sistema. Perché «quasi»? Perché è sicuro che una funzionalità, appunto, non funzioni. Ad esempio, potresti dover usare una connessione cablata perché non funziona il WiFi. Su tonymacx ci sono dei pacchetti di kext (driver) proprio per questo. Ma ciò non rientra nello scopo della guida.

#### Procedimento 2:

<div>Questo secondo procedimento è meno complicato e più sicuro del primo, perché verrà fatto sulla Sandbox di VirtualBox. I primi passi son gli stessi, quindi: «…_Per prima cosa bisogna scaricare la DMG di Hazard. Ci sta mettendo tanto? Hehehe! Per un file di circa 5GB mi sembra più che normale no? Comunque, una volta ottenuta la DMG dell’OS bisogna convertirla con un fantastico programma chiamato "DMGtoISO" o una cosa del genere_…» — Autoquote 😉</div>

<div>Apriamo VirtualBox e creiamo la macchina virtuale con le seguenti impostazioni:

*   Tipo: Mac OS X > Snow Leopard (32 bit)
*   RAM: **almeno** 1024 MB (è importante!)
*   Disco *.VBI con almeno 30 GB

</div>

Andiamo nelle impostazioni della macchina virtuale appena creata e come disco di avvio selezioniamo la ISO convertita in precedenza; avviamo la macchina virtuale. Il resto è uguale: «…_<span style="font-family: inherit;">aspettiamo che la 1ª schermata di configurazione (quella della lingua) venga a noi. Selezioniamo Lingua Italiana, o </span>⌘+I (comando(che dovrebbe essere il tasto “menu contestuale”) + I)e successivamente dalla barra dei menu scegliamo Utility > Utility Disco. Scegliete e formattate in Mac OS Esteso (journaled) il disco che poi sarà quello d’installazione._
_Fatto? Perfetto! Ora accettiamo tutto e andiamo avanti fino a che non compare la schermata selezione disco di installazione e <u style="font-weight: bold;">NON CLICCARE SU INSTALLA!!</u> Piuttosto clicca quel rotondo pulsante chiamato “Personalizza...” e seleziona i kext (driver) compatibili con il tuo pc. Purtroppo questa è una fase delicata e io non ti posso aiutare... Fai una rapida ricerca Google oppure fai un po’ di trial and error. Quello su cui ti posso aiutare è, però, quando hai finito, che devi selezionare il disco formattato in precedenza._
_La barra va, giusto? OK. Ha finito? Benissimo!_
_Quando riavvii il pc potrai usare quasi appieno il nuovo(?) sistema. Perché «quasi»? Perché è sicuro che una funzionalità, appunto, non funzioni. Ad esempio, potresti dover usare una connessione cablata perché non funziona il WiFi. Su tonymacx ci sono dei pacchetti di kext (driver) proprio per questo. Ma ciò non rientra nello scopo della guida._» — Autoquote 😉
