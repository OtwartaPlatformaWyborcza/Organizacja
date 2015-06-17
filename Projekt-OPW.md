# System OPW 
Otwarta Platforma Wyborcza

# Moduły
Wszelkie moduły są zdefiniowanie jako pakiety wewnątrz `pl.otwartapw.opw`.

 

| Moduł | prefix | Kommentarz |
| ------------- | ------------- | ------------- |
| Referendum | `ref` | Referendum ogólnokrajowe | 
| Prezydenckie  | `pre` | Wybory prezydenckie |
| Parlamentarne  | `par` | Wybory parlamentarne (Sejm i Senat) |
| Unia Europejska  | `eu` | ? |


Przykładowa struktura pakietów dla modułu `PRE`  
`pl.otwartapw.opw.pre.entity`  
`pl.otwartapw.opw.pre.bean`  
`pl.otwartapw.opw.pre.management.controller`  
`pl.otwartapw.opw.pre.management.dto`  
`pl.otwartapw.opw.pre.management.handler`  
`pl.otwartapw.opw.pre.register`  
`pl.otwartapw.opw.pre.ws.import`  
`pl.otwartapw.opw.pre.ws.export`  
`pl.otwartapw.opw.pre.ws.management`  
`pl.otwartapw.opw.pre.ws.register`  


Podział na artefakty na przykładzie `PRE`. 


| Artefakt | Paczki | Kommentarz |
| ------------- | ------------- | ------------- |
| opw-pre-base | `.entity` `.bean` `.api` | JPA, API |
| opw-pre-managemet | `.view` `.dto` `.controller` | Maski administracyjne (JSF 2.2) |
| opw-pre-register | `.view` `.dto` `.controller` | Formularz rejestracji wolontariusza (JSF 2.2) |
| opw-pre-ws-import | `.service` `.dto` `.controller` | Serwis importu - zapis do bazy danych | 
| opw-pre-ws-export | `.service` `.dto` `.controller` | Serwis eksportu - odczyt bazy danych |
| opw-pre-ws-managemet | `.service` `.dto` `.controller` | Serwis administracyjny |
| opw-pre-ws-register | `.service` `.dto` `.controller` | Serwis rejestracji |
