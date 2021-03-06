# ![Icon](https://raw.github.com/clariuslabs/VisualStudio/master/icon/32.png) VisualStudio Targets


Contains MSBuild targets that are useful when developing Visual Studio extensions. 

* Provides the following MSBuild properties for version-aware projects:
  * `VisualStudioVersion`: for VS2010, sets it to '10.0'
  * `MinimumVisualStudioVersion`: equals `VisualStudioVersion` to allow opening on any version
  * `DevEnvDir`: if it's empty, for safe command-line building. Can be overriden.
  * `PublicAssemblies`: $(DevEnvDir)\PublicAssemblies\
  * `PrivateAssemblies`: $(DevEnvDir)\PrivateAssemblies\
  * `VSSDK`: the [VSSDK install directory]\VisualStudioIntegration\Common\Assemblies\ folder. Can be overriden.
  * `VSSDK20`: $(VSSDK)v2.0\
  * `VSSDK40`: $(VSSDK)v4.0\
  * `VSToolsPath`: path to the MSBuild targets for the VSSDK

* Smarter and simpler template authoring. Just set BuildAction to None on all your 
  template content as well as the .vstemplate, and they become Smart Templates automatically:
	* Supports <Include> metadata to add shared artifacts to the generated ZIP files
	* Does not regenerate ZIP files if content didn't change
	* Supports linked files that are copied to the output directory


More in-depth tutorials on using this project is available in the [wiki](https://github.com/clariuslabs/VisualStudio/wiki).

See the [readme](https://github.com/clariuslabs/VisualStudio/blob/master/nuget/Readme.txt) for the latest change log.

## Installation

To install Clarius Visual Studio Targets, run the following command in the Package Manager Console:

```
PM> Install-Package Clarius.VisualStudio
```



Icon [Infinity](http://thenounproject.com/term/infinity/9992/) by Cengiz SARI from [The Noun Project](http://thenounproject.com/).




[![Build Status](https://www.myget.org/BuildSource/Badge/clarius?identifier=97a997db-cde0-4f12-9d5f-a7e86b682873 "Build Status")](https://www.myget.org/gallery/clarius)
====================
This project is sponsored by Clarius Labs

[![Clarius Labs][2]][1]


  [1]: http://clariuslabs.github.io/
  [2]: http://clariuslabs.github.io/media/clariuslabs.png (Clarius Labs Logo)
