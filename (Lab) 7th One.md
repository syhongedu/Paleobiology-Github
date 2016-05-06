## Problem Set 1

> 16/20

1) max_ma means return only records whose temporal locality is at most this old and min_ma means return only records whose temporal locality is at least this old.

2) 

> You didn't need to print all the data!

````R
sort(tapply(DataPBDB[,"max_ma"],DataPBDB[,"genus"],max))
        Curvemysella             Galeomma              Oxyloma 
              0.0117               0.0117               0.0117 
         Perumytilus            Altenaeum            Asperarca 
              0.0117               0.1260               0.1260 
           Atactodea             Capsella           Cavatidens 
              0.1260               0.1260               0.1260 
               Comus            Ensiculus              Erodona 
              0.1260               0.1260               0.1260 
             Exotica            Foveadens           Glycydonta 
              0.1260               0.1260               0.1260 
           Kikaiarca            Laevigyra           Lamychaena 
              0.1260               0.1260               0.1260 
            Leptomya           Microcirce            Musculium 
              0.1260               0.1260               0.1260 
             Mytella           Paphonotia        Pascahinnites 
              0.1260               0.1260               0.1260 
       Pinguitellina            Redicirce             Regozara 
              0.1260               0.1260               0.1260 
           Scintilla           Scissulina          Semimytilus 
              0.1260               0.1260               0.1260 
          Semipecten          Thraciopsis           Diplothyra 
              0.1260               0.1260               0.7810 
           Goethemia         Lituyapecten            Noetiella 
              0.7810               0.7810               0.7810 
        Parahyotissa          Quidnipagus       Spiniplicatula 
              0.7810               0.7810               1.8060 
          Bernardina            Brechites               Darina 
              2.5880               2.5880               2.5880 
         Emiliodonta              Fabella           Fungiacava 
              2.5880               2.5880               2.5880 
         Heterodonax             Irusella            Kurtiella 
              2.5880               2.5880               2.5880 
          Marikellia             Milneria           Musculista 
              2.5880               2.5880               2.5880 
           Philobrya           Planostrea           Protothaca 
              2.5880               2.5880               2.5880 
          Psammacola          Psammotella        Psammotellina 
              2.5880               2.5880               2.5880 
         Rochefortia            Talabrica           Taxocardia 
              2.5880               2.5880               2.5880 
            Turtonia            Venatomya          Volachlamys 
              2.5880               2.5880               2.5880 
           Wallucina        Alectryonella           Cooperella 
              2.5880               3.6000               3.6000 
       Coralichlamys       Crassatellites              Cyamium 
              3.6000               3.6000               3.6000 
         Ensitellops              Eulopia           Halonympha 
              3.6000               3.6000               3.6000 
           Hemidonax             Hippagus            Humilaria 
              3.6000               3.6000               3.6000 
           Ischadium          Juxtamusium         Lissochlamys 
              3.6000               3.6000               3.6000 
          Melliteryx             Myochama            Neaeromya 
              3.6000               3.6000               3.6000 
           Nutricola             Ovalarca           Pliocardia 
              3.6000               3.6000               3.6000 
   Pseudogrammatodon           Pythinella          Serratovola 
              3.6000               3.6000               3.6000 
        Stralopecten               Theora             Tindaria 
              3.6000               3.6000               3.6000 
          Trigonella           Agerostrea          Barytellina 
              3.6000               5.3330               5.3330 
         Bulacanites             Cardinia         Choromytilus 
              5.3330               5.3330               5.3330 
      Clathrotellina        Costokidderia          Cyclomactra 
              5.3330               5.3330               5.3330 
          Cyprimeria               Dilora            Donacilla 
              5.3330               5.3330               5.3330 
           Elongaria             Ervillia       Excellichlamys 
              5.3330               5.3330               5.3330 
            Fugleria            Glibertia               Haumea 
              5.3330               5.3330               5.3330 
           Hemimetis           Iliochione         Laevichlamys 
              5.3330               5.3330               5.3330 
             Laseina           Leptaxinus             Lioberus 
              5.3330               5.3330               5.3330 
           Lirotarte          Lissopecten            Luciploma 
              5.3330               5.3330               5.3330 
             Macalia         Maoricardium           Modiolatus 
              5.3330               5.3330               5.3330 
           Neolepton            Notolimea          Notospisula 
              5.3330               5.3330               5.3330 
            Panacoma              Paphies                Patro 
              5.3330               5.3330               5.3330 
          Perrierina         Phialopecten         Planicardium 
              5.3330               5.3330               5.3330 
           Porterius         Qiongzhounia             Quadrans 
              5.3330               5.3330               5.3330 
        Rhomboidella            Ruditapes          Scissodesma 
              5.3330               5.3330               5.3330 
           Serratina        Strophocardia             Tellimya 
              5.3330               5.3330               5.3330 
          Tellinides         Tindariopsis             Ungulina 
              5.3330               5.3330               5.3330 
          Yabepecten         Zamorapecten        Austrochlamys 
              5.3330               5.3330               7.2460 
          Eupatorina          Lajonkairia        Panamicorbula 
              7.2460               7.2460               7.2460 
          Parvidacna           Pontalmyra        Prosodacnomya 
              7.2460               7.2460               7.2460 
      Pseudocatillus              Aloides             Anapella 
              7.2460              11.6080              11.6080 
        Arcopaginula          Austrovenus            Callonaia 
             11.6080              11.6080              11.6080 
        Chagrepecten            Chioneryx          Clidiophora 
             11.6080              11.6080              11.6080 
         Ctenocardia              Didacna           Divalucina 
             11.6080              11.6080              11.6080 
         Equichlamys             Hippopus           Humphreyia 
             11.6080              11.6080              11.6080 
          Litigiella           Melaxinaea            Minnivola 
             11.6080              11.6080              11.6080 
          Mycetopoda              Myllita            Paradacna 
             11.6080              11.6080              11.6080 
          Penicillus        Pseudamiantis      Pseudoarcopagia 
             11.6080              11.6080              11.6080 
             Pythina              Resania        Scrobicularia 
             11.6080              11.6080              11.6080 
       Scutarcopagia         Tellinidella               Tresus 
             11.6080              11.6080              11.6080 
            Acorylus           Adamussium          Afrocardium 
             11.6200              11.6200              11.6200 
        Carinastarte            Chionista          Choristodon 
             11.6200              11.6200              11.6200 
            Coelopis            Cymatoica           Lucinopsis 
             11.6200              11.6200              11.6200 
         Semierycina        Spathochlamys             Turneria 
             11.6200              11.6200              11.6200 
       Sarmatimactra              Zealeda               Eontia 
             12.7000              12.7000              13.8200 
            Ostreola         Plicatiforma          Radiolucina 
             13.8200              13.8200              13.8200 
          Rupellaria          Acturellina            Adipicola 
             13.8200              15.9700              15.9700 
         Anodontites          Anticorbula              Asaphis 
             15.9700              15.9700              15.9700 
             Chaceia           Clementina     Concentricavalva 
             15.9700              15.9700              15.9700 
        Conradostrea             Corculum         Cryptomactra 
             15.9700              15.9700              15.9700 
        Cryptopecten          Cyclodicama           Deltachion 
             15.9700              15.9700              15.9700 
          Diarmaidia       Dichotochlamys               Eupera 
             15.9700              15.9700              15.9700 
            Fabulina             Isomonia            Lioconcha 
             15.9700              15.9700              15.9700 
       Lunulicardium         Lymnocardium           Mactrinula 
             15.9700              15.9700              15.9700 
         Mactrodesma           Mytilaster         Nanaochlamys 
             15.9700              15.9700              15.9700 
        Neocorbicula          Neotrigonia        Obsoletiforma 
             15.9700              15.9700              15.9700 
             Ostomya         Pachyrotunda              Paramya 
             15.9700              15.9700              15.9700 
           Pillucina        Potamocorbula          Properycina 
             15.9700              15.9700              15.9700 
      Scalaricardita            Siratoria           Solecardia 
             15.9700              15.9700              15.9700 
       Solidicorbula         Veprichlamys             Aupouria 
             15.9700              15.9700              19.0000 
           Bartrumia        Cleidothaerus            Trichomya 
             19.0000              19.0000              19.0000 
          Virmysella           Armimiltha             Cardilia 
             19.0000              20.4400              20.4400 
        Cardiolucina      Costaglycymeris       Cristatopecten 
             20.4400              20.4400              20.4400 
        Decatopecten           Erycinella               Fulvia 
             20.4400              20.4400              20.4400 
          Hemimactra        Hysteroconcha         Kotorapecten 
             20.4400              20.4400              20.4400 
          Lepilucina           Mactrotoma             Moerella 
             20.4400              20.4400              20.4400 
        Mytiloconcha     Oppenheimopecten          Rudicardium 
             20.4400              20.4400              20.4400 
            Scacchia                Taras           Trinitasia 
             20.4400              20.4400              20.4400 
            Hinnites            Offadesma                Rohea 
             21.7000              21.7000              21.7000 
         Abrachlamys         Acrosterigma              Aligena 
             23.0300              23.0300              23.0300 
             Anatina          Annachlamys             Axinulus 
             23.0300              23.0300              23.0300 
             Bassina            Bentharca            Bucardium 
             23.0300              23.0300              23.0300 
         Carditopsis        Caribachlamys       Carolinapecten 
             23.0300              23.0300              23.0300 
        Chesacardium          Chesapecten         Circomphalus 
             23.0300              23.0300              23.0300 
        Crassicardia             Dallarca        Exallocorbula 
             23.0300              23.0300              23.0300 
         Ezocallista          Flexopecten           Florimetis 
             23.0300              23.0300              23.0300 
         Frigichione             Harvella          Hexacorbula 
             23.0300              23.0300              23.0300 
             Hiatula            Iphigenia                 Irus 
             23.0300              23.0300              23.0300 
          Korobkovia             Lasaeina                 Leda 
             23.0300              23.0300              23.0300 
        Lepidopecten          Leptomactra          Leptopecten 
             23.0300              23.0300              23.0300 
          Liromissus         Lunulicardia        Lunulicardita 
             23.0300              23.0300              23.0300 
             Malleus     Marvacrassatella              Melosia 
             23.0300              23.0300              23.0300 
            Milthona           Mioerycina           Mirapecten 
             23.0300              23.0300              23.0300 
        Mizuhopecten              Modiola         Modiomytilus 
             23.0300              23.0300              23.0300 
       Neopycnodonta        Nipponomarcia              Notirus 
             23.0300              23.0300              23.0300 
         Paleomarcia              Panomya         Patinopecten 
             23.0300              23.0300              23.0300 
           Penitella              Placuna          Planikellia 
             23.0300              23.0300              23.0300 
           Platyodon          Pleurodesma              Pristes 
             23.0300              23.0300              23.0300 
        Pseudolepton           Pteromeris             Scambula 
             23.0300              23.0300              23.0300 
         Semicorbula              Senilia          Sheldonella 
             23.0300              23.0300              23.0300 
         Somalidacna            Tellidora           Temblornia 
             23.0300              23.0300              23.0300 
            Timoclea             Tridacna          Zenatiopsis 
             23.0300              23.0300              23.0300 
             Zirfaea           Dendostrea            Digitaria 
             23.0300              28.1000              28.1000 
           Goodallia            Laciolina          Lindapecten 
             28.1000              28.1000              28.1000 
           Lucinella           Omanidacna         Placunanomia 
             28.1000              28.1000              28.1000 
          Pygocardia       Spaniodontella        Anomalocardia 
             28.1000              28.1000              28.4000 
      Austrohinnites             Congeria           Cyclinella 
             28.4000              28.4000              28.4000 
       Dimarzipecten         Gloripallium       Iheringinucula 
             28.4000              28.4000              28.4000 
          Janupecten               Lasaea              Leukoma 
             28.4000              28.4000              28.4000 
        Macrochlamis         Mancosinodia           Mercenaria 
             28.4000              28.4000              28.4000 
             Merisca           Modiolarca           Nodipecten 
             28.4000              28.4000              28.4000 
         Notochlamys         Paramusculus         Phragmorisma 
             28.4000              28.4000              28.4000 
            Pisidium           Pleiorytis        Pleurophopsis 
             28.4000              28.4000              28.4000 
         Proxichione           Retrotapes          Sectipecten 
             28.4000              28.4000              28.4000 
        Semelangulus            Stewartia          Ainicardita 
             28.4000              28.4000              33.9000 
       Amussiopecten        Antillipecten       Austrocallista 
             33.9000              33.9000              33.9000 
         Brevinucula             Chamelea           Chionopsis 
             33.9000              33.9000              33.9000 
                Cosa Costellamussiopecten           Crassadoma 
             33.9000              33.9000              33.9000 
               Ctena           Cyrenorita           Eotrigonia 
             33.9000              33.9000              33.9000 
          Felaniella          Fortipecten        Gigantopecten 
             33.9000              33.9000              33.9000 
          Globivenus                 Idas          Indoplacuna 
             33.9000              33.9000              33.9000 
           Leopecten              Liocyma           Lyropecten 
             33.9000              33.9000              33.9000 
          Manupecten            Megaxinus             Myadesma 
             33.9000              33.9000              33.9000 
             Myadora        Neoinoceramus       Papillicardium 
             33.9000              33.9000              33.9000 
       Paralucinella      Patagonicardium           Periglypta 
             33.9000              33.9000              33.9000 
           Plectodon           Pododesmus            Propeleda 
             33.9000              33.9000              33.9000 
          Psamosolen             Semelina             Serripes 
             33.9000              33.9000              33.9000 
        Similipecten              Solamen              Sunetta 
             33.9000              33.9000              33.9000 
        Tellidorella                 Tiza             Trisidos 
             33.9000              33.9000              33.9000 
         Vertipecten              Zenatia             Chaperia 
             33.9000              33.9000              34.3000 
           Agriopoma          Anisocardia             Antigona 
             37.2000              37.2000              37.2000 
      Austrotindaria          Avicularium            Axinactis 
             37.2000              37.2000              37.2000 
       Chrysocardium           Compsomyax          Condylocuna 
             37.2000              37.2000              37.2000 
        Cryptolucina          Dallocardia             Darcinia 
             37.2000              37.2000              37.2000 
            Ennucula           Eopapyrina           Epicodakia 
             37.2000              37.2000              37.2000 
           Gemellima          Isocrassina            Katelysia 
             37.2000              37.2000              37.2000 
                Kuia            Lirophora             Lissarca 
             37.2000              37.2000              37.2000 
            Lutraria         Microcardium         Notolimopsis 
             37.2000              37.2000              37.2000 
           Notostrea            Ovamactra               Paphia 
             37.2000              37.2000              37.2000 
          Parastarte             Placamen            Platygena 
             37.2000              37.2000              37.2000 
               Raeta        Rebeccapecten            Sawkinsia 
             37.2000              37.2000              37.2000 
         Semipallium         Spinosipella            Strigilla 
             37.2000              37.2000              37.2000 
             Tagelus       Trichomusculus              Venidia 
             37.2000              37.2000              37.2000 
              Woodia             Amiantis           Aperiploma 
             37.2000              38.0000              38.0000 
             Beguina            Calloarca               Euloxa 
             38.0000              38.0000              38.0000 
          Exosiperna            Geukensia          Hemicardium 
             38.0000              38.0000              38.0000 
            Hilberia              Ledella              Limarca 
             38.0000              38.0000              38.0000 
         Psammotreta           Simomactra          Spheniopsis 
             38.0000              38.0000              38.0000 
      Trigoniocardia            Venerupis        Victoripecten 
             38.0000              38.0000              38.0000 
           Wakullina             Amotapas           Arginopsis 
             38.0000              41.3000              41.3000 
             Boeuvia              Bruetia            Chattonia 
             41.3000              41.3000              41.3000 
       Condylocardia             Cumingia         Cuspicorbula 
             41.3000              41.3000              41.3000 
        Cytheriopsis          Dinocardium          Duplipecten 
             41.3000              41.3000              41.3000 
               Ensis              Gouldia          Grateloupia 
             41.3000              41.3000              41.3000 
        Juliacorbula               Kellia          Kokanostrea 
             41.3000              41.3000              41.3000 
         Longimactra             Macomona         Margaritaria 
             41.3000              41.3000              41.3000 
            Mauricia           Micromeris              Mulinia 
             41.3000              41.3000              41.3000 
          Nevenulora            Palliolum         Parmicorbula 
             41.3000              41.3000              41.3000 
          Pecchiolia          Pectinucula          Placopecten 
             41.3000              41.3000              41.3000 
          Polidevcia             Poroleda           Psammacoma 
             41.3000              41.3000              41.3000 
       Pseudamussium          Pseudochama           Recurvella 
             41.3000              41.3000              41.3000 
          Salaputium               Tawera           Textivenus 
             41.3000              41.3000              41.3000 
          Trigonarca          Trigonulina              Volupia 
             41.3000              41.3000              41.3000 
          Xenoloupia            Xylophaga               Marama 
             41.3000              41.3000              43.0000 
    Pseudoportlandia                Adula          Americardia 
             43.0000              47.8000              47.8000 
           Batequeus           Cavilucina          Crassinella 
             47.8000              47.8000              47.8000 
           Cryptomya              Cyclina                Gemma 
             47.8000              47.8000              47.8000 
          Glycimeris              Homomya      Hubertschenckia 
             47.8000              47.8000              47.8000 
            Huxleyia          Laubriereia           Mercimonia 
             47.8000              47.8000              47.8000 
             Meroena                Metis         Nicaisolopha 
             47.8000              47.8000              47.8000 
          Noetiopsis            Nucunella              Pandora 
             47.8000              47.8000              47.8000 
           Papyridea             Pinctada              Poromya 
             47.8000              47.8000              47.8000 
            Psathura               Rangia        Rhabdopitaria 
             47.8000              47.8000              47.8000 
        Ringicardium           Saccostrea         Scalpomactra 
             47.8000              47.8000              47.8000 
         Soletellina          Superlucina                Turia 
             47.8000              47.8000              47.8000 
           Ursirivus                Venus              Acharax 
             47.8000              47.8000              48.6000 
            Anodonta           Apolymetis            Arcinella 
             48.6000              48.6000              48.6000 
           Arginella           Argopecten               Artena 
             48.6000              48.6000              48.6000 
        Aspidopholas              Avicula             Azorinus 
             48.6000              48.6000              48.6000 
         Calyptogena          Carditamera             Cardites 
             48.6000              48.6000              48.6000 
         Clausinella         Crepispisula          Eufistulana 
             48.6000              48.6000              48.6000 
            Euphenax               Euvola             Exputens 
             48.6000              48.6000              48.6000 
       Ficusocorbula             Gastrana            Halonanus 
             48.6000              48.6000              48.6000 
            Hiatella         Joannisiella           Macrosolen 
             48.6000              48.6000              48.6000 
         Mactrellona               Marcia           Mytilopsis 
             48.6000              48.6000              48.6000 
       Neaeroporomya          Nitidavenus      Notogrammatodon 
             48.6000              48.6000              48.6000 
          Nuculoidea           Parapholas            Parinomya 
             48.6000              48.6000              48.6000 
               Perna               Phaxas     Pseudocuspidaria 
             48.6000              48.6000              48.6000 
         Pteropsella               Rakhia            Scapharca 
             48.6000              48.6000              48.6000 
         Temnoconcha             Tucetona              Tugonia 
             48.6000              48.6000              48.6000 
         Undulostrea            Venerella            Veremolpa 
             48.6000              48.6000              48.6000 
           Vesicomya             Amotapus            Amygdalum 
             48.6000              55.8000              55.8000 
      Ciliatocardium          Clavipholas            Clementia 
             55.8000              55.8000              55.8000 
          Conchocele         Cossmannella            Cultellus 
             55.8000              55.8000              55.8000 
                Cuna          Cycladicama          Cyclopecten 
             55.8000              55.8000              55.8000 
      Elliptotellina          Heteranomia         Jorgechlamys 
             55.8000              55.8000              55.8000 
        Laevicardium        Lamelliconcha          Lentipecten 
             55.8000              55.8000              55.8000 
          Mactropsis          Megacardita           Mesopeplum 
             55.8000              55.8000              55.8000 
        Mesosaccella            Nausitora            Paraglans 
             55.8000              55.8000              55.8000 
        Quadrilatera           Semeloidea            Sokolowia 
             55.8000              55.8000              55.8000 
          Solecurtus            Tivellina                 Abra 
             55.8000              55.8000              56.0000 
         Aequipecten            Africarca             Alveinus 
             56.0000              56.0000              56.0000 
             Amusium            Anapteris           Anisodonta 
             56.0000              56.0000              56.0000 
  Australoportlandia           Axinopsida               Bankia 
             56.0000              56.0000              56.0000 
              Barnea           Blagraveia           Callithaca 
             56.0000              56.0000              56.0000 
         Callocardia         Cardiniopsis        Cardiocardita 
             56.0000              56.0000              56.0000 
            Castalia         Clinocardium          Cochlodesma 
             56.0000              56.0000              56.0000 
          Cockburnia           Corbulomya          Cyclocardia 
             56.0000              56.0000              56.0000 
        Cyclochlamys             Diplodon              Discors 
             56.0000              56.0000              56.0000 
           Divalinga            Dreissena             Egerella 
             56.0000              56.0000              56.0000 
           Eophysema             Eumarcia           Eurhomalea 
             56.0000              56.0000              56.0000 
         Eurytellina               Fragum            Gaimardia 
             56.0000              56.0000              56.0000 
        Gigantostrea             Gomphina          Hadralucina 
             56.0000              56.0000              56.0000 
             Haliris             Hyotissa            Kellyella 
             56.0000              56.0000              56.0000 
              Lepton                Linga            Mesodesma 
             56.0000              56.0000              56.0000 
          Modiolaria                  Mya         Mytilosootus 
             56.0000              56.0000              56.0000 
            Nayadina               Noetia           Nymphactra 
             56.0000              56.0000              56.0000 
        Orthocardium             Oxyperas             Pachecoa 
             56.0000              56.0000              56.0000 
            Pachydon         Parathyasira            Pelecyora 
             56.0000              56.0000              56.0000 
        Petalocardia             Physoida            Plagiarca 
             56.0000              56.0000              56.0000 
           Potamomya          Protonoetia          Pterolucina 
             56.0000              56.0000              56.0000 
            Raetomya            Saxidomus         Schedocardia 
             56.0000              56.0000              56.0000 
             Sinodia          Sinodiopsis                 Sita 
             56.0000              56.0000              56.0000 
           Standella           Stirpulina          Tenuimactra 
             56.0000              56.0000              56.0000 
              Tivela         Trigonodesma         Vepricardium 
             56.0000              56.0000              56.0000 
         Zygochlamys           Acuticosta         Cerastoderma 
             56.0000              58.7000              58.7000 
           Cuneopsis           Eomeretrix           Lamprotula 
             58.7000              58.7000              58.7000 
        Austronucula           Basterotia          Bathytormus 
             59.2000              59.2000              59.2000 
              Chione         Claibornites           Comitileda 
             59.2000              59.2000              59.2000 
               Donax        Eburneopecten              Ervilia 
             59.2000              59.2000              59.2000 
         Ilymatogyra                Limea            Montacuta 
             59.2000              59.2000              59.2000 
             Mysella            Oryctomya           Periplomya 
             59.2000              59.2000              59.2000 
           Petricola              Pitaria         Pseudomiltha 
             59.2000              59.2000              59.2000 
       Sanguinolaria          Saxicavella               Solyma 
             59.2000              59.2000              59.2000 
               Tenea             Volsella                Aeora 
             59.2000              59.2000              61.6000 
           Anodontia            Aulacomya           Carditella 
             61.6000              61.6000              61.6000 
               Circe          Divaricella          Hedecardium 
             61.6000              61.6000              61.6000 
            Kitsonia            Laternula           Litorhadia 
             61.6000              61.6000              61.6000 
             Lyonsia         Miodontiscus         Notocallista 
             61.6000              61.6000              61.6000 
           Notodonax            Nucinella          Parvicorbis 
             61.6000              61.6000              61.6000 
           Pullastra              Sarepta          Serripecten 
             61.6000              61.6000              61.6000 
        Sootryenella             Tivelina         Transennella 
             61.6000              61.6000              61.6000 
           Trapezium             Vulsella               Adrana 
             61.6000              61.6000              61.7000 
              Mactra               Pholas             Vokesula 
             61.7000              61.7000              61.7000 
       Acanthocardia                 Acar               Acesta 
             66.0000              66.0000              66.0000 
               Acila          Actinodonta           Acutostrea 
             66.0000              66.0000              66.0000 
         Adansonella          Ambigostrea              Anadara 
             66.0000              66.0000              66.0000 
     Anechinocardium              Angulus               Anomia 
             66.0000              66.0000              66.0000 
           Aphrodina                 Arca          Arcomytilus 
             66.0000              66.0000              66.0000 
           Arcopagia            Arcoperna             Arcopsis 
             66.0000              66.0000              66.0000 
             Arctica            Arcticlam            Arcuatula 
             66.0000              66.0000              66.0000 
             Astarte               Atreta               Atrina 
             66.0000              66.0000              66.0000 
       Australoneilo               Axinus        Baluchicardia 
             66.0000              66.0000              66.0000 
            Barbatia          Barbierella            Bathyarca 
             66.0000              66.0000              66.0000 
             Batissa            Bicorbula               Bornia 
             66.0000              66.0000              66.0000 
       Bothrocorbula               Botula         Brachidontes 
             66.0000              66.0000              66.0000 
       Brachiodontes        Caestocorbula             Callista 
             66.0000              66.0000              66.0000 
           Callucina        Callucinopsis           Calorhadia 
             66.0000              66.0000              66.0000 
        Camptonectes            Cardiomya              Cardita 
             66.0000              66.0000              66.0000 
             Cardium              Carolia         Caryocorbula 
             66.0000              66.0000              66.0000 
           Cavilinga                Chama              Chlamys 
             66.0000              66.0000              66.0000 
          Clavagella           Clisocolus              Codakia 
             66.0000              66.0000              66.0000 
       Coralliophaga            Corbicula              Corbula 
             66.0000              66.0000              66.0000 
        Corbulamella        Costacallista         Costelloleda 
             66.0000              66.0000              66.0000 
         Crassatella           Crassatina          Crassostrea 
             66.0000              66.0000              66.0000 
            Crenella            Ctenoides          Cubitostrea 
             66.0000              66.0000              66.0000 
           Cucullaea           Cucullaria         Cuneocorbula 
             66.0000              66.0000              66.0000 
          Cuspidaria         Cyclorismina           Cyrtodaria 
             66.0000              66.0000              66.0000 
         Cyrtopleura             Cytherea            Dacrydium 
             66.0000              66.0000              66.0000 
       Delectopecten             Dentonia       Dhondtichlamys 
             66.0000              66.0000              66.0000 
               Dimya           Diplodonta           Disparilia 
             66.0000              66.0000              66.0000 
        Divarikellia              Dosinia          Dosiniopsis 
             66.0000              66.0000              66.0000 
           Electroma            Epilucina             Eriphyla 
             66.0000              66.0000              66.0000 
        Eriphylopsis              Erycina                 Etea 
             66.0000              66.0000              66.0000 
             Euciroa        Eucrassatella              Exogyra 
             66.0000              66.0000              66.0000 
             Fimbria       Flabellipecten        Flemingostrea 
             66.0000              66.0000              66.0000 
           Fulcrella            Gafrarium                 Gari 
             66.0000              66.0000              66.0000 
        Gastrochaena            Gervillia          Gibbolucina 
             66.0000              66.0000              66.0000 
               Glans              Glossus           Glycymeris 
             66.0000              66.0000              66.0000 
         Glyptoactis           Gonimyrtea           Goossensia 
             66.0000              66.0000              66.0000 
         Grammatodon         Granocardium          Gregariella 
             66.0000              66.0000              66.0000 
            Gryphaea        Gryphaeostrea                 Here 
             66.0000              66.0000              66.0000 
           Hilgardia           Hindsiella       Integricardium 
             66.0000              66.0000              66.0000 
             Isoarca            Isognomon           Jagolucina 
             66.0000              66.0000              66.0000 
          Jouannetia            Jupiteria         Katherinella 
             66.0000              66.0000              66.0000 
           Kelliella             Kummelia               Kuphus 
             66.0000              66.0000              66.0000 
            Lahillia               Ledina            Lentidium 
             66.0000              66.0000              66.0000 
          Leptosolen                 Lima              Limaria 
             66.0000              66.0000              66.0000 
            Limatula             Limopsis             Liostrea 
             66.0000              66.0000              66.0000 
          Lirodiscus           Lithophaga              Loparia 
             66.0000              66.0000              66.0000 
               Lopha              Loripes          Loxocardium 
             66.0000              66.0000              66.0000 
              Lucina            Lucinisca             Lucinoma 
             66.0000              66.0000              66.0000 
              Macoma        Macrocallista          Mactromeris 
             66.0000              66.0000              66.0000 
            Malletia             Martesia            Marwickia 
             66.0000              66.0000              66.0000 
          Megayoldia           Meiocardia             Meretrix 
             66.0000              66.0000              66.0000 
          Mesomiltha               Miltha        Miocardiopsis 
             66.0000              66.0000              66.0000 
          Miodomeris          Mixtipecten             Modiolus 
             66.0000              66.0000              66.0000 
          Monitilora             Musculus               Myrtea 
             66.0000              66.0000              66.0000 
             Mytilon              Mytilus                Neilo 
             66.0000              66.0000              66.0000 
          Neilonella              Neithea          Nemocardium 
             66.0000              66.0000              66.0000 
             Nemodon           Nicaniella           Nototeredo 
             66.0000              66.0000              66.0000 
              Nucula             Nuculana             Nuculoma 
             66.0000              66.0000              66.0000 
           Nuttallia       Odontogryphaea          Orthoyoldia 
             66.0000              66.0000              66.0000 
              Ostrea              Oxytoma              Panopea 
             66.0000              66.0000              66.0000 
           Paranomia         Parvamussium         Parvicardium 
             66.0000              66.0000              66.0000 
         Parvilucina               Pecten            Periploma 
             66.0000              66.0000              66.0000 
           Phacoides          Phelopteria           Pholadidea 
             66.0000              66.0000              66.0000 
          Pholadomya          Pholadopsis                Pinna 
             66.0000              66.0000              66.0000 
               Pitar          Placunopsis        Plagiocardium 
             66.0000              66.0000              66.0000 
        Plastomiltha          Pleuromeris            Plicatula 
             66.0000              66.0000              66.0000 
          Polymesoda           Portlandia           Praerangia 
             66.0000              66.0000              66.0000 
       Propeamussium         Prophetilora          Protocardia 
             66.0000              66.0000              66.0000 
      Pseudaphrodina          Pseudolimea               Pteria 
             66.0000              66.0000              66.0000 
         Pteromyrtea           Pulvinites        Purpurocardia 
             66.0000              66.0000              66.0000 
          Pycnodonte           Recticardo       Rhabdotophorus 
             66.0000              66.0000              66.0000 
            Saccella           Saxolucina        Scrobiculabra 
             66.0000              66.0000              66.0000 
              Semele          Semimodiola             Septifer 
             66.0000              66.0000              66.0000 
             Siliqua              Solemya                Solen 
             66.0000              66.0000              66.0000 
              Solena          Spaniorinus            Sphaerium 
             66.0000              66.0000              66.0000 
             Sphenia             Spineilo          Spissatella 
             66.0000              66.0000              66.0000 
             Spisula            Spondylus            Sportella 
             66.0000              66.0000              66.0000 
            Striarca           Striostrea         Syncyclonema 
             66.0000              66.0000              66.0000 
         Talochlamys            Tancredia                Tapes 
             66.0000              66.0000              66.0000 
             Tellina          Tellinimera        Tellinocyclas 
             66.0000              66.0000              66.0000 
            Teredina               Teredo              Thracia 
             66.0000              66.0000              66.0000 
            Thyasira        Trachycardium             Trigonia 
             66.0000              66.0000              66.0000 
           Trinacria              Uddenia           Unicardium 
             66.0000              66.0000              66.0000 
                Unio         Venericardia             Veniella 
             66.0000              66.0000              66.0000 
         Verticordia      Vetericardiella               Yoldia 
             66.0000              66.0000              66.0000 
           Yoldiella 
             66.0000 
