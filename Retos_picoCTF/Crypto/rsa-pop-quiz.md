#  rsa-pop-quiz

## Objetivo
Class, take your seats! It's PRIME-time for a quiz... `nc jupiter.challenges.picoctf.org 58617`

## Solución
Problema 1: 4636878989
Problema 2: 93089
Problema 3: NO
Problema 4: 836623060
Problema 5: 256931246631782714357241556582441991993437399854161372646318659020994329843524306570818293602492485385337029697819837182169818816821461486018802894936801257629375428544752970630870631166355711254848465862207765051226282541748174535990314552471546936536330397892907207943448897073772015986097770443616540466471245438117157152783246654401668267323136450122287983612851171545784168132230208726238881861407976917850248110805724300421712827401063963117423718797887144760360749619552577176382615108244813
Problema 6: NO
Problema 7: 1405046269503207469140791548403639533127416416214210694972085079171787580463776820425965898174272870486015739516125786182821637006600742140682552321645503743280670839819078749092730110549881891271317396450158021688253989767145578723458252769465545504142139663476747479225923933192421405464414574786272963741656223941750084051228611576708609346787101088759062724389874160693008783334605903142528824559223515203978707969795087506678894006628296743079886244349469131831225757926844843554897638786146036869572653204735650843186722732736888918789379054050122205253165705085538743651258400390580971043144644984654914856729
Problema 8: 
14311663942709674867122208214901970650496788151239520971623411712977119660454037678408741501

