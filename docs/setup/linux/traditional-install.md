# Traditional Unreal Setup

- Clone this repo
- Clone our [UnrealEnginePython fork](https://github.com/deepdrive/UnrealEnginePython) into the root of this project (not a submodule as we are going to make this a binary only)

```
cd Plugins
git clone https://github.com/deepdrive/UnrealEnginePython
```

- Tip: To avoid rebuilding UnrealEnginePython, move `Plugins/UnrealEnginePython` to your Engine plugins folder, i.e. `<your-unreal-dir>/Engine/Plugins/UnrealEnginePython/` after you've built the deepdrive-sim project with the plugin in `deepdrive-sim/Plugins`.

```
git clone git@github.com:EpicGames/UnrealEngine --branch 4.21
# or if you are using http: 
# git clone https://github.com/EpicGames/UnrealEngine --branch 4.21
```

`<your-unreal-dir>` is now populated with the Unreal Engine source.

##### Build Unreal

_Takes an hour with 12 cores_

```
cd UnrealEngine
./Setup.sh && ./GenerateProjectFiles.sh && make
```

More details on building Unreal [here](https://wiki.unrealengine.com/Building_On_Linux), though the above commands should be sufficient.

##### Get the substance plugin

Download the Substance plugin from [here](https://forum.allegorithmic.com/index.php/topic,26732.0.html) and unzip the `Plugins/Runtime/Substance` folder within it to
`<your-unreal-dir>/Plugins/Runtime` for Unreal 4.21. For other releases, see [here](https://forum.allegorithmic.com/index.php/board,23.0.html) or you can just use the sources downloaded by Windows / Mac marketplace.

##### Run the editor
```
./Engine/Binaries/Linux/UE4Editor
```

Finally open the deepdrive-sim uproject file within the editor.
