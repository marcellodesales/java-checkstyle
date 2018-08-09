# java-checkstyle
Klaviyo's Java Checkstyle config based on [Google's](http://checkstyle.sourceforge.net/google_style.html)

# Installation
## Maven
To integrate Klaviyo's Checkstyle configuration into a maven build, add the following to your project's `pom.xml`
```xml
  <build>
    <plugins>
      <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-checkstyle-plugin</artifactId>
        <version>3.0.0</version>
        <configuration>
          <configLocation>
            https://raw.githubusercontent.com/klaviyo/java-checkstyle/master/checkstyle.xml
          </configLocation>
        </configuration>
        <dependencies>
          <dependency>
            <groupId>com.puppycrawl.tools</groupId>
            <artifactId>checkstyle</artifactId>
            <version>8.11</version>
          </dependency>
        </dependencies>
      </plugin>
    </plugins>
  </build>
```

## IntellijIDEA
- Install the checkstyle plugin from the plugin browser or from [github](https://github.com/jshiell/checkstyle-idea)
- Once installed, open settings and navigate to `Other Settings` > `Checkstyle`
- Check `Treat Checkstyle errors as warnings` so you can distinguish between actual java syntax errors and simple linting errors
- Hit the plus button on the right side of the settings window to add a new configuration file and select file from HTTP. Make sure you use the [raw content link](https://github.com/klaviyo/java-checkstyle/raw/master/checkstyle.xml), not the prettified HTML view link.
![](idea-settings.png)
