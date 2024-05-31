***Software for automated analysis of ultrasound-activated microbubble interactions***

The application was made by Rares Comanici as a 4th year honours project under the supervision of Paul Campbell at the University of Dundee, United Kingdom.

The purpose of this software is to illustrate an early iteration of computer vision-aided detection of UCAs (ultrasound contrast agents).

Coded in the Wolfram language, under the Mathematica 14.0 environment for the fast expression-based language and in-built computer vision functions (plans to adapt it to Python in the near future).


***Setup and requirements***

Please note the project was coded and run under a Windows 11 machine and while there no issues to be expected on Windows 10, there might be signficant differences when the software is run on earlier versions of Windows (8/7/Vista/XP).

The software was not tested on any Unix-based systems (Linux or MacOS) as part of testing so it is uncertain whether or not there are compatibility issues on those platforms.

To run the project, select and download the latest notebook in the GitHub repository (31-3-2024_timestamps_final.nb) and the latest version of the Mathematica software of the official Wolfram website.

After both installs, the notebook should be accessible and editable.


***Data formats and import/export***

Several data formats are accepted (.jpg/.jpeg/.png/.bmp), though only .jpeg was tested due to the nature of the trial data courtesy of Paul Prentice.

For data scanning, make sure ALL the image data desired to be scanned at one time is placed within a folder of choice, since the routine will not look beyond the specified path.

To select the desired folder path, press Ctrl+F and write 'Replace with frame folder location' in the Find text bar. That will lead you to the SetDirectory command line in which the location of the data folder can be inputted. Make sure to put the folder path within the square brackets and within quotes (the program will return an error if not input properly).

Just under the SetDirectory line, you will encounter an Import command. Under the FileNames, you can choose which files you want to be read from the folder by choosing the naming pattern. For a surefire way of getting all data scanned, the '*' is any filename before the extension ('.jpg'). If you wish to read .bmp files for example, simply replace the "*.jpg" with "*.bmp" and proceed.

After this step is completed, press Ctrl+F again and write 'Replace with your directory of choice for the exported file' in the Find text bar. This will take you to another SetDirectory command line in which you should input the desired folder location path of the output (an .csv file). To change the filename of the output or the format, go to the Export command line below and replace "results.csv" with your desired output name and extension. If you desire to export the data to other formats (i.e. .xlsx), you have to mention it both in the filename ("results.xlsx" for example) and in place of "CSV" ("XLSX" for example) in all caps. Note that .csv formats are faster and have been tested with all trial data, whereas .xlsx has only been tested a few times and while it did not create any issues, you might encounter unexpected errors regarding measurement accuracy (due to the data logging constraints in regular Excel formats) or even while running the Mathematica notebook.


***Credits***

Rares Comanici (https://github.com/rarescomanici)

Thanks to Paul Campbell for guidance in this project.

GitHub repository can be found here: https://github.com/rarescomanici/bubble_honours_project


***License***

MIT License

Copyright (c) [2024] [Rares Comanici]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
