<strong><a href="https://github.com/DanRobo76/VMC-HELTY-FLOW/tree/main" >Versione Heavy</a></strong>

<!-- <img class="hidden-image" src="https://github.com/DanRobo76/VMC-HELTY-FLOW/assets/102819027/72d95647-d900-4fbc-acfa-6864b7f76321.png" alt="VMC"> -->

## VMC HELTY FLOW PLUS/ELITE LIGHT sviluppato per Home Assistant <a href="https://www.home-assistant.io/" target="_blank"><img src="https://user-images.githubusercontent.com/102819027/233830183-9c55677d-b6a1-4153-8d3c-219394ec8720.png" alt="immagine" style="width:10%;"></a> <a href="https://www.heltyair.com/prodotti/vmc-a-parete/flow-plus/" target="_blank"><img src="https://user-images.githubusercontent.com/102819027/233830311-1a5e8923-b991-46b1-84b0-f72198d5055d.png" alt="immagine" style="width:7%;"></a>
<pre style="font-size:10px; background-color: #d9ffcc;">
E-mail: <a href="mailto:danilo.robotti@gmail.com">danilo.robotti@gmail.com</a>
</pre>
<strong>Esonero di Responsabilità:</strong><br>
In nessun caso l'Ing. Danilo Robotti sarà responsabile di danneggiamenti diretti, indiretti, o conseguenti, correlati a difetti del presente SoftWare. 
Il Cliente ha l’onere e la responsabilità della scelta, dell’installazione, dell’uso e della gestione del SoftWare al fine del raggiungimento del risultato prefissatosi. 