````     
             
3) 

````R
sort(tapply(DataPBDB[,"min_ma"],DataPBDB[,"genus"],max))
               Bernardina         Curvemysella            Foveadens 
              0.0000               0.0000               0.0000 
            Galeomma              Mytella              Oxyloma 
              0.0000               0.0000               0.0000 
         Perumytilus            Altenaeum            Atactodea 
              0.0000               0.0117               0.0117 
            Capsella           Cavatidens       Clathrotellina 
              0.0117               0.0117               0.0117 
               Comus            Ensiculus              Erodona 
              0.0117               0.0117               0.0117 
      Excellichlamys              Exotica           Fungiacava 
              0.0117               0.0117               0.0117 
          Glycydonta          Heterodonax             Irusella 
              0.0117               0.0117               0.0117 
           Kikaiarca            Laevigyra           Lamychaena 
              0.0117               0.0117               0.0117 
            Leptomya              Macalia           Marikellia 
              0.0117               0.0117               0.0117 
          Microcirce             Milneria            Musculium 
              0.0117               0.0117               0.0117 
         Notospisula           Paphonotia        Pascahinnites 
              0.0117               0.0117               0.0117 
       Pinguitellina           Planostrea           Protothaca 
              0.0117               0.0117               0.0117 
          Psammacola        Psammotellina          Quidnipagus 
              0.0117               0.0117               0.0117 
           Redicirce             Regozara            Scintilla 
              0.0117               0.0117               0.0117 
          Scissulina          Semimytilus           Semipecten 
              0.0117               0.0117               0.0117 
          Tellinides          Thraciopsis            Venatomya 
              0.0117               0.0117               0.0117 
         Volachlamys            Wallucina            Asperarca 
              0.0117               0.0117               0.0120 
            Turtonia           Diplothyra            Goethemia 
              0.0120               0.1260               0.1260 
        Lituyapecten            Noetiella         Parahyotissa 
              0.1260               0.1260               0.1260 
           Brechites               Darina            Kurtiella 
              0.7810               0.7810               0.7810 
          Musculista            Nutricola            Philobrya 
              0.7810               0.7810               0.7810 
         Psammotella          Rochefortia       Spiniplicatula 
              0.7810               0.7810               0.7810 
           Talabrica           Taxocardia          Emiliodonta 
              0.7810               0.7810               1.8060 
             Fabella        Alectryonella             Cardinia 
              1.8060               2.5880               2.5880 
          Cooperella        Coralichlamys        Costokidderia 
              2.5880               2.5880               2.5880 
      Crassatellites              Cyamium           Cyprimeria 
              2.5880               2.5880               2.5880 
           Elongaria          Ensitellops              Eulopia 
              2.5880               2.5880               2.5880 
          Halonympha               Haumea            Hemidonax 
              2.5880               2.5880               2.5880 
            Hippagus            Humilaria           Iliochione 
              2.5880               2.5880               2.5880 
           Ischadium          Juxtamusium         Laevichlamys 
              2.5880               2.5880               2.5880 
        Lissochlamys           Melliteryx             Myochama 
              2.5880               2.5880               2.5880 
           Neaeromya             Ovalarca             Panacoma 
              2.5880               2.5880               2.5880 
          Perrierina           Pliocardia            Porterius 
              2.5880               2.5880               2.5880 
   Pseudogrammatodon           Pythinella         Qiongzhounia 
              2.5880               2.5880               2.5880 
            Quadrans          Scissodesma          Serratovola 
              2.5880               2.5880               2.5880 
        Stralopecten               Theora             Tindaria 
              2.5880               2.5880               2.5880 
          Trigonella             Ungulina           Yabepecten 
              2.5880               2.5880               2.5880 
        Zamorapecten           Agerostrea          Barytellina 
              2.5880               3.6000               3.6000 
         Bulacanites         Choromytilus          Cyclomactra 
              3.6000               3.6000               3.6000 
              Dilora            Donacilla             Ervillia 
              3.6000               3.6000               3.6000 
            Fugleria            Glibertia            Hemimetis 
              3.6000               3.6000               3.6000 
             Laseina           Leptaxinus             Lioberus 
              3.6000               3.6000               3.6000 
           Lirotarte          Lissopecten            Luciploma 
              3.6000               3.6000               3.6000 
        Maoricardium           Modiolatus            Neolepton 
              3.6000               3.6000               3.6000 
           Notolimea              Paphies                Patro 
              3.6000               3.6000               3.6000 
        Phialopecten         Planicardium         Rhomboidella 
              3.6000               3.6000               3.6000 
           Ruditapes            Serratina        Strophocardia 
              3.6000               3.6000               3.6000 
            Tellimya         Tindariopsis               Tresus 
              3.6000               3.6000               3.6000 
             Aloides             Anapella          Anodontites 
              5.3330               5.3330               5.3330 
         Anticorbula         Arcopaginula        Austrochlamys 
              5.3330               5.3330               5.3330 
         Austrovenus            Callonaia         Chagrepecten 
              5.3330               5.3330               5.3330 
           Chioneryx          Clidiophora     Concentricavalva 
              5.3330               5.3330               5.3330 
         Ctenocardia              Didacna           Divalucina 
              5.3330               5.3330               5.3330 
         Equichlamys           Eupatorina               Eupera 
              5.3330               5.3330               5.3330 
            Hippopus           Humphreyia          Lajonkairia 
              5.3330               5.3330               5.3330 
          Litigiella           Mactrinula           Melaxinaea 
              5.3330               5.3330               5.3330 
           Minnivola           Mycetopoda              Myllita 
              5.3330               5.3330               5.3330 
        Neocorbicula         Pachyrotunda        Panamicorbula 
              5.3330               5.3330               5.3330 
           Paradacna           Parvidacna           Penicillus 
              5.3330               5.3330               5.3330 
          Pontalmyra        Prosodacnomya        Pseudamiantis 
              5.3330               5.3330               5.3330 
     Pseudoarcopagia       Pseudocatillus              Pythina 
              5.3330               5.3330               5.3330 
             Resania        Scrobicularia        Scutarcopagia 
              5.3330               5.3330               5.3330 
        Tellinidella             Acorylus           Adamussium 
              5.3330               7.2460               7.2460 
         Afrocardium         Carinastarte            Chionista 
              7.2460               7.2460               7.2460 
         Choristodon             Coelopis            Cymatoica 
              7.2460               7.2460               7.2460 
          Lucinopsis          Semierycina        Spathochlamys 
              7.2460               7.2460               7.2460 
            Turneria          Acturellina            Adipicola 
              7.2460              11.6080              11.6080 
            Axinulus              Chaceia         Conradostrea 
             11.6080              11.6080              11.6080 
            Corculum         Cryptomactra         Cryptopecten 
             11.6080              11.6080              11.6080 
          Deltachion           Diarmaidia       Dichotochlamys 
             11.6080              11.6080              11.6080 
       Exallocorbula          Frigichione             Isomonia 
             11.6080              11.6080              11.6080 
           Lioconcha        Lunulicardium         Lymnocardium 
             11.6080              11.6080              11.6080 
         Mactrodesma          Neotrigonia              Ostomya 
             11.6080              11.6080              11.6080 
         Paleomarcia              Paramya        Potamocorbula 
             11.6080              11.6080              11.6080 
         Properycina        Sarmatimactra           Solecardia 
             11.6080              11.6080              11.6080 
        Veprichlamys              Zealeda              Asaphis 
             11.6080              11.6080              11.6200 
              Eontia           Mytilaster         Nanaochlamys 
             11.6200              11.6200              11.6200 
       Obsoletiforma             Ostreola         Plicatiforma 
             11.6200              11.6200              11.6200 
         Radiolucina           Rupellaria       Scalaricardita 
             11.6200              11.6200              12.7000 
            Cardilia           Clementina          Cyclodicama 
             13.8200              13.8200              13.8200 
            Fabulina               Fulvia            Pillucina 
             13.8200              13.8200              13.8200 
           Siratoria        Solidicorbula            Tellidora 
             13.8200              13.8200              13.8200 
            Aupouria            Bartrumia        Cleidothaerus 
             15.9000              15.9000              15.9000 
           Offadesma                Rohea            Trichomya 
             15.9000              15.9000              15.9000 
          Virmysella          Abrachlamys         Acrosterigma 
             15.9000              15.9700              15.9700 
             Aligena              Anatina          Annachlamys 
             15.9700              15.9700              15.9700 
          Armimiltha              Bassina            Bentharca 
             15.9700              15.9700              15.9700 
           Bucardium         Cardiolucina       Carolinapecten 
             15.9700              15.9700              15.9700 
        Chesacardium          Chesapecten         Circomphalus 
             15.9700              15.9700              15.9700 
     Costaglycymeris         Crassicardia       Cristatopecten 
             15.9700              15.9700              15.9700 
            Dallarca         Decatopecten           Erycinella 
             15.9700              15.9700              15.9700 
         Ezocallista           Florimetis           Hemimactra 
             15.9700              15.9700              15.9700 
             Hiatula        Hysteroconcha       Iheringinucula 
             15.9700              15.9700              15.9700 
           Iphigenia           Korobkovia         Kotorapecten 
             15.9700              15.9700              15.9700 
            Lasaeina                 Leda           Lepilucina 
             15.9700              15.9700              15.9700 
         Leptomactra          Leptopecten              Leukoma 
             15.9700              15.9700              15.9700 
          Liromissus         Lunulicardia        Lunulicardita 
             15.9700              15.9700              15.9700 
          Mactrotoma     Marvacrassatella              Melosia 
             15.9700              15.9700              15.9700 
            Milthona           Mioerycina           Mirapecten 
             15.9700              15.9700              15.9700 
        Mizuhopecten              Modiola           Modiolarca 
             15.9700              15.9700              15.9700 
        Modiomytilus             Moerella         Mytiloconcha 
             15.9700              15.9700              15.9700 
       Neoinoceramus        Nipponomarcia              Notirus 
             15.9700              15.9700              15.9700 
    Oppenheimopecten              Panomya         Patinopecten 
             15.9700              15.9700              15.9700 
           Penitella         Phragmorisma              Placuna 
             15.9700              15.9700              15.9700 
           Platyodon              Pristes           Retrotapes 
             15.9700              15.9700              15.9700 
         Rudicardium             Scacchia             Scambula 
             15.9700              15.9700              15.9700 
             Senilia          Somalidacna                Taras 
             15.9700              15.9700              15.9700 
          Temblornia           Trinitasia          Zenatiopsis 
             15.9700              15.9700              15.9700 
             Zirfaea             Hinnites          Carditopsis 
             15.9700              19.0000              20.4400 
       Caribachlamys          Flexopecten          Fortipecten 
             20.4400              20.4400              20.4400 
            Harvella          Hexacorbula                 Irus 
             20.4400              20.4400              20.4400 
        Lepidopecten              Malleus        Neopycnodonta 
             20.4400              20.4400              20.4400 
         Planikellia          Pleurodesma         Pseudolepton 
             20.4400              20.4400              20.4400 
          Pteromeris          Semicorbula             Serripes 
             20.4400              20.4400              20.4400 
         Sheldonella             Timoclea             Tridacna 
             20.4400              20.4400              20.4400 
       Anomalocardia       Austrohinnites             Chaperia 
             23.0300              23.0300              23.0300 
            Congeria           Crassadoma           Cyclinella 
             23.0300              23.0300              23.0300 
          Dendostrea            Digitaria        Dimarzipecten 
             23.0300              23.0300              23.0300 
        Gloripallium            Goodallia            Laciolina 
             23.0300              23.0300              23.0300 
              Lasaea          Lindapecten            Lucinella 
             23.0300              23.0300              23.0300 
        Macrochlamis         Mancosinodia           Mercenaria 
             23.0300              23.0300              23.0300 
             Merisca           Nodipecten          Notochlamys 
             23.0300              23.0300              23.0300 
          Omanidacna         Paramusculus             Pisidium 
             23.0300              23.0300              23.0300 
        Placunanomia           Pleiorytis        Pleurophopsis 
             23.0300              23.0300              23.0300 
         Proxichione           Pygocardia          Sectipecten 
             23.0300              23.0300              23.0300 
        Semelangulus       Spaniodontella            Stewartia 
             23.0300              23.0300              23.0300 
             Zenatia           Janupecten           Aperiploma 
             23.0300              25.2000              28.1000 
         Brevinucula Costellamussiopecten           Felaniella 
             28.1000              28.1000              28.1000 
       Gigantopecten           Globivenus                 Idas 
             28.1000              28.1000              28.1000 
          Manupecten            Megaxinus             Myadesma 
             28.1000              28.1000              28.1000 
      Papillicardium            Plectodon            Propeleda 
             28.1000              28.1000              28.1000 
            Semelina         Similipecten           Simomactra 
             28.1000              28.1000              28.1000 
        Tellidorella                 Tiza          Vertipecten 
             28.1000              28.1000              28.1000 
         Ainicardita        Amussiopecten        Antillipecten 
             28.4000              28.4000              28.4000 
           Arcinella           Argopecten       Austrocallista 
             28.4000              28.4000              28.4000 
            Chamelea           Chionopsis                 Cosa 
             28.4000              28.4000              28.4000 
               Ctena           Cyrenorita           Eotrigonia 
             28.4000              28.4000              28.4000 
              Euvola          Indoplacuna            Leopecten 
             28.4000              28.4000              28.4000 
             Liocyma           Lyropecten              Myadora 
             28.4000              28.4000              28.4000 
          Mytilopsis        Paralucinella      Patagonicardium 
             28.4000              28.4000              28.4000 
          Periglypta           Pododesmus           Psamosolen 
             28.4000              28.4000              28.4000 
           Scapharca              Solamen              Sunetta 
             28.4000              28.4000              28.4000 
         Temnoconcha             Trisidos          Undulostrea 
             28.4000              28.4000              28.4000 
           Agriopoma             Amiantis          Anisocardia 
             33.9000              33.9000              33.9000 
            Antigona         Aspidopholas       Austrotindaria 
             33.9000              33.9000              33.9000 
         Avicularium            Axinactis              Beguina 
             33.9000              33.9000              33.9000 
          Callithaca            Calloarca         Cardiniopsis 
             33.9000              33.9000              33.9000 
            Castalia        Chrysocardium          Clavipholas 
             33.9000              33.9000              33.9000 
          Compsomyax          Condylocuna         Cryptolucina 
             33.9000              33.9000              33.9000 
         Dallocardia             Darcinia             Diplodon 
             33.9000              33.9000              33.9000 
            Ennucula           Eopapyrina           Epicodakia 
             33.9000              33.9000              33.9000 
              Euloxa           Exosiperna            Gemellima 
             33.9000              33.9000              33.9000 
           Geukensia          Hemicardium             Hilberia 
             33.9000              33.9000              33.9000 
             Homomya          Isocrassina            Katelysia 
             33.9000              33.9000              33.9000 
                Kuia              Ledella              Limarca 
             33.9000              33.9000              33.9000 
           Lirophora             Lissarca             Lutraria 
             33.9000              33.9000              33.9000 
        Microcardium              Mulinia         Notolimopsis 
             33.9000              33.9000              33.9000 
           Notostrea            Ovamactra             Pachydon 
             33.9000              33.9000              33.9000 
              Paphia           Parastarte             Placamen 
             33.9000              33.9000              33.9000 
           Platygena          Psammotreta                Raeta 
             33.9000              33.9000              33.9000 
       Rebeccapecten            Sawkinsia          Semipallium 
             33.9000              33.9000              33.9000 
         Sinodiopsis          Spheniopsis         Spinosipella 
             33.9000              33.9000              33.9000 
           Strigilla              Tagelus       Trigoniocardia 
             33.9000              33.9000              33.9000 
           Venerupis              Venidia        Victoripecten 
             33.9000              33.9000              33.9000 
           Wakullina               Woodia          Zygochlamys 
             33.9000              33.9000              33.9000 
      Trichomusculus           Apolymetis               Artena 
             36.0000              37.2000              37.2000 
             Avicula             Azorinus          Calyptogena 
             37.2000              37.2000              37.2000 
       Cardiocardita             Cardites          Clausinella 
             37.2000              37.2000              37.2000 
        Crepispisula          Eufistulana             Exputens 
             37.2000              37.2000              37.2000 
            Gastrana         Joannisiella          Mactrellona 
             37.2000              37.2000              37.2000 
         Nitidavenus      Notogrammatodon           Nuculoidea 
             37.2000              37.2000              37.2000 
          Parapholas     Pseudocuspidaria     Pseudoportlandia 
             37.2000              37.2000              37.2000 
              Rakhia              Tugonia            Veremolpa 
             37.2000              37.2000              37.2000 
           Vesicomya              Acharax                Adula 
             37.2000              38.0000              38.0000 
            Amotapas            Arginella           Arginopsis 
             38.0000              38.0000              38.0000 
             Boeuvia              Bruetia          Carditamera 
             38.0000              38.0000              38.0000 
           Chattonia        Condylocardia            Cryptomya 
             38.0000              38.0000              38.0000 
            Cumingia         Cuspicorbula         Cytheriopsis 
             38.0000              38.0000              38.0000 
         Dinocardium          Duplipecten                Ensis 
             38.0000              38.0000              38.0000 
             Gouldia          Grateloupia            Halonanus 
             38.0000              38.0000              38.0000 
            Hiatella      Hubertschenckia             Huxleyia 
             38.0000              38.0000              38.0000 
        Juliacorbula               Kellia          Kokanostrea 
             38.0000              38.0000              38.0000 
         Longimactra             Macomona               Marama 
             38.0000              38.0000              38.0000 
        Margaritaria             Mauricia           Micromeris 
             38.0000              38.0000              38.0000 
          Modiolaria           Nevenulora           Noetiopsis 
             38.0000              38.0000              38.0000 
           Palliolum            Papyridea            Parinomya 
             38.0000              38.0000              38.0000 
        Parmicorbula           Pecchiolia          Pectinucula 
             38.0000              38.0000              38.0000 
               Perna          Placopecten           Polidevcia 
             38.0000              38.0000              38.0000 
            Poroleda              Poromya            Potamomya 
             38.0000              38.0000              38.0000 
          Psammacoma        Pseudamussium          Pseudochama 
             38.0000              38.0000              38.0000 
          Recurvella           Salaputium            Saxidomus 
             38.0000              38.0000              38.0000 
              Tawera           Textivenus           Trigonarca 
             38.0000              38.0000              38.0000 
         Trigonulina             Tucetona              Volupia 
             38.0000              38.0000              38.0000 
          Xenoloupia            Xylophaga            Africarca 
             38.0000              38.0000              41.3000 
         Americardia             Anodonta   Australoportlandia 
             41.3000              41.3000              41.3000 
          Axinopsida            Batequeus           Cavilucina 
             41.3000              41.3000              41.3000 
        Cossmannella          Crassinella              Cyclina 
             41.3000              41.3000              41.3000 
            Eumarcia             Euphenax        Ficusocorbula 
             41.3000              41.3000              41.3000 
              Fragum                Gemma           Glycimeris 
             41.3000              41.3000              41.3000 
         Laubriereia           Macrosolen               Marcia 
             41.3000              41.3000              41.3000 
          Mercimonia              Meroena                Metis 
             41.3000              41.3000              41.3000 
       Neaeroporomya         Nicaisolopha            Nucunella 
             41.3000              41.3000              41.3000 
             Pandora         Parathyasira               Phaxas 
             41.3000              41.3000              41.3000 
            Pinctada            Plagiarca          Protonoetia 
             41.3000              41.3000              41.3000 
            Psathura          Pterolucina          Pteropsella 
             41.3000              41.3000              41.3000 
              Rangia        Rhabdopitaria         Ringicardium 
             41.3000              41.3000              41.3000 
          Saccostrea         Scalpomactra              Sinodia 
             41.3000              41.3000              41.3000 
         Soletellina            Standella           Stirpulina 
             41.3000              41.3000              41.3000 
         Superlucina                Turia            Ursirivus 
             41.3000              41.3000              41.3000 
           Venerella                Venus          Aequipecten 
             41.3000              41.3000              47.8000 
              Barnea          Callocardia         Clinocardium 
             47.8000              47.8000              47.8000 
          Cockburnia           Corbulomya          Cyclocardia 
             47.8000              47.8000              47.8000 
             Discors            Divalinga             Egerella 
             47.8000              47.8000              47.8000 
           Eophysema           Eurhomalea            Gaimardia 
             47.8000              47.8000              47.8000 
        Gigantostrea             Gomphina          Hadralucina 
             47.8000              47.8000              47.8000 
              Lepton                Linga            Mesodesma 
             47.8000              47.8000              47.8000 
        Mytilosootus             Nayadina               Noetia 
             47.8000              47.8000              47.8000 
          Nymphactra         Orthocardium             Oxyperas 
             47.8000              47.8000              47.8000 
           Pelecyora         Petalocardia             Physoida 
             47.8000              47.8000              47.8000 
            Raetomya        Sanguinolaria         Schedocardia 
             47.8000              47.8000              47.8000 
                Sita               Tivela         Trigonodesma 
             47.8000              47.8000              47.8000 
        Vepricardium         Jorgechlamys                 Abra 
             47.8000              48.0000              48.6000 
            Alveinus             Amotapus              Amusium 
             48.6000              48.6000              48.6000 
           Amygdalum            Anapteris           Anisodonta 
             48.6000              48.6000              48.6000 
              Bankia           Blagraveia       Ciliatocardium 
             48.6000              48.6000              48.6000 
           Clementia          Cochlodesma           Conchocele 
             48.6000              48.6000              48.6000 
           Cultellus                 Cuna          Cycladicama 
             48.6000              48.6000              48.6000 
         Cyclopecten            Dreissena          Eurytellina 
             48.6000              48.6000              48.6000 
         Heteranomia             Hyotissa            Kellyella 
             48.6000              48.6000              48.6000 
        Laevicardium        Lamelliconcha          Lentipecten 
             48.6000              48.6000              48.6000 
          Mactropsis          Megacardita         Mesosaccella 
             48.6000              48.6000              48.6000 
                 Mya            Nausitora             Pachecoa 
             48.6000              48.6000              48.6000 
           Paraglans           Semeloidea            Sokolowia 
             48.6000              48.6000              48.6000 
          Solecurtus          Tenuimactra            Tivellina 
             48.6000              48.6000              48.6000 
        Cyclochlamys       Elliptotellina              Haliris 
             53.0000              53.0000              53.0000 
          Mesopeplum         Quadrilatera           Acuticosta 
             53.0000              53.0000              55.8000 
              Adrana         Cerastoderma            Cuneopsis 
             55.8000              55.8000              55.8000 
          Eomeretrix           Lamprotula         Pseudomiltha 
             55.8000              55.8000              55.8000 
             Anadara      Anechinocardium              Angulus 
             56.0000              56.0000              56.0000 
           Aulacomya         Austronucula           Basterotia 
             56.0000              56.0000              56.0000 
         Bathytormus              Batissa            Cardiomya 
             56.0000              56.0000              56.0000 
              Chione         Claibornites           Clisocolus 
             56.0000              56.0000              56.0000 
          Comitileda        Coralliophaga         Costelloleda 
             56.0000              56.0000              56.0000 
          Crassatina             Dentonia          Divaricella 
             56.0000              56.0000              56.0000 
               Donax        Eburneopecten              Ervilia 
             56.0000              56.0000              56.0000 
       Eucrassatella        Flemingostrea          Hedecardium 
             56.0000              56.0000              56.0000 
           Hilgardia          Ilymatogyra                Limea 
             56.0000              56.0000              56.0000 
               Lopha               Macoma               Mactra 
             56.0000              56.0000              56.0000 
         Mactromeris           Megayoldia           Mesomiltha 
             56.0000              56.0000              56.0000 
           Montacuta              Mysella         Notocallista 
             56.0000              56.0000              56.0000 
          Nototeredo            Nuttallia            Oryctomya 
             56.0000              56.0000              56.0000 
          Periplomya            Petricola               Pholas 
             56.0000              56.0000              56.0000 
             Pitaria            Pullastra       Rhabdotophorus 
             56.0000              56.0000              56.0000 
             Sarepta          Saxicavella               Semele 
             56.0000              56.0000              56.0000 
         Serripecten                Solen               Solena 
             56.0000              56.0000              56.0000 
              Solyma            Sphaerium           Striostrea 
             56.0000              56.0000              56.0000 
               Tapes                Tenea            Trapezium 
             56.0000              56.0000              56.0000 
            Trigonia                 Unio             Vokesula 
             56.0000              56.0000              56.0000 
            Volsella          Actinodonta        Bothrocorbula 
             56.0000              56.8000              58.7000 
         Cyrtopleura        Scrobiculabra          Semimodiola 
             58.7000              58.7000              58.7000 
       Tellinocyclas                Aeora            Anodontia 
             58.7000              59.2000              59.2000 
          Carditella              Carolia                Circe 
             59.2000              59.2000              59.2000 
         Crassostrea             Kitsonia            Laternula 
             59.2000              59.2000              59.2000 
          Lirodiscus           Litorhadia              Lyonsia 
             59.2000              59.2000              59.2000 
       Macrocallista         Miodontiscus            Notodonax 
             59.2000              59.2000              59.2000 
           Nucinella          Parvicorbis         Sootryenella 
             59.2000              59.2000              59.2000 
             Spisula              Thracia             Tivelina 
             59.2000              59.2000              59.2000 
        Transennella             Vulsella        Acanthocardia 
             59.2000              59.2000              61.6000 
          Acutostrea          Adansonella          Ambigostrea 
             61.6000              61.6000              61.6000 
              Anomia            Aphrodina          Arcomytilus 
             61.6000              61.6000              61.6000 
           Arcopagia            Arcoperna             Arcopsis 
             61.6000              61.6000              61.6000 
             Arctica            Arcticlam            Arcuatula 
             61.6000              61.6000              61.6000 
              Atreta               Atrina               Axinus 
             61.6000              61.6000              61.6000 
         Barbierella            Bathyarca            Bicorbula 
             61.6000              61.6000              61.6000 
              Botula        Caestocorbula             Callista 
             61.6000              61.6000              61.6000 
           Callucina        Callucinopsis         Camptonectes 
             61.6000              61.6000              61.6000 
        Caryocorbula            Cavilinga                Chama 
             61.6000              61.6000              61.6000 
             Chlamys           Clavagella              Codakia 
             61.6000              61.6000              61.6000 
        Corbulamella        Costacallista             Crenella 
             61.6000              61.6000              61.6000 
           Ctenoides          Cubitostrea           Cucullaria 
             61.6000              61.6000              61.6000 
          Cuspidaria           Cyrtodaria             Cytherea 
             61.6000              61.6000              61.6000 
           Dacrydium       Dhondtichlamys                Dimya 
             61.6000              61.6000              61.6000 
          Diplodonta           Disparilia         Divarikellia 
             61.6000              61.6000              61.6000 
             Dosinia          Dosiniopsis            Electroma 
             61.6000              61.6000              61.6000 
            Eriphyla         Eriphylopsis              Erycina 
             61.6000              61.6000              61.6000 
                Etea              Euciroa              Exogyra 
             61.6000              61.6000              61.6000 
             Fimbria       Flabellipecten            Fulcrella 
             61.6000              61.6000              61.6000 
           Gafrarium                 Gari         Gastrochaena 
             61.6000              61.6000              61.6000 
           Gervillia          Gibbolucina                Glans 
             61.6000              61.6000              61.6000 
          Glycymeris          Glyptoactis           Gonimyrtea 
             61.6000              61.6000              61.6000 
          Goossensia         Granocardium          Gregariella 
             61.6000              61.6000              61.6000 
            Gryphaea        Gryphaeostrea                 Here 
             61.6000              61.6000              61.6000 
          Hindsiella       Integricardium              Isoarca 
             61.6000              61.6000              61.6000 
           Isognomon           Jagolucina           Jouannetia 
             61.6000              61.6000              61.6000 
           Kelliella             Kummelia               Kuphus 
             61.6000              61.6000              61.6000 
              Ledina            Lentidium           Leptosolen 
             61.6000              61.6000              61.6000 
                Lima              Limaria             Limopsis 
             61.6000              61.6000              61.6000 
            Liostrea           Lithophaga              Loparia 
             61.6000              61.6000              61.6000 
             Loripes          Loxocardium               Lucina 
             61.6000              61.6000              61.6000 
           Lucinisca             Lucinoma             Martesia 
             61.6000              61.6000              61.6000 
           Marwickia           Meiocardia               Miltha 
             61.6000              61.6000              61.6000 
       Miocardiopsis           Miodomeris          Mixtipecten 
             61.6000              61.6000              61.6000 
          Monitilora             Musculus               Myrtea 
             61.6000              61.6000              61.6000 
             Mytilon                Neilo           Neilonella 
             61.6000              61.6000              61.6000 
             Neithea          Nemocardium              Nemodon 
             61.6000              61.6000              61.6000 
          Nicaniella             Nuculoma       Odontogryphaea 
             61.6000              61.6000              61.6000 
         Orthoyoldia              Oxytoma              Panopea 
             61.6000              61.6000              61.6000 
           Paranomia         Parvamussium         Parvicardium 
             61.6000              61.6000              61.6000 
         Parvilucina               Pecten            Periploma 
             61.6000              61.6000              61.6000 
           Phacoides          Phelopteria           Pholadidea 
             61.6000              61.6000              61.6000 
         Pholadopsis          Placunopsis        Plagiocardium 
             61.6000              61.6000              61.6000 
        Plastomiltha          Pleuromeris            Plicatula 
             61.6000              61.6000              61.6000 
          Polymesoda           Portlandia           Praerangia 
             61.6000              61.6000              61.6000 
       Propeamussium         Prophetilora          Protocardia 
             61.6000              61.6000              61.6000 
         Pseudolimea               Pteria          Pteromyrtea 
             61.6000              61.6000              61.6000 
          Pulvinites        Purpurocardia           Recticardo 
             61.6000              61.6000              61.6000 
            Saccella           Saxolucina             Septifer 
             61.6000              61.6000              61.6000 
             Siliqua              Solemya          Spaniorinus 
             61.6000              61.6000              61.6000 
             Sphenia          Spissatella            Spondylus 
             61.6000              61.6000              61.6000 
           Sportella             Striarca         Syncyclonema 
             61.6000              61.6000              61.6000 
         Talochlamys            Tancredia          Tellinimera 
             61.6000              61.6000              61.6000 
            Teredina               Teredo        Trachycardium 
             61.6000              61.6000              61.6000 
           Trinacria              Uddenia           Unicardium 
             61.6000              61.6000              61.6000 
            Veniella          Verticordia      Vetericardiella 
             61.6000              61.6000              61.6000 
              Yoldia            Yoldiella                 Acar 
             61.6000              61.6000              61.7000 
              Acesta                Acila                 Arca 
             61.7000              61.7000              61.7000 
             Astarte        Australoneilo        Baluchicardia 
             61.7000              61.7000              61.7000 
            Barbatia               Bornia         Brachidontes 
             61.7000              61.7000              61.7000 
       Brachiodontes           Calorhadia              Cardita 
             61.7000              61.7000              61.7000 
             Cardium            Corbicula              Corbula 
             61.7000              61.7000              61.7000 
         Crassatella            Cucullaea         Cuneocorbula 
             61.7000              61.7000              61.7000 
        Cyclorismina        Delectopecten            Epilucina 
             61.7000              61.7000              61.7000 
             Glossus          Grammatodon            Jupiteria 
             61.7000              61.7000              61.7000 
        Katherinella             Lahillia             Limatula 
             61.7000              61.7000              61.7000 
            Malletia             Meretrix             Modiolus 
             61.7000              61.7000              61.7000 
             Mytilus               Nucula             Nuculana 
             61.7000              61.7000              61.7000 
              Ostrea           Pholadomya                Pinna 
             61.7000              61.7000              61.7000 
               Pitar       Pseudaphrodina             Spineilo 
             61.7000              61.7000              61.7000 
             Tellina             Thyasira         Venericardia 
             61.7000              61.7000              61.7000 
          Pycnodonte 
             63.3000 
