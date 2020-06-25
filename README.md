# Create Netty native binary.

This is the [time server example](https://netty.io/wiki/user-guide-for-4.x.html#wiki-h3-8) from Netty together 
with the minimum necessary substitutions to create native images on GraalVM plus a build file that configures
Graals `native-image` tool for you. 

## Build and run

You need [Maven](https://maven.apache.org), [GraalVM](https://www.graalvm.org) and GraalVMs [native image tool](https://www.graalvm.org/getting-started/#native-images) for this to work. 

Build native images:

```
./mvnw clean package
```

Run the time server on port 4711:

```
./target/server 4711
```

Run the client in a different shell to get the time from the server:

```
./target/client localhost 4711
```
