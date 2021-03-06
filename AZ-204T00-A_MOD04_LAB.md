# **Lab: Constructing a polyglot data solution**

# **Student lab answer key**

Exercise 1: Creating database resources in Azure

Task 1: Open the Azure portal

1. On the     taskbar, select the **Microsoft Edge** icon.
2. In the     open browser window, browse to the Azure portal ([portal.azure.com](https://portal.azure.com/)).
3. Enter     the email address for your Microsoft account, and then select **Next**.
4. Enter     the password for your Microsoft account, and then select **Sign in**.

**Note**: If this is your first time signing in to the Azure portal, you will be offered a tour of the portal. Select **Get Started** to skip the tour and begin using the portal.

 

 

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image002.png)

 

 

Task 2: Create an Azure SQL Database server resource

1. In the     Azure portal’s navigation pane, select **All services**.
2. From     the **All services** blade, select **SQL servers**.
3. From     the **SQL servers** blade, find your list of SQL server     instances.
4. From     the **SQL servers** blade, select **Add**.
5. From     the **Create SQL Database Server** blade, observe the tabs     from the blade, such as **Basics**, **Networking**,     and **Additional settings**.

**Note**: Each tab represents a step in the workflow to create a new Azure SQL Database server. You can select **Review + Create** at any time to skip the remaining tabs.

1. 1. From      the **Basics** tab, perform the following actions:
   2. Leave      the **Subscription** drop-down list set to its default      value.
   3. In      the **Resource group** section, select **Create new**,      enter **PolyglotData**, and then select **OK**.
   4. In      the **Server name** text box, enter **polysqlsrvr \*[yourname]\***.
   5. In      the **Location** drop-down list, select **(US) East US**.
   6. In      the **Server admin login** text box, enter **testuser**.
   7. In      the **Password** text box, enter **TestPa55w.rd**.
   8. In      the **Confirm password** text box, enter **TestPa55w.rd** again.

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image004.png)

1. 1. Select **Next:      Networking**.

2. From     the **Networking** tab, perform the following actions:

1. 1. In      the **Allow Azure services and resources to access this server** section,      select **Yes**.
   2. Select **Review      + Create**.

2. From     the **Review + Create** tab, review the options that you     selected during the previous steps.

3. Select **Create** to     create the SQL Database server by using your specified configuration.

**Note**: At this point in the lab, we are only creating the Azure SQL logical server. We will create the Azure SQL database instance later in the lab.

**Note**: Wait for the creation task to complete before you move forward with this lab.

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image006.png)

Task 3: Create an Azure Cosmos DB account resource

1. In the     Azure portal’s navigation pane, select **All services**.
2. From     the **All services** blade, select **Azure Cosmos DB**.
3. From     the **Azure Cosmos DB** blade, find your list of Azure Cosmos     DB instances.
4. From     the **Azure Cosmos DB** blade, select **Add**.
5. From     the **Create Azure Cosmos DB Account** blade, observe the     tabs from the blade, such as **Basics**, **Network**,     and **Tags**.

**Note**: Each tab represents a step in the workflow to create a new Azure Cosmos DB account. You can select **Review + Create** at any time to skip the remaining tabs.

1. From     the **Basics** tab, perform the following actions:

1. 1. Leave      the **Subscription** list set to its default value.
   2. In      the **Resource group** section, select **PolyglotData** from      the list.
   3. In      the **AccountName** text box, enter **polycosmos\*[yourname]\***.
   4. In the **API** drop-down      list, select **Core (SQL)**.
   5. In      the **Notebooks (Preview)** section, select **Off**.
   6. In      the **Apply Free Tier Discount** section, select **Do      Not Apply**.
   7. In      the **Location** drop-down list, select the **(US)      East US** region.
   8. In      the **Account Type** section, select **Non-Production**.
   9. In      the **Multi-region Writes** section, select **Disable**.
   10. Select **Review      + Create**.

2. From     the **Review + Create** tab, review the options that you     selected during the previous steps.

3. Select **Create** to     create the Azure Cosmos DB account by using your specified configuration.

**Note**: Wait for the creation task to complete before you move forward with this lab.

​      ![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image008.png)

1. In the     Azure portal’s navigation pane, select the **Resource groups** link.
2. From     the **Resource groups** blade, find and then select the **PolyglotData** resource     group that you created earlier in this lab.
3. From     the **PolyglotData** blade, select the **polycosmos\*[yourname]\*** Azure     Cosmos DB account that you created earlier in this lab.
4. From     the **Azure Cosmos DB account** blade, find the **Settings** section     from the blade, and then select the **Keys** link.
5. In     the Keys pane, record the value in the **PRIMARY     CONNECTION STRING** text box. You’ll use this value later in this     lab.

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image010.png)

 

PRIMARY CONNECTION STRING

AccountEndpoint=https://polycosmosjvtc.documents.azure.com:443/;AccountKey=KDQ9QVDTMjobKd222xlnXaoM7LHfrG6taST4YjP0JBxmQxKL63JWoJPKvW0yukSIiLHSJgB9WSwp2ijrr8vzLg==;

Task 4: Create an Azure Storage account resource

