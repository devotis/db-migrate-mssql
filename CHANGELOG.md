# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.1.5] - 2021-03-15

### Fixed

- Add foreign key query #6

## [1.1.4] - 2021-03-15

### Fixed

- Now closing the connection and displaying an error log (advance to rolling back transactions on error) #5

## [1.1.3] - 2020-03-18

### Fixed

- mssql syntax for adding a column #3

## [1.1.2] - 2019-10-24

### Changed

- Explain in readme how to install this as an alias for `db-migrate-mssq`.

## [1.1.1] - 2019-10-24

### Changed

- Documented installation

## [1.1.0] - 2019-10-24

### Added

- Each migration is run within a transaction. Failed sql means migration did not happen. (PR #2) ([jpinkster](https://github.com/jpinkster))

## [1.0.1] - 2019-04-14

### Fixed

- Invalid object name '[your-schema].migrations'. Was caused by checking the `recordset` property that is already removed by the `all` and `runSql` functions.

## [1.0.0] - 2019-04-13

I've built db-migrate-mssql today. I started from a fork of https://github.com/db-migrate/pg . Took me about half a day to build it, and it's working. Without transactions for now. I'm sure there's room for improvement though. If you want to try, run: yarn add @devotis/db-migrate-mssql

I've not adapted the tests from pg to mssql yet, so no guarantees, but I'm able to migrate up and down. I tried only runSql thus far.
