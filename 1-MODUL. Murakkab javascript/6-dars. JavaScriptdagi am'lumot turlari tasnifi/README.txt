JAVASCRIPT. MA'LUMOTLAR TURLARI VA OPERATORLARI. JAVASCRIPT MA'LUMOTLAR TURLARI O'ZGARUVCHILAR TURINI O'RNATADI
O'zgaruvchi - bu nomli xotira bo'lagi bo'lib, unda siz ba'zi ma'lumotlarni saqlashingiz va undan olishingiz mumkin.

O'zgaruvchilar var kalit so'zi yordamida e'lon qilinadi (yaratiladi).

// xabar - o'zgaruvchining nomi var message;

O'zgaruvchini yaratganingizda, darhol unga qiymat belgilashingiz mumkin.

O'zgaruvchiga qiymat "=" operatori yordamida beriladi.

// masalan, o'zgarmaydigan elektron pochta yarating va qatorni tayinlang " no-reply@astr.org"var email =" no-reply@astr.org"; // elektron pochta o'zgaruvchisini yangi qiymatga o'rnating email = " support@astr.org";

O'zgaruvchining qiymatini olish uchun siz unga faqat nom bilan murojaat qilishingiz kerak.

// masalan, elektron pochta o'zgaruvchisining qiymatini brauzer konsoliga chop eting: console.log (elektron pochta);

Bitta var kalit so'zi bilan bir nechta o'zgaruvchilarni e'lon qilish uchun vergul qo'yish kerak.

Var narxi = 78,55, miqdori = 10, xabar;

JavaScript dinamik yoki zaif terilgan tildir. Bu shuni anglatadiki, o'zgaruvchini e'lon qilishda u qabul qilishi mumkin bo'lgan ma'lumotlar turini ko'rsatish shart emas. Shuning uchun, o'zgaruvchiga birinchi navbatda bitta ma'lumot turiga ega bo'lgan qiymatni, keyin esa boshqasini qo'yishingiz mumkin.

Var chiqishi = "muvaffaqiyat"; // o'zgaruvchida qator ma'lumotlar turi bor chiqdi = 28; // bir xil o'zgaruvchi, lekin allaqachon "raqam" ma'lumotlar turiga ega chiqdi = true; // bir xil o'zgaruvchi, lekin allaqachon mantiqiy qiymatni saqlaydi

O'zgaruvchining qiymati cheksiz ko'p marta o'zgartirilishi mumkin.

// yaratilgan o'zgaruvchan yosh var age; // o'zgaruvchan yoshga 67 yosh = 67 qiymati beriladi; // o'zgaruvchan yosh "Pensiya yoshi" ga o'rnatiladi age = "Pensiya yoshi"; // o'zgaruvchan yosh 55 yoshga o'rnatiladi = 55;

Mijoz tomonini ishlab chiqishda ma'lum bir o'zgaruvchida faqat bitta ma'lumot turidan foydalanish yaxshi amaliyotdir, ya'ni. o'zgaruvchiga har xil turdagi ma'lumotlarning qiymatlarini yozmang. O'zgaruvchida qanday turdagi ma'lumotlarni kutish kerakligini tushunish uchun o'zgaruvchini yaratishda uni ma'lum bir qiymat bilan ishga tushirish tavsiya etiladi.

O'zgaruvchining nomi harflar, raqamlar va $ va _ belgilaridan iborat bo'lishi mumkin. Bunday holda, o'zgaruvchining birinchi belgisi raqam bo'lmasligi kerak. Bundan tashqari, ajratilgan so'zlarni o'zgaruvchi nomi sifatida ishlatib bo'lmaydi.

// ikkita o'zgaruvchi yarating, birinchi o'zgaruvchi telefon deb nomlanadi, ikkinchisi o'lchov; telefon, xabar;

O'zgaruvchan nomdagi harflarning holati muhim ahamiyatga ega. Ya'ni, masalan, o'zgaruvchan telefon va Telefon ikki xil o'zgaruvchidir.

Agar qat'iy rejim ishlatilmasa, siz var kalit so'zisiz asl qiymatga ega o'zgaruvchi yaratishingiz mumkin.

Narxi = 250,00; // o'zgaruvchi yarating va uni 250,00 foiz bilan ishga tushiring = "20%"; // o'zgaruvchi yarating va uni "20%" qatori bilan ishga tushiring

Lekin o'zgaruvchilarni bu tarzda yaratish tavsiya etilmaydi.

Ma'lumotlar turlari
JavaScript-da ma'lumotlar turlarini ibtidoiy va ob'ekt turlariga bo'lish mumkin.

Primitiv ma'lumotlar turlarini o'z ichiga olgan o'zgaruvchilar qiymatni aniq saqlaydi.

JavaScript-da 5 ta ibtidoiy ma'lumotlar turlari ajralib turadi:

raqam (raqam);
qator (tor);
mantiqiy turi (boolean);
null;
aniqlanmagan.
Agar bitta o'zgaruvchiga ibtidoiy ma'lumotlar turini o'z ichiga olgan boshqasiga qiymat berilgan bo'lsa, u holda u ushbu qiymatning o'z nusxasini oladi.

Var x = 77, y = x; x = 55; y; // 77

Ob'ektni o'z ichiga olgan o'zgaruvchilar aslida ob'ektning o'zini emas, balki unga havolani saqlaydi.

Ob'ektni o'z ichiga olgan boshqa bir o'zgaruvchiga qiymat belgilasangiz (unga havola), u ham unga havolani oladi. Ushbu operatsiya natijasida bu ikki o'zgaruvchi bir xil ob'ektga havolani o'z ichiga oladi.

// 1-misol ("ob'ekt" ma'lumotlar turi bilan) var koord1 = (x: 77, y: 100), koord2 = koord1; koordinat1.x = 55; // ob'ektning x xossasini yangi qiymatga o'rnatish coord2.x; // 55, chunki coord1 va coord2 bir xil ob'ektga havolani o'z ichiga oladi // 2-misol (ma'lumotlar turi "massiv" bilan) var coord1 =, koord2 = koord1; kord1 = 55; // 0 indeksli elementni yangi qiymatga o'rnating coord2; // 55, chunki coord1 va coord2 bir xil ob'ektga havolani o'z ichiga oladi // 3-misol (ma'lumotlar turi "sana" bilan) var date1 = new Date (2018,00,01), date2 = date1; date2 = date2.setDate (date2.getDate () + 7); // sanani 7 kunga oshirish sana1; // 01/07/2018, chunki sana1 va sana2 bir xil ob'ektga havolani o'z ichiga oladi

Raqam
JavaScript ma'lumotlaridagi son turi umumiydir. U butun va kasr sonlarni ifodalash uchun ishlatiladi.

Var int = 5; // integer var float = 5,98; // kasr son

JavaScript-da raqamlarni ifodalash formati IEEE 754-2008 standartiga muvofiq amalga oshiriladi.

JavaScript-da butun sonlar nafaqat o'nlik kasr tizimida, balki sakkizta (0) yoki o'n oltilik sanoq tizimi (0x) Qavslar ichida berilgan prefikslar yordamida:

Var int = 010; // 8 int = 055; // 45 int = 0xFF; // 255 int = 0xB8; // 184

Raqamlarni yozish mumkin eksponentsial:

Var soni = 2e3; // 2 * 10 ^ 3 sonining eksponensial belgisi (2000) num = 2e-3; // 2 sonining eksponensial belgisi * 10 ^ -3 (0,002) num = 3,2e3; // 3200 num = 1,5e-2; // 0,015

Raqamli ma'lumotlar turi raqamlardan tashqari o'z ichiga oladi maxsus raqamli qiymatlar:

Cheksizlik (ijobiy cheksizlik);
-Infinity (salbiy cheksizlik);
NaN (Raqam emas).
Maxsus qiymat Infinity juda katta ijobiy raqamni bildiradi, ya'ni. JavaScript-da ifodalab bo'lmaydigan raqam, chunki u juda katta.

Maxsus qiymatlar -Infinity, aksincha, juda katta manfiy sonni anglatadi, ya'ni. JavaScript bilan ifodalab bo'lmaydigan raqam, chunki u ham juda katta.

Hisoblash natijasida bo'ladigan ifodalarga misol maxsus raqamli qiymatlar qaytarildi:

5/0; // Infinity -5/0; // -Infinity Math.pow (10,399); // Infinity (10 dan 399 gacha) Math.pow (10.399); // -Infinity (-10 dan 399 gacha)

NaN qiymati JavaScript hisoblay olmaydigan matematik amallarni bajarish natijasida qaytariladi.

5 - "Salom"; // NaN (5-raqamdan chiziqni olib tashlang) 1000 / "20px"; // NaN (satrga bo'lingan raqam) true * "1rem"; // NaN (mantiqiy haqiqiy satrga ko'paytirish)

Aytgancha, juda qiziq narsa shundaki, JavaScript-dagi NaN qiymati hech narsaga, shu jumladan o'ziga teng emas.

NaN == NaN; // noto'g'ri NaN === NaN; // yolg'on

Mantiqiy ma'lumotlar turi
Mantiqiy - bu faqat ikkita qiymatga ega bo'lgan ibtidoiy ma'lumotlar turi: rost va noto'g'ri.

Var a = rost; var b = noto'g'ri;

String
String - bu JavaScript matnni ifodalash uchun foydalanadigan ma'lumotlar turi.

JavaScript satri 0 yoki bo'lishi mumkin Ko'proq belgilar.

JavaScript har doim string formati sifatida Unicode kodlashdan foydalanadi.

