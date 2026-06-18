# Transcriptomics-Jaar-2

Famke Brouwer
LBM3 - J2P4 - Transcriptomics


# Transcriptomics toont aan dat genen komen anders tot expressie bij patiënten met Rheumatoïde artitis 

## 📁 Inhoud/structuur

- `Introductie` – Korte introductie en achtergrond informatie.  
- `Methode` - Methode gebruikt voor analyses. 
- `Scripts` – Scripts voor extra uitleg over de gebruikte analyses en methodes. 
- `Resultaten` - Volcanoplot, go-analyse en KEGG analyse.
- `Bronnen` - Gebruikte bronnen.
- `README.md` - Het document om de tekst hier te genereren.


---

## 🧠 Introductie
Rheumatoïde artritis (RA) is een auto-immuunziekte die zorgt voor chronische inflammatie in gewrichten, voornamelijk in de handen en voeten. Het zorgt voor veel pijn en op den duur ook weefselschade en functie-verlies. De exacte oorzaak is nog onbekend, maar men neemt wel aan dat het zeer waarschijnlijk een genetische oorzaak heeft. ​(Hall et al., 2024)​  

 

Transcriptomics is een technologie, die complexe analyses kan uitvoeren op het gebied van RNA-expressie. Met behulp van RNA sequencing en transcriptomics kunnen verschillen in genexpressie bij mensen met RA en gezonde mensen in kaart gebracht worden ​(Miyamoto et al., 2025) ​. Binnen transcriptomics kan worden gekeken naar biologische processen, betrokken genen, en signaalroutes. Dit kan met behulp van KEGG-pathways en Gene Ontology. In dit onderzoek worden patiënten met RA vergeleken met gezonde individuen om te kijken of er bepaalde genen meer of minder tot expressie komen en er word gekeken of metabole processen anders verlopen bij RA. ​(Wang et al., 2024)​


## 🧬 Methoden
Voor deze transcriptomics-analyse werd gebruikgemaakt van RNA-sequencingdata van acht personen: vier met reumatoïde artritis (RA) en vier zonder RA. De [ruwe sequencingbestanden](Ruwe%20data/)
 (FASTQ) werden uitgepakt en ingelezen in R. Vervolgens werd het [humane referentiegenoom](Referentie%20genoom) geïndexeerd met het pakket Rsubread, waarna de reads van de samples werden uitgelijnd met de functie align(). De gegenereerde [BAM-bestanden](BAM%20files) zijn gebruikt voor analyse.
Met featureCounts werd er een countmatrix gemaakt, waarbij een aangepaste GTF-annotatie werd gebruikt om alleen op exons te tellen. Vervolgens is er een [volledige count-matrix](Count%20matrix) gebruikt voor verder onderzoek.
De verschillen in genexpressie tussen RA en controle werden bepaald met het pakket DESeq2. De resultaten werden geëxporteerd naar een CSV-bestand en gevisualiseerd met behulp van EnhancedVolcano.
Vervolgens werd met een R-pakket (goseq) onderzocht welke biologische processen verhoogt voorkwamen in genen die anders tot expressie kwamen bij RA. Deze processen (Go-termen) kunnen betrokken zijn bij de ziekte en werden gevisualiseerd met behulp van ggplots2. Daarna is er een KEGG-analyse om dieper in te gaan op de biochemische pathways, die zijn gevisualiseerd met behulp van pathview. Het onderzoek is vastgelegd volgend de principes van data stewardship, met duidelijke mappen structuur en reproduceerbaarheid. 

📄 **[Klik hier voor het volledige script](Scripts/Script%20R%20Casus.R)**
  

[![Klik hier voor het volledige script](https://img.shields.io/badge/Script_R_Casus-pink?style=flat&logo=R&logoColor=white)](Scripts/Script%20R%20Casus.R)


## 📊 Resultaten

### 🌋 Volcanoplot van genexpressie (EnhancedVolcano)
In figuur 1 is een volcanoplot zichtbaar van 29.407 genen zichtbaar. Er is zichtbaar dat er veel genen zijn rond de log2-fold = 0, die niet significant verschillen. De groene stippen zijn de genen die significant verschillen van expressie. 

<img src="Resultaten/Volcanoplot.png" width ="250" height ="350">
Figuur 1: Volcanoplot toont de log2-fold change (x-as) tegen de -log10 p-waarde (y-as) voor alle gemeten genen (totaal: 29.407)

**[Afbeelding vergroten 🔍](Resultaten/Volcanoplot.png)**


### 📊 GO-analyse
In figuur 2 is duidelijk zichtbaar de gen expressie in processen zoals bijvoorbeeld, het immuun-respons significant veranderd zijn. 

<img src="Resultaten/Go-analyse.pdf" width ="500" height ="350">
Figuur 2: Barplot Go-analyse, toont aan bij welke processen meeste verandering in gen expressie is waargenomen. 

**[Afbeelding vergroten 🔍](Resultaten/Go-anlyse.pdf)**


### 🧬 Pathway-analyse KEGG Rheumatoïde Artritis
In figuur 3 zijn opvallende bevindingen waargenomen, waaronder de genen **IL6, IL1β en MMP13** die verhoogd tot expressie komen. Deze genen zijn betrokken bij ontsteking, kraakbeenschade en gewrichtsvernietiging. Ook zijn er genen zoals, **TGFβ**, (betrokken bij immuunonderdrukking en weefselherstel) en **IL23** (stimuleert ontstekingsbevorderende T-cellen), die juist onderdukt worden.

<img src="Resultaten/hsa05323 pathview results.png" width ="500" height ="350">
Figuur 3: KEGG pathview afbeelding, geeft duidelijk verhoogd (Rood) en verlaagde (Groen) activiteit van ontstekingsgenen weer.

**[Afbeelding vergroten 🔍](Resultaten/hsa05323%20pathview%20results.png)**


## ⚡Conclusie
De resultaten tonen aan dat er een verandering in genexpressie is bij patiënten RA. Dit is bevestigd in de volcanoplot, die aangaf dat er een veel significant verschillende genen zijn bij RA patiënten. In de Go-analyse is aangetoond dat veel genen die significant verschillen betrokken zijn bij het **immuunrespons**. Dit is verder bevestigd door de KEGG pathways waar genen **IL6, IL1β en MMP13** verhoogd tot expressie kwamen. Deze genen zijn betrokken bij ontsteking, kraakbeenschade en gewrichtsvernietiging. Ook waren er genen zoals, **TGFβ**, (betrokken bij immuunonderdrukking en weefselherstel) en **IL23** (stimuleert ontstekingsbevorderende T-cellen), die juist onderdukt werden. Dit gaf aan dat er bij mensen met RA een verstoring plaats vond in ontstekingregulatie.

In dit onderzoek is dus aangetoond dat transcriptomics een handige tool is in het begrijpen van de ziekte RA. Daarom word aanbevolen meer onderzoek te doen met grotere groepen en bijvoorbeeld verschillende statia RA, om hopelijk meer mogelijke biomarkers te ontdekken.
