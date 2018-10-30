## Hvorfor R til analyse?
* Open source = gratis
* State of the art datascience-biblioteker
* Reproducerbart. Vis f.eks et kompleks regneark, med en masse uafhængiheder. Umuligt at gennemskue. Hvad hvis du får et nyt datasæt? Ikke modulært, du kan ikke genbruge dele af din analyse. 
* Verdens bedste data-science IDE, RStudio
* R producerer publikationsklar grafik
* R understøtter alle de analyser, du kan komme i tanke om.

## Hvorfor ikke R til analyse
* R spiller ikke så let ind i et klassisk windows corporate miljø, her er tableau og powerBI nemmere at få i produktion (men det kan sagtens lade sig gøre med R)
* Hvis du skal lave algoritmer der kræver ekstrem hastighed (men god integration med cpp)
* Hvis du skal lave analyser eller produkter til et python-only produktionsmiljø

## Fordele ved tidyverse
* [Tidy tools manifesto](https://tidyverse.tidyverse.org/articles/manifesto.html)
>Programs must be written for people to read, and only incidentally for machines to execute.

* Human readable code - eksempel på operation i R med nestede funktionskald, firkantede parenteser, etc, sammenlignet med et pænt pipet tidy workflow
* You're coding for you 3 months in the future!
* Self-documenting code - brug mindre tid på at kommentere din kode, og mere tid på koden
* Der er konsistens mellem de forskellige pakker i tidyverse.

* Fortæl om RStudio, og deres mission - samler de bedste hjerner indenfor R til at udvikle standarder og moderne udvidelser til R til data science, tjener penge på enterprise produkter

## Markdown
* Hurtig introduktion til markdown. Smart, fordi code-chunks evalueres dynamisk, velegnet til rapporter etc. Tvinger dig til god kodestil og relativt ryddelige scripts.
* Hurtig demo af konvertering til HTML / PDF ? (kræver selvfølgelig installation af knirt etc., men markdown er et stærkt undervisningsværktøj. 
* Få deltagerne til at lave deres øvelser i markdown

## Kursusemner (godt klar over, at alt dette ikke kan nås, pick and choose)
* Kort simplificeret introduktion til Rs datatyper (struktur: vector, list, data-frame, type: integer, numeric, character, factor, bool). Ingen scalars i R.

* readr og dens vigtigste funktioner til messy data ingression, herunder locale, missing values etc.
    * col-type parsing
    * `parse_*`, parser NA, NAN etc.
    * `locale`, holder styr på locale-specifikke kommaer, decimaltegn, etc.
* magrittr, `%>%`
* long vs. wide format, fordele ulemper, hvad forventer tidyverse? Data reshaping `spread`, `gather`, etc.
* tibble - fordele, `as_tibble`, `glimpse`, 
* dplyr verbs, `select`, `filter`, `mutate`, etc.
* tidy select helpers `starts_with`, `contains`. Super stærke for større datasæt.
* SQL-style grouping og summarizing, `group_by`, `summarize`, summary functions within-groups, f.eks `mean`.
* `mutate`på grouped tibble, viser per-group column-creation, hvilken er et hyppigt problem, der er nederen i base R.
* joins 
* ggplot2, et par hurtige imponerende one-liners der viser styrken og flexibiliten ved ggplot
* geoms
* aestethics and data mappings forklaret intuitivt

## Konkrete øvelser
* Læs et datasæt ind fra forskellige kilder, csv., excel, SQL, SAS, etc.
* Læs et messy datasæt ind med forskellige NA-typer, forkerte decimaltegn, ufuldkommen sidste linie, tal der er formateret som strings, etc. Typiske real-life scenarier.
* Øvelser i filtrering, selektion, long/wide-konvertering, grouping, summarisering, joining
* Datasæt til exploration og plot: cars, diamonds
* Godt real-life example: Folk downloader deres rigtige time-baserede strømforbrug fra eloverblik.dk
    * Visualiser forbrug over tid
    * Se kun på ændringer i natforbrug, dagsforbrug, aftenforbrug
    * Udregn means af forskellige vinduer over døgnet og visualiser
    * Fjern outliers

## Markdown
* Dynamiske og parameteriserede rapporter i markdown
* Markdown til HTML, PDF, word (evt officer-pakken), slides. Rapportering kan automatiseres til mange formater.
