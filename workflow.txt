Start with a project you want to use Git with and review Git source control. This will help you get Git up and running in the editor. When done with that, come back here.

**Expanding Git outside the editor**

.gitignore file should be set to ignore the following:

/Binaries

/DerivedDataCache

/Intermediate

/Saved

*.sln

*.sdf

*.suo

The following folders should be committed:

/Content (could be handled by the editor plugin if you have that set up)

/Config

/Build

/Source

Don't forget to check in your .uproject file as well.

**Connecting your local git repo up to remote repo**

'git init' only stores files into a local git repository. To store them on a remote service you have to issue the command line command:

git remote add origin <remote url>

The editor plugin does not handle pushes and pulls, so you will need to use an external tool to keep your project's remote repo up to date.

**After pulling a project down for the first time**

Once you have pulled a committed project down from some remote git repository there are couple of things to be aware of.

1. If the project is a C++ project, find the .uproject file in explorer, right click and 'Generate Visual Studio project files'. Until you do this (or create a new code class from the editor) you will not have any visual studio solution to access.

2. Open the Epic Launcher and launch unreal. When you get the project selector click Browse and find your .uproject file.

3. Unreal will then prompt you to rebuild binaries. This will take a few minutes.

Once the binaries are built (and your solution files are generated if it is a C++ project) you should be good to start developing.

Note: While the editor plugin will continue to handle your content for you, if you are changing source files, creating new C++ classes, etc, you will need to have an external tool installed to check those files in.
