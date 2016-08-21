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

## Source materials

Source materials are abled to be updated from OmegaT project code.
OmegaT project code is fetched by git submodule strategy.
There is a utility task for updating source from original code.

```bash
$ git submodule init
$ git submodule update
```
Or you can do it with clone time at once;

```bash
$ git clone --recursive https://github.com/miurahr/omegat-jp-trial.git
```

then you can update source files;

```bash
$ ./gradlew update
```

Once you have a omegat-code fetched but want to update source again,
you can do it with following procedure;

```bash
$ git submodule update --remote
$ ./gradlew update
```

You can see git manual in Japanese for submodule at
https://git-scm.com/book/ja/v2/Git-%E3%81%AE%E3%81%95%E3%81%BE%E3%81%96%E3%81%BE%E3%81%AA%E3%83%84%E3%83%BC%E3%83%AB-%E3%82%B5%E3%83%96%E3%83%A2%E3%82%B8%E3%83%A5%E3%83%BC%E3%83%AB


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


## License

Hereis distributed under the GNU General Public License 3.0.

