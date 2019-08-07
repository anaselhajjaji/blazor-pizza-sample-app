# Installation
1- Add ElectronNET.API NuGet package to BlazingPizza.Server project

2- In Program.cs
```csharp
...
public static IHostBuilder CreateHostBuilder(string[] args) =>
            Host.CreateDefaultBuilder(args)                
                .ConfigureWebHostDefaults(webBuilder =>
                {
                    webBuilder.UseElectron(args).UseStartup<Startup>();
                });                
...
```
3- Startup.cs, add the following line as the last statement in Configure method
```csharp
Electron.WindowManager.CreateWindowAsync();
```
4- Install ElectronNet CLI: dotnet tool install ElectronNET.CLI -g

5- In BlazingPizza.Server folder run: electronize init

# Run the app
electronize start
