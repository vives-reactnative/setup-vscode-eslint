# Setup ESLint, Prettier & VSCode

## What is ESLint

Klik op onderstaande afbeelding om youtube video te bekijken over ESLint
[![ESLint](https://img.youtube.com/vi/aWFwJVjfDlE/0.jpg)](https://www.youtube.com/watch?v=aWFwJVjfDlE)

## Setup ESLint

### One time

Install ESLint globally

Open je commandline en voer volgend commando uit

```
npm install -g eslint
```

Open Visual Studio Code en voeg volgende plugin toe:

- ESLint (Integrates ESLint JavaScript into VS Code)

Install en reload

![Install ESLint extension in VSCode](https://github.com/vives-reactnative/setup-vscode-eslint/blob/rallycodingconfig/images/eslintextension.gif "Install ESLint extension in VSCode")

Indien in het project een ESLint config bestand aanwezig is zal VSCode onmiddellijk feedback geven op de JavaScript code als die niet voldoet aan de vooropgestelde regels

### Configureren van ESLint in ieder RN project

Op een Terminal in de root folder van je project.

**Tip**: Dit kan ook in VS Code, view Terminal

#### Stap 1

Voeg volgende development dependencies toe aan je project. Open een commandline in de root folder van je project, in de folder waar ook het bestand package.json is terug te vinden.

```
npm install --save-dev eslint-config-rallycoding
```

Na het uitvoeren van dit commando op de command line zal in package.json een development dependency zijn toegevoegd

#### Stap 2

Voeg een bestand .eslintrc toe aan de root van je React Native project

```json
{
  "extends": "rallycoding",
  "rules": {
    "import/no-extraneous-dependencies": 0
  }
}
```

## Setup Prettier

VSCode toont ons nu alle ESLint-warning. Maar we moeten ze nog steeds handmatig corrigeren. Boe! Om het onszelf gemakkelijker te maken, installeren we een andere tool genaamd Prettier. Prettier zal onze code automatisch voor ons opmaken wanneer we erom vragen of wanneer we een bestand opslaan.

### One time

Install Prettier globally

Open je commandline en voer volgend commando uit

```
npm install -g prettier
```

Open Visual Studio Code en voeg volgende plugin toe:

- Prettier - Code formatter

Install en reload

![Install Prettier extension in VSCode](https://github.com/vives-reactnative/setup-vscode-eslint/blob/rallycodingconfig/images/prettier.png "Install Prettier extension in VSCode")

In Visual Studio Code open Preferences > Settings

- editor.formatOnSave: true
- eslint.autoFixOnSave: true
- eslint.alwaysShowStatus: true

## Setup VSCode

Andere handige plugins in VSCode:

- Code Runner
- React Native Snippet
- React Native Tools