````             

4) `sort(table(DataPBDB[,"genus"]))`
   Anadara with 1916 occurrences

5) Used same code as number 2 and 3 for stratigraphic range
   Stratigraphic range of Anadara is 66 - 56 million years old.
   
   > I'm not sure how you got that result. The range is from 66-0. -1 Points

## Problem Set 2
1) Lucina[,"paleolng"] tries to find all the paleolongitude in our Lucina sample
   length(Lucina[,"paleolng"] symbolizes the length of vectors in Lucina[,"paleolng"] function
   sample(Lucina[,"paleolng"],length(Lucina[,"paleolng"]),replace=TRUE)) randomly resample the occurrences    of Lucina
   and mean function finds the mean of paleolongitude of these randomly resampled Lucina occurrences.

2) `plot(density(ResampledMeans))`
   Yes, the distribution looks approximately Gaussian since the graph shows typically "bell-curve" shape    (highest in the median value and lowest in both max and min values) which is characteristic feature of    Gaussian distribution.

3) `mean(ResampledMeans)`
   24.16227
   This value is almost similar to the original mean value which is 24.1997

4) Use sort(ResampledMeans) to sort ResampledMeans (couldn't paste every value from the R, because they are too much. However, values are sorted in order by this function)

5) `quantile(ResampledMeans,c(0.025,0.975))`
    2.5%    97.5% 
   21.82094 26.28630

