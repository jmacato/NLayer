# Nlayer

NLayer is a fully managed MP3 to WAV decoder. The code was originally based 
on [JavaLayer](http://www.javazoom.net/javalayer/javalayer.html) (v1.0.1), 
which has been ported to C#.



## Usage

To use NLayer for decoding MP3, first import NLayer.Core via your NuGet package manager or by executing `dotnet add package NLayer.Core` on your project root.

```cs
using NLayer;
```

Then create an `MpegFile`, pass a file name or a stream to the constructor, and use `ReadSamples` for decoding the content:

```cs
var fileName = "myMp3File.mp3";
var mpegFile = new MpegFile(filename);
float[] samples = new float[44100];
mpegFile.ReadSamples(samples, 0, 44100);
```

More information could be found in code documents.

## Use with NAudio

This fork removed the option for NAudio support.
