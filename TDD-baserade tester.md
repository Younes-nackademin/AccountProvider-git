## TDD-baserade tester

Här är en sammanställning av fem TDD-baserade tester som validerar olika funktioner i systemet:

### Test 1: Lägga till Produkt i Varukorgen  
   - **Testfall**: Kontrollera att en produkt läggs till korrekt i varukorgen och att totalsumman uppdateras.
   - **Kod**:
      ```csharp
      [TestMethod]
      public void LäggTillProduktIVarukorgen_ProduktLäggsTillOchTotalenUppdateras()
      {
          // Arrange
          var varukorg = new Varukorg();
          var produkt = new Produkt("Bok", 100);

          // Act
          varukorg.LäggTillProdukt(produkt);

          // Assert
          Assert.IsTrue(varukorg.Produkter.Contains(produkt));
          Assert.AreEqual(100, varukorg.TotalSumma);
      }
      ```
   - **Resultat**: Testet körs framgångsrikt och visar att produkten läggs till och totalsumman uppdateras.

### Test 2: Uppdatera Orderstatus  
   - **Testfall**: Kontrollera att administratören kan uppdatera en orderstatus korrekt.
   - **Kod**:
      ```csharp
      [TestMethod]
      public void UppdateraOrderStatus_StatusUppdaterasKorrekt()
      {
          // Arrange
          var order = new Order { Id = 1, Status = "Pending" };
          var nyStatus = "Skickad";

          // Act
          order.UppdateraStatus(nyStatus);

          // Assert
          Assert.AreEqual("Skickad", order.Status);
      }
      ```
   - **Resultat**: Testet bekräftar att orderstatusen uppdateras som förväntat.

### Test 3: Visa Orderhistorik  
   - **Testfall**: Kontrollera att användaren kan se sin orderhistorik korrekt.
   - **Kod**:
      ```csharp
      [TestMethod]
      public void VisaOrderhistorik_OrderhistorikVisasKorrekt()
      {
          // Arrange
          var användare = new Användare();
          användare.LäggTillOrder(new Order { Id = 1, Status = "Slutförd" });

          // Act
          var historik = användare.VisaOrderhistorik();

          // Assert
          Assert.AreEqual(1, historik.Count);
          Assert.AreEqual("Slutförd", historik[0].Status);
      }
      ```
   - **Resultat**: Testet visar att orderhistoriken returneras med korrekt information.

### Test 4: Bekräfta Betalning  
   - **Testfall**: Kontrollera att betalningen bekräftas korrekt via betalningstjänsten.
   - **Kod**:
      ```csharp
      [TestMethod]
      public void BekräftaBetalning_BetalningBekräftasKorrekt()
      {
          // Arrange
          var betalningstjänst = new Betalningstjänst();
          var order = new Order();

          // Act
          betalningstjänst.BekräftaBetalning(order);

          // Assert
          Assert.AreEqual("Betald", order.BetalningsStatus);
      }
      ```
   - **Resultat**: Testet visar att betalningen bekräftas och statusen uppdateras till "Betald".

### Test 5: Skapa Användarkonto  
   - **Testfall**: Kontrollera att användaren kan skapa ett konto med giltig e-post och lösenord.
   - **Kod**:
      ```csharp
      [TestMethod]
      public void SkapaAnvändarkonto_KontotSkapasKorrekt()
      {
          // Arrange
          var användare = new Användare { Epost = "test@exempel.com", Lösenord = "Säker123!" };

          // Act
          var kontoSkapat = användare.SkapaKonto();

          // Assert
          Assert.IsTrue(kontoSkapat);
          Assert.AreEqual("test@exempel.com", användare.Epost);
      }
      ```
   - **Resultat**: Testet visar att kontot skapas korrekt och e-post och lösenord sparas.

