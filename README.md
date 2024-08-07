# Node.js və MongoDB: Back-end Məlumat Bazası Tətbiqlərinin İnkişafı

## Giriş

Node.js və NoSQL məlumat bazaları birləşdirildikdə server tərəfində tətbiq inkişafında inqilab yaradır. W3Techs-in sorğusuna görə, yalnız ABŞ-da 6.3 milyondan çox veb sayt Node.js istifadə edir, bu da onu yeni server tərəfli tətbiqlər üçün ən yaxşı seçim edir. Arxa plan (Back-end) tətbiqlərin mühərrikidir, istifadəçi autentifikasiyası, məlumatların işlənməsi və serverlər və istifadəçi interfeysləri arasında ünsiyyət kimi funksiyaları idarə edir.

Server tərəfli tətbiq vaxtı olan Node.js, JavaScript istifadə edərək arxa plan inkişafını dəyişdirib, bu da ön tərəf (front-end) inkişafı üçün geniş istifadə edilən eyni dildir. O, həmçinin ön və arxa plan arasında çoxlu ünsiyyətləri səmərəli idarə edir, bu da cavab verən və səmərəli tətbiqlər yaratmaq üçün əla seçimdir. MongoDB isə struktursuz və yarı strukturlu məlumatların manipulyasiyası, saxlanması və geri alınması üçün elastiklik və miqyaslanma təmin edir.


## Məlumat və Məlumat Bazalarına Giriş (Introduction to Data and Databases)

Məlumat, sözlər, rəqəmlər və ya hətta şəkillər formasında faktların toplusudur. Məlumat hər hansı bir müəssisənin ən vacib aktivlərindən biridir və demək olar ki, hər yerdə istifadə edilir və toplanır. Məsələn, bankınız sizin adınız, ünvanınız, telefon nömrəniz və hesab nömrələriniz kimi məlumatlarınızı saxlayır. Eyni şəkildə, kredit kartı şirkətiniz və PayPal hesablarınız da sizin haqqınızda məlumat saxlayır. Məlumatın əhəmiyyəti nəzərə alınaraq, onun təhlükəsiz və asan əldə edilə bilən olması vacibdir və burada məlumat bazaları işə düşür.

**Məlumat bazası** məlumatın daxil edilməsi, saxlanması, axtarışı, alınması və dəyişdirilməsi üçün nəzərdə tutulmuş məlumatlar və ya məlumatların toplusudur. **Məlumat bazası idarəetmə sistemi (DBMS)** məlumat bazasını yaradan və saxlayan proqramlar dəstəsidir. Bu, sorğu adlanan bir funksiyadan istifadə edərək məlumatı saxlamağa, dəyişdirməyə və çıxarmağa imkan verir. Məsələn, altı aydan çox aktiv olmayan müştəriləri tapmaq istəyirsinizsə, DBMS bu məlumatı məlumat bazasından çıxara bilər.

"Məlumat bazası" və "DBMS" terminləri fərqli olmasına baxmayaraq, onlar tez-tez bir-birinin əvəzinə istifadə edilir. Müxtəlif növ məlumat bazaları var və onların seçimlərinə məlumat növü və strukturu, sorğu mexanizmləri, gecikmə tələbləri, əməliyyat sürətləri və məlumatın nəzərdə tutulan istifadəsi kimi bir neçə amil təsir göstərir.

İki əsas məlumat bazası növü **əlaqəli** və **əlaqəsiz**dir:

1. **Əlaqəli Məlumat Bazaları (RDBMS)**: Bunlar məlumatları sətir və sütunlardan ibarət cədvəl formatında təşkil etmək prinsipləri əsasında qurulmuşdur və yaxşı müəyyən edilmiş struktur və sxemə malikdir. Düz fayllardan fərqli olaraq, RDBMS-lər çoxlu cədvəllər və böyük məlumat həcmləri üzrə mürəkkəb məlumat əməliyyatları və sorğular üçün optimallaşdırılmışdır. Əlaqəli məlumat bazaları üçün standart sorğu dili Structured Query Language (SQL) adlanır.

