# Lego

Extracts and decompresses .fib archives found in various Lego games.

## Games Tested

* LEGO Batman 3: Beyond Gotham (3DS)
* LEGO Harry Potter: Years 1-4 (PSP)
* LEGO Harry Potter: Years 5-7 (3DS/PSP)
* The LEGO Movie Videogame (Vita)
* LEGO Pirates of the Caribbean (3DS)
* LEGO Star Wars III: The Clone Wars (3DS/PSP)

## Notes

Some games come with accompanying csv files that list filenames. If one is
found, it will be used. Otherwise, the script will make a semi-educated guess
as to what the appropriate file extension should be based on similarities to
known formats. Chances are high it will be wrong in many instances, as the IDs
used in the file headers appear to shuffle around a bit between games.

For a (little) more accuracy, you can provide the fib_ex function with the
platform the .fib file was obtained from, and it will try to use that information
to better guess the correct file extension.

Image data is assigned the mostly arbitrary extension of .lga and should be
supported by [Scarlet](https://github.com/xdanieldzd/Scarlet) in the near future.

Audio data is assigned the extension .lwav—based on what I've seen, these are
custom containers that store one or more Nintendo 3DS CWAV files and/or some
form of PSP audio.

## Acknowledgements

* [FireyFly](https://github.com/FireyFly) for the decompression algorithm.
* [xdanieldzd](https://github.com/xdanieldzd) for the image formats.