6) 95% of confidence interval means that probability of the true values of parameter lies within specific range of genera is 95%. In question 5, subtract 97.5th to 2.5th percentile equals 95 percentile which leads to the 95% confidence interval. Therefore, in 95% of probability, values are lie within 21.92094 and 26.28630 which makes two of these above values into lower and upper confidence interval of the mean.
 
## Problem Set 3
1. Lucina is likely to still alive. Since it's earliest interval is 0.00 whih represents modern.

2. 
````R
   Dallarca <- subset(DataPBDB,DataPBDB[,"genus"]=="Dallarca")
   estimateExtinction(Dallarca[,"min_ma"],0.95)
   Earliest   Latest 
   2.58800 -3.88749
````

3) No. According to the confidence interval, the earliest extant of Dallarca is 2.588. This data represents that Dallarca went extinct during the end of the Pliocene Epoch

4) Both. The earliest record in the confidence interval (2.588) is almost closer to the latest age of the Pliocene epoch (2.58). Therefore, the confidence interval and pure fossil record show almost similar answer that both can be trusted well in case of Dallarca. However, if I have to choose one, I would choose pure reading of fossil record since it has longer time span than confidence interval (It would be clearer for me if I know the exact date of the last Dallarca occurrence)

## Problem Set 4
1). Since it is randomly distributed, the record of randomly distributed taxon would not match with the lithology (which represents paleoenvironment and ecology of the organism) and show somewhat different pattern than actual fossil records

