X-Prolog is a lightweight Prolog system intended to facilitate programming in Prolog on Android. The app runs Prolog programs in a text view, web view or as a bound service to a client app. A sample client is available at https://github.com/xprolog/sample-client.

<i>got tool?</i> The app depends on user-defined tools for editing and building projects. The tools are written in Prolog and are visible on devices with developer options. The app and tools exchange data through transfer variables and formatted output. This release includes trivial tools intended to demonstrate the app's tooling feature.

The app defines extension points at which transfer variables are available (to tools) and formatted output (from tools) is recognized. A tool may be configured to contribute to one or more extension points by specifying a context term.

A context term is read-term of the form <i>context(Name, FileTypes, Priority) </i>, where <i>Name</i> is the name of an extension point, <i>FileTypes</i> is a list of acceptable file types and <i>Priority</i> is an integer not less than zero, the meaning of which varies depending on the extension point.

This release defines three extension points: <i>build, edit</i> and <i>reconcile</i>, which allow tools to contribute to, respectively, building projects, editing source files and reconciling source models.

To build a project, open a file in the top directory of the project and click <i>Build</i>. To export the project into a runnable object file on the local file system, click <i>Export</i>. To run the object file, click <i>Run</i>.

A file is considered source-file if there exists one or more tools that build the file, possibly transforming it into another source file. This release includes a single build tool, <i>Compile</i>, which translates a Prolog source file (.pl) into a quick-load file (.ql).

Known issues include occurs check, logical update view, attributed variables among others.
