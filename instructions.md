# Create Typescript Project from Scratch

## Init

npx gitignore node
yarn init --yes
yarn add -D typescript eslint jest

## config package.json

    * "scripts"
    * "types"

## Volta Pin

volta pin node yarn   // pin last stable versions of node and yarn

## Git

git init
git add -A
git commit -m "initial commit"

## typescript initialization

yarn tsc --init

// config tsconfig.json

## Eslint initialization

yarn eslint --init

    -- check syntax and find problems
    -- type of modules: None
    -- which framework: none (react?)
    -- does your project use Typescript: Yes
    -- where code runs: Node/Browser
    -- format config: json
    -- install dependencies with npm: Yes

delete package.json.lock

yarn

configure .eslintrc.json

create tsconfig.eslint.json

yarn lint

## Configure Jest

yarn add -D jest @types/jest @babel/core @babel/preset-env @babel/preset-typescript

mkdir tests

add file index.test.ts

configure .babelrc, tests/tsconfig.json

yarn lint

yarn build

yarn test

## Add git remote

git remote add gitlab12_web_ts_boilerplate <http://10.100.102.104:10080/web/typescript-project-boilerplate.git>
git push -u gitlab12_web_ts_boilerplate --all
git push -u gitlab12_web_ts_boilerplate --tags

## Add Api-Extractor

yarn add -D @microsoft/api-extractor @microsoft/api-documenter

yarn api-extractor init

modify api-extractor.json

mkdir etc
(where api report will be placed)

yarn api-extractor run --local

(add temp to .gitignore )

--- after updating ts source code
--should run:
     yarn build
     yarn api-extractor run --local

-- yarn api-extractor run   ==> helps to detect public api changes (will fail if API changed)

## Api Documenter

yarn api-documenter markdown -i temp -o docs