1. In the     Azure portal’s navigation pane, select **All services**.
2. From     the **All services** blade, select **Storage Accounts**.
3. From     the **Storage accounts** blade, find your list of Storage     instances.
4. From     the **Storage accounts** blade, select **Add**.
5. From     the **Create storage account** blade, observe the tabs from     the blade, such as **Basics**, **Advanced**, and **Tags**.

**Note**: Each tab represents a step in the workflow to create a new Azure Storage account. You can select **Review + Create** at any time to skip the remaining tabs.

1. From     the **Basics** tab, perform the following actions:

1. 1. Leave      the **Subscription** list set to its default value.
   2. In      the **Resource group** section, select **PolyglotData** from      the list.
   3. In      the **Storage account name** text box, enter **polystor\*[yourname]\***.
   4. In      the **Location** drop-down list, select the **(US)      East US** region.
   5. In      the **Performance** section, select **Standard**.
   6. In      the **Account kind** drop-down list, select **StorageV2      (general purpose v2)**.
   7. In      the **Replication** drop-down list, select **Locally-redundant      storage (LRS)**.
   8. In      the **Access tier (default)** section, ensure that **Hot** is      selected.
   9. Select **Review      + Create**.

2. From     the **Review + Create** tab, review the options that you     selected during the previous steps.

3. Select **Create** to     create the storage account by using your specified configuration.

**Note**: Wait for the creation task to complete before you move forward with this lab.

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image012.png)

Review

In this exercise, you created all the Azure resources that you’ll need for a polyglot data solution.

Exercise 2: Import and validate data

Task 1: Upload image blobs

1. In the     Azure portal’s navigation pane, select the **Resource groups** link.
2. From     the **Resource groups** blade, find and select the **PolyglotData** resource     group that you created earlier in this lab.
3. From     the **PolyglotData** blade, select the **polystor\*[yourname]\*** storage     account that you created earlier in this lab.
4. From     the **Storage account** blade, select the **Containers** link     in the **Blob service** section from the blade.
5. In     the **Containers** section, select **+ Container**.
6. In     the **New container** ollowing actions:

1. 1. In      the **Name** text box, enter **images**.
   2. In      the **Public access level** drop-down list, select **Blob      (anonymous read access for blobs only)**.
   3. Select **OK**.

2. Back in     the **Containers** section, select the newly created **images** container.

3. From     the **Container** blade, find the **Settings** section     from the blade, and then select the **Properties** link.

4. In the     Properties pane, record the value in the **URL** text box.     You’ll use this value later in this lab.

 

 

https://polystorjvtc.blob.core.windows.net/images

 

1. Find     and select the **Overview** link from the blade.
2. From     the blade, select **Upload**.
3. In     the **Upload blob** pop-up, perform the following actions:

1. 1. In      the **Files** section, select the **Folder** icon.
   2. In      the **File Explorer** window, browse to **Allfiles      (F):\Allfiles\Labs\04\Starter\Images**, select all 42 individual **.jpg** image      files, and then select **Open**.
   3. Ensure      that **Overwrite if files already exist** is selected, and      then select **Upload**.

 

**Note**: Wait for all the blobs to upload before you continue with this lab.

Task 2: Upload an SQL .bacpac file

1. In the     Azure portal’s navigation pane, select the **Resource groups** link.
2. From     the **Resource groups** blade, find and select the **PolyglotData** resource     group that you created earlier in this lab.
3. From     the **PolyglotData** blade, select the **polystor\*[yourname]\*** storage     account that you created earlier in this lab.
4. From     the **Storage account** blade, select the **Containers** link     in the **Blob service** section from the blade.
5. In     the **Containers** section, select **+ Container**.
6. In     the **New container** pop-up, perform the following actions:

1. 1. In      the **Name** text box, enter **databases**.
   2. In      the **Public access level** drop-down list, select **Private      (no anonymous access)**.
   3. Select **OK**.

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image014.png)

 

 

 

 

 

1. Back in     the **Containers** section, select the newly created **databases** container.
2. From     the **Container** blade, select **Upload**.
3. In     the **Upload blob** pop-up, perform the following actions:

1. 1. In      the **Files** section, select the **Folder** icon.
   2. In      the **File Explorer** window, browse to **Allfiles      (F):\Allfiles\Labs\04\Starter**, select the **AdventureWorks.bacpac** file,      and then select **Open**.
   3. Ensure      that **Overwrite if files already exist** is selected, and      then select **Upload**.

**Note**: Wait for the blob to upload before you continue with this lab.

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image016.png)

 

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image018.png)

 

 

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image020.png)

 

 

Task 3: Import an SQL database

1. In the     Azure portal’s navigation pane, select the **Resource groups** link.
2. From     the **Resource groups** blade, find and select the **PolyglotData** resource     group that you created earlier in this lab.
3. From     the **PolyglotData** blade, select the **polysqlsrvr\*[yourname]\*** SQL     server that you created earlier in this lab.
4. From     the **SQL server** blade, select **Import database**.
5. From     the **Import database** blade, perform the following actions:

1. 1. Leave      the **Subscription** list set to its default value.
   2. Select      the **Storage** option.

 

