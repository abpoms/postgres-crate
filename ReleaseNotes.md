# Release notes

## postgres-0.7.0-beta.2

- Partially fix issue #2

- Actually use the settings passed to postgres
  The settings argument of pallet.crate.postgres/postgres was not actually 
  used. This patch fixes this by passing it to the existing settings-map 
  call instead.

## postgres-0.7.0-beta.1

- update for pallet 0.7.0
  Note this changes function names to use postgres-settings and
  install-postgres instead of settings and postgres

## postgres-0.6.1

- Add an option to postgresql-script to specify the database name

- Uses subprocess in postgresql-script to avoid working directory changes

- Fix warning from postgresql-script, and add a title
  Remove the 'could not change directory' warning, and add a title argument
  to allow identification of scripts in the log

- Add a :share key to postgres settings

- Guard postgres service actions with a check for :auto start clusters

- Add a test for merging postgres settings

- Add controldata functions to postgres

- Return errors if psql fails

- Disable postgres init services properly

- Ensure postgres settings are merged properly

- Add a function to return the default cluster name in postgres

- Add a check-settings function to postgres

- Ensure unique options in postgres settings

- Remove default ident permissions from postgres crate

- Update postgres crate to work for multiple clusters

- Add multi-db instance capability for postgres

- Postgres fixes and addition of wal directory for streaming replication


## postgres-0.6.0

- Add scm information to enable module release

- Remove :settings from postgres parameters key

- Allow sql script from multiple sources
  Script can now be supplied by any mechanism supported by remote-file

- Remove unused require

- Update postgres crate to use settings
  Also added support for postgres 9.0 on debian, and redhat based distros.


## pallet-crates-0.5.0


## pallet-crates-0.4.4


## pallet-crates-0.4.3

- Update for 0.5.0-SNAPSHOT
  Change pallet.resource.* to pallet.action.*. Change stevedore calls to
  script functions to use unquote and the pallet.script.lib namespace.
  Change request to session.  Change build-resources to build-actions.


## pallet-crates-0.4.2


## pallet-crates-0.4.1


## pallet-crates-0.4.0


## pallet-crates-0.4.0-beta-1

- After seeing a mailing list message from Stuart Halloway regarding the
  future of as-str, changed all instances of as-str to clojure.core/name.

- Formatting fixes, and add simple test file for postgresql

- Add crate to install and configure postgresql.

