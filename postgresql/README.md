# PostgreSQL

#### Installation

In order to install PogreSQL, we will use the Posgres App. Search for the latest 9.3.5 release and download it in the list of [releases](https://github.com/PostgresApp/PostgresApp/releases).

Move the app to the **Application** folder and double click the app. Postgres app will install and start the server.

Update the app's preferences to **Start Postgres automatically after login**

#### Command Line Utilities

In order to add Postgres command line utilities, we'll need to change the $PATH environment variable:

* for Bash users, add the following to the `~/.bash_profile`:

`export PATH=$PATH:/Applications/Postgres.app/Contents/Versions/9.3/bin`

You can now check if the path is set up correctly by typing `which psql`.

PostgreSQL: `clusterdb` `createdb` `createlang` `createuser` `dropdb` `droplang` `dropuser` `ecpg` `initdb` `oid2name` `pg_archivecleanup` `pg_basebackup` `pg_config` `pg_controldata` `pg_ctl` `pg_dump` `pg_dumpall` `pg_receivexlog` `pg_resetxlog` `pg_restore` `pg_standby` `pg_test_fsync` `pg_test_timing` `pg_upgrade` `pgbench` `postgres` `postmaster` `psql` `reindexdb` `vacuumdb` `vacuumlo`

#### Using PostgreSQL with Ruby

In order to access PostgreSQL databases from [Ruby](ruby/README.md) projects, you'll need to install the [pg](https://rubygems.org/gems/pg/versions/0.18.2) gem. If you've already installed Ruby, then installing the `pg` gem is as easy as running in Terminal the following command: `gem install pg -- --with-pg-config=<path-to-pg_config>`. 

**Note:** The path to `pg_config` is the same as the one used to add Postgres' command line utilities: `/Applications/Postgres.app/Contents/Versions/9.3/bin/pg_config`

#### Useful Commands

After setting the command line utilities, you'll be able to manipulate PostgreSQL through Terminal's command line. Here are a coupld of useful commands:

* Connect to specific database: `psql -d <database_name>` 
* Dump database: `pg_dump <db_name> > <path_to_export_file>.dump.out`
* Dump and compress database: `pg_dump <db_name> | gzip -c > <path_to_export_file>.dump.out.gz`
* Import from dump file: `psql -d <db_name> -f <path_to_export_file>.dump.out`

