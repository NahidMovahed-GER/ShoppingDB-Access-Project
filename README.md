# ShoppingDB – Access Datenbankprojekt

Dieses Projekt nutzt einen echten Datensatz aus **Kaggle** („Shopping Trends Dataset“).  
Die Excel-Datei wurde importiert und anschließend in eine saubere Access-Datenbank-Struktur umgewandelt.

Die ursprüngliche Tabelle (`Shopping_trends`) wurde in drei logisch getrennte Tabellen aufgeteilt:

- **Customer** – Kundendaten  
- **Product** – Artikeldaten  
- **Orders** – Bestellungen  

Die Tabellen sind über Fremdschlüssel miteinander verbunden:

- CustomerID → Orders  
- ProductID → Orders  

Dadurch entsteht eine übersichtliche und normalisierte Datenbank.

## Inhalte der Datenbank

### **Customer**
- CustomerID (AutoNumber)
- Age  
- Gender  
- Location  
- Subscription Status  
- Review Rating  

### **Product**
- ProductID (AutoNumber)
- ProductName  
- Category  
- Size  
- Color  
- Season  

### **Orders**
- OrderID (AutoNumber)
- CustomerID  
- ProductID  
- PurchaseAmount  
- PaymentMethod  
- ShippingType  
- ReviewRating  
- Subscription  
- Quantity  
- OrderDate  

## Ziel des Projekts
- Arbeiten mit echten Daten
- Normalisierung in separate Tabellen
- Erstellen von Joins und Analysen
- Formulare für Benutzer
- Automatisierung (Import + Logging + Export)

Dieses Projekt eignet sich perfekt als Beispiel für:
### Datenbankentwicklung, Access-Automatisierung, SQL-Analyse und Datenmigration.

## Funktionen des Projekts
### Automatischer Import neuer Kunden

- Neue Einträge aus shopping_trends_updated.csv
- Abgleich per CustomerID
- Nur neue Kunden werden übernommen
- Ergebnis erscheint in einer Meldung
- Ein Eintrag wird im MigrationLog gespeichert

### Wichtige Abfragen

Alle Abfragen laufen direkt in Access:
- qry_NewCustomers
- qry_AppendNewCustomers
- qry_UmsatzProKunde
- qry_UmsatzNachSubscription
- qry_UmsatzNachStandort
Screenshots der Ergebnisse befinden sich im Ordner docs/.

### Export-Funktion

Die Analyse „Umsatz nach Standort“ wird per Button in eine Excel-Datei exportiert.

## Quelle
Datensatz: **Kaggle – Shopping Trends Dataset**  
(Öffentlich verfügbar für Analyse- und Lernzwecke.)

## Nutzung
1. Access-Datei öffnen  
2. Tabellen oder Abfragen auswählen  
3. Beziehungen unter „Database Tools → Relationships“ ansehen  
4. Eigene Auswertungen erstellen

ShoppingDB
```/

│
├─ data/                         # Original- und Update-Datensatz
│   ├─ shopping_trends.csv
│   └─ shopping_trends_updated.csv
│
├─ docs/
│   ├─ forms/                    # Screenshots der Formulare
│   ├─ logs/                     # Screenshots der Log-Tabelle
│   ├─ queries/                  # Screenshots der Abfragen
│   └─ exports/                  # Export-Dateien (Excel)
│
├─ src/
│   └─ ShoppingDB.accdb          # Die Access-Datenbank
│
└─ README.md
```
## Screenshots

Screenshots befinden sich im Ordner docs/:
- Hauptmenü
- Import-Erfolgs-Meldung
- MigrationLog-Tabelle
- Alle wichtigen Abfragen
- Export-Datei im Explorer







