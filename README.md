# Patchify

# Split Large TIFF Files into Smaller Tiles

This code is a script that can split large TIFF files into smaller tiles of a specified size (in this case, 500 x 500 pixels). It uses the GDAL library to read the TIFF files and create the smaller tiles.

The script first checks if the output folder exists and creates it if it doesn't. Then, it goes through all the files in the input folder and only considers TIFF files (those with the file extension ".tif").

For each TIFF file, it calculates the number of rows and columns of tiles required to cover the entire image, and then iterates over the rows and columns to extract the tiles. The tiles are extracted using the gdal.Translate method and saved in the output folder with a file name indicating the row and column number of the tile.

The code also handles the case of the last tile of each row, which may be smaller than the specified tile size (in this case, 250 x 512 pixels). This tile is extracted in the same way as the other tiles and saved with a file name indicating that it's the last column tile for the respective row.

Overall, this script provides an efficient way to split large TIFF files into smaller tiles for further processing.