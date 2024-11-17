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