2. **Əlaqəsiz Məlumat Bazaları (NoSQL)**: "Not Only SQL" olaraq da bilinir, əlaqəsiz məlumat bazaları bulud hesablama, Əşyaların İnterneti -the Internet of Things (IoT) və sosial medianın yayılması ilə təsirlənən bu gün yaradılan məlumatların həcmi, müxtəlifliyi və sürətini idarə etmək üçün yaranmışdır. NoSQL məlumat bazaları sürət, elastiklik və miqyaslanma üçün qurulmuşdur və sxemsiz və ya sərbəst formalı məlumat saxlamağa imkan verir. Onlar struktursuz və yarı strukturlu məlumatları idarə etmək qabiliyyətlərinə görə böyük məlumatların işlənməsi üçün geniş istifadə olunur.

---------------------------------------------------------------------

### Əlaqəli Məlumat Bazaları (Relational Databases)

Əlaqəli məlumat bazası məlumatı cədvəl quruluşunda təşkil edir, burada cədvəllər ortaq məlumat elementləri əsasında əlaqələndirilə bilər. Bu cədvəllər sətir və sütunlardan ibarətdir, sətirlar qeydləri, sütunlar isə atributları təmsil edir. Məsələn, şirkətdə hər bir müştəri haqqında məlumatları saxlayan **Müştəri Cədvəli**ni nəzərdən keçirək. Sütunlara Müştəri ID, Müştəri Adı, Müştəri Ünvanı və Müştəri Əsas Telefonu daxil ola bilər və hər sətir müştəri qeydini təmsil edir.

Əlaqəli məlumat bazasındakı cədvəllər ortaq sahələr vasitəsilə əlaqələndirilə bilər. Məsələn, bir şirkət hər bir müştəri ilə bağlı əməliyyat məlumatlarını ehtiva edən **Əməliyyat Cədvəli**nə də malik ola bilər. Bu cədvəl Əməliyyat Tarixi, Müştəri ID, Əməliyyat Məbləği və Ödəniş Metodu kimi sütunları ehtiva edə bilər. **Müştəri Cədvəli** və **Əməliyyat Cədvəli** ortaq Müştəri ID sahəsi ilə əlaqələndirilə bilər, bu da xüsusi bir dövr ərzində bütün əməliyyatları ümumiləşdirən müştəri hesabatları kimi hərtərəfli hesabatlar hazırlamaq üçün sorğulara imkan verir.

Cədvəllərin ortaq məlumatlara əsaslanaraq əlaqələndirilə bilməsi əlaqəli məlumat bazalarının güclü xüsusiyyətidir. Bu, bir və ya daha çox cədvəldə mövcud məlumatlardan yeni cədvəllərin tək bir sorğu vasitəsilə çıxarılmasına, fikirlərin yaranmasına və daha yaxşı qərar verməyə dəstək olur. Əlaqəli məlumat bazaları **Structured Query Language (SQL)**-dən məlumatların sorğulanması üçün istifadə edir.

Əlaqəli məlumat bazaları, məlumatların yaxşı müəyyən edilmiş struktur və sxemə malik olan sətir və sütunlar şəklində təşkil edildiyi düz faylların, məsələn, elektron cədvəllərin təşkilat prinsiplərinə əsaslanır. Bununla belə, elektron cədvəllərdən fərqli olaraq, əlaqəli məlumat bazaları böyük məlumat həcmlərinin optimallaşdırılmış saxlanması, əldə edilməsi və emalı üçün nəzərdə tutulmuşdur. Əlaqəli məlumat bazasındakı hər bir cədvəlin unikal sətir və sütun dəsti var və cədvəllər arasındakı əlaqələr məlumatın təkrarlanmasını minimuma endirir.

Bundan əlavə, əlaqəli məlumat bazaları məlumat sahələrini xüsusi məlumat növləri və dəyərləri ilə məhdudlaşdırmaqla məlumatların uyğunluğunu və bütövlüyünü təmin edir. SQL milyonlarla qeydiyyatı emal etməyə və böyük miqdarda məlumatı tez bir zamanda çıxarmağa imkan verir. Əlaqəli məlumat bazalarının təhlükəsizlik arxitekturası məlumatlara nəzarətli giriş təmin edir və məlumatların idarəedilməsi standartlarına və siyasətlərinə uyğunluğu təmin edir.

