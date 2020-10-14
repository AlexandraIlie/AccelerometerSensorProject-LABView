# AccelerometerSensorProject-LABView

Obtinerea datelor de accelerometru de pe smartphone sau tableta folosind LabVIEW, UDPSensor si DataDashboard.
Acest proiect implica conectarea unui device Android si a unui laptop la aceeasi adresa IP, cu scopul obtinerii unor date in timp real cu privire la senzorii de accelerometru ai device-ului inteligent. Pentru ca acest lucru sa fie posibil, am folosit urmatoarele medii de lucru:
*	un laptop conectat la internet, care are o versiune cat mai recenta de LabVIEW instalata;
Laboratorul de instrumente virtuale(LabVIEW): este o platforma de proiectare a sistemului si mediul de dezvoltare pentru un limbaj de programare vizuala de la National Instruments.
Limbajul grafic este denumit ‘G’; nu trebuie confundat cu codul G. Lansat intial pentru Apple Macintosh in 1986, LabVIEW este utilizat in mod obisnuit pentru achizitia de date, controlul instrumentelor si automatizarea industriala pe o varietate de sisteme de operare, inclusiv Microsoft Windows, diverse versiuni de Unix, Linux si macOS.
*	un device Android care sa aiba instalata aplicatia gratuita UDP Sensor app by Quadroid de pe Google Play. Aceasta aplicatie este necesara pentru a distribui datele de accelerometru pentru a putea fi citite in LabVIEW;
Senzorul UDP citeste valorile accelerometrului, giroscopului, barometrului si magnetometrului prin Android NDK. Aceste valori sunt trimise la adresa IP specificata si Port prin pachete UDP.
*	aplicatia DataDashboard by National Instruments instalata tot pe deviceul Android ce are ca scop tot afisarea datelor, dar pe telefon.
Data Dashboard permite crearea de vizualizari portabile personalizate ale aplicatiilor LabVIEW National Instruments. Folosind aceasta aplicatie, puteti crea tablouri pentru a afisa valorile variabilelor partajate publicate in retea si serviciile Web LabVIEW implementate pe indicatori, cum ar fi diagrame, casete de text si LED-uri.

Ulterior, am imbunatatit proiectul prin introducerea unor filtre ce presupun netezirea datelor date de semnale si salvarea valorilor obtinute intr-un fixier de tip excel.

# UDPReceiver.vi:
[![dsada.jpg](https://i.postimg.cc/zvk8TFPm/dsada.jpg)](https://postimg.cc/XBXRbdbx)

# AquireShowSensorData.vi FrontPanel:
[![Aquire-Show-Sensor-Data-vi-front-Panel.jpg](https://i.postimg.cc/hPkRhwGJ/Aquire-Show-Sensor-Data-vi-front-Panel.jpg)](https://postimg.cc/4mQSSWVZ)

# DataDashboard:
[![Data-Dashboard.jpg](https://i.postimg.cc/nLQkrRCL/Data-Dashboard.jpg)](https://postimg.cc/Lq2f0Vkd)

# FilteringSignals.vi:
[![Filtering-Signals.jpg](https://i.postimg.cc/DZLXkRmq/Filtering-Signals.jpg)](https://postimg.cc/474dpL6d)

# Testarea Aplicatiei
1.	Pentru testarea acestei aplicatii, trebuie mai intai sa oprim Windows Firewall cu scopul de a activa conexiunile primite de la server (Control Panel\System and Security\Windows Defender Firewall\Customize Settings).
2.	Urmatorul pas este reprezentat de determinarea IP-ului. Pentru aceasta, intram in cmd si tastam ipconfig. Adresa IP corecta este cea denumita Ipv4 Adress.
3.	Se introduc adressa IP si portul in aplicatia UDP Sensor(se apasa ON), cat si in LabView;
4.	Cand toate intrarile sunt completate si aplicatia senzor UDP ruleaza, se apasa butonul de Executie din panoul frontal. Aceasta va porni aplicatia LabView. Ca rezultat, ar trebui sa vedem datele senzorului, care arata acceleratiile pe cele trei axe X, Y si Z;
5.	Pentru DataDashboard, se verifica daca toate variabilele sunt conectate si se apasa butonul de run. 



