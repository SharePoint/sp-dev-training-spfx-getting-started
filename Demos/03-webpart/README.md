# Interact with SPFx Client-Side Web Parts in Modern Sites

In this demo you will add and interact with SharePoint Framework based client-side web parts in a SharePoint Online modern site collection.

1. Open a browser and navigate to the development site you created in the first exercise. If prompted, login using your Work or School credentials.

1. Select the **Pages** link in the left-hand Quick Launch navigation menu.

    ![Screenshot of the SharePoint site's Quick Launch navigation with the Pages library highlighted](./../../Images/ex03-pages-library.png)

1. In the **Pages** library, select the **New** button from the toolbar and select **Site Page** to create a new page.

    ![Screenshot of creating a new modern site page in the Pages library](./../../Images/ex03-new-sitepage.png)

1. Set the name of the page to **Getting Started**.

    ![Screenshot of the page name](./../../Images/ex03-add-webpart-01.png)

1. Select the web part icon button to open the list of available web parts.

    ![Screenshot of the web part icon on the page](./../../Images/ex03-add-webpart-02.png)

1. Select the web part **Text**.

    ![Screenshot of the web part toolbox](./../../Images/ex03-add-webpart-03.png)

1. When the web part is added to the page, add some text and use the rich-text formatting tools provided in the toolbar.

    ![Screenshot of the web part on the page](./../../Images/ex03-add-webpart-04.png)

1. Click **Save as draft** to see the page as your users will see it.

    ![Screenshot of saving the page](./../../Images/ex03-add-webpart-05.png)

    ![Screenshot of the draft page](./../../Images/ex03-add-webpart-06.png)

### Verify your Developer Environment is Configured

> NOTE: The instructions below assume you are using v1.9.1 of the SharePoint Framework Yeoman generator. 

Use the tools installed in exercise 2 to create a new SharePoint Framework component and test it in the local developer environment.

1. Open a command prompt and change to an empty folder where you want to store the files for the project.
1. Run the SharePoint Yeoman generator by executing the following command:

    ```shell
    yo @microsoft/sharepoint
    ```

    Use the following to complete the prompt that is displayed:

    * **What is your solution name?**: HelloWorld
    * **Which baseline packages do you want to target for your component(s)?**: SharePoint Online only (latest)
    * **Where do you want to place the files?**: Use the current folder
    * **Do you want to allow the tenant admin the choice of being able to deploy the solution to all sites immediately without running any feature deployment or adding apps in sites?**: No
    * **Will the components in the solution require permissions to access web APIs that are unique and not shared with other components in the tenant?**: No    
    * **Which type of client-side component to create?**: WebPart
    * **What is your Web part name?**: HelloWorld
    * **What is your Web part description?**: HelloWorld description
    * **Which framework would you like to use?**: No JavaScript framework

    After provisioning the folders required for the project, the generator will install all the dependency packages using NPM.

1. When NPM completes downloading all dependencies, install the developer certificate by executing the following command:

    ```shell
    gulp trust-dev-cert
    ```

1. Run the project by executing the following command:

    ```shell
    gulp serve
    ```

1. The SharePoint Framework's gulp **serve** task will build the project, start a local web server and launch a browser open to the SharePoint Workbench.

    ![Screenshot of the SharePoint Workbench](./../../Images/ex03-testing-01.png)

1. Select the web part icon button to open the list of available web parts.

    ![Screenshot of adding the HelloWorld web part](./../../Images/ex03-testing-02.png)

1. Select the **HelloWorld** web part.

    ![Screenshot of the HelloWorld web part](./../../Images/ex03-testing-03.png)

1. Edit the web part's properties by selecting the pencil (edit) icon in the toolbar to the left of the web part.

    ![Screenshot of the web part edit toolbar](./../../Images/ex03-testing-04.png)

1. In the property pane that opens, change the value of the **Description Field**. Notice how the web part updates as you make changes to the text.

    ![Screenshot of editing the web part property pane](./../../Images/ex03-testing-05.png)

1. Close the browser and stop the local web server by pressing <kbd>CTRL</kbd>+<kbd>C</kbd> in the command prompt.