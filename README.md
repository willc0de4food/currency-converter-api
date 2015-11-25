## Intro
I've exported this from the Google Code project [Currency Converter API](https://code.google.com/p/currency-converter-api/)

## Readme copied from Google Code
**Currency Converter** is a Java library which provides API for currency conversion. It uses different bank web-services to fetch rates and provides a single programming interface for any of supported web-services.

##### Currently these web-services are supported:
* bank-ua.com
* GoogleFinance web-service is under development for now

##### Currency Converter is available as a maven artifact:
```xml
<dependency>
  <groupId>com.tunyk.currencyconverter</groupId>
  <artifactId>currency-converter-api</artifactId>
  <version>1.0</version>
</dependency>
```

##### Example:

```java
// create an instance where USD is a default currency to convert from, and EUR a default one to convert to
// Using one of the implementation: BankUaCom
CurrencyConverter currencyConverter = new BankUaCom(Currency.USD, Currency.EUR);

// convert USD to EUR (the first parameter is amount of money you'd like to convert)
currencyConverter.convertCurrency(1f);

// the same
currencyConverter.convertCurrency(1f, Currency.EUR);

// the same
currencyConverter.convertCurrency(1f, Currency.USD, Currency.EUR);

// convert EUR to USD
currencyConverter.convertCurrency(1f, Currency.EUR, Currency.USD);

// and you can continue with any other supported currencies...
```