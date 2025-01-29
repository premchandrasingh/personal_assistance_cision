## Slack Git Enterprise App

https://cision.slack.com/apps/A0F7YS2SX-github-enterprise-server

- autonomy-git-media-studio
  https://hooks.slack.com/services/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
- autonomy-git-pushes
  https://hooks.slack.com/services/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

## Local git clone

    git clone Cision.OMC20.BoilerPlate/.git BoilerPlateClone

## Rename master to main

    git branch -m master main

===============================================================

## Get list of template available

    dotnet new --list   ---- deprecated
    dotnet new list    ----- new way

## Search template

    dotnet new --search React   --------- deprecated
    dotnet new search React     ------ new way

## Get the uninstall command

    dotnet new -u ----- deprecated
    dotnet new uninstall ----- new way

## Install a template command

_Go the the root folder where ".template.config" is contained - not inside the ".template.config" folder_
dotnet new --install <the path or the template name> ----- deprecated
dotnet new -i cision-webapi ----- setup the private package source in C:\Users\prem.leishangthem\AppData\Roaming\NuGet\NuGet.Config
dotnet new install . --debug:reinit ----- if the template source is at the root
dotnet new install cision-webapi ----- https://learn.microsoft.com/en-us/dotnet/core/tools/custom-templates
dotnet new install cision-worker
dotnet new install "D:\00Projects\local_nuget\cision-webapi.1.0.1.nupkg" ----- directly from nupkg file

## Uninstall a template command

_Go the the root folder where ".template.config" is contained - not inside the ".template.config" folder_

    dotnet new --uninstall <the path or the template name>  ----- deprecated
    dotnet new uninstall <the path or the template name>  ----- new way
    dotnet new uninstall .  ----- uninstall template by the name of current folder

    dotnet new uninstall cision-webapi
    dotnet new uninstall cision-worker

## Create project using the template

    dotnet new  cision-webapi --help
    dotnet new  cision-webapi -o Cision.Dist20.DistroDoc
    dotnet new  cision-webapi -o Cision.Dist20.AccountManagment
    dotnet run --project ./Cision.Dist20.DistroDoc/src/Cision.Dist20.DistroDoc.Web

## Pack/Create nuget file for custom-templates

    dotnet pack WebApi.Template.Package.csproj -c Release -o ../
    dotnet pack WorkerService.Template.Package.csproj -c Release -o ../

## C:\Users\prem.leishangthem\AppData\Local\NuGet\v3-cache

## Remove folder recursively.

Will prompt for confirmation.

WARNING:-Adding another parameter /q will disable the prompt for confirmation

    rmdir Cision.Dist20.DistroDoc /s

===============================================================

# Deploy nuget project specific sharable packages

### Media Service

### Media Store

### OMI (Order media integration)

    dotnet nuget push "D:\00Projects\Dist2.0\Cision.OMI.Share\Cision.OMI.Domain.Entities\bin\Release\Cision.OMI.Domain.Entities.1.0.3.nupkg" --source "cisionGithub"
    dotnet nuget push "D:\00Projects\Dist2.0\Cision.OMI.Share\Cision.OMI.Infrastructure.EntityConfig\bin\Release\Cision.OMI.Infrastructure.EntityConfig.1.0.5.nupkg" --source "cisionGithub"

