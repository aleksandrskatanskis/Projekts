# Darba uzdevums
Es nodarbojos ar brīvo cīņu, un man dažreiz dod iespēju palīdzēt organizēt sacensības. Līdz šim brīdim process bija sekojošs. Pirms sacensībām galvenais sekretārs saņem iesniegumus no dažādām komandām un ieraksta tos savā sarakstā (nezinu kāpēc, bet visi to darīja uz A4 lapas). Sacensību dienā, sveršanas laikā saraksti mainās, jo kāds var saslimt vai aiziet uz citu svara kategoriju. Pēc sveršanas līdz sacensību sākumam ir apmēram 2 stundas. Tajā laikā apmēram 4-5 sekretāriem (mans darbs) jāuzraksta ar roku lielāko daļu sacensību protokolu (izloze + ierakstīšana turnīra tīklā), lai sacensības varētu sākties. Pēc tam jāpabeidz visu. Ja sacensības ir lielas un starptautiskas, svara kategoriju skaits var sasniegt 40+. Es optimizēju šo procesu ar savu programmu, kas veic izlozi un izveido sarakstus ātri un efektīvi, ļaujot sacensību organizatoriem vairāk koncentrēties uz pārējām lietām. 

Šī programma jau tika demonstrēta tuvākajiem sacensību organizatoriem, un tā tiks izmantota 27. janvārī Ķēkavā, par ko es saņemšu atalgojumu.  :)

# Izmantotas bibliotēkas
Šajā Python skriptā tiek izmantotas vairākas bibliotēkas, lai veiktu teksta apstrādi un radītu Word dokumentus:

1. os: Šī bibliotēka nodrošina iespēju veikt darbības ar operētājsistēmu, piemēram, darbības ar failu ceļiem. Šajā gadījumā tā tiek izmantota, lai iegūtu failu sarakstu direktorijā un apvienotu ceļus.

2. random: Šī bibliotēka nodrošina funkcijas gadījuma skaitļu ģenerēšanai un apstrādei. Šajā skriptā tā tiek izmantota, lai sajauktu teksta rindiņas pirms to ievietošanas Word dokumentā.

3. docx: Šī bibliotēka ļauj veidot un rediģēt Word dokumentus (.docx). Izmantojot to, tiek izveidots jauns Word dokumentu objekts (Document), un tiek pievienoti dažādi elementi, piemēram, virsraksti, tabulas un formatējums.

4. Cm, Pt: Šie ir docx.shared bibliotēkas elementi, kas tiek izmantoti, lai norādītu izmērus centimetros (Cm) vai punktos (Pt) Word dokumenta elementiem, piemēram, tabulas kolonnām vai teksta fontam.

# Izmantotas metodes

Metodes, kas tiek izmantotas programmatūras izmantošanai:

1. createWordFromText(textFilePath): Šī funkcija veic visu nepieciešamo darbību, lai izveidotu Word dokumentu no norādītā teksta faila. Tā iegūst faila saturu, sajaukā to, izveido Word dokumentu ar virsrakstu un tabulu, un pēc tam saglabā dokumentu noražu direktorijā.

2. for filename in textFiles:
    textFilePath = os.path.join(spiskiDirectory, filename)
    createWordFromText(textFilePath)
skripts, kur tiek iegūts saraksts ar visiem teksta failiem textFiles, un pēc tam tiek veikta createWordFromText izsaukšana katram failam.