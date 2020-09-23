<div align="center">

## \* Make Your Own \*WAV\* Player\! \*


</div>

### Description

This is the code to *PLAY*, *STOP*, and *LOOP* WAV files. Its really easy! even for a beginner! You can make your own WAV Player!
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Matt Evans](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/matt-evans.md)
**Level**          |Unknown
**User Rating**    |2.6 (13 globes from 5 users)
**Compatibility**  |VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0
**Category**       |[Windows API Call/ Explanation](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/windows-api-call-explanation__1-39.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/matt-evans-make-your-own-wav-player__1-1654/archive/master.zip)

### API Declarations

```
Declare Function sndPlaySound Lib "winmm.dll" Alias "sndPlaySoundA" (ByVal lpszSoundName As String, ByVal uFlags As Long) As Public Const SND_SYNC = &H0
Public Const SND_ASYNC = &H1
Public Const SND_NODEFAULT = &H2
Public Const SND_MEMORY = &H4
Public Const SND_LOOP = &H8
Public Const SND_NOSTOP = &H10
```


### Source Code

```
Sub WAVStop()
Call WAVPlay(" ")
End Sub
Sub WAVLoop(File)
Dim SoundName As String
SoundName$ = File
wFlags% = SND_ASYNC Or SND_LOOP
X = sndPlaySound(SoundName$, wFlags%)
End Sub
Sub WAVPlay(File)
Dim SoundName As String
SoundName$ = File
wFlags% = SND_ASYNC Or SND_NODEFAULT
X = sndPlaySound(SoundName$, wFlags%)
End Sub
```

