## User Story 3: Skapa konto

- **User Story**: Som ny användare vill jag kunna skapa ett konto så att jag kan spara mina uppgifter för framtida köp och spåra mina beställningar.

- **Beskrivning**: En ny användare ska kunna registrera sig genom att ange sina uppgifter och skapa ett konto. Efter registreringen ska användaren kunna logga in med sina nya inloggningsuppgifter.

- **Acceptanskriterier**:
  - Användaren kan fylla i ett registreringsformulär med personliga uppgifter (t.ex. namn, e-post, lösenord).
  - Systemet validerar att alla obligatoriska fält är ifyllda och att e-post och lösenord är i korrekt format.
  - Användaren får en bekräftelse på att kontot skapats och kan logga in.

- **Aktiviteter**:
  - Skapa en registreringssida med nödvändiga fält.
  - Implementera servervalidering för att säkerställa att e-post och lösenord är giltiga.
  - Spara användaruppgifter i databasen och visa en bekräftelse.

- **Testfallsbeskrivningar**:
  - Testfall 1: Kontrollera att användaren kan fylla i och skicka in registreringsformuläret.
  - Testfall 2: Kontrollera att valideringsmeddelanden visas om obligatoriska fält är tomma eller felaktiga.
  - Testfall 3: Kontrollera att användaren kan logga in efter att kontot har skapats.

---
