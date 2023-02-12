# Patchify
 
 This code is a script to split a large TIFF file into smaller tiles of a specified size (500 x 500 pixels in this case). The script uses the GDAL library to read the TIFF files and create smaller tiles.

The code first checks if the output folder exists, and creates it if it doesn't. Then, it iterates over all files in the input folder and only considers TIFF files (files ending with '.tif').

For each TIFF file, it calculates the number of rows and columns of tiles required to cover the entire image and then iterates over the rows and columns to extract the tiles. The tiles are extracted using the gdal.Translate method and saved in the output folder with a file name indicating the row and column number of the tile.

Finally, the code also handles the case of the last tile of each row which may be smaller than the specified tile size (250 x 512 pixels in this case). This tile is extracted in the same way as the other tiles, and saved with a file name indicating it's the last column tile for the respective row.
