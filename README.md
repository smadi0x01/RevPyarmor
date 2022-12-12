## Get Started
- <h4> Firstly download the Pytractor.py file </h4>
- <h4> virustotal of file:</h4> https://www.virustotal.com/gui/file/ccb36820cb53149b83b3f4429dbe3b0687eebe8331a0f5e6d0a36f1e23595e66/detection

## Steps

- Use pyinstxtractor.py to extract the executable in Python 3.7
- Using the extracted files, create the following directory structure: 
<details><title>Details</title>

|-- martisor.pyc

-- pytransform

|-- __init__.py

|-- _pytransform.dll

|-- license.lic
-- pytransform.key

>> One directory, Five files for running on Linux, you need _pytransform.so downloadable from https://pyarmor.dashingsoft.com/platforms.html
</details>

- Install psutil using pip (Required for pyarmor). From now on, you can just run python3.7 martisor.pyc instead of the unpackme executable.

- Pyarmor encrypts the code objects on disk and they are only decrypted at runtime just before they are executed. The entire logic is implemented in _pytransform.dll. There are anti-debugging/timing checks to prevent us from using a debugger to dump code objects from memory. 
But there's no need to use a debugger at all when CPython itself is open source. 

- Compile Python 3.7 from source. Modify the _PyEval_EvalFrameDefault function such that it dumps the code object to disk. By doing so we do not need to bother about all the anti-debugging and encrypted stuff. This is because pyarmor decrypts the code object in memory before it hands it to the Python VM for execution.

- Run strings on the dumped code  object. We get many base64 strings. Like this one: CkdFTkVSQVRFLUtFWS0wWDcyR09ELVVOUEFDS01FCg==

- Finally, decode base64 & Enjoy The Movement!
