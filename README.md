# PluginDemo

This is a starter Minecraft plugin.

Features:

* Minimal Minecraft Plugin based on [Creating a blank Spigot plugin, using Maven](https://www.spigotmc.org/wiki/creating-a-plugin-with-maven-using-intellij-idea/).
* Minimal plugin version set to 1.13 of the Spigot API and tested on version 1.16 of the API. If your plugin uses newer or older Minecraft API features, you can change that in `plugin.yml`.
* Compiles with Maven.
* Compilation tested on MacOS Java 14.
* To support older servers compiled with Java 8, target was changed to 1.8 in `pom.yml`.
* Tested plugin on these servers:
    * Spigot 1.16.4-R0.1-SNAPSHOT (compile with Java 14 on MacOS) when testing plugin locally.
    * Paper 1.16.4 (compiled with Java 8) running on a paid hosting service using an older version of Java.

## Steps for using this template for your own projects

- [ ] Read about [Spigot plugin development](https://www.spigotmc.org/wiki/spigot-plugin-development/) (recommended).
- [ ] Create a new package (instead of `com.briangershon.demo`) and matching folder structure. Move `App.java` in there. Add your plugin logic.
- [ ] Update `plugin.yml` and populate with the meta data for your plugin.
- [ ] Update `pom.xml` top section to match your plugin as well as `<dependency>` section if you're using a different Spigot version.

## Development Environment Setup and Workflow

If you haven't create a plugin before, you'll need to setup your local development environment and understand the compile and test workflow. I've created a [Minecraft Plugin Development Guide](https://gist.github.com/briangershon/7a009cad2a1e11a7b785e8b8bf6ada1a) to cover this.

## To Release Your Plugin

Make sure you first update the plugin version in `pom.xml` in `<version>1.0.0</version>`.

    mvn clean package

You should now have your new plugin jar file in `target` folder.

## To install on your Spigot compatable Minecraft Server

Copy `target/PluginDemo-n.n.n.jar` to your server `/plugin` folder, and reload server configuration (or just restart server).

You should see these two messages in your server console:

```
[11:50:26] [Server thread/INFO]: [PluginDemo] Enabling PluginDemo v0.0.1
[11:50:26] [Server thread/INFO]: [PluginDemo] Hello, SpigotMC!
```