# Deploy nuget packages

    dotnet nuget push "D:\00Projects\Dist2.0\templates\cision-webapi.1.0.15.nupkg" --source "cisionGithub"
    dotnet nuget push "D:\00Projects\Dist2.0\templates\cision-worker.1.0.3.nupkg" --source "cisionGithub"

    dotnet nuget push "D:\00Projects\GOAT\cision-goat-core\src\src\CoreCalc\bin\Release\CoreCalc.0.0.28.nupkg" --source "cisionGithub"

    dotnet nuget push "D:\00Projects\Common\Cision.Logging\src\bin\Release\Cision.Logging.1.0.8.nupkg" --source "cisionGithub"

    dotnet nuget push "D:\00Projects\Common\Cision.HealthCheck\src\bin\Release\Cision.HealthCheck.6.0.3.nupkg" --source "cisionGithub"

    dotnet nuget push "D:\00Projects\Common\Cision.Swagger\src\Cision.ApiVersioning\bin\Release\Cision.ApiVersioning.6.0.0.nupkg" --source "cisionGithub"
    dotnet nuget push "D:\00Projects\Common\Cision.Swagger\src\Cision.Swagger\bin\Release\Cision.Swagger.6.0.16.nupkg" --source "cisionGithub"

    dotnet nuget push "D:\00Projects\Common\Cision.Auth\src\Cision.AccountValidation\bin\Release\Cision.AccountValidation.6.0.2.nupkg" --source "cisionGithub"
    dotnet nuget push "D:\00Projects\Common\Cision.Auth\src\Cision.Auth.Abstractions\bin\Release\Cision.Auth.Abstractions.1.0.7.nupkg" --source "cisionGithub"
    dotnet nuget push "D:\00Projects\Common\Cision.Auth\src\Cision.Authentication\bin\Release\Cision.Authentication.6.1.6.nupkg" --source "cisionGithub"
    dotnet nuget push "D:\00Projects\Common\Cision.Auth\src\Cision.Authentication.ACM\bin\Release\Cision.Authentication.ACM.6.1.7.nupkg" --source "cisionGithub"
    dotnet nuget push "D:\00Projects\Common\Cision.Auth\src\Cision.Authorization\bin\Release\Cision.Authorization.6.0.21.nupkg" --source "cisionGithub"
    dotnet nuget push "D:\00Projects\Common\Cision.Auth\src\Cision.Authorization.ACM\bin\Release\Cision.Authorization.ACM.6.0.20.nupkg" --source "cisionGithub"
    dotnet nuget push "D:\00Projects\Common\Cision.Auth\src\Cision.Authorization.UMT\bin\Release\Cision.Authorization.UMT.6.0.5.nupkg" --source "cisionGithub"
    dotnet nuget push "D:\00Projects\Common\Cision.Auth\src\Cision.S2SClient\bin\Release\Cision.S2SClient.6.0.25.nupkg" --source "cisionGithub"
    dotnet nuget push "D:\00Projects\Common\Cision.Auth\src\Cision.S2SClient.MySql\bin\Release\Cision.S2SClient.MySql.6.0.8.nupkg" --source "cisionGithub"
    dotnet nuget push "D:\00Projects\Common\Cision.Auth\src\Cision.S2SClient.SqlServer\bin\Release\Cision.S2SClient.SqlServer.6.0.10.nupkg" --source "cisionGithub"



    dotnet nuget push "D:\00Projects\Common\Cision.Fileupload\src\bin\Release\Cision.FileUpload.6.2.20.nupkg" --source "cisionGithub"

    dotnet nuget push "D:\00Projects\Common\Cision.NotableEvent\src\Cision.NotableEvent\bin\Release\Cision.NotableEvent.1.0.2.nupkg" --source "cisionGithub"

    dotnet nuget push "D:\00Projects\Common\Cision.VirusScanner\src\bin\Release\Cision.VirusScanner.1.0.1.nupkg" --source "cisionGithub"

    dotnet nuget push "D:\00Projects\Common\Cision.ErrorHandling\src\Cision.ErrorHandling\bin\Release\Cision.ErrorHandling.6.0.4.nupkg" --source "cisionGithub"

    dotnet nuget push "D:\00Projects\Common\Cision.Polly\src\Cision.Polly\bin\Release\Cision.Polly.1.0.1.nupkg" --source "cisionGithub"

    dotnet nuget push "D:\00Projects\Common\Cision.Telemetry\src\bin\Release\Cision.Telemetry.1.0.2.nupkg" --source "cisionGithub"

    dotnet nuget push "D:\00Projects\Common\Cision.PubSub\src\Cision.Kafka\bin\Release\Cision.Kafka.1.1.9.nupkg" --source "cisionGithub"
    dotnet nuget push "D:\00Projects\Common\Cision.PubSub\src\Cision.Kafka.MessageLogging\bin\Release\Cision.Kafka.MessageLogging.1.0.4.nupkg" --source "cisionGithub"

    dotnet nuget push "D:\00Projects\Common\Cision.Migration\src\Cision.Migration\bin\Release\Cision.Migration.0.0.6.nupkg" --source "cisionGithub"
    dotnet nuget push "D:\00Projects\Common\Cision.Migration\src\Cision.Migration.dbup\bin\Release\Cision.Migration.dbup.0.0.10.nupkg" --source "cisionGithub"
    dotnet nuget push "D:\00Projects\Common\Cision.Migration\src\Cision.Migration.dbup-mysql\bin\Release\Cision.Migration.dbup-mysql.0.0.6.nupkg" --source "cisionGithub"
    dotnet nuget push "D:\00Projects\Common\Cision.Migration\src\Cision.Migration.dbup-oracle\bin\Release\Cision.Migration.dbup-oracle.0.0.4.nupkg" --source "cisionGithub"
    dotnet nuget push "D:\00Projects\Common\Cision.Migration\src\Cision.Migration.dbup-postgresql\bin\Release\Cision.Migration.dbup-postgresql.0.0.5.nupkg" --source "cisionGithub"
    dotnet nuget push "D:\00Projects\Common\Cision.Migration\src\Cision.Migration.dbup-sqlite\bin\Release\Cision.Migration.dbup-sqlite.0.0.4.nupkg" --source "cisionGithub"
    dotnet nuget push "D:\00Projects\Common\Cision.Migration\src\Cision.Migration.dbup-sqlserver\bin\Release\Cision.Migration.dbup-sqlserver.0.0.4.nupkg" --source "cisionGithub"
    dotnet nuget push "D:\00Projects\Common\Cision.Migration\src\Cision.Migration.EFCore\bin\Release\Cision.Migration.EFCore.6.0.3.nupkg" --source "cisionGithub"

    dotnet nuget push "D:\00Projects\Common\Cision.WorkerService\src\Cision.Extensions.Hosting.Quartz\bin\Release\Cision.Extensions.Hosting.Quartz.1.0.4.nupkg" --source "cisionGithub"
    dotnet nuget push "D:\00Projects\Common\Cision.WorkerService\src\Cision.Common.BgWorker\bin\Release\Cision.Common.BgWorker.1.0.9.nupkg" --source "cisionGithub"

    dotnet nuget push "D:\00Projects\Common\Cision.Utility\src\Cision.Utility.Paging\bin\Release\Cision.Utility.Paging.1.0.1.nupkg" --source "cisionGithub"

===============================================================

    Get-ChildItem  -Filter *.* -Recurse | Where-Object {$_.Name -like "*WebApi.Template.PlayGround*"} | ForEach { $newname = ([String]$_.FullName).Replace("WebApi.Template.PlayGround","WebApi.Template"); Rename-item -Path $_.FullName $newname; }

    for /r %F in (*.sln,*.cs,*.json,*.csproj) do (JREPL "WebApi.Template.PlayGround" "WebApi.Template" /F "%F" /o -)

    We suggest to follow the project naming convension as org.[app-group].[app-name].[app-type].\\n Example:- Cision.Dist20.ECom.Web or Cision.ECom.Web

===============================================================

    netstat -nao 1 | find "10.18.242.60"
