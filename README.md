# ShieldCert

[![Maven Central](https://img.shields.io/maven-central/v/com.shieldcert/core)](https://central.sonatype.com/artifact/com.shieldcert/core)

ShieldCert is a library that helps you protect your application's communications.

---

## Documentation

👉 Full documentation is available at [docs.shieldcert.com](https://docs.shieldcert.com).

---

## Usage

Add the dependency from Maven Central:

```kotlin
dependencies {
    implementation("com.shieldcert:core:0.1.0")
}
```

```

val config = ShieldCertConfig(
            publicKey = "-----BEGIN PUBLIC KEY-----.......-----END PUBLIC KEY-----\n",
            apiKey = "API_KEY",
            expiredTimeout = 60.toDuration(DurationUnit.MINUTES)
        )

        ShieldCert.initSDK(
            application, //APLICATION/CONTEXT/ACTIVITY
            config
        )


// Protect 

val http = HttpClient(CIO) {
                install(ContentNegotiation) {
                    json()
                }
                install(Logging) {
                    logger = Logger.ANDROID
                    level = LogLevel.HEADERS
                }
                engine {
                    sslEngine()
                }
            }
            try {
                val txt = http.get("https://tls-v1-2.badssl.com:1012").bodyAsText()
                println(txt)
            } catch (e: Exception) {
                e.printStackTrace()
            }
```

