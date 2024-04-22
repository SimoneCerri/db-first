# !Quest! #

- Modellare la struttura di una **tabella** per memorizzare tutti i dati riguardanti delle auto usate messe in vendita da un concessionario. []

## DATA ##

- `ID` ( ex. "1" ) { BIGINT - NOTNULL - UNIQUE - AUTO_INCREMENT }
- `brand` ( ex. "Fiat" ) { TEXT - NOTNULL }
- `model` ( ex. "Panda" ) { TEXT - NOTNULL }
- `year_of_production` ( ex. "1980" ) { YEAR - NULL - DEFAULT(0000) }
- `km` ( ex. "900000" ) { SMALLINT - NOTNULL }
- `car_type` ( ex. "suv/coupè/sedan/offroad/jdm/racecar" ) { VARCHAR(7) - NULL }
- `transmission_type` ( ex. "manual/automatic" ) { VARCHAR(9) - NULL - DEFAULT("manual") }
- `engine_type` ( ex. "diesel/gas/methane/petrol/eletric" ) { VARCHAR(7) - NULL - DEFAULT("petrol") }
- `engine_displacement` ( ex. "1100 fire" ) { TEXT - NULL }
- `condition` ( ex. "good/bad/medium" ) { VARCHAR(6) - NOTNULL }
- `price` ( ex. "20000 $" ) { DECIMAL(10, 2) - NOTNULL }
- `annual_maintenance_price` ( ex. "600 $" ) { DECIMAL(6, 2) - NULL - DEFAULT(unknown) }
- `maintenance_history` ( ex. "always passed" ) { TEXT - NULL - - DEFAULT(unknown) }
- `accident_history` ( ex. "2 accidents before: etc etc etc etc etc.." ) { TEXT - NULL - DEFAULT(unknown) }
- `previous_owner_history` ( ex. "3 owners before" ) { TEXT - NULL - DEFAULT("only owner") }
- `photo` ( ex. "image_url" )  { TEXT - NOTNULL }
- `city_origin` ( ex. "Napoli" ) { VARCHAR(10) - NOTNULL }
- `special_equipments` ( ex. "air conditioning, Maria Teresa on car's dashboard, etc etc etc.." ) { TEXT - NULL - DEFAULT("no equiptments") }
- `seller_name` ( ex. "Fabio De Luigi" ) { TEXT - NULL - DEFAULT(unknown) }
- `seller_vote` ( ex. "1/5" ) { VARCHAR(3) - NULL - DEFAULT(0/5) }
- `seller_number` ( ex. "3330573853" ) { SMALLINT - NOTNULL }
- `seller_sales_history` ( ex. "this person has already sold 4 cars on this site" ) { TEXT - NULL - DEFAULT("first-sale") }
- `payment_options` ( ex. "Option_1: Card, Option_2: Cash, Option_3: Exchange" ) { TEXT - NULL - DEFAULT("Cash-only") }
- `available_to_test` ( ex. "true/false" ) { BOOLEAN - NULL - DEFAULT(0) }

### Table of the database ###

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
