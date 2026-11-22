# Završni rad za Python cjelinu

- ***ETL pipeline*** za obradu podataka o prodaji i rezultata utakmica.

- Pregleda toka koda:
    
1. **Ekstrakcija** - preuzimanje podataka za obradu (smješteni na putanji data/raw):

    + matches.parquet
    + orders.json
    + products.csv
    + teams.csv

2. **Transformacija** - obrada preuzetih podataka:

    + čišćenje i standardizacija podataka
    + uklanjanje duplikata
    + računanje transakcija
    + kreiranje tabele lige

3. **Učitavanje** - upisivanje izlaznih podataka (smješteni na putanji data/processed):

    + clean_orders.parquet
    + league_table.csv
    + products.csv
    + rejected_orders.csv
    + revenue_by_category.csv
    + revenue_by_team.csv
    + sales_after_results.csv
    + summary.csv



- Uticaj rezultata na prihode klubova

|  Rezultat   | Broj dana |   Zarada   | Dnevni prosjek |
|-------------|-----------|------------|----------------|
|    none     |    954    |  4427150.0 |     4640.62    | 
|      W      |    339    |  2999230.0 |     8847.29    |
|      D      |    228    |  1180180.0 |     5176.23    |
|      L      |    339    |  1012330.0 |     2986.22    |

*none predstavlja dane kada nije bilo utakmica

- Iz datih rezultata moguće je zaključliti da su klubovi imali skoro duplo veću zaradu u danima nakon pobjede nego u danima bez utakmica.
- Izjednačenja su blago uticala na povećanje prihoda u odnosu na dane bez utakmice
- Dok su gubici imali negativan uticaj na prodaju.