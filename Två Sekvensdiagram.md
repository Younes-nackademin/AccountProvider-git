![Skärmbild (119)](https://github.com/user-attachments/assets/c3012cab-a300-484d-8ae4-be407e1df42c)

Sekvensdiagram

 Kundens orderläggnings- och betalningsflöde
    participant Kund
    participant System
    participant Betalningstjänst
    participant Lager

    Kund->>System: Logga in
    System-->>Kund: Bekräftelse på inloggning
    Kund->>System: Söker och lägger till produkt i varukorgen
    System->>Lager: Kontrollera lagersaldo
    Lager-->>System: Bekräfta tillgänglighet
    Kund->>System: Gå till varukorgen och välj betalningsmetod
    System->>Betalningstjänst: Skicka betalningsuppgifter
    Betalningstjänst-->>System: Bekräfta betalning
    System-->>Kund: Orderbekräftelse skickad
    System->>Lager: Uppdatera lagerstatus

 Administratörens orderhanteringsflöde
    participant Administratör
    participant System
    participant Lager

    Administratör->>System: Logga in
    System-->>Administratör: Bekräftelse på inloggning
    Administratör->>System: Visa alla ordrar
    System-->>Administratör: Lista med ordrar
    Administratör->>System: Uppdatera orderstatus
    System->>Lager: Uppdatera lagersaldo
    Lager-->>System: Bekräftelse på uppdatering
    Administratör->>System: Generera rapport
    System-->>Administratör: Rapport skapad
