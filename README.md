# Project Work Time - Logging

## Learning Goals

- Spend some time working on your project.

## Project Work Time

Now that we have learned a little more about logging in our Spring applications,
it's time to apply this new knowledge to our projects!

Modify the service classes in your project to add some helpful logging messages
for when the application is running. Consider the following instructions:

- Make use of the logging framework and log to a file called
  `spring-project.log`.
  - Use the `@Slf4j` Lombok annotation to instantiate a `Logger` instance for
    each service class.
  - The logging level should be set to INFO at the very least.
  - Provide log statements for when creating or posting data to the data source.
  - Provide log statements for when deleting data from the data source.
  - Provide log statements for when retrieving data from the data source.

Here is a simple output of what a log could look like in your application:

```text
2022-12-21 12:11:57.891  INFO 17625 --- [           main] c.e.s.SpringProjectApplication           : Started SpringProjectApplication in 3.633 seconds (JVM running for 4.141)
2022-12-21 12:12:32.941  INFO 17625 --- [nio-8080-exec-2] o.a.c.c.C.[Tomcat].[localhost].[/]       : Initializing Spring DispatcherServlet 'dispatcherServlet'
2022-12-21 12:12:32.942  INFO 17625 --- [nio-8080-exec-2] o.s.web.servlet.DispatcherServlet        : Initializing Servlet 'dispatcherServlet'
2022-12-21 12:12:32.943  INFO 17625 --- [nio-8080-exec-2] o.s.web.servlet.DispatcherServlet        : Completed initialization in 1 ms
2022-12-21 12:12:33.241  INFO 17625 --- [nio-8080-exec-2] c.e.springproject.service.CamperService  : Suzie Bingham has been added as a camper!
2022-12-21 12:13:14.364  INFO 17625 --- [nio-8080-exec-3] c.e.springproject.service.CamperService  : Dustin Henderson has been added as a camper!
2022-12-21 12:13:25.036  INFO 17625 --- [nio-8080-exec-4] c.e.springproject.service.CamperService  : Retrieved campers from the data source
2022-12-21 12:14:02.497  INFO 17625 --- [nio-8080-exec-5] c.e.s.service.ActivityService            : Archery has been added as an activity!
2022-12-21 12:14:37.730  INFO 17625 --- [nio-8080-exec-7] c.e.s.service.ActivityService            : Retrieved activities from data source
2022-12-21 12:15:19.192  INFO 17625 --- [nio-8080-exec-8] c.e.s.service.ActivityService            : Successfully deleted the activity with ID 3
2022-12-21 12:15:45.924  INFO 17625 --- [nio-8080-exec-9] c.e.s.service.ActivityService            : Arts and Crafts has been added as an activity!
2022-12-21 12:16:19.886  INFO 17625 --- [io-8080-exec-10] c.e.springproject.service.SignupService  : Suzie Bingham signed up for Arts and Crafts at hour 9!
2022-12-21 12:16:39.615  INFO 17625 --- [nio-8080-exec-1] c.e.springproject.service.CamperService  : Retrieved camper with ID 1
2022-12-21 12:16:39.622  INFO 17625 --- [nio-8080-exec-1] c.e.springproject.service.CamperService  : Found activity signups for camper 1
```

Notice in the log above that the log provides information about the data being
added, retrieved, and deleted.

Refer back to the lessons in this section to help you walk through setting up
the SLF4J logging framework and other logging configurations.

Part of the stretch goals is to implement PUT requests. If you attempt this
stretch goal, try to add logging for when updating data to the data source.

Another stretch goal is to configure the root logging level to INFO and the
application logging level to TRACE. If time allows, you may add additional
trace log statements to your application.

## Resources

- [Spring Logging Documentation](https://docs.spring.io/spring-boot/docs/2.1.18.RELEASE/reference/html/boot-features-logging.html)
- [Lombok Slf4j Annotation Documentation](https://projectlombok.org/api/lombok/extern/slf4j/Slf4j)
