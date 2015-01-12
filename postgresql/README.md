# PostgreSQL

#### Installation

In order to install PogreSQL, we will use the Posgres App. Search for the latest 9.3.5 release and download it in the list of [releases](https://github.com/PostgresApp/PostgresApp/releases).

Move the app to the **Application** folder and double click the app. Postgres app will install and start the server.

Update the app's preferences to **Start Postgres automatically after login**

#### Command Line Utilities

In order to add Postgres command line utilities, we'll need to change the $PATH environment variable:

* for Bash users, add the following to the `~/.bash_profile`:

`export PATH=$PATH:/Applications/Postgres.app/Contents/Versions/9.3/bin`