Satrni yaratish (string literal) tomonidan amalga oshiriladi matnni yakka yoki qo'sh tirnoq .

"JavaScript"; "ECMAScript";

JavaScript-da bitta va ikkita tirnoq o'rtasida farq yo'q.

Ammo, ba'zi hollarda, qo'sh tirnoq emas, balki faqat bitta tirnoqdan foydalanish mantiqan to'g'ri keladi va aksincha.

Misol uchun, satrda qo'sh tirnoq bo'lsa, uni bitta tirnoq ichiga olish qulayroqdir. Bu undagi qo'sh tirnoqlardan qochish zaruratini yo'q qiladi.

"" ECMAScript ""; // qochish yo'q (bitta tirnoq yordamida) "\" ECMAScript \ ""; // qochish bilan

JavaScript qatori maxsus belgilarni o'z ichiga olishi mumkin. Masalan, \ n (satr uzatish), \ t (tab), \ r (karetaning qaytishi) va boshqalar.

"Bu taklif. \ NA Bu ham taklif, lekin u yangi qatordan boshlanadi.";

Satrlar yordamida siz qo'shish (birlashma) amalini yoki boshqacha aytganda, birlashtirishni bajarishingiz mumkin. Buning uchun "+" operatori ishlatiladi. Ushbu operatsiyaning g'oyasi ikkinchi qatorni birinchisining oxiriga qo'shishdir.

"Men sevaman" + "JavaScript"; // Men JavaScript-ni yaxshi ko'raman

Qiymat "aniqlanmagan"
undefined - bu aniqlanmaganga teng bitta qiymatga ega bo'lgan maxsus ibtidoiy ma'lumotlar turi.

Ushbu ma'lumotlar turi e'lon qilingan o'zgaruvchiga ega bo'lib, unga hali qiymat berilmagan.

Var raqami; // aniqlanmagan

Mavjud bo'lmagan ob'ekt xususiyatiga kirishda aniqlanmagan qiymat ham qaytariladi.

Var obj = (); // bo'sh ob'ekt obj.prop; // aniqlanmagan

"null" qiymati
null - null ga teng bitta qiymatga ega bo'lgan maxsus ibtidoiy ma'lumotlar turi.

null faqat "hech narsa" yoki "noma'lum qiymat" ma'nosiga ega bo'lgan maxsus qiymatdir, ya'ni. bu hech narsani anglatmaydi.

Ob'ekt
Ob'ekt nom-qiymat juftliklaridan tashkil topgan ma'lumotlar strukturasidir.

Ob'ektning literal belgisi yordamida ob'ekt yaratish quyidagicha amalga oshiriladi:

(ism_1: qiymat_1, ism_2: qiymat_2, nom_3: qiymat_3, ...)

Ko'rib turganingizdek, nom qiymatdan ikki nuqta bilan, juftliklar esa vergul bilan ajratilgan.

Bundan tashqari, agar funktsiya juftlikning qiymati sifatida harakat qilsa, u holda bu ob'ektning usuli deyiladi. Boshqa barcha juftliklar, ya'ni. qiymat sifatida funksiya ishlatilmaydigan juftliklar obyekt xossalari deyiladi.

Boshqacha qilib aytganda, ob'ekt - bu xususiyatlar va usullardan tashkil topgan ma'lumotlar strukturasi.

Var shaxs = (ism: "Vitaliy", yosh: 27, getAge: funktsiya () ("Yosh:" + this.age;ni qaytaring))

Obyekt xususiyatlariga nuqta yoki qavs yordamida kirish mumkin.

// brauzer konsoliga age xususiyati qiymatini chop etish // 1 usul (nuqta orqali) console.log (person.age); // 2-yo'l (qavslar yordamida) console.log (shaxs ["yosh"]); // getAge usulini chaqirish; qaytaradigan qiymat console.log (person.getAge ()) da chop etiladi;

Operator turi
Typeof operatori ifodaning ma'lumotlar turi haqidagi ma'lumotni satr sifatida olish uchun ishlatiladi.

typeof operatorining sintaksisi (qavssiz variant):

Ifoda turi

typeof operatorining sintaksisi (qavslar yordamida):

Turi (ifoda)

Var nomi, yosh = 37, email = " v3@gmail.com", isLicense = rost, qiziqish: null, lastExperience: (davr:" 2011 yil iyun - 2018 yil iyun ", joy:" ISACA, Moskva ", pozitsiya:" Veb dizayner "), getExperience: funktsiya () ( lastExperience.periodni qaytarish + "(" + lastExperience.position + "-" + lastExperience.place + ")";); nom turi; // "aniqlanmagan" yosh turi; // Litsenziyaning "raqami" turi; // "boolean" qiziqish turi; / / "object" (1) typeof lastExperience; // "object" typeof getExperience; // "funktsiya" (2) / * (1) - bu tilda birinchi amalga oshirilganidan beri mavjud bo'lgan xato; u hali ham mavjud emas. muvofiqlikni saqlash uchun o'rnatildi va skriptlarni yozishda buni hisobga olish kerak; null - ibtidoiy ma'lumotlar turi, u ob'ekt emas * / / * (2) - typeof operatori funktsiyalarni alohida ajratishi juda qulay; lekin JavaScipt-dagi funksiya ham ob'ektdir; agar siz quyidagi konstruktsiyani bajarsangiz, buni osongina tekshirishingiz mumkin: * / typeof getExperience .__ proto __.__ proto__ // "ob'ekt" (funktsiya prototipi ob'ektdir)

Doimiylar
ECMAScript 6 ning chiqarilishi bilan konstantalarni yaratish mumkin bo'ldi. Bu const kalit so'zi yordamida amalga oshiriladi.

Const COLOR_RED = "# ff0000";

Doimiy o'zgaruvchidir, uning qiymati o'zgartirishdan himoyalangan. Bular. qiymatni o'zgartirishga urinayotganda xatolik yuzaga keladi.

Const COLOR_RED = "# ff0000"; COLOR_RED = "# f44336"; // Tugallanmagan TypeError: Doimiy o'zgaruvchiga tayinlash.

Agar, masalan, konstanta ob'ektni o'z ichiga olsa, uni o'zgartirish mumkin emas, aniqrog'i unga havola. Ammo bu ob'ektning xususiyatlarini o'zgartirish mumkin.

