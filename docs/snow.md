
We are going to create Form used to order network-services.

Good place to start is <a href="https://developer.servicenow.com/dev.do#!/learn/courses/quebec/app_store_learnv2_aescreateappfromscratch_quebec_create_an_app_from_scratch_with_app_engine_studio">this Servicenow course</a>:


When you have your developer instance up and basic-undestanding of Servicenow we can continue with our own Service-catalog form.

#### GIT:
Github is used to store our demo-project.
You can't add my repository to your Snow directly, create fork first. 
This is also explained in <a href="https://developer.servicenow.com/dev.do#!/learn/learning-plans/quebec/new_to_servicenow/app_store_learnv2_scripting_quebec_exercise_fork_repository_and_import_application_for_the_client_side_scripting_module">Servicenow-documentation</a>

Repository is not yet available, you should try creating app from scratch to have better undestanding of all steps.

#### Snow:
First step with SNOW is to create needed credentials for github and Jenkins.
From left navigation search credentials and add "basic auth" credentials for both Git and Jenkins.
With Github you have to use "personal access token" instead of password.

Create Personal Access Token in github settings>Developer Settings and select "write:packages" checkbox and generate token to use as password.


#### Steps:
 - Create REST Action to Flow Designer
 - Build Flow Designer flow
 - Create Catalog Item

...to be continued..
