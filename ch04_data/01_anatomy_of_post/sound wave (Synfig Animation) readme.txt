To make the gif, I had Synfig output png files at 960 x 540

Then I used the command line tool ffmpeg to turn those pngs into an animated gif. I ran two commands: The first command generates a palette, and the second command uses the palette plus the png animation files to make a gif that runs at 30 frames per second.

ffmpeg -i "sound wave (Synfig Animation).%04d.png" -vf palettegen palette.png

ffmpeg -r 30 -i "sound wave (Synfig Animation).%04d.png" -i palette.png -lavfi paletteuse output.gif 