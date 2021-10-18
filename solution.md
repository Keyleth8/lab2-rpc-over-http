#Server
To build and deploy the server, I've used the following commands:
```
./gradlew :server:build
./gradlew :server:bootRun
```

#Client
To build and deploy the client, the server has to be running. Once it has been deployed, the client can be deployed using the following:
```
./gradlew :client:build
./gradlew :client:bootRun
```
At first, deploying the client threw an error on both the server and the client. To fix it, I added a `TranslationResponse.apply()` function in the server's function `translation()`.

Now it shows the following output:
```
Result of translating [Translate me!] is [¡Tradúceme!]
```