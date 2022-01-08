
We are going to create Form used to order network-services.

Good place to start is <a href="https://developer.servicenow.com/dev.do#!/learn/courses/quebec/app_store_learnv2_aescreateappfromscratch_quebec_create_an_app_from_scratch_with_app_engine_studio">this Servicenow course</a>:


When you have your developer instance up and basic-undestanding of Servicenow we can continue with our own Service-catalog form.

#### GIT:
Github is used to store our demo-project.
You can't add my repository to your Snow directly, create fork first. 
This is also explained in <a href="https://developer.servicenow.com/dev.do#!/learn/learning-plans/quebec/new_to_servicenow/app_store_learnv2_scripting_quebec_exercise_fork_repository_and_import_application_for_the_client_side_scripting_module">Servicenow-documentation</a>

Repository is not yet available, you should try creating app from scratch to have better understanding of all steps.

#### Snow:
First step with SNOW is to create needed credentials for github and Jenkins.
From left navigation search credentials and add "basic auth" credentials for both Git and Jenkins.
With Github you have to use "personal access token" instead of password.

![snow_creds1](https://user-images.githubusercontent.com/22885213/148637912-c41d6728-07c9-493f-b062-13c4f0b0a824.png)

Create Personal Access Token in github settings>Developer Settings and select "write:packages" checkbox and generate token to use as password.


#### Steps:

1. Create new blank app in Studio
2. Create REST Action to Flow Designer
3. Build Flow Designer flow
4. Create Catalog Item

...details below..

##### 1. Create app:
- Find studio from left navigation menu
- From "Select application" window, choose "Create application"
- Give name and description, use scoped -selection > create
- For role you can select 'admin'. See documentation for more details.
- Select 'classic' format
- You can skip table-creation: Done with tables
- Select start from design-screen.
- For table select 'Cisco Apic' > create > Done with apps > Done
- Open your new app from menu.

![studio_create_app1](https://user-images.githubusercontent.com/22885213/148638689-bef1025d-a176-4e68-a89a-ed3466d07be4.png)

##### 2. & 3. - Subflow and REST Action
- In app, select 'Create Application File'
- Type 'flow' in filter field and select 'Flow' from results
- Select subflow and give subflow name when asked, keep other default-values now

  Now you can start subflow definitions:
  - Type inputs first. These values will be asked from user in Catalog-form which we create later
  - First action in flow is REST-message to Jenkins-server. Action > type 'rest' to search-field > select 'IntegrationHub'
  - Here we can see that SNOW-IntegrationHub plugin is needed and you have to install that before we can continue.
  - Find plugins from main-menu and search "Servicenoe IntegrationHub installer" and activate that. Now you have to wait until plugin is activated.
  - <a href="https://developer.servicenow.com/dev.do#!/learn/courses/quebec/app_store_learnv2_rest_quebec_rest_integrations/app_store_learnv2_rest_quebec_rest_in_integrationhub/app_store_learnv2_rest_quebec_activating_integrationhub">Plugin guide in docs</a>
  - Now you have to save your flow and wait.
  - While waiting you can create your catalog :)

##### 4. Create Catalog
- In Studio, select 'Create Application File'
- Find 'Catalog Item' and create that.
- Give name and jump to 'Process Engine' page.

.. to be continued when my tests and plugin activation is ready ..
