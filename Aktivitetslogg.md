# Projekt Dokumentation - Vecka 44

## Aktivitetsdiagram

- **Beskrivning**: Här är en skärmdump av aktivitetsdiagrammet som visualiserar flödet för både administratör och kund.
- **Skärmdump**:
[Aktivitetsdiagram]![github com_Younes-nackademin_ActivityDiagrams_blob_main_ActivityNYA_diagrams md (3)](https://github.com/user-attachments/assets/19b8ac3f-804e-44dc-b030-b1046d68206f)


*Beskrivning:* Aktivitetsdiagrammet visar inloggning, orderhantering, lagerstatus och betalningsprocesser för administratören, samt flöden för kundens köp och orderbekräftelse.

---

## User Stories

### User Story 1: Lägga till produkt i varukorgen
- **User Story**: Som användare vill jag kunna lägga till en produkt i min varukorg så att jag kan samla produkter jag är intresserad av att köpa.

- **Beskrivning**: Användaren ska kunna klicka på en knapp för att lägga till produkter i sin varukorg.

- **Skärmdump**:
[Lägg till i varukorgen]![1](https://github.com/user-attachments/assets/2b56a16d-033b-4cbb-9885-79f51b734f91)


*Beskrivning:* Denna bild visar knappen "Lägg till i varukorgen" på produktsidan.

---

### User Story 2: Slutföra köp från varukorgen
- **User Story**: Som användare vill jag kunna slutföra ett köp av produkter i min varukorg så att jag kan genomföra en beställning.

- **Beskrivning**: Användaren ska kunna gå från varukorgen till en sida för att ange betalningsinformation och slutföra köpet.

- **Skärmdump**:
[Köp från varukorgen]![2](https://github.com/user-attachments/assets/c80c5cd5-0fc3-4179-990d-1be3e9c9cab0)


*Beskrivning:* Denna bild visar betalningssidan där användaren anger betalningsinformation.

---

### User Story 3: Skapa konto
- **User Story**: Som ny användare vill jag kunna skapa ett konto så att jag kan spara mina uppgifter för framtida köp och spåra mina beställningar.

- **Beskrivning**: En ny användare ska kunna registrera sig genom att ange sina uppgifter och skapa ett konto.

- **Skärmdump**:
[Registreringssidan]![3](https://github.com/user-attachments/assets/5051b358-4b15-42a8-a865-0d73a385fe92)


*Beskrivning:* Denna bild visar registreringsformuläret för att skapa ett konto.

---

### User Story 4: Se orderhistorik
- **User Story**: Som användare vill jag kunna se min orderhistorik så att jag kan granska mina tidigare beställningar.

- **Beskrivning**: En inloggad användare ska kunna se en lista över sina tidigare beställningar.

- **Skärmdump**:
[Orderhistorik]![4](https://github.com/user-attachments/assets/23463140-9853-4fc3-8cbb-9e97c1d79849)


*Beskrivning:* Denna bild visar orderhistorikssidan för användaren.

---

### User Story 5: Glömt lösenord
- **User Story**: Som användare vill jag kunna återställa mitt lösenord om jag har glömt det, så att jag kan logga in på mitt konto igen.

- **Beskrivning**: Användaren ska kunna återställa sitt lösenord genom att ange sin e-postadress.

- **Skärmdump**:
[Återställ lösenord]![5](https://github.com/user-attachments/assets/0eb47e17-ee9e-4c46-9467-74fcc3ff031c)


*Beskrivning:* Denna bild visar sidan för att återställa lösenordet.

---

## Vecka 45

### Sekvensdiagram

- **Beskrivning**: Under denna vecka har jag skapat och dokumenterat två sekvensdiagram för att tydligt illustrera flödet av kundens orderläggning och betalningsprocess samt administratörens orderhantering i systemet.

- **Sekvensdiagram 1**: Kundens orderläggnings- och betalningsflöde  
   - Diagrammet visar kundens interaktioner med systemet, från inloggning och sökning av produkter, till betalning och orderbekräftelse. Diagrammet inkluderar även externa system som lagerhantering och betalningstjänst för att illustrera de olika stegen i flödet.

- **Sekvensdiagram 2**: Administratörens orderhanteringsflöde  
   - Detta diagram visar administratörens flöde för att logga in, visa ordrar, uppdatera orderstatus och generera rapporter. Sekvensdiagrammet inkluderar interaktioner mellan systemet och lagersystemet för att säkerställa att lagerstatusen uppdateras korrekt vid varje order.

- **Dokumentation och metod**:  
   - Jag har använt Mermaid-syntax för att skapa sekvensdiagrammen och inkluderat både en visuell representation samt källkoden i dokumentationen. Diagrammen är granskade för att säkerställa att de stämmer överens med user stories och aktivitetsdiagram för att ge en tydlig bild av systemets interaktioner.

- **Skärmdump**:  
   ![Sekvensdiagram](https://github.com/user-attachments/assets/c3012cab-a300-484d-8ae4-be407e1df42c)  
   *Beskrivning:* Bilden visar de två sekvensdiagrammen, där kundens orderläggnings- och betalningsflöde samt administratörens orderhanteringsflöde visualiseras för att ge en tydlig bild av systemets interaktioner.


---

![github com_Younes-nackademin_ActivityDiagrams_blob_main_TDD-baserade%20tester md (1)](https://github.com/user-attachments/assets/f3e862ba-296f-4530-a44f-e86b0cb002dd)


---

# Aktivitetslogg: Visual Studio Vecka 44-46

---

## Vecka 44
- **Skapade projektet AccountProvider:**  
  Jag startade ett nytt projekt i Visual Studio och lade upp en struktur med lager för modeller, tester och databas.  
- **Dokumenterade användarberättelser:**  
  Jag skrev användarberättelser för att beskriva hur systemet hanterar produkter och ordrar.  
- **Ritade aktivitetsdiagram och sekvensdiagram:**  
  Jag ritade aktivitetsdiagram och sekvensdiagram för att visa flödet för både kunder och administratörer.

---

## Vecka 45
- **Skrev enhetstester för Product-klassen:**  
  Jag använde TDD (Test-Driven Development) och skrev tester för `Product`-klassen innan jag implementerade funktionaliteten.  
- **Kopplade projektet till databasen:**  
  Jag kopplade projektet till databasen med hjälp av Entity Framework. Jag använde DbContext för att koppla mina klasser till tabeller i databasen och skapade databasen med migreringar. Jag debuggar också problem, som när connection strings var fel eller när data inte sparades rätt.  
- **Skapade ett Order Repository:**  
  Jag skapade ett repository för att hantera ordrar i databasen och lade till funktioner för att skapa, läsa och uppdatera ordrar.

---

## Vecka 46
- **Slutförde projektet:**  
  Jag säkerställde att alla funktioner var implementerade och att testerna passerade utan fel.  
- **Följde designprinciper:**  
  Jag arbetade enligt TDD och följde SOLID-principer för att hålla koden enkel, lätt att ändra och välstrukturerad.  

---



# Aktivitetslogg: Vecka 44-46

#### Grupparbete och planering
- Jag och gruppen använde **Jira** för att planera och hålla koll på våra uppgifter.
- Vi samarbetade och såg till att allt blev klart i tid.
