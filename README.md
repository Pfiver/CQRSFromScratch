# CQRSFromScratch

Extension of the Mob Programming session with Clement https://twitter.com/clem_bouillier and Emilien https://twitter.com/Ouarzy
at the SoCraTes 2017 conference https://twitter.com/SoCraTes_CH

The project now works inMicrosoft Visual Studio Code https://www.visualstudio.com/en-us/products/code-vs.aspx
which is available free of charge for Mac.

Unit tests can be executed on save with dotnet-watch: https://docs.microsoft.com/en-us/aspnet/core/tutorials/dotnet-watch

If you install VS Code and start with only the `TweetShould.cs` file
1. Start VS Code, install C# Extension and dotnet core command line tools
1. Create a directory `CQRS` on the file system
1. `cd` to it in the terminal and run `$ dotnet new xunit`
2. Add this snippet to the CQRS.csproj file:
    ````
    <ItemGroup>
        <DotNetCliToolReference Include="Microsoft.DotNet.Watcher.Tools" Version="1.0.0" />
    </ItemGroup>
    ````
3. Drop the `TweetShould.cs` into the directory
3. Then execute these commands:
    ````
    bash-4.4$ dotnet add package FluentAssertions
    bash-4.4$ dotnet restore
    bash-4.4$ dotnet watch test
    ````

----

Enjoy!
