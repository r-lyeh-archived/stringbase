stringbase
==========

- **Stringbase** is a collaborative effort aimed to translate common texts found in videogames and regular apps.
- All github users can fork-and-pullreq freely and contribute to the project. All commits are welcome and merged.
- Any content in this repository is public domain and can be freely used in commercial and non-commercial software.

Sample
------

ID|TAGS|en|es
:--|:--|:--:|:--:
HELLO_WORLD||Hello world|Hola mundo

Data format
-----------

- ID and EN locale always match. ID is tokenized, though (no spaces, uppercase, ...)
- Tags are used to disambiguate ID contexts (ie, informal/courtesy, singular/plural, verb/noun, male/female/thing, animal/person...). Feel free to add them as needed.
- When no translation is found, a fallback translation can optionally used.
- Proposed fallback is searching for replacements from locality to globality
  - Ie, assuming our app is in es-AR mode, search for ID in es-AR table,
  - if not found, search for es-* string that matches best (see note below)
  - if not found, search for es string
  - if not found, search for en-* string that matches best (see note below) 
  - if not found, search for en string
  - if not found, detokenize ID and use it as string.

- Note: In case more than one result is found, select your policy carefully: 
  - like, pick up the second most spoken language in current locale
  - or,   pick up the locale matches the most (by physical proximity, by cultural legacy, by historical reasons...)
  - etc...

- There is a proposed fallback order tree at the bottom of this file.

A few more samples:

ID|TAGS|en|es
:--|:--|:--:|:--: 
HELLO_WORLD||Hello world|Hola mundo

ID|TAGS|en|es
:--|:--|:--:|:--:
I_AM_GERMAN||I am german|Soy alemán

ID|TAGS|de
---|:--|:--:
I_AM_GERMAN|MALE|Ich bin Deutscher 
I_AM_GERMAN|FEMALE|Ich bin Deutsche.

ID|TAGS|en-GB 
:--|:--|:--:
NEIGHBORHOOD_HAS_NO_COLOR||Neighbourhood has no color

ID|TAGS|es|es-ES|es-AR 
:--|:--|:--:|:--:|:--: 
TWO_BLOCKS_AWAY_FROM_HERE|DISTANCE|A dos bloques de aquí|A dos manzanas de aquí|A dos cuadras de aquí 

External links and alternatives
-------------------------------

- https://github.com/xlevus/r-gamedev-polygot/network
- http://polyglot.wikia.com/wiki/Polyglot_Wiki
- https://docs.google.com/spreadsheet/ccc?key=0AljNkWIESSQodGdUWWpuajdQUWZ4eTBmeTd6eEYwM2c&usp=sharing#gid=2
- https://docs.google.com/spreadsheet/ccc?key=0Al1cNCkGdEJfdF8xX0dsaHl6ZVpzMDF2OW9JaWVWMVE&usp=drive_web#gid=0

Locale map
----------