2) Since likelihood of preservation does not change, this assumption would not show any geological biases (such as preservational biases) and might lead to the different pattern compare to the actual fossil records.

## Problem Set 5
1)
````R
nrow(DataPBDB)
   [1] 67618
   nrow(ExtantData)
   [1] 59097
````   
   8521 occurrences were lost by limiting to only extant bivalves.
2)
````R
nrow(unique(DataPBDB))
   [1] 67618
   nrow(unique(ExtantData))
   [1] 59097
````

According to these data, 12.6% of Cenozoic bivalves in the PBDB are still extant today.

> You made a mistake somewhere, the correct different should be about 52 percent. -1 Points

3) 
````R
sort(tapply(ExtantData[,"max_ma"],ExtantData[,"genus"],max))
   Curvemysella       Galeomma    Perumytilus      Altenaeum      Asperarca 
        0.0117         0.0117         0.0117         0.1260         0.1260 
     Atactodea       Capsella          Comus      Ensiculus        Erodona 
        0.1260         0.1260         0.1260         0.1260         0.1260 
       Exotica     Lamychaena       Leptomya        Mytella  Pascahinnites 
        0.1260         0.1260         0.1260         0.1260         0.1260 
 Pinguitellina      Scintilla     Scissulina    Semimytilus     Semipecten 
        0.1260         0.1260         0.1260         0.1260         0.1260 
    Diplothyra   Parahyotissa      Brechites         Darina     Fungiacava 
        0.7810         0.7810         2.5880         2.5880         2.5880 
   Heterodonax       Irusella      Kurtiella     Marikellia     Musculista 
        2.5880         2.5880         2.5880         2.5880         2.5880 
     Philobrya     Protothaca    Psammotella  Psammotellina    Rochefortia 
        2.5880         2.5880         2.5880         2.5880         2.5880 
     Talabrica       Turtonia    Volachlamys      Wallucina     Cooperella 
        2.5880         2.5880         2.5880         2.5880         3.6000 
 Coralichlamys Crassatellites        Cyamium    Ensitellops     Halonympha 
        3.6000         3.6000         3.6000         3.6000         3.6000 
     Hemidonax      Humilaria      Ischadium    Juxtamusium   Lissochlamys 
        3.6000         3.6000         3.6000         3.6000         3.6000 
    Melliteryx       Myochama      Neaeromya      Nutricola     Pliocardia 
        3.6000         3.6000         3.6000         3.6000         3.6000 
    Pythinella    Serratovola         Theora       Tindaria   Choromytilus 
        3.6000         3.6000         3.6000         3.6000         5.3330 
