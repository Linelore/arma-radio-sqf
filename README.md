# LL Radio

LL-radio is uesd to add a controllable radio with stop, start and next functionality to any object in arma 3.


## Installation

1. Place all files and folders in you mission directory
2. Add the following to the init of the object you want to use as the radio
```sqf
[this]execVM "Scripts\Radio\radioStart.sqf"; 
```

### Adding sounds
1. Place the a .oog file of the sound in the sounds folder
2. In description.ext add the file to the CfgSounds class list (Check the [wiki](https://community.bistudio.com/wiki/Description.ext#CfgSounds) if unsure how)
3. In \Scripts\Radio\radioStart.sqf on line 2 change the value _numberOfSoungs 
4. In \Scripts\Radio\radioStart.sqf on line 39 add:
```
	case 3 : {	
		[_speaker, ["mySoundHere",2000,1]] remoteExec ["say3d"];
		_soungLength = 15;
	};
```
5. Change "mySoundHere" to the name given to the sound in the description.ext 
6. Change _soungLength to the length of the sound in seconds

## License
[MIT](https://choosealicense.com/licenses/mit/)
