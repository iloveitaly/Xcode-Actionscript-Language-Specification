This is for Xcode 4 & Flash 8.  

Not working yet... xcode 4 seems to have changed the language specifications alot: http://www.cocoabuilder.com/archive/xcode/300157-xcode-4-and-personal-pbfilespec-xclabgspec-files.html  

### INSTALLATION ###

**Note:** this assumed your cwd is this cloned github repo.  

```
if [[ ! -e "/Library/Application Support/Developer/Shared/Xcode/Specifications" ]]; then
	echo "Specification folder DNE... need admin privileges to create it"
	sudo mkdir "/Library/Application Support/Developer/Shared/Xcode/Specifications"
fi

if [[ -e $PWD/ActionScript.pbfilespec && -e $PWD/ActionScript.pblangspec ]]; then
	sudo cp $PWD/ActionScript.pbfilespec $PWD/ActionScript.pblangspec "/Library/Application Support/Developer/Shared/Xcode/Specifications"
else
	echo "Wrong folder: needed files DNE"
fi

exit 0
```

One line version for copy/paste:

	if [[ ! -e "/Library/Application Support/Developer/Shared/Xcode/Specifications" ]]; then sudo mkdir "/Library/Application Support/Developer/Shared/Xcode/Specifications"; fi; if [[ -e $PWD/ActionScript.pbfilespec && -e $PWD/ActionScript.pblangspec ]]; then sudo cp $PWD/ActionScript.pbfilespec $PWD/ActionScript.pblangspec "/Library/Application Support/Developer/Shared/Xcode/Specifications"; fi
