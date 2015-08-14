# Introduction #

New version of tesseractdotnetwrapper has released on 2011 July, 04.

It is based-on tesseract-ocr v3.01 [r590](https://code.google.com/p/tesseractdotnet/source/detail?r=590).

Here is the link:
http://code.google.com/p/tesseractdotnet/

http://tesseractdotnet.googlecode.com/files/tesseractdotnetwrapper_r590.zip

http://tesseractdotnet.googlecode.com/files/IPoVn_Release_x86.zip

**Notes: developed on vs2008 team. All assemblies should work well on x86 platform application.**

# Details #

**Changed logs and notes:**

- libleptxxx.dll is replaced by integrating directly its static librarian inside tesseract project,

- use ROI, UseROI properties for recognition in region of interest (see: Simple3.cs in IPoVnOCRer project),

- added: CreateBinaryPix(), CreateGreyPix() in PixConverter (PixFromImage maybe will be deprecated),

- created new document layout (adapt to tesseract-engine v3.01 [r590](https://code.google.com/p/tesseractdotnet/source/detail?r=590)) structure: DocumentLayout >> Block >> Paragraph >> TextLine >> Word >> Character/Symbol,

- be able to set tessdata path,

- be able to recognize with others OcrEngineMode,

- be able to analyze layout only,

- be able to recognize in parallel, see Simple3.cs in IPoVnOCRer project,

- use IPoVn.IPCore to load/save/crop/invert/binarize image in generic image format,

- test tesseract.dll in .net 4/vs2010 please look at Simple1.cs only, other **.cs maybe need to compile IPoVn.IPCore project,**

- be able to own your flow to process:

----- 0. Do some pre-processing first (in my case: adaptive thresholding was performed)

----- 1. AnalyseLayout() -> get blobs (block/paragraph/textline/word....)

----- 2. Do some image processing for each blobs

----- 3. Recognize for each ROI/blobs with OcrEngineMode/PageSegmentMode corresponding to

----- 4. Do some post-processing (VietOCR is an example).

IPoVnOCRer project:

- Simple1.cs: use tesseract.dll only
----- example to recognize and analyze layout.

- Simple2.cs: tesseract.dll + IPoVn.IPCore + IPoVnSystem
----- example to recognize and analyze layout after performing adaptive thresholding.

- Simple3.cs: tesseract.dll + IPoVn.IPCore + IPoVnSystem
----- example to recognize in ROIs