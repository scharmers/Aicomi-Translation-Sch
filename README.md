# Aicomi-Translation-Sch

A fork of Aicomi-Translation by Scharmers. 
1. Focuses mainly on dialogue (i.e. the files in the \Dialogue folder) GUI is not changed.
2. Dialogue lines have been reworked to read more "naturally".
3. Consider this project as being in a permanent WIP state with no expectation of completion but as of 10-7-25 I've modfied hundreds, if not thousands of lines
4. Please feel free to check out, say, the cheerful personality as an example of my work and completion.
5. As of 10-7-25, H lines have not been dumped, so H and "interstitial" subtitles are not present.

**## Original Readme**

Fan translations for Aicomi, for use with [XUnity Auto Translator](https://github.com/bbepis/XUnity.AutoTranslator).

You can see which languages are supported [here](https://github.com/IllusionMods/Aicomi-Translation/tree/main/Translation).

## Installation Instructions

1. Prerequisites
	- [BepInEx v6 IL2CPP](https://github.com/BepInEx/BepInEx) (latest nightly version)
	- [XUnity Auto Translator](https://github.com/bbepis/XUnity.AutoTranslator) (latest BepInEx6 IL2CPP version)

2. Delete the existing `BepInEx\Translation` folder from your game directory if it exists.

3. Install This Translation
	- Download the latest release from the [Releases](https://github.com/IllusionMods/Aicomi-Translation/releases) page.
	- Extract the contents of the archive into your game directory. Overwrite files if asked. Ensure that the `BepInEx\Translation` folder is placed correctly. 

4. See if it works
	- If you wish to change the language, edit the `BepInEx\config\XUnity.AutoTranslator.cfg` file and set the `Language` option to your desired language code (e.g. ``Language=zh-TW``).
	- Launch the game. The translations should now be applied automatically.
	- If you see untranslated text (e.g. names of items added by mods or future game updates), you may need to change the `Endpoint` option. Press Alt+0 while in-game to open the XUnity Auto Translator menu and select a different endpoint.


## Contributing

If you are comfortable with Git, fork the repository and submit PRs. Since the PRs will be squash merged, do not PR from your main branch or you will have issues if you try to PR again.

To add a new language, copy the `Translation/en` folder to a new folder with the appropriate [IETF language tag](https://en.wikipedia.org/wiki/IETF_language_tag) (e.g. `Translation/fr` for French), then only edit the files in that folder.

Otherwise, you can use the GitHub web interface to easily make single-file changes:

1. Browse the repository on GitHub and open the file you want to improve translations in.
2. Click the edit (pencil) icon at the top right of the file view to open the online editor.
3. Edit the text on the right of = as needed. Do not edit anything on the left of the = sign!
4. Loot for the "Propose changes" button. Add a short title and description for your change. Tell it to make a fork and a new branch, and start a pull request.

**Tip:** For small fixes (typos, single lines), editing on GitHub is easiest. For larger changes, you can still use the GitHub website by repeating the above steps for each file.

### Compiling New Releases

Releases must be made with the TranslationTool included in this repository, or some ADV dialogue lines will not be translated in-game. This is because the tool has to generate regexes for lines with placeholder tags that represent character names in-game.

First build the whole translation tools solution in Visual Studio 2022+, then run ReleaseTool by draggin the repository folder onto it. The tool will generate a new release zip in the same folder as the executable.