```
Afrikaans,af,af
Albanian,sq,sq
Amharic,am,am
Arabic - Algeria,ar,ar-dz
Arabic - Bahrain,ar,ar-bh
Arabic - Egypt,ar,ar-eg
Arabic - Iraq,ar,ar-iq
Arabic - Jordan,ar,ar-jo
Arabic - Kuwait,ar,ar-kw
Arabic - Lebanon,ar,ar-lb
Arabic - Libya,ar,ar-ly
Arabic - Morocco,ar,ar-ma
Arabic - Oman,ar,ar-om
Arabic - Qatar,ar,ar-qa
Arabic - Saudi,Arabia,ar,ar-sa
Arabic - Syria,ar,ar-sy
Arabic - Tunisia,ar,ar-tn
Arabic - United,Arab,Emirates,ar,ar-ae
Arabic - Yemen,ar,ar-ye
Armenian,hy,hy
Assamese,as,as
Azeri - Cyrillic,az,az-az
Azeri - Latin,az,az-az
Basque,eu,eu
Belarusian,be,be
Bengali - Bangladesh,bn,bn
Bengali - India,bn,bn
Bosnian,bs,bs
Bulgarian,bg,bg
Burmese,my,my
Catalan,ca,ca
Chinese - China,zh,zh-cn
Chinese - Hong,Kong,SAR,zh,zh-hk
Chinese - Macau,SAR,zh,zh-mo
Chinese - Singapore,zh,zh-sg
Chinese - Taiwan,zh,zh-tw
Croatian,hr,hr
Czech,cs,cs
Danish,da,da
Divehi/Dhivehi/Maldivian,dv,dv
Dutch - Belgium,nl,nl-be
Dutch - Netherlands,nl,nl-nl
English - Australia,en,en-au
English - Belize,en,en-bz
English - Canada,en,en-ca
English - Caribbean,en,en-cb
English - Great,Britain,en,en-gb
English - India,en,en-in
English - Ireland,en,en-ie
English - Jamaica,en,en-jm
English - New,Zealand,en,en-nz
English - Phillippines,en,en-ph
English - Southern,Africa,en,en-za
English - Trinidad,en,en-tt
English - United,States,en,en-us
English - Zimbabwe,en
Estonian,et,et
Faroese,fo,fo
Farsi - Persian,fa,fa
Finnish,fi,fi
French - Belgium,fr,fr-be
French - Cameroon,fr
French - Canada,fr,fr-ca
French - Congo,fr
French - Cote,d'Ivoire,fr
French - France,fr,fr-fr
French - Luxembourg,fr,fr-lu
French - Mali,fr
French - Monaco,fr
French - Morocco,fr
French - Senegal,fr
French - Switzerland,fr,fr-ch
French - West,Indies,fr
FYRO,Macedonia,mk,mk
Gaelic - Ireland,gd,gd-ie
Gaelic - Scotland,gd,gd
Galician,gl
Georgian,ka
German - Austria,de,de-at
German - Germany,de,de-de
German - Liechtenstein,de,de-li
German - Luxembourg,de,de-lu
German - Switzerland,de,de-ch
Greek,el,el
Guarani - Paraguay,gn,gn
Gujarati,gu,gu
Hebrew,he,he
Hindi,hi,hi
Hungarian,hu,hu
Icelandic,is,is
Indonesian,id,id
Italian - Italy,it,it-it
Italian - Switzerland,it,it-ch
Japanese,ja,ja
Kannada,kn,kn
Kashmiri,ks,ks
Kazakh,kk,kk
Khmer,km,km
Korean,ko,ko
Lao,lo,lo
Latin,la,la
Latvian,lv,lv
Lithuanian,lt,lt
Malay - Brunei,ms,ms-bn
Malay - Malaysia,ms,ms-my
Malayalam,ml,ml
Maltese,mt,mt
Maori,mi,mi
Marathi,mr,mr
Mongolian,mn,mn
Mongolian,mn,mn
Nepali,ne,ne
Norwegian - Bokml,nb,no-no
Norwegian - Nynorsk,nn,no-no
Oriya,or,or
Polish,pl,pl
Portuguese - Brazil,pt,pt-br
Portuguese - Portugal,pt,pt-pt
Punjabi,pa,pa
Raeto-Romance,rm,rm
Romanian - Moldova,ro,ro-mo
Romanian - Romania,ro,ro
Russian,ru,ru
Russian - Moldova,ru,ru-mo
Sanskrit,sa,sa
Serbian - Cyrillic,sr,sr-sp
Serbian - Latin,sr,sr-sp
Setsuana,tn,tn
Sindhi,sd,sd
Sinhala;,Sinhalese,si,si
Slovak,sk,sk
Slovenian,sl,sl
Somali,so,so
Sorbian,sb,sb
Spanish - Argentina,es,es-ar
Spanish - Bolivia,es,es-bo
Spanish - Chile,es,es-cl
Spanish - Colombia,es,es-co
Spanish - Costa,Rica,es,es-cr
Spanish - Dominican,Republic,es,es-do
Spanish - Ecuador,es,es-ec
Spanish - El,Salvador,es,es-sv
Spanish - Guatemala,es,es-gt
Spanish - Honduras,es,es-hn
Spanish - Mexico,es,es-mx
Spanish - Nicaragua,es,es-ni
Spanish - Panama,es,es-pa
Spanish - Paraguay,es,es-py
Spanish - Peru,es,es-pe
Spanish - Puerto,Rico,es,es-pr
Spanish - Spain,(Traditional),es,es-es
Spanish - Uruguay,es,es-uy
Spanish - Venezuela,es,es-ve
Swahili,sw,sw
Swedish - Finland,sv,sv-fi
Swedish - Sweden,sv,sv-se
Tajik,tg,tg
Tamil,ta,ta
Tatar,tt,tt
Telugu,te,te
Thai,th,th
Tibetan,bo,bo
Tsonga,ts,ts
Turkish,tr,tr
Turkmen,tk,tk
Ukrainian,uk,uk
Urdu,ur,ur
Uzbek - Cyrillic,uz,uz-uz
Uzbek - Latin,uz,uz-uz
Vietnamese,vi,vi
Welsh,cy,cy
Xhosa,xh,xh
Yiddish,yi,yi
Zulu,zu,zu
```
