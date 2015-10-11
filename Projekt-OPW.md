# System OPW
Otwarta Platforma Wyborcza (OPW) to oprogramowanie klasy enterprise, którego podstawowym zadaniem jest niezależna i obiektywna weryfikacja wyników wyborów.  
Celem projektu OPW nie jest kompletna implementacja wymagań sprecyzowanych przez PKW w ramach projektu PW2 (Platforma Wyborcza 2).

# Architektura
System OPW składa się z następujących, wpełni niezależnych modułów.

| Akcja wyborcza | Moduł | Kommentarz |
| ------------- | ------------- | ------------- | ------------- |
| Prezydenckie  | [opw-pre](https://github.com/OtwartaPlatformaWyborcza/opw-pre) |  Wybory prezydenckie |
| Referendum | `ref` | Referendum ogólnokrajowe |
| Parlamentarne  | `par` | Wybory parlamentarne (Sejm i Senat) |
| Unia Europejska  | `eu` | ? |

Poszczególne moduły są zdefiniowanie jako pakiety wewnątrz `pl.otwartapw.opw`.

## Moduł PRE
Dedykowany moduł do obsługi wyborów prezydenckich.

### Artefakty

| Nazwa | Typ | Kommentarz |
| ------------- | ------------- | ------------- |
| opw-pre-base | war | JPA, API |
| opw-pre-managemet | war | Maski administracyjne (JSF 2.2) |
| [opw-pre-register](https://github.com/OtwartaPlatformaWyborcza/opw-pre-register) | war | Formularz rejestracji wolontariusza (JSF 2.2) |
| opw-pre-inbound-ws | war | Serwis importu - zapis do bazy danych |
| opw-pre-outbound-ws | war | Serwis eksportu - odczyt bazy danych |
| opw-pre-managemet-ws | war | Serwis administracyjny |
| opw-preregister-ws | war | Serwis rejestracji |
| opw-pre-register-ws-api | jar | Definicja API, DTO, walidacji |

### Struktura pakietów (backend)
`pl.otwartapw.opw.pre.api`  
`pl.otwartapw.opw.pre.bean`  
`pl.otwartapw.opw.pre.entity`  
`pl.otwartapw.opw.pre.management.controller`  
`pl.otwartapw.opw.pre.management.dto`  
`pl.otwartapw.opw.pre.management.handler`  
`pl.otwartapw.opw.pre.register`  
`pl.otwartapw.opw.pre.inbound.ws`  
`pl.otwartapw.opw.pre.outbound.ws`  
`pl.otwartapw.opw.pre.management.ws`  
`pl.otwartapw.opw.pre.register.ws`  

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
| opw-ref-inbound-ws | war | Serwis importu danych |
| opw-ref-outbound-ws | war | Serwis eksportu danych |
| opw-ref-management-ws | war | Serwis administracyjny REST  |
| opw-ref-register-ws | war | Serwis rejestracji wolontariusza |

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