```bash
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking]  
└─$ nc jupiter.challenges.picoctf.org 58617  
Good morning class! It's me Ms. Adleman-Shamir-Rivest  
Today we will be taking a pop quiz, so I hope you studied. Cramming just will not  
do!  
You will need to tell me if each example is possible, given your extensive crypto  
knowledge.  
Inputs and outputs are in decimal. No hex here!  
#### NEW PROBLEM ####  
q : 60413  
p : 76753  
##### PRODUCE THE FOLLOWING ####  
n  
IS THIS POSSIBLE and FEASIBLE? (Y/N):Y  
#### TIME TO SHOW ME WHAT YOU GOT! ###  
n: 4636878989  
Outstanding move!!!  
  
  
#### NEW PROBLEM ####  
p : 54269  
n : 5051846941  
##### PRODUCE THE FOLLOWING ####  
q  
IS THIS POSSIBLE and FEASIBLE? (Y/N):Y  
#### TIME TO SHOW ME WHAT YOU GOT! ###  
q: 93089  
Outstanding move!!!  
  
  
#### NEW PROBLEM ####  
e : 3  
n : 12738162802910546503821920886905393316386362759567480839428456525224226445173  
031635306683726182522494910808518920409019414034814409330094245825749680913204566  
832337704700165993198897029795786969124232138869784626202501366135975223827287812  
326250577148625360887698930625504334325804587329905617936581116392784684334664204  
309771430814449606147221349888320403451637882447709796221706470239625292297988766  
493746209684880843111138170600039888112404411310974758532603998608057008811836384  
597579147244737606088756299939654265086899096359070667266167754944587948695842171  
915048619846282873769413489072243477764350071787327913  
##### PRODUCE THE FOLLOWING ####  
q  
p  
IS THIS POSSIBLE and FEASIBLE? (Y/N):N  
Outstanding move!!!  
  
  
#### NEW PROBLEM ####  
q : 66347  
p : 12611  
##### PRODUCE THE FOLLOWING ####  
totient(n)  
IS THIS POSSIBLE and FEASIBLE? (Y/N):Y  
#### TIME TO SHOW ME WHAT YOU GOT! ###  
totient(n): 836623060  
Outstanding move!!!  
  
  
#### NEW PROBLEM ####  
plaintext : 635729417148931154719098761554457513358196788649948409135266140641404  
444047520534288284123635766597343146249135508941371039227338020303879324156430477  
4271529108729717  
e : 3  
n : 29129463609326322559521123136222078780585451208149138547799121083622333250646  
678767769126248182207478527881025116332742616201890576280859777513414460842754045  
651093593251726785499360828237897586278068419875517543013545369871704159718105354  
690802726645710699029936754265654381929650494383622583174075805797766685192325859  
982797796060391271817578087472948205626257717479858369754502615173773514087437504  
532994142632207906501079835037052797306690891600559321673928943158514646572885986  
881016569647357891598545880304236145548059520898133142087545369179876065657214225  
826997676844000054327141666320553082128424707948750331  
##### PRODUCE THE FOLLOWING ####  
ciphertext  
IS THIS POSSIBLE and FEASIBLE? (Y/N):Y  
#### TIME TO SHOW ME WHAT YOU GOT! ###  
ciphertext: 256931246631782714357241556582441991993437399854161372646318659020994  
329843524306570818293602492485385337029697819837182169818816821461486018802894936  
801257629375428544752970630870631166355711254848465862207765051226282541748174535  
990314552471546936536330397892907207943448897073772015986097770443616540466471245  
438117157152783246654401668267323136450122287983612851171545784168132230208726238  
881861407976917850248110805724300421712827401063963117423718797887144760360749619  
552577176382615108244813  
Outstanding move!!!  
  
  
#### NEW PROBLEM ####  
ciphertext : 10752401345107934853994451075614360420392571726218503379932844501179  
276054552894499371978339254216342863717232351225262456711111066616866474311520379  
151098570994236660962643699588778167465127223356630381497967750710116858773937569  
9009734588985482369702634499544891509228440194615376339573685285125730286623323  
e : 3  
n : 27566996291508213932419371385141522859343226560050921196294761870500846140132  
385080994630946107675330189606021165260590147068785820203600882092467797813519434  
652632126061353583124063944373336654246386074125394368479677295167494332556053947  
231141336142392086767742035970752738056297057898704112912616565299451359791548536  
846025854378347423520104947907334451056339439706623069503088916316369813499705073  
573777577169392401411708920615574908593784282546154486446779246790294398198854547  
069593987224578333683144886242572837465834139561122101527973799583927411936200068  
176539747586449939559180772690007261562703222558103359  
##### PRODUCE THE FOLLOWING ####  
plaintext  
IS THIS POSSIBLE and FEASIBLE? (Y/N):N  
Outstanding move!!!  
  
  
#### NEW PROBLEM ####  
q : 92092076805892533739724722602668675840671093008520241548191914215399824020372  
076186460768206814914423802230398410980218741906960527104568970225804374404612617  
736579286959865287226538692911376507934256844456333236362669879347073756238894784  
951597211105734179388300051579994253565459304743059533646753003894559  
p : 97846775312392801037224396977012615848433199640105786119757047098757998273009  
741128821931277074555731813289423891389911801250326299324018557072727051765547115  
514791337578758859803890173153277252326496062476389498019821358465433398338364421  
624871010292162533041884897182597065662521825095949253625730631876637  
e : 65537  
##### PRODUCE THE FOLLOWING ####  
d  
IS THIS POSSIBLE and FEASIBLE? (Y/N):Y  
#### TIME TO SHOW ME WHAT YOU GOT! ###  
d: 140504626950320746914079154840363953312741641621421069497208507917178758046377  
682042596589817427287048601573951612578618282163700660074214068255232164550374328  
067083981907874909273011054988189127131739645015802168825398976714557872345825276  
946554550414213966347674747922592393319242140546441457478627296374165622394175008  
405122861157670860934678710108875906272438987416069300878333460590314252882455922  
351520397870796979508750667889400662829674307988624434946913183122575792684484355  
489763878614603686957265320473565084318672273273688891878937905405012220525316570  
5085538743651258400390580971043144644984654914856729  
Outstanding move!!!  
  
  
#### NEW PROBLEM ####  
p : 15314304227252786879841261241720443415693514687428299094238669402046286191806  
868456128176357703470660060838769914807101519472553339412606982685718242866042781  
827737872497755436591023152482725816090449377474874908847732820481217193598708871  
5261127321911849092207070653272176072509933245978935455542420691737433  
ciphertext : 15898528329836486259454280642537682745047492250031819804208947573732  
209296147142448425785475270839697919293976182333838349380319082449313123936042811  
917218253196274432195116911131311101664245124078266845291992250418272429673592762  
174381527121624558596357902629676671110003023710107905410987270486412752306303470  
410502366293287214002128769133995449197216690029130480234844827254205117539992852  
496638836353167147769854523276743309449394023887611024408163270210444112592577810  
624181267012402352918669635578760260278590557042623644240179185252741450067430771  
092134328724271261927055861090533852597204599189199436235384288  
e : 65537  
n : 23952937352643527451379227516428377705004894508566304313177880191662177061878  
993798938496818120987817049538365206671401938265663712351239785237507341311858383  
628932183083145614696585411921662992078376103990806989257289472590902167457302888  
198293135333083734504191910953238278860923153746261500759411620299864395158783509  
535039259714359526738924736952759753503357614939203434092075676169179112452620687  
731670534906069845965633455748606649062394293289967059348143206600765820021392608  
270528856238306849191113241355842396325210132358046616312901337987464473799040762  
271876389031455051640937681745409057246190498795697239  
##### PRODUCE THE FOLLOWING ####  
plaintext  
IS THIS POSSIBLE and FEASIBLE? (Y/N):Y  
#### TIME TO SHOW ME WHAT YOU GOT! ###  
plaintext: 1431166394270967486712220821490197065049678815123952097162341171297711  
9660454037678408741501  
Outstanding move!!!  
  
  
If you convert the last plaintext to a hex number, then ascii, you'll find what y  
ou need! ;)
```

