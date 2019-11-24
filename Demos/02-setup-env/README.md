# Setup your local SPFx Developer Environment

In this demo you will setup your local developer environment with everything you need start creating SharePoint Framework components.

### Install a Code Editor

You will need a text editor to edit your code files. There are no requirements for what you need in a text editor.

The remainder of this lab and most of the examples you'll find from Microsoft use [Visual Studio Code](https://code.visualstudio.com/).

### Install Node.js

The tools used in compiling, debugging, and packaging SharePoint Framework projects are built using Node.js, a runtime that enables JavaScript to run locally versus in a browser. Therefore the first step is to install the runtime, Node.js, before installing the required tools.

> Node.js is available in two different releases: the long term support release (aka: LTS) is the most stable version that is recommended for most users while the current version contains the latest features.
> Before installing Node.js, you should verify you haven't installed it previously. Open a command prompt or terminal (depending on your developer platform) and execute the following command:
>
> ```shell
> node -v
> ```
>
> If a version number is returned, you already have Node.js. The version(s) of Node.js you may use depends on the environment(s) you will be targeting. If you will be targeting SharePoint Server 2016, you must use Node.js version 8.x. If you will be targeting SharePoint Server 2019 and/or SharePoint Online, then you can use either Node.js version 8.x or Node.js version 10.x. 

If you already have a version of Node.js that is compatible with the environment(s) you will be targeting, then skip to the next section.

1. Open a browser and navigate to the Node.js Foundation site: https://www.nodejs.org.

    Note that the LTS version is currently 12.x so you will need to navigate further into the site to find the appropriate installer.

1. Select **Downloads** from the top menu navigation then scroll to the bottom of the page and select **Previous Releases**.

    ![Screenshot of the Downloads page](./../../Images/ex02-installnode-02.png)

1. In the Previous Releases page, select Node.js 8.x if you will be targeting SharePoint Server 2016 or Node.js 10.x if you will be targeting SharePoint Server 2019 and/or SharePoint Online.

    ![Screenshot of the Previous Releases page](./../../Images/ex02-installnode-03.png)

1. Download the appropriate installer or binary for the platorm you are using.

    ![Screenshot of the Node.js 10.x page](./../../Images/ex02-installnode-04.png)

1. Run the installer, accepting all the default options. This will install Node.js and NPM (*a package manager that Node.js uses, similar to .NET's NuGet*).

### Install Required Tools

The SharePoint Framework development experience utilizes a set of tools built on Node.js that are popular among web developers. These tools are built on Node.js which means they can be used on any platform and will work the same way. This includes Windows, macOS and Linux.

1. Install Yeoman - http://yeoman.io

    Yeoman is a scaffolding engine which executes *generators* that prompt the user with questions. Based on the answers to these questions, Yeoman then creates the folders and files defined by the generator.

      1. Open a command prompt / terminal window and execute the following command to install Yeoman globally with NPM:

          ```shell
          npm install --global yo
          ```

1. Install the SharePoint Framework Yeoman generator.

    Microsoft has created a Yeoman generator for scaffolding SharePoint Framework projects.

      1. Open a command prompt / terminal window and execute the following command to install the SharePoint Framework Yeoman generator globally with NPM:

          ```shell
          npm install --global @microsoft/generator-sharepoint
          ```

1. Install Gulp - https://gulpjs.com

    Gulp is a task runner utility. It's similar to MSBuild, a tool used by .NET developers and Visual Studio to compile projects, package solutions into redistributes and start a debugging experience.

      1. Open a command prompt / terminal window and execute the following command to install Gulp globally with NPM:

          ```shell
          npm install --global gulp
          ```