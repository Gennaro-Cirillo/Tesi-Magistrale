# Tesi-Magistrale
FIM and FIM like method for eikonal equation and ray-tracing

I codici sono stati stilati su Google Colab, quindi su dei notebook Jupyter. 
Per tale motivo ogni file è autoreferenziale, ovvero non chiama funzioni o usa variabili provenienti da altri file. Questo significa anche che nei diversi codici appaiono spesso le stesse funzioni ricopiate, ma non c'era altro modo se non quello di passare per il Drive (cosa che ho cercato di evitare).

I codici sono divisi in cartelle e nominati opportunamente, di seguito lascio una breve descrizione di cosa c'è nelle cartelle:

Nella cartella Eikonal_method ci sono i metodi del FIM e del FIM senza lista (FIM-Jacobi) implementati sia per CPU che per GPU tramite CuPy e RawKernel, sui casi del labirinto ad S e della lente di Luneburg. Il metodo FIM è quello nominato con FIM_v2 (versione 2), mentre quello senza lista è nominato come FIM_v3 (versione 3). Il FIM_v1 (versione 1) potete anche anche non considerarlo in quanto era la prima versione che ho mezzo inventato io ed implementato quando ancora non avevo capito bene le cose. Inoltre non è vettorializzata e per tale motivo di questa versione 1 c’è solo l’implementazione CPU e non sarà utilizzata per fare il ray-tracing. 


Nella cartella Eikonal_method + RayTracing ci sono le prove dei codici che, una volta calcolata l’Iconale (nei codici l’ho chiamata T) con i metodi implementati nella cartella Eikonal_method vanno a tracciare il raggio. Le sottocartelle sono divise in base all’ordine della Godunov e degli algoritmi di interpolazione. Ognuno di questi codici gira su CPU e lavora sul dominio labirintico ad S, per simulazioni su altri domini vedere la sottocartella “Altre Simulazioni”.
I codici dovrebbero essere tutti funzionati, ma ci sono un paio di blocchi di codice che sono invece delle prove.
P.S. => in queste cartelle la versione la v1 è indicativa del FIM normale mentre la v2 è identificativa del FIM senza lista 


Nella cartella Implementazioni Finali ci sono sia il Gold Standard che i codici in cui vengono parallelizzato i fasci di raggi.
In particolare, la cartella sui fasci di raggi in parallelo sono riportate le prove sul come portare su GPU un fascio di raggi, mentre nel file Gold Standard sono riportate le simulazione sui casi più complessi e estesi, tutti eseguiti completamente su GPU (sia calcolo Iconale che raggi).
