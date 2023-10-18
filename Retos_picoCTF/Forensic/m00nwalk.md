#  m00nwalk

## Objetivo
Decode this [message](https://jupiter.challenges.picoctf.org/static/d6fcea5e3c6433680ea4f914e24fab61/message.wav) from the moon.

## Solución
```bash                                                                         
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking]  
└─$ wget https://jupiter.challenges.picoctf.org/static/d6fcea5e3c6433680ea4f914e24fab61/message.wav  
--2023-10-17 23:47:03--  https://jupiter.challenges.picoctf.org/static/d6fcea5e3c6433680ea4f914e24fab61/message.wav  
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8  
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.  
HTTP request sent, awaiting response... 200 OK  
Length: 11066998 (11M) [application/octet-stream]  
Saving to: ‘message.wav’  
  
message.wav                               100%[===================================================================================>]  10.55M   965KB/s    in 14s        
  
2023-10-17 23:47:17 (780 KB/s) - ‘message.wav’ saved [11066998/11066998]  
  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking]  
└─$ open message.wav    
kf.service.services: KApplicationTrader: mimeType "x-scheme-handler/file" not found  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking]  
└─$ I: 23:48:21,513 tagger.main:1541: Sending messages to main instance: ['LOAD /home/emgeek/Documents/pruebasHacking/message.wav']  
  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking]  
└─$ git clone https://github.com/colaclanth/sstv.git  
Cloning into 'sstv'...  
remote: Enumerating objects: 221, done.  
remote: Counting objects: 100% (59/59), done.  
remote: Compressing objects: 100% (10/10), done.  
remote: Total 221 (delta 51), reused 49 (delta 49), pack-reused 162  
Receiving objects: 100% (221/221), 1.01 MiB | 570.00 KiB/s, done.  
Resolving deltas: 100% (139/139), done.  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking]  
└─$ cd sstv             
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking/sstv]  
└─$ ls  
LICENSE  README.md  examples  setup.py  sstv  test  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking/sstv]  
└─$ python3 setup.py install  
running install  
/usr/lib/python3/dist-packages/setuptools/_distutils/cmd.py:66: SetuptoolsDeprecationWarning: setup.py install is deprecated.  
!!  
  
       ********************************************************************************  
       Please avoid running ``setup.py`` directly.  
       Instead, use pypa/build, pypa/installer, pypa/build or  
       other standards-based tools.  
  
       See https://blog.ganssle.io/articles/2021/10/setup-py-deprecated.html for details.  
       ********************************************************************************  
  
!!  
 self.initialize_options()  
/usr/lib/python3/dist-packages/setuptools/_distutils/cmd.py:66: EasyInstallDeprecationWarning: easy_install command is deprecated.  
!!  
  
       ********************************************************************************  
       Please avoid running ``setup.py`` and ``easy_install``.  
       Instead, use pypa/build, pypa/installer, pypa/build or  
       other standards-based tools.  
  
       See https://github.com/pypa/setuptools/issues/917 for details.  
       ********************************************************************************  
  
!!  
 self.initialize_options()  
error: can't create or remove files in install directory  
  
The following error occurred while trying to add or remove files in the  
installation directory:  
  
   [Errno 13] Permission denied: '/usr/local/lib/python3.11/dist-packages/test-easy-install-11482.write-test'  
  
The installation directory you specified (via --install-dir, --prefix, or  
the distutils default setting) was:  
  
   /usr/local/lib/python3.11/dist-packages/  
  
Perhaps your account does not have write access to this directory?  If the  
installation directory is a system-owned directory, you may need to sign in  
as the administrator or "root" account.  If you do not have administrative  
access to this machine, you may wish to choose a different installation  
directory, preferably one that is listed in your PYTHONPATH environment  
variable.  
  
For information on other options, you may wish to consult the  
documentation at:  
  
 https://setuptools.pypa.io/en/latest/deprecated/easy_install.html  
  
Please make the appropriate changes for your system and try again.  
  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking/sstv]  
└─$ sudo python3 setup.py install  
[sudo] password for emgeek:    
running install  
/usr/lib/python3/dist-packages/setuptools/_distutils/cmd.py:66: SetuptoolsDeprecationWarning: setup.py install is deprecated.  
!!  
  
       ********************************************************************************  
       Please avoid running ``setup.py`` directly.  
       Instead, use pypa/build, pypa/installer, pypa/build or  
       other standards-based tools.  
  
       See https://blog.ganssle.io/articles/2021/10/setup-py-deprecated.html for details.  
       ********************************************************************************  
  
!!  
 self.initialize_options()  
/usr/lib/python3/dist-packages/setuptools/_distutils/cmd.py:66: EasyInstallDeprecationWarning: easy_install command is deprecated.  
!!  
  
       ********************************************************************************  
       Please avoid running ``setup.py`` and ``easy_install``.  
       Instead, use pypa/build, pypa/installer, pypa/build or  
       other standards-based tools.  
  
       See https://github.com/pypa/setuptools/issues/917 for details.  
       ********************************************************************************  
  
!!  
 self.initialize_options()  
running bdist_egg  
running egg_info  
creating sstv.egg-info  
writing sstv.egg-info/PKG-INFO  
writing dependency_links to sstv.egg-info/dependency_links.txt  
writing entry points to sstv.egg-info/entry_points.txt  
writing requirements to sstv.egg-info/requires.txt  
writing top-level names to sstv.egg-info/top_level.txt  
writing manifest file 'sstv.egg-info/SOURCES.txt'  
reading manifest file 'sstv.egg-info/SOURCES.txt'  
adding license file 'LICENSE'  
writing manifest file 'sstv.egg-info/SOURCES.txt'  
installing library code to build/bdist.linux-x86_64/egg  
running install_lib  
running build_py  
creating build  
creating build/lib  
creating build/lib/sstv  
copying sstv/command.py -> build/lib/sstv  
copying sstv/__init__.py -> build/lib/sstv  
copying sstv/common.py -> build/lib/sstv  
copying sstv/decode.py -> build/lib/sstv  
copying sstv/__main__.py -> build/lib/sstv  
copying sstv/spec.py -> build/lib/sstv  
creating build/bdist.linux-x86_64  
creating build/bdist.linux-x86_64/egg  
creating build/bdist.linux-x86_64/egg/sstv  
copying build/lib/sstv/command.py -> build/bdist.linux-x86_64/egg/sstv  
copying build/lib/sstv/__init__.py -> build/bdist.linux-x86_64/egg/sstv  
copying build/lib/sstv/common.py -> build/bdist.linux-x86_64/egg/sstv  
copying build/lib/sstv/decode.py -> build/bdist.linux-x86_64/egg/sstv  
copying build/lib/sstv/__main__.py -> build/bdist.linux-x86_64/egg/sstv  
copying build/lib/sstv/spec.py -> build/bdist.linux-x86_64/egg/sstv  
byte-compiling build/bdist.linux-x86_64/egg/sstv/command.py to command.cpython-311.pyc  
byte-compiling build/bdist.linux-x86_64/egg/sstv/__init__.py to __init__.cpython-311.pyc  
byte-compiling build/bdist.linux-x86_64/egg/sstv/common.py to common.cpython-311.pyc  
byte-compiling build/bdist.linux-x86_64/egg/sstv/decode.py to decode.cpython-311.pyc  
byte-compiling build/bdist.linux-x86_64/egg/sstv/__main__.py to __main__.cpython-311.pyc  
byte-compiling build/bdist.linux-x86_64/egg/sstv/spec.py to spec.cpython-311.pyc  
creating build/bdist.linux-x86_64/egg/EGG-INFO  
copying sstv.egg-info/PKG-INFO -> build/bdist.linux-x86_64/egg/EGG-INFO  
copying sstv.egg-info/SOURCES.txt -> build/bdist.linux-x86_64/egg/EGG-INFO  
copying sstv.egg-info/dependency_links.txt -> build/bdist.linux-x86_64/egg/EGG-INFO  
copying sstv.egg-info/entry_points.txt -> build/bdist.linux-x86_64/egg/EGG-INFO  
copying sstv.egg-info/requires.txt -> build/bdist.linux-x86_64/egg/EGG-INFO  
copying sstv.egg-info/top_level.txt -> build/bdist.linux-x86_64/egg/EGG-INFO  
zip_safe flag not set; analyzing archive contents...  
creating dist  
creating 'dist/sstv-0.1-py3.11.egg' and adding 'build/bdist.linux-x86_64/egg' to it  
removing 'build/bdist.linux-x86_64/egg' (and everything under it)  
Processing sstv-0.1-py3.11.egg  
Copying sstv-0.1-py3.11.egg to /usr/local/lib/python3.11/dist-packages  
Adding sstv 0.1 to easy-install.pth file  
Installing sstv script to /usr/local/bin  
  
Installed /usr/local/lib/python3.11/dist-packages/sstv-0.1-py3.11.egg  
Processing dependencies for sstv==0.1  
Searching for PySoundFile  
Reading https://pypi.org/simple/PySoundFile/  
Downloading https://files.pythonhosted.org/packages/2a/b3/0b871e5fd31b9a8e54b4ee359384e705a1ca1e2870706d2f081dc7cc1693/PySoundFile-0.9.0.post1-py2.py3-none-any.whl#sh  
a256=db14f84f4af1910f54766cf0c0f19d52414fa80aa0e11cb338b5614946f39947  
Best match: PySoundFile 0.9.0.post1  
Processing PySoundFile-0.9.0.post1-py2.py3-none-any.whl  
Installing PySoundFile-0.9.0.post1-py2.py3-none-any.whl to /usr/local/lib/python3.11/dist-packages  
Adding PySoundFile 0.9.0.post1 to easy-install.pth file  
detected new path './sstv-0.1-py3.11.egg'  
  
Installed /usr/local/lib/python3.11/dist-packages/PySoundFile-0.9.0.post1-py3.11.egg  
Searching for scipy==1.10.1  
Best match: scipy 1.10.1  
Adding scipy 1.10.1 to easy-install.pth file  
detected new path './PySoundFile-0.9.0.post1-py3.11.egg'  
  
Using /usr/lib/python3/dist-packages  
Searching for numpy==1.24.2  
Best match: numpy 1.24.2  
Adding numpy 1.24.2 to easy-install.pth file  
Installing f2py script to /usr/local/bin  
Installing f2py3 script to /usr/local/bin  
Installing f2py3.11 script to /usr/local/bin  
  
Using /usr/lib/python3/dist-packages  
Searching for Pillow==10.0.0  
Best match: Pillow 10.0.0  
Adding Pillow 10.0.0 to easy-install.pth file  
  
Using /usr/lib/python3/dist-packages  
Searching for cffi==1.15.1  
Best match: cffi 1.15.1  
Adding cffi 1.15.1 to easy-install.pth file  
  
Using /usr/lib/python3/dist-packages  
Finished processing dependencies for sstv==0.1  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking/sstv]  
└─$ cd ..     
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking]  
└─$ ls  
990.tar  message.wav  mystery  sstv  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking]  
└─$ sstv -d message.wav -o resultado.png  
[sstv] Searching for calibration header... Found!       
[sstv] Detected SSTV mode Scottie 1  
[sstv] Decoding image...                                   [####################################################################################################] 100%  
[sstv] Drawing image data...  
[sstv] ...Done!  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking]  
└─$ open resultado.png

```

la bandera es: picoCTF{beep_boop_im_in_space}
## Notas adicionales


## Referencias