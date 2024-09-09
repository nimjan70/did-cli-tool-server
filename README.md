# Server CLI-Tool

Welcome to the Server CLI-Tool Repository.<br>
This repository provides an SDK for generating a server wallet and DID document.

## Folder Structure
```
did-cli-tool-server
├── CHANGELOG.md
├── CLA.md
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── LICENSE.dependencies.md
├── MAINTAINERS.md
├── README.md
├── README_ko.md
├── RELEASE-PROCESS.md
├── SECURITY.md
├── docs
│   └── api
│       ├── CLI-Tool_SERVER_API.md
│       └── CLI-Tool_SERVER_API_ko.md
└── source
    └── did-cli-tool-server
        ├── .gitignore
        ├── build.gradle
        ├── gradle
        │    └── wrapper
        ├── gradlew
        ├── gradlew.bat
        ├── libs
        ├── README_ko.md
        ├── README.md
        ├── settings.gradle
        └── src
```

| Name                    | Description                                     |
| ----------------------- | ----------------------------------------------- |
| source                  | SDK source code project                         |
| docs                    | Documentation                                   |
| ┖ api                   | API guide documentation                         |
| README.md               | Overview and description of the project         |
| CLA.md                  | Contributor License Agreement                   |
| CHANGELOG.md            | Version-specific changes in the project         |
| CODE_OF_CONDUCT.md      | Code of conduct for contributors                |
| CONTRIBUTING.md         | Contribution guidelines and procedures          |
| LICENSE.dependencies.md | Licenses for the project’s dependency libraries |
| MAINTAINERS.md          | General guidelines for maintaining              |
| RELEASE-PROCESS.md      | Release process                                 |
| SECURITY.md             | Security policies and vulnerability reporting   |

## Libraries

Libraries can be found in the [build folder](did-cli-tool-server/source/did-cli-tool-server/build/libs).

1. Copy each of the files below to the libs in your server project.
   <br> - `did-datamodel-server-1.0.0.jar`
   <br> - `did-crypto-sdk-server-1.0.0.jar`
   <br> - `did-core-sdk-server-1.0.0.jar`
   <br> - `did-wallet-sdk-server-1.0.0.jar`

2. Add the following dependencies to the build.gradle of the server project.

```groovy
    implementation files('libs/did-datamodel-sdk-server-1.0.0.jar')
    implementation files('libs/did-crypto-sdk-server-1.0.0.jar')
    implementation files('libs/did-core-sdk-server-1.0.0.jar')
    implementation files('libs/did-wallet-sdk-server-1.0.0.jar')

    implementation 'org.bouncycastle:bcprov-jdk18on:1.78.1'
    implementation group: 'info.picocli', name: 'picocli', version: '4.2.0'
    implementation group: 'com.google.code.gson', name: 'gson', version: '2.8.9'
    implementation 'org.hibernate.validator:hibernate-validator:7.0.0.Final'
```
3. Sync `Gradle` to ensure the dependencies are properly added.

## API Reference

API Reference can be found [here](docs/api/CLI-Tool_SERVER_API.md)


## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) and [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) for details on our code of conduct, and the process for submitting pull requests to us.


## License
Copyright 2024 Raonsecure