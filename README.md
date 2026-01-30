# Intranet Ticketing System (ASP.NET WebForms)

Interni tiketing sistem za prijavu i obradu zahteva zaposlenih. Sadrži **user portal** (kreiranje i praćenje tiketa) i **admin panel** (dodela, statusi, notifikacije).
  
## Tehnologije
- ASP.NET WebForms (C#), .NET Framework
- MS SQL (osTicket-inspirisana šema: `ts_*` tabele)
- Windows autentifikacija + LDAP
- SMTP email notifikacije

## Funkcionalnosti
- Kreiranje, filtriranje i praćenje tiketa (user deo)
- Dodela agenata, promene statusa i komentari (admin deo)
- Email obaveštenja (Outlook/SMTP)
- Validacija unosa, logovanje i osnovna statistika

## Podešavanje okruženja
1. **Baza**: pokrenite `docs/setup-database.sql` (lokalni SQL Server)  
2. **Konekcija**: u `web.config` zamenite placeholder-e:
   ```xml
   <connectionStrings>
     <add name="TicketDb"
       connectionString="Data Source=__SERVER__;Initial Catalog=__DB__;User Id=__USER__;Password=__PASS__;" />
   </connectionStrings>
