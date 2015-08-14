# Introduction #

A tutorial to create Tesseract Engine 3.01/3.x .net wrapper.

# Details #

**The current version supported to extract locations of detected characters. Also, you can run parallel for a set of images.**

Below is a quick tutorial:


**Note: Use [sources](http://tesseract-ocr.googlecode.com/svn/trunk/)/[tessdata](http://tesseract-ocr.googlecode.com/svn/trunk/tessdata/)/[third party](http://tesseract-ocr.googlecode.com/svn/trunk/vs2008/lib/) from svn; [tesseract-ocr](http://code.google.com/p/tesseract-ocr/) version should be 3.01 [r552](https://code.google.com/p/tesseractdotnet/source/detail?r=552)**

1.
Download all files at: [TesseractEngineWrapper](https://tesseractdotnet.googlecode.com/svn/trunk/dotnetwrapper/TesseractEngineWrapper)

> Merge downloaded files with your source code. **You can also do copy and override, if you make sure that your source code version is 3.01 [r552](https://code.google.com/p/tesseractdotnet/source/detail?r=552).**



2.
Add two new files ([tesseractenginewrapper.h](http://code.google.com/p/tesseractdotnet/source/browse/trunk/dotnetwrapper/TesseractEngineWrapper/tesseractenginewrapper.h) and [tesseractenginewrapper.cpp](http://code.google.com/p/tesseractdotnet/source/browse/trunk/dotnetwrapper/TesseractEngineWrapper/tesseractenginewrapper.cpp)) to [tesseract project](http://code.google.com/p/tesseract-ocr/)


3.
Changed the project settings as belows:

> Configuration Type: **Dynamic Library (.dll)**

> Common Language Runtime Support: **Old Syntax (/clr:oldSyntax)**

> Output File: **tesseractengine3.dll**

> Also need to add **System, System.Drawing** assembly to **Common Properties\Framework and References**

4.
After that, apply building the project.



**Note:**
You can also find simple application at [dotnetwrapper](https://tesseractdotnet.googlecode.com/svn/trunk/dotnetwrapper)

If you use above application; you have to configure tesseract engine first (from **main menu >> tools >> options**), and copy Leptonica library to application path.