Const COLORS = (qizil: "# ff0000", yashil: "# 00ff00", ko'k: "# 00ff00") COLORS = ["# ff0000", "# 00ff00", "# 00ff00"]; // Tugallanmagan TypeError: Doimiy o'zgaruvchiga tayinlash. COLORS.green = "# 4caf50";

Ma'lumotlar turlari dasturlash tillarida ma'lumotlar tasnifini yaratishga yordam beradi. Misol uchun, raqam va belgilar qatori JavaScript turlicha ishlov beradigan turli xil ma'lumotlar turlaridir.

Bu juda muhim, chunki har bir ma'lumot turi ma'lum qiymatlarni olishi va muayyan harakatlarni bajarishi mumkin. JavaScript-da o'zgaruvchilar ustida operatsiyalarni bajarish uchun siz ko'rsatgan har bir o'zgaruvchining ma'lumotlar turini tushunish muhimdir.

Ushbu qo'llanma sizni JavaScript ma'lumotlar turlari bilan tanishtiradi.

Eslatma: Qoʻllanmadagi maʼlumotlar toʻliq emas, lekin bu yerda asosiy JavaScript opsiyalari bilan tanishishingiz mumkin.

Dinamik yozish
JavaScript dinamik tildir. Bu shuni anglatadiki, ma'lumotlar turini tekshirish kompilyatsiya emas, balki ishga tushirishda amalga oshiriladi.

Dinamik tillarda bir xil nomdagi o'zgaruvchilar har xil turdagi ma'lumotlarni saqlash uchun ishlatilishi mumkin.

Masalan, var kalit so'zi bilan aniqlangan t o'zgaruvchisi har xil turdagi ma'lumotlarni saqlashi mumkin; u ham ishga tushirilishi mumkin, lekin aniqlanmagan:

var t = 16; // t - son
var t = "Tereza"; // t - satr
var t = rost; // t - mantiqiy
var t; // t aniqlanmagan

Barcha t o'zgaruvchilari turli xil JavaScript ma'lumotlar turlarini o'z ichiga oladi. JavaScript-da siz o'zgaruvchini ishlatishdan oldin uning ma'lumotlar turini aniq belgilashingiz shart emas.

Raqamlar
JavaScript butun sonlar va suzuvchi nuqta raqamlarini ajratmasdan bitta raqamli ma'lumotlar turiga ega. Shuning uchun JavaScript-da raqamlar kasrli yoki kasrsiz yozilishi mumkin:

var num1 = 93;
var num2 = 93,00;

Yuqoridagi misolda ikkala o'zgaruvchida vergul bormi yoki yo'qmi, raqamlar mavjud.

JavaScript-ning eksponensial belgisi juda katta yoki kichik raqamlarni qisqartirish imkonini beradi:

var num3 = 987e8; // 98700000000
var num4 = 987e-8; // 0,00000987

JavaScript-da raqamlar 15 ta raqamgacha aniq hisoblanadi. Bu degani, 16-raqamga yetgandan so'ng, raqamlar yaxlitlanadi:

var num5 = 999999999999999; // 999999999999999 sifatida qoladi
var num6 = 9999999999999999; // 10000000000000000 gacha yaxlitlangan

Shuningdek, JavaScript-dagi raqamlar uchta ramziy ma'noga ega:

Infinity - cheksizlikka yaqinlashadigan ijobiy son bo'lgan raqamli qiymat.

Infinity - cheksizlikka yaqinlashadigan salbiy son bo'lgan raqamli qiymat.

NaN - No-a-Number, suzuvchi nuqtali raqamning maxsus holati.

Infinity va -Infinity JavaScript-da mavjud bo'lgan maksimal mumkin bo'lgan sondan tashqaridagi sonni hisoblashda qaytariladi. Ular, shuningdek, aniqlanmagan qiymatlarni hisoblashda, masalan, nolga bo'lishda paydo bo'ladi:

var num7 = 5/0; // Cheksizlik
var num8 = -5 / 0; // -Cheksizlik

Texnik jihatdan, agar raqam JavaScript-ning yuqori chegarasi bo'lgan 1,797693134862315E + 308 dan katta bo'lsa, Infinity qaytariladi.

Xuddi shunday, raqam pastki chegaradan chiqib ketganda -Infinity ko'rsatiladi, -1,797693134862316E + 308.

Infinity raqamini tsikllarda ham ishlatish mumkin:

while (num9! = Infinity) (
// Bu yerda kod num9 = Infinity orqali bajariladi
}

Aniqlanmagan raqamlar uchun NaN chiqadi. Agar siz raqam va noaniq qiymat ustida matematik amalni bajarishga harakat qilsangiz, NaN olasiz. Masalan:

var x = 20 / "Shark"; // x NaN bo'ladi

20 ni Shark qatoriga bo'lish mumkin emasligi sababli, x ning qiymati NaN bo'ladi.

Biroq, agar qatorni raqamli qiymat sifatida baholash mumkin bo'lsa, JavaScript matematik ifodani bajaradi:

var y = 20 / "5"; // y 4 bo'ladi

JavaScript 5 ni raqamli qiymat sifatida ko'rib chiqishi mumkinligi sababli, 5 matematik bo'linish operatori bilan ishlaydi.

Agar ifodadagi bitta o'zgaruvchiga NaN qiymati berilgan bo'lsa, ikkinchi operand raqam bo'lsa ham, natija NaN bo'ladi.

var a = NaN;
var b = 37;
var c = a + b; // c NaN bo'ladi

Shunday qilib, JavaScript-da faqat bitta raqamli ma'lumotlar turi mavjud. JavaScript-da butun sonlar va suzuvchi nuqta raqamlarini ajratish shart emas, chunki JavaScript dinamik tildir.

Satrlar
Satr - bu bir yoki bir nechta belgilar (harflar, raqamlar va boshqa belgilar) ketma-ketligi. Satrlar matnli ma'lumotlardir.

JavaScript-da satrlar bitta va ikkita tirnoq ichida keladi. Satr yaratish uchun siz qo'shtirnoq ichiga belgilar ketma-ketligini kiritishingiz kerak:

var singleQuotes = "Bu bitta qo'shtirnoq ichidagi satr.";
var doubleQuotes = "Bu ikki tirnoq ichidagi satr.";

Siz bitta yoki ikkita tirnoqdan foydalanishingiz mumkin, lekin bitta dasturning kodida siz ketma-ket bir turdagi tirnoqlardan foydalanishingiz kerak.

Salom Dunyo! kompyuter dasturlashda satrlar qanday ishlatilishini ko'rsatadi. Aslida, in bu misol satr – “Salom, dunyo!” iborasini tashkil etuvchi belgilar ketma-ketligi. ogohlantirishda ().







Meni bosing



Kodni ishga tushirish va "Meni bosing" tugmasini bosish orqali siz matnli qalqib chiquvchi oynani ko'rasiz:

Boshqa ma'lumotlar turlari singari, satrlar ham o'zgaruvchilarda saqlanishi mumkin.

var hw = "Salom, Dunyo!";

Keyin o'zgaruvchini chaqirish orqali satrni ko'rsatishingiz mumkin:

...

...
Salom Dunyo!

Stringlar ma'lumotlarni foydalanuvchiga uzatish va dasturga qaytarish imkonini beradi.

Mantiqiy ma'lumotlar turi
Mantiqiy (yoki mantiqiy) ma'lumotlar turi ikkita qiymatdan iborat, haqiqiy va noto'g'ri.

Ushbu tur informatika fanida mantiq va algoritmlar bilan bog'liq bo'lgan haqiqat qiymatlarini ifodalash uchun ishlatiladi.

Eslatma: Ushbu ma'lumotlar turi matematik Jorj Bul sharafiga nomlangan.

Matematikadagi ko'plab operatsiyalar to'g'ri yoki noto'g'ri deb baholanishi mumkin bo'lgan natijalarni keltirib chiqaradi:

Bundan ko'proq:

500> 100 rost
1>5 noto'g'ri
Dan kichik; .. dan kamroq:

200 < 400 true
4 < 2 false
5 = 5 rost
500 = 400 noto'g'ri
Boshqa turlar singari, mantiqiy ma'lumotlar turlari ham o'zgaruvchilarda saqlanishi mumkin.

var myBool = 5> 8; // yolg'on

5 8 dan ko'p bo'lmagani uchun myBool noto'g'ri bo'ladi.

JavaScript-da kodlash jarayonida siz mantiqiy ma'lumotlar qanday ishlashini va haqiqatni baholovchi turli funktsiyalar va operatsiyalar dastur oqimini qanday o'zgartirishi mumkinligini bilib olasiz.

Massivlar
Massiv bitta o'zgaruvchida bir nechta qiymatlarni o'z ichiga olishi mumkin. Bu shuni anglatadiki, siz qiymatlar ro'yxatini massiv ichida saqlashingiz va ularni takrorlashingiz mumkin.

Massivdagi har bir qiymat element deb ataladi. Indeks yordamida massiv elementlariga murojaat qilishingiz mumkin.

Massivlar kvadrat qavslar bilan belgilanadi.

Satrlar massivi quyidagicha ko'rinadi:

var fish = ["akula", "krevetka", "masxaraboz", "ilan balig'i"];

O'zgaruvchan baliqni chaqirib, siz natijaga erishasiz:

["akula", "katta baliq", "masxaraboz", "ilan balig'i"]

Massivlar juda moslashuvchan ma'lumotlar turidir, chunki ular o'zgaruvchan: siz elementlarning qiymatlarini qo'shishingiz, olib tashlashingiz va o'zgartirishingiz mumkin.

Ob'ektlar
JavaScript-dagi obyekt kalitlardan iborat: qiymat juftlari.

Obyekt sintaksisi kalitlardan iborat: qiymat juftlari. Ob'ekt ikki tomondan jingalak qavslar ichiga olingan (()).

Ob'ektdagi juftliklar bo'shliqlar bilan ajratiladi:

var sammy = (ismi: "Wally", familiyasi: "Shark", rangi: "ko'k", joylashuvi: "okean");

Bundan tashqari, ob'ekt bir necha qatorda yozilishi mumkin (bu ayniqsa katta ob'ektlarga tegishli).

var Wally = (
ismingiz: "Wally",
familiyasi: "Shark",
rang: "ko'k",
Manzil: "Okean"
};

Bir nechta ma'lumotlar turlari bilan ishlash
Siz yaratgan har bir dastur bir necha turdagi ma'lumotlarni o'z ichiga olishi mumkin, ammo operatsiyalar odatda bitta turdagi ma'lumotlarda amalga oshiriladi. raqamlarga matematika, satrlarga esa kesish qo'llaniladi.

Barcha ma'lumotlar turlarida ishlaydigan operatorlardan foydalanish (masalan, + operatori raqamlar qo'shishi yoki qatorlarni birlashtirishni amalga oshirishi mumkin), siz kutilmagan natijalarga erishishingiz mumkin.

Agar siz birlashtirish uchun o'zgaruvchi yaratsangiz, JavaScript har bir elementni satr sifatida izohlaydi.

var o = "Okean" + 5 + 3;

O o'zgaruvchini chaqirish orqali siz quyidagi natijaga erishasiz:

Biroq, agar satr avval raqamlar bilan, keyin esa satr bilan kelsa, + operatori qo'shish va keyin birlashtirishni amalga oshiradi:

var p = 5 + 3 + "Okean";
8Okean

Natijalarning oldindan aytib bo'lmaydiganligi sababli, bir xil turdagi ma'lumotlarda operatsiyalar va usullarni bajarish qulayroqdir. Biroq, JavaScript, ba'zi boshqa dasturlash tillarida bo'lgani kabi, ma'lumotlar turlarini aralashtirishda xatolarni qaytarmaydi.

Xulosa
Endi siz JavaScript ma'lumotlar turlari bilan tanishsiz. Bu yerda keltirilgan turlarning har biri JavaScript dasturlarini yozishda muhim ahamiyatga ega.

Teglar: O'zgaruvchi - bu qiymat berilgan identifikator. O'zgaruvchiga dasturda kirish mumkin, unga tayinlangan qiymat bilan shu tarzda ishlaydi.
O'z-o'zidan, JavaScript o'zgaruvchisi unda saqlanadigan qiymatlar turi haqida ma'lumotni o'z ichiga olmaydi. Bu shuni anglatadiki, o'zgaruvchiga, masalan, satrga yozish orqali siz keyinchalik unga raqam yozishingiz mumkin. Bunday operatsiya dasturda xatolikka olib kelmaydi. Shuning uchun JavaScript ba'zan "tiplanmagan" til deb ataladi.