Clathrotellina    Cyclomactra      Donacilla Excellichlamys       Fugleria 
        5.3330         5.3330         5.3330         5.3330         5.3330 
        Haumea   Laevichlamys     Leptaxinus       Lioberus    Lissopecten 
        5.3330         5.3330         5.3330         5.3330         5.3330 
       Macalia   Maoricardium     Modiolatus      Neolepton      Notolimea 
        5.3330         5.3330         5.3330         5.3330         5.3330 
       Paphies     Perrierina       Quadrans   Rhomboidella      Ruditapes 
        5.3330         5.3330         5.3330         5.3330         5.3330 
   Scissodesma      Serratina       Tellimya   Tindariopsis       Ungulina 
        5.3330         5.3330         5.3330         5.3330         5.3330 
       Aloides   Arcopaginula    Austrovenus    Ctenocardia     Divalucina 
       11.6080        11.6080        11.6080        11.6080        11.6080 
   Equichlamys       Hippopus     Melaxinaea      Minnivola        Pythina 
       11.6080        11.6080        11.6080        11.6080        11.6080 
 Scrobicularia  Scutarcopagia         Tresus       Acorylus     Adamussium 
       11.6080        11.6080        11.6080        11.6200        11.6200 
   Afrocardium    Choristodon      Cymatoica    Semierycina  Spathochlamys 
       11.6200        11.6200        11.6200        11.6200        11.6200 
      Ostreola    Radiolucina     Rupellaria      Adipicola        Asaphis 
       13.8200        13.8200        13.8200        15.9700        15.9700 
       Chaceia       Corculum   Cryptopecten       Fabulina      Lioconcha 
       15.9700        15.9700        15.9700        15.9700        15.9700 
    Mactrinula     Mytilaster    Neotrigonia        Paramya  Potamocorbula 
       15.9700        15.9700        15.9700        15.9700        15.9700 
    Solecardia   Veprichlamys  Cleidothaerus      Trichomya   Cardiolucina 
       15.9700        15.9700        19.0000        19.0000        20.4400 
  Decatopecten         Fulvia     Mactrotoma       Moerella       Scacchia 
       20.4400        20.4400        20.4400        20.4400        20.4400 
      Hinnites      Offadesma   Acrosterigma        Aligena        Anatina 
       21.7000        21.7000        23.0300        23.0300        23.0300 
   Annachlamys       Axinulus        Bassina      Bentharca    Carditopsis 
       23.0300        23.0300        23.0300        23.0300        23.0300 
 Caribachlamys   Circomphalus    Flexopecten        Hiatula      Iphigenia 
       23.0300        23.0300        23.0300        23.0300        23.0300 
          Irus           Leda    Leptopecten   Lunulicardia        Malleus 
       23.0300        23.0300        23.0300        23.0300        23.0300 
    Mirapecten        Modiola        Notirus        Panomya   Patinopecten 
       23.0300        23.0300        23.0300        23.0300        23.0300 
     Penitella        Placuna      Platyodon     Pteromeris        Senilia 
       23.0300        23.0300        23.0300        23.0300        23.0300 
   Sheldonella      Tellidora       Timoclea       Tridacna        Zirfaea 
       23.0300        23.0300        23.0300        23.0300        23.0300 
    Dendostrea      Digitaria      Goodallia      Laciolina    Lindapecten 
       28.1000        28.1000        28.1000        28.1000        28.1000 
     Lucinella  Anomalocardia       Congeria     Cyclinella   Gloripallium 
       28.1000        28.4000        28.4000        28.4000        28.4000 
        Lasaea     Mercenaria        Merisca     Modiolarca     Nodipecten 
       28.4000        28.4000        28.4000        28.4000        28.4000 
      Pisidium   Semelangulus      Stewartia    Brevinucula       Chamelea 
       28.4000        28.4000        28.4000        33.9000        33.9000 
          Cosa     Crassadoma          Ctena     Felaniella     Globivenus 
       33.9000        33.9000        33.9000        33.9000        33.9000 
          Idas        Liocyma     Lyropecten     Manupecten      Megaxinus 
       33.9000        33.9000        33.9000        33.9000        33.9000 
       Myadora Papillicardium     Periglypta      Plectodon     Pododesmus 
       33.9000        33.9000        33.9000        33.9000        33.9000 
     Propeleda       Semelina       Serripes   Similipecten        Solamen 
       33.9000        33.9000        33.9000        33.9000        33.9000 
       Sunetta       Trisidos        Zenatia      Agriopoma       Antigona 
       33.9000        33.9000        33.9000        37.2000        37.2000 
    Compsomyax    Condylocuna    Dallocardia       Ennucula     Epicodakia 
       37.2000        37.2000        37.2000        37.2000        37.2000 
     Katelysia      Lirophora       Lissarca       Lutraria   Microcardium 
       37.2000        37.2000        37.2000        37.2000        37.2000 
        Paphia     Parastarte       Placamen          Raeta    Semipallium 
       37.2000        37.2000        37.2000        37.2000        37.2000 
  Spinosipella      Strigilla        Tagelus Trichomusculus       Amiantis 
       37.2000        37.2000        37.2000        37.2000        38.0000 
       Beguina      Geukensia        Ledella        Limarca    Psammotreta 
       38.0000        38.0000        38.0000        38.0000        38.0000 
    Simomactra Trigoniocardia      Venerupis  Condylocardia       Cumingia 
       38.0000        38.0000        38.0000        41.3000        41.3000 
   Dinocardium          Ensis        Gouldia   Juliacorbula         Kellia 
       41.3000        41.3000        41.3000        41.3000        41.3000 
   Longimactra       Macomona        Mulinia      Palliolum     Pecchiolia 
       41.3000        41.3000        41.3000        41.3000        41.3000 
   Placopecten       Poroleda  Pseudamussium    Pseudochama         Tawera 
       41.3000        41.3000        41.3000        41.3000        41.3000 
   Trigonulina      Xylophaga          Adula    Americardia     Cavilucina 
       41.3000        41.3000        47.8000        47.8000        47.8000 
   Crassinella      Cryptomya          Gemma       Huxleyia        Pandora 
       47.8000        47.8000        47.8000        47.8000        47.8000 
     Papyridea       Pinctada        Poromya         Rangia     Saccostrea 
       47.8000        47.8000        47.8000        47.8000        47.8000 
  Scalpomactra    Soletellina          Venus        Acharax     Apolymetis 
       47.8000        47.8000        47.8000        48.6000        48.6000 
     Arcinella     Argopecten        Avicula       Azorinus    Calyptogena 
       48.6000        48.6000        48.6000        48.6000        48.6000 
   Carditamera       Cardites    Clausinella         Euvola       Gastrana 
       48.6000        48.6000        48.6000        48.6000        48.6000 
      Hiatella   Joannisiella    Mactrellona         Marcia     Mytilopsis 
       48.6000        48.6000        48.6000        48.6000        48.6000 
    Nuculoidea     Parapholas          Perna         Phaxas      Scapharca 
       48.6000        48.6000        48.6000        48.6000        48.6000 
   Temnoconcha       Tucetona        Tugonia      Vesicomya      Amygdalum 
       48.6000        48.6000        48.6000        48.6000        55.8000 