#
![Immagine](https://github.com/DanRobo76/VMC-HELTY-FLOW-LIGHT/assets/102819027/f9c1db6b-9e9a-4015-965e-fb62277403f7)

<strong>Pre-Requisiti:</strong><br> 
<sub>- Installare <strong><a href="https://www.home-assistant.io/installation/">Home Assistant</a></strong>;</sub><br>
<sub>- Installare l'Add On [Facoltativo, ma Consigliato] <strong>File Edit</strong>, di Home Assistant;</sub><sub>   [Impostazioni->Componenti aggiuntivi->Raccolta di Componenti Aggiuntivi->File editor].</sub><br>
<sub>- Assicurarsi che la VMC venga visualizzata all'interni dell'APP <strong><a href="https://play.google.com/store/apps/details?id=com.helty.heltyair&hl=it&gl=US&pli=1">Air Guard</a></strong>; diversamente, impiegando la stessa, inserirla nell'infrastuttura di rete, prima di procedere.</sub><br>
#
<strong>Punti di Forza:</strong>
  - Invia Comandi da remoto alla VMC, leggendone i valori Contenuti;
  - Possibili Servizi da impiegare in un'Automazione:                                                                                    
    <img src="https://github.com/DanRobo76/VMC-HELTY-FLOW/assets/102819027/d63e3903-1a11-444c-9c1b-4ad4ebf1b365" alt="immagine" style="width:300%;"> 
 #
![image](https://user-images.githubusercontent.com/102819027/235299358-88373b06-b62e-4867-88ab-287cad60bb6d.png)<br>
<strong>1</strong> Rendere gli indirizzi IP della/e VMC, statici attraverso il Router; la VMC risponde sulla porta 5001. <br>
<strong>2</strong> Verificare se nel File configuration.yaml, contenuto all'interno della cartella "config", è presente il seguente Codice all'inizio: <br>

<pre style="font-size:10px; background-color: #d9ffcc;">
  homeassistant:
    packages: !include_dir_named packages/
</pre>

  ![image](https://user-images.githubusercontent.com/102819027/235297601-64f027ab-5696-4a5c-aa36-c2bbbbcb5836.png)

  , diversamente inserirlo, salvare il File "configuration.yaml" e riavviare Home Assistant [Non usare il Riavvio Rapido]<BR>

<strong>3</strong> Verificare la presenza della cartella "packages" all'interno della cartella "config" del Server Home Assistant; se non è presente, creare l'intero  percorso ovvero: \\192.168.1.xxx\config\packages\vmc_helty_flow_light<BR>
 <strong>3.1</strong> all'interno del percorso \config\packages\vmc_helty_flow_light copiare i seguenti Files:<BR> 
  <pre style="font-size:10px; background-color: #d9ffcc;">
     - vmc_helty_flow_light_master_[data].yaml
     - Scheda Interfaccia vmc_helty_flow_light_master_[data]
  </pre>
 , presenti nella scheda "CODE" -> Download ZIP:<BR>

<img width="309" alt="Code" src="https://github.com/DanRobo76/VMC-HELTY-FLOW-LIGHT/assets/102819027/65eb9f70-14df-4daf-a338-a1a4b337ee83"><BR>

 
<strong>4</strong> in Home Assistant andare in Panoramica -> cliccare in alto a destra sui ... puntini -> Modifica plancia -> AGGIUNGI SCHEDA -> Manuale -> Selezionare tutto il Codice , cancellare tutto il codice e incollare il contenuto del file "Scheda Interfaccia vmc_helty_flow_light_master_[data].txt"<br>
<strong>5</strong> trovare e sostituire all'interno del file "vmc_helty_flow_light_master_[data].yaml" l'indirizzo IP, da 192.168.1.160 con l'indirizzo Ip, vedi (Punto <strong>1</strong>)  [Aprire in Home Assistant il Pannello "File editor", cliccare sull' icona "Cartellina", andare in "packages", andare in "vmc_helty_flow_light" e selezionare il file "vmc_helty_flow_light_master_[data].yaml", cliccare sull'icona "Lente" ovvero Cerca", inserire l'Indirizzo IP 192.168.1.160 nel campo "Search for" e il nuovo Indirizzo IP, (Punto <strong>1</strong>) nel campo "Replace", cliccare su "All" e successivamente salvare il file cliccando sull'icona "Dischetto"; riavviare Home Assistant. [Non usare il Riavvio Rapido]<br>
  
###   Se si hanno a disposizione più VMC, ripetere i punti sottostanti per ogni VMC:                      

<strong>6</strong> Copiare e Incollare i seguenti Files nella cartella \config\packages\vmc_helty_flow_light:
 <pre style="font-size:10px; background-color: #d9ffcc;">
    - vmc_helty_flow_light_master_[data].yaml
    - Scheda Interfaccia vmc_helty_flow_light_master_[data]
 </pre> 
<strong>7</strong> Rinominare i seguenti Files:
  <pre style="font-size:10px; background-color: #d9ffcc;">
    - da vmc_helty_flow_light_master_[data] - Copia.yaml a vmc_helty_flow_light_[nome]_[data].yaml (Es. vmc_helty_flow_light_sala_[data].yaml)
    - da Scheda Interfaccia vmc_helty_flow_light_master_[data] - Copia a Scheda Interfaccia vmc_helty_flow_light_[nome]_[data].txt (Es. Scheda Interfaccia vmc_helty_flow_light_sala_[data].txt)
  </pre> 
<strong>8</strong> Aprire in Home Assistant il Pannello "File editor", cliccare sull' icona "Cartellina", andare in "packages", andare in "vmc_helty_flow_light" e selezionare il file "vmc_helty_flow_light_[nome]_[data].yaml":<BR>
 - cliccare sull'icona "Lente" ovvero Cerca", inserire [master] nel campo "Search for" e inserire il nuovo [nome] nel campo "Replace", cliccare su "All" e successivamente salvare il file cliccando sull'icona "Dischetto"; <BR>
 - cliccare sull'icona "Lente" ovvero Cerca", trovare e inserire il [vecchio IP] nel campo "Search for" e inserire il nuovo [IP] nel campo "Replace", cliccare su "All" e successivamente salvare il file cliccando sull'icona "Dischetto"; <BR>
 - cliccare sull' icona "Cartellina", andare in "packages", andare in "vmc_helty_flow_light" e selezionare il file "Scheda Interfaccia vmc_helty_flow_light_[nome]_[data].txt":<BR>
 - cliccare sull'icona "Lente" ovvero Cerca", inserire [master] nel campo "Search for" e inserire il nuovo [nome] nel campo "Replace", cliccare su "All" e successivamente salvare il file cliccando sull'icona "Dischetto"; <BR>
 
<strong>9</strong> Riavviare Home Assistant [Non usare il Riavvio Rapido] <br>
<strong>10</strong> in Home Assistant andare in Panoramica -> cliccare in alto a destra sui ... puntini -> Modifica plancia -> AGGIUNGI SCHEDA -> Manuale -> Selezionare tutto il Codice , cancellare tutto il codice e incollare il contenuto del file "Scheda Interfaccia vmc_helty_flow_light_[nome]_[data].txt"<br>
#

#### Se il progetto ti è piaciuto <a href="https://www.paypal.com/donate/?business=YU9379GL8VDW4&amount=1.2&no_recurring=1&item_name=Se+il+progetto+ti+%C3%A8+piaciuto%2C++offrimi+un+GinSeng%21+%0A%3B%29&currency_code=EUR">Clicca Qui</a> per offrirmi un GinSeng! <a href="https://www.paypal.com/donate/?business=YU9379GL8VDW4&amount=1.2&no_recurring=1&item_name=Se+il+progetto+ti+%C3%A8+piaciuto%2C++offrimi+un+GinSeng%21+%0A%3B%29&currency_code=EUR"><img src="https://user-images.githubusercontent.com/102819027/233830035-709efa6b-94d7-4ea6-865b-76ab5c1eee6d.png" alt="immagine" style="width:3%;"></a>
<br>
oppure scansionare il seguente QR code:
<img src="https://github.com/DanRobo76/VMC-HELTY-FLOW/assets/102819027/81ba7208-fbad-4fab-8ceb-cdcf901fdb61.png" alt="immagine" style="width:20%;">
<br>
