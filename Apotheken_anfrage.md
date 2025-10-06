
—

💻 PHP-Beispiel: Anfrage an Apotheke (Versand & Tracking)
—


<?php
// Empfängeradresse der Apotheke
$to = "kontakt@apotheke-beispiel.de";  // <-- Hier Apotheke-Mail eintragen

// Betreffzeile
$subject = "Nachfrage zu Sendungsverfolgung und Versanddienstleister";

// Absenderdaten
$from = "johannes.fluegel@example.com";  // <-- Eigene Mailadresse
$headers = "From: Johannes Flügel <" . $from . ">\r\n";
$headers .= "Reply-To: " . $from . "\r\n";
$headers .= "Content-Type: text/plain; charset=UTF-8\r\n";

// Nachrichtentext
$message = <<<EOT
Sehr geehrte Damen und Herren,

ich möchte mich erkundigen, ob es bei Ihnen üblich ist, dass Sendungsverläufe über DHL-Tracking mitunter nicht oder nur verzögert aktualisiert werden.
Mir ist aufgefallen, dass sich der Status bei manchen Sendungen ungewöhnlich verhält, und ich möchte verstehen, ob dies erfahrungsgemäß an der Übermittlung seitens DHL liegt oder ob es in bestimmten Fällen durch interne Abläufe oder Nutzerverhalten beeinflusst werden kann.

In diesem Zusammenhang würde mich auch interessieren, welche Schritte Sie unternehmen, um eine möglichst transparente und nachvollziehbare Sendungsverfolgung für Ihre Kundinnen und Kunden sicherzustellen.

Zudem wäre es hilfreich, wenn man bereits im Vorfeld erfahren könnte, mit welchem Versanddienstleister die Lieferung erfolgt. So ließe sich vermeiden, dass Kundinnen und Kunden durch unklare Versandabläufe oder wiederkehrende Probleme mit bestimmten Dienstleistern unnötig belastet werden.
Eine solche Information trägt sicherlich dazu bei, langfristig Vertrauen und Zufriedenheit zu stärken.

Ich danke Ihnen im Voraus für Ihre Rückmeldung und Aufklärung zu diesem Thema.

Mit freundlichen Grüßen  
Johannes Flügel  
Südstraße 25(a)  
95615 Marktredwitz  
Postnummer: 1061209009  
06.10.2025
EOT;

// E-Mail versenden
if (mail($to, $subject, $message, $headers)) {
    echo "Ihre Anfrage wurde erfolgreich an die Apotheke gesendet.";
} else {
    echo "Beim Senden Ihrer Anfrage ist ein Fehler aufgetreten.";
}
?>


—

🔧 Kurze Anleitung:

—
1.	Ersetze die Zeile
—
php

$to = "kontakt@apotheke-beispiel.de";

—

 mit der echten E-Mail-Adresse der Apotheke.

	2.	Optional kannst du auch deine eigene Adresse in $from ändern.
	3.	Lade die Datei z. B. als apothekenanfrage.php auf deinen Webserver hoch oder führe sie lokal mit Mail-Unterstützung (z. B. über XAMPP mit SMTP) aus.
	4.	Nach Absenden wird deine Nachricht formatiert als Klartext-Mail an die Apotheke gesendet.

 