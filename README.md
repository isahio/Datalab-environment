# Datalab environment

Ga van de MWM2 wifi op de MWM2-Guest wifi!

Open een <b>Anaconda Prompt</b> terminal en typ:

<code>conda init bash</code>

Dit zorgt ervoor dat jouw terminal klaar is voor het runnen van de commands. Het beste is om de terminal nu af te sluiten en een nieuwe te openen zodat alles correct wordt uitgevoerd. 

Je kan de installatie verifiëren door te kijken of je terminal zoiets als (base) voor elke line heeft staan. 

Met de nieuwe terminal, run de commands zoals volgt: (BELANGRIJK: niet alles tegelijk maar stap voor stap!!)

<code>curl https://raw.githubusercontent.com/isahio/trial/main/environment.env?token=GHSAT0AAAAAACO2ABJBLVLURDOMCRF3ECYAZO6AKHA > environment.yml</code>

<code>conda install -n base conda-libmamba-solver</code>

<code>conda config --set solver libmamba</code>

<code>conda env create -f environment.yml</code>

<code>rm environment.yml</code>

Dit downloadt een beschrijving van welke bibliotheken gedownload en geinstalleerd moeten worden, en installeert de bibliotheken. Daarna verwijderd het de omschrijvingen. 

Nu, wanneer je een nieuwe terminal opent kan je het volgende command gebruiken om onze <i>Datalab</i> environment te gebruiken :)

<code>conda activate datalab</code>


Om de environment elke keer te gebruiken als je een nieuwe (Anaconda) terminal opent, doen we als volgt:

<code>echo 'conda activate datalag' >> ~/.bash_profile</code>

We moeten nu nog twee opdrachten uitvoeren, die ervoor zullen zorgen dat Python en sqlite naar behoren functioneren op Windows:

<code>echo "alias python='winpty python'" >> ~/.bash_profile</code>

<code>echo "alias sqlite3='winpty sqlite3'" >> ~/.bash_profile</code>

<code>echo "alias checkpy='winpty checkpy'" >> ~/.bash_profile</code>

Nu, herstart je terminal, en controleer of deze start in de <b>datalab</b> environment.
