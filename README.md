**# payments-system**
We are builing system to searching data using different search criteria
a. By Zip code or State or City or Type or Bank Name
b. By City & State

**#How to Load Data?**
Data will be loading in memory while we up the application, for that I have used init method in payment service where we put PostConstruct annotation of spring frameowrk.

**# How to Read data from CSV:**
I have used one openCSV lib to parse data from CSV and store result in java pojo object so once all data are read in memory then we are skipping first record as this contains header information which is meaning less for us.

**#How to start application**
 command: mvn spring-boot:run

**#How Search Functionalty will work?**
Case 1:By Zip code or State or City or Type or Bank Name
this is a GET call and for the generic search which can be searched by zip code or state or city or bank name
http://localhost:8081/api/v1/payment/search?searchKeyword=New York
This will give the records in that particular city

http://localhost:8081/api/v1/payment/search?searchKeyword=TX
This will give the records in that particular state

Case 2: By City & State
this is a GET call and for searching by city and state
http://localhost:8081/api/v1/payment/search?city=New York&state=NY


