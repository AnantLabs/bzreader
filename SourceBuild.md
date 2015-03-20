# Introduction #

How to build BzReader in 11 steps with free tools only.

  1. Download TortoiseSvn from http://tortoisesvn.net/downloads
  1. Create a folder BzReader
  1. Right click in this empty folder and select "SVN Checkout"
  1. Fill "http://bzreader.googlecode.com/svn/trunk/" in the first textbox, leave the second textbox as is and press OK. It should download the latest version
  1. Go to http://www.microsoft.com/express/2005/download/default.aspx and download and install Visual C++ 2005  Express and Visual C# 2005 Express
  1. Go to http://www.microsoft.com/downloads/details.aspx?familyid=71DEB800-C591-4F97-A900-BEA146E4FAE1&displaylang=en to download and install Platform SDK
  1. Open BzReader.sln in Visual C++ Express
  1. Select Tools -> Options -> Projects and Solutions -> VC++ Directories and add these paths:
    * Executable files: C:\Program Files\Microsoft Platform SDK\Bin
    * Include files: C:\Program Files\Microsoft Platform SDK\include
    * Library files: C:\Program Files\Microsoft Platform SDK\lib
  1. Build the bzip2 library
  1. Close the Visual C++ Express and open the solution file again, but now in Visual C# Express
  1. Build it and feel free to modify it and send patches :)