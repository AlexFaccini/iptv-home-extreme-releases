# IPTV Home Extreme - release

Qui stanno solo gli APK firmati dell'app, uno per release. Il codice sorgente e' in un repo
privato: questo repo esiste perche' un APK allegato a una release privata si scarica solo con un
token, e un token dentro l'app e' un segreto che chiunque puo' estrarre.

L'app legge da se' `releases/latest`, confronta il tag con la versione installata e, se e' piu'
recente, scarica l'APK e chiede di installarlo.

- Tag: `vYYYY.MM.DD.NNN` (data di build + contatore giornaliero).
- Un solo `.apk` per release.
- Le prerelease e le bozze vengono ignorate dall'app.

Gli APK sono firmati con una chiave personale, non con quella di Google Play: al primo
installo Android chiedera' di consentire l'installazione da fonte sconosciuta.
