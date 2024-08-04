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

