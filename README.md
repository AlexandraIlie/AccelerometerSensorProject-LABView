# AccelerometerSensorProject-LABView

Obtinerea datelor de accelerometru de pe smartphone sau tableta folosind LabVIEW, UDPSensor si DataDashboard.
Acest proiect implica conectarea unui device Android si a unui laptop la aceeasi adresa IP, cu scopul obtinerii unor date in timp real cu privire la senzorii de accelerometru ai device-ului inteligent.
  	Pentru ca acest lucru sa fie posibil, am folosit urmatoarele medii de lucru:
•	un laptop conectat la internet, care are o versiune cat mai recenta de LabVIEW instalata;
Laboratorul de instrumente virtuale(LabVIEW): este o platforma de proiectare a sistemului si mediul de dezvoltare pentru un limbaj de programare vizuala de la National Instruments.
Limbajul grafic este denumit ‘G’; nu trebuie confundat cu codul G. Lansat intial pentru Apple Macintosh in 1986, LabVIEW este utilizat in mod obisnuit pentru achizitia de date, controlul instrumentelor si automatizarea industriala pe o varietate de sisteme de operare, inclusiv Microsoft Windows, diverse versiuni de Unix, Linux si macOS.
•	un device Android care sa aiba instalata aplicatia gratuita UDP Sensor app by Quadroid de pe Google Play. Aceasta aplicatie este necesara pentru a distribui datele de accelerometru pentru a putea fi citite in LabVIEW;
Senzorul UDP citeste valorile accelerometrului, giroscopului, barometrului si magnetometrului prin Android NDK. Aceste valori sunt trimise la adresa IP specificata si Port prin pachete UDP.
•	aplicatia DataDashboard by National Instruments instalata tot pe deviceul Android ce are ca scop tot afisarea datelor, dar pe telefon.
Data Dashboard permite crearea de vizualizari portabile personalizate ale aplicatiilor LabVIEW National Instruments. Folosind aceasta aplicatie, puteti crea tablouri pentru a afisa valorile variabilelor partajate publicate in retea si serviciile Web LabVIEW implementate pe indicatori, cum ar fi diagrame, casete de text si LED-uri.

