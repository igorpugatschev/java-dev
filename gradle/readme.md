## Step 0. Before you Begin

Make sure you have Gradle installed.

```bash
brew install gradle
```

## Step 1. Initializing the Project

To test the Gradle installation, run Gradle from the command-line:

```bash
gradle --version
```
Run gradle init with the following parameters to generate a Java application:

```bash
gradle init --type java-application  --dsl groovy
```
When you are done, the directory should look as follows:

```
.
├── .gradle                 
│   └── ⋮
├── gradle                  
│   ├── libs.versions.toml  
│   └── wrapper
├── gradlew                 
├── gradlew.bat             
├── settings.gradle         
├── app                     
│   ├── build.gradle
│   └── src
└── ⋮                       
```

### Step 2. Understanding the Gradle Wrapper

The Gradle Wrapper is the preferred way of starting a Gradle build. The Wrapper downloads (if needed) and then invokes a specific version of Gradle declared in the build.

These scripts allow you to run a Gradle build without requiring that Gradle be installed on your system. It also helps ensure that the same version of Gradle is used for builds by different developers and between local and CI machines.

From now on, you will never invoke Gradle directly; instead, you will use the Gradle wrapper.

## Step 3. Invoking the Gradle Wrapper

Use the wrapper by entering the following command:

```bash
./gradlew build
```

The first time you run the wrapper, it downloads and caches the Gradle binaries if they are not already installed on your machine.

The Gradle Wrapper is designed to be committed to source control so that anyone can build the project without having to first install and configure a specific version of Gradle.

