## Policy Component Demonstration

The [Policy Components with Google Datastore](PolicyComponentsForDataStore) example may be cloned and unit tested with the in-memory database. However a webapp that demonstrates its use is also available here. The demonstration shows the application pane that is used for component manipulation within an empty frame. 

The webapp is configured to run on [Google Appengine](https://cloud.google.com/appengine/) and may be run locally using the [App Engine SDK](https://cloud.google.com/appengine/docs/java/tools/devserver) which can be easily [downloaded](https://cloud.google.com/appengine/docs/java/download). If this is installed then this repository may be cloned and run as follows.

```
{*appengineSDKLocation*}/bin/dev_appserver.sh {*gitDirectory*}/PolicyComponentsDemo/war

```

When the server has completed startup then the application will be running at running at `http://localhost:8080/`. Any Datastore entities created can be viewed at `http://localhost:8080/_ah/admin/datastore` with a namespace of 'GuestUserId'.

A Docker image is also available to run the server.

```
docker run -p 8080:8080  username/application-name

```
If another local port number is preferrable then sibstitute -p *nnnn*:8080 where *nnnn* is the required local port. Running from the Docker image means that Datastore entities will **not** be persisted between runs.

Alternatively the application is hosted [here](https://quick-composite-90109.appspot.com), though the response times are often very poor.
___

#### Usage 

The example is presented with in an empty frame without the bulk of the application. Right clicking within the table shows the menu and allows a new component to be created.

 <p align="center">
<img src="https://github.com/srbaird/PolicyComponentsDemo/blob/master/images/Right click.jpg" alt="Right click menu"  >

The available component types are shown for selection. Choose one and press 'OK'. This will create a new policy component.

 <p align="center">
<img src="https://github.com/srbaird/PolicyComponentsDemo/blob/master/images/Create menu.jpg" alt="Create component popup"  >

The table will display the new component. At the far right of the row is a 'Settings' type icon. Clicking on this will show the available options for that row. 

 <p align="center">
<img src="https://github.com/srbaird/PolicyComponentsDemo/blob/master/images/Options menu.jpg" alt="Create new relationhip menu"  >

Selecting the 'New relationship...' option presents a popup which allows a relation to another component to be established. Once the relationship type and the target component are selected then pressing 'Ok' will create the association. In this example only one component has been created so only a self referential relationship is available. 

 <p align="center">
<img src="https://github.com/srbaird/PolicyComponentsDemo/blob/master/images/Relationship popup.jpg" alt="Create new relationhip popup"  >

Once complete the component and its relationships will be displayed.

 <p align="center">
<img src="https://github.com/srbaird/PolicyComponentsDemo/blob/master/images/New%20Relationship.jpg" alt="Relationship structure"  >



