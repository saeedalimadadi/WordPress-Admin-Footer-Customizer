# WordPress Admin Footer Customizer

This code snippet allows you to **customize the text displayed in the footer of your WordPress admin panel**. By default, this area usually shows "Thank you for creating with WordPress." This customization is particularly useful for web developers, agencies, or site owners who wish to white-label the admin area for clients, provide their own branding, or simply change the default message.

## Why customize the admin footer text?

* **White-Labeling:** Replace the default WordPress branding with your own company's name or a client's branding.
* **Professional Touch:** Adds a custom, professional feel to the admin dashboard.
* **Information/Credit:** Provides a subtle way to include your agency's credit, support information, or a custom message.
* **Consistency:** Maintains brand consistency across all aspects of the website, even in the backend.

## Features

* Replaces the default WordPress admin footer text with a custom message.
* Allows for plain text or HTML content (e.g., links).
* Easy to modify the custom message.

## Installation

There are two primary methods to implement this code:

### Method 1: As a Standalone Plugin (Recommended)

Creating a small, dedicated plugin is the most robust way to add this customization. It ensures your modification remains active regardless of theme changes.

1.  Create a new folder named `wp-admin-footer-text` inside your WordPress site's `wp-content/plugins/` directory.
2.  Inside this new folder, create a file named `wp-admin-footer-text.php`.
3.  Copy and paste the following code into `wp-admin-footer-text.php`:

    ```php
    <?php
    /**
     * Plugin Name: WordPress Admin Footer Customizer
     * Description: Customizes the text displayed in the footer of the WordPress admin panel.
     * Version: 1.0
     * Author: Your Name (Optional)
     * License: GPL-2.0-or-later
     */

    if ( ! defined( 'ABSPATH' ) ) {
        exit; // Exit if accessed directly.
    }

    add_filter(
        'admin_footer_text',
        function ( $footer_text ) {
            // Edit the line below to customize the footer text.
            // You can use plain text or HTML.
            $footer_text = 'Powered by <a href="[https://royanmobtaker.ir](https://royanmobtaker.ir)" target="_blank" rel="noopener">Royan Mobtaker</a>';
            
            return $footer_text;
        }
    );
    ?>
    ```

4.  **Customize the text:** Change the value of `$footer_text` in the code above to your desired message.
5.  Go to your WordPress admin dashboard, navigate to **"Plugins"**, and **activate** the "WordPress Admin Footer Customizer" plugin.

### Method 2: Adding to your Theme's functions.php File

You can add this code directly to your active theme's `functions.php` file. **Before doing so, it's highly recommended to back up your `functions.php` file.**

1.  Navigate to `wp-content/themes/YourThemeName/` (replace `YourThemeName` with the actual name of your active theme).
2.  Open the `functions.php` file.
3.  Add the following code to the end of the file (before the closing `?>` tag, if one exists):

    ```php
    add_filter(
        'admin_footer_text',
        function ( $footer_text ) {
            // Edit the line below to customize the footer text.
            // You can use plain text or HTML.
            $footer_text = 'Powered by <a href="[https://royanmobtaker.ir](https://royanmobtaker.ir)" target="_blank" rel="noopener">Royan Mobtaker</a>';
            
            return $footer_text;
        }
    );
    ```

4.  **Customize the text:** Change the value of `$footer_text` in the code above to your desired message.

## Customization

To change the footer text, simply modify the string assigned to `$footer_text` within the function. You can include HTML tags like `<a>` for links, `<strong>` for bold text, etc.

**Example:**

```php
$footer_text = 'Developed with &hearts; by <a href="[https://yourwebsite.com](https://yourwebsite.com)" target="_blank">Your Company</a>';
```

## Contributing
Contributions are welcome! If you have suggestions or improvements for this code, feel free to open a "Pull Request" or report an "Issue."

## License
This project is licensed under the GPL-2.0-or-later License.

---

# سفارشی‌ساز فوتر پنل مدیریت وردپرس

این قطعه کد به شما امکان می‌دهد تا **متن نمایش داده شده در فوتر (پاورقی) پنل مدیریت وردپرس خود را سفارشی‌سازی کنید**. به طور پیش‌فرض، این قسمت معمولاً "با تشکر از شما برای ایجاد با وردپرس." را نمایش می‌دهد. این سفارشی‌سازی به ویژه برای توسعه‌دهندگان وب، آژانس‌ها یا صاحبان سایت که مایل به سفیدسازی (white-label) ناحیه مدیریت برای مشتریان خود، ارائه برند خود، یا صرفاً تغییر پیام پیش‌فرض هستند، مفید است.

## چرا متن فوتر پنل مدیریت را سفارشی‌سازی کنیم؟