O'zgaruvchidan foydalanishdan oldin uni var yoki let kalit so'zi yordamida e'lon qilish kerak. Konstanta haqida gap ketganda, const kalit so'zi ishlatiladi. Siz ushbu kalit so'zlardan foydalanmasdan o'zgaruvchini e'lon qilishingiz va unga qiymat belgilashingiz mumkin, ammo bu tavsiya etilmaydi.

▍Var kalit so'zi
ES2015 dan oldin var kalit so'zidan foydalanilgan yagona yo'l o'zgaruvchan deklaratsiyalar.
Var a = 0
Agar bu konstruktsiyada var o'tkazib yuborilsa, qiymat e'lon qilinmagan o'zgaruvchiga tayinlanadi. Ushbu operatsiyaning natijasi dasturning qaysi rejimda bajarilishiga bog'liq.

Shunday qilib, agar qattiq rejim yoqilgan bo'lsa, bu xatolikka olib keladi. Agar qat'iy rejim yoqilmagan bo'lsa, o'zgaruvchi bilvosita e'lon qilinadi va global ob'ektga tayinlanadi. Xususan, bu funktsiyada shu tarzda bilvosita e'lon qilingan o'zgaruvchi funktsiya o'z ishini tugatgandan so'ng mavjud bo'lishini anglatadi. Odatda, funktsiyalarda e'lon qilingan o'zgaruvchilar o'z chegaralaridan "ketmasligi" kutiladi. Bu shunday ko'rinadi:

Funktsiya notVar () (bNotVar = 1 // buni qilmaslik yaxshiroq) notVar () console.log (bNotVar)
Konsol 1 ball oladi, odatda dasturdan bunday xatti-harakatni hech kim kutmaydi, bNotVar = 1 ifodasi o'zgaruvchini e'lon qilish va ishga tushirishga urinish emas, balki funksiya doirasidan tashqarida bo'lgan o'zgaruvchiga kirishga urinish sifatida ko'rinadi ( bu juda normal). Natijada, yashirin o'zgaruvchan deklaratsiyalar o'quvchini chalkashtirib yuboradi va dasturning kutilmagan xatti-harakatlariga olib kelishi mumkin. Biz funksiyalar va qamrovlar haqida keyinroq gaplashamiz, ammo hozircha ifodaning ma’nosi o‘zgaruvchini e’lon qilish bo‘lsa, maxsus kalit so‘zlardan foydalanishga harakat qiling. Agar ushbu misolda funksiyaning tanasi var bNotVar = 1 shaklida qayta yozilsa, yuqoridagi kod parchasini ishga tushirishga urinish xato xabariga olib keladi (uni brauzer konsolida ko'rishingiz mumkin).

Misol uchun, u quyidagicha ko'rinishi mumkin: Tugallanmagan ReferenceError: bNotVar aniqlanmagan. Uning ma'nosi dastur mavjud bo'lmagan o'zgaruvchi bilan ishlay olmasligi bilan bog'liq. Kutilmaganda o'zini tutishi mumkin bo'lgan tushunarsiz kod yozishdan ko'ra, dasturni birinchi marta ishga tushirganingizda bunday xato xabarini ko'rish yaxshiroqdir.

Agar o'zgaruvchini e'lon qilishda u ishga tushirilmasa yoki hech qanday qiymat berilmasa, unga avtomatik ravishda aniqlanmagan qiymat beriladi.

Var a // typeof a === "aniqlanmagan"
var kalit so'zi bilan e'lon qilingan o'zgaruvchilar ko'p marta qayta e'lon qilinishi mumkin, ularga yangi qiymatlar tayinlanadi (lekin bu o'quvchini chalkashtirib yuborishi mumkin).

Var a = 1 var a = 2
Bitta ifodada bir nechta o'zgaruvchilar e'lon qilinishi mumkin:

Var a = 1, b = 2
O'zgaruvchining qamrovi - bu o'zgaruvchi mavjud bo'lgan (ko'rinadigan) dastur maydoni.

Funksiyadan tashqarida var kalit soʻzi bilan ishga tushirilgan oʻzgaruvchi global obyektga tayinlanadi. U global miqyosga ega va dasturning istalgan joyidan foydalanish mumkin. Agar oʻzgaruvchi funksiya ichidagi var kalit soʻzi yordamida eʼlon qilingan boʻlsa, u faqat shu funksiya ichida koʻrinadi va u uchun mahalliy oʻzgaruvchi hisoblanadi.

Agar oʻzgaruvchi nomi global miqyosdagi oʻzgaruvchining nomiga toʻgʻri keluvchi var funksiyasidan foydalangan holda funksiyada eʼlon qilinsa, u global oʻzgaruvchi bilan “ust-boshlanadi”. Ya'ni, funksiya ichidagi bunday o'zgaruvchiga kirishda uning mahalliy versiyasidan foydalaniladi.

Bloklar (jingalak qavslar ichiga olingan kod sohalari) yangi doiralar yaratmasligini tushunish muhimdir. Funktsiya chaqirilganda yangi qamrov yaratiladi. Kalit so'z var blok doirasi emas, balki funktsional doirasi deb ataladigan narsaga ega.

Agar o'zgaruvchi funktsiya kodida e'lon qilingan bo'lsa, u butun funktsiya kodiga ko'rinadi. Agar o'zgaruvchi funktsiya kodining oxirida var yordamida e'lon qilingan bo'lsa ham, siz kodning boshida ham unga murojaat qilishingiz mumkin, chunki JavaScript ko'tarish mexanizmidan foydalanadi. Ushbu mexanizm o'zgaruvchan deklaratsiyalarni "ko'taradi", lekin ularni ishga tushirish operatsiyalarini emas. Bu chalkashlik manbai bo'lishi mumkin, shuning uchun funktsiyangizning boshida o'zgaruvchilarni e'lon qilishni qoidaga aylantiring.

▍let kalit so'zi
Let kalit so'zi ES2015 da taqdim etilgan va uni oddiygina var ning "blok" versiyasi deb atash mumkin. Let kalit so'zi bilan e'lon qilingan o'zgaruvchilar u e'lon qilingan blok, bayonot yoki ifoda va ichki bloklarga qamrab olinadi.
“Let” so‘zining o‘zi chalkashdek tuyulsa, uning o‘rniga “let” so‘zini ishlatishni tasavvur qilishingiz mumkin. Keyin let color = "qizil" iborasini ingliz tiliga shunday tarjima qilish mumkin: "rang qizil bo'lsin" va rus tiliga - "rang qizil bo'lsin".

Let kalit so'zidan foydalanish orqali siz var kalit so'zi bilan bog'liq noaniqliklardan xalos bo'lishingiz mumkin (masalan, let yordamida bir xil o'zgaruvchini ikki marta e'lon qila olmaysiz). Funktsiyadan tashqarida let dan foydalanish, masalan, tsikllarni ishga tushirishda global o'zgaruvchilar yaratmaydi.

Masalan, bunday kod xatoga yo'l qo'yadi:

uchun (i = 0; i< 5; i++) { console.log(i) } console.log(i)
Agar siklni ishga tushirish vaqtida var kalit so'zi yordamida hisoblagich i e'lon qilinsa, u o'z ishini tugatgandan so'ng i tsikldan tashqarida mavjud bo'ladi.

Hozirgi vaqtda zamonaviy standartlar asosida JS dasturlarini ishlab chiqishda var dan butunlay voz kechib, faqat let va const kalit so'zlaridan foydalanish mumkin.

▍const kalit so'zi
Var yoki let kalit so'zlari yordamida e'lon qilingan o'zgaruvchilar ustidan yozish mumkin. Agar bu kalit so'zlar o'rniga const ishlatilsa, uning yordamida e'lon qilingan va ishga tushirilgan konstantaga yangi qiymat berish mumkin emas.
Const a = "test"
Bu misolda a doimiysiga yangi qiymat berish mumkin emas. Ammo shuni ta'kidlash kerakki, agar a raqam kabi ibtidoiy qiymat emas, balki ob'ekt bo'lsa, const kalit so'zidan foydalanish bu ob'ektni o'zgarishlardan himoya qilmaydi.

Ob'ekt o'zgaruvchiga yozilgan deb aytishganda, ular aslida nimani anglatadi, o'zgaruvchi ob'ektga havolani saqlaydi. Ushbu havolani o'zgartirib bo'lmaydi va havola olib boradigan ob'ektning o'zini o'zgartirish mumkin.

const kalit so'zi ob'ektlarni o'zgarmas qilib qo'ymaydi. U shunchaki tegishli konstantalarda yozilgan ularga havolalarni o'zgarishlardan himoya qiladi. Bu shunday ko'rinadi:

Const obj = () console.log (obj.a) obj.a = 1 // ishlayotgan console.log (obj.a) // obj = 5 // xatolik yuzaga keladi
Initsializatsiya vaqtida doimiy objga yangi bo'sh ob'ekt yoziladi. Uning mavjud bo'lmagan xususiyatiga kirishga urinish a xatolikka olib kelmaydi. Konsol aniqlanmagan bo'ladi. Shundan so'ng, biz ob'ektga yangi xususiyat qo'shamiz va unga yana kirishga harakat qilamiz. Bu safar ushbu xususiyatning qiymati konsolga yuboriladi - 1. Agar siz misolning oxirgi satriga izohni olib tashlasangiz, ushbu kodni bajarishga urinish xatolikka olib keladi.

const kalit so'zi let so'ziga juda o'xshaydi, xususan, u blokli.