Əlaqəli məlumat bazaları kiçik masaüstü sistemlərdən tutmuş geniş miqyaslı bulud əsaslı sistemlərə qədər müxtəlif formalarda ola bilər. Onlar açıq mənbəli və daxili dəstəklənən, açıq mənbəli kommersiya dəstəyi ilə və ya kommersiya qapalı mənbəli sistemlər ola bilər. Populyar əlaqəli məlumat bazalarına **IBM DB2, Microsoft SQL Server, MySQL, Oracle Database** və **PostgreSQL** daxildir. **Database-as-a-Service (DBaaS)** kimi tanınan bulud əsaslı əlaqəli məlumat bazaları, buludun məhdudiyyətsiz hesablama və saxlama imkanlarına çıxışına görə getdikcə daha çox populyarlaşır. Qeyd edilən bulud əlaqəli məlumat bazalarına **Amazon Relational Database Service (RDS), Google Cloud SQL, IBM DB2 on Cloud, Oracle Cloud** və **SQL Azure** daxildir.

Əlaqəli məlumat bazalarının bir neçə üstünlüyü var:

1. **Mənalı Məlumat Yaratma (Creating Meaningful Information)**: Cədvəlləri birləşdirmək qabiliyyəti mənalı məlumat yaratmağa imkan verir.
2. **Elastiklik (Flexibility)**: SQL yeni sütunlar, cədvəllər əlavə etməyə və digər dəyişikliklər etməyə imkan verir, məlumat bazası işlək vəziyyətdə olarkən belə.
3. **Redundantlığın Azaldılması (Reduced Redundancy)**: Məlumat redundantlığı minimuma endirilir, müştəri məlumatları Müştəri Cədvəlində bir dəfə saxlanılır və Əməliyyat Cədvəlində əlaqələndirilir.
4. **Ehtiyat Nüsxə və Fəlakətdən Qurtarma Asanlığı (Ease of Backup and Disaster Recovery)**: Əlaqəli məlumat bazaları asan ixrac və idxal variantlarını dəstəkləyir və bulud əsaslı sistemlərdə davamlı güzgüləmə təmin edir.
5. **ACID Uyğunluğu (ACID Compliance)**: Əlaqəli məlumat bazaları məlumatların dəqiqliyini və uyğunluğunu təmin edən **ACID (Atomicity, Consistency, Isolation, Durability)** prinsiplərinə əməl edir.

**Əlaqəli Məlumat Bazalarının İstifadə Halları**:
- **Online Transaction Processing (OLTP)**: Əməliyyat yönümlü tapşırıqlar üçün yaxşı uyğun gəlir, çox sayda istifadəçi və tez-tez sorğular və yeniləmələrə uyğun gəlir.
- **Data Warehouses**: Biznes zəkası üçün tarixi məlumatları təhlil edən **Online Analytical Processing (OLAP)** üçün optimallaşdırılmışdır.
- **IoT Həlləri**: Sürət və kənar cihazlardan məlumat toplama və emal etmə qabiliyyəti tələb edir.

**RDBMS-in Məhdudiyyətləri**:
- Yarı-strukturlaşdırılmış və ya strukturlaşdırılmamış məlumatlar üçün uyğun deyil.
- RDBMS arasında köçürmə üçün eyni sxemlər və məlumat növləri tələb edir.
- Məhdud məlumat sahəsinin uzunluğu məlumatların saxlanmasını məhdudlaşdıra bilər.

Bu məhdudiyyətlərə baxmayaraq, əlaqəli məlumat bazaları böyük məlumatlar, bulud hesablama, IoT cihazları və sosial medianın dövründə strukturlaşdırılmış məlumatlar üçün dominant texnologiya olaraq qalır.

---------------------------------------------------------------------------------

### Əlaqəli Məlumat Konsepsiyaları (Relational Data Concepts)

Əlaqəli model məlumat bazaları üçün ən çox istifadə olunan məlumat modelidir, çünki bu, məlumat müstəqilliyinə imkan verir. Məlumatlar sadə quruluşda, yəni cədvəllərdə saxlanılır ki, bu da məntiqi, fiziki və saxlama müstəqilliyini təmin edir. Əlaqəli məlumat modelinə alternativ olaraq, model-əlaqə (ER entity-relationship) məlumat modeli istifadə olunur.

