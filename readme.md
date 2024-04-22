# !Quest! #

- Modellare la struttura di una **tabella** per memorizzare tutti i dati riguardanti delle auto usate messe in vendita da un concessionario. [x]

## DATA ##

- `ID` | BIGINT - NOTNULL - UNIQUE - AUTO_INCREMENT |
- `brand` | TEXT - NOTNULL |
- `model` | TEXT - NOTNULL |
- `year_of_production` | YEAR - NULL - DEFAULT(0000) |
- `km` | SMALLINT - NOTNULL |
- `car_type` | VARCHAR(7) - NULL |
- `transmission_type` | VARCHAR(9) - NULL - DEFAULT("manual") |
- `engine_type` | VARCHAR(7) - NULL - DEFAULT("petrol") |
- `engine_displacement` | TEXT - NULL |
- `condition` | VARCHAR(6) - NOTNULL |
- `price` | DECIMAL(10, 2) - NOTNULL |
- `annual_maintenance_price` | DECIMAL(6, 2) - NULL - DEFAULT(unknown) |
- `maintenance_history` | TEXT - NULL - DEFAULT(unknown) |
- `accident_history` | TEXT - NULL - DEFAULT(unknown) |
- `previous_owner_history` | TEXT - NULL - DEFAULT("only owner") |
- `photo` | TEXT - NOTNULL |
- `city_origin` | VARCHAR(10) - NOTNULL |
- `special_equipments` | TEXT - NULL - DEFAULT("no equiptments") |
- `seller_name` | TEXT - NULL - DEFAULT(unknown) |
- `seller_vote` | VARCHAR(3) - NULL - DEFAULT(0/5) |
- `seller_number` | SMALLINT - NOTNULL |
- `seller_sales_history` | TEXT - NULL - DEFAULT("first-sale") |
- `payment_options` | TEXT - NULL - DEFAULT("Cash-only") |
- `available_to_test` | BOOLEAN - NULL - DEFAULT(0) |

### EXAMPLE ### 
>Database's table with some examples

|  ID  |  BRAND  |  MODEL  |  YEAR OF PROD.  |  KM  |  TYPE  |  TRANSMISSION  |  ENGINE  |  ENGINE-DISPL.  |
|:-----|:--------:|:------:|:------:|:------:|:------:|:------:|:------:|------:|
|  1 |  Fiat  |  Panda 4x4  |  1980  |  900000  |  offroad  |  manual  |  madonne  |  1100 fire  |
|  2  |  Ferrari  |  F40  |  1992  |  1992  |  1000  |  racecar  |  manual  |  petrol  |  2,936 cc (2.9 L) twin-turbocharged V8  |
|  3  |  Nissan  |  GTR R-34  |  1999  |  1999  |  20000  |  jdm  |  manual  |  petrol  |  2.6 L twin-turbocharged RB26DETT I6  |

|  CONDITION  |  PRICE  |  MAINTENANCE-PRICE  |  PHOTO  |  CITY  |  EQUIPMENTS  |  MAINTENANCE-PRICE  |  MAINTENANCE-HISTORY  |  ACCIDENT-HISTORY  |
|:-----|:--------:|:------:|:------:|:------:|:------:|:------:|:------:|------:|
|  medium  |  3000  |  gratis  |  url_panda4x4  |  Napoli  |  Maria Teresa  |  unknown  |  unknown  |  unknown  |
|  medium  |  1000000  |  1000  |  url_ferrari_f40  |  Bologna  |  None  |  unknown  |  unknown  |  unknown  |
|  good  |  85000  |  2000  |  url_godzilla  |  Japan  |  None  |  unknown  |  unknown  |  unknown  |


|  OWNER-HISTORY  |  SELLER-NAME  |  SELLER-VOTE  |  SELLER-NUMBER  |  SELLER-HISTORY  |  PAYMENTS  |  TEST  |
|:-----|:--------:|:--------:|:------:|:------:|:------:|------:|
|  only-owner  |  Fabio Onesto  |  1/5  |  3330573853  |  first-sale  |  Cash-only  |  false  |
|  only-owner  |  unknown  |  4/5  |  3320523553  |  first-sale  |  Cash/Card  |  true  |
|  only-owner  |  unknown  |  3/5  |  3380933813  |  first-sale  |  Exchange  |  true  |
