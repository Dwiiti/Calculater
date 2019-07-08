# Calculater
Slave
Continuous integration is a coding philosophy and set of practices that drive development teams to implement small changes and
check in code to version control repositories frequently. Because most modern applications require developing code in different
platforms and tools, the team needs a mechanism to integrate and validate its changes.

The technical goal of CI is to establish a consistent and automated way to build, package, and test applications. With consistency
in the integration process in place, teams are more likely to commit code changes more frequently, which leads to better 
collaboration and software quality.

Continuous delivery picks up where continuous integration ends. CD automates the delivery of applications to selected 
infrastructure environments. Most teams work with multiple environments other than the production, such as development and testing
environments, and CD ensures there is an automated way to push code changes to them.  CD automation then performs any necessary 
service calls to web servers, databases, and other services that may need to be restarted or follow other procedures when 
applications are deployed.

A mature CI/CD practice has the option of implementing continuous deployment where application changes run through the CI/CD 
pipeline and passing builds are deployed directly to production environments. Teams practicing continuous delivery elect to deploy
to production on daily or even hourly schedule, though continuous delivery isn’t always the optimal for every business application.   

Continuous integration and delivery requires continuous testing because the objective is to deliver quality applications and code
to users. Continuous testing is often implemented as a set of automated regression, performance, and other tests that are executed
in the CI/CD pipeline.

Fig( CI_CD_Flow.pdf )

Continuous integration is a development philosophy backed by process mechanics and some automation. When practicing CI, developers
commit their code into the version control repository frequently and most teams have a minimal standard of committing code at least
daily. The rationale behind this is that it’s easier to identify defects and other software quality issues on smaller code 
differentials rather than larger ones developed over extensive period of times. In addition, when developers work on shorter 
commit cycles, it is less likely for multiple developers to be editing the same code and requiring a merge when committing.

One technique is to use version-control branching. A branching strategy such as Gitflow is selected to define protocols over how
new code is merged into standard branches for development, testing and production. Additional feature branches are created for 
ones that will take longer development cycles. When the feature is complete, the developers can then merge the changes from 
feature branches into the primary development branch. This approach works well, but it can become difficult to manage if there 
are many features being developed concurrently.

The build process itself is then automated by packaging all the software, database, and other components. For example, if you 
were developing a Java application, CI would package all the static web server files such as HTML, CSS, and JavaScript along 
with the Java application and any database scripts.

TEST

Automated testing frameworks help quality assurance engineers define, execute, and automate various types of tests that can help
development teams know whether a software build passes or fails. They include functionality tests that are developed at the end 
of every sprint and aggregated into a regression test for the entire application. These regression tests then inform the team 
whether a code change failed one or more of the tests developed across all functional areas of the application where there is 
test coverage.

A best practice is to enable and require developers to run all or a subset of regressions tests in their local environments. 
This step ensures that developers only commit code to version control after regression tests pass on the code changes.

Regression tests are just the start. Performance testing, API testing, static code analysis, security testing, and other testing 
forms can also be automated. The key is to be able to trigger these tests either through command line, webhook, or web service 
and that they respond with success or fail status codes.

Once testing is automated, continuous testing implies that the automation is integrated into the CI/CD pipeline. Some unit and 
functionality tests can be integrated into CI that flags issues before or during the integration process. Test that require a 
full delivery environment such as performance and security testing are often integrated into CD and performed after builds are 
delivered to target environments.

Continuous delivery is the automation that pushes applications to delivery environments. Most development teams typically have 
one or more development and testing environments where application changes are staged for testing and review. A CI/CD tool such 
as Jenkins 

CD pipeline includes many of these steps:

    Pulling code from version control and executing a build.
    Executing any required infrastructure steps that are automated as code to stand up or tear down cloud infrastructure..
    Moving code to the target compute environment like dev,test,UAT,pre-prod,prod.
    Managing the environment variables and configuring them for the target environment.
    Pushing application components to their appropriate services, such as web servers, API services, and database services.
    Executing any steps required to restarts services or call service endpoints that are needed for new code pushes.
    Executing continuous tests and rollback environments if tests fail.
    Providing log data and alerts on the state of the delivery.