1. 1. From      the **Storage accounts** blade, select the **polystor\*[yourname]\*** storage      account that you created earlier in this lab.
   2. From      the **Containers** blade, select the **databases** container      that you created earlier in this lab.
   3. From      the **Container** blade, select the **AdventureWorks.bacpac** blob      that you created earlier in this lab, and then select **Select** to      close the blade.
   4. Back      from the **Import database** blade, leave the **Pricing      tier** option set to its default value.
   5. In      the **Database name** text box, enter **AdventureWorks**.
   6. Leave      the **Collation** text box set to its default value.
   7. In      the **Server admin login** text box, enter **testuser**.
   8. In      the **Password** text box, enter **TestPa55w.rd**.
   9. Select **OK**.

2. ![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image022.png)

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image023.png)

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image025.png)

**Note**: Wait for the database to be created before you continue with this lab. If you receive a firewall-related error on the import step, it means you did not correctly configure the **Allow Azure services to access server** setting on your SQL Server earlier in the lab. Review your settings, delete the empty **AdventureWorks** database, and then attempt your import again.

Task 4: Use an imported SQL database

1. In the     Azure portal’s navigation pane, select the **Resource groups** link.
2. From     the **Resource groups** blade, find and select the **PolyglotData** resource     group that you created earlier in this lab.
3. From     the **PolyglotData** blade, select the **polysqlsrvr\*[yourname]\*** SQL     server that you created earlier in this lab.
4. From     the **SQL server** blade, find the **Security** section     from the blade, and then select the **Firewalls and virtual networks** link.
5. In the     Firewalls and virtual networks pane, perform the following actions:

1. 1. Select **Add      client IP**
   2. Select **Save**.
   3. In      the **Success!** confirmation dialog, select **OK**.

**Note**: This step will ensure that your local machine will have access to the databases that are associated with this server.

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image027.png)

88.1.197.251

1. In the     Azure portal’s navigation pane, select the **Resource groups** link.
2. From     the **Resource groups** blade, find and select the **PolyglotData** resource     group that you created earlier in this lab.
3. From     the **PolyglotData** blade, select the **AdventureWorks** SQL     database that you created earlier in this lab.
4. From     the **SQL database** blade, find the **Settings** section     from the blade, and then select the **Connection strings** link.

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image029.png)

 

 

1. In the     Connection strings pane, record the value in the **ADO.NET (SQL     Authentication)** text box. You’ll use this value later in this     lab.

 

Server=tcp:polysqlsrvrjvtc.database.windows.net,1433;Initial Catalog=polysqlsrvrjvtc;Persist Security Info=False;User ID=testuser;Password=**TestPa55w.rd**;MultipleActiveResultSets=False;Encrypt=True;TrustServerCertificate=False;Connection Timeout=30;

 

1. Update     the connection string that you recorded by performing the following     actions:

1. 1. Within      the connection string, find the *your_username* placeholder      and replace it with **testuser**.
   2. Within      the connection string, find the *your_password* placeholder      and replace it with **TestPa55w.rd**.

**Note**: For example, if your connection string was originally Server=tcp:polysqlsrvrinstructor.database.windows.net,1433;Initial Catalog=AdventureWorks;User ID={your_username};Password={your_password};, your updated connection string will be Server=tcp:polysqlsrvrinstructor.database.windows.net,1433;Initial Catalog=AdventureWorks;User ID=testuser;Password=TestPa55w.rd;

1. Find     and select the **Query editor (preview)** link from the     blade.
2. In the     Query editor pane, perform the following actions:

1. 1. In the **Login** text      box, enter **testuser**.
   2. In      the **Password** text box, enter **TestPa55w.rd**.
   3. Select **OK**.

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image031.png)

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image033.png)

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image035.png)

1. In the     open query editor, enter the following query:

CodeCopy

SELECT * FROM AdventureWorks.dbo.Models

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image036.png)

1. Select **Run** to     run the query, and then observe the results.

**Note**: This query will return a list of models from the home page of the web application.

1. In the     query editor, replace the existing query with the following query:

CodeCopy

SELECT * FROM AdventureWorks.dbo.Products

1. Select **Run** to     run the query, and then observe the results.

**Note**: This query will return a list of products that are associated with each model.

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image038.png)

Review

In this exercise, you imported all the resources that you’ll use with your web application.

Exercise 3: Open and configure a .NET web application

Task 1: Open and build the web application

1. On     the **Start** screen, select the **Visual Studio Code** tile.
2. From     the **File** menu, select **Open Folder**.
3. In     the **File Explorer** window that opens, browse to **Allfiles     (F):\Allfiles\Labs\04\Starter\AdventureWorks**, and then select **Select     Folder**.
4. In     the **Visual Studio Code** window, right-click or activate     the shortcut menu for the Explorer pane, and then select **Open in     Terminal**.
5. At the     open command prompt, enter the following command, and then select Enter to     build the .NET web application:

CodeCopy

dotnet build

**Note**: The **dotnet build** command will automatically restore any missing NuGet packages prior to building all projects in the folder.

 

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image040.png)

 

1. Observe     the results of the build printed in the terminal. The build should     complete successfully with no errors or warning messages.
2. Select **Kill     Terminal** or the **Recycle Bin** icon to close the     currently open terminal and any associated processes.

Task 2: Update the SQL connection string

1. In the Explorer pane     of the **Visual Studio Code** window, expand the **AdventureWorks.Web** project.
2. Open     the **appsettings.json** file.
3. In the     JavaScript Object Notation (JSON) object on line 3, find the **ConnectionStrings.AdventureWorksSqlContext** path.     Observe that the current value is empty:

