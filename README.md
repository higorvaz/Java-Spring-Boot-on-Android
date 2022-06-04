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

#### **Step 2: Check system requirements**

Verify if you have Java installed on your system

```shell
java -version
```

![](https://lh6.googleusercontent.com/AE5gsvuD2N6_XHQT43U92-0WW5GfRnVTmltHXdRCpdCjtETbE9uDZI02LhHB_E3sggrgD3WCzL0xwm_WumBQ3AKdgPwH1p0H7U5qL6gppTnkDmP4FYEMlCaReBuMiyIsfavAHKqvZfwzN9bHGA)

If no, update your system and install it

```shell
apt update -y && apt upgrade -y && apt install openjdk-17-jdk
```

#### **Step 3: Add your code**

Remove the original file DemoApplication.java located at src/main/java/com/example/demo folder.

```shell
rm src/main/java/com/example/demo/DemoApplication.java
```

Now create and edit a new DemoApplication.java adding the code below

```shell
nano -l -A -S -m src/main/java/com/example/demo/DemoApplication.java
```

![](https://lh3.googleusercontent.com/HM33zZbOPb6pp0gVZgDDJqYip6MT31c5lZJyxGfL6HOChTNV_49TQl9FKnx0AOzCGvfyToNQz72olfnUrJW8denIUCTffks9rteICVMLhY3XAVvm3X6EBqi4LYfbpJ3prDOcyYbwW0AkftT-0A)

```java
package com.example.demo;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.bind.annotation.RestController;

@SpringBootApplication
@RestController
public class DemoApplication {

    public static void main(String[] args) {
        SpringApplication.run(DemoApplication.class, args);
    }

    @GetMapping("/hello")
    public String hello(@RequestParam(value = "name", defaultValue = "World") String name) {
        return String.format("Hello %s!", name);
    }
}
```

Save

```shell
CTRL + o
```

Exit

```shell
CTRL + x
```

![](https://lh5.googleusercontent.com/LQycOtazvuEDeBnzZcrILjPEWJy-t6YK51oP_GbGcTS8LhTHBx__mj-VvPbE9ACO9RHoXSPWFVl4wnaRcMGLq4Pqi9sdC0UkNXyYwww8UXNeJjHvtiexOKhqT2xPOSujQpm2Ynd-zx37WXxKVg)

#### **Step 4: Try it**

```shell
./mvnw spring-boot:run
```

![](https://lh5.googleusercontent.com/qjrFsHuJaFWedNRIi3v8vlF8chlExhPpx8ZGUyn61x28KPtyppTal3jutOAqbjsCoJNL0OT40b1kJrLjRU_NdnTbHiNMy8yRlUPtKVUL8T0XI02b_MRhJeWIV7XCVjYq4rQK5wJhXKuGod9Wmw)

It will take some seconds to compile and show the results like this:

![](https://lh5.googleusercontent.com/iyPTdQXY7sX9cpbUskj3DSFO6aaaB0YWuRPdebTI3crg4vycuT0zBUZKDDmy8nm1j0wLdepNd-xgFff3heDL10l1ZEnrEhAM-O54_Lc2tkSXgYgug-BRfk87hlHFGPP8kDf-lAgXHIztSrkt6A)

a
