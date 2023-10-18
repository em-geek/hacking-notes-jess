#  c0rrupt

## Objetivo
We found this [file](https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery). Recover the flag.

## Solución
```bash                                                                          ┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking]  
└─$ xxd mystery | head                                                                            
00000000: 8965 4e34 0d0a b0aa 0000 000d 4322 4452  .eN4........C"DR  
00000010: 0000 066a 0000 0447 0802 0000 007c 8bab  ...j...G.....|..  
00000020: 7800 0000 0173 5247 4200 aece 1ce9 0000  x....sRGB.......  
00000030: 0004 6741 4d41 0000 b18f 0bfc 6105 0000  ..gAMA......a...  
00000040: 0009 7048 5973 aa00 1625 0000 1625 0149  ..pHYs...%...%.I  
00000050: 5224 f0aa aaff a5ab 4445 5478 5eec bd3f  R$......DETx^..?  
00000060: 8e64 cd71 bd2d 8b20 2080 9041 8302 08d0  .d.q.-.  ..A....  
00000070: f9ed 40a0 f36e 407b 9023 8f1e d720 8b3e  ..@..n@{.#... .>  
00000080: b7c1 0d70 0374 b503 ae41 6bf8 bea8 fbdc  ...p.t...Ak.....  
00000090: 3e7d 2a22 336f de5b 55dd 3d3d f920 9188  >}*"3o.[U.==. ..  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking]  
└─$ hexeditor mystery  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking]  
└─$ file mystery    
mystery: data  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking]  
└─$ hexeditor mystery  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking]  
└─$ xxd mystery | head  
00000000: 8950 4e47 0d0a 1a0a 0000 000d 4322 4452  .PNG........C"DR  
00000010: 0000 066a 0000 0447 0802 0000 007c 8bab  ...j...G.....|..  
00000020: 7800 0000 0173 5247 4200 aece 1ce9 0000  x....sRGB.......  
00000030: 0004 6741 4d41 0000 b18f 0bfc 6105 0000  ..gAMA......a...  
00000040: 0009 7048 5973 aa00 1625 0000 1625 0149  ..pHYs...%...%.I  
00000050: 5224 f0aa aaff a5ab 4445 5478 5eec bd3f  R$......DETx^..?  
00000060: 8e64 cd71 bd2d 8b20 2080 9041 8302 08d0  .d.q.-.  ..A....  
00000070: f9ed 40a0 f36e 407b 9023 8f1e d720 8b3e  ..@..n@{.#... .>  
00000080: b7c1 0d70 0374 b503 ae41 6bf8 bea8 fbdc  ...p.t...Ak.....  
00000090: 3e7d 2a22 336f de5b 55dd 3d3d f920 9188  >}*"3o.[U.==. ..  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking]  
└─$ hexeditor mystery    
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking]  
└─$ xxd mystery | head  
00000000: 8950 4e47 0d0a 1a0a 0000 000d 4948 4452  .PNG........IHDR  
00000010: 0000 066a 0000 0447 0802 0000 007c 8bab  ...j...G.....|..  
00000020: 7800 0000 0173 5247 4200 aece 1ce9 0000  x....sRGB.......  
00000030: 0004 6741 4d41 0000 b18f 0bfc 6105 0000  ..gAMA......a...  
00000040: 0009 7048 5973 aa00 1625 0000 1625 0149  ..pHYs...%...%.I  
00000050: 5224 f0aa aaff a5ab 4445 5478 5eec bd3f  R$......DETx^..?  
00000060: 8e64 cd71 bd2d 8b20 2080 9041 8302 08d0  .d.q.-.  ..A....  
00000070: f9ed 40a0 f36e 407b 9023 8f1e d720 8b3e  ..@..n@{.#... .>  
00000080: b7c1 0d70 0374 b503 ae41 6bf8 bea8 fbdc  ...p.t...Ak.....  
00000090: 3e7d 2a22 336f de5b 55dd 3d3d f920 9188  >}*"3o.[U.==. ..  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking]  
└─$ file mystery  
mystery: PNG image data, 1642 x 1095, 8-bit/color RGB, non-interlaced  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking]  
└─$ open mystery    
kf.service.services: KApplicationTrader: mimeType "x-scheme-handler/file" not found  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking]  
└─$ kf.i18n.kuit: "Unknown subcue ':whatsthis,' in UI marker in context {@info:whatsthis, %1 the action's text}."  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-aptus-mos"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-arq"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-bay"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-bmq"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-cap"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-cine"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-cs1"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-dc2"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-drf"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-dxo"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-epson-eip"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-epson-erf"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-fff"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-hasselblad-3fr"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-iiq"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-kodak-dcs"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-kodak-kc2"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-mamiya-mef"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-mfw"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-minolta-mdc"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-mng"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-obm"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-ori"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-ptx"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-pxn"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-qtk"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-r3d"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-raw"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-rdc"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-rwl"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-rwz"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-samsung-srw"  
org.kde.kdegraphics.gwenview.lib: Unresolved mime type  "image/x-sti"  
org.kde.kdegraphics.gwenview.lib: Unresolved raw mime type  "image/x-samsung-srw"  
libpng warning: pHYs: CRC error  
libpng error: PNG unsigned integer out of range  
org.kde.kdegraphics.gwenview.lib: QImageReader::read() using format hint "png" failed: "Unknown error"  
org.kde.kdegraphics.gwenview.lib: A bad Qt image decoder moved the buffer to 91 in a call to canRead()! Rewinding.  
org.kde.kdegraphics.gwenview.lib: Image format is actually "png" not "png"  
libpng warning: pHYs: CRC error  
libpng error: PNG unsigned integer out of range  
org.kde.kdegraphics.gwenview.lib: Error decoding png file  
libpng warning: pHYs: CRC error  
libpng error: PNG unsigned integer out of range  
libpng warning: pHYs: CRC error  
libpng error: PNG unsigned integer out of range  
libpng warning: pHYs: CRC error  
libpng error: PNG unsigned integer out of range  
  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking]  
└─$ sudo apt-get install pngcheck  
[sudo] password for emgeek:    
Reading package lists... Done  
Building dependency tree... Done  
Reading state information... Done  
The following packages were automatically installed and are no longer required:  
 docker-buildx-plugin docker-compose-plugin gcc-12-base libcodec2-1.1 libgcc-12-dev libgupnp-igd-1.0-4 libnfs13 libobjc-12-dev libslirp0 libstdc++-12-dev pigz  
 slirp4netns  
Use 'sudo apt autoremove' to remove them.  
The following NEW packages will be installed:  
 pngcheck  
0 upgraded, 1 newly installed, 0 to remove and 842 not upgraded.  
Need to get 68.6 kB of archives.  
After this operation, 208 kB of additional disk space will be used.  
Get:1 http://kali.download/kali kali-rolling/main amd64 pngcheck amd64 3.0.3-3 [68.6 kB]  
Fetched 68.6 kB in 1s (80.6 kB/s)  
Selecting previously unselected package pngcheck.  
(Reading database ... 445672 files and directories currently installed.)  
Preparing to unpack .../pngcheck_3.0.3-3_amd64.deb ...  
Unpacking pngcheck (3.0.3-3) ...  
Setting up pngcheck (3.0.3-3) ...  
Processing triggers for man-db (2.11.2-3) ...  
Processing triggers for kali-menu (2023.4.5) ...  
Scanning processes...                                                                                                                                                    
Scanning processor microcode...                                                                                                                                          
Scanning linux images...                                                                                                                                                 
  
Running kernel seems to be up-to-date.  
  
The processor microcode seems to be up-to-date.  
  
No services need to be restarted.  
  
No containers need to be restarted.  
  
No user sessions are running outdated binaries.  
  
No VM guests are running outdated hypervisor (qemu) binaries on this host.  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking]  
└─$ pngcheck mystery                     
mystery  CRC error in chunk pHYs (computed 38d82c82, expected 495224f0)  
ERROR: mystery  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking]  
└─$ hexeditor mystery               
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking]  
└─$ pngcheck mystery                
mystery  invalid chunk length (too large)  
ERROR: mystery  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking]  
└─$ pngcheck -v mystery  
File: mystery (202940 bytes)  
 chunk IHDR at offset 0x0000c, length 13  
   1642 x 1095 image, 24-bit RGB, non-interlaced  
 chunk sRGB at offset 0x00025, length 1  
   rendering intent = perceptual  
 chunk gAMA at offset 0x00032, length 4: 0.45455  
 chunk pHYs at offset 0x00042, length 9: 5669x5669 pixels/meter (144 dpi)  
:  invalid chunk length (too large)  
ERRORS DETECTED in mystery  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking]  
└─$ hexeditor mystery     
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking]  
└─$ pngcheck -v mystery  
File: mystery (202940 bytes)  
 chunk IHDR at offset 0x0000c, length 13  
   1642 x 1095 image, 24-bit RGB, non-interlaced  
 chunk sRGB at offset 0x00025, length 1  
   rendering intent = perceptual  
 chunk gAMA at offset 0x00032, length 4: 0.45455  
 chunk pHYs at offset 0x00042, length 9: 5669x5669 pixels/meter (144 dpi)  
:  invalid chunk length (too large)  
ERRORS DETECTED in mystery  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking]  
└─$ hexeditor mystery     
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking]  
└─$ pngcheck -v mystery  
File: mystery (202940 bytes)  
 chunk IHDR at offset 0x0000c, length 13  
   1642 x 1095 image, 24-bit RGB, non-interlaced  
 chunk sRGB at offset 0x00025, length 1  
   rendering intent = perceptual  
 chunk gAMA at offset 0x00032, length 4: 0.45455  
 chunk pHYs at offset 0x00042, length 9: 5669x5669 pixels/meter (144 dpi)  
 chunk IDAT at offset 0x00057, length 65445  
   zlib: deflated, 32K window, fast compression  
 chunk IDAT at offset 0x10008, length 65524  
 chunk IDAT at offset 0x20008, length 65524  
 chunk IDAT at offset 0x30008, length 6304  
 chunk IEND at offset 0x318b4, length 0  
No errors detected in mystery (9 chunks, 96.3% compression).  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking]  
└─$ open mystery    
```


## Notas adicionales


## Referencias

https://youtu.be/7zY4VkiWbBI?si=IeJci0_CGgHhMHm_