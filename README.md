# Ukko

*Ukko* the Finnish god of weather, and the skies. The highest of the pagan gods resembling Thor with an axe that allows him to control lightning.

## Getting Started

### Tech Stack

* [Xamarin.Forms](https://github.com/xamarin/Xamarin.Forms)
* [ReactiveUI](https://github.com/reactiveui/ReactiveUI)
* [Refit REST Library](https://github.com/reactiveui/refit)
* [Splat](https://github.com/reactiveui/splat)
* [ASP.NET Core WebAPI 2.1](https://github.com/aspnet/Home)

### Services

* [OpenWeatherMapAPI](https://openweathermap.org/api)

### Developer Environment Setup

The getting started guide is still currently in progress and will later have basic environment details. Until then hang tight and thank you for your interest in our humble project.

* Download and install [.NET Core 2.1 SDK](https://www.microsoft.com/net/download)
* Install Visual Studio Community with .NET Core, and Xamarin options selected. Will be targeting the three latest versions and all of their updates for Android, and iOS. *Visual Studio only please to keep this consistent as other IDEs have cause build errors for one or the other with metadata conflicts, and file generation.*
* Install [Conveyor](https://marketplace.visualstudio.com/items?itemName=vs-publisher-1448185.ConveyorbyKeyoti) and follow all of the directions on the page for configuration. This will greatly simplify testing on a remote device. If you have some other preferred method go ahead and do that. *Might only work on Windows*.

After cloning you will need to make a change before you can successfully use the application. Locate the *ApplicationSettings.cs* file located in the *...\<DIRECTORY_PROJECT_CLONED_TO>\Ukko\Ukko\Ukko* directory and open it. Then open the *Ukko.API.sln* (API solution) and run it by going to the debug menu or pressing F5. A window should pop up like the one from the conveyor instructions. Copy the IP addres it displays (your local network ip for your dev machine) and the port. Then paste this in the ApplicationSettings file for the *LOCALHOST_API_ADDRESS* value. Should look like the following:

```csharp
public static readonly string LOCALHOST_API_ADDRESS = "http://192.168.86.24:45455/api";
```

This is so you can test the API locally within the android emulator. This will be most useful after changes are made to the API project, and to offload costs with server bandwith.

**Please be sure to build locally and that the build is successful, and tests have passed before pushing to GitHub. Regression tests included.** Breaking the build may result in expulsion as a collaborator.

### UI/UX and Design Tools

For the most part the design should follow the native platform design guidelines. This is to keep it as familiar and easy to use as possible in each respective ecosystem for their users. All design in Xamarin should be handled in XAML and not the codebehind.

* To begin with Android will be the only project we will focus on. Eventually we shall add in functionality for iOS and UWP as desired to keep the initial release small.
* [iOS](https://developer.apple.com/design/human-interface-guidelines/ios/overview/themes/)
* [Android](https://material.io/design/)
* [UWP](https://developer.microsoft.com/en-us/windows/apps/design)

For the design portion a couple tools will be used to help the design process go a little more smoothly across different screen sizes, aspect ratios, etc and so we can keep a common theme. 

* [Adobe XD](https://www.adobe.com/products/xd.html)
* [Zeplin](https://zeplin.io/)

Design files and assets should be moved to their respective location. So in the case of Adobe XD files they should be saved to the iOS folder for iOS designs on the design branch. The assets exported for direct use should be in the correct location within the project for development on a development branch.

## Contribution Conventions and Guidelines

To keep the developers happy please use conventions and guidelines throughout the application. Developers can sometimes be very grumpy creatures.

* [Microsoft C# Coding Conventions](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/inside-a-program/coding-conventions)
* [Microsoft REST API Guidelines](https://github.com/Microsoft/api-guidelines/blob/vNext/CONTRIBUTING.md)
* [Github Flow](https://guides.github.com/introduction/flow/)
* [White House Web API Standards](https://github.com/WhiteHouse/api-standards/blob/master/README.md)

To start contributing fork the project, and work from the beta branch. Then submit a pull request. Pleas eonly work on current issues, and include a *#ISSUE_NUMBER* in the commit message.