CodeCopy

"ConnectionStrings": {

  "AdventureWorksSqlContext": "",

  ...

},

1. Update     the value of the **AdventureWorksSqlContext** property by     setting its value to the **ADO.NET (SQL Authentication) connection     string** of the SQL database that you recorded earlier in     this lab.

**Note**: It’s important that you use your updated connection string here. The original connection string copied from the portal won’t have the username and password necessary to connect to the SQL database.

1. Save     the **appsettings.json** file.

Task 3: Update the blob base URL

1. In the     JSON object on line 8, find the **Settings.BlobContainerUrl** path.     Observe that the current value is empty:

CodeCopy

"Settings": {

  "BlobContainerUrl": "",

  ...

}

1. Update     the value of the **BlobContainerUrl** property by setting its     value to the **URL** property of the Azure Storage blob     container named **images** that you recorded earlier in this     lab.
2. Save     the **appsettings.json** file.

Task 4: Validate the web application

1. In     the **Visual Studio Code** window, access the shortcut menu     or right-click or activate the shortcut menu for the Explorer pane, and     then select **Open in Terminal**.
2. At the     open command prompt, enter the following command, and then select Enter to     switch your terminal context to the **AdventureWorks.Web** folder:

CodeCopy

cd .\AdventureWorks.Web\

1. At the     command prompt, enter the following command, and then select Enter to run     the .NET web application:

CodeCopy

dotnet run

**Note**: The **dotnet run** command will automatically build any changes to the project and then start the web application without a debugger attached. The command will output the URL of the running application and any assigned ports.

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image042.png)

1. On the     taskbar, select the **Microsoft Edge** icon.
2. In the     open browser window, browse to the currently running web application ([http://localhost:5000](http://localhost:5000/)).
3. In the     web application, observe the list of models displayed from the front page.
4. Find     the **Water Bottle** model, and then select **View     Details**.
5. From     the **Water Bottle** product detail page, find **Add to     Cart**, and then observe that the checkout functionality is currently     disabled.
6. Close     the browser window displaying your web application.
7. Return     to the **Visual Studio Code** window, and then select **Kill     Terminal** or the **Recycle Bin** icon to close the     currently open terminal and any associated processes.

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image044.png)

Review

In this exercise, you configured your ASP.NET web application to connect to your resources in Azure.

Exercise 4: Migrating SQL data to Azure Cosmos DB

Task 1: Create a migration project

1. In     the **Visual Studio Code** window, access the shortcut menu     or right-click or activate the shortcut menu for the Explorer pane, and     then select **Open in Terminal**.
2. At the     open command prompt, enter the following command, and then select Enter to     create a new .NET console project named **AdventureWorks.Migrate** in     a folder with the same name:

CodeCopy

dotnet new console --name AdventureWorks.Migrate -f netcoreapp3.0::5.0.1

**Note**: The **dotnet new** command will create a new **console** project in a folder with the same name as the project.

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image046.png)

1. At the     command prompt, enter the following command, and then select Enter to add     a reference to the existing **AdventureWorks.Models** project:

CodeCopy

dotnet add .\AdventureWorks.Migrate\AdventureWorks.Migrate.csproj reference .\AdventureWorks.Models\AdventureWorks.Models.csproj

**Note**: The **dotnet add reference** command will add a reference to the model classes contained in the **AdventureWorks.Models** project.

1. At the command     prompt, enter the following command, and then select Enter to add a     reference to the existing **AdventureWorks.Context** project:

CodeCopy

dotnet add .\AdventureWorks.Migrate\AdventureWorks.Migrate.csproj reference .\AdventureWorks.Context\AdventureWorks.Context.csproj

**Note**: The **dotnet add reference** command will add a reference to the context classes contained in the **AdventureWorks.Context** project.

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image048.png)

1. At the     command prompt, enter the following command, and then select Enter to     switch your terminal context to the **AdventureWorks.Migrate** folder:

CodeCopy

cd .\AdventureWorks.Migrate\

1. At the     command prompt, enter the following command, and then select Enter to     import version 2.2.6 of **Microsoft.EntityFrameworkCore.SqlServer** from     NuGet:

CodeCopy

dotnet add package Microsoft.EntityFrameworkCore.SqlServer --version 3.0.1

**Note**: The **dotnet add package** command will add the **Microsoft.EntityFrameworkCore.SqlServer** package from **NuGet**. For more information, go to: [Microsoft.EntityFrameworkCore.SqlServer](https://www.nuget.org/packages/Microsoft.EntityFrameworkCore.SqlServer/3.0.1).

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image050.png)

1. At the     command prompt, enter the following command, and then select Enter to     import version 3.4.1 of **Microsoft.Azure.Cosmos** from     NuGet:

CodeCopy

dotnet add package Microsoft.Azure.Cosmos --version 3.4.1

**Note**: The **dotnet add package** command will add the **Microsoft.Azure.Cosmos** package from **NuGet**. For more information, go to: [Microsoft.Azure.Cosmos](https://www.nuget.org/packages/Microsoft.Azure.Cosmos/3.4.1).

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image052.png)

1. At the     command prompt, enter the following command, and then select Enter to     build the .NET console application:

CodeCopy

dotnet build

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image054.png)

