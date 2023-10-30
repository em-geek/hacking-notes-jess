#  Matryoshka doll

## Objetivo
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/205adad23bf9d8303081a0e71c9beab8/dolls.jpg)

## Solución
```bash                                                                          ..
..
..
┌──(emgeek㉿EmGeek-Kali-PC)-[~/…/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]  
└─$ cd _4_c.jpg.extracted    
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/…/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted]  
└─$ ls  
136DA.zip  flag.txt  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/…/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted]  
└─$ cat flag.txt    
picoCTF{96fac089316e094d41ea046900197662}
                                                                                                                                                                  ```

Se le aplico una y otra vez binwalk a las imagens que iban sakiendo hasta que llegamos a la flag

## Notas adicionales


## Referencias