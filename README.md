## Parcours français

Ce dépôt est accompagné d’un parcours documentaire en français consacré à PoolTogether TWAB Controller. Voir [docs/fr/](docs/fr/).

<p align="center">
  <a href="https://github.com/pooltogether/pooltogether--brand-assets">
    <img src="https://github.com/pooltogether/pooltogether--brand-assets/blob/977e03604c49c63314450b5d432fe57d34747c66/logo/pooltogether-logo--purple-gradient.png?raw=true" alt="PoolTogether Brand" style="max-width:100%;" width="400">
  </a>
</p>


# PoolTogether V5 TWAB Controller


[![Code Coverage](https://github.com/pooltogether/v5-twab-controller/actions/workflows/coverage.yml/badge.svg)](https://github.com/pooltogether/v5-twab-controller/actions/workflows/coverage.yml)
[![built-with openzeppelin](https://img.shields.io/badge/built%20with-OpenZeppelin-3677FF)](https://docs.openzeppelin.com/)
[![GPLv3 license](https://img.shields.io/badge/License-GPLv3-blue.svg)](http://perso.crans.org/besson/LICENSE.html)


<strong>Have questions or want the latest news?</strong>
<br/>Join the PoolTogether Discord or follow us on Twitter:


[![Discord](https://badgen.net/badge/icon/discord?icon=discord&label)](https://pooltogether.com/discord)
[![Twitter](https://badgen.net/badge/icon/twitter?icon=twitter&label)](https://twitter.com/PoolTogether_)


## Overview


The Time-Weighted Average Balance (TWAB) Controller is a system that keeps track of users token balances, their historic balances and their average balances of historic time periods. It is calculated by looking at the balances held during a queried time period, weighting them based on the duration they were held and returning an average amount held for the whole time period.


This ability to look back in time is critically important for PoolTogether, so that users can deposit and withdraw freely into a prize pool while having their liquidity contribution measured perfectly.


For example:


- If a user held 100 tokens for 1 week, then their average balance over that time was 100.
- If instead they held 100 for half of the week and then 200 for the second half, then their average for the week would be 150.


## Development


### Installation


You may have to install the following tools to use this repository:


- [Foundry](https://github.com/foundry-rs/foundry) to compile and test contracts
- [direnv](https://direnv.net/) to handle environment variables
- [lcov](https://github.com/linux-test-project/lcov) to generate the code coverage report


Install dependencies:


```
npm i
```


### Env


Copy `.envrc.example` and write down the env variables needed to run this project.


```
cp .envrc.example .envrc
```


Once your env variables are setup, load them with:


```
direnv allow
```


### Compile


Run the following command to compile the contracts:


```
npm run compile
```