1. Select **Kill     Terminal** or the **Recycle Bin** icon to close the     currently open terminal and any associated processes.

Task 2: Create a .NET class

1. In     the Explorer pane of the **Visual Studio Code** window,     expand the **AdventureWorks.Migrate** project.
2. Open     the **Program.cs** file.
3. From     the code editor tab for the **Program.cs** file, delete all     the code in the existing file.
4. Add the     following lines of code to import the **AdventureWorks.Models** and **AdventureWorks.Context** namespaces     from the referenced **AdventureWorks.Models** and **AdventureWorks.Context** projects:

CodeCopy

using AdventureWorks.Context;

using AdventureWorks.Models;

1. Add the     following line of code to import the **Microsoft.Azure.Cosmos** namespace     from the **Microsoft.Azure.Cosmos** package imported from     NuGet:

CodeCopy

using Microsoft.Azure.Cosmos;

1. Add the     following line of code to import the **Microsoft.EntityFrameworkCore** namespace     from the **Microsoft.EntityFrameworkCore.SqlServer** package     imported from NuGet:

CodeCopy

using Microsoft.EntityFrameworkCore;

1. Add the     following lines of code to add **using** directives for the     built-in namespaces that will be used in this file:

CodeCopy

using System;

using System.Collections.Generic;

using System.Linq;

using System.Threading.Tasks;

1. Enter     the following code to create a new **Program** class:

CodeCopy

public class Program

{

}

1. Within     the **Program** class, enter the following line of code to     create a new string constant named **sqlDBConnectionString**:

CodeCopy

private const string sqlDBConnectionString = "";

1. Update     the **sqlDBConnectionString** string constant by setting its     value to the **ADO.NET (SQL Authentication) connection string** of     the SQL database that you recorded earlier in this lab.

**Note**: It’s important that you use your updated connection string here. The original connection string copied from the portal won’t have the username and password necessary to connect to the SQL database.

1. Within     the **Program** class, enter the following line of code to     create a new string constant named **cosmosDBConnectionString**:

CodeCopy

private const string cosmosDBConnectionString = "";

1. Update the **cosmosDBConnectionString** string     constant by setting its value to the **PRIMARY CONNECTION STRING** of     the Azure Cosmos DB account that you recorded earlier in this lab.
2. Within     the **Program** class, enter the following code to create a     new asynchronous **Main** method:

CodeCopy

public static async Task Main(string[] args)

{

}

1. Within     the **Main** method, add the following line of code to print     an introductory message to the console:

CodeCopy

await Console.Out.WriteLineAsync("Start Migration");

1. Save     the **Program.cs** file.
2. In     the **Visual Studio Code** window, access the shortcut menu     or right-click or activate the shortcut menu for the Explorer pane, and     then select **Open in Terminal**.
3. At the     open command prompt, enter the following command, and then select Enter to     switch your terminal context to the **AdventureWorks.Migrate** folder:

CodeCopy

cd .\AdventureWorks.Migrate\

1. At the     command prompt, enter the following command, and then select Enter to     build the .NET console application:

CodeCopy

dotnet build

1. Select **Kill     Terminal** or the **Recycle Bin** icon to close the     currently open terminal and any associated processes.

Task 3: Get SQL database records by using Entity Framework

1. Within     the **Main** method of the **Program** class     within the **Program.cs** file, add the following line of     code to create a new instance of the **AdventureWorksSqlContext** class,     passing in the *sqlDBConnectionString* variable as the     connection string value:

CodeCopy

using AdventureWorksSqlContext context = new AdventureWorksSqlContext(sqlDBConnectionString);

1. Within     the **Main** method, add the following block of code to issue     a language-integrated query (LINQ) to get all **Models** and     child **Products** from the database and store them in an     in-memory **List<>** collection:

CodeCopy

List<Model> items = await context.Models

  .Include(m => m.Products)

  .ToListAsync<Model>();

1. Within     the **Main** method, add the following line of code to print     the number of records imported from SQL Database:

CodeCopy

await Console.Out.WriteLineAsync($"Total Azure SQL DB Records: {items.Count}");

1. Save     the **Program.cs** file.
2. In     the **Visual Studio Code** window, access the shortcut menu     or right-click or activate the shortcut menu for the Explorer pane, and     then select **Open in Terminal**.
3. At the     open command prompt, enter the following command, and then select Enter to     switch your terminal context to the **AdventureWorks.Migrate** folder:

CodeCopy

cd .\AdventureWorks.Migrate\

1. At the     command prompt, enter the following command, and then select Enter to     build the .NET console application:

CodeCopy

dotnet build

**Note**: If there are any build errors, review the **Program.cs** file in the **Allfiles (F):\Allfiles\Labs\04\Solution\AdventureWorks\AdventureWorks.Migrate** folder.

1. Select **Kill     Terminal** or the **Recycle Bin** icon to close the     currently open terminal and any associated processes.

Task 4: Insert items into Azure Cosmos DB

1. Within     the **Main** method of the **Program** class     within the **Program.cs** file, add the following line of     code to create a new instance of the **CosmosClient** class,     passing in the *cosmosDBConnectionString* variable as the     connection string value:

CodeCopy

using CosmosClient client = new CosmosClient(cosmosDBConnectionString);

1. Within     the **Main** method, add the following line of code to create     a new **database** named **Retail** if it doesn’t     already exist in the Azure Cosmos DB account:

