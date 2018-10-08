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

### Configureren van ESLint in je RN project
Op een Terminal in de root folder van je project. **Tip**: Dit kan ook in VS Code

#### Stap 1
Voeg volgende development dependencies toe aan je project:
```
npm install --save-dev eslint eslint-config-airbnb eslint-plugin-import eslint-plugin-react eslint-plugin-jsx-a11y babel-eslint
```

#### Stap 2
```
eslint --init
```

1. Selecteer 'Use a popular style guide'
2. Selecteer Airbnb
3. Selecteer JSON type
4. Update to newer versions? Yes

Herstart VS Code

#### Stap 3
Het bestand .eslintrc.json is toegevoegd. Open het bestand en overschrijf het met volgende:
```json
{
  "env": {
    "node": true,
    "browser": true,
    "es6": true
  },
  "parser": "babel-eslint",
  "extends": "airbnb",
  "plugins": ["react", "jsx-a11y", "import"],
  "rules": {
    "react/jsx-filename-extension": [1, { "extensions": [".js", ".jsx"] }],
    "react/prop-types": [1]
  }
}

```

## Setup Prettier
Open Visual Studio Code en voeg volgende plugin toe:
- Prettier - Code formatter

Install en reload

In Visual Studio Code open Preferences > Settings
- editor.formatOnSave: true
- eslint.autoFixOnSave: true
- eslint.alwaysShowStatus: true
- files.autoSave: onFocusChange


## Setup VSCode
Andere handige plugins in VSCode:
- Code Runner
- React Native Snippet
- React Native Tools
