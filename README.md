<h1 style="font-weight:normal">
  <a href="https://sourcerer.io">
    <img src=https://user-images.githubusercontent.com/20287615/34189346-d426d4c2-e4ef-11e7-9da4-cc76a1ed111d.png alt="Sourcerer" width=35>
  </a>
  &nbsp;sourcerer.io&nbsp;
  <a href="https://sourcerer.io/start"><img src=https://img.shields.io/badge/sourcerer-start%20now-brightgreen.svg?colorA=087c08></a>
  <a href="https://github.com/sourcerer-io/sourcerer-app/releases"><img src=https://img.shields.io/github/release/sourcerer-io/sourcerer-app.svg?colorB=58839b></a>
  <a href="https://github.com/sourcerer-io/sourcerer-app/blob/master/LICENSE.md"><img src=https://img.shields.io/github/license/sourcerer-io/sourcerer-app.svg?colorB=ff0000></a>
</h1>

A visual profile for software engineers.
<br>

<p align="center">
  <img alt="sergey" src="https://user-images.githubusercontent.com/20287615/41826375-ffe3c62a-77dd-11e8-9352-62c8a8f476a6.gif">
</p>

Features
========
* Build profile automatically with a single click
* Support of 100 languages (even exotic like COBOL)
* More than 1000 libraries usage detection with per-line statistics
* Visual repsentation of your developing experience
* *Finally!* Summary of all repositories you've contributed too 
* Discover interesting facts about yourself
* News that is relevant to your code

Creating your profile is just the first step for us at Sourcerer. Some of the things on our roadmap include:
* Engineers to follow and learn from
* Technology and libraries you should know about
* Projects that could use your help

Get started
===========

The easiest way to get started is with your open source repos. Go to <https://sourcerer.io/start>, and select *Build with GitHub* and watch your profile build. 

For closed source repos, you will need to use this app. If you already created an account using GitHub, you would have received an email with credentials for the app. If not, You will need a new account, which you can get at <https://sourcerer.io/join>.

Showcase
========
<center>
  <table>
    <tr>
      <td><a href="https://sourcerer.io/chdemko"><img width="131" alt="chdemko" src="https://user-images.githubusercontent.com/29913247/41827998-512ef768-783b-11e8-9afd-f94fac1b2886.png"></a></td>
      <td><a href="https://sourcerer.io/chendaniely"><img width="131" alt="chendaniely" src="https://user-images.githubusercontent.com/29913247/41827999-514d0b22-783b-11e8-8a05-af7191b86f6c.png"></a></td>
      <td><a href="https://sourcerer.io/lauragift21"><img width="131" alt="lauragift21" src="https://user-images.githubusercontent.com/29913247/41828000-5169ac8c-783b-11e8-9955-a3cb114c37f7.png"></a></td>
      <td><a href="https://sourcerer.io/maracuja-juice"><img width="131" alt="maracuja-juice" src="https://user-images.githubusercontent.com/29913247/41828001-5184d8fe-783b-11e8-9d5f-ce57d208d7cd.png"></a></td>
    </tr>
    <tr>
      <td><a href="https://sourcerer.io/marisbotero"><img width="131" alt="marisbotero" src="https://user-images.githubusercontent.com/29913247/41828002-519fb4a8-783b-11e8-98dd-ed3599b16a5a.png"></a></td>
      <td><a href="https://sourcerer.io/nordes"><img width="131" alt="nordes" src="https://user-images.githubusercontent.com/29913247/41828003-51baff56-783b-11e8-883c-608fd476afc9.png"></a></td>
      <td><a href="https://sourcerer.io/ppapadeas"><img width="131" alt="ppapadeas" src="https://user-images.githubusercontent.com/29913247/41828004-51d833f0-783b-11e8-9681-9725a7e3ed6a.png"></a></td>
      <td><a href="https://sourcerer.io/praharshjain"><img width="131" alt="praharshjain" src="https://user-images.githubusercontent.com/29913247/41828005-51f4fb48-783b-11e8-9f29-071bef43909f.png"></a></td>
    </tr>
  </table>
</center>

Requirements
============

* Linux or macOS
* Java 8+ Platform ([JRE](http://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html) for Linux or [JDK](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) for macOS)

Usage
=====

To install sourcerer run the following command:

```
curl -s https://sourcerer.io/app/install | bash
```

To run wizard use "sourcerer" command

Internals
=========

The app looks at repos locally on your machine, and then sends stats to sourcerer.io. The best way to verify is to look at the code. [src/main/proto/sourcerer.proto](https://github.com/sourcerer-io/sourcerer-app/blob/develop/src/main/proto/sourcerer.proto) is a good start as it describes the client-server protocol.
The Sourcerer app does **NOT** upload source code anywhere, and it **NEVER** will.

Build
=====

To build and run this application, you'll need latest versions of Git, Gradle and JDK installed on your computer. From your command line:

```
# Clone this repository
$ git clone https://github.com/sourcerer-io/sourcerer-app.git

# Go into the repository
$ cd sourcerer-app

# Build
$ gradle build

# Run the app
$ java -jar build/libs/sourcerer-app.jar
```

FAQ
===

### How to process close source repos?
We process only public repos using GitHub OAuth. To process close source repos you need to run sourcerer app locally. See get started for instructions. Sourcerer app sends only statistical information to our servers and never sends code.

### Why do we need GitHub permissions?
We use emails to indetify commits authorship, read orgs access to get list of public repositories that you've contributed to. You also need to grant access to read this public information from org

### Other questions
See sourcerer.io/faq 

Contributing
============

We love contributions!  Check out the [Contribution guide](https://github.com/sourcerer-io/sourcerer-app/blob/master/CONTRIBUTING.md) for more information.

Some handy links:<br>
* [Sourcerer Site](https://sourcerer.io/)
* [Sourcerer Blog](https://blog.sourcerer.io)
* [Follow Sourcerer on Twitter](https://twitter.com/sourcerer_io)
* [Follow Sourcerer on Facebook](https://www.facebook.com/sourcerer.io/)

License
=======

Sourcerer is under the MIT license. See the [LICENSE](https://github.com/sourcerer-io/sourcerer-app/blob/develop/LICENSE.md) for more information.
