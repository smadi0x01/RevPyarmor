![image](https://user-images.githubusercontent.com/75253629/198406644-f75ec147-0e46-4326-a999-06a052f0721e.png)

## Get Started

- <h4> Firstly download the Pytractor.py file </h4>
- <h4> virustotal of file:</h4> https://www.virustotal.com/gui/file/ccb36820cb53149b83b3f4429dbe3b0687eebe8331a0f5e6d0a36f1e23595e66/detection

## Steps

```bash Use pytractor.py to extract the executable in Python 3.7 
bash Using the extracted files, create the following directory structure: ```
<details><summary>Click Here</summary>

|-- martisor.pyc

-- pytransform

|-- __init__.py

|-- _pytransform.dll

|-- license.lic
-- pytransform.key
>> One directory, Five files for running on Linux, you need _pytransform.so downloadable from https://pyarmor.dashingsoft.com/platforms.html
</details>

- Install psutil using pip (required for pyarmor). From now on, you can just run python3.7 martisor.pyc instead of the unpackme executable. ```

- Pyarmor encrypts the code objects on disk and they are only decrypted at runtime just before they are executed. The entire logic is implemented in _pytransform.dll. There are anti-debugging/timing checks to prevent us from using a debugger to dump code objects from memory. 
But there's no need to use a debugger at all when CPython itself is open source.

- Compile python 3.7 from source. Modify the _PyEval_EvalFrameDefault function such that it dumps the code object to disk. By doing so we do not need to bother about all the anti-debugging and encrypted stuff. This is because pyarmor decrypts the code object in memory before it hands it to the Python VM for execution.

- Run strings on the dumped code  object. We get many base64 strings. Like this one: CkdFTkVSQVRFLUtFWS0wWDcyR09ELVVOUEFDS01FCg==

- Finally, decode base64 & Enjoy The Movement!

## ⚠️ Important
- This technique doesnt work for paid pyarmor or wrap (not 100% sure on wrap) protection there are better methods to reverse it, cause you can also just get the bytecode which would be way more easy then you patch it, no clue if this still works on lastest versions (the method)

## ⚠️ Disclaimer :
- I am not responsible for any misuse of this information, its only for education purposes 

## 📞 Contact :
<p align="center">
<a href="https://instagram.com/smadi0x01" target="blank"><img align="center" src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/instagram.svg" alt="smadi" height="25" width="25" /></a>
<a href="https://linkedin.com/in/saud-smadi" target="blank"><img align="center" src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/linkedin.svg" alt="smadi" height="25" width="25" /></a>
<a href="https://t.me/rootsmadi" target="blank"><img align="center" src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/telegram.svg" alt="smadi" height="25" width="25" /></a>
</p>
