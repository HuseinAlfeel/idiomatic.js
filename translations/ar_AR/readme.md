Safe raw copy from line 1 till 517:

# مبادئ كتابة الجافاسكريبت المتسقة والاصطلاحية


## هذا مستند حي ومتطور، والأفكار الجديدة لتحسين الكود الذي نكتبه مرحب بها دائماً. ساهم معنا: انسخ الفرع (fork)، استنسخ (clone)، أنشئ فرعاً (branch)، أرسل التزاماتك (commit)، ادفع التغييرات (push)، أرسل طلب دمج (pull request).


* Rick Waldron [@rwaldron](http://twitter.com/rwaldron), [github](https://github.com/rwaldron)
* Mathias Bynens [@mathias](http://twitter.com/mathias), [github](https://github.com/mathiasbynens)
* Schalk Neethling [@ossreleasefeed](http://twitter.com/ossreleasefeed), [github](https://github.com/ossreleasefeed/)
* Kit Cambridge  [@kitcambridge](http://twitter.com/kitcambridge), [github](https://github.com/kitcambridge)
* Raynos  [github](https://github.com/Raynos)
* Matias Arriola [@MatiasArriola](https://twitter.com/MatiasArriola), [github](https://github.com/MatiasArriola/)
* John Fischer [@jfroffice](https://twitter.com/jfroffice), [github](https://github.com/jfroffice/)
* Idan Gazit [@idangazit](http://twitter.com/idangazit), [github](https://github.com/idangazit)
* Leo Balter [@leobalter](http://twitter.com/leobalter), [github](https://github.com/leobalter)
* Breno Oliveira [@garu_rj](http://twitter.com/garu_rj), [github](https://github.com/garu)
* Leo Beto Souza [@leobetosouza](http://twitter.com/leobetosouza), [github](https://github.com/leobetosouza)
* Ryuichi Okumura [@okuryu](http://twitter.com/okuryu), [github](https://github.com/okuryu)
* Pascal Precht [@PascalPrecht](http://twitter.com/PascalPrecht), [github](https://github.com/pascalprecht)
* EngForDev [engfordev](http://www.opentutorials.org/course/167/1363) - Hwan Min Hong / MinTaek Kwon [@leoinsight](http://twitter.com/leoinsight) / Tw Shim [@marocchino](http://twitter.com/marocchino), [github](https://github.com/marocchino) / Nassol Kim [@nassol99](http://twitter.com/nassol99), [github](https://github.com/nassol) / Juntai Park [@rkJun](http://twitter.com/rkJun), [github](https://github.com/rkJun) / Minkyu Shim / Gangmin Won / Justin Yoo [@justinchronicle](http://twitter.com/justinchronicle) / Daeyup Lee
* Marco Trulla [@marcotrulla](http://twitter.com/marcotrulla), [github](https://github.com/Ragnarokkr)
* Alex Navasardyan [@alexnavasardyan](http://twitter.com/alexnavasardyan), [github](https://github.com/2k00l)
* Mihai Paun [@mihaipaun](http://twitter.com/mihaipaun), [github](https://github.com/mihaipaun)
* Evgeny Mandrikov [@\_godin\_](http://twitter.com/_godin_), [github](https://github.com/Godin)
* Sofish Lin [@sofish](http://twitter.com/sofish), [github](https://github.com/sofish)
* Дејан Димић [@dejan_dimic](http://twitter.com/dejan_dimic), [github](https://github.com/rubystream)
* Miloš Gavrilović [@gavrisimo](http://twitter.com/gavrisimo), [github](https://github.com/gavrisimo)
* Duc Nguyen [@ducntq](https://twitter.com/ducntq), [github](https://github.com/ducntq)
* James Young [@jamsyoung](http://twitter.com/jamsyoung), [github](https://github.com/jamsyoung)
* Stephane Moreau [github](https://github.com/stmoreau)  
* Boris Nekezov [github](https://github.com/boris-nekezov)  
* Akshat Joshi [@akshat_joshi](http://twitter.com/akshat_joshi), [github](https://https://github.com/akshatjoshii)



## "كل الكود في أي مشروع برمجي يجب أن يبدو وكأن شخصاً واحداً قام بكتابته، بغض النظر عن عدد المطورين الذين ساهموا فيه."



### هذا المستند يحدد الممارسات التي أتبعها في كل كود أكون المؤلف الأصلي له. المساهمات في المشاريع التي أنشأتها يجب أن تتبع هذه الإرشادات.

### لست أحاول فرض تفضيلاتي الشخصية على كود الآخرين أو مشاريعهم؛ إذا كان هناك أسلوب شائع موجود، فيجب احترامه.


ريبيكا مورفي (Rebecca Murphey)

### "جزء من كونك راعياً جيداً لمشروع ناجح هو إدراك أن كتابة الكود لنفسك فقط فكرة سيئة™. إذا كان آلاف الأشخاص يستخدمون كودك، فاكتب كودك للوضوح الأقصى، وليس حسب تفضيلك الشخصي لكيفية الذكاء ضمن المواصفات."

إيدان غازيت (Idan Gazit)

### "أن كتابة الكود لنفسك فقط فكرة سيئة، هو أمر يجب على كل مشرف جيد لمشروع ناجح أن يدركه™. عندما يستخدم آلاف الأشخاص كودك، اكتب كودك بأقصى وضوح ممكن، وليس فقط حسب تفضيلاتك الشخصية."


## v3∙LatestCopyPublishمبادئ كتابة الجافاسكريبت المتسقة والاصطلاحية
هذا مستند حي ومتطور، والأفكار الجديدة لتحسين الكود الذي نكتبه مرحب بها دائماً.
ساهم معنا: انسخ المستودع (fork)، استنسخ (clone)، أنشئ فرعاً (branch)، أرسل التزاماتك (commit)، ادفع التغييرات (push)، أرسل طلب دمج (pull request).

فلسفة المشروع الأساسية

"كل الكود في أي مشروع برمجي يجب أن يبدو وكأن شخصاً واحداً قام بكتابته، بغض النظر عن عدد المطورين الذين ساهموا فيه."

هذا المستند يحدد الممارسات التي أتبعها في كل كود أكون المؤلف الأصلي له. المساهمات في المشاريع التي أنشأتها يجب أن تتبع هذه الإرشادات.
لست أحاول فرض تفضيلاتي الشخصية على كود الآخرين أو مشاريعهم؛ إذا كان هناك أسلوب شائع موجود، فيجب احترامه.
ريبيكا مورفي (Rebecca Murphey)

"جزء من كونك راعياً جيداً لمشروع ناجح هو إدراك أن كتابة الكود لنفسك فقط فكرة سيئة™. إذا كان آلاف الأشخاص يستخدمون كودك، فاكتب كودك للوضوح الأقصى، وليس حسب تفضيلك الشخصي لكيفية الذكاء ضمن المواصفات."

إيدان غازيت (Idan Gazit)

"أن كتابة الكود لنفسك فقط فكرة سيئة، هو أمر يجب على كل مشرف جيد لمشروع ناجح أن يدركه™. عندما يستخدم آلاف الأشخاص كودك، اكتب كودك بأقصى وضوح ممكن، وليس فقط حسب تفضيلاتك الشخصية."


## الترجمات المتاحة

* [ORIGINAL](https://github.com/rwldrn/idiomatic.js/)
* [Bulgarian](https://github.com/rwldrn/idiomatic.js/tree/master/translations/bg_BG)
* [German](https://github.com/rwldrn/idiomatic.js/tree/master/translations/de_DE)
* [French](https://github.com/rwldrn/idiomatic.js/tree/master/translations/fr_FR)
* [Spanish](https://github.com/rwldrn/idiomatic.js/tree/master/translations/es_ES)
* [Portuguese - Brazil](https://github.com/rwldrn/idiomatic.js/tree/master/translations/pt_BR)
* [Korean](https://github.com/rwldrn/idiomatic.js/tree/master/translations/ko_KR)
* [Japanese](https://github.com/rwldrn/idiomatic.js/tree/master/translations/ja_JP)
* [Italian](https://github.com/rwldrn/idiomatic.js/tree/master/translations/it_IT)
* [Russian](https://github.com/rwldrn/idiomatic.js/tree/master/translations/ru_RU)
* [Romanian](https://github.com/rwldrn/idiomatic.js/tree/master/translations/ro_RO)
* [简体中文](https://github.com/rwldrn/idiomatic.js/tree/master/translations/zh_CN)
* [Serbian - cyrilic alphabet](https://github.com/rwldrn/idiomatic.js/tree/master/translations/ср_СР)
* [Serbian - latin aplphabet](https://github.com/rwldrn/idiomatic.js/tree/master/translations/sr_SR)
* [Greek](https://github.com/rwaldron/idiomatic.js/tree/master/translations/gr_GR)
* [Hindi](https://github.com/rwaldron/idiomatic.js/tree/master/translations/hi_HI)
* [العربية](https://github.com/rwaldron/idiomatic.js/tree/master/translations/ar_AR)

## محتوى مهم، غير متعلق بالأسلوب الاصطلاحي:


### جودة الكود: أدوات رائعة، موارد ومراجع

 * [JavaScript Plugin](http://docs.codehaus.org/display/SONAR/JavaScript+Plugin) für [Sonar](http://www.sonarsource.org/)
 * [Plato](https://github.com/jsoverson/plato)
 * [jsPerf](http://jsperf.com/)
 * [jsFiddle](http://jsfiddle.net/)
 * [jsbin](http://jsbin.com/)
 * [JavaScript Lint (JSL)](http://javascriptlint.com/)
 * [jshint](http://jshint.com/)
 * [jslint](http://jslint.org/)
 * [Editorconfig](http://editorconfig.org/)

[Leveraging Code Quality Tools by Anton Kovalyov](http://anton.kovalyov.net/slides/gothamjs/)


### التعلم المتقدم

[http://es5.github.com/](http://es5.github.com/)


يجب اعتبار المراجع التالية: 1) غير مكتملة، و 2) قراءة إجبارية. لا أتفق دائماً مع الأسلوب المكتوب من قبل المؤلفين أدناه، لكن شيئاً واحداً مؤكد: إنهم متسقون. علاوة على ذلك، هؤلاء هم سلطات حقيقية في هذه اللغة.

 * [Baseline For Front End Developers](http://rmurphey.com/blog/2012/04/12/a-baseline-for-front-end-developers/)
 * [Eloquent JavaScript](http://eloquentjavascript.net/)
 * [JavaScript, JavaScript](http://javascriptweblog.wordpress.com/)
 * [Adventures in JavaScript Development](http://rmurphey.com/)
 * [Perfection Kills](http://perfectionkills.com/)
 * [Douglas Crockford's Wrrrld Wide Web](http://www.crockford.com)
 * [JS Assessment](https://github.com/rmurphey/js-assessment)

### عملية البناء والنشر


يجب على كل مشروع استخدام مكونات لفحص الكود (lint) واختباره وضغطه للاستخدام في بيئة الإنتاج. بن آلان صمم grunt لهذه المهمة [grunt](https://github.com/cowboy/grunt) وقد حل رسمياً محل مجلد "kits/" في هذا المستودع (Repository).


### أدوات الاختبار


المشاريع يجب أن تحتوي على نوع من اختبارات الوحدة (Unit) أو المرجعية (Reference) أو التنفيذ (Implementation) أو الوظيفية (Functional). العروض التوضيحية لحالات الاستخدام لا تكفي كاختبارات. القائمة أدناه تحتوي على مجموعة من أطر عمل الاختبار المفيدة.

 * [QUnit](http://github.com/jquery/qunit)
 * [Jasmine](https://github.com/pivotal/jasmine)
 * [Vows](https://github.com/cloudhead/vows)
 * [Mocha](https://github.com/visionmedia/mocha)
 * [Hiro](http://hirojs.com/)
 * [JsTestDriver](https://code.google.com/p/js-test-driver/)
 * [Buster.js](http://busterjs.org/)

## فهرس المحتويات

 * [المسافات البيضاء](#whitespace)
 * [الصيغة الجميلة](#spacing)
 * [فحص الأنواع](#type)
 * [التقييم الشرطي](#cond)
 * [الأسلوب العملي](#practical)
 * [التسمية](#naming)
 * [متفرقات](#misc)
 * [الكائنات الأصلية والمضيفة](#native)
 * [التعليقات](#comments)
 * [الكود أحادي اللغة](#language)



------------------------------------------------

## تمهيد


الأقسام التالية تحدد دليل أسلوب معقول لتطوير الجافاسكريبت الحديث وليس الهدف منها أن تكون وصفة طبية. أهم ما يجب استخلاصه هو قانون اتساق الأسلوب. مهما كان الأسلوب الذي تختاره لمشروعك، يجب اعتباره قانوناً.





## بيان الأسلوب الاصطلاحي


1. <a name="whitespace">Whitespace</a>
    - لا تخلط أبداً بين المسافات والتبويبات
    - قبل أن تبدأ مشروعاً وتكتب أي كود، اختر بين المسافات الناعمة (Soft Indents) أو التبويبات الحقيقية.

        - من أجل سهولة القراءة، أنصح بتعيين حجم المسافة البادئة دائماً إلى حرفين. يعني مسافتين تمثلان تبويبة حقيقية.



    - إذا كان محررك يدعم إعداد "إظهار الرموز غير المرئية"، يجب تفعيله. فوائد هذه الممارسة:

        - فرض الاتساق
        - إزالة المسافات البيضاء في نهاية السطر
        - إزالة المسافات البيضاء من الأسطر الفارغة
        - تسهيل قراءة الالتزامات (Commits) والاختلافات (Diffs)

2. <a name="spacing">الصيغة الجميلة</a>

    A. المسافات، الأقواس المجعدة، وفواصل الأسطر

    ```javascript

// if/else/for/while/try تحتوي دائماً على مسافات، أقواس مجعدة
// وتمتد عبر أسطر متعددة
    // Das trägt zur Lesbarkeit bei

## محتوى مهم، غير متعلق بالأسلوب الاصطلاحي:

### جودة الكود: أدوات رائعة، موارد ومراجع

 * [إضافة الجافاسكريبت](http://docs.codehaus.org/display/SONAR/JavaScript+Plugin) لـ [Sonar](http://www.sonarsource.org/)
 * [Plato](https://github.com/jsoverson/plato)
 * [jsPerf](http://jsperf.com/)
 * [jsFiddle](http://jsfiddle.net/)
 * [jsbin](http://jsbin.com/)
 * [JavaScript Lint (JSL)](http://javascriptlint.com/)
 * [jshint](http://jshint.com/)
 * [jslint](http://jslint.org/)
 * [Editorconfig](http://editorconfig.org/)

[الاستفادة من أدوات جودة الكود بقلم أنطون كوفاليوف](http://anton.kovalyov.net/slides/gothamjs/)


### التعلم المتقدم

[http://es5.github.com/](http://es5.github.com/)

يجب اعتبار المراجع التالية: 1) غير مكتملة، و 2) *قراءة إجبارية*. لا أتفق دائماً مع الأسلوب المكتوب من قبل المؤلفين أدناه، لكن شيئاً واحداً مؤكد: إنهم متسقون. علاوة على ذلك، هؤلاء هم سلطات حقيقية في هذه اللغة.

 * [خط الأساس لمطوري الواجهات الأمامية](http://rmurphey.com/blog/2012/04/12/a-baseline-for-front-end-developers/)
 * [الجافاسكريبت البليغة](http://eloquentjavascript.net/)
 * [جافاسكريبت، جافاسكريبت](http://javascriptweblog.wordpress.com/)
 * [مغامرات في تطوير الجافاسكريبت](http://rmurphey.com/)
 * [إتقان القتل](http://perfectionkills.com/)
 * [عالم دوغلاس كروكفورد الواسع](http://www.crockford.com)
 * [تقييم الجافاسكريبت](https://github.com/rmurphey/js-assessment)

### عملية البناء والنشر

يجب على كل مشروع استخدام مكونات لفحص الكود (lint) واختباره وضغطه للاستخدام في بيئة الإنتاج. بن آلان صمم [grunt](https://github.com/cowboy/grunt) لهذه المهمة وقد حل رسمياً محل مجلد "kits/" في هذا المستودع.

### أدوات الاختبار

المشاريع _يجب_ أن تحتوي على نوع من اختبارات الوحدة (Unit) أو المرجعية (Reference) أو التنفيذ (Implementation) أو الوظيفية (Functional). العروض التوضيحية لحالات الاستخدام لا تكفي كاختبارات. القائمة أدناه تحتوي على مجموعة من أطر عمل الاختبار المفيدة.

 * [QUnit](http://github.com/jquery/qunit)
 * [Jasmine](https://github.com/pivotal/jasmine)
 * [Vows](https://github.com/cloudhead/vows)
 * [Mocha](https://github.com/visionmedia/mocha)
 * [Hiro](http://hirojs.com/)
 * [JsTestDriver](https://code.google.com/p/js-test-driver/)
 * [Buster.js](http://busterjs.org/)

## فهرس المحتويات

 * [المسافات البيضاء](#whitespace)
 * [الصيغة الجميلة](#spacing)
 * [فحص الأنواع](#type)
 * [التقييم الشرطي](#cond)
 * [الأسلوب العملي](#practical)
 * [التسمية](#naming)
 * [متفرقات](#misc)
 * [الكائنات الأصلية والمضيفة](#native)
 * [التعليقات](#comments)
 * [الكود أحادي اللغة](#language)



------------------------------------------------

## تمهيد

الأقسام التالية تحدد دليل أسلوب معقول لتطوير الجافاسكريبت الحديث وليس الهدف منها أن تكون وصفة طبية. أهم ما يجب استخلاصه هو **قانون اتساق الأسلوب**. مهما كان الأسلوب الذي تختاره لمشروعك، يجب اعتباره قانوناً.





## بيان الأسلوب الاصطلاحي


1. <a name="whitespace">المسافات البيضاء</a>
    - لا تخلط أبداً بين المسافات والتبويبات
    - قبل أن تبدأ مشروعاً وتكتب أي كود، اختر بين المسافات الناعمة (Soft Indents) أو التبويبات الحقيقية.
        - من أجل سهولة القراءة، أنصح بتعيين حجم المسافة البادئة دائماً إلى حرفين. يعني مسافتين تمثلان تبويبة حقيقية.
    - إذا كان محررك يدعم إعداد "إظهار الرموز غير المرئية"، يجب تفعيله. فوائد هذه الممارسة:
        - فرض الاتساق
        - إزالة المسافات البيضاء في نهاية السطر
        - إزالة المسافات البيضاء من الأسطر الفارغة
        - تسهيل قراءة الالتزامات (Commits) والاختلافات (Diffs)

2. <a name="spacing">الصيغة الجميلة</a>

    أ. المسافات، الأقواس المجعدة، وفواصل الأسطر

    ```javascript

    // if/else/for/while/try تحتوي دائماً على مسافات، أقواس مجعدة
    // وتمتد عبر أسطر متعددة
    // هذا يساهم في سهولة القراءة

    // 2.A.1.1
    // أمثلة على صيغة مكتظة جداً

    if(Condition) doSomething();

    while(condition) iterating++;

    for(var i=0;i<100;i++) someIterativeFn();


    // 2.A.1.1
    // استخدم المسافات البيضاء لتحسين سهولة القراءة

    if ( condition ) {
      // statements
    }

    while ( condition ) {
      // statements
    }

    for ( var i = 0; i < 100; i++ ) {
      // statements
    }

    // أفضل:

    var i,
        length = 100;

    for ( i = 0; i < length; i++ ) {
      // statements
    }

    // أو...

    var i = 0,
        length = 100;

    for ( ; i < length; i++ ) {
      // statements
    }

    var prop;

    for ( prop in object ) {
      // statements
    }

    if ( true ) {
      // statements
    } else {
      // statements
    }
    ```


    ب. التخصيصات، التصريحات، الدوال (المسماة، التعبيرات، المنشئات)




 

  ```javascript

// 2.B.1.1
// المتغيرات
var foo = "bar",
    num = 1,
    undef;

// التعبيرات الحرفية:
var array = [],
    object = {};

// 2.B.1.2
// استخدام `var` واحد فقط لكل نطاق (دالة) يحسن من القابلية للقراءة
// ويحافظ على قائمة التصريحات خالية من التشويش

// سيء
var foo = "";
var bar = "";
var qux;

// جيد
var foo = "",
    bar = "",
    quux;

// أو..
var // تعليق هنا
foo = "",
bar = "",
quux;

// 2.B.1.3
// عبارات var يجب أن تكون دائماً في بداية النطاق المعني (الدالة)
// نفس الشيء ينطبق على const و let من ECMAScript 6

// سيء
function foo() {
  // شيء ما
  var bar = "",
      qux;
}

// جيد
function foo() {
  var bar = "",
      qux;

  // كل العبارات بعد تصريح var
}
    // 2.B.2.1
// تصريح الدالة المسماة
function foo( arg1, argN ) {
}

// الاستخدام
foo( arg1, argN );

// 2.B.2.2
// تصريح الدالة المسماة
function square( number ) {
  return number * number;
}

// الاستخدام
square( 10 );

// أسلوب تمرير الاستمرارية المتكلف حقاً
function square( number, callback ) {
  callback( number * number );
}

square( 10, function( square ) {
  // عبارات callback
});

// 2.B.2.3
// تعبير الدالة
var square = function( number ) {
  // إرجاع شيء قيم ومتعلق
  return number * number;
};

// تعبير الدالة مع المعرف
// هذا الشكل المفضل له القيمة المضافة لكونه
// قادر على استدعاء نفسه وله هوية في تتبع المكدس:
var factorial = function factorial( number ) {
  if ( number < 2 ) {
    return 1;
  }

  return number * factorial( number - 1 );
};

// 2.B.2.4
// تصريح المنشئ
function FooBar( options ) {
  this.options = options;
}

// الاستخدام
var fooBar = new FooBar({ a: "alpha" });

fooBar.options;
// { a: "alpha" }
C. الاستثناءات، الانحرافات الطفيفة

```javascript
// 2.C.1.1
// الدوال مع callbacks
foo(function() {
  // لاحظ عدم وجود مسافة إضافية بين القوس الأول
  // لاستدعاء الدالة المنفذة وكلمة "function"
});

// دالة تقبل مصفوفة، بدون مسافة
foo([ "alpha", "beta" ]);

// 2.C.1.2
// دالة تقبل كائناً، بدون مسافة
foo({
  a: "alpha",
  b: "beta"
});

// حرف string واحد، بدون مسافة
foo("bar");

// أقواس التعبير، بدون مسافة
if ( !("foo" in obj) ) {
  obj = (obj.bar || defaults).baz;
}

    ```

    D. الاتساق يفوز دائماً

في الأقسام 2.A-2.C، نرى الميزة من استخدام المسافات البيضاء والقابلية للقراءة والاتساق.
من المهم دائماً اعتبار تفضيلات التنسيق، مثل المسافات البيضاء داخل الأقواس، كخيارات اختيارية. ومع ذلك، يجب أن يمتد تنسيق واحد بشكل موحد عبر كامل النص المصدري.

```javascript

// 2.D.1.1

if (condition) {
  // statements
}

while (condition) {
  // statements
}

for (var i = 0; i < 100; i++) {
  // statements
}

if (true) {
  // statements
} else {
  // statements
}
    ```

 
E. علامات الاقتباس

سواء كنت تفضل علامات الاقتباس المفردة أو المزدوجة فلا يهم على الإطلاق. الجافاسكريبت يفسرها بنفس الطريقة دائماً. الشيء الوحيد الذي **يجب** الانتباه إليه بالتأكيد هو الاتساق. **لا تخلط أبداً علامات الاقتباس داخل مشروع واحد.** اختر أسلوباً والتزم به.


F. نهايات الأسطر والأسطر الفارغة

المسافات البيضاء يمكن أن تدمر الاختلافات (diffs). يمكن استخدام خطافات ما قبل الالتزام (Pre-Commit-Hooks) لإزالة المسافات البيضاء في نهاية الأسطر والأسطر الفارغة.

3. <a name="type">فحص الأنواع</a>

    A. الأنواع الأولية

    String:

        typeof variable === "string"

    Number:

        typeof variable === "number"

    Boolean:

        typeof variable === "boolean"

    Object:

        typeof variable === "object"

    Array:

        Array.isArray( arrayArtigesObjekt )
                                    (عند الإمكان)    

    Node:

        elem.nodeType === 1

    null:

        variable === null

    null oder undefined:

        variable == null

    undefined:

  المتغيرات العامة:

            typeof variable === "undefined"


    المتغيرات المحلية:

            variable === undefined

            الخصائص:

            object.prop === undefined
            object.hasOwnProperty( prop )
            "prop" in object

 B. الأنواع المُجبرة


لنأخذ التأثيرات التالية...

هذا الـ HTML مُعطى:

    ```html

    <input type="text" id="foo-input" value="1">
    ```

    ```js

    // 3.B.1.1

// `foo` تم تعريفه بالقيمة `0` وهو من النوع `number`
    var foo = 0;

    // typeof foo;
    // "number"
    ...

// لاحقاً في الكود يجب عليك استبدال `foo` بقيمة جديدة من عنصر input
    foo = document.getElementById("foo-input").value;

// إذا كنت تريد الآن الاختبار باستخدام `typeof foo`، ستكون النتيجة `string`
// هذا يعني، إذا كان لديك منطق يختبر `foo` هكذا:

    if ( foo === 1 ) {

        importantFunction();

    }

// `importantFunction()` لن يتم تنفيذها أبداً، حتى لو كان `foo` له القيمة "1"

    // 3.B.1.2

// يمكنك تجنب هذه المشاكل عن طريق إجبار الأنواع باستخدام العمليات الأحادية + أو -:

    foo = +document.getElementById("foo-input").value;
//    ^ العامل الأحادي + يحول المعامل الأيمن إلى رقم (Number)
    // typeof foo;
    // "number"

    if ( foo === 1 ) {

    importantFunction();

    }

// `importantFunction()` سيتم تنفيذها
    ```

هنا بعض الحالات التي تُستخدم فيها الإجبارات:


    ```javascript

    // 3.B.2.1

    var number = 1,
        string = "1",
        bool = false;

    number;
    // 1

    number + "";
    // "1"

    string;
    // "1"

    +string;
    // 1

    +string++;
    // 1

    string;
    // 2

    bool;
    // false

    +bool;
    // 0

    bool + "";
    // "false"
    ```


    ```javascript
    // 3.B.2.2

    var number = 1,
        string = "1",
        bool = true;

    string === number;
    // false

    string === number + "";
    // true

    +string === number;
    // true

    bool === number;
    // false

    +bool === number;
    // true

    bool === string;
    // false

    bool == !!string;
    // true
    ```

    ```javascript
    // 3.B.2.3

    var array = [ "a", "b", "c" ];

    !!~array.indexOf("a");
    // true

    !!~array.indexOf("b");
    // true

    !!~array.indexOf("c");
    // true

    !!~array.indexOf("d");
    // false
    ```

    ```javascript
    // 3.B.2.3


    var num = 2.5;

    parseInt( num, 10 );

// هو نفس...

    ~~num;

    num >> 0;

    num >>> 0;

// يُرجع 2


// تذكر أن الأرقام السالبة تُعامل بشكل مختلف...

    var neg = -2.5;

    parseInt( neg, 10 );

// هو نفس...

    ~~neg;

    neg >> 0;

// يُرجع 2
// ومع ذلك...

    neg >>> 0;

// يُرجع 4294967294


    ```
//**********************************************
4. <a name="cond">التقييم الشرطي</a>

    ```javascript
    //4.1.1
    // عندما تريد فقط فحص ما إذا كان المصفوفة لها طول، ...
    if ( array.length > 0 ) ...

    // افحصها هكذا:
    if ( array.length ) ...


    // 4.1.2
    // عندما تريد فقط فحص ما إذا كانت المصفوفة فارغة...
    if ( array.length === 0 ) ...

    // افعلها بهذه الطريقة:
    if ( !array.length ) ...


    // 4.1.3
    // عندما تريد فحص ما إذا كان النص غير فارغ
    if ( string !== "" ) ...

    // ... افعلها هكذا:
    if ( string ) ...


    // 4.1.4
    // عندما تريد فحص ما إذا كان النص فارغاً...
    if ( string === "" ) ...

    // ... افعلها هكذا:
    if ( !string ) ...


    // 4.1.5
    // عندما تريد فحص ما إذا كانت المرجعية false...
    if ( foo === false ) ...

    // ... استخدم النفي لإجبار تقييم true
    if ( !foo ) ...

    // ... لكن احذر، هذا سيعمل أيضاً مع 0، ""، null، undefined و NaN
    // إذا كان يجب عليك الاختبار لقيمة false منطقية، افعلها هكذا:
    if ( foo === false ) ...

    // 4.1.7
    // عندما تريد فحص مرجعية قد تكون null أو undefined، لكن ليس false...
    if ( foo === null || foo === undefined ) ...

    // ... استفد من ميزة إجبار النوع
    if ( foo == null ) ...

    // تذكر، '==' سيطابق 'null' مع 'null' و 'undefined'، لكن ليس 'false'، "" أو 0
    null == undefined

    ```


5. <a name="practical">الأسلوب العملي</a>

    ```javascript

    // 5.1.1
    // وحدة تطبيقية

    (function( global ) {
      var Module = (function() {

        var data = "secret";

        return {
          // خاصية منطقية Bool
          bool: true,
          // قيمة نصية String
          string: "a string",
          // خاصية مصفوفة Array
          array: [ 1, 2, 3, 4 ],
          // خاصية كائن Object
          object: {
            lang: "en-Us"
          },
          getData: function() {
            // تُرجع قيمة data
            return data;
          },
          setData: function( value ) {
            // تضع قيمة data
            return ( data = value );
          }
        };
      })();

      // هنا يمكن أن تحدث أشياء أخرى

      // جعل الوحدة متاحة في النطاق العام
      global.Module = Module;

    })( this );

    ```

    ```javascript

    // 5.2.1
    // منشئ تطبيقي // A Practical Constructor


    (function( global ) {

      function Ctor( foo ) {

        this.foo = foo;

        return this;
      }

      Ctor.prototype.getFoo = function() {
        return this.foo;
      };

      Ctor.prototype.setFoo = function( val ) {
        return ( this.foo = val );
      };


      // لاستدعاء المنشئ بدون `new`، ربما تفعل شيئاً مثل هذا:
      var ctor = function( foo ) {
        return new Ctor( foo );
      };


      // جعل المنشئ متاحاً في النطاق العام
      global.ctor = ctor;

    })( this );

    ```

6. <a name="naming">التسمية</a>

    أنت لست مُجمِّعاً/مترجماً (compiler)، فلا تحاول أن تكون واحداً.

    الكود التالي مثال على تسمية سيئة بشكل فظيع:

    ```javascript

    // 6.1.1
    // مثال على كود بتسمية سيئة

    function q(s) {
      return document.querySelectorAll(s);
    }
    var i,a=[],els=q("#foo");
    for(i=0;i<els.length;i++){a.push(els[i]);}
    ```

    لقد كتبت بلا شك كوداً مثل هذا من قبل - هذا ينتهي اليوم.

    هنا نفس الكود، لكن أوضح وأكثر تفكيراً ومع بنية قابلة للقراءة:

    ```javascript

    // 6.2.1
    // مثال على كود بتسمية محسنة

    function query( selector ) {
      return document.querySelectorAll( selector );
    }

    var idx = 0,
      elements = [],
      matches = query("#foo"),
      length = matches.length;

    for( ; idx < length; idx++ ){
      elements.push( matches[ idx ] );
    }

    ```

    بعض النقاط الإضافية حول التسمية:

    ```javascript

    // 6.3.1
    // تسمية النصوص

    `dog` هو نص


    // 6.3.2
    // تسمية المصفوفات

    `dogs` هي مصفوفة تتكون من نصوص `dog`


    // 6.3.3
    // تسمية الدوال، الكائنات، المثيلات إلخ

    camelCase; // تصريحات الدوال و var


    // 6.3.4
    // تسمية المنشئات والنماذج الأولية

    PascalCase; // دالة المنشئ


    // 6.3.5
    // تسمية التعبيرات النمطية

    rDesc = //;


    // 6.3.6
    // من دليل أسلوب مكتبة Google Closure

    functionNamesLikeThis;
    variableNamesLikeThis;
    ConstructorNamesLikeThis;
    EnumNamesLikeThis;
    methodNamesLikeThis;
    SYMBOLIC_CONSTANTS_LIKE_THIS;



    ```

7. <a name="misc">متفرقات</a>

    هذا القسم يعرض أفكاراً ومفاهيم يجب ألا تُعتبر عقائدية. الهدف منها تشجيع التساؤل حول الممارسات التي تظهر مراراً وتكراراً في برمجة الجافاسكريبت.

    A. يجب تجنب عبارات `switch`.

    يبدو أن هناك تحسينات قوية في تنفيذ عبارات `switch` في أحدث إصدارات Firefox و Chrome.
    http://jsperf.com/switch-vs-object-literal-vs-module

    https://github.com/rwldrn/idiomatic.js/issues/13

    ```javascript

    // 7.A.1.1
    // مثال على عبارة Switch

    switch( foo ) {
      case "alpha":
        alpha();
        break;
      case "beta":
        beta();
        break;
      default:
        // Fallback
        break;
    }

    // 7.A.1.2
    // من الأفضل استخدام كائن حرفي أو وحدة:

    var switchObj = {
      alpha: function() {
        // statements
        // a return
      },
      beta: function() {
        // statements
        // a return
      },
      _default: function() {
        // statements
        // a return
      }
    };

    var switchModule = (function () {
      return {
        alpha: function() {
          // statements
          // a return
        },
        beta: function() {
          // statements
          // a return
        },
        _default: function() {
          // statements
          // a return
        }
      };
    })();


    // 7.A.1.3
    // إذا كان `foo` خاصية في `switchObj` أو `switchModule`، نفذ هذا الكود هنا..

    ( Object.hasOwnProperty.call( switchObj, foo ) && switchObj[ foo ] || switchObj._default )( args );

    ( Object.hasOwnProperty.call( switchObj, foo ) && switchModule[ foo ] || switchModule._default )( args );

    // إذا كنت تثق في قيم `foo` وتعرف ما بداخلها،
    // يمكنك حذف فحص OR وتنفيذ الكود فقط:

    switchObj[ foo ]( args );

    switchModule[ foo ]( args );

    // هذا النمط يوفر أيضاً إعادة استخدام الكود

    ```

    B. الإرجاع المبكر يجعل الكود أكثر قابلية للقراءة مع فرق أداء طفيف

    ```javascript

    // 7.B.1.1
    // سيء:
    function returnLate( foo ) {
      var ret;

      if ( foo ) {
        ret = "foo";
      } else {
        ret = "quux";
      }
      return ret;
    }

    // جيد:

    function returnEarly( foo ) {

      if ( foo ) {
        return "foo";
      }
      return "quux";
    }

    ```

8. <a name="native">الكائنات الأصلية والمضيفة</a>

    المبدأ الأساسي هنا:

    ### لا تفعل أشياء غير منطقية وكل شيء سيكون بخير.

    لتعزيز هذا المفهوم أكثر، شاهد العرض التقديمي التالي:

    #### “Everything is Permitted: Extending Built-ins” by Andrew Dupont (JSConf2011, Portland, Oregon)

    https://www.youtube.com/watch?v=xL3xCO7CLNM


9. <a name="comments">التعليقات</a>

    * التعليقات متعددة الأسطر جيدة
    * التعليقات في نهاية السطر ممنوعة!
    * تعليقات أسلوب JSDoc جيدة، لكنها تتطلب وقتاً أكثر.


10. <a name="language">الكود أحادي اللغة</a>

    البرامج يجب أن تُكتب باللغة التي يحددها مشرف المشروع، أياً كانت تلك اللغة.

## الملحق

### Comma First.

أي مشروع يستخدم هذا المستند كدليل أسلوب أساسي لا يقبل تنسيق Comma-First، ما لم يُحدد صراحة من قبل مؤلف المشروع.

----------


<a rel="license" href="http://creativecommons.org/licenses/by/3.0/deed.en_US"><img alt="Creative Commons License" style="border-width:0" src="http://i.creativecommons.org/l/by/3.0/80x15.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">Principles of Writing Consistent, Idiomatic JavaScript</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="https://github.com/rwldrn/idiomatic.js" property="cc:attributionName" rel="cc:attributionURL">Rick Waldron and Contributors</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/3.0/deed.en_US">Creative Commons Attribution 3.0 Unported License</a>.<br />Based on a work at <a xmlns:dct="http://purl.org/dc/terms/" href="https://github.com/rwldrn/idiomatic.js" rel="dct:source">github.com/rwldrn/idiomatic.js</a>.