Ciliatocardium      Clementia     Conchocele      Cultellus           Cuna 
       55.8000        55.8000        55.8000        55.8000        55.8000 
   Cycladicama    Cyclopecten Elliptotellina    Heteranomia   Laevicardium 
       55.8000        55.8000        55.8000        55.8000        55.8000 
   Megacardita     Mesopeplum      Nausitora     Solecurtus           Abra 
       55.8000        55.8000        55.8000        55.8000        56.0000 
   Aequipecten       Alveinus        Amusium     Axinopsida         Bankia 
       56.0000        56.0000        56.0000        56.0000        56.0000 
        Barnea    Callocardia   Clinocardium    Cochlodesma     Corbulomya 
       56.0000        56.0000        56.0000        56.0000        56.0000 
   Cyclocardia   Cyclochlamys        Discors      Divalinga      Dreissena 
       56.0000        56.0000        56.0000        56.0000        56.0000 
      Eumarcia     Eurhomalea    Eurytellina         Fragum      Gaimardia 
       56.0000        56.0000        56.0000        56.0000        56.0000 
      Gomphina        Haliris       Hyotissa         Lepton          Linga 
       56.0000        56.0000        56.0000        56.0000        56.0000 
     Mesodesma     Modiolaria            Mya         Noetia       Oxyperas 
       56.0000        56.0000        56.0000        56.0000        56.0000 
  Parathyasira      Pelecyora      Saxidomus      Standella         Tivela 
       56.0000        56.0000        56.0000        56.0000        56.0000 
  Vepricardium    Zygochlamys   Cerastoderma     Basterotia    Bathytormus 
       56.0000        56.0000        58.7000        59.2000        59.2000 
        Chione          Donax        Ervilia          Limea      Montacuta 
       59.2000        59.2000        59.2000        59.2000        59.2000 
       Mysella      Petricola        Pitaria  Sanguinolaria    Saxicavella 
       59.2000        59.2000        59.2000        59.2000        59.2000 
      Volsella      Anodontia      Aulacomya     Carditella          Circe 
       59.2000        61.6000        61.6000        61.6000        61.6000 
   Divaricella      Laternula        Lyonsia   Miodontiscus   Notocallista 
       61.6000        61.6000        61.6000        61.6000        61.6000 
     Nucinella        Sarepta   Transennella      Trapezium       Vulsella 
       61.6000        61.6000        61.6000        61.6000        61.6000 
        Adrana         Mactra         Pholas  Acanthocardia           Acar 
       61.7000        61.7000        61.7000        66.0000        66.0000 
        Acesta          Acila        Anadara        Angulus         Anomia 
       66.0000        66.0000        66.0000        66.0000        66.0000 
          Arca      Arcopagia       Arcopsis        Arctica      Arcuatula 
       66.0000        66.0000        66.0000        66.0000        66.0000 
       Astarte         Atrina         Axinus       Barbatia      Bathyarca 
       66.0000        66.0000        66.0000        66.0000        66.0000 
       Batissa         Bornia         Botula   Brachidontes       Callista 
       66.0000        66.0000        66.0000        66.0000        66.0000 
     Callucina   Camptonectes      Cardiomya        Cardita        Cardium 
       66.0000        66.0000        66.0000        66.0000        66.0000 
  Caryocorbula      Cavilinga          Chama        Chlamys     Clavagella 
       66.0000        66.0000        66.0000        66.0000        66.0000 
       Codakia  Coralliophaga      Corbicula        Corbula    Crassatella 
       66.0000        66.0000        66.0000        66.0000        66.0000 
    Crassatina    Crassostrea       Crenella      Ctenoides      Cucullaea 
       66.0000        66.0000        66.0000        66.0000        66.0000 
    Cuspidaria     Cyrtodaria    Cyrtopleura       Cytherea      Dacrydium 
       66.0000        66.0000        66.0000        66.0000        66.0000 
 Delectopecten          Dimya     Diplodonta        Dosinia      Electroma 
       66.0000        66.0000        66.0000        66.0000        66.0000 
     Epilucina        Erycina        Euciroa  Eucrassatella        Fimbria 
       66.0000        66.0000        66.0000        66.0000        66.0000 
     Gafrarium           Gari   Gastrochaena          Glans        Glossus 
       66.0000        66.0000        66.0000        66.0000        66.0000 
    Glycymeris     Gonimyrtea    Gregariella      Isognomon     Jouannetia 
       66.0000        66.0000        66.0000        66.0000        66.0000 
     Jupiteria      Kelliella         Kuphus      Lentidium           Lima 
       66.0000        66.0000        66.0000        66.0000        66.0000 
       Limaria       Limatula       Limopsis     Lithophaga          Lopha 
       66.0000        66.0000        66.0000        66.0000        66.0000 
       Loripes         Lucina      Lucinisca       Lucinoma         Macoma 
       66.0000        66.0000        66.0000        66.0000        66.0000 
 Macrocallista    Mactromeris       Malletia       Martesia     Megayoldia 
       66.0000        66.0000        66.0000        66.0000        66.0000 
    Meiocardia       Meretrix         Miltha       Modiolus     Monitilora 
       66.0000        66.0000        66.0000        66.0000        66.0000 
      Musculus         Myrtea        Mytilus          Neilo     Neilonella 
       66.0000        66.0000        66.0000        66.0000        66.0000 
   Nemocardium     Nototeredo         Nucula       Nuculana       Nuculoma 
       66.0000        66.0000        66.0000        66.0000        66.0000 
     Nuttallia    Orthoyoldia         Ostrea        Panopea   Parvamussium 
       66.0000        66.0000        66.0000        66.0000        66.0000 
  Parvicardium    Parvilucina         Pecten      Periploma      Phacoides 
       66.0000        66.0000        66.0000        66.0000        66.0000 
    Pholadidea     Pholadomya          Pinna          Pitar  Plagiocardium 
       66.0000        66.0000        66.0000        66.0000        66.0000 
   Pleuromeris      Plicatula     Polymesoda     Portlandia  Propeamussium 
       66.0000        66.0000        66.0000        66.0000        66.0000 
        Pteria  Purpurocardia     Pycnodonte       Saccella         Semele 
       66.0000        66.0000        66.0000        66.0000        66.0000 
      Septifer        Siliqua        Solemya          Solen      Sphaerium 
       66.0000        66.0000        66.0000        66.0000        66.0000 
       Sphenia        Spisula      Spondylus       Striarca     Striostrea 
       66.0000        66.0000        66.0000        66.0000        66.0000 
  Syncyclonema    Talochlamys          Tapes        Tellina         Teredo 
       66.0000        66.0000        66.0000        66.0000        66.0000 
       Thracia       Thyasira  Trachycardium   Venericardia    Verticordia 
       66.0000        66.0000        66.0000        66.0000        66.0000 
        Yoldia      Yoldiella 
       66.0000        66.0000 

 sort(tapply(ExtantData[,"min_ma"],ExtantData[,"genus"],max))
 Curvemysella       Galeomma        Mytella    Perumytilus      Altenaeum 
        0.0000         0.0000         0.0000         0.0000         0.0117 
     Atactodea       Capsella Clathrotellina          Comus      Ensiculus 
        0.0117         0.0117         0.0117         0.0117         0.0117 
       Erodona Excellichlamys        Exotica     Fungiacava    Heterodonax 
        0.0117         0.0117         0.0117         0.0117         0.0117 
      Irusella     Lamychaena       Leptomya        Macalia     Marikellia 
        0.0117         0.0117         0.0117         0.0117         0.0117 
 Pascahinnites  Pinguitellina     Protothaca  Psammotellina      Scintilla 
        0.0117         0.0117         0.0117         0.0117         0.0117 
    Scissulina    Semimytilus     Semipecten    Volachlamys      Wallucina 
        0.0117         0.0117         0.0117         0.0117         0.0117 
     Asperarca       Turtonia     Diplothyra   Parahyotissa      Brechites 
        0.0120         0.0120         0.1260         0.1260         0.7810 
        Darina      Kurtiella     Musculista      Nutricola      Philobrya 
        0.7810         0.7810         0.7810         0.7810         0.7810 
   Psammotella    Rochefortia      Talabrica     Cooperella  Coralichlamys 
        0.7810         0.7810         0.7810         2.5880         2.5880 
Crassatellites        Cyamium    Ensitellops     Halonympha         Haumea 
        2.5880         2.5880         2.5880         2.5880         2.5880 
     Hemidonax      Humilaria      Ischadium    Juxtamusium   Laevichlamys 
        2.5880         2.5880         2.5880         2.5880         2.5880 
  Lissochlamys     Melliteryx       Myochama      Neaeromya     Perrierina 
        2.5880         2.5880         2.5880         2.5880         2.5880 
    Pliocardia     Pythinella       Quadrans    Scissodesma    Serratovola 
        2.5880         2.5880         2.5880         2.5880         2.5880 
        Theora       Tindaria       Ungulina   Choromytilus    Cyclomactra 
        2.5880         2.5880         2.5880         3.6000         3.6000 
     Donacilla       Fugleria     Leptaxinus       Lioberus    Lissopecten 
        3.6000         3.6000         3.6000         3.6000         3.6000 
  Maoricardium     Modiolatus      Neolepton      Notolimea        Paphies 
        3.6000         3.6000         3.6000         3.6000         3.6000 
  Rhomboidella      Ruditapes      Serratina       Tellimya   Tindariopsis 
        3.6000         3.6000         3.6000         3.6000         3.6000 
        Tresus        Aloides   Arcopaginula    Austrovenus    Ctenocardia 
        3.6000         5.3330         5.3330         5.3330         5.3330 
    Divalucina    Equichlamys       Hippopus     Mactrinula     Melaxinaea 
        5.3330         5.3330         5.3330         5.3330         5.3330 
     Minnivola        Pythina  Scrobicularia  Scutarcopagia       Acorylus 
        5.3330         5.3330         5.3330         5.3330         7.2460 
    Adamussium    Afrocardium    Choristodon      Cymatoica    Semierycina 
        7.2460         7.2460         7.2460         7.2460         7.2460 
 Spathochlamys      Adipicola       Axinulus        Chaceia       Corculum 
        7.2460        11.6080        11.6080        11.6080        11.6080 
  Cryptopecten      Lioconcha    Neotrigonia        Paramya  Potamocorbula 
       11.6080        11.6080        11.6080        11.6080        11.6080 
    Solecardia   Veprichlamys        Asaphis     Mytilaster       Ostreola 
       11.6080        11.6080        11.6200        11.6200        11.6200 
   Radiolucina     Rupellaria       Fabulina         Fulvia      Tellidora 
       11.6200        11.6200        13.8200        13.8200        13.8200 
 Cleidothaerus      Offadesma      Trichomya   Acrosterigma        Aligena 
       15.9000        15.9000        15.9000        15.9700        15.9700 
       Anatina    Annachlamys        Bassina      Bentharca   Cardiolucina 
       15.9700        15.9700        15.9700        15.9700        15.9700 
  Circomphalus   Decatopecten        Hiatula      Iphigenia           Leda 
       15.9700        15.9700        15.9700        15.9700        15.9700 
   Leptopecten   Lunulicardia     Mactrotoma     Mirapecten        Modiola 
       15.9700        15.9700        15.9700        15.9700        15.9700 
    Modiolarca       Moerella        Notirus        Panomya   Patinopecten 
       15.9700        15.9700        15.9700        15.9700        15.9700 
     Penitella        Placuna      Platyodon       Scacchia        Senilia 
       15.9700        15.9700        15.9700        15.9700        15.9700 
       Zirfaea       Hinnites    Carditopsis  Caribachlamys    Flexopecten 
       15.9700        19.0000        20.4400        20.4400        20.4400 
          Irus        Malleus     Pteromeris       Serripes    Sheldonella 
       20.4400        20.4400        20.4400        20.4400        20.4400 
      Timoclea       Tridacna  Anomalocardia       Congeria     Crassadoma 
       20.4400        20.4400        23.0300        23.0300        23.0300 
    Cyclinella     Dendostrea      Digitaria   Gloripallium      Goodallia 
       23.0300        23.0300        23.0300        23.0300        23.0300 
     Laciolina         Lasaea    Lindapecten      Lucinella     Mercenaria 
       23.0300        23.0300        23.0300        23.0300        23.0300 
       Merisca     Nodipecten       Pisidium   Semelangulus      Stewartia 
       23.0300        23.0300        23.0300        23.0300        23.0300 
       Zenatia    Brevinucula     Felaniella     Globivenus           Idas 
       23.0300        28.1000        28.1000        28.1000        28.1000 
    Manupecten      Megaxinus Papillicardium      Plectodon      Propeleda 
       28.1000        28.1000        28.1000        28.1000        28.1000 
      Semelina   Similipecten     Simomactra      Arcinella     Argopecten 
       28.1000        28.1000        28.1000        28.4000        28.4000 
      Chamelea           Cosa          Ctena         Euvola        Liocyma 
       28.4000        28.4000        28.4000        28.4000        28.4000 
    Lyropecten        Myadora     Mytilopsis     Periglypta     Pododesmus 
       28.4000        28.4000        28.4000        28.4000        28.4000 
     Scapharca        Solamen        Sunetta    Temnoconcha       Trisidos 
       28.4000        28.4000        28.4000        28.4000        28.4000 
     Agriopoma       Amiantis       Antigona        Beguina     Compsomyax 
       33.9000        33.9000        33.9000        33.9000        33.9000 
   Condylocuna    Dallocardia       Ennucula     Epicodakia      Geukensia 
       33.9000        33.9000        33.9000        33.9000        33.9000 
     Katelysia        Ledella        Limarca      Lirophora       Lissarca 
       33.9000        33.9000        33.9000        33.9000        33.9000 
      Lutraria   Microcardium        Mulinia         Paphia     Parastarte 
       33.9000        33.9000        33.9000        33.9000        33.9000 
      Placamen    Psammotreta          Raeta    Semipallium   Spinosipella 
       33.9000        33.9000        33.9000        33.9000        33.9000 
     Strigilla        Tagelus Trigoniocardia      Venerupis    Zygochlamys 
       33.9000        33.9000        33.9000        33.9000        33.9000 
