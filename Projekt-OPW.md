# System OPW
Otwarta Platforma Wyborcza (OPW) to oprogramowanie klasy enterprise, którego podstawowym zadaniem jest niezależna i obiektywna weryfikacja wyników wyborów.  
Celem projektu OPW nie jest kompletna implementacja wymagań sprecyzowanych przez PKW w ramach projektu PW2 (Platforma Wyborcza 2).

# Architektura
System OPW składa się z następujących, wpełni niezależnych modułów.

| Akcja wyborcza | Moduł | Kommentarz |
| ------------- | ------------- | ------------- | ------------- |
| Referendum | `ref` | Referendum ogólnokrajowe |
| Prezydenckie  | `pre` |  Wybory prezydenckie |
| Parlamentarne  | `par` | Wybory parlamentarne (Sejm i Senat) |
| Unia Europejska  | `eu` | ? |

Poszczególne moduły są zdefiniowanie jako pakiety wewnątrz `pl.otwartapw.opw`.

## Moduł PRE
Dedykowany moduł do obsługi wyborów prezydenckich.

### Artefakty

| Nazwa | Typ | Kommentarz |
| ------------- | ------------- | ------------- |
| opw-pre-base | war | JPA, API |
| opw-pre-managemet |  | Maski administracyjne (JSF 2.2) |
| [opw-pre-register](https://github.com/OtwartaPlatformaWyborcza/opw-pre-register) | war | Formularz rejestracji wolontariusza (JSF 2.2) |
| opw-pre-ws-inbound | war | Serwis importu - zapis do bazy danych |
| opw-pre-ws-outbound | war | Serwis eksportu - odczyt bazy danych |
| opw-pre-ws-managemet | war | Serwis administracyjny |
| [opw-pre-ws-register](https://github.com/OtwartaPlatformaWyborcza/opw-pre-ws-register) | war | Serwis rejestracji |
| [opw-pre-ws-register-model](https://github.com/OtwartaPlatformaWyborcza/opw-pre-ws-register-model) | jar | Definicja API, walidacja jak i klasy DTO.  |

### Struktura pakietów (backend)
`pl.otwartapw.opw.pre.api`  
`pl.otwartapw.opw.pre.bean`  
`pl.otwartapw.opw.pre.entity`  
`pl.otwartapw.opw.pre.management.controller`  
`pl.otwartapw.opw.pre.management.dto`  
`pl.otwartapw.opw.pre.management.handler`  
`pl.otwartapw.opw.pre.register`  
`pl.otwartapw.opw.pre.ws.inbound`  
`pl.otwartapw.opw.pre.ws.outbound`  
`pl.otwartapw.opw.pre.ws.management`  
`pl.otwartapw.opw.pre.ws.register`  

### Aplikacje klienckie
`opw-client-obwodowa-angularjs`  
`opw-client-dashboard-jquery`  


## Moduł REF
Dedykowany moduł do obsługi referendum.

### Artefakty Backend

| Artefakt | Typ | Komentarz |
| ------------- | ------------- | ------------- |
| opw-ref-base | war | Dokumentacja, Analiza, JPA, DTO  |
| opw-ref-management | war | Maski administracyjne |
| opw-ref-register | war | Formularz rejestracji wolontariusza |
| opw-ref-ws-inbound | war | Serwis importu danych |
| opw-ref-ws-outbound | war | Serwis eksportu danych |
| opw-ref-ws-management | war | Serwis administracyjny REST  |
| opw-ref-ws-register | war | Serwis rejestracji wolontariusza |

### Artefakty Frontend
* opw-ref-dashboad

Komisarz wyborczy
komisja obwodowa
pkw
wyborcy
pytanie proste tak / nie
pytanie wariantowe / zlozone kilka odpowiedzi, multiple choice



perpektywa / scope / frekwencja
krajowa

komisja obwodowa - gmina - powiat - wojewodztwo

rodzaje obwodow takie same przy prezydenckich
