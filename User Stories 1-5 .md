## User Story 1: Lägga till produkt i varukorgen

- **User Story**: Som användare vill jag kunna lägga till en produkt i min varukorg så att jag kan samla produkter jag är intresserad av att köpa.

- **Beskrivning**: Användaren ska kunna klicka på en knapp för att lägga till produkter i sin varukorg. Efter att produkten är tillagd ska användaren kunna fortsätta handla eller gå till varukorgen för att se sina valda produkter.

- **Acceptanskriterier**:
  - Användaren kan lägga till en eller flera produkter i varukorgen.
  - Produkten sparas i varukorgen även om användaren navigerar till andra sidor.
  - Användaren kan se en uppdaterad total summa för produkterna i varukorgen.

- **Aktiviteter**:
  - Skapa en knapp "Lägg till i varukorgen" på produktsidan.
  - Implementera en funktion som lägger till produkten i varukorgen och uppdaterar totalsumman.
  - Visa en indikator eller meddelande för att bekräfta att produkten har lagts till i varukorgen.

- **Testfallsbeskrivningar**:
  - Testfall 1: Kontrollera att produkten visas i varukorgen när användaren klickar på "Lägg till i varukorgen".
  - Testfall 2: Kontrollera att totalsumman uppdateras korrekt när en ny produkt läggs till.
  - Testfall 3: Kontrollera att produkten förblir i varukorgen om användaren navigerar bort från sidan och sedan återvänder.

---

## User Story 2: Slutföra köp från varukorgen

- **User Story**: Som användare vill jag kunna slutföra ett köp av produkter i min varukorg så att jag kan genomföra en beställning.

- **Beskrivning**: Användaren ska kunna gå från varukorgen till en sida för att ange betalningsinformation och slutföra köpet. Efter att betalningen har genomförts ska användaren få en orderbekräftelse.

- **Acceptanskriterier**:
  - Användaren kan navigera från varukorgen till betalningssidan.
  - Användaren kan ange betalningsuppgifter och bekräfta sin betalning.
  - Användaren får en orderbekräftelse efter att köpet är genomfört.

- **Aktiviteter**:
  - Skapa en knapp "Till betalning" i varukorgen som leder till betalningssidan.
  - Implementera formulärfält för att samla in betalningsuppgifter.
  - Skapa en funktion som bearbetar betalningen och visar en orderbekräftelse.

- **Testfallsbeskrivningar**:
  - Testfall 1: Kontrollera att användaren kan navigera från varukorgen till betalningssidan.
  - Testfall 2: Kontrollera att betalningsuppgifterna valideras korrekt.
  - Testfall 3: Kontrollera att en orderbekräftelse visas när betalningen är godkänd.

---

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

## User Story 4: Se orderhistorik

- **User Story**: Som användare vill jag kunna se min orderhistorik så att jag kan granska mina tidigare beställningar.

- **Beskrivning**: En inloggad användare ska kunna se en lista över sina tidigare beställningar, inklusive information om beställda produkter, belopp och status.

- **Acceptanskriterier**:
  - Användaren kan navigera till en orderhistoriksida från sin profil.
  - Orderhistoriksidan visar en lista över tidigare beställningar med datum, produktinformation, och orderstatus.
  - Användaren kan se detaljerad information om en specifik beställning.

- **Aktiviteter**:
  - Skapa en orderhistoriksida som hämtar tidigare beställningar från databasen.
  - Implementera en funktion för att visa detaljer om varje beställning.
  - Lägg till en navigationslänk till orderhistoriken från användarens profil.

- **Testfallsbeskrivningar**:
  - Testfall 1: Kontrollera att en inloggad användare kan se sin orderhistorik.
  - Testfall 2: Kontrollera att orderhistoriken visar korrekt information för varje beställning.
  - Testfall 3: Kontrollera att användaren kan öppna och se detaljer för en specifik beställning.

---

## User Story 5: Glömt lösenord

- **User Story**: Som användare vill jag kunna återställa mitt lösenord om jag har glömt det, så att jag kan logga in på mitt konto igen.

- **Beskrivning**: Användaren ska kunna återställa sitt lösenord genom att ange sin e-postadress. Systemet skickar då en återställningslänk till användarens e-postadress.

- **Acceptanskriterier**:
  - Användaren kan ange sin e-postadress för att begära en återställning av lösenordet.
  - Systemet skickar ett e-postmeddelande med en återställningslänk.
  - Användaren kan ange ett nytt lösenord via återställningslänken och logga in med det nya lösenordet.

- **Aktiviteter**:
  - Skapa ett formulär där användaren kan ange sin e-postadress för lösenordsåterställning.
  - Implementera funktionalitet för att skicka återställningslänken till användarens e-post.
  - Skapa en sida för att ange ett nytt lösenord när användaren klickar på återställningslänken.

- **Testfallsbeskrivningar**:
  - Testfall 1: Kontrollera att användaren kan skicka en begäran om lösenordsåterställning.
  - Testfall 2: Kontrollera att ett e-postmeddelande skickas till användaren med återställningslänken.
  - Testfall 3: Kontrollera att användaren kan ange ett nytt lösenord via återställningslänken och logga in.

---

## Skärmdump av Aktivitetsdiagram

Här är en skärmdump av aktivitetsdiagrammet som visualiserar flödet för både administratör och kund:

[Aktivitetsdiagram]![github com_Younes-nackademin_ActivityDiagrams_blob_main_ActivityNYA_diagrams md (3)](https://github.com/user-attachments/assets/7c48d78f-337a-4ada-a2b1-285f48aaf963)

*Beskrivning:* Aktivitetsdiagrammet visar inloggning, orderhantering, lagerstatus och betalningsprocesser för administratören, samt flöden för kundens köp och orderbekräftelse. Diagrammet omfattar även betalningsalternativet Klarna.
