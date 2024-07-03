# Note for Flight Simulator Config files

## Micosoft Flight Simulator 2004 (Deprecated)

Just Copy the logbook.log file to the "Flight Simulator Files" directory in your documents folder.

## Micsooft Flight Simulator X (fsx)

The flight logs are extracted with a tool: fslogbook.
The fsx.cfg file in the fsx_config folder is a config example to trust some gauges and launch fsx with windowed mode.

## Microsoft Flight Simulator (2020)

The flight logs are extracted with the flight log analyzer, which is a paid software.

## X-Plane 12 (No macOS operations, because I do not have MacOS devices)

### Microsoft Windows

Use powershell or command promot (cmd) to link flight logs and control preferences.
The %XPlaneDir% is the directory where you install X-Plane 12, and %RepoDir% is the directory for this project.

#### PowerShell

```powershell
New-Item -ItemType SymbolicLink -Path %XPlaneDir%"\Output\logbooks" -Target %RepoDir%"\flight_logs\xp12_logs"
New-Item -ItemType SymbolicLink -Path %XPlaneDir%"\Output\preferences\control profiles" -Target %RepoDir%"\xp12_config\control profiles"
```

#### Cmd

```cmd
mklink /d %XPlaneDir%"\Output\logbooks" %RepoDir%"\flight_logs\xp12_logs"
mklink /d %XPlaneDir%"\Output\preferences\control profiles" %RepoDir%"\xp12_config\control profiles"
```

### Linux

Just use \"ln" command.
The $XPlaneDir is the directory where you install X-Plane 12, and $RepoDir is the directory for this project.

```shell
ln -s $RepoDir/flight_logs/xp12_logs $XPlaneDir'/Output/logbooks'
ln -s $RepoDir'/xp12_config/control profile' $XPlaneDir'/Output/preferences/control profiles'
```
