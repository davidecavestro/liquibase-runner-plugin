# Jenkins Liquibase Plugin
---

# About

Adds Liquibase as an available build step.  See Liquibase documentation at http://www.liquibase.org/.

# Installation

*  Install the liquibase-runner plugin.
*  Create an empty version of your database on the target server (if applicable).


# Configuration

## "Execute" versus "Invoke"

There are two ways of using this plugin, distinguished by "Execute Liquibase" versus "Invoke Liquibase"

**Execute**

Use this build step if you have an existing liquibase installation and wish to have it run just as if you were doing so 
from command line.  The build's console log will contain the stdout/stderr output of liquibase.

Once you've created your installation in Jenkins's configuration, it will be available for selection in this build step. 

Your liquibase installation should include the driver for your database.

**Invoke**

The "Invoke Liquibase" build step runs liquibase internally and doesn't require an existing installation.  Furthermore, 
any changesets executed during the build are reported.

The types of databases you can use is restricted by those in the drop-down list. 
  
# The Future
  
I'd like to minimize the difference between "Invoke" and "Execute" and have changesets be reported in both types of
build steps.
 





