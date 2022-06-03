# Java-Spring-Boot-on-Android

> ## Running Java Spring Boot on pure Android phone or virtual device

_"Pratique a linguagem de programação e o framework mais utilizado por grandes corporações somente com seu Smartphone Android e sem necessidade de alterar configurações avançadas como "root" ou instalação de aplicativos suspeitos."_

### What you'll build

You will build a classic “Hello World!” endpoint which any browser can connect to. You can even tell it your name, and it will respond in a more friendly way.

### What you’ll need

*   An Android phone or an Android Virtual Device (AVD)
*   A command line Android app, I recommend Termux
*   A Java™ Development Kit (JDK)
*   Basic Linux command line knowledge 
*   Will and curiosity

#### **Step 1: Start a new Spring Boot project**

Use start.spring.io to create a “web” project. In the “Dependencies” dialog search for and add the “web” dependency as shown in the screenshot. Hit the “Generate” button, download the zip.

![](https://lh4.googleusercontent.com/Q9Ay-uYOIMHDmAzehb36hnB_6FyPUG_l21SdjRwcztt91EFatIsTqMH_zT-72z9Mf-F52V8ndwsQnZSE93Ch02aO-qJ75e2_PGdtCjLLwXR3cWMdRzqNzgxvaGsEJdfDFYCcKgJ8slaNh2Ayiw)

Locate the downloaded demo.zip file path.

![](https://lh6.googleusercontent.com/4zJ-qMJSOU10VnGEZ7XnbQUVIsoKPl6OgXkNYf9KjPKusC4m67QI_0eBDHR7q1dClTipWogcKW-Jd0hYkEQf1qVjdAO0Xj9g3RtlRSpEMA5EAWMRni_K2cQdckcqrI-chKOTX5mvEUxkDBOJoA)

Copy it to the home Termux folder

```shell
cd && cp /storage/emulated/0/Download/demo.zip demo.zip
```

Unzip it and go to the demo unzipped folder

```shell
unzip demo.zip && cd demo
```

#### **Step 2: Check system requirements:**

  
Verify if you have Java installed on your system  
java -version
