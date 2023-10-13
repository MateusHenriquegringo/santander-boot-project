# santander-boot-project
final project of bootcamp, RESTful API

# diagrama de classes

``` mermaid
classDiagram
  class User {
    + name: String
    - account: Account
    - card: Card
    - features[]: List<Feature>
    - news[]: List<News>
  }
  class Account {
    + number: String
    + agency: String
    + balance: Double
    + limit: Double
  }
  class Card {
    + number: String
    + limit: Double
  }
  class Feature {
    + icon: String
    + description: String
  }
  class News {
    + icon: String
    + description: String
  }

  User "1"*--"N" Feature
  User "1"*--"1" Account
  User "1"*--"N" Card 
  User "1"*-- "1"News 

```