Para el problema 5 se uso el siguiente codigo:
```python
plaintext = 6357294171489311547190987615544575133581967886499484091352661406414044440475205342882841236357665973431462491355089413710392273380203038793241564304774271529108729717
e = 3
n = 29129463609326322559521123136222078780585451208149138547799121083622333250646678767769126248182207478527881025116332742616201890576280859777513414460842754045651093593251726785499360828237897586278068419875517543013545369871704159718105354690802726645710699029936754265654381929650494383622583174075805797766685192325859982797796060391271817578087472948205626257717479858369754502615173773514087437504532994142632207906501079835037052797306690891600559321673928943158514646572885986881016569647357891598545880304236145548059520898133142087545369179876065657214225826997676844000054327141666320553082128424707948750331

ciphertext = pow(plaintext, e, n)
print("Ciphertext:", ciphertext)

```

Para el problema 7 se uso:
```python
import sympy

p = 97846775312392801037224396977012615848433199640105786119757047098757998273009741128821931277074555731813289423891389911801250326299324018557072727051765547115514791337578758859803890173153277252326496062476389498019821358465433398338364421624871010292162533041884897182597065662521825095949253625730631876637
q = 92092076805892533739724722602668675840671093008520241548191914215399824020372076186460768206814914423802230398410980218741906960527104568970225804374404612617736579286959865287226538692911376507934256844456333236362669879347073756238894784951597211105734179388300051579994253565459304743059533646753003894559
e = 65537

# Calcular n
n = p * q

# Calcular phi(n)
phi_n = (p - 1) * (q - 1)

# Calcular d (inverso modular de e modulo phi(n))
d = sympy.mod_inverse(e, phi_n)

print("Private Key (d):", d)

```