CodeCopy

Database database = await client.CreateDatabaseIfNotExistsAsync("Retail");

1. Within     the **Main** method, add the following block of code to     create a new **container** named **Online** if     it doesn’t already exist in the Azure Cosmos DB account with a partition     key path of **/Category** and a throughput of **1000** Request     Units:

CodeCopy

Container container = await database.CreateContainerIfNotExistsAsync("Online",

  partitionKeyPath: $"/{nameof(Model.Category)}",

  throughput: 1000

);

1. Within     the **Main** method, add the following line of code to create     an *int* variable named **count**:

CodeCopy

int count = 0;

1. Within     the **Main** method, add the following block of code to     create a **foreach** loop that iterates over the objects in     the **items** collection:

CodeCopy

foreach (var item in items)

{

}

1. Within     the **foreach** loop in the **Main** method, add     the following line of code to **upsert** the object into the     Azure Cosmos DB collection and save the result in a variable of type *ItemResponse<>* named **document**:

CodeCopy

ItemResponse<Model> document = await container.UpsertItemAsync<Model>(item);

1. Within     the **foreach** loop contained in the **Main** method,     add the following line of code to print the activity ID of each upsert     operation:

CodeCopy

await Console.Out.WriteLineAsync($"Upserted document #{++count:000} [Activity Id: {document.ActivityId}]");

1. Back     within the **Main** method (outside of the **foreach** loop),     add the following line of code to print the number of documents exported     to Azure Cosmos DB:

CodeCopy

await Console.Out.WriteLineAsync($"Total Azure Cosmos DB Documents: {count}");

1. Save     the **Program.cs** file.
2. In     the **Visual Studio Code** window, access the shortcut menu     or right-click or activate the shortcut menu for the Explorer pane, and     then select **Open in Terminal**.
3. At the     open command prompt, enter the following command, and then select Enter to     switch your terminal context to the **AdventureWorks.Migrate** folder:

CodeCopy

cd .\AdventureWorks.Migrate\

1. At the     command prompt, enter the following command, and then select Enter to     build the .NET console application:

CodeCopy

dotnet build

**Note**: If there are any build errors, review the **Program.cs** file in the **Allfiles (F):\Allfiles\Labs\04\Solution\AdventureWorks\AdventureWorks.Migrate** folder.

 

 

 

Task 5: Perform a migration

1. At the     open command prompt, enter the following command, and then select Enter to     run the .NET console application:

CodeCopy

dotnet run

**Note**: The **dotnet run** command will start the console application.

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image056.png)

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image058.png)

1. Observe     the various data that prints to the screen, including initial SQL record     count, individual upsert activity identifiers, and final Azure Cosmos DB     document count.
2. Select **Kill     Terminal** or the **Recycle Bin** icon to close the     currently open terminal and any associated processes.

Task 6: Validate the migration

1. Return     to the **Microsoft Edge** browser window with the Azure     portal.
2. In the     Azure portal’s navigation pane, select the **Resource groups** link.
3. From     the **Resource groups** blade, find and select the **PolyglotData** resource     group that you created earlier in this lab.
4. From     the **PolyglotData** blade, select the **polycosmos\*[yourname]\*** Azure     Cosmos DB account that you created earlier in this lab.
5. From     the **Azure Cosmos DB account** blade, find and select     the **Data Explorer** link from the blade.
6. In the     Data Explorer pane, expand the **Retail** database node.
7. Expand     the **Online** container node, and then select **New     SQL Query**.

**Note**: The label for this option might be hidden. You can get labels by hovering over the icons in the Data Explorer pane.

1. From     the query tab, enter the following text:

CodeCopy

SELECT * FROM models

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image060.png)

1. Select **Execute     Query**, and then observe the list of JSON models that the query     returns.
2. Back in     the query editor, replace the existing text with the following text:

CodeCopy

SELECT VALUE COUNT(1) FROM models

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image062.png)

1. Select **Execute     Query**, and then observe the result of the **COUNT** aggregate     operation.
2. Return     to the **Visual Studio Code** window.

Review

In this exercise, you used Entity Framework and the .NET SDK for Azure Cosmos DB to migrate data from SQL Database to Azure Cosmos DB.

Exercise 5: Accessing Azure Cosmos DB by using .NET

Task 1: Update library with the Cosmos SDK and references

1. In     the **Visual Studio Code** window, access the shortcut menu     or right-click or activate the shortcut menu for the Explorer pane, and     then select **Open in Terminal**.
2. At the     open command prompt, enter the following command, and then select Enter to     switch your terminal context to the **AdventureWorks.Context** folder:

CodeCopy

cd .\AdventureWorks.Context\

1. At the     command prompt, enter the following command, and then select Enter to     import **Microsoft.Azure.Cosmos** from NuGet:

CodeCopy

dotnet add package Microsoft.Azure.Cosmos --version 3.4.1

**Note**: The **dotnet add package** command will add the **Microsoft.Azure.Cosmos** package from **NuGet**. For more information, go to: [Microsoft.Azure.Cosmos](https://www.nuget.org/packages/Microsoft.Azure.Cosmos/3.4.1).

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image064.png)

1. At the     command prompt, enter the following command, and then select Enter to     build the .NET web application:

CodeCopy

