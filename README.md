android-studio Cookbook
=======================
Install Android-Studio

Supports
--------
* Linux
* OSX

Requirements
------------
You'll need Java 6+ to run android studio.  API-19 (KitKat) supports Java7, but you'll want Java6 for all other api levels.
On OSX, the Java installer will fire up when you launch Android Studio, on Linux, you'll want to use the java cookbook

#### packages
- `java` - android-studio needs java


Attributes
----------
<table>
  <tr>
    <th>Key</th>
    <th>Type</th>
    <th>Description</th>
    <th>Default</th>
  </tr>
  <tr>
    <td><tt>[:android][:install_haxm]</tt></td>
    <td>Install HAXM Module</td>
    <td>leave this enabled unless you like using slow ARM emulators</td>
    <td><tt>true</tt></td>
  </tr>
  <tr>
    <td><tt>[:android][:use_gradle]</tt></td>
    <td>Gradle</td>
    <td>You're gonna want newer gradle than AndroidStudio ships with, and this will let you bump it as you like</td>
    <td><tt>1.10</tt></td>
  </tr>
  <tr>
    <td><tt>[:android][:emulator][:genymotion]</tt></td>
    <td>Genymotion</td>
    <td>even the free one is better than the android-sdk emulator, use it.</td>
    <td><tt>true</tt></td>
  </tr>
</table>


Genymotion
----------
You'll want to go to Android Studio's `Preferences>>Plugins>>Browse Repository` and install the Genymotion plugin so you can lauch Geny's from within Android Studio.

Usage
-----
Just include `android-studio` in your node's `run_list` -- but you should probably make an android-dev role and include it that way:

```json
{
  "name":"my_node",
  "run_list": [
    "recipe[android-studio]"
  ]
}
```

Contributing
------------
TODO: (optional) If this is a public cookbook, detail the process for contributing. If this is a private cookbook, remove this section.

e.g.
1. Fork the repository on Github
2. Create a named feature branch (like `add_component_x`)
3. Write your change
4. Write tests for your change (if applicable)
5. Run the tests, ensuring they all pass
6. Submit a Pull Request using Github

License and Authors
-------------------
Authors: Jake Plimack