Para el problema 8 se uso:
```python
Python 3.11.6 (main, Oct  8 2023, 05:06:43) [GCC 13.2.0] on linux  
Type "help", "copyright", "credits" or "license" for more information.  
>>> p = 1531430422725278687984126124172044341569351468742829909423866940204628619  
180686845612817635770347066006083876991480710151947255333941260698268571824286604  
278182773787249775543659102315248272581609044937747487490884773282048121719359870  
88715261127321911849092207070653272176072509933245978935455542420691737433  
>>> c = 1589852832983648625945428064253768274504749225003181980420894757373220929  
614714244842578547527083969791929397618233383834938031908244931312393604281191721  
825319627443219511691113131110166424512407826684529199225041827242967359276217438  
152712162455859635790262967667111000302371010790541098727048641275230630347041050  
236629328721400212876913399544919721669002913048023484482725420511753999285249663  
883635316714776985452327674330944939402388761102440816327021044411259257781062418  
126701240235291866963557876026027859055704262364424017918525274145006743077109213  
4328724271261927055861090533852597204599189199436235384288  
>>> e = 65537  
>>> n = 2395293735264352745137922751642837770500489450856630431317788019166217706  
187899379893849681812098781704953836520667140193826566371235123978523750734131185  
838362893218308314561469658541192166299207837610399080698925728947259090216745730  
288819829313533308373450419191095323827886092315374626150075941162029986439515878  
350953503925971435952673892473695275975350335761493920343409207567616917911245262  
068773167053490606984596563345574860664906239429328996705934814320660076582002139  
260827052885623830684919111324135584239632521013235804661631290133798746447379904  
0762271876389031455051640937681745409057246190498795697239  
>>> q = n // p  
>>> tn = (p-1)*(q-1)  
>>> d = inverse(e, tn)  
Traceback (most recent call last):  
 File "<stdin>", line 1, in <module>  
NameError: name 'inverse' is not defined. Did you mean: 'reversed'?  
>>> print(q)  
156408916769576372285319235535320446340733908943564048157238512311891352879208957  
302116527435165097143521156600690562005797819820759620198602417583539668686152735  
534648541252847927334505648478214810780526425005943955838623325525300844493280040  
860604499838598837599791480284496210333200247148213274376422459183  
>>> print(tn)  
239529373526435274513792275164283777050048945085663043131778801916621770618789937  
989384968181209878170495383652066714019382656637123512397852375073413118583836289  
321830831456146965854119216629920783761039908069892572894725909021674573028881982  
931353330837345041919109532382788609231537462615007594116202998640856068244674307  
981759825115742140442392837039356563185153139971017378608788915372490543296755318  
667907765255461270004347560612949086480248606922933798140926297529066478738010566  
912902078311128153979670546686412927769655299089190760697559921624858726290745808  
31718586702591072217415299182973577373701681500624  
>>> import sympy  
>>> d = sympy.mod_inverse(e, tn)  
>>> m = pow(c, d, n)  
>>> m  
143116639427096748671222082149019706504967881512395209716234117129771196604540376  
78408741501
```

Para descubiri el texto se uso el siguiente codigo:
```python
# Número dado
numero = 14311663942709674867122208214901970650496788151239520971623411712977119660454037678408741501

# Convertir a hexadecimal
hexadecimal = hex(numero)[2:]

# Convertir a texto ASCII
ascii_text = bytearray.fromhex(hexadecimal).decode()

print("Hexadecimal:", hexadecimal)
print("Texto ASCII:", ascii_text)

```

la bandera es:
```bash
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking/rsapopquiz]  
└─$ python plaintext.py    
Hexadecimal: 7069636f4354467b7741385f74683474245f696c6c336147616c2e2e6f32366365666362327d  
Texto ASCII: picoCTF{wA8_th4t$_ill3aGal..o26cefcb2}
```


## Notas adicionales


## Referencias
--https://www.youtube.com/watch?v=HIwgWauz-fc&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=40

--https://mregraoncyber.com/picoctf-writeup-rsa-pop-quiz/

--https://www.cs.drexel.edu/~popyack/IntroCS/HW/RSAWorksheet.html

--https://es.symbolab.com/