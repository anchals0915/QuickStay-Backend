# Quick Stay (Backend)

A Short-term rental platform that prioritizes female travellers’ safety and comfort while enhancing the overall booking experience. 

Spring boot backend of the Quick Stay

### Key Features:
+ Booking management for travelers
+ Landlord reservation management
+ Search for houses by criteria (location, date, guests, beds, etc)
+ Authentication and Authorization (Role management) with Auth0 (OAuth2)
+ Domain-driven design

## Usage
### Prerequisites
- [JDK 21](https://adoptium.net/temurin/releases/)
- IDE ([VSCode](https://code.visualstudio.com/download), [IntelliJ](https://www.jetbrains.com/idea/download/))


### Launch
#### Maven
``./mvnw spring-boot:run  -Dspring-boot.run.arguments="--AUTH0_CLIENT_ID=<client-id> --AUTH0_CLIENT_SECRET=<client-secret>"``

#### IntelliJ
Go in IntelliJ add the environment variables and then run it.
