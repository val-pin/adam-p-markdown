# Informationsarten

## Flüchtig vs. Persistent
* **Flüchtige Informationen** werden dem Benutzer einmalig signalisiert und nicht gespeichert. Die Information ist nach der einmaligen Darstellung nicht mehr abrufbar.

* **Transiente Informationen** sind im Prinzip auch flüchtig, werden aber für einen längeren Zeitraum zwischengespeichert (aber nie persistiert). Dies sind z.B. Informationen die auf eine Session begrenzt zur Verfügung stehen.

* **Persistente Informationen** werden dauerhaft (bzw. für ein beliebiges Zeitintervall) im System vorgehalten und der Benutzer hat die Möglichkeit diese Information erneut abzurufen.

* **Hybride Informationen** werden mit einem Medium flüchtig dargestellt und können an einer anderen Stelle persistent vorgehalten werden.

## Push vs. Pull
* **Push Informationen** werden dem Benutzer direkt zugestellt. Das System ist dafür verantwortlich, dass der Benutzer aktiv mit der Information versorgt wird.
* **Pull Informationen** werden vom Benutzer abgerufen, das System stellt diese nur an einer definierten Stelle zur Verfügung.
* Auch hier ist ein **Hybrid denkbar**, der bspw. per Push über die Existenz informiert, Detailinformationen werden aber vom Benutzer per Pull abgeholt. 

## Prominenz
* Ein **Toast** stellt Informationen zeitweise zur Verfügung und bringt diese kurzzeitig ins Blickfeld des Benutzers. Dies eignet sich primär für flüchtige Informationen.
* Informationen können zentral in der **Hall** dargestellt werden. Dies eignet sich besonders dazu dem Benutzer eine Orientierung über die Räume und deren Aktivitäten zu bieten.
* Auf einem **Splashscreen** können dem Benutzer ebenfalls zentral Informationen bereit gestellt werden. Dieser ist vor allem dafür geeignet dem Benutzer „Komfortinformationen“ zu bieten, um das Arbeiten mit dem System zu erleichtern. Hier ist z.B. eine Liste mit den zuletzt genutzten Räumen oder mit Aktivitäten anderer (in Beziehung stehender) Nutzer denkbar.
* **Infoseiten** bieten weitere Informationen zu Elementen. So lassen sich z.B. Änderungshistorien darstellen.
* In **Teaserbereichen** können Sekundärinformationen im System dargestellt werden. Diese können kontextsensitiv sein, müssen es aber nicht.
* Die **Benutzerliste** ist ein spezieller Teaser. In ihr werden alle Benutzer eines Raumes (genauer: mit Zugangsberechtigung zu diesem) dargestellt. Die Benutzerliste ist in jedem Raum sichtbar.  
* Im **Contentbereich** sollten immer dann für Informationen dargestellt werden, wenn sie direkt mit Nutzerinteraktion zusammenhängen bzw. für den laufenden Arbeitsvorgang wichtig sind. Diese können dort zentral oder auch kontextsensitiv dargestellt werden.

# Aktionen in CURE
## Benutzer
### Benutzer registriert sich
Diese Information ist für das Groß der Nutzer relativ unbedeutend. Die Information kann aber dazu helfen das System lebendiger zu gestalten.
### Benutzer loggt sich ein
Der Benutzerlogin ist auf den ersten Blick auch eher unbedeutend. Für andere Benutzer, die mit dem Benutzer aufgrund von Relationen (man befindet sich im selben Raum, man bearbeitet ein Dokument, welches zuletzt von einem anderen Nutzer bearbeitet wurde, etc.) interagieren möchten, kann die Information aber sehr wichtig sein.
### Benutzer loggt sich aus
Ähnlicher Informationsgehalt wie der Benutzerlogin. Einzig die Tatsache, dass man Benutzer nicht beliebig darauf hinweisen möchte, dass das System nicht mehr genutzt wird, ist zu beachten. Der Benutzerlogin hat mehr „Werbegehalt“ für das System. Für interagierende Nutzer ist der Informationsgehalt aber ähnlich anzusiedeln wie beim Login.
### Benutzer chattet
Ein Benutzer der im Chat aktiv ist kann für andere Benutzer interessant sein. Auch die Information, dass ein Benutzer für den Chat bereitsteht ist wichtig (es sei denn, dies sind per Definition alle eingeloggten Benutzer). Interessant ist auch, mit welchen Benutzern sich dieser im Gespräch befindet, da dies stattfindende Gruppendynamiken aufzeigen kann. Ein Beispiel: Drei Mitglieder eines Raumen unterhalten sich im Chat. Ein vierter Benutzer befindet sich gerade in einem anderen Raum und liest eine Wikiseite. Wenn er die stattfindende Unterhaltung „sehen“ könnte, wäre dies eine sehr interessante Information.

## Räume
### Benutzer bekommt Zugriff auf einen Raum
Ein Benutzer bekommt einen Schlüssel für einen Raum ausgestellt und kann ab jetzt mit diesem interagieren.   Diese Information ist interessant für andere Benutzer in diesem Raum.
### Benutzer betritt einen Raum
Ein Benutzer betritt einen Raum und steht somit anderen Benutzern im Raum für direkte Interaktion zur Verfügung. Nutzer sollten immer ein ausgeprägtes „Gefühl“ darüber haben, wer sich außer Ihnen in einem Raum aufhält. 
### Benutzer verlässt einen Raum
Ein Benutzer wechselt in einen anderen Raum, schließt seine Session oder ähnliches. Er steht dem verlassenden Raum somit nicht für eine Interaktion zur Verfügung. Die Benutzergruppe muss daher auf das Verlassen aufmerksam gemacht werden. 
 gibt seinen Schlüssel zu einem Raum zurück. Diese Information ist für die Nutzer des Raumes interessant, insbesondere aber für den Benutzer, der den Schlüssel angelegt hat bzw. den Raum administriert.
