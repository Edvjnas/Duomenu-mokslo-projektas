# Duomenų-mokslo-projektas
Kalbos žymėjimo klaidų taisymas taikant klasterizaciją ir klasifikavimą.

Pateikiame viso projekto kodą. Atskiros dvi dalys: pradinė analizė ir hipotezės, pilnas kalbos atpažinimo algoritmas.

 # Santrauka
 Šiame darbe bus kuriamas ir įgyvendinamas metodas, skirtas automatiškai priskirti kalbas tekstams. Pasiūlytas metodas remsis kelių etapų seka: pirmiausia, duomenys bus suskirstyti į klasterius naudojant KMeans algoritmą, siekiant aptikti galimus kalbinės struktūros skirtumus. Tuomet, jei klasteriai išsiskirs pakankamai aiškiai, kalba bus priskiriama automatiškai remiantis dažniausiais žodžiais bei jų kalbiniais bruožais. Jei toks atskyrimas nebus pakankamas, bus taikomas logistinės regresijos modelis, mokomas naudojant iš anksto parinktus reprezentatyvius anglų kalbos pavyzdžius ir konkrečios šalies ne anglų kalbos segmentus. Jei ir po šio etapo kai kurių įrašų kalbos liks neapibrėžtos, jiems bus pritaikytas fastText modelis, kuris leis priskirti kalbą tik esant aukštam pasitikėjimo lygiui. 
 Bus siekiama, kad metodas veiktų automatizuotai, bet kartu leistų įsiterpti žmogui tik tais atvejais, kai automatinis sprendimas yra nepakankamai tikslus arba dviprasmiškas. Metodas bus įvertintas empiriškai,pasitelkiant Lietuvos ir Kanados duomenis, siekiant apimti skirtingus problemos scenarijus– nuo vienos dominuojančios ne anglų kalbos iki mišrių kalbinių struktūrų. Rezultatai parodys, kad pasiūlyta sistema gebės patikimai atskirti klaidingai sužymėtus duomenis ir ženkliai pagerins bendrą kalbos žymėjimo kokybę dideliuose tekstiniuose rinkiniuose.
 ## Raktiniai žodžiai : Kalbos identifikavimas, automatinis žymėjimas, klasterizacija, logistinė regresija, fastText, pusiau prižiūrimas mokymas, duomenų kokybės gerinimas.
 
 # Correction of Language Labeling Errors Using Clustering and Classification
 # Abstract
 In this work, a method will be developed and implemented to automatically assign language labels. The proposed method will follow a multi–stage process: first, the data will be clustered using the KMeans algorithm
 in order to identify possible differences in linguistic structure. If the clusters are clearly distinguishable, the
 language will be assigned automatically based on the most frequent words and their linguistic features. If this
 separation is insufficient, a logistic regression model will be applied, trained on pre–selected representative
 samples of English language data and segments from a specific non–English language within the target count
 ry. If the language of some entries still cannot be determined after this stage, the fastText model will be used,
 which assigns a language label only when the confidence level is sufficiently high.
 The goal is to ensure that the method operates in a fully automated manner, while still allowing human
 intervention in cases where automatic decisions are uncertain or ambiguous. The method will be evaluated
 empirically using data from Lithuania and Canada, in order to cover different types of scenarios– from data
 sets dominated by a single non–English language to those with mixed multilingual structures. The results are
expected to demonstrate that the proposed system can reliably identify mislabelled entries and significantly
 improve the overall quality of language annotations in large–scale textual datasets.
 ## Keywords : Language identification, automatic labeling, clustering, logistic regression, fastText, semi supervised learning, data quality improvement