Sadələşdirilmiş kitabxana məlumat bazası nümunəsini istifadə edərək, model-əlaqə diaqramı (ERD) modellərı (cədvəlləri) və onların əlaqələrini təmsil edə bilər. Kitabxana nümunəsində kitablar var. Kitab bir və ya bir çox müəllif tərəfindən yazıla bilər. Kitabxana bir və ya bir çox kitab nüsxəsinə sahib ola bilər və hər bir nüsxə eyni vaxtda yalnız bir borcalan tərəfindən borc götürülə bilər.

ER modeli məlumat bazasını müstəqil model kimi istifadə etməkdən çox, modellər toplusu kimi görməyi təklif edir. Əlaqəli məlumat bazalarını dizayn etmək üçün vasitə kimi istifadə olunur. ER modelində modellər məlumat bazasındakı digər modellərdən müstəqil olaraq mövcud olan obyektlərdir. ER diaqramının quruluş elementləri modellər və atributlardır.

Model adətən isim olur: şəxs, yer və ya əşya. ER diaqramında model düzbucaqlı olaraq təsvir edilir. Modellərin atributları olur, yəni modeli xarakterizə edən və onun haqqında daha çox məlumat verən məlumat elementləri. ER diaqramında atributlar oval şəkilində təsvir edilir.

Sadələşdirilmiş kitabxana nümunəsini istifadə edərək, "kitab" modeldir. Kitab modelinin atributlarına kitab adı, nəşr və nəşr ili daxil ola bilər. Atributlar tam olaraq bir modelə bağlıdır. Kitab modeli məlumat bazasında cədvəl olduqda, atributlar cədvəlin sütunları olur. Cədvəl sətirlər və sütunların birləşməsindən ibarətdir və xəritələşdirmə zamanı model cədvələ çevrilir, lakin hələ də sətir və sütunlar şəklini almır. Atributlar sütunlara çevrilir və sonradan hər sütuna məlumat dəyərləri əlavə edilir, beləliklə cədvəl forması tamamlanır.

Hər bir atribut müxtəlif formatlarda məlumat dəyərləri saxlayır, məsələn, simvollar, rəqəmlər, tarixlər və valyuta. Kitab cədvəli nümunəsində, başlıq simvollardan ibarət ola bilər və dəyişkən simvol məlumat növü olaraq təyin edilir: Varchar. Uzunluğu dəyişməyən simvol sütunları üçün Char istifadə olunur. Nəşr və il sütunları rəqəmlər olardı, ISBN sütunu isə rəqəmlərlə yanaşı tirelər də ehtiva etdiyinə görə Char ola bilər.

Kitab modeli xəritələşdirmə nümunəsini istifadə edərək, müəllif, müəllif siyahısı, borcalan, borc və nüsxə kimi model adlarından istifadə edərək sadələşdirilmiş kitabxana nümunəmiz üçün cədvəllər yarada bilərik. Model atributları bu cədvəllərin sütunları olacaq. Hər cədvələ təkrarları qarşısını alan və cədvəllər arasında əlaqələri müəyyən edən, hər bir sətiri unikal olaraq müəyyən edən əsas açar təyin olunur. Cədvəllər həmçinin digər cədvəllərdə müəyyən edilən əsas açarları olan xarici açarları da ehtiva edə bilər ki, bu da cədvəllər arasında əlaqələri yaradır.

Əlaqəli modelin əsas üstünlüyü məntiqi, fiziki məlumat müstəqilliyi və saxlama müstəqilliyidir. Modellər çoxsaylı xüsusiyyətlərə malik müstəqil obyektlərdir. Əlaqəli məlumat bazasına xəritələşdirərkən modellər cədvəl kimi təmsil olunur və atributlar sütunlara xəritələnir. Ümumi məlumat növlərinə Char və Varchar kimi simvollar, tam ədədlər və onluq kimi rəqəmlər və tarix və vaxtı əhatə edən vaxt möhürləri daxildir. Əsas açar cədvəldə xüsusi bir sətiri unikal olaraq müəyyən edir və məlumatın təkrar olunmasının qarşısını alır.

--------------------------------------------------------------------------