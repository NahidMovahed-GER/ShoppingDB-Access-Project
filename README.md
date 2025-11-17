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
Die Datenbank zeigt, wie man einen echten, ungeordneten Datensatz in ein sauberes relationales Datenmodell überführt.  
Damit wird das Arbeiten mit Abfragen, Berichten und Analysen deutlich einfacher.

## Erweiterungen
Das Projekt wird später erweitert, unter anderem um:

- Beispielabfragen (SQL & Design View)  
- Formulare  
- Reports  
- Kleine Analysen zur Einkaufsstatistik  

## Quelle
Datensatz: **Kaggle – Shopping Trends Dataset**  
(Öffentlich verfügbar für Analyse- und Lernzwecke.)

## Nutzung
1. Access-Datei öffnen  
2. Tabellen oder Abfragen auswählen  
3. Beziehungen unter „Database Tools → Relationships“ ansehen  
4. Eigene Auswertungen erstellen

ShoppingDB
```
/
├─ README.md                     # Erklärung des Projekts
├─ ShoppingDB.accdb             # Access-Datenbank
├─ data/
│  └─ shopping_trends.csv       # Original-Datensatz von Kaggle
├─ docs/
│  ├─ schema_relationships.png  # Screenshot Relationships-Fenster

```

