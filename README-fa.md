[繁中版](./README-tw.md) | [簡中版](./README-zh.md) | [Português (Brasil)](./README-pt_BR.md) | [Français](./README-fr.md) | [한국어](./README-ko.md) | [Nederlands](./README-nl.md) | [Indonesia](./README-id.md) | [ไทย](./README-th.md) | [Русский](./README-ru.md) | [Українська](./README-uk.md) | [Español](./README-es.md) | [Italiano](./README-it.md) | [日本語](./README-ja.md) | [Deutsch](./README-de.md) | [Türkçe](./README-tr.md) | [Tiếng Việt](./README-vi.md) | [Монгол](./README-mn.md) | [हिंदी](./README-hi.md) | [العربية](./README-ar.md) | [Polski](./README-pl.md) | [Македонски](./README-mk.md) | [ລາວ](./README-lo.md) | [Ελληνικά](./README-el.md) | [فارسی](./README-fa.md)
<div dir="rtl">


# چک لیست امنیت API ها
در این صفحه چک لیستی از موارد امنیتی API ها در هنگام طراحی، توسعه، تست و انتشار بررسی شده است.



---

## احراز هویت (Authentication)
- [ ] از احراز هویت پایه (`Basic Auth`) استفاده نکنید، از روش های استاندارد نظیر [JWT](https://jwt.io/), [OAuth](https://oauth.net/) استفاده کنید.
- [ ] چرخ را دوباره اختراع نکنید، از روش های استاندارد احراز هویت (`Authentication`)، تولید توکن (`Token Generation`) و ذخیره کلمه عبور (`Password Storage`) استفاده کنید.
- [ ] از روش های `Max Retry` و محدود کردن تعداد دفعات ورود استفاده کنید.
- [ ] برای تمام داده های حساس از رمزنگاری استفاده کنید. 

## JWT (Json Web Token)
- [ ] از یک کلید تصادفی و پیچیده برای `JWT Secret` استفاده کنید تا حمله `Brute Force` بر روی توکن بسیار سخت شود. 
- [ ] الگوریتم را از طریقه `Payload` باز نکنید، الگوریتم را در سمت `Backend` نگه دارید. (روش‌های رمزنگاری `HS256` و `RS256` پیشنهاد می‌شود)
- [ ] زمان عمر `Token` را (`TTL`, `RTTL`) تا حد امکان کوتاه تنظیم کنید.
- [ ] اطلاعات حساس را در `JWT Payload` ذخیره نکنید، در این حالت به راحتی قابل شکستن است.


</div>
