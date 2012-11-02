Secure RESTful Services with Maven, Spring, Apache CXF and Spring Security.

See http://blogs.justenougharchitecture.com/?p=499 for more detials.

Type in one of the following URL’s to access the service:
- Unsecure – http://localhost:8080/jaxrscxf/services/timeoftheday/asplaintext
- secure json response – http://localhost:8080/jaxrscxf/services/timeoftheday/asjson/mathew
- secure xml response – http://localhost:8080/jaxrscxf/services/timeoftheday/asxml/mathew


If you need to push this code to the open source PaaS Cloudfoundry.com then follow these instructions (of course refer to Cloudfoundy website too)...
- First get an account at cloudfoundry.com (hereafter referred to as CF). Whether you chose to go micro CF or the hosted version is your call. I assume hosted here. Note down the one time token.
- Ensure you have ruby and rubygems installed.
- run - *gems install vmc* (vmc is the command line tool to interact with CF)
- run - *vmc target http://api.mattscloud.cloudfoundry.me/* (where mattscloud is your cf account). Use your one time token during this step.
- Go to the maven project root folder and run *mvn package*.
- Move to the target folder where the war file resides.
- run - *vmc login* (login using your CF credentials)
- run - *vmc push jaxrscxf*  (to delete the deployed application run *vmc delete jaxrscxf*)
