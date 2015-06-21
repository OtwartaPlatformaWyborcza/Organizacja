# System OPW 
Otwarta Platforma Wyborcza (OPW) to oprogramowanie klasy enterprise, którego podstawowym zadaniem jest niezależna i obiektywna weryfikacja wyników wyborów.  
Celem projektu OPW nie jest kompletna implementacja wymagań sprecyzowanych przez PKW w ramach projektu PW2 (Platforma Wyborcza 2). 

# Architektura
System OPW składa się z następujących, wpełni niezależnych modułów.

| Moduł | prefix | Kommentarz |
| ------------- | ------------- | ------------- |
| Referendum | `ref` | Referendum ogólnokrajowe | 
| Prezydenckie  | `pre` | Wybory prezydenckie |
| Parlamentarne  | `par` | Wybory parlamentarne (Sejm i Senat) |
| Unia Europejska  | `eu` | ? |

Poszczególne moduły są zdefiniowanie jako pakiety wewnątrz `pl.otwartapw.opw`.

## Moduł PRE
Moduł dedykowany do obsługi Wyborów prezydenckich. 

### Artefakty

| Artefakt | Paczki | Kommentarz |
| ------------- | ------------- | ------------- |
| opw-pre-base | `.entity` `.bean` `.api` | JPA, API |
| opw-pre-managemet | `.view` `.dto` `.controller` | Maski administracyjne (JSF 2.2) |
| opw-pre-register | `.view` `.dto` `.controller` | Formularz rejestracji wolontariusza (JSF 2.2) |
| opw-pre-ws-import | `.service` `.dto` `.controller` | Serwis importu - zapis do bazy danych | 
| opw-pre-ws-export | `.service` `.dto` `.controller` | Serwis eksportu - odczyt bazy danych |
| opw-pre-ws-managemet | `.service` `.dto` `.controller` | Serwis administracyjny |
| opw-pre-ws-register | `.service` `.dto` `.controller` | Serwis rejestracji |

### Struktura pakietów (backend)
`pl.otwartapw.opw.pre.api`  
`pl.otwartapw.opw.pre.bean`  
`pl.otwartapw.opw.pre.entity`  
`pl.otwartapw.opw.pre.management.controller`  
`pl.otwartapw.opw.pre.management.dto`  
`pl.otwartapw.opw.pre.management.handler`  
`pl.otwartapw.opw.pre.register`  
`pl.otwartapw.opw.pre.ws.import`  
`pl.otwartapw.opw.pre.ws.export`  
`pl.otwartapw.opw.pre.ws.management`  
`pl.otwartapw.opw.pre.ws.register`  

### Aplikacje klienckie 
`opw-client-obwodowa-angularjs`  
`opw-client-dashboard-jquery`  