* **سفیدسازی (White-Labeling):** برندینگ پیش‌فرض وردپرس را با نام شرکت خود یا برند مشتری جایگزین کنید.
* **لمس حرفه‌ای:** یک حس سفارشی و حرفه‌ای به داشبورد مدیریت می‌بخشد.
* **اطلاعات/اعتبار:** راهی ظریف برای قرار دادن اعتبار آژانس شما، اطلاعات پشتیبانی یا یک پیام سفارشی فراهم می‌کند.
* **سازگاری:** سازگاری برند را در تمام جنبه‌های وب‌سایت، حتی در بخش پشتی، حفظ می‌کند.

## قابلیت‌ها

* متن پیش‌فرض فوتر پنل مدیریت وردپرس را با یک پیام سفارشی جایگزین می‌کند.
* امکان استفاده از متن ساده یا محتوای HTML (مانند لینک‌ها) را فراهم می‌کند.
* تغییر پیام سفارشی آسان است.

## نصب

برای پیاده‌سازی این کد، دو روش اصلی وجود دارد:

### روش ۱: به عنوان یک افزونه مستقل (توصیه شده)

ایجاد یک افزونه کوچک و اختصاصی، قوی‌ترین راه برای افزودن این قابلیت است. این تضمین می‌کند که تغییر شما صرف‌نظر از تغییر قالب، فعال باقی بماند.

1.  یک پوشه جدید با نام `wp-admin-footer-text` در مسیر `wp-content/plugins/` سایت وردپرسی خود ایجاد کنید.
2.  در داخل این پوشه جدید، یک فایل با نام `wp-admin-footer-text.php` ایجاد کنید.
3.  کد زیر را در `wp-admin-footer-text.php` کپی و جایگذاری کنید:

    ```php
    <?php
    /**
     * Plugin Name: WordPress Admin Footer Customizer
     * Description: Customizes the text displayed in the footer of the WordPress admin panel.
     * Version: 1.0
     * Author: Your Name (Optional)
     * License: GPL-2.0-or-later
     */

    if ( ! defined( 'ABSPATH' ) ) {
        exit; // Exit if accessed directly.
    }

    add_filter(
        'admin_footer_text',
        function ( $footer_text ) {
            // خط زیر را برای سفارشی‌سازی متن فوتر ویرایش کنید.
            // می‌توانید از متن ساده یا HTML استفاده کنید.
            $footer_text = 'قدرت گرفته از <a href="[https://royanmobtaker.ir](https://royanmobtaker.ir)" target="_blank" rel="noopener">رویان مبتکر</a>';
            
            return $footer_text;
        }
    );
    ?>
    ```

4.  **متن را سفارشی‌سازی کنید:** مقدار `$footer_text` را در کد بالا به پیام دلخواه خود تغییر دهید.
5.  وارد پنل مدیریت وردپرس خود شوید، به بخش **"افزونه‌ها"** بروید و افزونه **"سفارشی‌ساز فوتر پنل مدیریت وردپرس"** را **فعال کنید**.

### روش ۲: اضافه کردن به فایل functions.php قالب شما

می‌توانید این کد را مستقیماً به فایل `functions.php` قالب فعال خود اضافه کنید. **پیشنهاد اکید می‌شود قبل از انجام این کار، از فایل `functions.php` خود یک پشتیبان (backup) تهیه کنید.**

1.  به مسیر `wp-content/themes/YourThemeName/` بروید (به جای `YourThemeName` نام واقعی قالب فعال خود را قرار دهید).
2.  فایل `functions.php` را باز کنید.
3.  کد زیر را به انتهای فایل (قبل از تگ بستن `?>`، در صورت وجود) اضافه کنید:

    ```php
    add_filter(
        'admin_footer_text',
        function ( $footer_text ) {
            // خط زیر را برای سفارشی‌سازی متن فوتر ویرایش کنید.
            // می‌توانید از متن ساده یا HTML استفاده کنید.
            $footer_text = 'قدرت گرفته از <a href="[https://royanmobtaker.ir](https://royanmobtaker.ir)" target="_blank" rel="noopener">رویان مبتکر</a>';
            
            return $footer_text;
        }
    );
    ```

4.  **متن را سفارشی‌سازی کنید:** مقدار `$footer_text` را در کد بالا به پیام دلخواه خود تغییر دهید.

## سفارشی‌سازی

برای تغییر متن فوتر، به سادگی رشته اختصاص داده شده به `$footer_text` را در داخل تابع تغییر دهید. می‌توانید تگ‌های HTML مانند `<a>` برای لینک‌ها، `<strong>` برای متن پررنگ و غیره را شامل کنید.

**مثال:**

```php
$footer_text = 'توسعه یافته با &hearts; توسط <a href="[https://yourwebsite.com](https://yourwebsite.com)" target="_blank">شرکت شما</a>';
```

## مشارکت (Contributing)
مشارکت شما خوشایند است! اگر پیشنهاد یا بهبودهایی برای این کد دارید، می‌توانید یک "Pull Request" ایجاد کنید یا "Issue" جدیدی را گزارش دهید.

## مجوز (License)
این پروژه تحت مجوز GPL-2.0-or-later منتشر شده است.