### Benutzer legt einen Raum an
Ein Benutzer legt einen neuen Raum an.  Diese Information ist besonders bei Unterräumen interessant für alle Benutzer des Hauptraums.
### Benutzer bearbeitet einen Raum
Die Information, dass ein Raum von Benutzer X bearbeitet wird ist essentiell für alle Benutzer, die sich gerade in dem Raum befinden, aber auch für alle anderen Teilnehmer mit Zugang zu diesem Raum sehr interessant. Beginnen andere Benutzer zeitgleich mit der Bearbeitung des Raumes, so wird die Information von kritischer Wichtigkeit.
### Benutzer löscht einen Raum
Hier ist der Informationsbedarf entsprechend dem Bearbeiten oder sogar noch höher. Der Konflikt, dass ein Raum gelöscht wird, in dem sich noch Nutzer befinden oder in dem Unterräume existieren erfordert ein sehr gutes Informationskonzept. 
### Benutzer verliert Zugriff auf einen Raum
Ein Benutzer gibt seinen Schlüssel zu einem Raum zurück oder bekommt diesen entzogen. Diese Information ist für die Nutzer des Raumes interessant, insbesondere aber für den Benutzer, der den Schlüssel angelegt hat bzw. den Raum administriert.

## Ordner
### Benutzer öffnet einen Ordner
Ein Benutzer öffnet einen Ordern, um den Dateiinhalt zu betrachten. Diese Information ist interessant für Benutzer, die den Ordner bearbeiten möchten.
### Benutzer legt einen Ordner an
Das Anlegen eines Ordners ist eine interessante Information für alle, die einen Zugang zu dem entsprechenden Raum haben.
### Benutzer bearbeitet einen Ordner
Das Bearbeiten ist eine wichtige Information für alle, die sich in dem Ordner aufhalten und insbesondere für die Benutzer, die den Raum ebenfalls bearbeiten.
### Benutzer löscht einen Ordner
Wird ein Ordner gelöscht, so ist dies interessant für alle Benutzer, die Zugriff auf den Raum haben.
### Benutzer lädt Datei in Ordner
Neue Dateien in einem Ordner sind interessant für alle Benutzer, die Zugriff auf den Raum haben.
### Benutzer entfernt Datei aus Ordner
Hier ist der Informationsbedarf entsprechend dem Bearbeiten oder sogar noch höher. Der Konflikt, dass ein Ordner gelöscht wird, in dem sich noch Nutzer befinden oder Dateien abgelegt sind erfordert ein sehr gutes Informationskonzept. 
### Benutzer schließt einen Ordner
Wichtig für Benutzer, die einen Ordner bearbeiten (möchten).

## Wikiseiten
### Seite anlegen
Legt ein Benutzer einen neue Wikiseite innerhalb eines Raumes an, so ist dies vermutlich eine wichtige Information für alle Teilnehmer. Hier könnte es sogar die Möglichkeit geben, dass der Autor entscheidet, wie wichtig die Informationen für andere Nutzer sind und in welchem Umfang diese informiert werden.
### Seite editieren
Eine geänderte Wikiseite enthält potentiell neue Informationen für alle Benutzer des Raumes. Wie bei der Neuanlage eines Raumes, so kann auch hier evtl. der Autor entscheiden, wie die Nutzer informiert werden. 
### Seite löschen
Wird eine Wikiseite gelöscht, so müssen alle Betrachter dieser Seite frühzeitig informiert werden. Auch für alle anderen Mitglieder des Raumes ist diese Information wichtig.


#Anwendungsmatrix

Spalte 1: F=Flüchtig, T=Transient, P=Persistent, H=Hybrid
Spalte 2: >=Push, <=Pull, H=Hybrid
Spalte 3: T=Toast, H=Hall, S=Splashscreen, I=Infoseite, R=Teaser, B=Benutzerliste, C=Content*

|     Benutzergruppe |  Alle   | Zugriff     | Geöffnet          | In Bearbeitung |
|--------------------|---------|-------------|-------------------|----------------|
| Aktion             |         |             |                   |                |
| **Registrierung**  |         |             |                   |                |
| Login              | F > T   |             | T > B             |                |
| Logout             |         |             | T > B             |                |
| Chatten            |         | H H SR      | F > B             |                |
|                    |         |             |                   |                |
| **Raumaktionen**   |         |             |                   |                |
| Zugriff vergeben   |         | H H IR      | P > B             |                |
| Raum betreten      |         |             | T > B             | T > C          |
| Raum verlassen     |         | P < I       | T > B             | F > C          |
| Raum anlegen       | P < H   |             |                   |                |
| Raum bearbeiten    |         |             |                   | T > C          |
| Raum löschen       |         | T < S       | T > C             | T > C          |
| Zugriff verlieren  |         | TP H SI     | T > B             | T > C          |
|                    |         |             |                   |                |
| **Ordneraktionen** |         |             |                   |                |
| Ordner öffnen      |         |             |                   |                |
| Ordner anlegen     |         | T > R       |                   |                |
| Ordner bearbeiten  |         |             | T > C             | T > C          |
| Ordner löschen     |         |             | T > C             | T > C          |
| Datei hochladen    |         | T > R       |                   |                |
| Datei entfernen    |         | P < I       | T > C             |                |
| Ordner schließen   |         |             |                   |                |
|                    |         |             |                   |                |
| **Wikiseiten**     |         |             |                   |                |
| Seite anlegen      |         | H H IR      |                   |                |
| Seite editieren    |         | H H IR      | T > C             | T > C          |
| Seite löschen      |         | H H IR      | T > C             | T > C          |
