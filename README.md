Gigapan-Downloader-and-stitcher
===============================

##Gigapan Panorama Downloader and offline stitcher to Photoshop PSB or TIFF. 

This cross-platform Python 2.X script downloads gigapan pictures at the resolution specified and very fast stitch (assemble) with export to one big PSB (Photoshop Large Image file) or TIFF using Imagemagick.  
Work in Windows and in any Linux.  
Can resume download, downloaded tiles not reloaded. Will download all missing tiles  

###How to run?
1. Install Python 2.X (3.X is not supported) from python.org (Windows) or use "yum install python2.7" or similar command in Linux.  
2. Install Imagemagick from http://www.imagemagick.org/script/binary-releases.php#windows (Windows). I recommend install ImageMagick-*-x64-static.exe x64 version, if you have x64 OS. For Linux use "yum install imagemagick" or similar command.  
3. Download this script using "Save As" from https://raw.github.com/DeniR/Gigapan-Downloader-and-stitcher/master/gigapanDownloader.py  
4. Change path to montage.exe in gigapanDownloader.py (Windows, default is "C:\\Program Files\\ImageMagick-6.8.5-Q16\\montage.exe") or change default /usr/bin/montage in Linux.  
5. Select outputformat in gigapanDownloader.py - psb for large gigapans (default) or tif.  
6. Run **python gigapanDownloader.py \<imageid> \<level>** in cmd or console. All tiles of the specified resolution level will be downloaded to \<imageid> directory, and stitched gigapan will be exported to <imageid>-giga.psb.

Example, http://www.gigapan.com/gigapans/130095  
The \<imageid> is 130095

python gigapanDownloader.py 130095 5  
This will download the level 5 image tiles into directory "130095" and will make gigapan image "130095-giga.psb"
Important: If you want to download the highest resolution level avaiable choose level 0  

###Note

Gigapan site is very slow, also this script use only one thread. If you want to add multithreaded download - you are welcome.
You can try with different resolution levels to see the size of the image that will be downloaded and choose the level you need, just remember to delete the downloaded tiles