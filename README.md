# Orb Project Template

[![CircleCI Build Status](https://circleci.com/gh/choilmto/orb.svg?style=shield "CircleCI Build Status")](https://circleci.com/gh/choilmto/orb) [![CircleCI Orb Version](https://img.shields.io/badge/endpoint.svg?url=https://badges.circleci.io/orb/choilmto/orb)](https://circleci.com/orbs/registry/orb/choilmto/orb) [![GitHub License](https://img.shields.io/badge/license-MIT-lightgrey.svg)](https://raw.githubusercontent.com/choilmto/orb/master/LICENSE) [![CircleCI Community](https://img.shields.io/badge/community-CircleCI%20Discuss-343434.svg)](https://discuss.circleci.com/c/ecosystem/orbs)


# About this project

Currently, CircleCI aggregates build times as part of their Insights they provide users. However, the information they provide looks at trends going back as far as 90 days. This orb gives Node users a granular view of their build times by piping the information to their existing log service.

# How to use

For an example code base that uses the orb, see [https://github.com/choilmto/orbtoberfest-example](https://github.com/choilmto/orbtoberfest-example). For every build step that matches the pattern `*build*`, this orb will capture the length of time CircleCI takes to build. The orb expects npm to be able to run the script `log:build_time`, where `process.env` variables will passed.

| Variable name | Value                                           |
|---------------|:------------------------------------------------|
| JOB_DURATION  | The time CircleCI takes to build in milliseconds|
| VERSION       | The version listed in `package.json`            |
| PULL_REQUESTS | Information on related pull requests            |
| JOB_NAME      | The name of the job in `config.yml`             |