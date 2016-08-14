# OmegaT Japanese localization git project trial 

Here is a team translation project for OmegaT (trial)

## Prerequisite

Please ensure that a Java Runtime Environment version 1.8 or later is installed in your system.
Also it is neccesary to connect the internet to download some of libraries to run OmegaT.

To configure proxy for Gradle, prepare a file `$HOME/.gradle/gradle.properteis` includes
```
systemProp.http.proxyHost=hostname
systemProp.http.proxyPort=8080
systemProp.http.proxyUser=xxxx
systemProp.http.proxyPassword=xxx
```

## How to generate translation files

Please call Gradle build system `gradlew` command from console.

```
$ ./gradlew translate
```

If you runs it on MS Windows platform, please call batch file.

```
$ .\gradlew.bat translate
```

Generator depends on a couple of libraries and applications, you need to connect
your platform to internet. If you are behind proxy server or firewall, please
refer Gradle documentation how to configure Gradle for network connections.
It will download some jar files from https://jcenter.bintray.com repository.

## How to translate

The project use OmegaT, Computer Aided Translation tool.
OmegaT is an Open Source Software and freely available for translators.
It is a kind of a translation memory.

The repository is designed to work with OmegaT team features. This means
translators who work on the repository are collaborative team.

## Contributions

Translation updates are not supporeted to merge with PR. Instead of push a request,
please ask us to join as a member who can write a repository.

OmegaT has a team feature. It automatically push translation contribution
onto github repository.

If you want to join, please leave a issue to express your will.

We use custom version of OmegaT Version 4.0 snapshot for automation of the project.
You should use gradle to launch custom OmegaT;

```
$ ./gradlew omegat
```

It automatically starts OmegaT GUI and prepares environment for you.

Bundled version of OmegaT is version 4.0 snapshot with small modifications.
One is a proxy configuration to follow system settings. Other is an addition of option
for unknown HTML entities.

## License

Hereis distributed under the GNU General Public License 3.0.