dotnet build

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image066.png)

1. Select **Kill     Terminal** or the **Recycle Bin** icon to close the     currently open terminal and any associated processes.

Task 2: Write .NET code to connect to Azure Cosmos DB

1. In     the Explorer pane of the **Visual Studio Code** window,     expand the **AdventureWorks.Context** project.
2. Access     the shortcut menu or right-click or activate the shortcut menu for     the **AdventureWorks.Context** folder node, and then     select **New File**.
3. At the     new file prompt, enter **AdventureWorksCosmosContext.cs**.
4. From     the code editor tab for the **AdventureWorksCosmosContext.cs** file,     add the following lines of code to import the **AdventureWorks.Models** namespace     from the referenced **AdventureWorks.Models** project:

CodeCopy

using AdventureWorks.Models;

1. Add the     following lines of code to import the **Microsoft.Azure.Cosmos** and **Microsoft.Azure.Cosmos.Linq** namespaces     from the **Microsoft.Azure.Cosmos** package imported from     NuGet:

CodeCopy

using Microsoft.Azure.Cosmos;

using Microsoft.Azure.Cosmos.Linq;

1. Add the     following lines of code to add **using** directives for the     built-in namespaces that will be used in this file:

CodeCopy

using System;

using System.Collections.Generic;

using System.Linq;

using System.Threading.Tasks;

1. Enter     the following code to add an **AdventureWorks.Context** namespace     block:

CodeCopy

namespace AdventureWorks.Context

{

}

1. Within     the **AdventureWorks.Context** namespace, enter the following     code to create a new **AdventureWorksCosmosContext** class:

CodeCopy

public class AdventureWorksCosmosContext

{

}

1. Update     the declaration of the **AdventureWorksCosmosContext** class     by adding a specification indicating that this class will implement     the **IAdventureWorksProductContext** interface:

CodeCopy

public class AdventureWorksCosmosContext : IAdventureWorksProductContext

{

}

1. Within     the **AdventureWorksCosmosContext** class, enter the     following line of code to create a new read-only *Container* variable     named **_container**:

CodeCopy

private readonly Container _container;

1. Within     the **AdventureWorksCosmosContext** class, add a new     constructor with the following signature:

CodeCopy

public AdventureWorksCosmosContext(string connectionString, string database = "Retail", string container = "Online")

{

}

1. Within     the constructor, add the following block of code to create a new instance     of the **CosmosClient** class and then obtain both a **Database** and **Container** instance     from the client:

CodeCopy

_container = new CosmosClient(connectionString)

  .GetDatabase(database)

  .GetContainer(container);

1. Within     the **AdventureWorksCosmosContext** class, add a new **FindModelAsync** method     with the following signature:

CodeCopy

public async Task<Model> FindModelAsync(Guid id)

{

}

1. Within     the **FindModelAsync** method, add the following blocks of     code to create a LINQ query, transform it into an iterator, iterate over     the result set, and then return the single item in the result set:

CodeCopy

var iterator = _container.GetItemLinqQueryable<Model>()

  .Where(m => m.id == id)

  .ToFeedIterator<Model>();

 

List<Model> matches = new List<Model>();

while (iterator.HasMoreResults)

{

  var next = await iterator.ReadNextAsync();

  matches.AddRange(next);

}

 

return matches.SingleOrDefault();

1. Within     the **AdventureWorksCosmosContext** class, add a new **GetModelsAsync** method     with the following signature:

CodeCopy

public async Task<List<Model>> GetModelsAsync()

{

}

1. Within     the **GetModelsAsync** method, add the following blocks of     code to run an SQL query, get the query result iterator, iterate over the     result set, and then return the union of all results:

CodeCopy

string query = $@"SELECT * FROM items";

 

var iterator = _container.GetItemQueryIterator<Model>(query);

 

List<Model> matches = new List<Model>();

while (iterator.HasMoreResults)

{

   var next = await iterator.ReadNextAsync();

  matches.AddRange(next);

}

 

return matches;

1. Within     the **AdventureWorksCosmosContext** class, add a new **FindProductAsync** method     with the following signature:

CodeCopy

public async Task<Product> FindProductAsync(Guid id)

{

}

1. Within     the **FindProductAsync** method, add the following blocks of     code to run an SQL query, get the query result iterator, iterate over the     result set, and then return the single item in the result set:

CodeCopy

string query = $@"SELECT VALUE products

​          FROM models

​          JOIN products in models.Products

​          WHERE products.id = '{id}'";

 

var iterator = _container.GetItemQueryIterator<Product>(query);

 

List<Product> matches = new List<Product>();

while (iterator.HasMoreResults)

{

  var next = await iterator.ReadNextAsync();

  matches.AddRange(next);

}

 

return matches.SingleOrDefault();

1. Save     the **AdventureWorksCosmosContext.cs** file.
2. In     the **Visual Studio Code** window, access the shortcut menu     or right-click or activate the shortcut menu for the Explorer pane, and     then select **Open in Terminal**.
3. At the     open command prompt, enter the following command, and then select Enter to     switch your terminal context to the **AdventureWorks.Context** folder:

CodeCopy

cd .\AdventureWorks.Context\

1. At the     command prompt, enter the following command, and then select Enter to     build the .NET web application:

CodeCopy

dotnet build

