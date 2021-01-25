<p align="center">
  <img width="500px" src="https://raw.githubusercontent.com/Wieku/danser-go/master/assets/textures/coinbig.png"/>
</p>

# osu-danser

[![GitHub release](https://img.shields.io/github/release/wieku/danser-go.svg)](https://github.com/Wieku/danser-go/releases/latest)
[![CodeFactor](https://www.codefactor.io/repository/github/wieku/danser-go/badge)](https://www.codefactor.io/repository/github/wieku/danser-go)
[![Discord server](https://img.shields.io/discord/713705871758065685.svg?label=&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2)](https://discord.gg/ysykK8s)

danser-go is a visualiser for osu! maps written in Go.

Application is in dev phase so only few things work. But if you want to test it, you should follow steps at the end of this readme.

## Dance examples
* [REOL - YoiYoi Kokon [Yoi] - Dance comparison](https://youtu.be/QZ6-MaWWyA8)
* [Omoi - Chiisana Koi no Uta (Synth Rock Cover) [Kroytz's EX EX] - TAG2 Mirror Collage](https://youtu.be/Vo0Pbpu113Y)
* [Sex Whales & Fraxo - Dead To Me (feat. Lox Chatterbox) [extrad1881 (ar 10)] Mirror Collage](https://youtu.be/KCHqrVGdXrk)
* [Halozy - Genryuu Kaiko [Higan Torrent] Mirror Collage](https://youtu.be/HCVIBQh4ljI)
* [Nightcore - Flower Dance [Amachoco ARX.7] Mandala Mirror Collage](https://youtu.be/HBC89S-UwFc)
* [MDK - Press Start [bhop_start_collab] - Co-Op Mirror Collage](https://youtu.be/P5mYXvH48Uk)
* [Flower Dance (osu! cursordance)](https://youtu.be/lcnnz3fN3bs)

## How to download it

### Executables
You can download Windows/Linux/MacOS 64-bit binaries from [releases](https://github.com/Wieku/danser-go/releases).

### Builded to RUN
This version was already builded by Kyow with all requirements:
+ Added a menu by Meloons - [Here you can find the Menu](https://github.com/MelonIs45/dansermenu/releases/tag/2.0)

## How to run it

### Windows executable
```bash
- Open DAИSER Menu.exe
- Click on "Main Menu"
- Search for MAP
- Choose Difficulty
- Select executable (danser***.exe)
- Create Command then Execute Command
```

### Linux/Unix/Windows(bash/Powershell) executable
```bash
./danser*** <arguments>
```

### Project

#### Prerequisites

* [64-bit go (1.15 at least)](https://golang.org/dl/)
* gcc (Linux/MacOS), [mingw-w64](http://mingw-w64.org/) (Windows)
* OpenGL library (shipped with drivers)
* xorg-dev (Linux)

#### Building and running the project

You need to enter the cloned/downloaded repository.

If you're running it for the first time or when you made some changes type:
```bash
go build
```

This will automatically download and build needed dependencies.

Then type:
```bash
./danser-go <arguments>
```

#### Arguments
* `-artist="NOMA"` or `-a="NOMA"`
* `-title="Brain Power"` or `-t="Brain Power"`
* `-difficulty="Overdrive"` or `-d="Overdrive"`
* `-creator="Skystar"` or `-c="Skystar"`
* `-md5=hash` - overrides above arguments and tries to find `.osu` file with the same MD5 hash
* `-cursors=2` - number of cursors used in mirror collage
* `-tag=2` - number of TAG cursors
* `-speed=1.5` - music speed. Value of 1.5 equals to osu!'s DoubleTime
* `-pitch=1.5` - music pitch. Value of 1.5 equals to osu!'s Nightcore pitch. To recreate osu!'s Nightcore mod, use with 1.5 speed
* `-settings=name` - if argument is not empty then app will try to load `settings-name.json` instead of `settings.json`
* `-debug` - shows more info during the map, overrides `Graphics.DrawFPS` setting
* `-play` - play through the map in osu!standard mode
* `-skip` - fade right into map's drain time
* `-scrub=20.5` - start the map at the given time (in seconds)
* `-knockout` - knockout mode

Since danser 0.4.0b full names for artist, title, difficulty and creator arguments don't have to be strict with `.osu` file. 

Examples which should give the same result:

```bash
<executable> -d="Overdrive" -tag=2 //Assuming that there is only ONE map with "Overdrive" as its difficulty name

<executable> -t="Brain Power" -d="Overdrive" -tag=2

<executable> -t "Brain Power" -d Overdrive -tag 2

<executable> -t="ain pow" -difficulty="rdrive" -tag=2

<executable> -md5=59f3708114c73b2334ad18f31ef49046 -tag=2
```

About settings or knockout usage, look at wiki.

## Credits

[osu!](https://osu.ppy.sh/) was created by osu! team ([@ppy](https://github.com/ppy)) and osu! community.

Default skin was created by [Haskorion](https://osu.ppy.sh/users/3252321): [Redd Glass HD](https://osu.ppy.sh/community/forums/topics/211396)

Uses [Exo2](https://fonts.google.com/specimen/Exo+2) font under [SIL Open Font License](http://scripts.sil.org/cms/scripts/page.php?site_id=nrsi&id=OFL_web)
