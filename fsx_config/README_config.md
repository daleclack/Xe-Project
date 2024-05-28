### FSX Config example

This is a example of fsx.cfg file, which is the configuration file for Microsoft Flight Simulator X: Steam Edition

The location of fsx.cfg file is \<User Folder\>\\Appdata\AppData\Roaming\Microsoft\FSX\

The important configs:

#### 1. Trusted modules

```ini
[Trusted]
D:\SteamLibrary\steamapps\common\FSX\SimObjects\Airplanes\IRIS PC-21\Panel\dsd_fsx_xml_sound.gau.czbzccbqoqkbtnqaciirakbckqraztcztulnbcuw=2
```

The trusted modules for flight simulator x, for wine/proton on linux, the trusted module paths may need to manually add the cfg file.

Note: The trusted modules information should generated from microsoft windows.

#### 2. Window mode

Due to some bug of wine/proton, the Flight Simulator X may can't start flight with full screen mode, the config is in the [Main] Section of fsx.cfg.

This is a example for window mode.

```ini
[Main]
Maximized=2
```
