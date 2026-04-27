
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lina MaLio – Second Hand Mode</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #f8fdf6 0%, #f0f9ed 100%);
        }

        /* Navigation */
        nav {
            background: linear-gradient(135deg, #2d6a4f 0%, #40916c 100%);
            padding: 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 8px rgba(45, 106, 79, 0.15);
        }

        .nav-container {
            max-width: 900px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 20px;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .logo img {
            height: 45px;
            width: auto;
        }

        .logo-text {
            color: white;
            font-weight: 700;
            font-size: 1.3rem;
            letter-spacing: -0.5px;
        }

        .nav-links {
            display: flex;
            gap: 30px;
            list-style: none;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s ease;
            font-size: 0.95rem;
        }

        .nav-links a:hover {
            color: #b7e4c7;
        }

        .hamburger {
            display: none;
            flex-direction: column;
            gap: 6px;
            cursor: pointer;
        }

        .hamburger span {
            width: 25px;
            height: 3px;
            background: white;
            border-radius: 2px;
            transition: all 0.3s ease;
        }

        /* Container */
        .container {
            max-width: 900px;
            margin: 0 auto;
            padding: 20px;
        }

        header {
            background: linear-gradient(135deg, #2d6a4f 0%, #40916c 100%);
            color: white;
            padding: 60px 20px;
            margin-bottom: 60px;
            border-radius: 0 0 12px 12px;
            box-shadow: 0 4px 6px rgba(45, 106, 79, 0.1);
            text-align: center;
        }

        header h1 {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 12px;
            letter-spacing: -0.5px;
        }

        header p {
            font-size: 1.2rem;
            font-weight: 300;
            opacity: 0.95;
        }

        section {
            margin-bottom: 50px;
            padding: 0 20px;
        }

        h2 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: #2d6a4f;
            border-bottom: 3px solid #52b788;
            padding-bottom: 10px;
            display: inline-block;
        }

        h3 {
            font-size: 1.3rem;
            margin-bottom: 15px;
            color: #40916c;
            margin-top: 20px;
        }

        p {
            margin-bottom: 15px;
            line-height: 1.8;
            color: #555;
        }

        ul {
            margin-left: 20px;
            margin-bottom: 15px;
        }

        li {
            margin-bottom: 10px;
            line-height: 1.8;
        }

        .highlight {
            background: white;
            border-left: 5px solid #52b788;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 2px 8px rgba(82, 183, 136, 0.08);
            margin-bottom: 40px;
        }

        .highlight h2 {
            border-bottom: none;
            padding-bottom: 0;
            margin-bottom: 15px;
        }

        a {
            color: #40916c;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        a:hover {
            color: #2d6a4f;
            text-decoration: underline;
        }

        a.button {
            display: inline-block;
            margin-top: 15px;
            padding: 12px 28px;
            background: linear-gradient(135deg, #40916c 0%, #2d6a4f 100%);
            color: white;
            text-decoration: none;
            border-radius: 6px;
            font-weight: 600;
            transition: all 0.3s ease;
            box-shadow: 0 4px 12px rgba(45, 106, 79, 0.2);
        }

        a.button:hover {
            background: linear-gradient(135deg, #2d6a4f 0%, #1b4332 100%);
            transform: translateY(-2px);
            box-shadow: 0 6px 16px rgba(45, 106, 79, 0.3);
            text-decoration: none;
        }

        footer {
            background: #2d6a4f;
            color: white;
            padding: 40px 20px;
            margin-top: 80px;
            font-size: 0.95rem;
            line-height: 1.8;
        }

        footer h2 {
            color: white;
            border-bottom: 3px solid #52b788;
            margin-top: 30px;
            margin-bottom: 20px;
        }

        footer h3 {
            color: #c1ddc1;
            margin-top: 25px;
            margin-bottom: 15px;
        }

        footer p {
            color: #d8f3dc;
        }

        footer a {
            color: #b7e4c7;
        }

        footer a:hover {
            color: white;
        }

        .divider {
            width: 100%;
            height: 1px;
            background: rgba(255, 255, 255, 0.2);
            margin: 30px 0;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .nav-links {
                position: absolute;
                top: 60px;
                left: 0;
                right: 0;
                background: linear-gradient(135deg, #2d6a4f 0%, #40916c 100%);
                flex-direction: column;
                gap: 0;
                padding: 20px;
                display: none;
                box-shadow: 0 4px 8px rgba(45, 106, 79, 0.2);
            }

            .nav-links.active {
                display: flex;
            }

            .nav-links a {
                padding: 12px 0;
                border-bottom: 1px solid rgba(255, 255, 255, 0.2);
            }

            .hamburger {
                display: flex;
            }

            header {
                padding: 40px 20px;
            }

            header h1 {
                font-size: 2rem;
            }

            header p {
                font-size: 1rem;
            }

            h2 {
                font-size: 1.5rem;
            }

            .highlight {
                padding: 20px;
            }

            .logo img {
                height: 40px;
            }

            .logo-text {
                font-size: 1.1rem;
            }

            .nav-links {
                gap: 0;
            }

            .container {
                padding: 15px;
            }

            section {
                padding: 0;
            }
        }

        @media (max-width: 480px) {
            header h1 {
                font-size: 1.5rem;
            }

            header p {
                font-size: 0.95rem;
            }

            h2 {
                font-size: 1.3rem;
            }

            h3 {
                font-size: 1.1rem;
            }

            .highlight {
                padding: 15px;
            }

            footer {
                padding: 20px;
            }
        }
    </style>
</head>

<body>
    <!-- Navigation -->
    <nav>
        <div class="nav-container">
            <div class="logo">
                <img src="Logo Lina Malio.png">
                <span class="logo-text">Lina MaLio</span>
            </div>
            <ul class="nav-links" id="navLinks">
                <li><a href="#angebot">Angebot</a></li>
                <li><a href="#impressum">Impressum</a></li>
                <li><a href="#datenschutz">Datenschutz</a></li>
                <li><a href="#agb">AGB</a></li>
                <li><a href="#kontakt">Kontakt</a></li>
            </ul>
            <div class="hamburger" id="hamburger">
                <span></span>
                <span></span>
                <span></span>
            </div>
        </div>
    </nav>

    <div class="container">
        <!-- Kurzbeschreibung -->
        <section>
            <p>
                Bei Lina MaLio findest du handverlesene Second-Hand-Mode zu absoluten Bestpreisen. 
                Jedes Teil wird sorgfältig geprüft und mit Liebe ausgewählt.
            </p>
        </section>

        <!-- Über uns -->
        <section>
            <h2>Über Lina MaLio</h2>
            <p>
                Lina MaLio ist ein kleines Herzensprojekt mit dem Ziel, Mode nachhaltiger zu machen. 
                Wir glauben daran, dass schöne Kleidung kein neues Etikett braucht.
            </p>
        </section>

        <!-- Besonderheiten -->
        <section class="highlight">
            <h2>Warum Lina MaLio?</h2>
            <ul>
                <li>✔ Sorgfältig geprüfte Qualität</li>
                <li>✔ Nachhaltig & ressourcenschonend</li>
                <li>✔ Faire Preise</li>
                <li>✔ Liebevoll verpackt</li>
            </ul>
        </section>

        <!-- Angebot -->
        <section id="angebot">
            <h2>Unser Angebot</h2>
            <p>Aktuell findest du bei uns:</p>
            <ul>
                <li>Damenmode</li>
                <li>Accessoires</li>
                <li>Saisonale Einzelstücke</li>
            </ul>
        </section>

        <!-- Call to Action -->
        <section class="highlight" id="kontakt">
            <h2>Neugierig geworden?</h2>
            <p>Schau dich gerne um oder kontaktiere uns bei Fragen.</p>
            <a href="mailto:support@lina-malio.de" class="button">Kontakt aufnehmen</a>
        </section>
    </div>

    <footer>
        <div class="container">
            <div class="divider"></div>

            <!-- Impressum -->
            <h2 id="impressum">Impressum</h2>

            <h3>Angaben gemäß § 5 TMG</h3>
            <p>
                Lina MaLio GbR<br>
                Bahnhofstraße 29<br>
                76744 Wörth am Rhein<br>
                Deutschland
            </p>

            <h3>Kontakt</h3>
            <p>
                E-Mail: <a href="mailto:support@lina-malio.de">support@lina-malio.de</a><br>
                Website: <a href="https://www.lina-malio.de" target="_blank">www.lina-malio.de</a>
            </p>

            <h3>Vertretungsberechtigung</h3>
            <p>Selina Scherthan, Justin Scherthan</p>

            <h3>Umsatzsteuer-Identifikationsnummer</h3>
            <p>DE[beantragt]</p>

            <h3>Verantwortlicher für den Inhalt (§ 55 Abs. 2 RStV)</h3>
            <p>Justin Scherthan</p>

            <h3>Haftungsausschluss</h3>
            <p>
                Wir übernehmen keine Haftung für die Inhalte externer Links. 
                Für den Inhalt der verlinkten Seiten sind ausschließlich deren Betreiber verantwortlich.
            </p>

            <h3>Verpackungsgesetz – Systembeteiligung (§ 7 VerpackG)</h3>
            <p>
                Lina MaLio GbR ist gemäß § 7 Abs. 1 des Verpackungsgesetzes verpflichtet, 
                sich an einem dualen System zur Rücknahme und Verwertung von Verkaufsverpackungen zu beteiligen. 
                Wir beteiligen uns über das duale System INTERSEROH+ GmbH am Rücknahmesystem.
            </p>

            <h3>Hinweise zu Marken und Produktdarstellungen</h3>
            <p>
                Alle genannten Marken- und Produktnamen sind Eigentum der jeweiligen Rechteinhaber. 
                Die Nennung erfolgt ausschließlich zur Beschreibung der angebotenen Waren. 
                Lina MaLio GbR steht in keiner wirtschaftlichen Verbindung zu den genannten Markenherstellern. 
                Es handelt sich um den gewerblichen Handel mit gebrauchter Originalware.
            </p>

            <h3>Echtheitsprüfung / Second-Hand-Hinweis</h3>
            <p>
                Alle angebotenen Artikel werden vor dem Verkauf sorgfältig auf Echtheit und Zustand geprüft. 
                Es handelt sich ausschließlich um gebrauchte Ware, sofern nicht ausdrücklich anders angegeben.
            </p>

            <div class="divider"></div>

            <!-- Datenschutzerklärung -->
            <h2 id="datenschutz">Datenschutzerklärung</h2>

            <p>
                Wir freuen uns über Ihr Interesse an unserer Website. Der Schutz Ihrer personenbezogenen 
                Daten ist uns ein wichtiges Anliegen. Nachfolgend informieren wir Sie über die Verarbeitung 
                personenbezogener Daten bei der Nutzung unserer Website gemäß der Datenschutz-Grundverordnung (DSGVO).
            </p>

            <h3>1. Verantwortlicher</h3>
            <p>
                Lina MaLio GbR<br>
                Bahnhofstraße 29<br>
                76744 Wörth am Rhein<br>
                Deutschland<br><br>
                E-Mail: <a href="mailto:support@lina-malio.de">support@lina-malio.de</a>
            </p>

            <h3>2. Erhebung und Speicherung personenbezogener Daten</h3>
            <p>
                Beim Aufrufen unserer Website werden durch den von Ihnen verwendeten Internet-Browser automatisch 
                Informationen an den Server unserer Website gesendet. Diese Informationen werden temporär in einem 
                sogenannten Logfile gespeichert.
            </p>

            <p>Erfasst werden dabei insbesondere:</p>
            <ul>
                <li>IP-Adresse des anfragenden Gerätes</li>
                <li>Datum und Uhrzeit des Zugriffs</li>
                <li>Name und URL der abgerufenen Datei</li>
                <li>Website, von der aus der Zugriff erfolgt (Referrer-URL)</li>
                <li>Verwendeter Browser und ggf. das Betriebssystem Ihres Gerätes</li>
            </ul>

            <p>
                Die genannten Daten werden verarbeitet, um einen reibungslosen Verbindungsaufbau der Website 
                zu gewährleisten sowie zur Systemsicherheit und -stabilität. 
                Rechtsgrundlage: Art. 6 Abs. 1 lit. f DSGVO.
            </p>

            <h3>3. Kontaktaufnahme per E-Mail</h3>
            <p>
                Wenn Sie uns per E-Mail kontaktieren, werden die von Ihnen übermittelten personenbezogenen Daten 
                (z. B. Name, E-Mail-Adresse, Nachricht) ausschließlich zur Bearbeitung Ihrer Anfrage gespeichert 
                und verwendet. Rechtsgrundlage: Art. 6 Abs. 1 lit. b DSGVO.
            </p>

            <h3>4. Weitergabe von Daten</h3>
            <p>Eine Übermittlung Ihrer persönlichen Daten an Dritte findet nicht statt, außer:</p>
            <ul>
                <li>Sie haben Ihre ausdrückliche Einwilligung dazu erteilt</li>
                <li>Die Weitergabe ist zur Erfüllung rechtlicher Verpflichtungen erforderlich</li>
                <li>Die Weitergabe ist zur Abwicklung von Vertragsverhältnissen erforderlich</li>
            </ul>

            <h3>5. Cookies</h3>
            <p>Unsere Website verwendet keine Cookies.</p>

            <h3>6. Ihre Rechte als betroffene Person</h3>
            <p>Sie haben das Recht:</p>
            <ul>
                <li>Auskunft über Ihre bei uns gespeicherten personenbezogenen Daten zu verlangen (Art. 15 DSGVO)</li>
                <li>Berichtigung unrichtiger Daten zu verlangen (Art. 16 DSGVO)</li>
                <li>Löschung Ihrer Daten zu verlangen (Art. 17 DSGVO)</li>
                <li>Einschränkung der Verarbeitung zu verlangen (Art. 18 DSGVO)</li>
                <li>Widerspruch gegen die Verarbeitung einzulegen (Art. 21 DSGVO)</li>
                <li>Datenübertragbarkeit zu verlangen (Art. 20 DSGVO)</li>
            </ul>

            <p>
                Zudem haben Sie das Recht, sich bei einer Datenschutzaufsichtsbehörde zu beschweren.
            </p>

            <h3>7. Datensicherheit</h3>
            <p>
                Wir verwenden geeignete technische und organisatorische Sicherheitsmaßnahmen, um Ihre Daten 
                gegen zufällige oder vorsätzliche Manipulationen, teilweisen oder vollständigen Verlust 
                sowie gegen den unbefugten Zugriff Dritter zu schützen.
            </p>

            <h3>8. Aktualität und Änderung dieser Datenschutzerklärung</h3>
            <p>
                Diese Datenschutzerklärung ist aktuell gültig (Stand: April 2026). 
                Durch die Weiterentwicklung unserer Website oder aufgrund gesetzlicher Vorgaben kann eine 
                Änderung dieser Datenschutzerklärung erforderlich werden.
            </p>

            <div class="divider"></div>

            <!-- Allgemeine Geschäftsbedingungen -->
            <h2 id="agb">Allgemeine Geschäftsbedingungen (AGB)</h2>

            <h3>1. Geltungsbereich</h3>
            <p>
                Diese Allgemeinen Geschäftsbedingungen (AGB) gelten für alle Verträge, die zwischen 
                Lina MaLio GbR und Verbrauchern über den Verkauf von Waren geschlossen werden.
            </p>

            <h3>2. Vertragspartner</h3>
            <p>
                Der Kaufvertrag kommt zustande mit:<br>
                Lina MaLio GbR<br>
                Bahnhofstraße 29<br>
                76744 Wörth am Rhein<br>
                Deutschland
            </p>

            <h3>3. Angebot und Vertragsschluss</h3>
            <p>
                Die Darstellung der Waren stellt kein rechtlich bindendes Angebot dar, 
                sondern eine unverbindliche Aufforderung zur Abgabe einer Bestellung. 
                Der Vertrag kommt zustande, wenn wir die Bestellung ausdrücklich bestätigen oder die Ware versenden.
            </p>

            <h3>4. Preise und Versandkosten</h3>
            <p>
                Alle angegebenen Preise sind Endpreise gemäß § 19 UStG (Kleinunternehmerregelung), 
                zuzüglich ggf. anfallender Versandkosten, sofern diese nicht ausdrücklich anders ausgewiesen sind.
            </p>

            <h3>5. Lieferung</h3>
            <p>
                Die Lieferung erfolgt an die vom Kunden angegebene Lieferadresse. 
                Angaben zu Lieferzeiten sind unverbindlich, sofern nicht ausdrücklich ein fester Liefertermin zugesagt wurde.
            </p>

            <h3>6. Zahlungsbedingungen</h3>
            <p>
                Die Zahlung erfolgt per den im jeweiligen Angebot angegebenen Zahlungsarten. 
                Der Kaufpreis ist unmittelbar nach Vertragsschluss fällig.
            </p>

            <h3>7. Eigentumsvorbehalt</h3>
            <p>Die Ware bleibt bis zur vollständigen Zahlung unser Eigentum.</p>

            <h3>8. Gewährleistung</h3>
            <p>
                Es gelten die gesetzlichen Gewährleistungsrechte. 
                Bei gebrauchten Waren kann die Gewährleistungsfrist auf ein Jahr verkürzt sein, 
                sofern dies gesetzlich zulässig ist.
            </p>

            <h3>9. Haftung</h3>
            <p>
                Wir haften uneingeschränkt bei Vorsatz und grober Fahrlässigkeit. 
                Bei leichter Fahrlässigkeit nur bei Verletzung wesentlicher Vertragspflichten.
            </p>

            <h3>10. Schlussbestimmungen</h3>
            <p>
                Es gilt das Recht der Bundesrepublik Deutschland. 
                Sollten einzelne Bestimmungen dieser AGB unwirksam sein, 
                bleibt die Wirksamkeit der übrigen Bestimmungen unberührt.
            </p>
        </div>
    </footer>

    <script>
        // Mobile Menu Toggle
        const hamburger = document.getElementById('hamburger');
        const navLinks = document.getElementById('navLinks');

        hamburger.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });

        // Close menu when a link is clicked
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
            });
        });
    </script>
</body>
</html>