**Note**: If there are any build errors, review the **AdventureWorksCosmosContext.cs** file in the **Allfiles (F):\Allfiles\Labs\04\Solution\AdventureWorks\AdventureWorks.Context** folder.

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image068.png)

1. Select **Kill     Terminal** or the **Recycle Bin** icon to close the     currently open terminal and any associated processes.

Task 3: Update the Azure Cosmos DB connection string

1. In the Explorer pane     of the **Visual Studio Code** window, expand the **AdventureWorks.Web** project.
2. Open     the **appsettings.json** file.
3. In the     JSON object on line 4, find the **ConnectionStrings.AdventureWorksCosmosContext** path.     Observe that the current value is empty:

CodeCopy

"ConnectionStrings": {

  ...

  "AdventureWorksCosmosContext": "",

  ...

},

1. Update     the value of the **AdventureWorksCosmosContext** property by     setting its value to the **PRIMARY CONNECTION STRING** of the     Azure Cosmos DB account that you recorded earlier in this lab.
2. Save     the **appsettings.json** file.

Task 4: Update .NET application startup logic

1. In     the Explorer pane of the **Visual Studio Code** window,     expand the **AdventureWorks.Web** project.
2. Open     the **Startup.cs** file.
3. In     the **Startup** class, find the existing **ConfigureProductService** method:

CodeCopy

public void ConfigureProductService(IServiceCollection services)

{

  services.AddScoped<IAdventureWorksProductContext, AdventureWorksSqlContext>(provider =>

​    new AdventureWorksSqlContext(

​      _configuration.GetConnectionString(nameof(AdventureWorksSqlContext))

​    )

  );

}

**Note**: The current product service uses SQL as its database.

1. Within     the **ConfigureProductService** method, delete all existing lines     of code:

CodeCopy

public void ConfigureProductService(IServiceCollection services)

{

}

1. Within     the **ConfigureProductService** method, add the following     block of code to change the products provider to the **AdventureWorksCosmosContext** implementation     that you created earlier in this lab:

CodeCopy

services.AddScoped<IAdventureWorksProductContext, AdventureWorksCosmosContext>(provider =>

  new AdventureWorksCosmosContext(

​    _configuration.GetConnectionString(nameof(AdventureWorksCosmosContext))

  )

);

1. Save     the **Startup.cs** file.

Task 5: Validate that the .NET application successfully connects to Azure Cosmos DB

1. In     the **Visual Studio Code** window, access the shortcut menu     or right-click or activate the shortcut menu for the Explorer pane, and     then select **Open in Terminal**.
2. At the     open command prompt, enter the following command, and then select Enter to     switch your terminal context to the **AdventureWorks.Web** folder:

CodeCopy

cd .\AdventureWorks.Web\

1. At the     command prompt, enter the following command, and then select Enter to run     the ASP.NET web application:

CodeCopy

dotnet run

**Note**: The **dotnet run** command will automatically build any changes to the project and then start the web application without a debugger attached. The command will output the URL of the running application and any assigned ports.

1. On the     taskbar, select the **Microsoft Edge** icon.
2. In the     open browser window, browse to the currently running web application ([http://localhost:5000](http://localhost:5000/)).

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image070.png)

1. In the     web application, observe the list of models displayed from the front page.
2. Find     the **Touring-1000** model, and then select **View     Details**.

![img](file:///C:/Users/josev/AppData/Local/Temp/msohtmlclip1/01/clip_image072.png)

1. From     the **Touring-1000** product detail page, perform the     following actions:

1. 1. In      the **Select options** list, select **Touring-1000      Yellow, 50, $2,384.07**.
   2. Find **Add      to Cart**, and then observe that the checkout functionality is still      disabled.

2. Close     the browser window displaying your web application.

3. Return     to the **Visual Studio Code** window, and then select **Kill     Terminal** or the **Recycle Bin** icon to close the     currently open terminal and any associated processes.

Review

In this exercise, you wrote C# code to query an Azure Cosmos DB collection by using the .NET SDK.

Exercise 6: Clean up your subscription

Task 1: Open Azure Cloud Shell

1. In the     portal, select the **Cloud Shell** icon to open a new shell     instance.

**Note**: The **Cloud Shell** icon is represented by a greater than sign (>) and underscore character (_).

1. If this     is your first time opening Cloud Shell using your subscription, you can     use the **Welcome to Azure Cloud Shell Wizard** to configure     Cloud Shell for first-time usage. Perform the following actions in the     wizard:

1. 1. A      dialog box prompts you to create a new storage account to begin using the      shell. Accept the default settings, and then select **Create      storage**.

**Note**: Wait for the Cloud Shell to finish its initial setup procedures before moving forward with the lab.If you don’t notice the Cloud Shell configuration options, this is most likely because you’re using an existing subscription with this course’s labs. The labs are written with the presumption that you’re using a new subscription.

Task 2: Delete resource groups

1. At the     command prompt, enter the following command, and then select Enter to     delete the **PolyglotData** resource group:

CodeCopy

az group delete --name PolyglotData --no-wait --yes

1. Close     the Cloud Shell pane in the portal.

Task 3: Close the active applications

1. Close     the currently running Microsoft Edge application.
2. Close     the currently running Visual Studio Code application.

Review

In this exercise, you cleaned up your subscription by removing the resource groups used in this lab.

 