Trichomusculus     Apolymetis        Avicula       Azorinus    Calyptogena 
       36.0000        37.2000        37.2000        37.2000        37.2000 
      Cardites    Clausinella       Gastrana   Joannisiella    Mactrellona 
       37.2000        37.2000        37.2000        37.2000        37.2000 
    Nuculoidea     Parapholas        Tugonia      Vesicomya        Acharax 
       37.2000        37.2000        37.2000        37.2000        38.0000 
         Adula    Carditamera  Condylocardia      Cryptomya       Cumingia 
       38.0000        38.0000        38.0000        38.0000        38.0000 
   Dinocardium          Ensis        Gouldia       Hiatella       Huxleyia 
       38.0000        38.0000        38.0000        38.0000        38.0000 
  Juliacorbula         Kellia    Longimactra       Macomona     Modiolaria 
       38.0000        38.0000        38.0000        38.0000        38.0000 
     Palliolum      Papyridea     Pecchiolia          Perna    Placopecten 
       38.0000        38.0000        38.0000        38.0000        38.0000 
      Poroleda        Poromya  Pseudamussium    Pseudochama      Saxidomus 
       38.0000        38.0000        38.0000        38.0000        38.0000 
        Tawera    Trigonulina       Tucetona      Xylophaga    Americardia 
       38.0000        38.0000        38.0000        38.0000        41.3000 
    Axinopsida     Cavilucina    Crassinella       Eumarcia         Fragum 
       41.3000        41.3000        41.3000        41.3000        41.3000 
         Gemma         Marcia        Pandora   Parathyasira         Phaxas 
       41.3000        41.3000        41.3000        41.3000        41.3000 
      Pinctada         Rangia     Saccostrea   Scalpomactra    Soletellina 
       41.3000        41.3000        41.3000        41.3000        41.3000 
     Standella          Venus    Aequipecten         Barnea    Callocardia 
       41.3000        41.3000        47.8000        47.8000        47.8000 
  Clinocardium     Corbulomya    Cyclocardia        Discors      Divalinga 
       47.8000        47.8000        47.8000        47.8000        47.8000 
    Eurhomalea      Gaimardia       Gomphina         Lepton          Linga 
       47.8000        47.8000        47.8000        47.8000        47.8000 
     Mesodesma         Noetia       Oxyperas      Pelecyora  Sanguinolaria 
       47.8000        47.8000        47.8000        47.8000        47.8000 
        Tivela   Vepricardium           Abra       Alveinus        Amusium 
       47.8000        47.8000        48.6000        48.6000        48.6000 
     Amygdalum         Bankia Ciliatocardium      Clementia    Cochlodesma 
       48.6000        48.6000        48.6000        48.6000        48.6000 
    Conchocele      Cultellus           Cuna    Cycladicama    Cyclopecten 
       48.6000        48.6000        48.6000        48.6000        48.6000 
     Dreissena    Eurytellina    Heteranomia       Hyotissa   Laevicardium 
       48.6000        48.6000        48.6000        48.6000        48.6000 
   Megacardita            Mya      Nausitora     Solecurtus   Cyclochlamys 
       48.6000        48.6000        48.6000        48.6000        53.0000 
Elliptotellina        Haliris     Mesopeplum         Adrana   Cerastoderma 
       53.0000        53.0000        53.0000        55.8000        55.8000 
       Anadara        Angulus      Aulacomya     Basterotia    Bathytormus 
       56.0000        56.0000        56.0000        56.0000        56.0000 
       Batissa      Cardiomya         Chione  Coralliophaga     Crassatina 
       56.0000        56.0000        56.0000        56.0000        56.0000 
   Divaricella          Donax        Ervilia  Eucrassatella          Limea 
       56.0000        56.0000        56.0000        56.0000        56.0000 
         Lopha         Macoma         Mactra    Mactromeris     Megayoldia 
       56.0000        56.0000        56.0000        56.0000        56.0000 
     Montacuta        Mysella   Notocallista     Nototeredo      Nuttallia 
       56.0000        56.0000        56.0000        56.0000        56.0000 
     Petricola         Pholas        Pitaria        Sarepta    Saxicavella 
       56.0000        56.0000        56.0000        56.0000        56.0000 
        Semele          Solen      Sphaerium     Striostrea          Tapes 
       56.0000        56.0000        56.0000        56.0000        56.0000 
     Trapezium       Volsella    Cyrtopleura      Anodontia     Carditella 
       56.0000        56.0000        58.7000        59.2000        59.2000 
         Circe    Crassostrea      Laternula        Lyonsia  Macrocallista 
       59.2000        59.2000        59.2000        59.2000        59.2000 
  Miodontiscus      Nucinella        Spisula        Thracia   Transennella 
       59.2000        59.2000        59.2000        59.2000        59.2000 
      Vulsella  Acanthocardia         Anomia      Arcopagia       Arcopsis 
       59.2000        61.6000        61.6000        61.6000        61.6000 
       Arctica      Arcuatula         Atrina         Axinus      Bathyarca 
       61.6000        61.6000        61.6000        61.6000        61.6000 
        Botula       Callista      Callucina   Camptonectes   Caryocorbula 
       61.6000        61.6000        61.6000        61.6000        61.6000 
     Cavilinga          Chama        Chlamys     Clavagella        Codakia 
       61.6000        61.6000        61.6000        61.6000        61.6000 
      Crenella      Ctenoides     Cuspidaria     Cyrtodaria       Cytherea 
       61.6000        61.6000        61.6000        61.6000        61.6000 
     Dacrydium          Dimya     Diplodonta        Dosinia      Electroma 
       61.6000        61.6000        61.6000        61.6000        61.6000 
       Erycina        Euciroa        Fimbria      Gafrarium           Gari 
       61.6000        61.6000        61.6000        61.6000        61.6000 
  Gastrochaena          Glans     Glycymeris     Gonimyrtea    Gregariella 
       61.6000        61.6000        61.6000        61.6000        61.6000 
     Isognomon     Jouannetia      Kelliella         Kuphus      Lentidium 
       61.6000        61.6000        61.6000        61.6000        61.6000 
          Lima        Limaria       Limopsis     Lithophaga        Loripes 
       61.6000        61.6000        61.6000        61.6000        61.6000 
        Lucina      Lucinisca       Lucinoma       Martesia     Meiocardia 
       61.6000        61.6000        61.6000        61.6000        61.6000 
        Miltha     Monitilora       Musculus         Myrtea          Neilo 
       61.6000        61.6000        61.6000        61.6000        61.6000 
    Neilonella    Nemocardium       Nuculoma    Orthoyoldia        Panopea 
       61.6000        61.6000        61.6000        61.6000        61.6000 
  Parvamussium   Parvicardium    Parvilucina         Pecten      Periploma 
       61.6000        61.6000        61.6000        61.6000        61.6000 
     Phacoides     Pholadidea  Plagiocardium    Pleuromeris      Plicatula 
       61.6000        61.6000        61.6000        61.6000        61.6000 
    Polymesoda     Portlandia  Propeamussium         Pteria  Purpurocardia 
       61.6000        61.6000        61.6000        61.6000        61.6000 
      Saccella       Septifer        Siliqua        Solemya        Sphenia 
       61.6000        61.6000        61.6000        61.6000        61.6000 
     Spondylus       Striarca   Syncyclonema    Talochlamys         Teredo 
       61.6000        61.6000        61.6000        61.6000        61.6000 
 Trachycardium    Verticordia         Yoldia      Yoldiella           Acar 
       61.6000        61.6000        61.6000        61.6000        61.7000 
        Acesta          Acila           Arca        Astarte       Barbatia 
       61.7000        61.7000        61.7000        61.7000        61.7000 
        Bornia   Brachidontes        Cardita        Cardium      Corbicula 
       61.7000        61.7000        61.7000        61.7000        61.7000 
       Corbula    Crassatella      Cucullaea  Delectopecten      Epilucina 
       61.7000        61.7000        61.7000        61.7000        61.7000 
       Glossus      Jupiteria       Limatula       Malletia       Meretrix 
       61.7000        61.7000        61.7000        61.7000        61.7000 
      Modiolus        Mytilus         Nucula       Nuculana         Ostrea 
       61.7000        61.7000        61.7000        61.7000        61.7000 
    Pholadomya          Pinna          Pitar        Tellina       Thyasira 
       61.7000        61.7000        61.7000        61.7000        61.7000 
  Venericardia     Pycnodonte 
       61.7000        63.3000 
       
````

4) `tapply(ExtantData[,"min_ma"],ExtantData[,"genus"],max)` -> Same code to get minimum age of stratigraphic range of genera, Every genera except  Curvemysella, Galeomma, Mytella, and Perumytilus are not extant according to the PBDB.

5. Scrobiculara <- subset(ExtantData,ExtantData[,"genus"]=="Scrobicularia")
   estimateExtinction(Scrobiculara[,"min_ma"],0.95)
   Earliest    Latest 
   0.01170   -34.70966 

   Meiocardia <- subset(ExtantData,ExtantData[,"genus"]=="Meiocardia")
   estimateExtinction(Meiocardia[,"min_ma"],0.95)
   Earliest    Latest 
   0.011700  -5.329574 

   Dimya <- subset(ExtantData,ExtantData[,"genus"]=="Dimya")
   estimateExtinction(Dimya[,"min_ma"],0.95)
   Earliest    Latest 
   0.781000 -2.054688

   Digitaria <- subset(ExtantData,ExtantData[,"genus"]=="Digitaria")
   estimateExtinction(Digitaria[,"min_ma"],0.95)
   Earliest    Latest 
   0.781000 -3.761154 
 
   Cuspidaria <- subset(ExtantData,ExtantData[,"genus"]=="Cuspidaria")
   estimateExtinction(Cuspidaria[,"min_ma"],0.95)
   Earliest    Latest 
   2.5880000 0.7771965 

   Arctica <- subset(ExtantData,ExtantData[,"genus"]=="Arctica")
   estimateExtinction(Arctica[,"min_ma"],0.95)
   Earliest    Latest 
   0.011700 -1.799104 

   Aloides <- subset(ExtantData,ExtantData[,"genus"]=="Aloides")
   estimateExtinction(Aloides[,"min_ma"],0.95)
   Earliest   Latest 
   5.333     -Inf 

   Kurtiella <- subset(ExtantData,ExtantData[,"genus"]=="Kurtiella")
   estimateExtinction(Kurtiella[,"min_ma"],0.95)
   Earliest    Latest 
   0.01170   -34.70966

   Gouldia <- subset(ExtantData,ExtantData[,"genus"]=="Gouldia")
   estimateExtinction(Gouldia[,"min_ma"],0.95)
   Earliest    Latest 
   0.011700 -2.047386

   Acrosterigma <- subset(ExtantData,ExtantData[,"genus"]=="Acrosterigma")
   estimateExtinction(Acrosterigma[,"min_ma"],0.95)
   Earliest    Latest 
   0.011700 -3.481128

   0% of these taxa have confidence intervals indicating that the taxon might be still extant. Even though most of genera lived until modern time (0.0117 mya) but they don't have fossil records until (0.0 mya) which means none of them still extant until now according to the PBDB.
   
   > That is a completely wrong interpretation. The negative confidence interval means that the confidence interval is projecting an extinction date into the future. -2 Points


 



