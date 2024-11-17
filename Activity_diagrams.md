```mermaid
graph TD;

%% Administratörens inloggnings- och orderhanteringsprocess
A[Administratör loggar in] --> B{Lyckad inloggning?}
B -->|Ja| C[Visa adminpanel med notiser och statistik]
B -->|Nej| D[Felmeddelande: Inloggning misslyckades]

%% Utökade funktioner i adminpanelen
C --> E[Se alla ordrar och använd filter]
C --> F[Generera rapporter]
C --> G[Hantera användarkonton]
C --> H[Visa lagerstatus och hantera lager]

%% Orderhantering
E --> E1[Se orderdetaljer]
E --> E2[Uppdatera orderstatus]
E --> E3[Lägg till intern kommentar]
E1 --> E4[Visa orderhistorik]
E2 --> E5[Automatisk lageruppdatering]
E3 --> E6[Flagga order för uppföljning]

%% Rapportgenerering med felhantering
F --> F1[Välj rapporttyp: försäljning, lager, leverans]
F1 --> F2[Generera PDF eller Excel-rapport]
F2 --> F3{Lyckades rapportgenerering?}
F3 -->|Ja| F4[Skicka rapport till ansvarig]
F3 -->|Nej| F5[Felmeddelande: Rapportgenerering misslyckades]

%% Användarhantering med felhantering
G --> G1[Lägg till ny användare]
G --> G2[Uppdatera användarinformation]
G --> G3[Ta bort användare]
G1 --> G4{Lyckades användaruppdatering?}
G4 -->|Ja| G5[Notis: Användare tillagd]
G4 -->|Nej| G6[Felmeddelande: Kunde inte lägga till användare]

%% Lagerhantering
H --> H1[Visa aktuell lagerstatus]
H --> H2[Lägg till nya produkter i lager]
H --> H3[Uppdatera produktinformation]
H1 --> H4{Låg lagerstatus?}
H4 -->|Ja| H5[Skicka notis om låg lagerstatus]

%% Kundens orderläggnings- och betalningsprocess
I[Kund loggar in] --> J[Söker produkter]
J --> K[Lägger produkter i varukorgen]
K --> L{Är varukorgen tom?}
L -->|Ja| J
L -->|Nej| M[Bekräftar order]
M --> N[Får orderbekräftelse]

%% Kundens betalningsprocess med Klarna-alternativ
N --> O[Gå till varukorgen]
O --> P[Välj betalningsmetod]
P --> Q{Välj betalningstyp?}

Q -->|Kreditkort| R[Fyll i kreditkortsinformation]
Q -->|Swish| S[Skanna Swish QR-kod]
Q -->|Faktura| T[Fyll i fakturainformation]
Q -->|Klarna| U[Välj Klarna-alternativ]

R --> V[Verifiera betalning]
S --> V
T --> V
U --> V

V --> W{Betalning godkänd?}
W -->|Ja| X[Orderbekräftelse skickad]
W -->|Nej| Y[Felmeddelande: Betalning misslyckades]

X --> Z[Slutförd order]
Z --> AA[Kund kan se orderhistorik]
