## Get Started
- Firstly download the Pytractor.py file
- Here's the virustotal of file: https://www.virustotal.com/gui/file/ccb36820cb53149b83b3f4429dbe3b0687eebe8331a0f5e6d0a36f1e23595e66/detection

## Steps

- Use pyinstxtractor.py to extract the executable in Python 3.7
- Using the extracted files, create the following directory structure:
.
|-- martisor.pyc

`-- pytransform

|-- __init__.py

|-- _pytransform.dll

|-- license.lic

`-- pytransform.key
>> One directory, Five files for running on Linux, you need _pytransform.so downloadable from https://pyarmor.dashingsoft.com/platforms.html

- Install psutil using pip (Required for pyarmor). From now on, you can just run python3.7 martisor.pyc instead of the unpackme executable.
- pyarmor encrypts the code objects on disk and they are only decrypted at runtime just before they are executed. The entire logic is implemented in _pytransform.dll. There are anti-debugging/timing checks to prevent us from using a debugger to dump code objects from memory. 
But there's no need to use a debugger at all when CPython itself is open source. 
