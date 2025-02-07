Issues:
Belangrijkste Labels:
•	🏆 High Priority
•	🚀 Medium Priority
•	⏳ Low Priority
•	🎨 Frontend
•	🖥 Backend
•	🗄 Database
•	🔗 API
•	🔐 Security
•	🏛 Architectuur
•	♿ Accessibility

________________________________________
🔹 Fundamentele Setup
1. Project Setup & Structuur 🏛 🖥 🗄 (🏆 Hoog)
•	Maak een repository aan en bepaal de folderstructuur.
•	Backend: Flask/FastAPI/Django.
•	Database: SQLite/MySQL/PostgreSQL.
•	Frontend: HTML, CSS (Bootstrap/Tailwind), JavaScript.
•	Zorg voor een .gitignore, README en een basisomgeving.
2. Database ERD Ontwerp 🗄 🏛 (🏆 Hoog)
•	Ontwerp een Entity-Relationship Diagram (ERD) voor: 
o	Ervaringsdeskundigen (gebruikers).
o	Beheerders.
o	Organisaties.
o	Onderzoeken.
o	Inschrijvingen.
•	Definieer relaties (1:N tussen ervaringsdeskundigen en inschrijvingen, enz.).
•	Kies database en maak een eerste migratie.
________________________________________
🔹 Gebruikersbeheer
3. Registratie & Authenticatie - Ervaringsdeskundigen 🎨🖥🗄 (🏆 Hoog)
•	Gebruikers kunnen zich registreren met: 
o	Naam, geboortedatum, beperking(en), e-mail, telefoonnummer.
•	Een beheerder moet een account goedkeuren voordat ze kunnen inloggen.
•	Gebruik hashing voor wachtwoorden.
•	Valideer dat een ervaringsdeskundige jonger dan 18 een toezichthouder moet hebben.
4. Registratie & Authenticatie - Beheerders 🖥🗄 (🏆 Hoog)
•	Beheerders moeten zich kunnen aanmelden.
•	Geen zelfregistratie voor beheerders.
•	Rollen en rechten moeten correct ingesteld worden.
5. Profielbeheer - Ervaringsdeskundigen 🎨🖥🗄 (🚀 Medium)
•	Ervaringsdeskundigen kunnen hun gegevens aanpassen na goedkeuring.
•	Geen extra goedkeuring vereist voor updates.
6. Zelf verwijderen van account (met reden) 🎨🖥🗄 (⏳ Laag)
•	Gebruikers moeten hun account kunnen deactiveren.
•	Beheerders kunnen verwijderde accounts nog inzien.
________________________________________
🔹 Onderzoeksmatching
7. Organisaties registreren & goedkeuren 🖥🗄 (🚀 Medium)
•	Organisaties moeten een API-sleutel ontvangen na goedkeuring.
8. Onderzoek aanmaken & goedkeuren 🎨🖥🗄🔗 (🏆 Hoog)
•	Organisaties kunnen onderzoeken aanmaken met: 
o	Titel, beschrijving, locatie, beloning, doelgroep (leeftijd, beperking, type onderzoek).
•	Beheerders moeten goedkeuring geven voordat het zichtbaar wordt.
9. Onderzoeken matchen met ervaringsdeskundigen 🎨🖥🗄 ♿ (🚀 Medium)
•	Ervaringsdeskundigen zien alleen onderzoeken die bij hun profiel passen.
•	UI: gebruik bijvoorbeeld kaarten i.p.v. een lijst.
10. Inschrijving op onderzoeken beheren 🎨🖥🗄 (🚀 Medium)
•	Ervaringsdeskundigen kunnen zich inschrijven op onderzoeken.
•	Beheerder moet deelname goedkeuren.
11. Zelf uitschrijven uit een onderzoek 🎨🖥🗄 (⏳ Laag)
•	Ervaringsdeskundigen moeten hun inschrijving kunnen annuleren.
•	Beheerder moet uitschrijving goedkeuren.
________________________________________
🔹 Beheerdersportal
12. Dashboard voor goedkeuringen (real-time updates) 🎨🖥🔗 (🏆 Hoog)
•	Beheerders zien in één overzicht: 
o	Goed te keuren onderzoeksaanvragen.
o	Nieuw geregistreerde ervaringsdeskundigen.
o	Goed te keuren inschrijvingen.
•	AJAX updates zorgen ervoor dat wijzigingen direct zichtbaar zijn.
13. Zoek- en filterfunctionaliteit voor lijsten 🎨🖥🗄 (🚀 Medium)
•	Beheerders moeten snel specifieke gebruikers en onderzoeken kunnen vinden.
•	Zoekfunctionaliteit in lijsten.
________________________________________
🔹 API Functionaliteit
14. API Authenticatie met API-sleutel 🔗🔐 (🏆 Hoog)
•	Organisaties krijgen een API-sleutel bij goedkeuring.
•	Sleutel wordt gebruikt voor API-verzoeken.
15. API - Onderzoeken beheren 🔗🖥🗄 (🚀 Medium)
•	Organisaties kunnen onderzoeken aanmaken en beheren via de API.
•	Alleen basisvelden mogen gewijzigd worden na goedkeuring.
16. API - Ingeschreven ervaringsdeskundigen ophalen 🔗🖥🗄 (🚀 Medium)
•	Organisaties kunnen de goedgekeurde deelnemers van een onderzoek ophalen via de API.
________________________________________
🔹 Security & Accessibility
17. WCAG 2.2 - AA naleving 🎨♿ (🚀 Medium)
•	Toegankelijkheid verbeteren voor schermlezers en navigatie via toetsenbord.
•	Dynamische contrastopties voor kleuren.
18. Formulier Validatie met JavaScript 🎨🖥 (🚀 Medium)
•	Controleer invoer direct (bijvoorbeeld verplichte velden).
19. Gegevensbeveiliging (RBAC, SQL Injections, CSRF) 🔐🖥 (🏆 Hoog)
•	Role-Based Access Control (RBAC) instellen.
•	SQL-injecties en CSRF voorkomen.
________________________________________
🔹 Extra Wenselijke Features
20. Notificatiesysteem (E-mail bij statuswijzigingen) 🖥🔗 (⏳ Laag)
•	Notificaties sturen naar organisaties en ervaringsdeskundigen.
21. Portal voor organisaties (CRUD UI) 🎨🖥 (⏳ Laag)
•	Een dashboard waarin organisaties hun onderzoeken kunnen beheren.
________________________________________

