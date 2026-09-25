# Lista soluțiilor de AI

## Înregistrări

### Agent de screening AML/KYC — informații negative despre persoanele juridice monitorizate

| Câmp | Răspuns |
|------------------------------|------------------------------------------------------------|
| **Denumirea** | Agent de screening AML/KYC. Dezvoltator: Banca. Folosește modelele de limbaj `gpt-4.1` și `gpt-4.1-mini` și modelul de embedding `text-embedding-3-large` (furnizor OpenAI), precum și căutarea web prin SerpAPI (rezultate Google) și Tavily |
| **Ce face** | Monitorizarea activității clienților persoane juridice în primul an de activitate în cadrul Băncii. Scopul: optimizarea acestui proces. Pentru fiecare persoană juridică monitorizată, soluția caută în surse web publice, în limbile engleză, română și rusă, informații negative (infracțiuni financiare, corupție, crimă organizată, sancțiuni, procese judiciare, probleme reputaționale) și propune un scor de risc și o recomandare privind relația de afaceri, pe care le analizează un angajat |
| **Tipul AI** | AI generativ. Se folosește și un model de embedding, pentru filtrarea paginilor după similitudinea de sens |
| **Modul de furnizare** | Dezvoltată intern, pe baza modelelor și a serviciilor de căutare ale unor terți, apelate prin API |
| **Unde rulează** | Hibrid. Scriptul rulează local, pe serverele Băncii din Republica Moldova; baza de date este, de asemenea, locală, în Republica Moldova. Modelele de limbaj și de embedding sunt apelate prin API la OpenAI, iar căutarea web — prin SerpAPI și Tavily. Regiunea/țara platformelor API: în principal SUA |
| **Stadiul utilizării** | Testare/experiment |
| **Pe ce date** | Date publice sau anonimizate. Soluția folosește doar date publice: denumirea persoanelor juridice și informații din pagini web publice. Nu se prelucrează informații ce constituie secret bancar |
| **Rolul rezultatului AI** | Recomandă sau fundamentează o decizie a angajatului. Rezultatul este doar o recomandare, sub supraveghere umană: un angajat analizează scorul, recomandarea și sursele indicate și ia personal decizia privind relația de afaceri. Soluția nu adoptă și nu execută nicio decizie privind clientul |
| **Afectează clienții** | Da, indirect. Persoanele juridice monitorizate sunt clienți ai Băncii, iar recomandarea privește continuarea, suspendarea sau încetarea relației de afaceri cu aceștia |
| **Perioada utilizării** | În curs. Aproximativ 500 de persoane juridice pe lună |
| **Responsabil** |  |