Zamonaviy sharoitda, qiymatlari o'zgartirilishi rejalashtirilmagan barcha ob'ektlarni e'lon qilish uchun const kalit so'zidan foydalanish juda maqbuldir, faqat alohida holatlarda ruxsat beriladi. Nega? Gap shundaki, dasturlarni murakkablashtirmaslik va xatolarga yo'l qo'ymaslik uchun mavjud bo'lgan eng oddiy konstruktsiyalardan foydalanishga intilish yaxshiroqdir.

Ma'lumotlar turlari
JavaScript ba'zan "tiplanmagan" til deb ataladi, ammo bu unday emas. To'g'ri, siz o'zgaruvchilarga har xil turdagi qiymatlarni yozishingiz mumkin, ammo JavaScript-da ma'lumotlar turlari mavjud. Xususan, biz ibtidoiy va ob'ektli ma'lumotlar turlari haqida gapiramiz.
Qiymatning ma'lumotlar turini aniqlash uchun typeof operatoridan foydalanishingiz mumkin. Operand turini ko'rsatadigan qatorni qaytaradi.

▍Birlamchi ma'lumotlar turlari
Mana JavaScript ibtidoiy ma'lumotlar turlari ro'yxati:
raqam (raqam)
qator (tor)
mantiqiy (mantiqiy qiymat)
null (maxsus qiymat null)
aniqlanmagan (maxsus qiymat aniqlanmagan)
belgi (belgi, maxsus holatlarda qo'llaniladi, ES6 da kiritilgan)
Bu yerda ma'lumotlar turlarining nomlari typeof operatori tomonidan qaytariladigan shaklda ko'rsatilgan.
Keling, ushbu ro'yxatdagi eng ko'p ishlatiladigan ma'lumotlar turlari haqida gapiraylik.

Raqam turi
JavaScript raqamlari qiymatlari 64 bitli ikki aniqlikdagi suzuvchi nuqtali raqamlar sifatida taqdim etiladi.
Raqamli harflar kodda butun, kasr sonlar esa o'nli yozuvda ifodalanadi. Raqamlarni yozish uchun boshqa usullardan foydalanishingiz mumkin. Misol uchun, agar sonli harfning boshida 0x prefiksi bo'lsa, u o'n oltilik yozuvda yozilgan raqam sifatida talqin qilinadi. Raqamlar ko'rsatkichli yozuvda ham yozilishi mumkin (bunday raqamlarda siz e harfini topishingiz mumkin).

Mana butun sonlarni yozishga misollar:

10 5354576767321 0xCC // o'n oltilik raqam
Mana kasr sonlar.

3.14 .1234 5.2e4 //5.2 * 10 ^ 4
Raqamli harflar (bu xatti-harakat ba'zi boshqa ibtidoiy turlar uchun xosdir), siz ularni ob'ekt deb atamoqchi bo'lganingizda, operatsiya bajarilayotganda avtomatik ravishda mos keladigan ob'ektlarga aylantiriladi, ular "ob'ektni o'rash" deb ataladi. Bunday holda, biz ob'ektni o'rash raqami haqida gapiramiz.

Masalan, Google Chrome konsolida raqamli harflar yozilgan a o'zgaruvchisiga ob'ekt sifatida kirishga urinish qanday ko'rinishga ega.

Raqamli ob'ektni o'rash bo'yicha maslahat

Agar, masalan, Number turidagi ob'ektning toString () usulidan foydalansangiz, u raqamning satr tasvirini qaytaradi. Brauzer konsolida (va oddiy kodda) bajarilishi mumkin bo'lgan mos keladigan buyruq quyidagicha ko'rinadi:

A.toString ()
Usul nomidan keyin qo'sh qavslarga e'tibor bering. Agar ular ta'minlanmagan bo'lsa, tizim xatolikka yo'l qo'ymaydi, lekin kutilgan natija o'rniga konsol 5 raqamining simli tasviriga umuman o'xshamaydigan narsani ko'rsatadi.

Global Number ob'ektidan konstruktor sifatida foydalanish mumkin, uning yordami bilan yangi raqamlar yaratilishi mumkin (garchi u bu shaklda deyarli ishlatilmasa ham), u o'z misollarini yaratmasdan mustaqil ob'ekt sifatida ham ishlatilishi mumkin (ya'ni, ba'zi raqamlar bilan ifodalangan). Yordam). Masalan, uning Number.MAX_VALUE xususiyati JavaScript-da ifodalanishi mumkin bo'lgan maksimal raqamli qiymatni o'z ichiga oladi.

String turi
String qiymatlari belgilar ketma-ketligidir. Bunday qiymatlar bitta yoki ikkita tirnoq ichiga olingan satr harflari sifatida belgilanadi.
"Bir qator" "Boshqa qator"
String qiymatlari teskari chiziq belgisi yordamida bir nechta qismlarga bo'linishi mumkin.

"A \ string"
Satrda qochish ketma-ketliklari bo'lishi mumkin, ular satr konsolga chop etilganda izohlanadi. Masalan, \ n ketma-ketligi satr tasmasi belgisini bildiradi. Teskari chiziq belgisi qo'shtirnoq ichiga olingan qatorlarga qo'shtirnoq qo'shish uchun ham ishlatilishi mumkin. Qo'shtirnoq belgisidan \ bilan qochish tizim uni maxsus belgi sifatida ko'rib chiqmasligiga olib keladi.

"Men ishlab chiquvchiman"
Satrlarni + operatori yordamida birlashtirish mumkin.

"A" + "string"

Shablon harflari
ES2015 shablon literallari yoki shablon satrlari deb ataladigan narsalarni taqdim etdi. Ular teskari belgilar (`) bilan o'ralgan satrlar va ba'zi qiziqarli xususiyatlarga ega.
`string`
Misol uchun, siz JavaScript ifodalarini baholash natijasi bo'lgan shablon harflarida ba'zi qiymatlarni almashtirishingiz mumkin.

`$ (bir narsa) bilan string` `$ boʻlgan satr (bir narsa + bir narsaElse)` `$ (obj.something ()) li satr`
Teskari belgilardan foydalanish ko'p qatorli satr harflarini yozishni osonlashtiradi:

`$ (bir narsa) bo'lgan satr`

Boolean turi
JavaScript-da mantiqiy so'zlar bilan ishlashda ishlatiladigan bir nechta ajratilgan so'zlar mavjud - haqiqiy va noto'g'ri. ==, ===, kabi taqqoslash operatsiyalari< , >, rost yoki yolgʻonni qaytaring.
Mantiqiy ifodalar dastur oqimini boshqarishga yordam berish uchun if va while kabi konstruksiyalarda qo'llaniladi.

Shuni ta'kidlash kerakki, agar rost yoki noto'g'ri qiymat kutilgan bo'lsa, siz til tomonidan avtomatik ravishda rost (haqiqat) yoki noto'g'ri (noto'g'ri) deb talqin qilinadigan boshqa qiymatlardan foydalanishingiz mumkin.

Xususan, quyidagilar noto'g'ri qiymatlardir:

0 -0 NaN undefined null "" // bo'sh qator
Boshqa barcha qiymatlar to'g'ri.

Null turi
JavaScript maxsus qiymatga ega, null, bu qiymat yo'qligini ko'rsatadi. Shunga o'xshash ma'nolar boshqa tillarda ham qo'llaniladi.
Belgilanmagan tur
O'zgaruvchiga yozilgan aniqlanmagan qiymat bu o'zgaruvchi ishga tushirilmaganligini va uning qiymati yo'qligini ko'rsatadi.
Bu qiymat qaytish kalit so'zi yordamida natijani aniq qaytarmaydigan funksiyalardan avtomatik ravishda qaytariladi. Agar funktsiya chaqirilganda ko'rsatilmagan ba'zi parametrlarni qabul qilsa, u ham aniqlanmaganga o'rnatiladi.

Qiymatni aniqlanmaganligini tekshirish uchun siz quyidagi konstruktsiyadan foydalanishingiz mumkin.

O'zgaruvchining turi === "aniqlanmagan"

▍Obyektlar
Barcha ibtidoiy bo'lmagan qiymatlar ob'ekt turiga tegishli. Biz funktsiyalar, massivlar, biz "ob'ektlar" deb ataydigan narsalar va boshqa ko'plab ob'ektlar haqida gapiramiz. Ushbu ma'lumotlar turlarining barchasi ob'ekt turiga asoslanadi va ular ko'p jihatdan farq qilsalar ham, ularning umumiy tomonlari ham ko'p.
Ifodalar
Ifodalar - bu amalga oshirilgan hisob-kitoblar asosida ma'lum bir qiymatni qayta ishlash va olish mumkin bo'lgan kod bo'laklari. JavaScript-da ifodalarning bir nechta toifalari mavjud.
Arifmetik ifodalar
Raqamlar bilan baholanadigan iboralar ushbu turkumga kiradi.
1/2 i ++ i - = 2 i * 2

String ifodalari
Bunday ifodalarni baholash natijasi satrlardir.
"A" + "string" "A" + = "string"

Birlamchi ifodalar
Literallar, konstantalar, identifikator murojaatlari shu turkumga kiradi.
2 0.02 "bir narsa" rost noto'g'ri bu // ijro konteksti, joriy ob'ektga havola aniqlanmagan i // bu erda i o'zgaruvchi yoki doimiy
Bunga ba'zi JavaScript kalit so'zlari va konstruktsiyalari ham kiradi.

Funktsiya sinfi funksiyasi * // rentabellik generatori // rentabellik generatorining ishini to'xtatib turish / davom ettirish buyrug'i * // boshqa iterator yoki generatorga asinxronizatsiya funktsiyasini topshirish * // asinxron funktsional ifodani kutish // asinxron funktsiyaning bajarilishini kutish / naqsh / men // muntazam ifoda() // guruhlash

Massiv va obyektni ishga tushirish ifodalari
// massiv harfi () // ob'ekt harfi (a: 1, b: 2) (a: (b: 1))
Mantiqiy ifodalar
Mantiqiy ifodalar mantiqiy operatorlardan foydalanadi, ularni baholash natijasi mantiqiy qiymatlardir.
A && b a || b! a

Mulkga kirish ifodalari
Bu ifodalar ob'ektlarning xossalari va usullariga kirish imkonini beradi.
Object.property // ob'ekt ob'ektining xususiyatiga (yoki usuliga) kirish ["xususiyat"]

Obyekt yaratish ifodalari
yangi ob'ekt () yangi (1) yangi MyRectangle ("nom", 2, (a: 4))
Funktsiya deklaratsiyasi ifodalari
funktsiya () () funktsiya (a, b) (qaytish a * b) (a, b) => a * b a => a * 2 () => (2-ga qaytish)
Qiyin ifodalar
Bunday iboralar ob'ektlarning funktsiyalari yoki usullarini chaqirish uchun ishlatiladi.
A.x (2) window.resize ()

Ob'ektlar bilan ishlash
Yuqorida biz allaqachon ob'ektlarga duch keldik, ob'ekt literallari haqida, ularning usullarini chaqirish, ularning xususiyatlariga kirish haqida. Bu erda biz ob'ektlar haqida batafsilroq gaplashamiz, xususan, prototipli meros mexanizmini va class kalit so'zidan foydalanishni ko'rib chiqamiz.
▍ Prototipli meros
JavaScript zamonaviy dasturlash tillari orasida prototip merosni qo'llab-quvvatlashi bilan ajralib turadi. Ko'pgina ob'ektga yo'naltirilgan tillar sinfga asoslangan meros modelidan foydalanadi.
Har bir JavaScript ob'ekti prototipi bo'lgan boshqa ob'ektga ishora qiluvchi maxsus xususiyatga (__proto__) ega. Ob'ekt prototipning xususiyatlari va usullarini meros qilib oladi.

Faraz qilaylik, bizda ob'ekt harfi yordamida yaratilgan ob'ekt bor.

Const car = ()
Yoki Object konstruktori yordamida obyekt yaratdik.

Const car = yangi ob'ekt ()
Ikkala holatda ham avtomobil prototipi Object.prototype bo'ladi.

Agar siz ob'ekt bo'lgan massiv yaratsangiz, uning prototipi Array.prototype ob'ekti bo'ladi.

Const list = // yoki shunday const list = new Array ()
Buni quyidagicha tekshirishingiz mumkin.

Avtomobil .__ proto__ == Ob'ekt.prototip // haqiqiy avtomobil .__ proto__ == yangi Ob'ekt () .__ proto__ // haqiqiy ro'yxat .__ proto__ == Ob'ekt.prototip // noto'g'ri ro'yxat .__ proto__ == Array.prototip / / haqiqiy ro'yxat .__ proto__ == yangi massiv () .__ proto__ // rost
Bu erda biz __proto__ xususiyatidan foydalandik, u ishlab chiquvchi uchun mavjud bo'lishi shart emas, lekin odatda siz unga murojaat qilishingiz mumkin. Shuni ta'kidlash kerakki, ko'proq ishonchli tarzda ob'ektning prototipini olish uchun global ning getPrototypeOf () usulidan foydalanish kerak Ob'ekt ob'ekti.

Object.getPrototypeOf (yangi Ob'ekt ())
Prototipning barcha xususiyatlari va usullari ushbu prototipga ega bo'lgan ob'ekt uchun mavjud. Misol uchun, ularning ro'yxati massiv uchun qanday ko'rinishga ega.




Massiv maslahati
Barcha ob'ektlar uchun asosiy prototip Object.prototype hisoblanadi.

Array.prototype .__ proto__ == Object.prototype
Object.prototype prototipiga ega emas.

Yuqorida biz ko'rgan narsa prototip zanjirining namunasidir.

Ob'ektning xossasi yoki usuliga kirishga urinayotganda, agar ob'ektning o'zida bunday xususiyat yoki usul bo'lmasa, ular uning prototipida, so'ngra prototip prototipida qidiriladi va keraklisi topilguncha davom etadi. , yoki prototip zanjiri tugamaguncha.

Yangi operator yordamida ob'ektlar yaratish va ob'ekt literallari yoki massiv literallaridan foydalanish bilan bir qatorda, Object.create () usuli yordamida ob'ektni yaratishingiz mumkin. Ushbu usulga o'tkazilgan birinchi argument u yaratgan ob'ektning prototipi bo'ladigan ob'ektdir.

Const car = Object.create (Object.prototype)
IsPrototypeOf () usuli yordamida ob'ekt boshqa ob'ektning prototip zanjirining bir qismi ekanligini tekshirishingiz mumkin.

Const ro'yxati = Array.prototype.isPrototypeOf (ro'yxat)

Konstruktor funktsiyalari
Yuqorida biz tilda mavjud bo'lgan konstruktor funksiyalaridan foydalangan holda yangi ob'ektlar yaratdik (ularni chaqirishda new kalit so'zi ishlatiladi). Bunday funktsiyalarni o'zingiz yaratishingiz mumkin. Keling, bir misolni ko'rib chiqaylik.
Funktsiya Shaxs (ism) (tush.name = ism) Shaxs.prototip.salom = funktsiya () (console.log (this.name)) ruxsat odam = yangi Shaxs ("Flavio") person.salom () console.log ( Person.prototype.isPrototypeOf (odam))
Bu erda biz konstruktor funksiyasini yaratamiz. Uni chaqirganingizda, kalit bilan ko'rsatilgan yangi ob'ekt yaratiladi bu so'z konstruktor tanasida. Biz bu obyektga name xossasini qo'shamiz va konstruktorga o'tgan narsani unga yozamiz. Ushbu ob'ekt konstruktordan avtomatik ravishda qaytariladi. Konstruktor funksiyasidan foydalanib, nom xossalari ular yaratilganda konstruktorga uzatilgan narsalarni o'z ichiga oladigan ko'plab ob'ektlarni yaratishingiz mumkin.

Konstruktorni yaratgandan so'ng, biz uning prototipiga ushbu funktsiya yordamida yaratilgan ob'ektning name xususiyatining qiymatini konsolga chop etadigan funksiya qo'shamiz. Ushbu konstruktor yordamida yaratilgan barcha ob'ektlar bir xil prototipga ega bo'ladi va shuning uchun bir xil salom () funktsiyasidan foydalanadi. Buni Shaxs tipidagi boshqa ob'ekt yaratish va uning salom () funksiyasini allaqachon misoldagi ob'ekt funktsiyasi bilan solishtirish orqali tekshirish oson (bu holda funksiya nomi qavssiz yoziladi).

▍Darslar
ES6 standartida JavaScript "sinf" sifatida tanildi.
Bungacha JavaScript faqat yuqorida tavsiflangan prototip meros mexanizmidan foydalanishi mumkin edi. JS ga boshqa tillardan kelgan dasturchilar uchun bu mexanizm g'ayrioddiy ko'rinardi. Shuning uchun tilda sinflar paydo bo'ldi, ular aslida prototip meros mexanizmi uchun "sintaktik shakar" hisoblanadi. Ya'ni, an'anaviy usul yordamida yaratilgan ob'ektlar ham, sinflar yordamida yaratilgan ob'ektlar ham prototiplarga ega.

Sinf deklaratsiyasi
Sinf deklaratsiyasi shunday ko'rinadi.
Sinf shaxsi (konstruktor (ism) (this.name = ism) salom () ("Salom, men" + this.name + "." deb qaytaring))
Sinf yangi ClassIdentifier () konstruksiyasi yordamida yangi ob'ektlarni yaratish uchun ishlatilishi mumkin bo'lgan identifikatorga ega.

Yangi obyekt yaratishda konstruktor usuli chaqiriladi, unga parametrlar uzatiladi.

Usullar sinfda e'lon qilinishi mumkin. Bizning holatda, salom () - bu sinfdan yaratilgan barcha ob'ektlar tomonidan chaqirilishi mumkin bo'lgan usul. Bu Person sinfi yordamida yangi ob'ekt yaratishga o'xshaydi.

Const flavio = yangi shaxs ("Flavio") flavio.hello ()

Sinfga asoslangan meros
Sinflar boshqa sinflarni kengaytirishi mumkin. Bunday sinflardan yaratilgan ob'ektlar asl sinfning usullarini ham, kengaytirilgan sinfda aniqlangan usullarni ham meros qilib oladi.
Agar boshqa sinfni kengaytiruvchi sinf (ushbu sinfdan meros bo'lib qolgan) nomi ota-sinfniki bilan bir xil bo'lgan usulga ega bo'lsa, bu usul dastlabkisidan ustun turadi.

Class Programmer extensions Shaxs (salom () (qaytish super.hello () + "Men dasturchiman.")) Const flavio = new Programmer ("Flavio") flavio.hello ()
Yuqoridagi misoldagi salom () usulini chaqirish Salom, men Flavioman qatorini qaytaradi. Men dasturchiman.

Sinflar o'zgaruvchilar (xususiyatlar) mavjudligini ta'minlamaydi, sinflar yordamida yaratilgan ob'ektlarning xossalari konstruktorda sozlanishi kerak.

Sinf ichida siz super kalit so'zidan foydalanib, ota-sinfga murojaat qilishingiz mumkin.

Statik usullar
Sinfda tavsiflangan usullarni sinfning o'ziga emas, balki ushbu sinf asosida yaratilgan ob'ektlarga murojaat qilish orqali chaqirish mumkin. Statik usullarni to'g'ridan-to'g'ri sinfga murojaat qilish orqali chaqirish mumkin.
Shaxsiy usullar
JavaScript-da xususiy (xususiy, shaxsiy) usullarni e'lon qilish imkonini beruvchi o'rnatilgan mexanizm mavjud emas. Ushbu cheklovni, masalan, yopilishlar yordamida chetlab o'tish mumkin.
Qabul qiluvchilar va sozlagichlar
Sinfda usullarni ularning oldidan get yoki set kalit so'zlari bilan tavsiflashingiz mumkin. Bu sizga qabul qiluvchilar va sozlagichlar - sinfdan yaratilgan ob'ektlarning xususiyatlariga kirishni boshqarish uchun ishlatiladigan funktsiyalarni yaratishga imkon beradi. Pseudo-xususiyatning qiymatini o'qishga urinilganda getter chaqiriladi va unga yangi qiymat yozishga harakat qilinganda sozlashchi chaqiriladi.
Sinf shaxsi (konstruktor (ism) (this.userName = name) to'siq nomi (qiymat) (this.userName = qiymat) olish nomi () (this.userNameni qaytaring))

Natijalar
Ushbu maqolada biz JavaScript-da o'zgaruvchilar, ma'lumotlar turlari, ifodalar va ob'ektlar bilan ishlash haqida gaplashdik. Funktsiyalar bizning keyingi maqolamizning mavzusi bo'ladi.
Hurmatli kitobxonlar! Agar siz JS-da uzoq vaqtdan beri yozayotgan bo'lsangiz, sinf kalit so'zining tilda paydo bo'lishiga qanday munosabatda ekanligingizni ayting.

Ushbu qo'llanmada biz juda muhim tushunchani - JavaScript ma'lumotlar turlarini tanishtiramiz. Ushbu kontseptsiyani diqqat bilan ko'rib chiqishni tavsiya qilamiz - agar siz uni boshidanoq tushunmasangiz, keyinchalik siz yaratgan dasturning g'alati xatti-harakatlariga tez-tez duch kelishingiz kerak bo'ladi.

Dinamik yozish
Jarayonda kompyuter dasturlari har biri dasturlash tilida qayta ishlanishi mumkin bo'lgan va ma'lum bir ma'lumot turiga tegishli bo'lgan turli xil qiymatlarni boshqarish.

JavaScript-da ma'lumotlar turlarini ikki toifaga bo'lish mumkin: oddiy (shuningdek, ibtidoiy deb ataladi) turlari va kompozit (shuningdek, havola yoki ob'ekt deb ataladi) turlari.

JavaScript zaif terilgan yoki dinamik dasturlash tili bo'lib, dasturni bajarish bosqichida, ular aytganidek, ma'lumotlar turlarini aniqlash, tahlil qilish va kompilyatsiya qilish imkonini beradi. Bu o'zgaruvchining turini oldindan aniqlashning hojati yo'qligini anglatadi. Turi dasturni bajarish jarayonida avtomatik ravishda aniqlanadi.
Shunday qilib, dasturning turli qismlarida bir xil o'zgaruvchi har xil turdagi qiymatlarni olishi mumkin:

Ma'lumotlar turlari
ECMAScript® standarti quyidagi ma'lumotlar turlarini belgilaydi:

Oddiy(ibtidoiy deb ham ataladi) turlari:
mantiqiy (inglizcha Boolean) - ikkita mumkin bo'lgan qiymatlarni qabul qilishi mumkin, ba'zan rost (to'g'ri) va noto'g'ri (noto'g'ri) deb ataladi;
null (inglizcha Null) - null qiymati odatda ataylab mavjud bo'lmagan yoki yaroqsiz ob'ekt yoki manzilga ishora qiluvchi havolani ifodalaydi;
undefined - oldindan belgilangan global o'zgaruvchini bildiradi, noaniq qiymat bilan ishga tushiriladi;
raqamli (ing. Number) - 64 bitli ikki aniqlikdagi suzuvchi nuqtali raqam formatidagi raqamli ma'lumotlar turi;
string (inglizcha String) - matnni ifodalash uchun foydalaniladigan belgilar ketma-ketligi;
simvol (ing. Symbol) - nusxalari yagona va o'zgarmas bo'lgan ma'lumotlar turi. (ECMAScript 6 da yangi).
Ob'ekt Ob'ekt - bu odatda ob'ektning xususiyatlari deb ataladigan nomlangan qiymatlar to'plami.
Ibtidoiy va kompozit turlarning farqi
Har bir ma'lumot turini ko'rib chiqishdan oldin, keling, operator turi bilan tanishamiz. typeof operatori o'zgaruvchining ma'lumotlar turini tavsiflovchi qatorni qaytaradi.
Keling, quyidagi misol bilan qanday ishlashini ko'rsatamiz:

Yuqoridagi misoldagi skript o'zgaruvchilarni e'lon qiladi, ularni ishga tushiradi (qiymatlarni tayinlaydi) va keyin har bir o'zgaruvchining turini chiqaradi.

Primitiv va kompozit ma'lumotlar turlari o'rtasidagi farq ularning qiymatlarini nusxalashda paydo bo'ladi.

O'zgaruvchiga oddiy turdagi qiymat berilganda, qiymatning o'zi (masalan, raqam) o'zgaruvchiga yoziladi. Biz qachon oddiy turdagi o'zgaruvchini tayinlash boshqasiga, u qiymatdan nusxa oladi... Natijada, har bir o'zgaruvchiga ega bo'ladi uning ma'nosi va o'zgaruvchilardan biridagi o'zgarishlar hech qanday tarzda ta'sir qilmaydi boshqa o'zgaruvchining qiymati bo'yicha:

O'zgaruvchi bo'lganda kompozitsiyaning qiymatini belgilang(mos yozuvlar) turi, keyin o'zgaruvchi yoziladi havola qiymati bo'yicha ( ob'ektga havola). Bir o'zgaruvchini (qiymatida kompozit qiymatga havola mavjud) boshqa o'zgaruvchiga tayinlaganimizda, u sodir bo'ladi. havolani nusxalash kompozit qiymatga. Natijada ikkala o'zgaruvchi ham bir xil kompozit qiymatga ishora qiladi va o'zgaruvchilardan birining qiymatining o'zgarishi ta'sir qiladi boshqa o'zgaruvchida:

Ibtidoiy turlar
Ob'ektlardan tashqari barcha JavaScript ma'lumotlar turlari o'zgarmasdir. Bu shuni anglatadiki, ularning qiymatlarini o'zgartirish mumkin emas, faqat yangi, boshqa qiymat bilan yoziladi. Masalan, satrlarni belgi bo'yicha tuzatish mumkin emas - ularni faqat to'liq qayta yozish mumkin. Ushbu turdagi qiymatlar "ibtidoiy" deb ataladi.

Dastur ishlashi mumkin bo'lgan eng oddiy ma'lumotlar literallar deyiladi. Literallar - bu JavaScript-da qiymatlarni ifodalash uchun ishlatiladigan raqamlar yoki satrlar. Taqdim etilgan ma'lumotlar juda xilma-xil bo'lishi mumkin, shuning uchun qiymatlar turli xil turlari... JavaScript-dagi eng oddiy ma'lumotlar turlari asosiy ma'lumotlar turlari deb ataladi: raqamlar, satrlar va mantiqiy. Ularning barchasi "ibtidoiy".

Mantiqiy (mantiqiy) turi "boolean"
Mantiqiy yoki mantiqiy qiymatlar (ularning ixtirochisi Boole nomi bilan atalgan) ikkita qiymatdan faqat bittasiga ega bo'lishi mumkin: rost yoki noto'g'ri. Qadriyatlar rost yoki noto'g'ri odatda taqqoslash yoki mantiqiy operatsiyalarda paydo bo'ladi.

Quyidagi dastur mantiqiy o'zgaruvchini yaratadi va keyin uning qiymatini if ​​/ else ifodasi yordamida tekshiradi:

Har qanday ifoda taqqoslash ifodasi sifatida ishlatilishi mumkin. 0, null, aniqlanmagan yoki bo'sh satr qiymatini qaytaradigan har qanday ifoda noto'g'ri deb talqin qilinadi. Boshqa qiymatni belgilovchi ifoda rost deb talqin qilinadi.

Eslatma: Mantiqiy qiymatlarni yozishda ular qo'shtirnoq ichida olinmaydi: var myVar = true;
Shu bilan birga, var myVar = "true" deb e'lon qilish qator o'zgaruvchisini yaratadi.

Raqamli ma'lumotlar turi
JavaScript-da butun son va suzuvchi nuqta o'rtasida hech qanday farq yo'q - aslida JavaScript barcha raqamlarni suzuvchi nuqta qiymati sifatida ifodalaydi.

JavaScript IEEE-754 standartida belgilangan raqamlarni ifodalash uchun 64 bitli formatdan foydalanadi. Ushbu format ± 1,7976931348623157 × 10,308 dan ± 5 × 10 -324 oralig'idagi raqamlarni ifodalashga qodir.

To'g'ridan-to'g'ri dastur kodida bo'lgan raqam sonli harf deyiladi. O'nlik butun son literallaridan tashqari, JavaScript o'n oltilik qiymatlarni taniydi.
O'n oltilik formatdagi raqamlar 0 dan 9 gacha bo'lgan har qanday raqamlar ketma-ketligini va a dan f gacha bo'lgan harflarni o'z ichiga olishi mumkin, bu albatta "0x" belgilar ketma-ketligidan boshlanadi.

Var a = 255; var b = 0xFF; // O'n oltilik sistemada 255 raqami

Bundan tashqari, JavaScript maxsus raqamli qiymatlarni o'z ichiga oladi:

NaN (raqam yoki hisoblash xatosi emas). Bu yaroqsiz ma'lumotlar, masalan, satrlar yoki aniqlanmagan qiymatlar ustida noto'g'ri matematik operatsiya natijasidir.
Cheksizlik (ijobiy cheksizlik). Ijobiy raqam JavaScript-da ifodalash uchun juda katta bo'lsa ishlatiladi.
-Infinity (salbiy cheksizlik). Salbiy raqam JavaScript-da ifodalash uchun juda katta bo'lsa ishlatiladi.
± 0 (musbat va salbiy 0). JavaScript ijobiy va salbiy nolni ajratib turadi.
String ma'lumotlar turi
Satr turi - har biri Unicode belgisini (harflar, raqamlar, tinish belgilari, maxsus belgilar va bo'shliqlar) ifodalovchi 16 bitli qiymatlarning o'zgarmas, tartiblangan ketma-ketligi. Satrlar bo'sh bo'lishi yoki bir yoki bir nechta belgilarni o'z ichiga olishi mumkin. Satrlar juft (") yoki bitta (") tirnoq yordamida yaratiladi. Bir juft tirnoq bilan ajratilgan qatorda qoʻsh tirnoqlardan foydalanishingiz mumkin va aksincha – bitta qoʻshtirnoq juft qoʻshtirnoq ichiga olingan qatorda ishlatilishi mumkin:

JavaScript-da qo'sh va bitta tirnoq o'rtasida farq yo'q, lekin satr boshida va oxiridagi qo'shtirnoqlarni ajratmaslik kerak. Masalan, bunday ifoda sintaksis xatosini keltirib chiqaradi:

var firstName = "Maks"; // sintaksis xatosi - turli tirnoqlar

Eslatma: JavaScript-da C, C++ va Java tillarida char kabi bitta belgi uchun maxsus maʼlumotlar turi mavjud emas. Bitta belgi bir uzunlikdagi qator sifatida ifodalanadi.

Null ma'lumotlar turi
Null turi faqat maxsus qiymatni o'z ichiga oladi, null.
Null kalit so'zini funksiya yoki o'zgaruvchi nomi sifatida ishlatib bo'lmaydi. Null qiymati "bo'sh" ob'ektga havola bo'lib, maxsus maqsadga ega - odatda o'zgaruvchini ishga tushirish uchun ishlatiladi, keyinchalik unga qiymat beriladi.

Null uchun typeof operatori "ob'ekt" qatorini qaytaradi, bu null maxsus "bo'sh" ob'ekt ekanligini bildiradi.

Aniqlanmagan ma'lumotlar turi
Aniqlanmagan tur (aniqlanmagan) o'z turini hosil qiladi, unda yagona maxsus qiymat aniqlanmagan. Bu var iborasi yordamida e'lon qilingan, lekin ishga tushirilmagan o'zgaruvchining ma'nosidir:

Aniqlanmagan qiymat hech qachon qiymat berilmagan o'zgaruvchiga, shuningdek, mavjud bo'lmagan ob'ekt xususiyatiga yoki massiv elementiga murojaat qilganda qaytariladi.

Shuni ta'kidlash kerakki, qiymati aniqlanmagan o'zgaruvchi umuman aniqlanmagan o'zgaruvchidan farq qiladi:

Ushbu misolda alert () usuli aniqlanmagan o'zgaruvchan yoshning qiymatini chiqaradi. Ikkinchi holda, e'lon qilinmagan o'zgaruvchan avtomobil ogohlantirish () usuliga o'tkaziladi, bu xatoga olib keladi.

Quyidagi misol Ajam dasturchilarni biroz chalkashtirib yuborishi mumkin, chunki ishga tushirilmagan va e'lon qilinmagan o'zgaruvchilar uchun typeof operatori aniqlanmaganni qaytaradi:

Yuqoridagi misolda yosh o'zgaruvchisi e'lon qilingan, lekin unga hech narsa yozilmagan, shuning uchun uning qiymati aniqlanmagan. O'zgaruvchan avtomobil e'lon qilinmagan - aslida bunday emas. Biroq, typeof har ikki holatda ham aniqlanmagan. Buning ma'nosi bor, albatta, chunki bu o'zgaruvchilarning hech biri bilan hech qanday operatsiyani bajarish mumkin emas, garchi texnik jihatdan ular butunlay boshqacha.

Eslatma: Har doim e'lon qilingan o'zgaruvchini ishga tushirish tavsiya etiladi. Bunday holda, typeof operatori o'zgaruvchining ishga tushirilmaganligi uchun emas, balki e'lon qilinmaganligi sababli aniqlanmaganligini bilib olasiz.

Aniqlanmagan qiymat null dan olingan, shuning uchun ECMA-262 da == ekvivalentlik operatori ularni teng deb hisoblaydi:

Null va undefined o'zaro bog'liq bo'lsa-da, ular turli xil usullarda qo'llaniladi. Siz o'zgaruvchini aniqlanmagan qilib belgilamasligingiz kerak, lekin null shart emas. Agar kerakli ob'ekt mavjud bo'lmasa, uning o'rniga null ishlatilishi kerak. Bu null qiymati bo'sh ob'ektga ko'rsatgich sifatida kiritilganligini ko'rsatadi va uning aniqlanmagandan farqini ta'kidlaydi.

Dasturda null va undefined o'rtasidagi farqni aniqlash uchun === identifikatsiya operatoridan foydalanish mumkin:

Ma'lumotlar turi Symbol
Belgi ECMAScript-ning 6-versiyasidan beri JavaScript uchun yangi. Simvol noyob, o‘zgarmas, ibtidoiy qiymat bo‘lib, noyob identifikatorlarni yaratish uchun ishlatiladi.

Belgini yaratish uchun Symbol funksiyasini chaqirish kerak:

var mySymbol = Symbol ();

Belgini aniqlash uchun typeof operatoridan foydalanishingiz mumkin, agar qiymat belgi bo'lsa, string belgisi qaytariladi:

Symbol funksiyasi ixtiyoriy parametrga ega - simni tasvirlash uchun ishlatiladigan satr:

Xususiyat nomi satrdir, shuning uchun ob'ektlar satrlarni qiymatlar bilan bog'lash uchun ko'rib chiqilishi mumkin. Birgalikda bu ma'lumotlar bo'laklari kalit-qiymat juftligini tashkil qiladi.

V JavaScript obyektlari ikkita sintaksisdan biri bilan yaratilishi mumkin:

1.var obj = (); // ob'ektdan foydalanish literal 2.var obj = new Object (); // konstruktor deb nomlangan usul yordamida

Ob'ektni literal yordamida yaratish oddiy o'zgaruvchini aniqlashdan boshlanadi. Ushbu bayonotning o'ng tomonida siz jingalak qavslar () ichida vergul bilan ajratilgan ro'yxat bo'lgan ob'ektni yozasiz. "nom-qiymat" jingalak qavslar ichiga olingan. Mulk nomi va qiymati ikki nuqta bilan ajratiladi:

var cat = ("oyoqlar": 4, "ism": "Murzik", "rang": "Redhead")

Ob'ektlarni yaratishning ikkinchi usuli Object () konstruktoridan foydalanishdir. Bunda birinchi navbatda new Object () ifodasi qo'llaniladi, so'ngra olingan ob'ektning xossalari aniqlanadi va ishga tushiriladi:

Bir o'zgaruvchini (qiymatida kompozit qiymatga havola mavjud) boshqa o'zgaruvchiga tayinlaganimizda, kompozit qiymatga havola ko'chiriladi. Natijada, ikkala o'zgaruvchi ham bir xil kompozit qiymatga ishora qiladi va o'zgaruvchilardan birining qiymatidagi o'zgarishlar boshqa o'zgaruvchiga ta'sir qiladi.
0, null, aniqlanmagan yoki bo'sh satr qiymatini qaytaradigan har qanday ifoda noto'g'ri deb talqin qilinadi.
Satrlar juft (") yoki bitta (") tirnoq yordamida yaratiladi. Bir juft qo'shtirnoq bilan ajratilgan qatorda qo'sh tirnoqlardan foydalanishingiz mumkin va aksincha - bitta qo'shtirnoq juft qo'shtirnoq ichiga olingan qatorda ishlatilishi mumkin.
Null qiymati "bo'sh" ob'ektga havola bo'lib, maxsus maqsadga ega - odatda o'zgaruvchini ishga tushirish uchun ishlatiladi, keyinchalik unga qiymat beriladi.
Qiymat (aniqlanmagan) var bayonoti bilan e'lon qilingan, lekin ishga tushirilmagan o'zgaruvchiga ega.
JavaScript-da ob'ektlar ikkita usuldan birida yaratilishi mumkin:
ob'ekt harfidan foydalanish
konstruktor deb ataladigan usul yordamida
Ob'ektda tartibsiz xususiyatlar to'plami mavjud bo'lib, ularning har biri nom va qiymatni o'z ichiga oladi. Istalgan vaqtda ob'ektga yangi nomlangan qiymatlarni qo'shishingiz yoki mavjudlarini o'chirishingiz mumkin.