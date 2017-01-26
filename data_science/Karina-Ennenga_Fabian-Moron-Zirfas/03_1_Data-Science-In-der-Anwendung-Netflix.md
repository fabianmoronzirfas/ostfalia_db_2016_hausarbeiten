## 3.1 Netflix 

TBD  


## 3.1.1 Datenerhebung

Netflix weiß von jedem Nutzer, was er schaut, wann er schaut, wie lange er etwas schaut, an welcher Stelle aufgehört wurde, zu schauen und wie er auf den Film oder die Serie aufmerksam geworden ist.

Diese riesige Menge an Daten wird von Algorithmen beobachtet. Laut dem amerikanischen Magazin The Atlantic beschäftigt Netflix allein 800 Ingenieure, die sich nur mit diesem Algorithmus beschäftigen.

The Atlantic hat recherchiert, wie die Algorithmen funktionieren. Auf die Funktionsweise des Algorithmus gehe ich im nächsten Abschnitt *Speicherung / Algorithmus* näher ein.

Das Herzstück von Netflix ist sein Empfehlungsmechanismus. Dieser basiert auf dem Algorithmus, der CineMatch genannt wird. Um diesen Mechanismus noch weiter zu verbessern, wurde 2006 von Netflix-Chef Reed Hastings ein Wettbewerb “The Netflix Prize” zur Verbesserung des Algorithmus, ausgeschrieben. Er versprach demjenigen, der es schaffen würde, den Algorithmus um 10 Prozent zu verbessern, 1 Million Dollar. (http://techblog.netflix.com/2012/04/netflix-recommendations-beyond-5-stars.html)

Letztendlich gewann ein Team, das eine Verbesserung von 8,43% geschafft hat. Das Team habe 2000 Stunden Arbeit damit verbracht, um einen Kombination aus 107 Algorithmen zu präsentieren.
Um den Algorithmus einsetzen zu können, mussten einige Anpassungen vorgenommen werden. So konnte beispielweise der ursprüngliche Algorithmus nicht mehr als 100 Millionen Bewertungen händeln, wobei zu dem Zeitpunkt bereits 5 Milliarden Bewertungen vorhanden waren.
In 2012 wurden bereits 75% der Filme und Serien aufgrund des Empfehlungssystems geschaut.


## 3.1.2 Speicherung / Algorithmus

In Anbetracht der Tatsache, dass Netflix mehr als 85 Millionen Abonnenten hat (Stand von Oktober 2016 laut http://www.wiwo.de/unternehmen/it/netflix-in-deutschland-mehr-abonnenten-als-einwohner/14702184.html), wird klar, dass sie ein riesiges Repertoire an “personalisierten Genres” haben.

In dem Artikel *How Netflix Reverse Engineered Hollywood* vom 02.01.2014 beschreibt das Magazin *The Atlantic* ihre Recherchearbeiten zum Algorithmus von Netflix.
Sie haben herausgefunden, dass Netflix zu diesem Zeitpunkt 76.897 Genres besitzt, um Filmtypen zu beschreiben. Zum heutigen Zeitpunkt sind es fast 93.000 (https://docs.google.com/spreadsheets/d/1eISFvq42Sll10xekyV-XQdwoG7_gjZpreNG40Pz8G0k/edit#gid=2125244376).

Zu den neuesten zählen Genres wie “Golden Globe Award-winning Understated Comedies” und “Critically-acclaimed Biographical Drug Documentaries”.

*The Atlantic* hat herausgefunden, dass Netflix jeden einzelnen denkbaren Film und jede Serie analysiert hat und sich somit eine enorme Datenbasis aufgebaut hat.
Dies gelang Ihnen, indem sie Menschen engagiert haben, die Filme schauen und diese mit unterschiedlichsten Metadaten beschreiben. Dazu gehören der Romantiklevel, wie blutrünstig ein Film ist und erzählerische Daten, wie zum Beispiel die Schlüssigkeit der Handlung.
Die ausgebildeten Filmeschauer bewerten dutzende von Eigenschaften, darunter auch den Moralstatus der Charaktere. Diese Eigenschaften werden mit den Gewohnheiten der Netflix User kombiniert, woraus ein großer Wettbewerbsvorteil für Netflix entsteht.


![adjectives](./images/adjectives.png)  

Durch den Alghorithmus hat Netflix eine neue Form des Empfehlens geschaffen.

### 3.1.2.1 Kollaboratives Filtern
http://inka.htw-berlin.de/Sieck/Abschlussarbeiten/Hebeisen.pdf

Die am häufigsten verbreitete Filtermethode für Empfehlungssysteme ist heutzutage das kollaborative Filtern. Ein kollaboratives System ist ein lernendes System, welches eine vorhandene Datenbasis nutzt. Anhand dieser Datenbasis sollen Verhaltensmuster von Nutzereingaben zu erkennen sein und es soll versucht werden, eine Verbindung zwischen eingegebenen und bereits vorhandenen Daten herzustellen (User-to-User). Es werden also Empfehlungen auf Basis von Bewertungen anderer Nutzer gegeben. Das Interessenprofil eines Nutzers soll auf das Interessenprofil eines anderen Nutzers übertragen werden. Bewertungen erfolgen hierbei entweder durch konkrete Bewertungen einer bestimmten Sache (zum Beispiel eines Filmes), indem beispielsweise anhand einer Skala ein Rating abgegeben wird oder angegeben wird, ob etwas nützlich war, oder aber auch durch das implizite Verhalten des Nutzers. Hierbei wird zum Beispiel berückstichtigt, wie lange ein Nutzer etwas angeschaut hat oder was angeschaut wurde.
Beim kollaborativen Filtern wird davon ausgegangen, dass man ein statistischer Nachbar ist, wenn man ähnliche Bewertungen abgegeben hat und dass etwas für einen Nutzer relevant oder interessant ist, wenn es auch für den statistischen Nachbarn interessant war.
Wenn Anna zum Beispiel Film 1 mit 3 Sternen, Film 3 mit 4 Sternen und Film 5 mit 2 Sternen bewertet hat und Julia Film 1 mit 2 Sternen, Film 3 mit 5 Sternen, Film 4 mit 4 Sternen und Film 5 mit 1 Stern bewertet hat, dann scheinen die beiden Benutzer Anna und Julia ähnlich zu sein. Anna kann also nach der kollaborativen Filtertechnik der Film 4 vorgeschlagen werden, den sie ja noch nicht gesehen hat, da ihre statistische Nachbarin Julia diesen Film interessant fand, bzw. ausreichend gut bewertet hat.

![kollaboratives Filtern](./images/kollaborativesFiltern.png)  

Bei dem kollaborativen Empfehlungssystem wurde versucht vorherzusagen, wie viele Sterne man einem Film geben würde. Dafür musste man möglichst viele Filme bewerten, um daraus überhaupt eine Tendenz und ein Profil des Nutzers erstellen zu können.

Das Hauptproblem von kollaborativen Empfehlungssystemen ist dementsprechend das Fehlen einer Datenbasis. Neue Nutzer haben noch keine Bewertungen abgegeben und haben somit auch keine statistischen Nachbarn. Selbes gilt auch für die Objekte, die einem System neu hinzugefügt werden. Wird also beispielweise ein Film neu hinzugefügt, hat er zu Beginn keine Bewertungen und kann somit nicht bei der Technik des kollaborativen Filtern berückstichtigt werden.

### 3.1.2.2 Inhaltsbasiertes Filtern

Eine andere Filtermethode ist das inhaltsbasierte Filtern. Hier werden Empfehlungen anhand von Ähnlichkeiten von Objekten oder Nutzerprofilen generiert. Die Objekte werden hierbei durch ihre Inhalte oder durch Eigenschaften und Metadaten beschrieben. Anders als beim kollaborativen Filtern wird hier nicht versucht, eine Verbindung zwischen mehreren Nutzern herzustellen, sondern es wird versucht, eine Verbindung zwischen mehreren Objekten herzustellen (Item-to-Item). Ein Nutzerprofil beinhaltet Interessen über Objekt-Attribute, die zum einen durch direkte Eingabe oder durch implizites Nutzungsverhalten (zum Beispiel der Analyse der Tätigkeiten des Nutzers) gesammelt werden. Empfehlungen werden ausgesprochen, wenn eine nahe Verbindung zwischen Nutzerpräferenzen und Objekteigenschaft besteht.

### 3.1.2.3 Algorithmus von Netflix
Eine Aussage im Atlantic Artikel besagt, dass Netflix ein System gebaut habe, welches wirklich nur mit einem in der Technologie-Welt vergleichbar ist, und zwar dem NewsFeed von Facebook. 


## 3.1.3 Analyse der Daten

Um Schlussfolgerungen aus Datenerhebungen zu ziehen, muss zuerst eine gewisse Menge an Daten zur Analyse bereit stehen.
Erst wenn genug Menschen beispielsweise an einer bestimmten Stelle Pause gedrückt oder vorgespult haben, kann man anfangen, Schlussfolgerungen aus diesem Verhalten zu ziehen.
Wenn ständig an der gleichen Stelle Pause gedrückt wird, könnte die Handlung zu langwierig oder langweilig geworden sein um das Interesse der Zuschauer zu halten. Es könnte auch sein, dass der Plot zu kompliziert wurde. Wenn genug Nutzer nach der Pause nie weiter schauen, könnte die Annahme getroffen werden, dass die Sendung schlecht ist.
Natürlich sind das alles aber nur Annahmen. Trotz der gigantischen gesammelten Datenmenge kann Netflix nicht mit 100%iger Sicherheit sagen, was dieses Verhalten der User bedeutet.

Aufgezeichnet werden alle erdenklichen Daten, von Standort des Nutzers, Gerät des Nutzers, Uhrzeit am Nutzungsort, Dauer der Nutzung, in welcher Sprache geschaut wird, ob ganze Folgen/Filme schaut werden oder ob abgebrochen wird, wann und wie lange pausiert wird, ob vorgespult wird, wann gestoppt wird und was geschaut wird natürlich, gespeichert. Außerdem werden die Ratings, die Likes, die geteilten Inhalte sowie die Interaktionen, wie Scrollen, Sucheingaben und das Hinzufügen zu Listen gespeichert.
Zum Einen weiß Netflix durch die Analyse dieser Daten, welche Schauspieler und welche Genres bevorzugt werden. Zum Anderen kann so aber auch herausgefunden werden, ob am Wochenende eher Serien oder eher Filme geschaut werden. Dies wird dann bei den nächsten Empfehlungen berücksichtigt und es wird mehr von den favorisierten Formaten vorgeschlagen.


## 3.1.4 Nutzung der Daten 

Laut Salon arbeitet Netflix seit 2012 daran, insofern Nutzen aus ihrer Big Date Kapazität zu ziehen, als dass sie versuchen damit ihre Programmauswahl zu beeinflussen. Konkret bedeutet es, dass sie Serien aufgrund ihrere Analyseergebnisse kaufen oder produzieren.
Das Pilot-Projekt dieser Strategie ist die Serie *House Of Cards*. *House Of Cards* war ursprünglich eine britische Miniserie, die 1990 auf dem britischen Kanal BBC ausgestrahlt wurde. Die Serie bestand nur aus vier Episoden und handelt von einem Politiker, der zusammen mit seiner Ehefrau Rachepläne ausübt, nachdem er vom Premierminister hintergangen wurde.

Aufgrund der Big Data-Analyse von Netflix wurde die Entscheidung getroffen, eine Neuauflage der britischen Serie *House Of Cards* zu produzieren.
Den Analyseergebnissen konnte man entnehmen, dass dieselben Personen, die das britische Original von *House Of Cards* liebten, ebenfalls Filme lieben, bei denen Kevin Spacey mitspielt oder die unter der Regie von David Fincher entstanden sind.

Die Argumente waren also:
- Die britische Version von *House of Cards* hatte ein großes Publikum,
- *The Social Network*, bei dem David Fincher Regie geführt hat, hatte ein großes Publikum,
- Nutzer, die die britische Version von *House Of Cards* geschaut haben, schauten oft auch Filme mit Kevin Spacey und/oder Filme, die unter der Regie von David Fincher entstanden sind.

Somit sollte das Remake der Serie, die für 13 Episoden 100 Millionen Dollar gekostet hat, ein Kinderspiel werden.

Verglichen zu traditionellen Studios, die außer den verkauften Tickets und DVDs kein Feedback ihrer Kunden bekommen, ist Netflix, was das Feedback und die Analyse angeht, Welten voraus. Netflix kann viel schneller handeln als die traditionelle Konkurrenz. Netflix muss vor der Produktion eines Film oder einer Serie nicht mehr ahnen, was die Nutzer sehen wollen, sondern stützt sich auf ihre Analysen. Sie können die Daten sogar bis auf die Postleitzahl herunterbrechen und herausfinden, welche Shows mit welchen Schauspielern die Nutzer in bestimmten Regionen am liebsten sehen.

Die traditionellen Studios haben einen großen Nachteil. Einer der größten Posten bei den Kosten einer Filmproduktion ist das Marketing. Es gibt aber keine Möglichkeit herauszufinden, welche der Marketingstragien erfolreich waren und welche nicht und ob es das Marketing überhaupt etwas bringt. Es können auch Millionen ins Marketing fließen und der Film wird trotzdem ein Flop.

Die Nutzer von Netflix entscheiden durch ihr Nutzungsverhalten, was produziert wird und was nicht. Ebenso legen sie fest, welche Schauspieler sie sehen wollen. Netflix hat es geschafft, eine Brücke zwischen Nutzern und Produzenten zu bauen. Das Team, das entscheidet, was produziert wird, kann sich ganz einfach an den Daten der Nutzer orientieren.

## 3.1.5 Visualisierung


Die Darstellung einzelner Sendungen hängt nicht vom Zufall ab. Ganz im Gegenteil: Die Platzierung und Auswahl der richtigen Sendungen für die einzelnen Zeilen ist ein wichtiger Teil des Personalisierungsansatzes von Netflix. Es muss also herausgefunden werden, welche Zeilen am relevantesten für jeden einzelnen Nutzer sind sowie mit welchen Sendungen die Zeilen gefüllt werden. Außerdem muss entschieden werden, an welcher Stelle der limitierten Startseite jede Zeile platziert wird, so dass die Auswahl des nächsten Videos intuitiv geschehen wird.

Hierfür nutzt Neflix das maschinelle Lernen. Die Maschine lernt, historische Informationen zu nutzen. Historische Informationen wären zum Beispiel:
+ welche Homepages wurden für die Mitglieder erstellt
+ wie interagieren die Mitglieder
+ was schauen die Mitglieder tatsächlich gerade an
+ was spielen sie überhaupt ab

Es gibt offenbar einige Herausforderungen für das Anlernen des Modells für maschinelles Lernen. Die Trainingsdaten für den Algorithmus müssen sehr bedacht ausgewählt werden. Die Herausforderung ist auch, wie die Zuordnung im Modell erlaubt ist. Wenn ein Nutzer ein Video aus einer bestimmten Zeile in der Vergangenheit abgespielt hat, heißt es nicht, dass der Nutzer dieses Video ebenfalls ausgewählt hätte, wenn es in einer anderen Zeile an erster Stelle gestanden hätte. Es könnte die Benennung der Zeile und nicht die Postition in der Zeile ausschlaggebend für das Abspielen gewesen sein. Ebenso herausfordernd kann das Lernen der Merkmale um Vielfalt darzustellen sein. Vor allem, wenn der Platz für potentielle Zeilen an unterschiedlichen Stellen groß ist, wenn der Rest der Seite (oder die bereits vergebenen Zeilen) für die Vielfalt berücksichtigt wird, ist der Platz für mögliche Seiten noch größer.

Um diese Herausforderungen zu bewältigen, ist es wichtig, eine gute Metrik auszuwählen. Von hoher Wichtigkeit für die Seitengenerierung ist, wie die Qualität der Seiten, die durch einen Algorithmus erzeugt wurden, zu bewerten ist. Jede mögliche Verbesserung des Algorithmus' wird sofort online in einem A/B-Test geprüft. Netflx möchte in der Lage sein, die wertvollen A/B-Testressourcen auf Algorithmen anzuwenden, von denen angenommen wird, dass sie die Qualität der Seiten wahrscheinlich verbessern. Die Parameter der Algorithmen sollte vor dem A/B-Test abgestimmt werden. Dazu können historische Daten verwendet werden, um hypothetische Seiten aus dem neuen algorithmischen Ansatz zu generieren.

Um sich Qualitätsmetriken auf Seitenebene auszudenken, hat sich Netflix von Rang-Metriken, die in der Informationsrückgewinnung inspirieren lassen.
TODO

http://techblog.netflix.com/2016/10/to-be-continued.html
Das Ziel des Empfehlungssystem von Netflix ist, die perfekte Serie oder den perfekten Film für jeden Nutzer zu kennen und diesen direkt beim Start von Netflix zu starten.
Wenn ein Nutzer Netflix öffnet, möchte er entweder eine ganz neue, für ihn unbekannte Show entdecken oder die nächste Folge einer bereits bekannten Serie sehen, bzw. einen angefangenen Film zuende schauen. Wenn Netflix vorhersagen kann, dass der Nutzer beim Öffnen gerade eine Serie oder einen Film weiterschauen möchte, so würde es Sinn machen, diese Show an präsenter Stelle auf der Startseite zu platzieren.
Grundsätzlich fokussiert Netflix sich hier auf die Zeile "Weiterschauen". Ein nicht unerheblicher Anteil der Streaming-Zeit erfolgt aufgrund der Platzierung der Serie oder des Films in dieser Zeile.
Wie die Zeile auf der Seite platziert wurde, hing von einigen Regeln ab, die wiederum vom der Plattform abhängig waren. In dem Artikel *To Be Continued: Helping you find shows to continue watching on Netflix* erklärt Netflix, sie wollen dies nun über die Plattformen hinweg vereinheitlichen um die Nutzererfahrung der "Weiterschauen"-Zeile anhand folgender zweier Dimensionen zu verbessern:
+ Verbesserung der Platzierung der Zeile: Sie soll höher platziert werden, wenn ein Nutzer im "Weiterschauen-Modus" ist. Sie soll tiefer platziert werden, wenn ein Nutzer eher nach einem neuen Titel sucht, sich also im "Entdeckungs-Modus" befindet.
+ Verbesserung der Reihenfolge der zuletzt angeschauten Shows in der Zeile in Abhängigkeit der Wahrscheinlichkeit, dass sie beim nächsten Aufruf von Netflix angeschaut/weitergeschaut werden.

Herauszufinden, wie hoch die Wahrscheinlichkeit ist, dass sich ein Nutzer gerade im "Weiterschauen-Modus" befindet, versucht Netflix über die Definition unterschiedlicher Aktivitätsmuster.
Ein Nutzer ist möglicherweise gewollt, eine Show fortzusetzen, wenn er:
+ schon viele Folgen einer Serie geschaut hat, diese aber noch nicht komplett zuende geschaut hat
+ vor Kurzem einen Film angefangen hat
+ eine Show vermehrt zu einer bestimmten Zeit am Tag oder über das aktuelle Gerät geschaut hat

Im "Entdeckungs-Modus" befindet sich der Nutzer eher, wenn er:
+ gerade einen Film zu Ende oder alle Staffeln und Episoden einer Serie geschaut hat
+ in letzter Zeit nichts mehr geschaut hat
+ sich neu bei Netflix angemeldet hat

Diese Hypothesen haben Netflix laut oben genanntem Artikel dazu motiviert, ein maschinenlernendes Modell zu bauen, welches obige Muster identifiziert und nutzt, um eine bessere "Weiterschauen"-Zeile zu generieren.

Um ein Empfehlungsmodell für die "Weiterschauen"-Zeile zu kreiren, braucht man zunächst Merkmale, die Muster aus dem Verhalten der Nutzer erkennen. Diese sollen dabei helfen, eine Vorhersage zu treffen, wann ein Nutzer eine Serie oder einen Film weitersehen möchte. Diese Merkmale werden als Input für das Erstellen des maschinenlernenden Modells. Die wichtigsten Merkmale können dann später nach einigen Testläufen optimiert und ausgewählt werden.

Im Artikel des Netflix Blogs haben die Autoren drei mögliche Ideen für das Erstellen des Weiterschauen-Modells berücksichtigt, darunter:
A. Eigenschaften auf Mitgliedsebene:
    + Daten über das Abonnement des Mitglieds, wie zum Beispiel die Dauer des Abonnements, das Land der Registrierung und die Sprachpräferenzen
    + Wie aktiv das Mitglied in letzter Zeit war
    + Die letzten Bewertungen des Mitglieds sowie Präferenzen in Genres

B. Eigenschaften über eine Sendung sowie die Interaktion des Nutzers mit dieser:
    + Wie lange ist es her, dass eine Sendung zu dem Katalog hinzugefügt, bzw. vom Mitglied geschaut wurde
    + Wie viel der Sendung hat das Mitglied geschaut
    + Metadaten über die Sendung, wie zum Beispiel Typ, Genre, Anzahl der Episoden. Beipsielsweise werden Kindersendungen öfert wiederholt geschaut
    + Beliebtheit und Relevanz der Sendung für das Mitglied
    + Wie oft das Mitglied die Sendung weitergeschaut hat

C. Kontextbezogene Eigenschaften:
    + Aktuelle Uhrzeit sowie Wochentag
    + Standort
    + Genutztes Gerät des Mitglieds

Für die optimale Darstellung der "Weiterschauen"-Zeile gibt es zwei Aufgaben: Sortierung der Ergebnisse innerhalb der Zeile sowie die Platzierung der Ergebnisse an eine sinnvolle Stelle auf der Startseite des Mitglieds.

Für die Sortierung der Ergebnisse innerhalb der "Weiterschauen"-Zeile hat Netflix ein Modell trainiert, das Sessions nutzt, in denen das Mitglied eine zuvor angesehene Sendung weiterschaut. In jeder Session lernt das Modell zwischen den Sendungen, die wiederholt werden, zu unterscheiden und ordnet diese in der vorhergesagten Wahrscheinlichkeit an.

Um die "Weiterschauen"-Zeile sinnvoll, bzw. an einer geeigneten Stelle auf der Startseite des Mitglieds zu platzieren, möchte Netflix die Wahrscheinlichkeit abschätzen, ob sich das Mitglied gerade im "Weiterschauen-Modus" oder aber im "Entdeckungs-Modus" befindet, so die Autoren des Blog Posts.
Aufgrund dieser Wahrscheinlichkeit könnten mehrere Ansätze verfolgt werden. Ein einfacher Ansatz wäre, dass es nur zwei Möglichkeiten gibt, die Zeile zu platzieren: oben auf der Seite oder weiter unten auf der Seite.
Durch Anwendung eines Schwellenwertes auf die vorhergesehene Wahrscheinlichkeit kann Netflix entscheiden, in welcher dieser beiden möglichen Positionen die Zeile platziert wird. Ein anderer Ansatz wäre, die Wahrscheinlichkeit auf verschiedene Positionen abzubilden.

## 3.1.6 Andere Anbieter:
Amazon Prime, Snap von Sky, Maxdome, Videoload, Watchever

http://techblog.netflix.com/2012/04/netflix-recommendations-beyond-5-stars.html